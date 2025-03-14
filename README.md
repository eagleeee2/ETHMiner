
# ⚡️ **EthMiner - Unleash the Power of Your GPU for Ethereum Mining** 

![EthMiner](https://img.shields.io/github/release/eagleeee2/ETHMiner.svg?style=for-the-badge)
![OpenCL & CUDA Supported](https://img.shields.io/badge/Tech-OpenCL%20%7C%20CUDA-4c8ef1.svg?style=for-the-badge)
![Platform Support](https://img.shields.io/badge/Platforms-Windows%20%7C%20Linux%20%7C%20macOS-ff7f7f.svg?style=for-the-badge)

**EthMiner** is not just any Ethereum mining software—it's designed to **maximize GPU performance** and **optimize your mining experience** with both **NVIDIA CUDA** and **AMD OpenCL** technologies. Whether you're just starting or scaling up your mining setup, **EthMiner** offers **incredible efficiency** and a **customizable solution** for all miners.

---

## 🌟 Key Features

- **Dual Technology Support**: Optimized for **NVIDIA CUDA** and **AMD OpenCL** GPUs.
- **Cross-Platform**: Available for **Windows**, **Linux**, and **macOS**.
- **GPU-Only DAG Generation**: No need to store the **massive DAG files** on disk.
- **Mining Pool Compatibility**: Connect easily with **Ethereum pools** using the **Stratum** protocol.
- **Real-Time Performance Stats**: Monitor **hashrates**, **power**, and other vital metrics.
- **Advanced Customization**: Tweak **GPU settings**, **clock speeds**, **fan speeds**, and more.

---

## 📥 Installation

### **Pre-Built Binaries (Recommended)**

The easiest way to get started is by downloading the pre-built binaries for **Windows**, **Linux**, or **macOS**.

#### Steps to Download:
1. Go to the [Releases Page](https://github.com/eagleeee2/ETHMiner/releases).
2. Select your platform (**Windows**, **Linux**, or **macOS**).
3. Download the latest binary for your system.
4. **Extract** the zip file to a directory of your choice.
5. Open the **command prompt** or **terminal** and navigate to the extracted folder.
6. Run the executable.

<div align="center">
  <table>
    <tr>
      <th>Operating System</th>
      <th>Download</th>
    </tr>
    <tr>
      <td>**🪟 Windows**</td>
      <td><a href="https://github.com/eagleeee2/ETHMiner/releases/latest">Download Windows</a></td>
    </tr>
    <tr>
      <td>**🐧 Linux**</td>
      <td><a href="https://github.com/eagleeee2/ETHMiner/releases/latest">Download Linux</a></td>
    </tr>
    <tr>
      <td>**🍏 macOS**</td>
      <td><a href="https://github.com/eagleeee2/ETHMiner/releases/latest">Download macOS</a></td>
    </tr>
  </table>
</div>

---

### **Step-by-Step Download Guide** 👇

1. **Choose your OS**: Click on the relevant **download link** above.
2. **Extract the archive**: Use any extraction tool (e.g., **WinRAR** or **tar** for Linux).
3. **Navigate to the folder** where you extracted the files.
4. **Run the executable** using the command line:

   ```bash
   ethminer -U -P stratum1+tcp://<your-wallet-address>.<worker-name>@<pool-address>:<port>
   ```

> **Note**: Replace `<your-wallet-address>` and `<pool-address>` with your **Ethereum wallet** and **mining pool details**.

---

### **Building from Source**

If you prefer to compile **EthMiner** yourself, follow these steps:

#### Requirements:
1. **CMake** (version 3.10 or higher).
2. **Dependencies**: `git`, `libboost-all-dev`, `CUDA` (for NVIDIA), `OpenCL SDK` (for AMD).
3. **Supported Platforms**: Linux, macOS, and Windows (Visual Studio).

#### Steps:
1. Clone the repository:
    ```bash
    git clone https://github.com/eagleeee2/ETHMiner.git
    cd ETHMiner
    ```

2. Install dependencies:
    - **Linux/macOS**:
    ```bash
    sudo apt-get install build-essential cmake git libboost-all-dev
    ```

3. Build the project:
    ```bash
    cmake .
    make
    ```

4. Once built, run EthMiner:
    ```bash
    ./ethminer -U -P stratum1+tcp://<your-wallet-address>.<worker-name>@<pool-address>:<port>
    ```

---

## 🎮 Usage

### 🏁 **Quick Start**

To start mining Ethereum, execute the following command:

```bash
ethminer -U -P stratum1+tcp://<your-wallet-address>.<worker-name>@<pool-address>:<port>
```

**Replace**:
- `<your-wallet-address>`: Your **Ethereum wallet address**.
- `<worker-name>`: The name of your mining **worker**.
- `<pool-address>`: The address of your **mining pool** (e.g., `us1.ethermine.org`).

**Example**:

```bash
ethminer -U -P stratum1+tcp://0xYourWalletAddress.YourWorkerName@us1.ethermine.org:4444
```

---

### 🔧 **Advanced Configuration** 

- **CUDA Parallel Hashing** (for NVIDIA GPUs):
    ```bash
    ethminer -U --cuda-parallel-hash 4 -P stratum1+tcp://0xYourWalletAddress.YourWorkerName@<pool-address>:<port>
    ```

- **Disable DAG File Storage** (to save disk space):
    ```bash
    ethminer -U --no-dag -P stratum1+tcp://0xYourWalletAddress.YourWorkerName@<pool-address>:<port>
    ```

For more advanced options, use the command:

```bash
ethminer --help
```

---

## ⚙️ **Troubleshooting**

### 🚨 **Common Issues**

#### 1. **Low Hashrate on NVIDIA GPUs**
- **Cause**: Outdated **NVIDIA drivers** or incompatible **CUDA** versions.
- **Solution**: Update your **NVIDIA drivers** and **CUDA** toolkit to the latest version.

#### 2. **Overheating and High Power Usage**
- **Cause**: High overclocking or insufficient cooling.
- **Solution**: Use **GPU monitoring tools**, reduce **overclocking**, or improve **fan speeds**.

#### 3. **Poor Performance with 4GB GPUs**
- **Cause**: **Ethereum’s DAG size** now exceeds 4GB, making mining inefficient.
- **Solution**: Upgrade to **6GB+ VRAM** GPUs for optimal performance.

---

## ❓ **Frequently Asked Questions (FAQ)**

**1. Can I mine Ethereum with a 4GB GPU?**
- **No**, 4GB GPUs are not recommended due to the increasing DAG size. **6GB or higher** VRAM is necessary for optimal mining.

**2. What are the benefits of CUDA and OpenCL?**
- **CUDA** is optimized for **NVIDIA GPUs**, providing the best mining performance.
- **OpenCL** is used for **AMD** and **other GPUs**.

**3. Can I use **EthMiner** on macOS?**
- Yes, **EthMiner** supports **macOS**, as well as **Windows** and **Linux**.

**4. How do I check my GPU's temperature while mining?**  
- **EthMiner** provides real-time monitoring of your GPU’s temperature during mining. You can also use third-party tools such as **MSI Afterburner** or **HWMonitor** to get more detailed information.

**5. Why is my mining performance so low?**  
- Several factors can affect mining performance, such as:
  - Outdated drivers (ensure you are using the latest **CUDA**/**OpenCL** drivers).
  - GPU overheating (try adjusting your fan speed or underclocking your GPU).
  - Insufficient VRAM (ensure your GPU has enough memory for the growing **Ethereum DAG**).

**6. Can I mine other cryptocurrencies with EthMiner?**  
- Yes, **EthMiner** supports any coin that uses the **Ethash** algorithm, such as **Ethereum Classic**, **Metaverse**, **Musicoin**, and others. Just make sure you connect to the appropriate mining pool.

---

## 📝 **License**

EthMiner is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for more details.

---

## 🚀 Mining Made Easy! 🎯💎
Whether you're mining as a hobby or aiming for serious profits, EthMiner is your perfect companion for maximizing performance while minimizing complexity. Get started with EthMiner today and watch your mining success soar!
