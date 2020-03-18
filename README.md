# CentOS 8 base AMI builder

These packer definitions will create minimal CentOS AMIs completely from scratch, meaning they are not built from existing AMIs.

It uses the "EBS Surrogate" packer builder to create them.

## Public AMI ID's


### SELinux Enabled
|  Region   |        AMI ID         |
| :-------: | :-------------------: |
| eu-west-1 | ami-06abab7e61a91f324 |
| eu-west-2 | ami-038f3f7ca0e5edae2 |
| us-east-1 | ami-06a6ac4ed9d8293a7 |

### SELinux Disabled
|  Region   |        AMI ID         |
| :-------: | :-------------------: |
| eu-west-1 | ami-0b8e6499700f8a47e |
| eu-west-2 | ami-06952c17510909f71 |
| us-east-1 | ami-0ff504b096ae798ea |

## Usage

CentOS 8:
```bash
packer build packer-base-centos8.json
```

CentOS 8 Stream:
```bash
packer build packer-base-centos8-selinux.json
```

## Credits

The original code for the CentOS 8 packer builds are credited to [@irvingpop](https://github.com/irvingpop) based on the repository [packer-chef-highperf-centos-ami](https://github.com/irvingpop/packer-chef-highperf-centos-ami)