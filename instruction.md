1. If you don’t have Rust installed:

         # curl https://sh.rustup.rs -sSf | sh

  2. Install cross-compiler toolchain:

         # apt install gcc-aach64-linux-gnu libc6 libc6-dev

  3. Create a new shell, or to reuse the existing shell:

         source $HOME/.cargo/env

  4. Install rustc target toolchain:

         % rustup target install aarch64-unknown-linux-gnu

  5. Put this in testing/geckodriver/.cargo/config:

         [target.arrch64-unknown-linux-gnu]
         linker = "arrch64-linux-gnu-gcc"

  6. Build geckodriver from testing/geckodriver:

         % cd testing/geckodriver
         % cargo build --release --target aarch64-unknown-linux-gnu
