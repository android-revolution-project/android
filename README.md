How to build Android Revolution Project

1. Install packages.
sudo su
apt-get install bison build-essential curl flex lib32ncurses5-dev lib32readline-gplv2-dev lib32z1-dev libesd0-dev libncurses5-dev libsdl1.2-dev libwxgtk2.8-dev libxml2 libxml2-utils lzop openjdk-7-jdk openjdk-7-jre pngcrush schedtool squashfs-tools xsltproc zip zlib1g-dev git-core make phablet-tools gperf git-core gnupg flex bison gperf libesd0-dev libwxgtk2.6-dev squashfs-tools build-essential zip curl libncurses5-dev zlib1g-dev sun-java6-jdk pngcrush schedtool g++-multilib lib32z1-dev lib32ncurses5-dev libc6-dev ia32-libs x11proto-core-dev lib32z-dev mingw32 tofrodos python-markdown python python-lunch libxml2-utils xsltproc libx11-dev:i386
2. Install JDK
add-apt-repository ppa:webupd8team/java && apt-get update && apt-get install oracle-java7-installer -y
3. Install repo

exit

# mkdir ~/bin

# PATH=~/bin:$PATH

# cd ~/bin

# curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo

# chmod a+x ~/bin/repo

4. Creating folder for src

# mkdir ~/cm12 && cd cm12

5. Enter in git (if not log in)

# git config --global user.email "youremail@ololo.com"

# git config --global user.name "yourname"

6. Download the sources

# repo init -u git://github.com/android-revolution-project/android.git -b master

# repo sync -f

7. After downloading the sources build the system

# cd cm12 && . build/envsetup.sh && lunch arp_saga-userdebug && make otapackage

Wait, then enjoy ;)
