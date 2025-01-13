# mcpelauncher package repository

Please read https://minecraft-linux.github.io for available packages.

# Debian and Ubuntu apt repos

## trust the apt repo to install packages

First of all your system have to trust the gpg key used to sign the repository, then you can add the distribution specfic apt repo.

```
curl -sS https://minecraft-linux.github.io/pkg/deb/pubkey.gpg | sudo tee -a /etc/apt/trusted.gpg.d/minecraft-linux-pkg.asc
```

## Releases

Releases before including v0.9.0 don't provide arm64 for debian, you may need to add the nightly repo to install the arm64 version.
Releases before including v0.11.4 don't provide armhf for debian, you may need to add the nightly repo to install the armhf version.
Releases before including v0.11.4 don't provide fedora 39 packages, you may need to add the nightly repo to install the fedora 39 version.

### focal (x86_64 / arm64)
```
echo "deb [arch=amd64,arm64] https://minecraft-linux.github.io/pkg/deb focal main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### jammy (x86_64 / arm64)
```
echo "deb [arch=amd64,arm64] https://minecraft-linux.github.io/pkg/deb jammy main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### kinetic (x86_64 / arm64)
```
echo "deb [arch=amd64,arm64] https://minecraft-linux.github.io/pkg/deb kinetic main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### noble (x86_64 / arm64)
```
echo "deb [arch=amd64,arm64] https://minecraft-linux.github.io/pkg/deb noble main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### oracular (x86_64 / arm64)
```
echo "deb [arch=amd64,arm64] https://minecraft-linux.github.io/pkg/deb oracular main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### bullseye (x86_64 / arm64 / armhf)
```
echo "deb [arch=amd64,arm64,armhf] https://minecraft-linux.github.io/pkg/deb bullseye main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### bookworm (x86_64 / arm64 / armhf)
```
echo "deb [arch=amd64,arm64,armhf] https://minecraft-linux.github.io/pkg/deb bookworm main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

## Nightly

### focal (x86_64 / arm64)
```
echo "deb [arch=amd64,arm64] https://minecraft-linux.github.io/pkg/deb focal-nightly main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### jammy (x86_64 / arm64)
```
echo "deb [arch=amd64,arm64] https://minecraft-linux.github.io/pkg/deb jammy-nightly main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### kinetic (x86_64 / arm64)
```
echo "deb [arch=amd64,arm64] https://minecraft-linux.github.io/pkg/deb kinetic-nightly main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### noble (x86_64 / arm64)
```
echo "deb [arch=amd64,arm64] https://minecraft-linux.github.io/pkg/deb noble-nightly main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### bullseye (x86_64 / arm64 / armhf)
```
echo "deb [arch=amd64,arm64,armhf] https://minecraft-linux.github.io/pkg/deb bullseye-nightly main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### bookworm (x86_64 / arm64 / armhf)
```
echo "deb [arch=amd64,arm64,armhf] https://minecraft-linux.github.io/pkg/deb bookworm-nightly main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

# Fedora rpm repos

## Releases

Releases before including v0.9.0 don't provide arm64, you may need to add the nightly repo to install the arm64 version.
Releases before including v0.11.4 don't provide fedora 39 packages, you may need to add the nightly repo to install the fedora 39 version.

### 36 (x86_64 / arm64) (**Deprecated** v0.11.4 is the last version)
```
cat | sudo tee /etc/yum.repos.d/minecraft-linux-pkg.repo << 'EOF'
[minecraft-linux-pkg]
name=minecraft-linux-pkg
baseurl=https://minecraft-linux.github.io/pkg/fedora-36
enabled=1
countme=1
repo_gpgcheck=0
type=rpm
gpgcheck=1
skip_if_unavailable=False
gpgkey=https://minecraft-linux.github.io/pkg/deb/pubkey.gpg
EOF
```

### 37 (x86_64 / arm64) (**Deprecated** v0.11.4 is the last version)
```
cat | sudo tee /etc/yum.repos.d/minecraft-linux-pkg.repo << 'EOF'
[minecraft-linux-pkg]
name=minecraft-linux-pkg
baseurl=https://minecraft-linux.github.io/pkg/fedora-37
enabled=1
countme=1
repo_gpgcheck=0
type=rpm
gpgcheck=1
skip_if_unavailable=False
gpgkey=https://minecraft-linux.github.io/pkg/deb/pubkey.gpg
EOF
```

### 38 (x86_64 / arm64)
```
cat | sudo tee /etc/yum.repos.d/minecraft-linux-pkg.repo << 'EOF'
[minecraft-linux-pkg]
name=minecraft-linux-pkg
baseurl=https://minecraft-linux.github.io/pkg/fedora-38
enabled=1
countme=1
repo_gpgcheck=0
type=rpm
gpgcheck=1
skip_if_unavailable=False
gpgkey=https://minecraft-linux.github.io/pkg/deb/pubkey.gpg
EOF
```

### 39 (x86_64 / arm64)
```
cat | sudo tee /etc/yum.repos.d/minecraft-linux-pkg.repo << 'EOF'
[minecraft-linux-pkg]
name=minecraft-linux-pkg
baseurl=https://minecraft-linux.github.io/pkg/fedora-39
enabled=1
countme=1
repo_gpgcheck=0
type=rpm
gpgcheck=1
skip_if_unavailable=False
gpgkey=https://minecraft-linux.github.io/pkg/deb/pubkey.gpg
EOF
```

### 40 (x86_64 ~~/ arm64~~)
```
cat | sudo tee /etc/yum.repos.d/minecraft-linux-pkg.repo << 'EOF'
[minecraft-linux-pkg]
name=minecraft-linux-pkg
baseurl=https://minecraft-linux.github.io/pkg/fedora-40
enabled=1
countme=1
repo_gpgcheck=0
type=rpm
gpgcheck=1
skip_if_unavailable=False
gpgkey=https://minecraft-linux.github.io/pkg/deb/pubkey.gpg
EOF
```

### 41 (x86_64 ~~/ arm64~~)
```
cat | sudo tee /etc/yum.repos.d/minecraft-linux-pkg.repo << 'EOF'
[minecraft-linux-pkg]
name=minecraft-linux-pkg
baseurl=https://minecraft-linux.github.io/pkg/fedora-41
enabled=1
countme=1
repo_gpgcheck=0
type=rpm
gpgcheck=1
skip_if_unavailable=False
gpgkey=https://minecraft-linux.github.io/pkg/deb/pubkey.gpg
EOF
```

## Nightly

### 38 (x86_64 / arm64)
```
cat | sudo tee /etc/yum.repos.d/minecraft-linux-pkg.repo << 'EOF'
[minecraft-linux-pkg]
name=minecraft-linux-pkg
baseurl=https://minecraft-linux.github.io/pkg/fedora-38-nightly
enabled=1
countme=1
repo_gpgcheck=0
type=rpm
gpgcheck=1
skip_if_unavailable=False
gpgkey=https://minecraft-linux.github.io/pkg/deb/pubkey.gpg
EOF
```

### 39 (x86_64 / arm64)
```
cat | sudo tee /etc/yum.repos.d/minecraft-linux-pkg.repo << 'EOF'
[minecraft-linux-pkg]
name=minecraft-linux-pkg
baseurl=https://minecraft-linux.github.io/pkg/fedora-39-nightly
enabled=1
countme=1
repo_gpgcheck=0
type=rpm
gpgcheck=1
skip_if_unavailable=False
gpgkey=https://minecraft-linux.github.io/pkg/deb/pubkey.gpg
EOF
```

### 40 (x86_64 / arm64)
```
cat | sudo tee /etc/yum.repos.d/minecraft-linux-pkg.repo << 'EOF'
[minecraft-linux-pkg]
name=minecraft-linux-pkg
baseurl=https://minecraft-linux.github.io/pkg/fedora-40-nightly
enabled=1
countme=1
repo_gpgcheck=0
type=rpm
gpgcheck=1
skip_if_unavailable=False
gpgkey=https://minecraft-linux.github.io/pkg/deb/pubkey.gpg
EOF
```

### 41 (x86_64 / arm64)
```
cat | sudo tee /etc/yum.repos.d/minecraft-linux-pkg.repo << 'EOF'
[minecraft-linux-pkg]
name=minecraft-linux-pkg
baseurl=https://minecraft-linux.github.io/pkg/fedora-41-nightly
enabled=1
countme=1
repo_gpgcheck=0
type=rpm
gpgcheck=1
skip_if_unavailable=False
gpgkey=https://minecraft-linux.github.io/pkg/deb/pubkey.gpg
EOF
```
