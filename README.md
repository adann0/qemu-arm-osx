# qemu-arm-osx

$ brew install qemu

# ArmV6l

$ qemu-system-arm \
    -M versatilepb \
    -cpu arm1176 \
    -m 256 \
    -hda 2019-04-08-raspbian-stretch-lite.img \
    -net nic \
    -net user,hostfwd=tcp::5022-:22 \
    -dtb versatile-pb.dtb \
    -kernel kernel-qemu-4.14.79-stretch \
    -append 'root=/dev/sda2 panic=1' \
    -no-reboot
