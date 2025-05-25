<div align="center">
  <img src="https://avatars.githubusercontent.com/u/176677387" width="150" height="auto" />
  <h1> JAI$KSH </h1>
</div>

Welcome to the **JAI$KSH** repository! 🎉 Dive into the world of RF interference with this unique project based on the ESP32 and NRF24 technology.

## 📚 Table of Contents
- [🎯 Possible Additions](#-possible-additions)
- [🚀 What Can You Do with This?](#-what-can-you-do-with-this)
- [📋 List of Components](#-list-of-components)
- [🧑‍🔧 Let's Get Started with Soldering!](#-lets-get-started-with-soldering)
- [📦 Flash Firmware](#-flash-firmware)
- [🌐 Web Interface](#-Web-Interface)

-----

## 🎯 Possible Additions
- **Deauthentication attack**
- **BLE spam**
- **Beacon spam**
- **nRF24 mousejack**

-----

## 🚀 What Can You Do with This?
This amazing jammer is built on the **ESP32** architecture integrated with **two NRF24** modules. With its extraordinary capabilities, you can effectively disrupt signals across different technologies including:
- **Bluetooth** 🔊
- **BLE** 📱
- **Drones** 🚁
- **Wi-Fi** 📶
- **Zigbee**📡

-----

## 📋 List of Components
To bring this project to life, you will need the following components:
1. **Two NRF24L01+PA+LNA modules** *(or one for the "Compact" version)* 🛠️
2. **ESP32-DevKitC** *(with Type-C)* **or**  **ESP32-DevKit V1** *(with Micro USB)*⚙️
3. **Two 16V capacitors** rated at **100µF** 🔋
4. **128x32 or 128x64 OLED display** 📺 *(Not required when using the "without OLED" version)*
5. **Tactile button** 🔘 *(Not required when using the "without OLED" version)*

-----

## 🧑‍🔧 Let's Get Started with Soldering!
<details>
<summary><strong>With OLED</strong></summary>

<div style="margin-left: 20px;">

## Differences between versions

The **Compact** version is equipped with a **single NRF24** module, while the **Standard** version features **two**.
 
Notably, the Compact version allows **uninterrupted access to the display** even when jamming is started. 

This will enable me to utilize features that may be added in the future but are currently **unavailable** in the **Standard version**. For instance, **one already implemented** feature is the a**bility to exit jamming mode** by simply pressing the "**OK**" button (*pin 25*). 

Given these advantages, **I highly recommend choosing the Compact version** for its versatility and potential for future enhancements.

---

<details>
<summary><strong>Compact</strong></summary>

<div style="margin-left: 20px;">

### HSPI Connection
| **Pin Name** | **ESP32 GPIO** | **Connection**       |
|--------------|----------------|----------------------|
| VCC          | 3.3V          | (+) capacitor        |
| GND          | GND           | (-) capacitor        |
| CE           | GPIO 16       |                      |
| CSN          | GPIO 15       |                      |
| SCK          | GPIO 14       |                      |
| MOSI         | GPIO 13       |                      |
| MISO         | GPIO 12       |                      |
| IRQ          |                |                      |

### OLED Connection
| **Pin Name** | **ESP32 GPIO** |
|--------------|----------------|
| VCC          | 3.3V          |
| GND          | GND           |
| SCL          | GPIO 22       |
| SDA          | GPIO 21       |

### Button Connection
| **Button Actions** | **ESP32 GPIO** |
|--------------|----------------|
| OK          | GPIO 25       |
| NEXT (Optional)             | GPIO 26       |
| PREVIOUS (Optional)            | GPIO 27       |


</div>
</details>

<details>
<summary><strong>Standard</strong></summary>

<div style="margin-left: 20px;">

### HSPI Connection
| **Pin Name** | **ESP32 GPIO** | **Connection**       |
|--------------|----------------|----------------------|
| VCC          | 3.3V          | (+) capacitor        |
| GND          | GND           | (-) capacitor        |
| CE           | GPIO 16       |                      |
| CSN          | GPIO 15       |                      |
| SCK          | GPIO 14       |                      |
| MOSI         | GPIO 13       |                      |
| MISO         | GPIO 12       |                      |
| IRQ          |                |                      |

### VSPI Connection
| **Pin Name** | **ESP32 GPIO** | **Connection**       |
|--------------|----------------|----------------------|
| VCC          | 3.3V          | (+) capacitor        |
| GND          | GND           | (-) capacitor        |
| CE           | GPIO 22       |                      |
| CSN          | GPIO 21       |                      |
| SCK          | GPIO 18       |                      |
| MOSI         | GPIO 23       |                      |
| MISO         | GPIO 19       |                      |
| IRQ          |                |                      |

### OLED Connection
| **Pin Name** | **ESP32 GPIO** |
|--------------|----------------|
| VCC          | 3.3V          |
| GND          | GND           |
| SCL          | GPIO 22       |
| SDA          | GPIO 21       |

### Button Connection
| **Button Actions** | **ESP32 GPIO** |
|--------------|----------------|
| OK          | GPIO 25       |
| NEXT (Optional)             | GPIO 26       |
| PREVIOUS (Optional)            | GPIO 27       |


</div>
</details>

</div>
</details>
<details>
<summary><strong>Without OLED</strong></summary>

<div style="margin-left: 20px;">

### HSPI Connection
| **Pin Name** | **ESP32 GPIO** | **Connection**       |
|--------------|----------------|----------------------|
| VCC          | 3.3V          | (+) capacitor        |
| GND          | GND           | (-) capacitor        |
| CE           | GPIO 16       |                      |
| CSN          | GPIO 15       |                      |
| SCK          | GPIO 14       |                      |
| MOSI         | GPIO 13       |                      |
| MISO         | GPIO 12       |                      |
| IRQ          |                |                      |

### VSPI Connection
| **Pin Name** | **ESP32 GPIO** | **Connection**       |
|--------------|----------------|----------------------|
| VCC          | 3.3V          | (+) capacitor        |
| GND          | GND           | (-) capacitor        |
| CE           | GPIO 22       |                      |
| CSN          | GPIO 21       |                      |
| SCK          | GPIO 18       |                      |
| MOSI         | GPIO 23       |                      |
| MISO         | GPIO 19       |                      |
| IRQ          |                |                      |

</div>
</details>
###### ⚠️ Important for source builds: Since v2.5.0, this project uses a modified RF24 library (see /lib).

-----

## 🌐 Web Interface

- To utilize the web interface, please follow the steps outlined below.
1. activate the **JAI$KSH Jammer**.
2. Connect to the Wi-Fi network named `JAI$KSH` using the password `JAIDEEP$KSH`.
3. open your web browser and navigate to the IP address `192.168.4.1`.
4. Now you can control your nRF24 jammer through an web interface.
