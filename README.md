# Kip Commander
Experimental Signal K Server plugin for remotely controlling Kip-based displays sugh as (but not limited to) mast displays.

**IMPORTANT NOTE**

This plugin, at the current state of development intentionally not available on the Signal K App Store, works only under the following conditions:

- Using the Kip branch available here https://github.com/raffmont/Kip
- The user the Kip display is logged into the Signal K server si named **mastdisplay**

## Installation

Set your current project developing directory before starting the installation procedure.

1. Clone the repository
```console bash
git clone https://github.com/raffmont/kip-commander.git
```

2. Change to the project directory

```console bash
cd kip-commander
```

3. Instally nodejs packages

```console bash
npm install
```

4. Build the Kip Commander plugin

```console bash
npm run build
```

5. Get the link to the plugin development directory

```console bash
npm link
```

The following step is different if a development or a production environment is going to be used.

- If you are running in a Signal K Server development environment:
  ```console bash
  cd signalk-server
  ```
  
- If you are running a production Signal K Server
  ```console bash
  cd
  cd .signalk
  ```

Finally, link the plugin where it is expected to be
  
```console bash
npm link kip-commander
```

Then restart your Signal K Server instance.
Remember to activate the plugin before using the user interface available as web application.

**REMEMBER**

Repeat the npm link / npm link kip-command cycle each time the Signal K Server or any production plugin is installed or
updated.
