
English | [简体中文](./README-zh.md)
  
A powerful tool for intercepting and modifying Ajax/Fetch request responses.

**Core Features：**   
- [x] Intercept and modify AJAX/Fetch request responses
- [x] Real-time request monitoring and visualization
- [x] Support immediate response mode without waiting for actual requests
- [x] Dynamic loading in development environment without affecting production code

## Installation
```
npm i xhr-mocker@latest
```
```javascript
// Entry file
import { mockInit } from 'xhr-mocker'
// Initialize at application entry
// React projects
mockInit({
    rules:[],  // Domain rules to intercept (supports regex), typically just configure main project domain
    excludeRules:[] , // Domain rules to exclude (supports regex), includes built-in exclusions
    mockPanelSdkUrl: '' // Mock panel SDK URL
    disabled: false // Whether to disable。If true, the mock-tool will not be loaded
})}
// Vue projects
mockInit({
  rules: []
}).then(() => {
  new Vue({
    render: h => h(App)
  }).$mount('#app')
})
```

## Usage Guide

### Enable Mock Features
1. Click the icon in the top right corner to open the control panel, where you can enable monitoring to view all request records
2. Toggle Mock functionality using the switch button
3. Configure immediate response mode for individual endpoints
  
### Customize Response Data
In the response editor, you can:
1. Freely edit response data
2. Extend functionality based on xhr-mocker-panel-sdk。eg: Auto-generate mock data from API documentation or generate simulated data using AI

## License
MIT License.
