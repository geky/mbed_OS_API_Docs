# I2CSlave

An I2C Slave, used for communicating with an I2C Master device.

Synchronization level: not protected.

## Example

Simple I2C responder

```c++
#include <mbed.h>
 
I2CSlave slave(p9, p10);
 
int main() {
   char buf[10];
   char msg[] = "Slave!";
 
   slave.address(0xA0);
   while (1) {
       int i = slave.receive();
       switch (i) {
           case I2CSlave::ReadAddressed:
               slave.write(msg, strlen(msg) + 1); // Includes null char
               break;
           case I2CSlave::WriteGeneral:
               slave.read(buf, 10);
               printf("Read G: %s\n", buf);
               break;
           case I2CSlave::WriteAddressed:
               slave.read(buf, 10);
               printf("Read A: %s\n", buf);
               break;
       }
       for(int i = 0; i < 10; i++) buf[i] = 0;    // Clear buffer
   }
}
```

## API


[![View code](https://www.mbed.com/embed/?type=library)](https://developer.mbed.org/users/mbed_official/code/mbed/docs/tip/classmbed_1_1I2CSlave.html)
