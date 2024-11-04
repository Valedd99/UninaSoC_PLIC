# Virtual Uart Host Application
### To build
```
make
```
### Usage
```
cd bin;
sudo ./host_virtual_uart <uart_paddr> [uart_length] [u_poll_period]
```
* uart_paddr: physical address of the virtual uart peripheral in the PCIe BAR
* uart_length: length of the mapping (CSR space of the peripheral) - default 20
* u_poll_period: poll period in microseconds - default 10
The application starts a prompt to interact with the SoC.
Each char you digit is sent to the SoC through the virtual uart peripheral.
The behaviour depends on the application running on the SoC.
### Examples
#### Virtual uart hello world
If the SoC runs the virtual_uart_hello_world application, it simply prints the "Hello world!!!" string.
```
Hello world!!!
```
#### Virtual uart echo server
If the SoC runs the virtual_uart_echo_server application, it waits for a string then reply with the same string.
```
Please enter a string: <your string>
This is your string: <your string> 
```