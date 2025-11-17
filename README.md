# Lapres Jarkom Modul 4 Kelompok K-02

| Nama | NRP |
| ---------------------- | ---------- |
| Nadia Kirana Afifah Prahandita | 5027241005 |
| Arya Bisma Putra Refman | 5027241036 |
----

# CIDR
## Topologi
Berikut adalah topologi yang digunakan dalam metode CIDR dengan CPT

<img width="1004" height="426" alt="image" src="https://github.com/user-attachments/assets/62174535-d131-4438-a98a-b8f39777d565" />


## Tree CIDR
Berikut adalah tree yang digunakan dalam metode CIDR dengan CPT
![WhatsApp Image 2025-11-17 at 22 54 12_de7fb05b](https://github.com/user-attachments/assets/cff4f71c-0f7e-4c68-9ab9-921ceb9f74e8)


## Penggabungan IP
### level 1
| Subnet | Gabungan dari 1 | Netmask | Gabungan dari 2 | Netmask | Netmask Akhir |
| ------ | --------------- | ------- | --------------- | ------- | ------------- |
| **B1** | A1              | /23     | A3              | /29     | **/22**       |
| **B2** | A2              | /27     | A4              | /26     | **/25**       |
| **B3** | A19             | /26     | A20             | /29     | **/25**       |
| **B4** | A17             | /22     | A22             | /30     | **/21**       |
| **B5** | A7              | /25     | A11             | /28     | **/24**       |
| **B6** | A13             | /23     | A14             | /23     | **/22**       |

### level 2
| Subnet | Gabungan dari 1 | Netmask | Gabungan dari 2 | Netmask | Netmask Akhir |
| ------ | --------------- | ------- | --------------- | ------- | ------------- |
| **C1** | B1              | /22     | B2              | /25     | **/21**       |
| **C2** | B6              | /22     | A15             | /30     | **/14**       |
| **C3** | B3              | /25     | A18             | /29     | **/24**       |
| **C4** | B5              | /24     | A10             | /30     | **/23**       |

### level 3
| Subnet | Gabungan dari 1 | Netmask | Gabungan dari 2 | Netmask | Netmask Akhir |
| ------ | --------------- | ------- | --------------- | ------- | ------------- |
| **D1** | C3              | /17     | A21             | /30     | **/16**       |
| **D2** | C1              | /21     | A5              | /30     | **/20**       |
| **D3** | C2              | /14     | A16             | /30     | **/13**       |
| **D4** | C4              | /9      | A12             | /22     | **/8**        |

### level 4
| Subnet | Gabungan dari 1 | Netmask | Gabungan dari 2 | Netmask | Netmask Akhir |
| ------ | --------------- | ------- | --------------- | ------- | ------------- |
| **E1** | D1              | /16     | B4              | /21     | **/15**       |
| **E2** | D3              | /13     | D4              | /8      | **/7**        |

### level 5
| Subnet | Gabungan dari 1 | Netmask | Gabungan dari 2 | Netmask | Netmask Akhir |
| ------ | --------------- | ------- | --------------- | ------- | ------------- |
| **F1** | E2              | /7      | A9              | /30     | **/6**        |

### level 6
| Subnet | Gabungan dari 1 | Netmask | Gabungan dari 2 | Netmask | Netmask Akhir |
| ------ | --------------- | ------- | --------------- | ------- | ------------- |
| **G1** | F1              | /6      | A6              | /25     | **/5**        |

### level 7
| Subnet | Gabungan dari 1 | Netmask | Gabungan dari 2 | Netmask | Netmask Akhir |
| ------ | --------------- | ------- | --------------- | ------- | ------------- |
| **H1** | G1              | /5      | A8              | /30     | **/4**        |

### level 8
| Subnet | Gabungan dari 1 | Netmask | Gabungan dari 2 | Netmask | Netmask Akhir |
| ------ | --------------- | ------- | --------------- | ------- | ------------- |
| **I1** | H1              | /4      | J2              | /14     | **/3**        |

### level 9
| Subnet | Gabungan dari 1 | Netmask | Gabungan dari 2 | Netmask | Netmask Akhir |
| ------ | --------------- | ------- | --------------- | ------- | ------------- |
| **J1** | I1              | /3      | D2              | /20     | **/2**        |

## Pembagian IP
| Subnet  | Network ID    | CIDR | Netmask (Desimal) | Broadcast      | Range IP (Host Awal – Host Akhir) |
| ------- | ------------- | ---- | ----------------- | -------------- | --------------------------------- |
| **A1**  | 192.212.0.0   | /30  | 255.255.255.252   | 192.212.0.3    | 192.212.0.1 – 192.212.0.2         |
| **A2**  | 192.212.0.4   | /27  | 255.255.255.224   | 192.212.0.35   | 192.212.0.5 – 192.212.0.34        |
| **A3**  | 192.212.0.36  | /29  | 255.255.255.248   | 192.212.0.43   | 192.212.0.37 – 192.212.0.42       |
| **A4**  | 192.212.0.44  | /26  | 255.255.255.192   | 192.212.0.107  | 192.212.0.45 – 192.212.0.106      |
| **A5**  | 192.212.0.108 | /30  | 255.255.255.252   | 192.212.0.111  | 192.212.0.109 – 192.212.0.110     |
| **A6**  | 192.212.0.112 | /25  | 255.255.255.128   | 192.212.0.239  | 192.212.0.113 – 192.212.0.238     |
| **A7**  | 192.212.1.0   | /25  | 255.255.255.128   | 192.212.1.127  | 192.212.1.1 – 192.212.1.126       |
| **A8**  | 192.212.1.128 | /30  | 255.255.255.252   | 192.212.1.131  | 192.212.1.129 – 192.212.1.130     |
| **A9**  | 192.212.1.132 | /30  | 255.255.255.252   | 192.212.1.135  | 192.212.1.133 – 192.212.1.134     |
| **A10** | 192.212.1.136 | /30  | 255.255.255.252   | 192.212.1.139  | 192.212.1.137 – 192.212.1.138     |
| **A11** | 192.212.1.140 | /28  | 255.255.255.240   | 192.212.1.155  | 192.212.1.141 – 192.212.1.154     |
| **A12** | 192.212.4.0   | /22  | 255.255.252.0     | 192.212.7.255  | 192.212.4.1 – 192.212.7.254       |
| **A13** | 192.212.8.0   | /23  | 255.255.254.0     | 192.212.9.255  | 192.212.8.1 – 192.212.9.254       |
| **A14** | 192.212.10.0  | /23  | 255.255.254.0     | 192.212.11.255 | 192.212.10.1 – 192.212.11.254     |
| **A15** | 192.212.12.0  | /30  | 255.255.255.252   | 192.212.12.3   | 192.212.12.1 – 192.212.12.2       |
| **A16** | 192.212.12.4  | /30  | 255.255.255.252   | 192.212.12.7   | 192.212.12.5 – 192.212.12.6       |
| **A17** | 192.212.16.0  | /22  | 255.255.252.0     | 192.212.19.255 | 192.212.16.1 – 192.212.19.254     |
| **A18** | 192.212.20.0  | /29  | 255.255.255.248   | 192.212.20.7   | 192.212.20.1 – 192.212.20.6       |
| **A19** | 192.212.20.8  | /26  | 255.255.255.192   | 192.212.20.71  | 192.212.20.9 – 192.212.20.70      |
| **A20** | 192.212.20.72 | /29  | 255.255.255.248   | 192.212.20.79  | 192.212.20.73 – 192.212.20.78     |
| **A21** | 192.212.20.80 | /30  | 255.255.255.252   | 192.212.20.83  | 192.212.20.81 – 192.212.20.82     |
| **A22** | 192.212.20.84 | /30  | 255.255.255.252   | 192.212.20.87  | 192.212.20.85 – 192.212.20.86     |

## Subneting
A5 (Router)
```
Interfaces
FastEthernet0/0 (ke Router Pusat)
• IPv4 Address : 192.212.15.202
• Subnet Mask  : 255.255.255.252

FastEthernet0/1 (ke A10)
• IPv4 Address : 192.212.15.213
• Subnet Mask  : 255.255.255.252

FastEthernet1/0 (A12)
• IPv4 Address : 192.212.0.1
• Subnet Mask  : 255.255.252.0

Static Routes
0.0.0.0/0       via 192.212.15.201
192.212.8.0/23  via 192.212.15.214
192.212.10.0/23 via 192.212.15.214
```

A10 (Router)
```
Interfaces
FastEthernet0/0 (ke A5)
• IP : 192.212.15.214
• Mask : 255.255.255.252

FastEthernet0/1 (A13)
• IP : 192.212.8.1
• Mask : 255.255.254.0

FastEthernet1/0 (A14)
• IP : 192.212.10.1
• Mask : 255.255.254.0

Static Route
0.0.0.0/0 via 192.212.15.213
```

A12 (Client)
```
IP Address      : 192.212.0.2
Subnet Mask     : 255.255.252.0
Default Gateway : 192.212.0.1
```

A8 (Router)
```
Interfaces
FastEthernet0/0 (ke Router Pusat)
• IP : 192.212.15.206
• Mask : 255.255.255.252

FastEthernet0/1 (A15)
• IP : 192.212.15.217
• Mask : 255.255.255.252

FastEthernet1/0 (A1)
• IP : 192.212.12.1
• Mask : 255.255.254.0

Static Routes
0.0.0.0/0          via 192.212.15.205
192.212.15.128/27  via 192.212.15.218
192.212.15.220/30  via 192.212.15.218
192.212.14.0/25    via 192.212.15.218
192.212.14.128/25  via 192.212.15.218
```

A15 (Router)
```
Interfaces
FastEthernet0/0 (ke A8)
• IP : 192.212.15.218
• Mask : 255.255.255.252

FastEthernet0/1 (A16)
• IP : 192.212.15.221
• Mask : 255.255.255.252

FastEthernet1/0 (A2)
• IP : 192.212.15.129
• Mask : 255.255.255.224

Static Routes
0.0.0.0/0         via 192.212.15.217
192.212.14.0/25   via 192.212.15.222
192.212.14.128/25 via 192.212.15.222
```

A16 (Router)
```
Interfaces
FastEthernet0/0 (ke A15)
• IP : 192.212.15.222
• Mask : 255.255.255.252

FastEthernet0/1 (A6)
• IP : 192.212.14.1
• Mask : 255.255.255.128

FastEthernet1/0 (A7)
• IP : 192.212.14.129
• Mask : 255.255.255.128

Static Route
0.0.0.0/0 via 192.212.15.221
```

A1 (Client)
```
IP : 192.212.12.2
Mask : 255.255.254.0
Gateway : 192.212.12.1
```

A2 (Client)
```
IP : 192.212.15.130
Mask : 255.255.255.224
Gateway : 192.212.15.129
```

A6 (Client)
```
IP : 192.212.14.2
Mask : 255.255.255.128
Gateway : 192.212.14.1
```

A7 (Client)
```
IP : 192.212.14.130
Mask : 255.255.255.128
Gateway : 192.212.14.129
```

A9 (Router)
```
Interfaces
FastEthernet0/0 : 192.212.15.210 /30
FastEthernet0/1 : 192.212.15.225 /30
FastEthernet1/0 : 192.212.15.233 /30

Static Routes
0.0.0.0/0         via 192.212.15.209
192.212.4.0/22    via 192.212.15.226
192.212.15.176/29 via 192.212.15.226
192.212.15.228/30 via 192.212.15.226
192.212.15.184/29 via 192.212.15.226
192.212.15.160/28 via 192.212.15.234
192.212.15.192/29 via 192.212.15.234
```

A21 (Router)
```
Interfaces
FastEthernet0/0 : 192.212.15.226 /30
FastEthernet0/1 : 192.212.15.229 /30
FastEthernet1/0 : 192.212.4.1 /22

Static Routes
0.0.0.0/0         via 192.212.15.225
192.212.15.176/29 via 192.212.15.230
192.212.15.184/29 via 192.212.15.230
```

A22 (Router)
```
Interfaces
FastEthernet0/0 : 192.212.15.230 /30
FastEthernet0/1 : 192.212.15.177 /29
FastEthernet1/0 : 192.212.15.185 /29

Static Route
0.0.0.0/0 via 192.212.15.229
```

A23 (Router)
```
Interfaces
FastEthernet0/0 : 192.212.15.234 /30
FastEthernet0/1 : 192.212.15.161 /28
FastEthernet1/0 : 192.212.15.193 /29

Static Route
0.0.0.0/0 via 192.212.15.233
```

Client Networks<br>
A11
```
IP : 192.212.15.162
Mask : 255.255.255.240
Gateway : 192.212.15.161
```

A20
```
IP : 192.212.15.194
Mask : 255.255.255.248
Gateway : 192.212.15.193
```

A17
```
IP : 192.212.4.2
Mask : 255.255.252.0
Gateway : 192.212.4.1
```

A18
```
IP : 192.212.15.178
Mask : 255.255.255.248
Gateway : 192.212.15.177
```

A3
```
IP : 192.212.15.186
Mask : 255.255.255.248
Gateway : 192.212.15.185
```

# VLSM
Untuk metode VLSM, kami menggunakan GNS3 sebagai platformnya

## Topologi
Berikut adalah topologi yang digunakan dalam metode VLSM dengan GSN3

<img width="5072" height="2944" alt="image" src="https://github.com/user-attachments/assets/9a6b88f8-e844-409c-9cbe-4b40842d3909" />

## Tree VLSM
Berikut adalah Tree yang digunakan dalam metode VLSM dengan GSN3
<img width="1898" height="1678" alt="TREE FIX" src="https://github.com/user-attachments/assets/5ce1bd33-8cf6-4815-a993-c4c73d8631df" />


## Pembagian IP
| **Nama** | **Network Address** | **Netmask**     | **Broadcast Address** | **Usable IP Range**             |
| -------- | ------------------- | --------------- | --------------------- | ------------------------------- |
| A12      | 192.212.0.0         | 255.255.252.0   | 192.212.3.255         | 192.212.0.1 – 192.212.3.254     |
| A17      | 192.212.4.0         | 255.255.252.0   | 192.212.7.255         | 192.212.4.1 – 192.212.7.254     |
| A13      | 192.212.8.0         | 255.255.254.0   | 192.212.9.255         | 192.212.8.1 – 192.212.9.254     |
| A14      | 192.212.10.0        | 255.255.254.0   | 192.212.11.255        | 192.212.10.1 – 192.212.11.254   |
| A1       | 192.212.12.0        | 255.255.254.0   | 192.212.13.255        | 192.212.12.1 – 192.212.13.254   |
| A6       | 192.212.14.0        | 255.255.255.128 | 192.212.14.127        | 192.212.14.1 – 192.212.14.126   |
| A7       | 192.212.14.128      | 255.255.255.128 | 192.212.14.255        | 192.212.14.129 – 192.212.14.254 |
| A19      | 192.212.15.0        | 255.255.255.192 | 192.212.15.63         | 192.212.15.1 – 192.212.15.62    |
| A4       | 192.212.15.64       | 255.255.255.192 | 192.212.15.127        | 192.212.15.65 – 192.212.15.126  |
| A2       | 192.212.15.128      | 255.255.255.224 | 192.212.15.159        | 192.212.15.129 – 192.212.15.158 |
| A11      | 192.212.15.160      | 255.255.255.240 | 192.212.15.175        | 192.212.15.161 – 192.212.15.174 |
| A18      | 192.212.15.176      | 255.255.255.248 | 192.212.15.183        | 192.212.15.177 – 192.212.15.182 |
| A3       | 192.212.15.184      | 255.255.255.248 | 192.212.15.191        | 192.212.15.185 – 192.212.15.190 |
| A20      | 192.212.15.192      | 255.255.255.248 | 192.212.15.199        | 192.212.15.193 – 192.212.15.198 |
| A5       | 192.212.15.200      | 255.255.255.252 | 192.212.15.203        | 192.212.15.201 – 192.212.15.202 |
| A8       | 192.212.15.204      | 255.255.255.252 | 192.212.15.207        | 192.212.15.205 – 192.212.15.206 |
| A9       | 192.212.15.208      | 255.255.255.252 | 192.212.15.211        | 192.212.15.209 – 192.212.15.210 |
| A10      | 192.212.15.212      | 255.255.255.252 | 192.212.15.215        | 192.212.15.213 – 192.212.15.214 |
| A15      | 192.212.15.216      | 255.255.255.252 | 192.212.15.219        | 192.212.15.217 – 192.212.15.218 |
| A16      | 192.212.15.220      | 255.255.255.252 | 192.212.15.223        | 192.212.15.221 – 192.212.15.222 |
| A21      | 192.212.15.224      | 255.255.255.252 | 192.212.15.227        | 192.212.15.225 – 192.212.15.226 |
| A22      | 192.212.15.228      | 255.255.255.252 | 192.212.15.231        | 192.212.15.229 – 192.212.15.230 |
| A23      | 192.212.15.232      | 255.255.255.252 | 192.212.15.235        | 192.212.15.233 – 192.212.15.234 |

## Config Node
A5 (Router)
```
# Ke Router Pusat
auto eth0
iface eth0 inet static
    address 192.212.15.202
    netmask 255.255.255.252
    gateway 192.212.15.201

# A10
auto eth1
iface eth1 inet static
    address 192.212.15.213
    netmask 255.255.255.252

# A12
auto eth2
iface eth2 inet static
    address 192.212.0.1
    netmask 255.255.252.0
```

A10 (Router)
```
# A5
auto eth0
iface eth0 inet static
    address 192.212.15.214
    netmask 255.255.255.252
    gateway 192.212.15.213

# A13
auto eth1
iface eth1 inet static
    address 192.212.8.1
    netmask 255.255.254.0

# A14
auto eth2
iface eth2 inet static
    address 192.212.10.1
    netmask 255.255.254.0
```

A8 (Router)
```
# Ke Router Pusat
auto eth0
iface eth0 inet static
    address 192.212.15.206
    netmask 255.255.255.252
    gateway 192.212.15.205

# A15
auto eth1
iface eth1 inet static
    address 192.212.15.217
    netmask 255.255.255.252

# A1
auto eth2
iface eth2 inet static
    address 192.212.12.1
    netmask 255.255.254.0
```

A15 (Router)
```
# A8
auto eth0
iface eth0 inet static
    address 192.212.15.218
    netmask 255.255.255.252
    gateway 192.212.15.217

# A16
auto eth1
iface eth1 inet static
    address 192.212.15.221
    netmask 255.255.255.252

# A2
auto eth2
iface eth2 inet static
    address 192.212.15.129
    netmask 255.255.255.224
```

A16 (Router)
```
# A15
auto eth0
iface eth0 inet static
    address 192.212.15.222
    netmask 255.255.255.252
    gateway 192.212.15.221

# A6
auto eth1
iface eth1 inet static
    address 192.212.14.1
    netmask 255.255.255.128

# A7
auto eth2
iface eth2 inet static
    address 192.212.14.129
    netmask 255.255.255.128
```

A9 (Router)
```
# Ke Router Pusat
auto eth0
iface eth0 inet static
    address 192.212.15.210
    netmask 255.255.255.252
    gateway 192.212.15.209

# A21
auto eth1
iface eth1 inet static
    address 192.212.15.225
    netmask 255.255.255.252

# A17
auto eth2
iface eth2 inet static
    address 192.212.4.1
    netmask 255.255.252.0
```

A21 (Router)
```
# A9
auto eth0
iface eth0 inet static
    address 192.212.15.226
    netmask 255.255.255.252
    gateway 192.212.15.225

# A22
auto eth1
iface eth1 inet static
    address 192.212.15.229
    netmask 255.255.255.252

# A18
auto eth2
iface eth2 inet static
    address 192.212.15.177
    netmask 255.255.255.248
```

A22 (Router)
```
# A21
auto eth0
iface eth0 inet static
    address 192.212.15.230
    netmask 255.255.255.252
    gateway 192.212.15.229

# A23
auto eth1
iface eth1 inet static
    address 192.212.15.233
    netmask 255.255.255.252

# A3
auto eth2
iface eth2 inet static
    address 192.212.15.185
    netmask 255.255.255.248
```
     
A23 (Router)
```
# A22
auto eth0
iface eth0 inet static
    address 192.212.15.234
    netmask 255.255.255.252
    gateway 192.212.15.233

# A11
auto eth1
iface eth1 inet static
    address 192.212.15.161
    netmask 255.255.255.240

# A20
auto eth2
iface eth2 inet static
    address 192.212.15.193
    netmask 255.255.255.248
```

A4 (Router)
```
# A19
auto eth1
iface eth1 inet static
    address 192.212.15.1
    netmask 255.255.255.192

# A4 Client
auto eth2
iface eth2 inet static
    address 192.212.15.65
    netmask 255.255.255.192
```

Router Pusat
```
# A5
auto eth0
iface eth0 inet static
    address 192.212.15.201
    netmask 255.255.255.252

# A8
auto eth1
iface eth1 inet static
    address 192.212.15.205
    netmask 255.255.255.252

# A9
auto eth2
iface eth2 inet static
    address 192.212.15.209
    netmask 255.255.255.252
```

Client Configuration<br>
Client A12
```
auto eth0
iface eth0 inet static
    address 192.212.0.2
    netmask 255.255.252.0
    gateway 192.212.0.1
```
    
Client A13
```
auto eth0
iface eth0 inet static
    address 192.212.8.2
    netmask 255.255.254.0
    gateway 192.212.8.1
```

Client A14
```
auto eth0
iface eth0 inet static
    address 192.212.10.2
    netmask 255.255.254.0
    gateway 192.212.10.1
```

Client A1
```
auto eth0
iface eth0 inet static
    address 192.212.12.2
    netmask 255.255.254.0
    gateway 192.212.12.1
```

Client A2
```
auto eth0
iface eth0 inet static
    address 192.212.15.130
    netmask 255.255.255.224
    gateway 192.212.15.129
```

Client A6
```
auto eth0
iface eth0 inet static
    address 192.212.14.2
    netmask 255.255.255.128
    gateway 192.212.14.1
```
Client A7
```
auto eth0
iface eth0 inet static
    address 192.212.14.130
    netmask 255.255.255.128
    gateway 192.212.14.129
```

Client A17
```
auto eth0
iface eth0 inet static
    address 192.212.4.2
    netmask 255.255.252.0
    gateway 192.212.4.1
```

Client A18
```
auto eth0
iface eth0 inet static
    address 192.212.15.178
    netmask 255.255.255.248
    gateway 192.212.15.177
```

Client A3
```
auto eth0
iface eth0 inet static
    address 192.212.15.186
    netmask 255.255.255.248
    gateway 192.212.15.185
```

Client A11
```
auto eth0
iface eth0 inet static
    address 192.212.15.162
    netmask 255.255.255.240
    gateway 192.212.15.161
```

Client A20
```
auto eth0
iface eth0 inet static
    address 192.212.15.194
    netmask 255.255.255.248
    gateway 192.212.15.193
```

Client A4
```
auto eth0
iface eth0 inet static
    address 192.212.15.66
    netmask 255.255.255.192
    gateway 192.212.15.65
```

Client A19
```
auto eth0
iface eth0 inet static
    address 192.212.15.2
    netmask 255.255.255.192
    gateway 192.212.15.1
```
    
## Routing
Router Pusat
```
# Routing ke A5 dan subnet di bawahnya
post-up route add -net 192.212.0.0 netmask 255.255.252.0 gw 192.212.15.202    # A12
post-up route add -net 192.212.15.212 netmask 255.255.255.252 gw 192.212.15.202  # A10
post-up route add -net 192.212.8.0 netmask 255.255.254.0 gw 192.212.15.202    # A13
post-up route add -net 192.212.10.0 netmask 255.255.254.0 gw 192.212.15.202   # A14

# Routing ke A8 dan subnet di bawahnya
post-up route add -net 192.212.12.0 netmask 255.255.254.0 gw 192.212.15.206   # A1
post-up route add -net 192.212.15.216 netmask 255.255.255.252 gw 192.212.15.206  # A15
post-up route add -net 192.212.15.128 netmask 255.255.255.224 gw 192.212.15.206  # A2
post-up route add -net 192.212.15.220 netmask 255.255.255.252 gw 192.212.15.206  # A16
post-up route add -net 192.212.14.0 netmask 255.255.255.128 gw 192.212.15.206  # A6
post-up route add -net 192.212.14.128 netmask 255.255.255.128 gw 192.212.15.206  # A7

# Routing ke A9 dan subnet di bawahnya
post-up route add -net 192.212.4.0 netmask 255.255.252.0 gw 192.212.15.210    # A17
post-up route add -net 192.212.15.224 netmask 255.255.255.252 gw 192.212.15.210  # A21
post-up route add -net 192.212.15.176 netmask 255.255.255.248 gw 192.212.15.210  # A18
post-up route add -net 192.212.15.228 netmask 255.255.255.252 gw 192.212.15.210  # A22
post-up route add -net 192.212.15.184 netmask 255.255.255.248 gw 192.212.15.210  # A3
post-up route add -net 192.212.15.232 netmask 255.255.255.252 gw 192.212.15.210  # A23
post-up route add -net 192.212.15.160 netmask 255.255.255.240 gw 192.212.15.210  # A11
post-up route add -net 192.212.15.192 netmask 255.255.255.248 gw 192.212.15.210  # A20
```

A5
```
# Default route
post-up route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.15.201

# Routing ke A10
post-up route add -net 192.212.8.0 netmask 255.255.254.0 gw 192.212.15.214    # A13
post-up route add -net 192.212.10.0 netmask 255.255.254.0 gw 192.212.15.214   # A14
```

A10
```
# Default route
post-up route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.15.213
```
A8
```
# Default route
post-up route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.15.205

# Routing ke A15 dan subnet di bawahnya
post-up route add -net 192.212.15.128 netmask 255.255.255.224 gw 192.212.15.218  # A2
post-up route add -net 192.212.15.220 netmask 255.255.255.252 gw 192.212.15.218  # A16
post-up route add -net 192.212.14.0 netmask 255.255.255.128 gw 192.212.15.218  # A6
post-up route add -net 192.212.14.128 netmask 255.255.255.128 gw 192.212.15.218  # A7
```

A15
```
# Default route
post-up route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.15.217

# Routing ke A16
post-up route add -net 192.212.14.0 netmask 255.255.255.128 gw 192.212.15.222   # A6
post-up route add -net 192.212.14.128 netmask 255.255.255.128 gw 192.212.15.222  # A7
```

A16
```
# Default route
post-up route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.15.221
```
A9
```
# Default route
post-up route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.15.209

# Routing ke A21 dan subnet di bawahnya
post-up route add -net 192.212.15.176 netmask 255.255.255.248 gw 192.212.15.226  # A18
post-up route add -net 192.212.15.228 netmask 255.255.255.252 gw 192.212.15.226  # A22
post-up route add -net 192.212.15.184 netmask 255.255.255.248 gw 192.212.15.226  # A3
post-up route add -net 192.212.15.232 netmask 255.255.255.252 gw 192.212.15.226  # A23
post-up route add -net 192.212.15.160 netmask 255.255.255.240 gw 192.212.15.226  # A11
post-up route add -net 192.212.15.192 netmask 255.255.255.248 gw 192.212.15.226  # A20
```

A21
```
# Default route
post-up route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.15.225

# Routing ke A22 dan subnet di bawahnya
post-up route add -net 192.212.15.184 netmask 255.255.255.248 gw 192.212.15.230  # A3
post-up route add -net 192.212.15.232 netmask 255.255.255.252 gw 192.212.15.230  # A23
post-up route add -net 192.212.15.160 netmask 255.255.255.240 gw 192.212.15.230  # A11
post-up route add -net 192.212.15.192 netmask 255.255.255.248 gw 192.212.15.230  # A20
```

A22
```
# Default route
post-up route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.15.229

# Routing ke A23
post-up route add -net 192.212.15.160 netmask 255.255.255.240 gw 192.212.15.234  # A11
post-up route add -net 192.212.15.192 netmask 255.255.255.248 gw 192.212.15.234  # A20
```

A23
```
# Default route
post-up route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.212.15.233
```




