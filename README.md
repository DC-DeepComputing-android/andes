

# Setup

```bash
$ mkdir your_workspace
$ cd your_workspace
$ repo init -u  ssh://git@github.com/DC-DeepComputing-android/manifest -b aosp-dp

$ repo sync -c -j 4


```



# Build

```bash

$ cd your_workspace
$ . andes.lunch
$ m

# You will see the following image files
$ cd $OUT; ls *.img; cd -

boot.img   dtbo-unsigned.img  super_empty.img  userdata.img           vendor_boot.img               vendor_ramdisk.img
cache.img  init_boot.img      super.img        vbmeta.img             vendor_boot-test-harness.img  vendor_ramdisk-test-harness.img
dtb.img    product.img        system_ext.img   vendor-bootconfig.img  vendor.img
dtbo.img   ramdisk.img        system.img       vendor_boot-debug.img  vendor_ramdisk-debug.img
```



# Burn

```bash
$ bash device/deepcomputing/k1-kernel/andes-qilai/qilai-img/flush.sh

# Now you should at fold: device/deepcomputing/k1-kernel/andes-qilai/qilai-img
$ ls device/deepcomputing/k1-kernel/andes-qilai/qilai-img/sdcard*
device/deepcomputing/k1-kernel/andes-qilai/qilai-img/sdcard.img


# Check of=/dev/xxx on your computer!!!! eg. it maybe /dev/sdb on some computer
# $ dd if=./sdcard.img of=/dev/xxx bs=100M status=progress
```





# Run

```bash
# poweron and U can see UI

```

