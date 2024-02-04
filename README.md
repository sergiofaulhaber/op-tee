# op-tee

# Para executar uma máquina arm via docker e qemu

	  sudo apt-get update
 	  sudo apt-get install qemu qemu-user-static binfmt-support docker.io
  	sudo apt-get install libglib2.0-dev libpixman-1-dev
  	docker run -it arm64v8/ubuntu bash
  
