# ICSim Full clean Installation 

# Get ICSim working clean!

First, look if your OP System is UpToDate:

  if you use Linux: ```shell apt update && apt upgrade ```
  
After this do:
  
  sudo apt-get install libsdl2-dev libsdl2-image-dev can-utils
  
Setup a virtual can interface:
  
  sudo modprobe can
  sudo modprobe vcan
  sudo ip link add dev vcan0 type vcan
  sudo ip link set up vcan0
  
After this do:

  make all
  
The Usage of ICSim:

   ./icsim vcan0	
   ./controls vcan0
