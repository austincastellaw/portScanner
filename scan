import socket


def scan_port(target_host, target_port):
    try:
        # Create a socket object
        sock = socket.socket(
            socket.AF_INET, socket.SOCK_STREAM
        )  # AF_INET (IPv4) SOCK_STREAM (for TCP)

        # Set a timeout for the connection attempt (in seconds)
        sock.settimeout(2)

        # Attempt to connect to the target host and port
        sock.connect((target_host, target_port))

        print(f"Port {target_port} is open")
        sock.close()
    except:
        print(f"Port {target_port} is closed")


def main():
    target_host = "172.217.7.206"  # Google's IP address
    target_ports = [
        80,
        443,
        22,
        21,
        25,
        53,
        143,
        3306,
    ]  # Ports to scan: 80 (HTTP), 443 (HTTPS), 22 (SSH), 21 (FTP), 25 (SMTP), 53 (DNS), 3306 (MySQL)

    for port in target_ports:
        scan_port(target_host, port)


if __name__ == "__main__":
    main()
