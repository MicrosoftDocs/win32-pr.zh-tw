---
title: 設定時間格式
description: 設定時間格式
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- MCI_SET 命令訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59eb5a9194f3f2598cd8f88fbefb3ea741f51eb9c25210deb6db69c54259e189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370886"
---
# <a name="setting-the-time-format"></a>設定時間格式

使用 [**mci \_ set**](mci-set.md) 命令訊息以及 [**mci \_ set \_ PARMS**](mci-set-parms.md) 結構來設定開啟裝置的時間格式。 將 **dwTimeFormat** 成員設定為下列其中一個常數。



| 常數                   | 時間格式                                          |
|----------------------------|------------------------------------------------------|
| MCI \_ 格式 \_ 位元組         | 以脈衝程式碼調製 PCM 格式檔案 (的位元組 \[ \])  |
| MCI \_ 格式 \_ 毫秒  | 毫秒                                         |
| MCI \_ 格式 \_ MSF           | 分鐘/秒/框架                                  |
| MCI \_ 格式 \_ 範例       | 範例                                              |
| MCI \_ 格式的 \_ SMPTE \_ 24     | SMPTE，24個框架                                      |
| MCI \_ 格式的 \_ SMPTE \_ 25     | SMPTE，25個框架                                      |
| MCI \_ 格式 \_ SMPTE \_ 30     | SMPTE，30個畫面格                                      |
| MCI \_ 格式的 \_ SMPTE \_ 30DROP | SMPTE，30個畫面格下降                                 |
| MCI \_ 格式 \_ TMSF          | 曲目/分鐘/秒/畫面格                            |
| MCI \_ SEQ \_ 格式 \_ SONGPTR  | MIDI 歌曲指標                                    |



 

下列範例會使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數，將 wDeviceID 變數所指定裝置的時間格式設定為毫秒。


```C++
UINT wDeviceID; 
MCI_SET_PARMS mciSetParms; 

// Set time format to milliseconds. 

mciSetParms.dwTimeFormat = MCI_FORMAT_MILLISECONDS; 
if( mciSendCommand(wDeviceID, MCI_SET, MCI_SET_TIME_FORMAT, 
                  (DWORD) &mciSetParms)) 
{
    // Error, unable to set time format. 
    return FALSE; 
}
else 
{
    // Time format set successfully. 
    return TRUE; 
}
```



 

 