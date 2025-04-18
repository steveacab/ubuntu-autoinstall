# ubuntu-autoinstall

The autoinsall.yaml is configured to be semi-interactive.

The Ubuntu Server installer will ask only for name, username, password and hostname.

The network (en*) is automatically configured to DHCP4 and 6.

It will use the whole storage to / and format it to ext4.

Language EN, Keyboard CH layout variant DE.

OpenSSH server will be installed automatically.

At the end the installer will update ONLY the security packages.

________________________________________________________________________________________________

Download the autoinstall.yaml file from the provided link and place it in the current directory.

`mkdir myiso
mv ubuntu-*.iso myiso/
cd myiso/
mkdir isomount
sudo mount -o loop ubuntu-*.iso isomount
rsync -a isomount/ extracted
sudo cp autoinstall.yaml myiso/extracted/
cd extracted
sudo xorriso -as mkisofs -r -V "This is an Ubuntu semi-interactive installation iso" -o ../custom-ubuntu.iso -J -l -b boot/grub/i386-pc/eltorito.img -c boot.catalog -no-emul-boot -boot-load-size 4 -boot-info-table .`



![Screenshot 2025-04-18 195341](https://github.com/user-attachments/assets/6a12b2a6-d9cb-421d-8d67-96dbf4db79a4)
![Screenshot 2025-04-18 195646](https://github.com/user-attachments/assets/50a146b3-9e2f-4592-87b5-97abdd5470a7)
![Screenshot 2025-04-18 194715](https://github.com/user-attachments/assets/80a4f7db-464a-4ca9-9aff-2b036a445d90)
![Screenshot 2025-04-18 195231](https://github.com/user-attachments/assets/05a10a30-b4f4-4ea8-8c2a-3aee2bfc0e73)
