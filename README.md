# UndeleteX
This Python script utilizes the `pytsk3` library to scan and recover deleted files from a disk image or partition. It identifies deleted files based on the file system's metadata and provides functionality to recover these files to a specified output directory. The tool supports both Linux and Windows systems, given the appropriate permissions and libraries.

## Installation

### Prerequisites

Ensure you have Python 3.x installed on your system. The script requires the `pytsk3` library, which may have additional dependencies.

#### On Linux

1. **Install `pytsk3` and Dependencies**:

   ```bash
   sudo apt-get update
   sudo apt-get install python3-pytsk3 libtsk-dev libewf-dev
   ```
   
2. **Install Python Packages:**

  ```bash
    pip install pytsk3
  ```

#### On Windows

1. **Install Python Packages:**

    ```bash
      pip install pytsk3
    ```

2. **Install Additional Dependencies:**

    Follow the instructions on the (PyTSK GitHub page)[https://github.com/py4n6/pytsk] for Windows-specific setup.

## Configuration

1. **Set the Disk Path**:
   
   Open the `main.py` file and update the `disk_path` variable to point to the disk or partition you wish to analyze.

   ```python
   disk_path = "/dev/sda2"  # Replace with your actual disk or partition path
   ```

2. **Set the Output Directory:**

    Specify the directory where recovered files will be saved by modifying the output_dir parameter in the list_files function call.

    ```python

    list_files(fs, output_dir="/path/to/recover/directory")
      ```

## Running the Script
#### On Linux

  -Open a Terminal.

  -Navigate to the Directory Containing the Script:

    ```bash

      cd /path/to/your/script
      ```

  -Run the Script with Appropriate Permissions:

   Depending on your system configuration, you may need to run the script with sudo to access the disk or partition:

  ```bash

    sudo python3 main.py
  ```

  If you encounter permission issues, ensure you have the necessary access rights to the disk or partition.

#### On Windows

  -Open Command Prompt or PowerShell.

  -Navigate to the Directory Containing the Script:

    ```cmd

      cd C:\path\to\your\script
      ```

  -Run the Script:

    ```cmd

        python main.py
      ```

## Troubleshooting

  Permission Issues: Ensure you have read access to the disk or partition. On Linux, use sudo if necessary.
  Library Errors: Ensure all required libraries are installed and configured correctly. Refer to the Installation guide for setup instructions.
  Script Errors: If the script encounters errors, check the error messages for details. Common issues may include incorrect disk paths or file system compatibility.

## Contact

For additional support or questions, please reach out to issakasaddick14@gmail.com


