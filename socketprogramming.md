# SERVER 
```
import socket

def start_server(host='0.0.0.0', port=12345):
    with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as server_socket:
        server_socket.bind((host, port))
        server_socket.listen(1)
        print(f"Server listening on {host}:{port}")
        
        conn, addr = server_socket.accept()
        with conn:
            print(f"Connected by {addr}")
            data = conn.recv(1024).decode('utf-8')
            print(f"Received data: {data}")

if __name__ == "__main__":
    start_server()

```

# CLIENT
```
import socket
import uuid

def get_mac_address():
    mac = ':'.join(['{:02x}'.format((uuid.getnode() >> i) & 0xff) for i in range(0, 8 * 6, 8)][::-1])
    return mac

def get_ip_address():
    with socket.socket(socket.AF_INET, socket.SOCK_DGRAM) as s:
        # Use Google's public DNS server to get the local IP address
        s.connect(("8.8.8.8", 80))
        ip_address = s.getsockname()[0]
    return ip_address

def send_info_to_server(server_host, server_port):
    mac_address = get_mac_address()
    ip_address = get_ip_address()
    data = f"MAC Address: {mac_address}, IP Address: {ip_address}"

    with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as client_socket:
        client_socket.connect((server_host, server_port))
        client_socket.sendall(data.encode('utf-8'))
        print(f"Sent data to server: {data}")

if __name__ == "__main__":
    server_host = '127.0.0.1'  # Change this to the server's IP address
    server_port = 12345
    send_info_to_server(server_host, server_port)
```
