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

* >Whenever you are going to play the game, you need to open XLaunch everytime and do all the above process:

<img width="1941" height="378" alt="image" src="https://github.com/user-attachments/assets/8f63ac81-b4eb-4b3b-9d80-3198a5928708" />







---

## Install dependencies

```
sudo apt update
sudo apt install make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev curl git libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev zip unzip 
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

#### Install Python 3.10, psutil & readchar

```
pyenv install 3.10
```

```
pip install psutil readchar
```



