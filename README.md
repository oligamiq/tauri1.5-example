# Tauri + Solid + Typescript

This template should help get you started developing with Tauri, Solid and Typescript in Vite.

## Recommended IDE Setup

- [VS Code](https://code.visualstudio.com/) + [Tauri](https://marketplace.visualstudio.com/items?itemName=tauri-apps.tauri-vscode) + [rust-analyzer](https://marketplace.visualstudio.com/items?itemName=rust-lang.rust-analyzer)

# install android
`npm run tauri android build`

`java -jar ./bundletool-all-1.15.5.jar build-apks --bundle=src-tauri\gen\android\app\build\outputs\bundle\universalRelease\app-universal-release.aab --output=signed.apks`
`java -jar ./bundletool-all-1.15.5.jar install-apks --apks=signed.apks`

rewrite signingConfigs on Build.gradle(app)

# standing
`keytool -genkey -v -keystore my-key.keystore -alias oligami -keyalg RSA -validity 10000`
`java -jar ./bundletool-all-1.15.5.jar build-apks --bundle=src-tauri\gen\android\app\build\outputs\bundle\universalRelease\app-universal-release.aab --output=signed.apks --ks=C:\bin\key\my-key.keystore --ks-key-alias=oligami --ks-pass=pass:password --key-pass=pass:password`
