# ssacli-text-file-exporter

This script is a prometheus textfile collector

It's parsing the output of the `ssacli` binary to interpret and cache

## Usage

```
python3 ssacli_exporter.py --output /var/lib/node_exporter/textfile/ssacli.prom
```

## Output

Controller labels are:
* Serial
* Firmware version

Physical disks labels are:
* Box
* Bay
* Port
* Serial

Logical drives labels are:
* Array

```
# HELP hp_smart_array_controller_status Controller status
# TYPE hp_smart_array_controller_status gauge
# HELP hp_smart_array_controller_cache_status Controller Cache Status
# TYPE hp_smart_array_controller_cache_status gauge
# HELP hp_smart_array_controller_cache_size Controller Cache Size in GB
# TYPE hp_smart_array_controller_cache_size gauge
# HELP hp_smart_array_controller_cache_available Controller Cache available in GB
# TYPE hp_smart_array_controller_cache_available gauge
# HELP hp_smart_array_disk_power_on_hours Number of power on hours
# TYPE hp_smart_array_disk_power_on_hours gauge
# HELP hp_smart_array_disk_usage Usage remaining for disk in %
# TYPE hp_smart_array_disk_usage gauge
# HELP hp_smart_array_disk_status Status of physical disk
# TYPE hp_smart_array_disk_status gauge
# HELP hp_smart_array_ld_status Logicial drive status
# TYPE hp_smart_array_ld_status gauge
# HELP hp_smart_array_ld_caching Logicial drive caching
# TYPE hp_smart_array_ld_caching gauge
```