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
 
curl -LO https://github.com/esp-rs/rust-build/releases/download/v1.61.0.0/install-rust-toolchain.sh
chmod a+x install-rust-toolchain.sh
./install-rust-toolchain.sh
#install cargo feature that is needed

cargo install cargo-generate
cargo install ldproxy
cargo install espflash
cargo install espmonitor

#installing esp libraries

git clone https://github.com/esp-rs/rust-build.git
cd rust-build
./install-rust-toolchain.sh

#create project template

cargo generate --vcs none --git https://github.com/esp-rs/esp-idf-template cargo



