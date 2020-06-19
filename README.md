# Terraform-AWS-hashcat

Deploy Hashcat to AWS Instance with Terraform.

# variables.tf file

```

variable "aws_access_key" {
  default = "D0N7PV5HC23DST0617"
}
variable "aws_secret_key" {
  default = "lsofwud3lsj2o4klfoLOLj4odj2o4jiopf"
}
variable "aws_region" {
  default = "eu-central-1"
}
variable "ssh_key_path" {
  default = "C:/Users/...."
}
variable "enable_rdp" {
  default = true
}
variable "gpu_instance" {
  default = "t2.large"
}
variable "ssh_key_name" {
  default = "terraform-key"
}

```



DEBUG

```
    1  ls
    2  sudo su root
    3  clear
    4  sudo /bin/bash NVIDIA-Linux-x86_64-410.104.run --ui=none --no-questions --silent -X
    5  clear
    6  sudo apt-get install linux-headers-$(uname -r)
    7  distribution=$(. /etc/os-release;echo $ID$VERSION_ID | sed -e 's/\.//g')
    8  echo $distribution
    9  wget https://developer.download.nvidia.com/compute/cuda/repos/$distribution/x86_64/cuda-$distribution.pin
   10  sudo mv cuda-$distribution.pin /etc/apt/preferences.d/cuda-repository-pin-600
   11  sudo apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/cuda/repos/$distribution/x86_64/7fa2af80.pub
   12  echo "deb http://developer.download.nvidia.com/compute/cuda/repos/$distribution/x86_64 /" | sudo tee /etc/apt/sources.list.d/cuda.list
   13  sudo apt-get update
   14  sudo apt-get -y install cuda-drivers
   15  reboot
   16  sudo reboot
   17  ls
   18  cd /
   19  ls
   20  7za x hashcat-5.1.0.7z
   21  sudo 7za x hashcat-5.1.0.7z
   22  ls
   23  cd hashcat-5.1.0/
   24  ls
   25  ls -lah
   26  bash hashcat64.bin -b
   27  sudo bash hashcat64.bin -b
   28  cd ..
   29  rm hashcat-5.1.0*
   30  sudo rm hashcat-5.1.0*
   31  ls
   32  rmdir hashcat-5.1.0/
   33  sudo rmdir hashcat-5.1.0/
   34  sudo rm -rf hashcat-5.1.0/
   35  wget https://hashcat.net/files/hashcat-5.1.0.7z
   36  cd
   37  wget https://hashcat.net/files/hashcat-5.1.0.7z
   38  7za x hashcat-5.1.0.7z
   39  cd hashcat-5.1.0/
   40  ls
   41  bash hashcat64.bin -b
   42  bash hashcat32.bin -b
   43  ls -lah
   44  ./hashcat
   45  ./hashcat64.bin
   46  ./hashcat64.bin  -b
   47  export PATH=/usr/local/cuda-11.0/bin${PATH:+:${PATH}}
   48  export LD_LIBRARY_PATH=/usr/local/cuda-11.0/lib64                         ${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}
   49  ./hashcat64.bin  -b
   50  /usr/bin/nvidia-persistenced --verbose
   51  cat /proc/driver/nvidia/version
   52  ./hashcat64.bin  -b
   53  sudo apt-get install ocl-icd-libopencl1 -y
   54  ./hashcat64.bin  -b
   55  history
```