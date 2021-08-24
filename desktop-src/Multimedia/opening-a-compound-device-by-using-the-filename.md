---
title: 使用檔案名開啟複合裝置
description: 使用檔案名開啟複合裝置
ms.assetid: 5199bb68-44be-4fad-af5b-8fe89f27caee
keywords:
- mciSendCommand 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5ef021c283337c0cea2085d79fefa91667ce1dac095ff7ae17fcc448c9461c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806358"
---
# <a name="opening-a-compound-device-by-using-the-filename"></a>使用檔案名開啟複合裝置

下列範例會藉由指定波形音訊檔案（名為 "TIMPANI"）來開啟波形音訊裝置。WAV "使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數。


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



 

 