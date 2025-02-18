# SPI-Slave-with-single-port-RAM
PI Slave Overview
The SPI Slave is a digital communication block designed to interface with an SPI Master device. It operates in a synchronous serial communication protocol, where the Master controls the clock (SCLK) and initiates data transfers. The SPI Slave responds to the Master's commands by receiving and transmitting data over the MOSI (Master Out Slave In) and MISO (Master In Slave Out) lines, respectively. The Slave Select (SS) line is used to enable or disable the Slave device.

Key Features:
Synchronous Communication: Operates based on a shared clock signal from the Master.

Full-Duplex Communication: Supports simultaneous data transmission and reception.

Configurable Modes: Supports different SPI modes (0-3) based on clock polarity (CPOL) and clock phase (CPHA).

Flexible Data Frame Size: Handles customizable data frame lengths.

How It Works:
The SPI Slave waits for the Master to assert the Slave Select (SS) signal. Once selected, it listens to the clock (SCLK) and receives data on the MOSI line while transmitting data on the MISO line. The communication is controlled by the SPI mode settings, which determine the clock polarity and phase.

Finite State Machine (FSM) State Diagram
![image](https://github.com/user-attachments/assets/25803b8a-919e-411f-adcc-0767a44cdca5)


The FSM controls the SPI Slave's operation, transitioning between states such as IDLE, RECEIVE, TRANSMIT, and PROCESS based on the SPI signals and internal logic.

Timing Diagram
![image](https://github.com/user-attachments/assets/40925a20-c8f4-420a-adf5-98f856660bac)

The timing diagram illustrates the relationship between the SCLK, SS, MOSI, and MISO signals during a typical SPI transaction. It shows how data is sampled and transmitted in sync with the clock.
