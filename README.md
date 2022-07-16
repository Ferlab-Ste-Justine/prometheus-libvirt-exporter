# prometheus-libvirt-exporter

Libvirt prometheus exporter for host and vm metrics.

By default, this exporter exposes metrics on the TCP port **9000** at the Path **/metrics**. 

# Usage

Run the binary with the **--help** flag to see the customization options.

# Exported Metrics

```
# HELP libvirt_domain_block_capacity_bytes Maximum capacity of the block device, in bytes.
# TYPE libvirt_domain_block_capacity_bytes gauge
libvirt_domain_block_capacity_bytes{domain, host, instance_id, instance_name, flavor_name, project_id, project_name, user_id, user_name, pool, volume, source_file, target_device}

# HELP libvirt_domain_block_allocation_bytes Size allocation on the block device, in bytes.
# TYPE libvirt_domain_block_allocation_bytes gauge
libvirt_domain_block_allocation_bytes{domain, host, instance_id, instance_name, flavor_name, project_id, project_name, user_id, user_name, pool, volume, source_file, target_device}

# HELP libvirt_domain_block_read_bytes_total Number of bytes read from a block device, in bytes.
# TYPE libvirt_domain_block_read_bytes_total counter
libvirt_domain_block_read_bytes_total{domain, host, instance_id, instance_name, flavor_name, project_id, project_name, user_id, user_name, pool, volume, source_file, target_device}

# HELP libvirt_domain_block_read_requests_total Number of read requests from a block device.
# TYPE libvirt_domain_block_read_requests_total counter
libvirt_domain_block_read_requests_total{domain, host, instance_id, instance_name, flavor_name, project_id, project_name, user_id, user_name, pool, volume, source_file, target_device}

# HELP libvirt_domain_block_write_bytes_total Number of bytes written from a block device, in bytes.
# TYPE libvirt_domain_block_write_bytes_total counter
libvirt_domain_block_write_bytes_total{domain, host, instance_id, instance_name, flavor_name, project_id, project_name, user_id, user_name, pool, volume, source_file, target_device}

# HELP libvirt_domain_block_write_requests_total Number of write requests from a block device.
# TYPE libvirt_domain_block_write_requests_total counter
libvirt_domain_block_write_requests_total{domain, host, instance_id, instance_name, flavor_name, project_id, project_name, user_id, user_name, pool, volume, source_file, target_device}

# HELP libvirt_domain_interface_receive_bytes_total Number of bytes received on a network interface, in bytes.
# TYPE libvirt_domain_interface_receive_bytes_total counter
libvirt_domain_interface_receive_bytes_total{domain, host, instance_id,  instance_name, flavor_name, project_id, project_name, source_bridge, target_device, user_id, user_name}

# HELP libvirt_domain_interface_receive_drops_total Number of packet receive drops on a network interface.
# TYPE libvirt_domain_interface_receive_drops_total counter
libvirt_domain_interface_receive_drops_total{domain, host, instance_id,  instance_name, flavor_name, project_id, project_name, source_bridge, target_device, user_id, user_name}

# HELP libvirt_domain_interface_receive_errors_total Number of packet receive errors on a network interface.
# TYPE libvirt_domain_interface_receive_errors_total counter
libvirt_domain_interface_receive_errors_total{domain, host, instance_id,  instance_name, flavor_name, project_id, project_name, source_bridge, target_device, user_id, user_name}

# HELP libvirt_domain_interface_receive_packets_total Number of packets received on a network interface.
# TYPE libvirt_domain_interface_receive_packets_total counter
libvirt_domain_interface_receive_packets_total{domain, host, instance_id,  instance_name, flavor_name, project_id, project_name, source_bridge, target_device, user_id, user_name}

# HELP libvirt_domain_interface_transmit_bytes_total Number of bytes transmitted on a network interface, in bytes.
# TYPE libvirt_domain_interface_transmit_bytes_total counter
libvirt_domain_interface_transmit_bytes_total{domain, host, instance_id,  instance_name, flavor_name, project_id, project_name, source_bridge, target_device, user_id, user_name}

# HELP libvirt_domain_interface_transmit_drops_total Number of packet transmit drops on a network interface.
# TYPE libvirt_domain_interface_transmit_drops_total counter
libvirt_domain_interface_transmit_drops_total{domain, host, instance_id,  instance_name, flavor_name, project_id, project_name, source_bridge, target_device, user_id, user_name}

# HELP libvirt_domain_interface_transmit_errors_total Number of packet transmit errors on a network interface.
# TYPE libvirt_domain_interface_transmit_errors_total counter
libvirt_domain_interface_transmit_errors_total{domain, host, instance_id,  instance_name, flavor_name, project_id, project_name, source_bridge, target_device, user_id, user_name}

# HELP libvirt_domain_interface_transmit_packets_total Number of packets transmitted on a network interface.
# TYPE libvirt_domain_interface_transmit_packets_total counter
libvirt_domain_interface_transmit_packets_total{domain, host, instance_id,  instance_name, flavor_name, project_id, project_name, source_bridge, target_device, user_id, user_name}

# HELP libvirt_domain_cpu_time_seconds_total Amount of CPU time used by the domain, in seconds.
# TYPE libvirt_domain_cpu_time_seconds_total counter
libvirt_domain_cpu_time_seconds_total{domain, host, instance_id, instance_name, flavor_name, project_id, project_name, user_id, user_name}

# HELP libvirt_domain_maximum_memory_bytes Maximum allowed memory of the domain, in bytes.
# TYPE libvirt_domain_maximum_memory_bytes gauge
libvirt_domain_maximum_memory_bytes{domain, host, instance_id, instance_name, flavor_name, project_id, project_name, user_id, user_name}

# HELP libvirt_domain_memory_available_bytes Memory available of the domain, in bytes.
# TYPE libvirt_domain_memory_available_bytes gauge
libvirt_domain_memory_available_bytes{domain, host, instance_id, instance_name, flavor_name, project_id, project_name, user_id, user_name}

# HELP libvirt_domain_memory_rss_bytes Resident Set Size of the process running the domain, in bytes.
# TYPE libvirt_domain_memory_rss_bytes gauge
libvirt_domain_memory_rss_bytes{domain, host, instance_id, instance_name, flavor_name, project_id, project_name, user_id, user_name}

# HELP libvirt_domain_memory_swap_in_bytes Memory swap in of domain(the total amount of data read from swap space), in bytes.
# TYPE libvirt_domain_memory_swap_in_bytes gauge
libvirt_domain_memory_swap_in_bytes{domain, host, instance_id, instance_name, flavor_name, project_id, project_name, user_id, user_name}

# HELP libvirt_domain_memory_swap_out_bytes Memory swap out of the domain(the total amount of memory written out to swap space), in bytes.
# TYPE libvirt_domain_memory_swap_out_bytes gauge
libvirt_domain_memory_swap_out_bytes{domain, host, instance_id, instance_name, flavor_name, project_id, project_name, user_id, user_name}

# HELP libvirt_domain_memory_unused_bytes Memory unused of the domain, in bytes.
# TYPE libvirt_domain_memory_unused_bytes gauge
libvirt_domain_memory_unused_bytes{domain, host, instance_id, instance_name, flavor_name, project_id, project_name, user_id, user_name}

# HELP libvirt_domain_memory_usable_bytes Memory usable of the domain(corresponds to 'Available' in /proc/meminfo), in bytes.
# TYPE libvirt_domain_memory_usable_bytes gauge
libvirt_domain_memory_usable_bytes{domain, host, instance_id, instance_name, flavor_name, project_id, project_name, user_id, user_name}

# HELP libvirt_domain_memory_usage_bytes Memory usage of the domain, in bytes.
# TYPE libvirt_domain_memory_usage_bytes gauge
libvirt_domain_memory_usage_bytes{domain, host, instance_id, instance_name, flavor_name, project_id, project_name, user_id, user_name}

# HELP libvirt_domain_state_code Code of the domain state
# TYPE libvirt_domain_state_code gauge
libvirt_domain_state_code{domain, host, instance_id, instance_name, flavor_name, project_id, project_name, user_id, user_name, state_desc}

# HELP libvirt_domain_virtual_cpus Number of virtual CPUs for the domain.
# TYPE libvirt_domain_virtual_cpus gauge
libvirt_domain_virtual_cpus{domain, host, instance_id, instance_name, flavor_name, project_id, project_name, user_id, user_name}

# HELP libvirt_domains_number Number of the domain
# TYPE libvirt_domains_number gauge
libvirt_domains_number{host}

# HELP libvirt_up Whether scraping libvirt's metrics was successful.
# TYPE libvirt_up gauge
libvirt_up{host}
```