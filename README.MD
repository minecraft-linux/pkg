# Debian and Ubuntu apt repos

## trust the apt repo to install packages

First of all your system have to trust the gpg key used to sign the repository, then you can add the distribution specfic apt repo.

```
curl -sS https://minecraft-linux.github.io/pkg/deb/pubkey.gpg | sudo tee -a /etc/apt/trusted.gpg.d/minecraft-linux-pkg.asc
```

## Releases

### bionic (arm64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb bionic main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### focal (x86_64 / arm64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb focal main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### jammy (x86_64 / arm64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb jammy main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### kinetic (x86_64 / arm64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb kinetic main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### lunar (x86_64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb lunar main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### bullseye (x86_64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb bullseye main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### bookworm (x86_64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb bookworm main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

## Nightly

### bionic (arm64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb bionic-nightly main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### focal (x86_64 / arm64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb focal-nightly main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### jammy (x86_64 / arm64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb jammy-nightly main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### kinetic (x86_64 / arm64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb kinetic-nightly main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### lunar (x86_64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb lunar-nightly main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### bullseye (x86_64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb bullseye-nightly main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

### bookworm (x86_64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb bookworm-nightly main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

# Fedora rpm repos

## Releases

### 36 (x86_64)
```
cat | sudo tee /etc/yum.repos.d/minecraft-linux-pkg.repo << EOF
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

### 37 (x86_64)
```
cat | sudo tee /etc/yum.repos.d/minecraft-linux-pkg.repo << EOF
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
## Nightly

### 36 (x86_64)
```
cat | sudo tee /etc/yum.repos.d/minecraft-linux-pkg.repo << EOF
[minecraft-linux-pkg]
name=minecraft-linux-pkg
baseurl=https://minecraft-linux.github.io/pkg/fedora-36-nightly
enabled=1
countme=1
repo_gpgcheck=0
type=rpm
gpgcheck=1
skip_if_unavailable=False
gpgkey=https://minecraft-linux.github.io/pkg/deb/pubkey.gpg
EOF
```

### 37 (x86_64)
```
cat | sudo tee /etc/yum.repos.d/minecraft-linux-pkg.repo << EOF
[minecraft-linux-pkg]
name=minecraft-linux-pkg
baseurl=https://minecraft-linux.github.io/pkg/fedora-37-nightly
enabled=1
countme=1
repo_gpgcheck=0
type=rpm
gpgcheck=1
skip_if_unavailable=False
gpgkey=https://minecraft-linux.github.io/pkg/deb/pubkey.gpg
EOF
```