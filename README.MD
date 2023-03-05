# Debian and Ubuntu apt repos

## bionic (arm64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb bionic main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

## focal (x86_64 / arm64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb focal main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

## jammy (x86_64 / arm64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb jammy main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

## kinetic (x86_64 / arm64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb kinetic main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

## lunar (x86_64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb lunar main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

## bullseye (x86_64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb bullseye main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

## bookworm (x86_64)
```
echo "deb https://minecraft-linux.github.io/pkg/deb bookworm main" | sudo tee /etc/apt/sources.list.d/minecraft-linux-pkg.list
```

## trust the apt repo to install packages

```
curl -sS https://minecraft-linux.github.io/pkg/deb/pubkey.gpg | sudo tee -a /etc/apt/trusted.gpg.d/minecraft-linux-pkg.asc
```

# Fedora rpm repos
## 36 (x86_64)
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

## 37 (x86_64)
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