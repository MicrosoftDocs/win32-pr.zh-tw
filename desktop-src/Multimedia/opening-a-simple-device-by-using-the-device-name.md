---
title: 使用裝置名稱開啟簡單的裝置
description: 使用裝置名稱開啟簡單的裝置
ms.assetid: 9e116499-2094-40e1-b2bc-3e3b8281a472
keywords:
- mciSendCommand 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d186451717a056188d6fc990188c7e73fcf34cf1339b0787f7cec6e7573557
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802324"
---
# <a name="opening-a-simple-device-by-using-the-device-name"></a>使用裝置名稱開啟簡單的裝置

下列範例會使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函式來指定裝置名稱，以開啟 CD 音訊裝置。


```C++
UINT wDeviceID;
DWORD dwReturn;
MCI_OPEN_PARMS mciOpenParms;
 
// Opens a CD audio device by specifying the device name.

mciOpenParms.lpstrDeviceType = "cdaudio";

if (dwReturn = mciSendCommand(NULL, MCI_OPEN, MCI_OPEN_TYPE,
    (DWORD)(LPVOID) &mciOpenParms))
{
    
    // Error, unable to open device.
    
}

// The device opened successfully; get the device ID.
wDeviceID = mciOpenParms.wDeviceID;
```



 

 