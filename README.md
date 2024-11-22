# 📞 SIP Message Analyzer

A Python script that analyzes SIP (Session Initiation Protocol) messages from PCAP files, extracting key information such as REGISTER and INVITE messages along with their network parameters.

## ✨ Features

- 📁 Processes multiple PCAP files from a designated folder
- 🔍 Extracts SIP messages (REGISTER and INVITE)
- 📋 Parses important headers including:
  - To/From headers with parameters
  - P-Access-Network-Info
  - Cellular-Network-Info
- 📊 Generates detailed analysis reports in text format
- 📈 Provides summary statistics for each PCAP file
- 🔄 Progress bars for both file and packet processing
- 🖥️ User-friendly GUI dialogs for directory selection

## 🔧 Requirements

- Python 3.x
- Wireshark/TShark (must be installed on your system)
- Required Python packages (for development):
  ```bash
  pip install -r requirements.txt
  ```

## 🚀 Development Setup

1. Clone the repository:
   ```bash
   git clone [repository-url]
   cd sip-analyzer
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv .venv
   .\.venv\Scripts\activate  # Windows
   source .venv/bin/activate # Linux/Mac
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the script directly:
   ```bash
   python sip-script.py
   ```

## 📦 Packaging as Executable

1. Ensure you have all requirements installed:
   ```bash
   pip install -r requirements.txt
   ```

2. Place your icon file (optional):
   - Add a PNG file named `android-chrome-120x120.png`
   - It will be automatically converted to ICO format

3. Build the executable:
   ```bash
   # Using virtual environment
   .\.venv\Scripts\pyinstaller.exe build_exe.spec
   
   # Or using Python module
   python -m PyInstaller build_exe.spec
   ```

4. Find the executable in the `dist` folder:
   - `dist/SIP-Analyzer.exe`

## 📥 Distribution Package

Create a distribution package by:
1. Creating a new folder named `SIP-Analyzer-Package`
2. Copying `dist/SIP-Analyzer.exe` into it
3. Including the README.txt file
4. (Optional) Adding sample PCAP files

## 🎯 End-User Usage

1. Install Prerequisites:
   - Install Wireshark/TShark on your system
   - Ensure it's added to system PATH

2. Run the Application:
   - Double-click `SIP-Analyzer.exe`
   - Select folder containing PCAP files when prompted
   - Choose output directory for analysis
   - Wait for processing to complete
   - Check output directory for results

## 📄 Output Format

The analyzer generates text files containing:
- Analysis summary with timestamp
- Total packet counts
- REGISTER and INVITE message counts
- Detailed message information including:
  - Message type
  - Timestamp
  - To/From headers
  - Network information
  - Cell IDs

## ⚠️ Error Handling

The script includes error handling for:
- Missing traces directory
- No PCAP files found
- TShark crashes
- Missing packet attributes
- General exceptions

## 🔍 Supported SIP Headers

The script extracts and parses:
- Message Type (REGISTER/INVITE)
- Timestamp
- To Header
- From Header
- P-Access-Network-Info with parameters
- Cellular-Network-Info with parameters

## 📚 Additional Resources

- [SIP Protocol RFC 3261](https://tools.ietf.org/html/rfc3261)
- [Wireshark Documentation](https://www.wireshark.org/docs/)
- [pyshark Documentation](https://kiminewt.github.io/pyshark/)

## 🐛 Known Issues

- Large PCAP files may require significant processing time
- Memory usage increases with file size
- TShark must be installed and accessible in system PATH

## 📄 License

MIT License

## 🤝 Contributing

1. Fork the repository
2. Create a new branch for your feature
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

Created with ❤️ by M. ElSakka

For support, contact: support@astravision.ai