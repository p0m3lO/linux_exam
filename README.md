# linux_exams

## Requirements

1. Vagrant
2. Virtualbox

## Usage

1. ***Provision the virtual exam machines***

    To use the virtual exam machine navigate to the ***exam_vm*** or the ***server_vm*** directory and provision the virtual machine:

    ```
    $ vagrant up
    ```
    
    After the virtual machine started you can access the ***web interface*** through the host browser at http://localhost:5000

2. ***Connect to the virtual exam machine***

    From the ***exam_vm/*** directory run:

    ```
    $ vagrant ssh
    ```

3. ***Start / stop the virtual exam web interface on demand***

    After connected to the virtual exam machine run:

    ```
    $ exam --start
    $ exam --stop
    ```

4. ***Stop the virtual exam machine***

    From the ***exam_vm/*** directory run:

    ```
    $ vagrant halt
    ```

6. ***Reload the virtual exam machine configuration after changes made to the vagrantfile***

    ```
    $ vagrant reload
    ```

## Issues

### Windows

If vagrant cannot provision the VM and it stucks you may need to disable WSL and restart:

```
bcdedit /set hypervisorlaunchtype off
```
