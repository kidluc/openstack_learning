Openstack HW req:
- Controller: 1-2 CPU, 8GB RAM, 100GB storage, 2 NIC (core component)
=> Run Identity service (Keystone), Image service (Glance), management Compute (Nova), management Networking (Neutron),  various Networking agents, and the dashboard.
=> Atleast 2 network interface and can optional run Block Storage, Object Storage, Orchestration, and Telemetry services.

- Compute: 2-4 CPU, 8+GB RAM, 100+ storage, 2 NIC (core)
=> Run hypervisor (Software that arbitrates and controls VM access to the actual underlying hardware.) operates instances (Default is KVM)
=> Run networking service agents to provides firewalling service instances via security groups (A set of network traffic filtering rules that are applied to a Compute instance.)
=> Can deploy more than 1 compute node

- Block storage (option)
=> Contains the disks Block Storage and Shared File System services provision for instances
=> Make separate storage network to increase performance and security.
=> Can deploy more than 1 compute node. Minimum 1 interface

- Object storage (option)
=> Contain the disks that the Object Storage service uses for storing accounts, containers, and objects.
=> Req: >= 2 nodes. minimum 1 interface

Networking
- Option 1: Provider networks
=> Đơn giản chạy với layer-2 service (bridging/switching) và phân chia VLAN. Bride mạng ảo đến mạng vật lý và dựa vào hạ tầng mạng
vật lý cho các service layer-3 (routing).
=> Yếu điểm là thiếu hỗ trợ với các self-service networks,layer-3 (routing) service ...
![]()
