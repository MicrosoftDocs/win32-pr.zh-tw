---
title: 使用 Device-Type 常數開啟簡單的裝置
description: 使用 Device-Type 常數開啟簡單的裝置
ms.assetid: 6ed5fd4b-534a-4e03-8130-07f831403a8e
keywords:
- mciSendCommand 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef65cf4546da2d7f7b6fdb5883232d0b1802f7b1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092674"
---
# <a name="opening-a-simple-device-by-using-the-device-type-constant"></a><span data-ttu-id="f7861-104">使用 Device-Type 常數開啟簡單的裝置</span><span class="sxs-lookup"><span data-stu-id="f7861-104">Opening a Simple Device by Using the Device-Type Constant</span></span>

<span data-ttu-id="f7861-105">下列範例會使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函式來指定裝置類型常數，以開啟 CD 音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="f7861-105">The following example opens a CD audio device by specifying a device-type constant using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


```C++
UINT wDeviceID;
DWORD dwReturn;
MCI_OPEN_PARMS mciOpenParms;

// Opens a CD audio device by specifying a device-type constant.

mciOpenParms.lpstrDeviceType = (LPCSTR) MCI_DEVTYPE_CD_AUDIO;

if (dwReturn = mciSendCommand(NULL, MCI_OPEN,
    MCI_OPEN_TYPE | MCI_OPEN_TYPE_ID, (DWORD)(LPVOID) &mciOpenParms))
{
    
    // Error, unable to open device.
    
}

// The device opened successfully; get the device ID.
wDeviceID = mciOpenParms.wDeviceID;
```



 

 