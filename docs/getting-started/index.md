# **Getting Started**

## Installation into an existing Capacitor application.

**_Note: these instructions require a Capacitor version of ^2.3.0_**

1. Build your webapp in your capacitor initiated project (_'npm run build' for example_).
2. Run `npm i @athlyzer/capacitor-community-electron` in your webapp project directory. This will install the platform for use with the `@capacitor/cli`.
3. Run `npx cap add @athlyzer/capacitor-community-electron` to initiate the platform, this will create the `electron` folder in your webapp project.
4. Run `npx cap open @athlyzer/capacitor-community-electron` to start your app in electron.

**_Note: You can use other `npx cap` commands with the platform by: `npx cap <command> @athlyzer/capacitor-community-electron`_**

<br />

## Changing the default configuration

In the `*yourAppDir*/electron/src/index.ts` file there will be a line reading: `const myCapacitorApp = createCapacitorElectronApp();` here you can pass an object with your desired config changes ([see config options for details](/extra/config-options)).

For example if you wanted to disable the splashscreen from showing while the app starts up you would pass an object like the following:

```typescript
const myCapacitorApp = createCapacitorElectronApp({
  splashScreen: {
    useSplashScreen: false,
  },
});
```
