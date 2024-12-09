# Bitcoin-CPU-Mining-Script
Bitcoin CPU Mining Script
A lightweight Bitcoin CPU mining script designed to run on Termux or Linux-based systems using the Bash shell. This script connects to a mining pool monitors your mining progress and allows you to withdraw funds once the balance reaches $50. Built and maintained by Sagar Parajuli.

Features
CPU-only mining: Designed specifically for CPU mining without requiring a GPU.
Mining Pool Support: Connects to your preferred mining pool.
Low CPU Usage: Configurable CPU thread count to avoid overheating.
Automatic Withdrawal: Generates a unique blockchain-like hash during the withdrawal process.
Progress Monitoring: Displays balance and mining progress.
Bash & Termux Compatibility: Lightweight and easy to use on Linux-based systems or mobile devices with Termux.
Requirements
Termux or a Linux-based terminal environment.
cpuminer: A CPU mining tool.
Access to a mining pool that supports CPU mining.
A valid Bitcoin address.
Installation
1. Clone the Repository
Open your terminal or Termux and run:

bash
Copy code
git clone git@github.com:sagarparajul107/Bitcoin-CPU-Mining-Script.git
cd bitcoin-cpu-mining-script
2. Install cpuminer
Install cpuminer for your system:

bash
Copy code
apt update
apt install build-essential libssl-dev -y
git clone https://github.com/pooler/cpuminer.git
cd cpuminer
./autogen.sh
./configure
make
apt make install
3. Edit the Script
Edit the script.sh file to add your mining pool details and Bitcoin address:

bash
Copy code
nano script.sh
Replace the placeholders with:

MINER_ADDRESS: Your Bitcoin address.
POOL_URL: The mining pool's URL and port.
Usage
Make the Script Executable:

bash
Copy code
chmod +x script.sh
Run the Script: Start mining by running:

bash
Copy code
./script.sh
Monitor Progress:

The script will display your mining progress and balance.
Once the balance reaches $50, the withdrawal process will be triggered automatically, and a unique hash will be generated.
Configuration
You can configure the following parameters in the script.sh file:

WORKERS: Number of CPU threads to use for mining. Start with 1 and increase gradually if your system can handle it.
Mining Pool URL: Update the pool URL to the one provided by your mining pool.
Bitcoin Address: Replace with your personal Bitcoin address.
Example Workflow
The script starts mining using cpuminer.
Connects to the mining pool and uses your CPU to process blocks.
Periodically checks the balance using the mining pool API.
Automatically triggers a withdrawal and generates a hash when the balance reaches $50.
Notes
Avoid using too many CPU threads (WORKERS) to prevent system overheating or slowdown.
Ensure that you are connected to a stable network for uninterrupted mining.
Use mining pools with reliable APIs and low fees for better returns.
Troubleshooting
Permission Denied: Ensure the script is executable:
bash
Copy code
chmod +x script.sh
cpuminer not found: Ensure you installed cpuminer correctly and it is in your system's PATH.
Low Mining Speed: Check your CPU’s capability and try using a lower thread count (WORKERS).
Acknowledgments
This script is created and maintained by Sagar Parajuli. Feel free to contribute or report issues via the GitHub repository. 
 
