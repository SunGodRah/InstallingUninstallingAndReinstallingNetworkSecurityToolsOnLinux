
# Installing, Uninstalling, and Reinstalling Network Security Tools on Linux

## Introduction
As a security analyst, I need to have tools like Suricata and tcpdump installed on my system for network security monitoring. In this lab, I will guide you through the process of installing, uninstalling, and reinstalling these applications on a Linux Bash shell using the APT package manager. By the end of this lab, I will confirm that both applications are installed correctly.

---

## Task 1: Ensure APT is Installed

First, I confirmed that APT, the package manager, was available on my system. I did this by simply typing the following command in the terminal:

```bash
apt
```

The output confirmed that APT was installed by displaying its version and usage information:

```
apt 1.8.2.3 (amd64)
Usage: apt [options] command
```

<p align="center">
  <img src="https://github.com/user-attachments/assets/84dd94db-6815-49de-94ef-8b8d290605c6" height="100%" width="100%">
</p>

With APT available, I was ready to proceed with installing the required applications.

---

## Task 2: Install and Uninstall Suricata

### Install Suricata
Next, I used the APT package manager to install Suricata, a powerful network analysis tool for intrusion detection. Here’s the command I used:

```bash
sudo apt install suricata
```

I pressed `ENTER` to confirm the installation when prompted. Once the installation was complete, I verified it by running:

```bash
suricata
```

This displayed version and usage information for Suricata, confirming that the installation was successful:

```
Suricata 4.1.2
USAGE: suricata [OPTIONS] [BPF FILTER]
```
<p align="center">
  <img src="https://github.com/user-attachments/assets/23df0e96-cc8b-4b9f-8431-7ff4fea0251c" height="100%" width="100%">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/65796a6d-2442-40f2-a9f0-21d7073bfbb7" height="100%" width="100%">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/5b525675-ed49-4c54-a524-80d74d9e061d" height="100%" width="100%">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/f4b110bf-6ac9-4d73-9bd9-eb30fe7bfc3c" height="100%" width="100%">
</p>


### Uninstall Suricata
Next, I uninstalled Suricata using the following command:

```bash
sudo apt remove suricata
```

Again, I pressed `ENTER` to confirm when prompted. To make sure Suricata was no longer installed, I ran the command:

```bash
suricata
```

This returned an error, confirming that Suricata had been successfully removed:

```
-bash: /usr/bin/suricata: No such file or directory
```

<p align="center">
  <img src="https://github.com/user-attachments/assets/6304772b-82ea-4910-9936-5581f74a6682" height="100%" width="100%">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/9d590fc8-c5cc-4467-abab-48a49227cd86" height="100%" width="100%">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/115b32a3-0c3a-480f-b914-0676da178689" height="100%" width="100%">
</p>

---

## Task 3: Install tcpdump

With Suricata removed, I proceeded to install `tcpdump`, a command-line tool for capturing network traffic, using the following command:

```bash
sudo apt install tcpdump
```

<p align="center">
  <img src="https://github.com/user-attachments/assets/b0beb29a-e950-4d16-ab3f-4ac5da09de89" height="100%" width="100%">
</p>



Once the installation was complete, I moved on to verifying the installations.

---

## Task 4: List Installed Applications

To ensure that tcpdump was installed correctly, I listed all installed applications using:

```bash
apt list --installed
```

This produced a long list of applications, including `tcpdump`:

```
tcpdump/oldstable,now 4.9.3-1~deb10u2 amd64 [installed]
```

Since I had previously uninstalled Suricata, it was not present in the list.

<p align="center">
  <img src="https://github.com/user-attachments/assets/a11d5da0-716c-4c5d-932d-aeaeb83c3736" height="100%" width="100%">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/399d7ae1-9b64-447f-ad95-7232b617ce26" height="100%" width="100%">
</p>

---

## Task 5: Reinstall Suricata

Finally, I reinstalled Suricata using:

```bash
sudo apt install suricata
```

<p align="center">
  <img src="https://github.com/user-attachments/assets/1e2a6128-0ee5-4206-9cc3-e3c1534d456d" height="100%" width="100%">
</p>

After confirming the installation, I listed all installed applications again:

```bash
apt list --installed
```

This time, both Suricata and tcpdump appeared in the list:

```
suricata/oldstable,now 1:4.1.2-2+deb10u1 amd64 [installed]
tcpdump/oldstable,now 4.9.3-1~deb10u2 amd64 [installed]
```

<p align="center">
  <img src="https://github.com/user-attachments/assets/e6ce9049-cf73-42a8-8d84-dc48a32e5597" height="100%" width="100%">
</p>

---

## Conclusion

In this lab, I successfully installed, uninstalled, and reinstalled two important network security tools: Suricata and tcpdump. I also verified the installation status using the APT package manager. Managing applications in a Linux environment is an essential skill for any security analyst, and this lab provided a solid foundation for working with these tools.
