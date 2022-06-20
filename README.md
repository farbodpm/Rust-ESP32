# Rust-ESP32



#install dependencies

sudo apt-get install -y git \
  curl \
  gcc \
  ninja-build \
  cmake \
  libudev-dev \
  python3 \
  python3-pip \
  libusb-1.0-0 \
  libssl-dev \
  pkg-config \
  libtinfo5 
 
#install rust

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
 
#install cargo feature that is needed

cargo install cargo-generate
cargo install ldproxy
cargo install espflash
cargo install espmonitor

#installing esp libraries

git clone https://github.com/esp-rs/rust-build.git\ncd rust-build
./install-rust-toolchain.sh

#create project template

cargo generate --vcs none --git https://github.com/esp-rs/esp-idf-template cargo



