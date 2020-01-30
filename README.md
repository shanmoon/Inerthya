# Inerthya
Simmeters Inerthya System

If you use Java version of Workspace, please use OpenJDK you can download it from here https://jdk.java.net/archive/

SimMeters Inerthya System is a distributed communication system to manage the creation of entire simulation hardware environment, this includes gauges, panels, actuators displays, and so much devices.

Its based on the CANBus topology network working at 500kbit/s and SFF standard frame format identifiers 11bit.

On the version 2.0 we reduced the payload from the simulation software to the system, and redefine the packet information to 10bytes.

We have two types of packet DOP and DIP (Data Output / Data Input packets) with the same format and following the specification of the CANAerospace protocol version 1.7

The system works over UDP connection on the port 6060 and the format of the UDP packets are described on inerthya.lua file insde of the wrappers folder.

Test UDP packets on UDP wrapper with command line;

echo 'ID_MACH_NUMBER=1.20;ID_INDICATED_AIRSPEED=350.00;' > /dev/udp/127.0.0.1/6060
