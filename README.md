# Face Recognition Door Lock System Using Raspberry Pi

This repository contains the implementation details for a "Face Recognition Door Lock System Using Raspberry Pi". This project addresses modern security concerns by integrating a facial recognition module with an electromagnetic door lock system.

## Table of Contents

  - [About the Project](https://www.google.com/search?q=%23about-the-project)
  - [Features](https://www.google.com/search?q=%23features)
  - [Hardware Requirements](https://www.google.com/search?q=%23hardware-requirements)
  - [Software Requirements](https://www.google.com/search?q=%23software-requirements)
  - [How it Works](https://www.google.com/search?q=%23how-it-works)
  - [Setup and Installation](https://www.google.com/search?q=%23setup-and-installation)
  - [Authors](https://www.google.com/search?q=%23authors)
  - [Acknowledgements](https://www.google.com/search?q=%23acknowledgements)

## About the Project

In an era of increasing security challenges, this project offers an advanced solution for access control. The system captures human images using a face recognition module, compares them against a stored database of authorized users, and automatically unlocks the door via an electromagnetic lock upon a successful match. It also enhances security by detecting unknown individuals and notifying authorized personnel via email, with an option to remotely unlock the door through an Android application. The primary objective is to provide a fast, robust, accurate, and reasonably straightforward face recognition methodology.

## Features

  * **Real-time Face Detection and Recognition**: Capable of detecting and recognizing faces from image files using the Raspberry Pi.
  * **Automated Door Unlock**: Unlocks an electromagnetic door lock upon successful recognition of an authorized user.
  * **Intruder Alert System**: Sends email notifications to authorized persons when an unknown individual is detected.
  * **Remote Access**: Allows authorized users to unlock the door via an Android application if they choose to grant access to an unknown person.
  * **Efficient Algorithms**: Utilizes the Haar cascade classifier for robust face detection and recognition.

## Hardware Requirements

The system is built around the Raspberry Pi platform and requires the following hardware components:

  * **Raspberry Pi 4 Model B**: Serves as the central processing unit for the system.
  * **USB Camera Module**: Used for capturing real-time human images for face recognition.
  * **SD Card**: Essential for storing the operating system and project files.
  * **Electromagnetic Lock (Solenoid Lock)**: Actuates the door lock mechanism.
  * **Relay (SRD-05VDC-SL-C)**: Controls the electromagnetic lock based on signals from the Raspberry Pi.
  * **Buck Converter**: Ensures efficient power management for the hardware ensemble.

## Software Requirements

The project relies on the following software and libraries:

  * **Raspbian OS**: The recommended operating system for Raspberry Pi.
  * **OpenCV 3**: An open-source computer vision library essential for image processing and face recognition tasks.
  * **Python**: The primary programming language used for the project's logic and algorithms.
  * **Blynk Library**: Used for communication with the Android application for remote unlocking (implied by code in appendix).
  * **SMTP Library**: Enables sending email notifications for unauthorized access attempts (implied by code in appendix).

## How it Works

The system operates by continuously capturing images via the USB camera. These images are processed using a face recognition module. If a face is detected, it is compared against a database of authorized users.

  * **Authorized User**: If a match is found, the Raspberry Pi sends a signal to the relay, which in turn unlocks the electromagnetic door lock.
  * **Unknown Person**: If an unknown person is detected, an email notification is sent to authorized personnel. This notification includes information about the detection, and authorized users can choose to remotely unlock the door via a connected Android application if they wish to grant access.

The core face recognition algorithm utilizes the Haar cascade classifier, known for its high detection rate and low false positive/negative rates.

## Setup and Installation

1.  **Raspbian OS Setup**: Download the latest version of Raspbian and write it to an SD card using a tool like `win32 disk imager`. Insert the SD card into the Raspberry Pi and boot it up. Configure the file system to expand to the full SD card space and enable booting to the graphical desktop.
2.  **Update Firmware**: After booting, update the Raspberry Pi's firmware and packages using the following commands in the terminal:
    ```bash
    sudo rpi-update
    sudo apt-get update
    sudo apt-get upgrade
    sudo reboot
    ```
3.  **OpenCV 3 Installation**: Install OpenCV 3 on your Raspberry Pi. This involves several steps to gather all dependencies and compile the library. (Detailed steps are available in the project documentation).
4.  **Project Code**: Transfer the project's Python source code onto the Raspberry Pi.
5.  **Database Setup**: Create a database of known faces. The system involves an enrollment process to add authorized users by capturing their images and generating facial encodings.
6.  **Hardware Connection**: Connect the USB camera, electromagnetic lock (via relay), and other peripherals to the Raspberry Pi's USB ports and GPIO pins as per the circuit design.

## Authors

  * **Karanam Akhil** (20U41A0409)
  * **Nandana Sai Kumar** (20U41A0450)
  * **Botta Bhanu Lokesh** (20U41A0425)

## Acknowledgements

This project was developed under the esteemed guidance of **Mrs.G. Siva Kumari**, Assistant Professor, Department of Electronics & Communication Engineering. We extend our gratitude to Dr. P. Poorna Priya, Professor & Head of the Department of Electronics & Communication Engineering, and Principal Dr. R. Vaikunta Rao, Dadi Institute of Engineering & Technology, for their motivation and support.
