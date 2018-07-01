# Ansible Role: Miniconda

Installs [Miniconda](https://conda.io/miniconda.html) on Ubuntu installations.

## Requirements

None.

## Role Variables

Variables and default values:

```yaml
# main Anaconda download server
miniconda_mirror: "https://repo.continuum.io/miniconda"

# version of python (2|3)
miniconda_python_ver: 3

# miniconda version
miniconda_ver: "4.5.4"

# miniconda checksums...
# https://repo.continuum.io/archive/
miniconda_checksums:
  Miniconda2-4.5.4-Linux-x86_64.sh: "md5:8a1c02f6941d8778f8afad7328265cf5"
  Miniconda3-4.5.4-Linux-x86_64.sh: "md5:a946ea1d0c4a642ddf0c3a26a18bb16d"

# when downloading the miniconda binary it might take a while
miniconda_timeout_seconds: 600

miniconda_parent_dir: /opt

miniconda_pkg_update: true
miniconda_install_packages: []
```

## Example Playbook

```yaml
- hosts: all
  roles:
    - jkglasbrenner.miniconda
```

## License

MIT
