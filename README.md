# ansible-qemu

1. Install [ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html), probably using pip.
2. Clone this repo
3. Update `hosts.yml` with your own hostname and username
    - Make sure you're not required to key in password manually when connecting to the server via ssh
4. Update the `workspace` variable in `qemu.yml` if needed. It's value is `/tmp/<username>` by default.
4. Run 
    ```
    ansible-playbook -i hosts.yml qemu.yml
    ```

Note: It's expected to see some fatal errors during execution. Do check if the last message is a success. If so, there shoule be an instruction to set `PATH`.
