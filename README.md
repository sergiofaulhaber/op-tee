# op-tee

# Para executar uma máquina arm via docker e qemu

	sudo apt-get update
 	sudo apt-get install qemu qemu-user-static binfmt-support docker.io
  	sudo apt-get install libglib2.0-dev libpixman-1-dev
  	docker run -it --rm arm64v8/ubuntu bash
Aparecerá um shell semelhante root@98b1e1360d34:/#  
A partir deste ponto os comandos linux ficam funcionais podendo instalar pacotes com o APT 


  # Para criar uma máquina arm com qemu e op-tee

	sudo apt update && apt upgrade -y
	sudo apt install -y adb acpica-tools  autoconf automake bc \
	bison build-essential ccache cpio cscope curl device-tree-compiler \
	e2tools expect fastboot flex ftp-upload gdisk git libattr1-dev \
	libcap-ng-dev libfdt-dev libftdi-dev libglib2.0-dev libgmp3-dev \
	libhidapi-dev libmpc-dev libncurses5-dev libpixman-1-dev libslirp-dev \
	libssl-dev libtool libusb-1.0-0-dev make mtools netcat ninja-build python3-cryptography \
	python3-pip python3-pyelftools python3-serial python-is-python3 \
	rsync swig unzip uuid-dev wget xdg-utils xterm xz-utils zlib1g-dev \
	qemu qemu-user-static binfmt-support docker.io libglib2.0-dev libpixman-1-dev \
	gcc-arm-linux-gnueabihf repo


	mkdir optee
	cd optee
	repo init -u https://github.com/OP-TEE/manifest.git -m qemu_v8.xml
	repo sync
	cd build
	make toolchains
	make run

