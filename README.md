# uketsuke (Web-Based Reception Kiosk)

A lightweight, single-file reception system optimized for iPad and iPhone. It transforms any iOS device into a professional, dedicated reception kiosk by leveraging PWA (Progressive Web App) technology.

##  Key Features

- **Offline Capability**: Built-in Service Worker ensures the system remains functional even without an internet connection once initially loaded.
- **Dynamic In-App Editor**: 
  - **Live Customization**: Modify button labels, sub-titles, and FaceTime addresses on the fly.
  - **Granular Control**: Adjust font sizes via a stepper, change text alignment, and pick custom color schemes (background/text) for each item.
  - **Efficient Management**: Supports one-click duplication and deletion of reception entries.
- **Zero-Backbone Architecture**: A standalone HTML/JavaScript file with no server-side database required; all configurations are stored locally via the `localStorage` API.
- **Secure Access**: The configuration panel is password-protected to prevent unauthorized modifications by visitors.
- **Native Experience**: Fully optimized for "Add to Home Screen" on iOS, providing a full-screen, immersive interface without browser UI elements.

##  Deployment and Usage

1. **Open**: Host the `index.html` on any web server or open the file in Safari on an iOS/iPadOS device.
2. **Install**: Tap the **Share** button and select **"Add to Home Screen."**
3. **Launch**: Open the "uketsuke" icon from your Home Screen.
4. **Initial Setup**:
   - Tap the **"設定 (Settings)"** button in the top-right corner.
   - Establish a new password (first-time setup).
   - Enter the editor to add your departments or staff names along with their FaceTime addresses.
5. **Customize**: Use the toolbar in edit mode to adjust font sizes, alignment, and colors. Tap **"完了 (Done)"** to save.

##  Technical Specifications

- **Frontend**: Vue.js 3 (Composition-ready via Global Build).
- **Storage**: Browser `localStorage` for persistent configuration.
- **Communication**: Triggers native video/audio calls using the `facetime://` URI scheme.
- **PWA**: Inline Service Worker implementation for resource caching and offline reliability.

##  Disclaimer

This software is provided "as is," without warranty of any kind. The author shall not be held liable for any damages or issues (such as missed calls or configuration loss) arising from the use of this application. It is strongly recommended to perform thorough testing in your specific network and device environment prior to professional implementation.

##  License

This project is licensed under the [MIT License](LICENSE).

### Third-Party Attribution
- **Vue.js**: MIT License (c) 2013-present, Yuxi (Evan) You.
