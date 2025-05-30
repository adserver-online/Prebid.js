# Overview

```
Module Name: Dochase Bidder Adapter
Module Type: Bidder Adapter
Maintainer: dochaseops@dochase.com
```

# Description

Dochase currently supports the BANNER and NATIVE type ads through prebid js

Module that connects to Dochase's demand sources.

# Test Request
```
  var adUnits = [
    {
      code: 'display-ad',
      mediaTypes: {
        banner: {
            sizes: [[300, 250]], 
        }
      }
      bids: [
        {
            bidder: 'dochase',
            params: {
                placement_id: 5550,  // Required parameter
                width: 300,   // Optional parameter 
                height: 250, // Optional parameter
                bid_floor: 0.5 // Optional parameter
            }
        }
      ]
    },
    {
      code: 'native-ad-container',
      mediaTypes: {
        native: {
          title: { required: true, len: 100 },
          image: { required: true, sizes: [300, 250] },
          sponsored: { required: false },
          clickUrl: { required: true },
          desc: { required: true },
          icon: { required: false, sizes: [50, 50] },
          cta: { required: false }
        }
      },
      bids: [
        {
          bidder: 'dochase',
          params: {
            placement_id: 5551, // Required parameter
			bid_floor: 1 // Optional parameter
          }
        }
      ]
    }
  ];
```
