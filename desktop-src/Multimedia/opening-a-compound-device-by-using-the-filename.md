---
title: 使用檔案名開啟複合裝置
description: 使用檔案名開啟複合裝置
ms.assetid: 5199bb68-44be-4fad-af5b-8fe89f27caee
keywords:
- mciSendCommand 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20eb271658f77c5af4d35db96dd7bdbe6753af08
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314893"
---
# <a name="opening-a-compound-device-by-using-the-filename"></a><span data-ttu-id="ed1de-104">使用檔案名開啟複合裝置</span><span class="sxs-lookup"><span data-stu-id="ed1de-104">Opening a Compound Device by Using the Filename</span></span>

<span data-ttu-id="ed1de-105">下列範例會藉由指定波形音訊檔案（名為 "TIMPANI"）來開啟波形音訊裝置。WAV "使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="ed1de-105">The following example opens the waveform-audio device by specifying a waveform-audio file named "TIMPANI.WAV" using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


```C++
UINT wDeviceID;
DWORD dwReturn;
MCI_OPEN_PARMS mciOpenParms;
 
// Opens a waveform-audio device by specifying the device and 
// file name.

mciOpenParms.lpstrDeviceType = "waveaudio";
mciOpenParms.lpstrElementName = "timpani.wav";

if (dwReturn = mciSendCommand(NULL, MCI_OPEN,
    MCI_OPEN_TYPE | MCI_OPEN_ELEMENT, (DWORD)(LPVOID) &mciOpenParms))
{
    
    // Error, unable to open device.
    
}

// The device opened successfully; get the device ID.
wDeviceID = mciOpenParms.wDeviceID;
```



 

 