
# Sample Kotlin/Jetpack-Compose

This sample-android-blockchain is a Jetpack Compose Android project designed for transparent and secure donation tracking. This repository serves as a sample for creating Daytona workspaces for Android projects, utilizing Jetpack Compose and integrating blockchain technologies.

---

## Prerequisites
- You should have Android sdk in your local system. You can download it from [here](https://developer.android.com/tools/releases/platform-tools)
- The path to your platform-tools should be configured in the environmental variables *```Path```*. For example- ```C:\Users\Anurag\AppData\Local\Android\Sdk\platform-tools```

## 🚀 Getting Started

### Open Using Daytona
Follow these steps to set up and start working on the HopeChain-Daytona project using Daytona:

1. **Install Daytona**
   - Follow the [Daytona Installation Guide](https://github.com/daytonaio/daytona#installation) to set up Daytona on your system.

2. **Docker**
   - You should have to download Docker for isolating and configuration of the whole setup.
   
3. **Jetbrains Gateway**
   - Set up JetBrains Gateway to establish an SSH connection between the project and your IDE.
   [Jetbrains Gateway Installation Guide](https://www.jetbrains.com/remote-development/gateway/)

4. **Set Default IDE**
   - Choose Intellij Idea Ultimate as your default ide by the following command.
   ```bash
   daytona ide
   ```
5. **Create the Workspace**
   - Run the following command to create a workspace:
   ```bash
   daytona create https://github.com/daytonaio/sample-android-blockchain
   ```

7. **Open in IntelliJ IDEA Ultimate**
   - Daytona will automatically download and open the project in IntelliJ IDEA Ultimate, pre-configured with the necessary SDKs and tools otherwise try command ```daytona code``` in a new terminal.
   
8. **Required Plugin**
   - Install the Android plugin to configure the Android setup in IntelliJ IDEA Ultimate:

![Screenshot 2024-12-10 150555](https://github.com/user-attachments/assets/b996bc3a-a4d1-4eca-94a1-cd4a7ca2f703)

   - Open the Android SDK setup by clicking the directory icon.

![Screenshot 2024-12-10 151013](https://github.com/user-attachments/assets/e7c8250f-448e-45ce-b411-d4817e7c32ec)
![Screenshot 2024-12-10 151031](https://github.com/user-attachments/assets/4d5393ba-212e-4da8-86ed-292094c4433a)

   - Accept the license agreement and proceed.

![Screenshot 2024-12-10 151518](https://github.com/user-attachments/assets/7dcda1e6-a1cd-471b-9ea7-a9b174dbfddc)
![Screenshot 2024-12-10 152345](https://github.com/user-attachments/assets/ff3d0e65-7a53-4baf-b89c-0848e2194628)
![Screenshot 2024-12-10 152736](https://github.com/user-attachments/assets/1f51bc0f-ae67-40e4-8659-4aae84e7e49a)

   - After completing the steps outlined above, the Run and Devices section will appear at the top of your IntelliJ IDEA Ultimate interface.
   - Now go to the build section and click on generate apk.
     
     ![Screenshot 2024-12-15 182755](https://github.com/user-attachments/assets/723fecee-f433-4282-95ca-4c109dec66a7)
     
   - After your debug_apk is generated after sometime, go to the notifications to check the path where it has been generated.
     
     ![Screenshot 2024-12-15 031919](https://github.com/user-attachments/assets/5041a1a8-b013-4292-80a7-6d053cce0dfc)
   - Now to copy the apk file from the container to your host machine or local system, use the below command and put your apk file path and the path where you want the file to be stored on your local system.
     
     ```bash
     docker cp <CONTAINER_ID>:/home/daytona/sample-android-blockchain/app/build/outputs/apk/debug/app-debug.apk /path/to/destination/on/host
     ```
   - Note: You can find the Container_ID in the docker as well as in the ide itself.

9. **Run on your Physical Android device**
 - Note: Make sure you have enabled developer options to run the app on your android device.
   [Enable Developer Options](https://developer.android.com/studio/debug/dev-options)!
- Now connect your Android device to your system using a USB cable.
- Type command ```adb devices``` in the local terminal to list the connected devices. 
  ```bash
  adb devices
  ```
- Install the apk on your android device:
  ```bash
  adb install path/to/your-app.apk
  ```
- Run the app:
  ```bash
  adb shell am start -n com.example.hopechaindaytona/.MainActivity
  ```

Here is an demo screenshot of how to do so:

![Screenshot 2024-12-15 032459](https://github.com/user-attachments/assets/a64d5ca7-3911-4d60-8c1b-c5d6c2e86001)

- After running the app, you can see the HopeChain app:
  
  <img src="https://github.com/user-attachments/assets/55405640-dfe1-44f5-8769-78273896cc51" alt="Screenshot_20241109_204057" width="250"/>

---

## 📂 Project Structure
The repository contains the following components:
- **Jetpack Compose UI**: Fully composed UI designed for modern Android development.
- **Blockchain Integration**: Supports blockchain interactions using the Solana network.
- **Auto Builder Support**: auto-configured development container for consistent development environments.

---
