# prometheus-libvirt-exporter

prometheus-libvirt-exporter for host and vm metrics exposed for prometheus, written in Go with pluggable metric collectors.

By default, this exporter exposes metrics on the TCP port **9000** at the Path **/metrics**. 

# Usage

Run the binary with the **--help** flag to see the customization options.

# Metrics Labels

The domain metrics all contain the following base labels:
- **domain**
- **flavorName**
- **host**
- **instanceId**
- **instanceName**
- **projectId**
- **projectName**
- **userId**
- **userName**

The block metrics contain the following additional labels:
- **pool**
- **volume**
- **source_file**
- **target_device**

The network interface metrics contain the following additional labels:
- **source_bridge**
- **target_device**

## metrics
Name | Label |Description
---------|---------|-------------
up|"host"|scraping libvirt's metrics state
domains_number|"host"|get number of domains
domain_state_code|"domain", "instanceName", "instanceId", "flavorName", "userName", "userId", "projectName", "projectId", "stateDesc", "host"|code of the domain state,include state description
maximum_memory_bytes|"domain", "instanceName", "instanceId", "flavorName", "userName", "userId", "projectName", "projectId", "host"|Maximum allowed memory of the domain, in bytes
memory_usage_bytes|"domain", "instanceName", "instanceId", "flavorName", "userName", "userId", "projectName", "projectId", "host"|Memory usage of the domain, in bytes
virtual_cpus|"domain", "instanceName", "instanceId", "flavorName", "userName", "userId", "projectName", "projectId", "host"|Number of virtual CPUs for the domain
cpu_time_seconds_total|"domain", "instanceName", "instanceId", "flavorName", "userName", "userId", "projectName", "projectId", "host"|Amount of CPU time used by the domain, in seconds
read_bytes_total|"domain", "instanceName", "instanceId", "flavorName", "userName", "userId", "projectName", "projectId", "source_file", "target_device", "host"|Number of bytes read from a block device, in bytes
read_requests_total|"domain", "instanceName", "instanceId", "flavorName", "userName", "userId", "projectName", "projectId", "source_file", "target_device", "host"|Number of read requests from a block device
write_bytes_total|"domain", "instanceName", "instanceId", "flavorName", "userName", "userId", "projectName", "projectId", "source_file", "target_device", "host"|Number of bytes written from a block device, in bytes
write_requests_total|"domain", "instanceName", "instanceId", "flavorName", "userName", "userId", "projectName", "projectId", "source_file", "target_device", "host"|Number of write requests from a block device
receive_bytes_total|"domain", "instanceName", "instanceId", "flavorName", "userName", "userId", "projectName", "projectId", "source_bridge", "target_device", "host"|Number of bytes received on a network interface, in bytes
receive_packets_total|"domain", "instanceName", "instanceId", "flavorName", "userName", "userId", "projectName", "projectId", "source_bridge", "target_device", "host"|Number of packets received on a network interface
receive_errors_total|"domain", "instanceName", "instanceId", "flavorName", "userName", "userId", "projectName", "projectId", "source_bridge", "target_device", "host"|Number of packet receive errors on a network interface
receive_drops_total|"domain", "instanceName", "instanceId", "flavorName", "userName", "userId", "projectName", "projectId", "source_bridge", "target_device", "host"|Number of packet receive drops on a network interface
transmit_bytes_total|"domain", "instanceName", "instanceId", "flavorName", "userName", "userId", "projectName", "projectId", "source_bridge", "target_device", "host"|Number of bytes transmitted on a network interface, in bytes
transmit_packets_total|"domain", "instanceName", "instanceId", "flavorName", "userName", "userId", "projectName", "projectId", "source_bridge", "target_device", "host"|Number of packets transmitted on a network interface
transmit_errors_total|"domain", "instanceName", "instanceId", "flavorName", "userName", "userId", "projectName", "projectId", "source_bridge", "target_device", "host"|Number of packet transmit errors on a network interface
transmit_drops_total|"domain", "instanceName", "instanceId", "flavorName", "userName", "userId", "projectName", "projectId", "source_bridge", "target_device", "host"|Number of packet transmit drops on a network interface