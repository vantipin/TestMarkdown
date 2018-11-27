# Examples of Interbit applications

# Glossary
- PPC - Public, Private, Control
- CAuth - chain authorization

# PPC Model
## PPC Chain Authorization
This diagram shows how chain authorization (CAuth) establishes secure sharing of private information from Interbit Accounts with other interbit applications.

### Active parties
**MyApps in Browser** -  This application represent your application frontend part. 
- [x] Frontend React application.
- [x] Runs read-only blockchain in browser. However it can dispatch actions to the full nodes. 

**Application Private Chain** - This application represent your application custom backend logic. 
- [x] Backend application. 
- [x] Full interbit node.

**Accounts in Browser** - This application represent frontend for Interbit platform authentication service. 
- [x] Frontend React application.
- [x] Runs read-only blockchain in browser. However it can dispatch actions to the full nodes.

**Accounts Private Chain** - This application represent Interbit authentication backend service. It is designed to be used with all your applications per product so that auth only needs to be implemented once, rather than once per each application. 
- [x] Backend application. 
- [x] Full interbit node.

### Hosting
All of the active parties are separate applications. Currently, each node would be manually launched. Peers are declared in the app configuration, so that you can decide the physical topology of the nodes.

There are deployment features in development that would allow a node to launch and receive its configuration from an already-existing blockchain network, but they are not ready yet.
![ppc-pattern1](https://user-images.githubusercontent.com/16136204/49014826-6e215e80-f192-11e8-868c-3fc80fdd34c8.jpg)

## PPC Implementation
This diagram documents in detail how interbit applications and Interbit Accounts currently implement the PPC pattern for authentication and authorization.
![ppc-pattern2](https://user-images.githubusercontent.com/16136204/49014827-6eb9f500-f192-11e8-9b64-0c90fb1f2416.jpg)



## UI Data Flow
### Active parties
- [x] Browser
- [x] React.js
- [x] Redux.js
- [x] Interbit Middleware - part of interbit-ui-tools
- [x] Redux-saga middleware
- [x] Interbit browser bundle

![ui-data-flow1](https://user-images.githubusercontent.com/16136204/49015446-28fe2c00-f194-11e8-9fa4-3a02fa5c5adc.jpg)
