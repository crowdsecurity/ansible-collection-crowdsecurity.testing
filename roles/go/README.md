
On most Linux: install Go from the binary distribution

Accepts the following variables

```yaml
# default to latest
golang_version: "1.18.5"
# you may want to add this to $PATH
golang_install_dir: "/opt/go/{{ golang_version }}"
```

example:

```yaml
- name: "install Go"
  hosts: all
  roles:
    - role: crowdsecurity.testing.go
      vars:
        golang_version: "1.18.5"
        golang_install_dir: "/opt/go/{{ golang_version }}"
```


On FreeBSD / OpenBSD / Alpine: install the default version of Go from the package manager.



# TODO:

 - make behavior on BSD / Alpine like Linux.

