 voxtomix-config
==============

Here is the voctomix configuration from the Toolbox VOC stored.

The git directory should be stored under this path:

```bash
/etc/voxtomix/
```

 Remote or same machine?
------------------------
**same machine:**
There are two different modi available for video mixing.
Either you are on the mixing computer with voctocore and voctogui running at the same device. Then you should use the ``master`` Branch here on this git.
There is [this](https://github.com/ToolboxBodensee/toolbox-voc_ansible) Ansible Playbook, that will do all the configuration for you.

**remote**
If you don't run voctocore and voctogui on the same device, than you should checkout the ``remote`` branch.
There you can find an minor modified configuration to acces the preview images via network.
You also need to clone the voctomix git and this git by hand. Please have a look into the voctomix README for needed dependencies.
```bash
git clone https://github.com/voc/voctomix.git -b master voctomix
sudo git clone https://github.com/ToolboxBodensee/toolbox-voc_ansible.git -b remote /etc/voctomix

```

 voctocore
---------
In voctocore.ini is the main configuration for the voctomix core process saved.
If a variable is not defined, it will use the default value from [/opt/voctomix/voctocore/default-config.ini](https://github.com/voc/voctomix/blob/master/voctocore/default-config.ini)

 voctogui
---------
In voctogui.ini is the configuration for the graphical frontend.
If a variable is not defined, it will use the default value from [/opt/voctomix/voctogui/default-config.ini](https://github.com/voc/voctomix/blob/master/voctogui/default-config.ini)

