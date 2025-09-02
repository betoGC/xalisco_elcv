![alt text](https://github.com/betoGC/xalisco_elcv/edit/main/Panel-Image.png)

# Installation Guide for Xalisco

## Linux

1. Open a terminal.  
2. Install the required libraries:

   ```bash
   sudo apt-get install build-essential
   ```

3. Install the Fortran compilers:

   ```bash
   sudo apt-get install gfortran
   ```

4. Install the Qt libraries, preferably version **5.0** from repos

   To avoid installing these libraries manually, you can install them via the terminal:

   ```bash
   sudo apt-get install lib-qt5 libqt5-dev libqt5-core qt5-dev-tools qt5-doc qt5-qmake
   ```

5. Obtain the compressed file `Xalisco_version.tar.gz` and extract it into a local directory:

   ```bash
   tar -zxvf Xalisco_version.tar.gz
   ```

6. Enter the extracted directory:

   ```bash
   cd Xalisco_version/
   ```

7. Run the `qmake` command (or `qt5-qmake` if available):

   ```bash
   qt5-qmake
   ```
   or
   ```bash
   qmake
   ```

8. Compile Xalisco:

   ```bash
   make
   ```

9. Once the compilation finishes successfully, an executable file will be created. You can run the program with:

   ```bash
   ./xalisco -platform wayland
   ```

10. Enjoy!

---

## Windows

1. Install a Bash shell using **Cygwin64** or **MinGW**.  
   In this tutorial we will assume **Cygwin** as the chosen shell, but MinGW should be very similar.  

2. Install the necessary libraries using the `setup.exe` tool available here:  
   [Cygwin Installer](https://cygwin.com/install.html)

  modern platforms have the possibility to work with WSL - windows subsystem for linux, if this is your case, 
  then you will need to install the X-server of your preference and qt5 libraries
3. During installation, select the following packages in the search tool:

   - `qt5-qmake`  
   - `gfortran`  
   - `g++`  
   - `qt5-dev`  
   - `Qt5Core`  
   - `qt5`

   > It is recommended to install all suggested packages during the search, since some utilities have cross-dependencies with other packages and versions.

4. Additionally, install the **X11** and **xinitd** libraries using the same procedure.  
   If dependencies are missing, check the official package repository for WSL, debian or Ubuntu search page:  
   [Cygwin Package Search](https://cygwin.com/cgi-bin2/package-grep.cgi?grep=build-e&arch=x86_64)

5. Once all compilers and libraries are installed, obtain the Xalisco source code and follow the **Linux installation steps starting from step 5**.
