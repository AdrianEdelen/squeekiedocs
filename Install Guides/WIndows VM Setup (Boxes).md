# Installing and setting up a Windows VM using the Boxes GUI


---

### Prerequisites:
- Linux with Boxes Installed
- A windows 10 ISO -> **[download](https://www.microsoft.com/en-us/software-download/windows10ISO)**
- Windows 10 VirtIO ISO -> **[download](https://fedorapeople.org/groups/virt/virtio-win/direct-downloads/stable-virtio/virtio-win.iso)**

---

#### Boxes Installation Steps

1. Open Boxes you should have a main screen similar to the gif below, without any existing VMs
2. Select the + button on the top left
![New VM Dialog](/assets/images/boxes/new_dialog.gif)
3. Select "Install From File"
4. In the resulting File Dialog, Select your windows 10 ISO

5. Once Selected, you will be prompted with the following dialog:
![Create VM Dialog](/assets/images/boxes/create_menu.png)
6. For this dialog perform the following actions:
    1. Rename the VM to your preferred name, this is a cosmetic label for the VM so the name does not matter.
    2. Expand the Operating System option to reveal the Operating System Search
    3. Search for and select Windows 10
    4. Size Memory appropriate to your system.
        1. In the scenario you are running the VM in the **foreground** as your primary task, allow for more ram (up to 75% can be acceptable with minimal background tasks on the host)
        2. In the scenario you are running the VM in the **background** try to allow only as much ram as is needed for the task.
    5. Size Storage appropriately for your needs and system.
7. Select Create on the top right.
8. After a few moments, your VM will be ready to open.

### Windows Setup
The standard Windows setup can at this point be done, selecting whichever features apply.

### Post Windows Install Setup
Once windows is installed and you are at the desktop follow the instructions here: [windows VirtIO drivers](https://pve.proxmox.com/wiki/Windows_VirtIO_Drivers)

### Notes
- The VM will grab your IO devices (mouse + keyboard) use lctrl+alt to ungrab it from the window
- when going into fullscreen hover the mouse on the top edge of the screen to bring down the menubar