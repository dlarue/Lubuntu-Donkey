# Lubuntu-Donkey
Create a bootable ISO image, based on Lubuntu 17.04, containing the parts and tools to get a donkeycar running in 30 minutes. Edit Add topics

Build a custom ISO containing everything you need to get a Donkey Car( http://donkeycar.com ) running autonomously. The tool i use is called Customizer( https://github.com/kamilion/customizer ).

What I do is start with latest Lubuntu 17.04 ISO from Canonical and loading that ISO on Customizer decomposes it into a directory named "Filesystem". I then have 1 script I tell Customizer to run so it  runs in the chroot automatically and it contains mostly apt commands to remvoe and install packaages into the Filesystem chroot environment. Then I have another script I run outside of Customizer, as root,  which punches into the Filesystem directory a bunch of things for the Filesystem/home/lunbunu directory/user.  For example, I had booted a standard Lubuntu ISO and ran Firefox then loaded up default pages, made them the Firefox default anda then I tar'ed up the .mozilla directory and I expand that when I build a new ISO using the 2nd script. The scripts are named doit-customizer-apt and doit-customizer.updates.
