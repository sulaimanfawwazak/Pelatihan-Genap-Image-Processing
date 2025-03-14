# **Setup | Pelatihan Genap 2025: Image Processing**

## **NOTE!!!**
- For this class, I highly encourage you to use Linux and get familiar with it. Such that, in this setup, even when you're using Windows, you'll have to install WSL (Windows Subsytem for Linux) to get the similar workflow as Linux.
- If you have any questions, don't hesitate to ask on the Whatsapp group chat or Microsoft Teams.

</br>

## **Windows**
-  **WSL (Windows Subsystem for Linux)**
	1. Open PowerShell or Command Prompt as Adminitrator and run: </br>
	```wsl --install```
	2. Restart your computer if needed
	3. Check the installation </br>
	```wsl --list --verbose```
	4. Install the Ubuntu 22.04 </br>
	```wsl --install -d Ubuntu-22.04```
	5. Seach and open Ubuntu WSL on the Start button

</br>

-  **Miniconda**
	1. Open the Ubuntu WSL
	2. Download the Miniconda Installer by running this command </br>
	```curl https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -o ~/Downloads/Miniconda3-latest-Linux-x86_64.sh```
	3. Run the installer by running this command: </br>
	```bash ~/Downloads/Miniconda3-latest-Linux- x86_64.sh```
	4. Follow the installer instruction
	5. Initialize the Miniconda by running this command: </br>
	```source ~/bashrc``` </br>
	or </br>
	```conda activate base``` </br>
	| **Side note**: `base` is the default environment, made by the Miniconda
	6. Check the installation result by running these commands: </br>
	```conda --version```
	7. Download the environment file using this command: </br>
	```wget -P ~/Downloads https://raw.githubusercontent.com/sulaimanfawwazak/Pelatihan-Vision-2025/main/environment.yml```

	8. Create the environment using this command </br>
	```conda env create --name imageproc -f ~/Downloads/environment.yml```
	9. Activate the environment </br>
	```conda activate imageproc```

</br>

-  **Jupyter Notebook**
	1. Open the Ubuntu WSL
	2. Activate the environment </br>
	```conda activate imageproc```
	3. Install Jupyter </br>
	```conda install -y jupyter```
	4. Install Conda Integration </br>
	```conda install -c conda-forge nb_conda```
	5. Install OpenCV </br>
	```conda install -c conda-forge opencv```
	6. Setup the Jupyter Kernel </br>
	```python -m ipykernel install --user --name viscon --display-name "Python (Image Processing)"```
	7. Run the Jupyter Notebook </br>
	```mkdir pelatihan-genap``` </br>
  ```cd pelatihan-genap``` </br>
  ```jupyter notebook```

</br>

-  **Visual Studio Code (VS Code)**
	1. Download the `.exe` file from https://code.visualstudio.com/
	2. Click twice on the downloaded file to start the installation
	3. Open the VS Code
	4. Open the extension menu
	5. Install these extensions:
		- Jupyter
		- Jupyter Keymap
		- Jupyter Notebook Renderes
		- Jupter Cell Tags
		- Jupyter Slide Show

</br>

-  **Additional Setup**
	1. Open the Ubuntu WSL
	2. Install these additional packages by running these commands: </br>
	```sudo apt install python-is-python3``` </br>
	```sudo apt install python3-pip``` 
	3. Deactivate the `base` environment by default when opening Terminal by running this command </br>
	```conda config --set auto_activate_base false```
	4. Create aliases to shorten the commands </br>
	```echo "alias ca="conda activate" >> ~/.bashrc``` </br>
	```echo "alias fixopenssl=\"export LD_LIBRARY_PATH=/lib/x86_64-linux-gnu:$LD_LIBRARY_PATH\"" >> ~/.bashrc```
	
</br>

## **Linux**
-  **Repository Update**
	1. Open the Terminal (`Ctrl + Alt + T`)
	2. Run these commands: </br>
	```sudo apt update``` </br>
	```sudo apt upgrade```

-  **Miniconda**
	1. Open the Terminal (`Ctrl + Alt + T`)
	2. Download the Linux Miniconda Installer </br>
	```curl https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -o ~/Downloads/Miniconda3-latest-Linux-x86_64.sh```
	3. Run the installer </br>
	```bash ~/Downloads/Miniconda3-latest-Linux- x86_64.sh```
	4. Follow the installer instructions
	5. Initialize the Miniconda: </br>
	```source ~/bashrc``` </br>
	or </br>
	```conda activate base``` </br>
	| **Side note**: `base` is the default environment, made by the Miniconda
	6. Check the installation result </br>
	```conda --version```
	7. Download the environment file </br>
	```wget -P ~/Downloads https://raw.githubusercontent.com/sulaimanfawwazak/Pelatihan-Vision-2025/main/environment.yml```
	8. Create the environment </br>
	```conda env create --name imageproc -f ~/Downloads/environment.yml```
	9. Activate the environment </br>
	```conda activate imageproc```

</br>

-  **Jupyter Notebook**
	1. Open the Terminal (`Ctrl + Alt + T`)
	2. Activate the environment </br>
	```conda activate imageproc```
	3. Install Jupyter </br>
	```conda install -y jupyter```
	4. Install Conda Integration </br>
	```conda install -c conda-forge nb_conda```
	5. Install OpenCV </br>
	```conda install -c conda-forge opencv```
	6. Setup the Jupyter Kernel </br>
	```python -m ipykernel install --user --name imageproc --display-name "Python (Image Processing)"```
	7. Run the Jupyter Notebook </br>
	```mkdir pelatihan-genap``` </br>
	```cd pelatihan-genap``` </br>
	```jupyter notebook```

</br>

-  **Visual Studio Code (VS Code)**
	1. Open the Terminal (`Ctrl + Alt + T`)
	2. Install the VS Code </br>
	```sudo snap install --classic code```
	3. Open the VS Code
	4. Open the extension menu
	5. Install these extensions:
		- Jupyter
		- Jupyter Keymap
		- Jupyter Notebook Renderes
		- Jupter Cell Tags
		- Jupyter Slide Show

</br>  

-  **Additional Setup**
	1. Open the Terminal (`Ctrl + Alt + T`)
	2. Install these additional packages by running these commands: </br>
	```sudo apt install python-is-python3``` </br>
	```sudo apt install python3-pip```
	3. Deactivate the `base` environment by default when opening Terminal by running this command: </br>
	```conda config --set auto_activate_base false```
	4. Create aliases to shorten the commands </br>
	```echo "alias ca="conda activate" >> ~/.bashrc``` </br>
	```echo "alias fixopenssl=\"export LD_LIBRARY_PATH=/lib/x86_64-linux-gnu:$LD_LIBRARY_PATH\"" >> ~/.bashrc```

</br>

## **MacOS**
-  **Homebrew**
	1. Open the Terminal
	2. Install Homebrew (if not installed) </br>
	```/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"```
	3. Verify the installation </br>
	```brew --version```

</br>

-  **Miniconda**
	1. Open the Terminal
	2. Download the MacOS Miniconda Installer </br>
	```curl https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh -o ~/Downloads/Miniconda3-latest-MacOSX.sh```
	3. Run the installer </br>
	```bash ~/Downloads/Miniconda3-latest-MacOSX.sh```
	4. Follow the installer instructions
	5. Initialize Miniconda </br>
	```source ~/.zshrc``` </br>
	or </br>
	```conda activate base``` </br>
	| **Side note**: `base` is the default environment, made by the Miniconda
	6. Download the environment file </br>
	```wget -P ~/Downloads https://raw.githubusercontent.com/sulaimanfawwazak/Pelatihan-Vision-2025/main/environment.yml```
	7. Create the environment </br>
	```conda env create --name imageproc -f ~/Downloads/environment.yml```
	8. Activate the environment </br>
	```conda activate imageproc```

</br>

-  **Jupyter Notebook**
	1. Open the Terminal
	2. Activate the environment </br>
	```conda activate imageproc```
	3. Install Jupyter </br>
	```conda install -y jupyter```
	4. Install additional dependencies </br>
	```conda install -c conda-forge nb_conda opencv```
	5. Setup the Jupyter Kernel </br>
	```python -m ipykernel install --user --name imageproc --display-name "Python (Image Processing)"```
	6. Run the Jupyter Notebook </br>
	```mkdir pelatihan-genap``` </br>
	```cd pelatihan-genap``` </br>
	```jupyter notebook```
  
</br>

-  **Visual Studio Code (VS Code)**
	1. Download the `.zip` file from https://code.visualstudio.com/
	2. Click twice on the downloaded file to start the installation
	3. Open the VS Code
	4. Open the extension menu
	5. Install these extensions:
		- Jupyter
		- Jupyter Keymap
		- Jupyter Notebook Renderes
		- Jupter Cell Tags
		- Jupyter Slide Show

</br>  

-  **Additional Setup**
	1. Make `python` alias
	```echo "alias python=python3" >> ~/.zshrc``` </br>
	```source ~/.zshrc```
	2. Deactivate the `base` environment by default when opening Terminal by running this command: </br>
	```conda config --set auto_activate_base false```
	3. Create aliases to shorten the commands </br>
	```echo "alias ca="conda activate" >> ~/.zshrc``` </br>
	```echo "alias fixopenssl=\"export LD_LIBRARY_PATH=/lib/x86_64-linux-gnu:$LD_LIBRARY_PATH\"" >> ~/.zshrc```

</br>

## **Resources**
- [https://github.com/jeffheaton/t81_558_deep_learning/blob/master/install/manual_setup3.ipynb](https://github.com/jeffheaton/t81_558_deep_learning/blob/master/install/manual_setup3.ipynb)
- [https://www.youtube.com/watch?v=eId6K8d0v6o&pp=ygUgaG93IHRvIGluc3RhbGwgd3NsIG9uIHdpbmRvd3MgMTE%3D](https://www.youtube.com/watch?v=eId6K8d0v6o&pp=ygUgaG93IHRvIGluc3RhbGwgd3NsIG9uIHdpbmRvd3MgMTE%3D)

</br>

-S. Fawwaz A. K