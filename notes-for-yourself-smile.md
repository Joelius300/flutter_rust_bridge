- Installed rustup directly (no AUR or repo)
- Installed flutter manually by cloning into the home directory
- `dart pub global activate ffigen`
- `cargo install flutter_rust_bridge_codegen`
- Install corrosion manually by cloning somewhere in a separate folder and following the [readme](https://github.com/corrosion-rs/corrosion#installation). Adjust [some configs](https://cjycode.com/flutter_rust_bridge/template/setup_desktop.html) (already done in this fork).
- Run generator. Has to be from root because of some bug?! so execute these commands inside the `with_flutter` folder.
  ```bash
  export CURR_DIR=$PWD && cd /
  flutter_rust_bridge_codegen --rust-input $CURR_DIR/rust/src/api.rs --dart-output $CURR_DIR/lib/bridge_generated.dart --c-output $CURR_DIR/ios/Runner/bridge_generated.h && cd $CURR_DIR
  ```

