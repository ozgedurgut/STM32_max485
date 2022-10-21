# STM32_max485
## Communication is provided between two STM32s using max485 modules.

RS485 is one of the most common method of communicating with a device using the modbus protocol.  
Here we will see how to use the RS485 to TTL converter module with STM32.   
I used 2 STM32 controller F103s connected via these modules and they will communicate with each other.  

The RO pin connects to the RX pin of the UART, and the DI pin connects to the TX pin.  
The RE and DE Pins are responsible for setting the module in Receiver or Transmitter mode.  
* When the RE pin is LOW and DE pin is LOW, the Module is set in the Receiver mode.  
* When the DE pin is HIGH and RE pin is HIGH, the Module is set in the Transmitter mode.   

The Pin A and the Pin B are the output pins which carries the transmission signal.  
<img src="https://github.com/ozgedurgut/STM32_max485/blob/main/s-l500KK.jpg"   >

Above is the wiring diagram of modules with STM32F103C8 controllers.

The RO pin is connected to the PA10 (UART1 RX) and DI pin is connected to the PA9 (UART1 TX).  
The RE and DE are connected together with the pin PA8, which we have set as the output in the MCU.  

### The CubeMX configuration is shown below ###

<img src="https://github.com/ozgedurgut/STM32_max485/blob/main/s-l500KK.jpg"   >
<img src="https://github.com/ozgedurgut/STM32_max485/blob/main/s-l500KK.jpg"   >



