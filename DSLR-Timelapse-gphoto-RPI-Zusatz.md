##Zusatz für das Repository topada/DSLR-Timelapse-gphoto-RPI

Beim dem zweiten Teil von Teil (3) der Anleitung

        cd ~
        tar zvxf gphoto2-2.5.3.tar.gz
        cd gphoto2-2.5.3/
        ./configure --prefix=/usr
        
hatte ich diese Meldung

        checking whether popt is required... no
        checking whether popt is requested... no
        checking popt.h usability... no
        checking popt.h presence... no
        checking for popt.h... no
        checking popt.h usability... no
        checking popt.h presence... no
        checking for popt.h... no
        configure: error:
        * Cannot autodetect popt.h
        *
        * Set POPT_CFLAGS and POPT_LIBS correctly.

Mit folgenden Befehl konnte ich den Fehler beheben:  

        sudo apt-get install libpopt-dev  
        make  
        sudo make install
