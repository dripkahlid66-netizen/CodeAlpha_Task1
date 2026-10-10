# CodeAlpha_Task1
[packet_sniffer.py.txt]
(https://github.com/user-attachments/files/33282492/packet_sniffer.py.txt)
packet_sniffer.py

#!/usr/bin/env python3
"""
Basic Network Sniffer - CodeAlpha Task 1
Captures and analyzes network packets
"""

from scapy.all import sniff, IP, TCP, UDP, ICMP
from datetime import datetime

packet_count = 0

def analyze_packet(packet):
    global packet_count
    packet_count += 1
    
    print("\n" + "="*70)
    print(f"PACKET #{packet_count} - {datetime.now().strftime('%H:%M:%S')}")
    print("="*70)
    
    if packet.haslayer(IP):
        ip_layer = packet[IP]
        print(f"\n[IP LAYER]")
        print(f"  Source IP: {ip_layer.src}")
        print(f"  Destination IP: {ip_layer.dst}")
        print(f"  Protocol: {ip_layer.proto}")
        print(f"  TTL: {ip_layer.ttl}")
        
        if packet.haslayer(TCP):
            tcp_layer = packet[TCP]
            print(f"\n[TCP LAYER]")
            print(f"  Source Port: {tcp_layer.sport}")
            print(f"  Destination Port: {tcp_layer.dport}")
            
        elif packet.haslayer(UDP):
            udp_layer = packet[UDP]
            print(f"\n[UDP LAYER]")
            print(f"  Source Port: {udp_layer.sport}")
            print(f"  Destination Port: {udp_layer.dport}")
            
        elif packet.haslayer(ICMP):
            icmp_layer = packet[ICMP]
            print(f"\n[ICMP LAYER]")
            print(f"  Type: {icmp_layer.type}")
            print(f"  Code: {icmp_layer.code}")

def start_sniffer():
    print("\n" + "*"*70)
    print("NETWORK PACKET SNIFFER - CodeAlpha Task 1")
    print("*"*70)
    print("\nStarting packet capture...")
    print("Press Ctrl+C to stop\n")
    
    try:
        sniff(prn=analyze_packet, store=False)
    except PermissionError:
        print("\n[ERROR] This program needs root/sudo permissions!")
    except KeyboardInterrupt:
        print(f"\n\nTotal packets: {packet_count}\n")

if __name__ == "__main__":
    start_sniffer()
