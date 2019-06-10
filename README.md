# react-native-airplay-btn
AirPlay library for iOS

## Installation with Automatic Linking
```js
npm i react-native-airplay-btn --save
react-native link
```

### How to create listeners

```js
import { AirPlayListener } from react-native-airplay-btn

this.airplayAvailableSubscription = AirPlayListener.addListener('airplayAvailable', devices => this.setState({
      airPlayAvailable: devices.available, --> devices.available is a boolean
})); 

this.airplayConnectedSubscription = AirPlayListener.addListener('airplayConnected', devices => this.setState({
      airPlayConnected: devices.connected, --> devices.connected is a boolean
      airPlayMirroring: devices.mirroring, --> devices.mirroring is a boolean
}));


// Remove Listeners in componentWillUnmount
this.airPlayConnected.remove();
this.airPlayAvailable.remove()

```

## Methods

```js
  AirPlay.startScan();

  AirPlay.disconnect();
```

### Create AirPlay Button

```js
import { AirPlayButton } from 'react-native-airplay-btn';

<AirPlayButton style={{ height: 30, width: 30, justifyContent: 'center', alignItems:'center' }} />
```

Note: The AirPlay Button does not show in the simulator


## Author

Nadia Dillon
