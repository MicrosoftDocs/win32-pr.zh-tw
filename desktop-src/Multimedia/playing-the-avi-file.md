---
title: 播放 AVI 檔案
description: 播放 AVI 檔案
ms.assetid: 6b3845c4-40ec-4824-88c8-6e4ac458f720
keywords:
- mciSendCommand 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e0c490a61bbd53dd62a8223a3ded1aa047ce071d1d2544a2b26d1a9152450b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038011"
---
# <a name="playing-the-avi-file"></a>播放 AVI 檔案

在使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函式來傳送 [**MCI \_ PLAY**](mci-play.md) 命令之前，您的應用程式會為結構配置記憶體、初始化它將使用的成員，以及設定對應至結構中所使用之成員的旗標。  (如果您的應用程式未設定結構成員的旗標，MCI 驅動程式會忽略該成員。 ) 例如，下列範例會從 **dwFrom** 指定的起始位置，播放電影至 **dwTo** 所指定的結束位置。  (如果任一位置為零，則會寫入範例，以避免使用位置。 ) 


```C++
DWORD PlayMovie(WORD wDevID, DWORD dwFrom, DWORD dwTo) 
{ 
    MCI_DGV_PLAY_PARMS mciPlay;    // play parameters 
    DWORD dwFlags = 0; 
 
    // Check dwFrom. If it is != 0 then set parameters and flags. 
    if (dwFrom){ 
        mciPlay.dwFrom = dwFrom; // set parameter 
        dwFlags |= MCI_FROM;     // set flag to validate member 
    } 
 
    // Check dwTo. If it is != 0 then set parameters and flags. 
    if (dwTo){ 
        mciPlay.dwTo = dwTo;    // set parameter 
        dwFlags |= MCI_TO;      // set flag to validate member 
    } 
 
    // Send the MCI_PLAY command and return the result. 
    return mciSendCommand(wDevID, MCI_PLAY, dwFlags, 
       (DWORD)(LPVOID)&mciPlay); 
} 
```



 

 