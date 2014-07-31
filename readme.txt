This is a fork of xrdp to be used as a simple honeypot. Everything is the same with teh exception that it logs username/password and will never 
succesfully login. 

To install under Ubuntu:
git clone https://github.com/kx499/xrdp.git
cd xrdp
sudo apt-get install autoconf libtool libpam0g-dev libx11-dev libxfixes-dev libssl-dev libxrandr-dev libxrandr2
sudo ./bootstrap
sudo ./configure
sudo make
sudo make install

Original Readme:

xrdp 0.9.0

Credits
  This project is very much dependent on NeutrinoRDP, FreeRDP, rdesktop, and
  the work of Matt Chapman and the NeutrinoRDP team members, of which I'm a
  member.

  Mark from up 19.9 was the first to work with rdp server code.

Tested with linux on i386, x64, sparc, and ppc.
I've got it compiling and working in windows with borland free tools.
Non of the sesman or Xserver stuff works in windows of course.

xrdp directory is the main server code
vnc directory is a simple vnc client module for xrdp
sesman directory is a session manager for xrdp that uses Xvnc for the Xserver
libxrdp directory is a static library needed by xrdp
rdp is an rdp client module for connecting to another rdp server
xup is a module used to connect to an rdp specific X11 server
Xserver is the files needed to build an rdp specific X11 server
COPYING is the licence file
design.txt is an attempt to expain the project design
prog_std.txt is an attemp to explain the programming standard used

since version 0.5.0 we switch to autotool to build xrdp

to build and install

change to the xrdp directory and run
./bootstrap
./configure
make
then as root
make install

see file-loc.txt to see what files are installed where

Jay Sorg
