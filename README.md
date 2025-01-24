# Expo Camera onBarCodeScanned Callback Issue

This repository demonstrates a bug in Expo's Camera API where the `onBarCodeScanned` callback intermittently returns an empty object or `undefined` instead of the expected barcode data.  The issue is particularly challenging to debug due to its inconsistent nature. 

## Bug Reproduction

The `bug.js` file contains code that attempts to scan barcodes using the Expo Camera API.  You may need to adjust the `barCodeTypes` to match the types of barcodes you are testing with. Running this code might sometimes (not always) result in the callback returning incorrect data. 

## Solution

The `bugSolution.js` offers a potential workaround.  This involves adding a delay before processing the scanned data, allowing the camera to fully capture and process the barcode.  While not a perfect fix, it may help reduce the frequency of the issue. 

## Contributing

Contributions are welcome! If you have a more robust solution or can provide more information on the root cause of this issue, please open a pull request.