<div align="left">

##   **Introduction📔**

BlockAssist is an AI assistant that learns from its user’s actions in Minecraft. The assistant appears in-game with you, starting with only basic knowledge of the game’s commands. As you play, it learns how to assist you in building, learning directly from your actions. It shows an early demo of assistance learning - a new paradigm for aligning agents to human preferences across domains.

</div>


<div align="center">

#  👨🏻‍💻 **Genysn BlockAssist Guide** 👨🏻‍💻 

<img width="1024" height="576" alt="image" src="https://github.com/user-attachments/assets/a9e2a194-4824-4cfc-89dd-dae78a6cd75d" />


</div>


## Device/System Requirements 💻

* >Minimum RAM = 8GB 

* >50-100 GB disk space

* >Multi‑core CPU

* >Wont work in VPS (Cpu based) , GPU require


# Pre-Requirements 🛠

## Install NVIDIA Game Ready Driver {IMPORTANT}

* >Go To: [DOWNLOAD](https://www.nvidia.com/en-us/drivers/)

* >Select your GPU, Window Vrsoin & Press `Find`

* >Click on `View` & Download the `GeForce Game Ready Driver` 

* >After Dow, Open it & Do all the processes to Install it into Your Machine:

* >Restart Your PC to make changes:

## Install VcXsrv Windows X Server

* [Download VcXsrv](https://sourceforge.net/projects/vcxsrv/)

* >Now open the XLaunch (VcXsrv) From Start icon:

* >Check `Multiple windows` ✔️

* >Check `Start no client` ✔️

* >Check `Disable access control` ✔️

* >Next & Finish: It gonna run on background:

* >❗Whenever you are going to play the game, you need to open XLaunch everytime and do all the above process:

<img width="1941" height="378" alt="image" src="https://github.com/user-attachments/assets/8f63ac81-b4eb-4b3b-9d80-3198a5928708" />


### Set DISPLAY and Audio to ~/.bashrc

```
echo -e '\n# WSL2 VcXsrv display setup\nexport DISPLAY=$(ip route | grep -m1 default | awk '"'"'{print $3}'"'"'):0.0\nexport LIBGL_ALWAYS_INDIRECT=0\nexport LIBGL_DEBUG=verbose' >> ~/.bashrc
```

* Reload ~/.bashrc

```
source ~/.bashrc
```

### Test VcXsrv

```
xeyes
```

>If a New Tab got pop-up with `EYES`, Than VcXsrv has set-up perfectly:

<img width="229" height="146" alt="Screenshot 2025-08-14 005355" src="https://github.com/user-attachments/assets/3e48848c-73be-45a4-9602-130a1ac6614e" />


## Get Hugging Face API token

#### 1. Go To: [huggingface.co](https://huggingface.co/) & Sign Up with Mail:

#### 2. Verify Your Email

#### 3. Generate a New Access Token

* >Click your profile icon (top right corner)

* >Select “Access Tokens” from the dropdown

* >Click “New token”

* >Name: something like “BlockAssist”

* >Role: choose Write

* >Click “Create”

#### 4. Copy & Save the token immediately - you won’t be able to see it again

#### 5. 📋 Lost it? Just delete the token and create a new one

---

## Install dependencies

```
sudo apt update
sudo apt install make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev curl git libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev zip unzip mesa-utils x11-apps
```

---

## Clone & move to blockassist Repo:

```
git clone https://github.com/gensyn-ai/blockassist.git
cd blockassist
```

### Install Java 1.8.0_152

```
./setup.sh
```

### Install pyenv

```
curl -fsSL https://pyenv.run | bash
```

* Add pyenv to your shell

```
cat <<'EOF' >> ~/.bashrc

# Pyenv setup
export PYENV_ROOT="$HOME/.pyenv"
[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init - bash)"
eval "$(pyenv virtualenv-init -)"
EOF
```

* Reload

```
source ~/.bashrc
```

### Install Python 3.10, psutil & readchar

```
pyenv install 3.10
```

```
pip install psutil readchar
```

---

## Run BlockAssist 🚀

#### 1. Move to blockassist Directory

```
cd blockassist
```

#### 2. Activate the `blockassist-venv` Environment

```
source blockassist-venv/bin/activate
```

#### 3. Make sure XLaunch (VcXsrv) running in background

#### 4. Start the BlockAssist

```
python run.py
```

#### 5. Enter Huggingface Token From [HERE]

