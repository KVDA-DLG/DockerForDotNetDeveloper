# Docker For Dot Net Developer
## WSL2 with Docker Engine
WSL2 provides a lightweight Linux environment without the need for a full VM
Steps: Open PowerShell (Admin) and run:
- Check if WSL is enabled
```bash
wsl --list --verbose
```
Note: If WSL is not installed, proceed to the next step else skip next step.
- Install WSL2 and Ubuntu 22.04 LTS
```bash
   wsl --install -d Ubuntu-22.04
```
- If WSL is already installed, ensure it's set to version 2
```bash
wsl --set-default-version 2
```
- Install Docker Engine inside WSL
```bash
sudo apt update
sudo apt install -y docker.io
```
- Start and enable Docker
```bash
sudo systemctl enable --now docker
```
- Add your user to the Docker group
```bash
sudo usermod -aG docker $USER
```
- Test Docker
```bash
docker run hello-world
```
Enjoy!, Now you have Docker running inside WSL2 without Docker Desktop!
