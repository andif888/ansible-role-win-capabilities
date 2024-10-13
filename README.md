# ansible-role-win-capabilities

Role to manage windows capabilities.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [win_capability_add_list](#win_capability_add_list)
  - [win_capability_delete_list](#win_capability_delete_list)
  - [win_capability_download_dir](#win_capability_download_dir)
  - [win_capability_download_filename](#win_capability_download_filename)
  - [win_capability_iso_relative_source_path](#win_capability_iso_relative_source_path)
  - [win_capability_iso_url](#win_capability_iso_url)
  - [win_capability_isos_remove_when_finished](#win_capability_isos_remove_when_finished)
  - [win_capability_post_reboot_delay](#win_capability_post_reboot_delay)
  - [win_capability_pre_reboot_delay](#win_capability_pre_reboot_delay)
  - [win_capability_reboot_when_required](#win_capability_reboot_when_required)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.1`

## Default Variables

### win_capability_add_list

List of windows capabilities to install

#### Default value

```YAML
win_capability_add_list: []
```

#### Example usage

```YAML
win_capability_add_list:
  - "Rsat.ActiveDirectory.DS-LDS.Tools~~~~0.0.1.0"
  - "Rsat.BitLocker.Recovery.Tools~~~~0.0.1.0"
  - "Rsat.CertificateServices.Tools~~~~0.0.1.0"
  - "Rsat.DHCP.Tools~~~~0.0.1.0"
  - "Rsat.Dns.Tools~~~~0.0.1.0"
  - "Rsat.FailoverCluster.Management.Tools~~~~0.0.1.0"
  - "Rsat.FileServices.Tools~~~~0.0.1.0"
  - "Rsat.GroupPolicy.Management.Tools~~~~0.0.1.0"
  - "Rsat.IPAM.Client.Tools~~~~0.0.1.0"
  - "Rsat.LLDP.Tools~~~~0.0.1.0"
  - "Rsat.NetworkController.Tools~~~~0.0.1.0"
  - "Rsat.NetworkLoadBalancing.Tools~~~~0.0.1.0"
  - "Rsat.RemoteAccess.Management.Tools~~~~0.0.1.0"
  - "Rsat.RemoteDesktop.Services.Tools~~~~0.0.1.0"
  - "Rsat.ServerManager.Tools~~~~0.0.1.0"
  - "Rsat.StorageMigrationService.Management.Tools~~~~0.0.1.0"
  - "Rsat.StorageReplica.Tools~~~~0.0.1.0"
  - "Rsat.SystemInsights.Management.Tools~~~~0.0.1.0"
  - "Rsat.VolumeActivation.Tools~~~~0.0.1.0"
  - "Rsat.WSUS.Tools~~~~0.0.1.0"
```

### win_capability_delete_list

List of windows capabilities to uninstall

#### Default value

```YAML
win_capability_delete_list: []
```

#### Example usage

```YAML
win_capability_delete_list:
  - "Browser.InternetExplorer~~~~0.0.11.0"
```

### win_capability_download_dir

Download directory for the ISO

#### Default value

```YAML
win_capability_download_dir: '{{ ansible_env.SystemRoot }}\temp\windows_isos'
```

### win_capability_download_filename

Save as name of the downloaded file

#### Default value

```YAML
win_capability_download_filename: ''
```

### win_capability_iso_relative_source_path

Relative path in the ISO where all the CAB files are stored

#### Default value

```YAML
win_capability_iso_relative_source_path: LanguagesAndOptionalFeatures
```

### win_capability_iso_url

URL to the Windows FoD ISO if installing offline

General Info:
https://learn.microsoft.com/en-us/azure/virtual-desktop/windows-11-language-packs

Windows 10 FoD
https://software-static.download.prss.microsoft.com/pr/download/19041.1.191206-1406.vb_release_amd64fre_FOD-PACKAGES_OEM_PT1_amd64fre_MULTI.iso

Windows 11 22h2 FoD
https://software-static.download.prss.microsoft.com/dbazure/988969d5-f34g-4e03-ac9d-1f9786c66749/22621.1.220506-1250.ni_release_amd64fre_CLIENT_LOF_PACKAGES_OEM.iso

Windows 11 24h2 FoD
https://software-static.download.prss.microsoft.com/dbazure/888969d5-f34g-4e03-ac9d-1f9786c66749/26100.1.240331-1435.ge_release_amd64fre_CLIENT_LOF_PACKAGES_OEM.iso

#### Default value

```YAML
win_capability_iso_url: ''
```

### win_capability_isos_remove_when_finished

Delete ISO file after unmouted and ansible role is finished

#### Default value

```YAML
win_capability_isos_remove_when_finished: true
```

### win_capability_post_reboot_delay

Wait number of seconds after reboot to continue

#### Default value

```YAML
win_capability_post_reboot_delay: 30
```

### win_capability_pre_reboot_delay

Wait number of seconds before rebooting

#### Default value

```YAML
win_capability_pre_reboot_delay: 5
```

### win_capability_reboot_when_required

Automatically reboot when a Windows feature requires it

#### Default value

```YAML
win_capability_reboot_when_required: true
```



## Dependencies

None.

## License

license (GPL-2.0-or-later, MIT, etc)

## Author

andif888
