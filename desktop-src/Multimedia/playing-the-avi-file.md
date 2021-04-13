---
title: 播放 AVI 檔案
description: 播放 AVI 檔案
ms.assetid: 6b3845c4-40ec-4824-88c8-6e4ac458f720
keywords:
- mciSendCommand 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31754bd5f66b455abc76d363c5ff3e5e286e8040
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314701"
---
# <a name="playing-the-avi-file"></a><span data-ttu-id="ceec0-104">播放 AVI 檔案</span><span class="sxs-lookup"><span data-stu-id="ceec0-104">Playing the AVI File</span></span>

<span data-ttu-id="ceec0-105">在使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函式來傳送 [**MCI \_ PLAY**](mci-play.md) 命令之前，您的應用程式會為結構配置記憶體、初始化它將使用的成員，以及設定對應至結構中所使用之成員的旗標。</span><span class="sxs-lookup"><span data-stu-id="ceec0-105">Before using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to send the [**MCI\_PLAY**](mci-play.md) command, your application allocates the memory for the structure, initializes the members it will use, and sets the flags corresponding to the members used in the structure.</span></span> <span data-ttu-id="ceec0-106"> (如果您的應用程式未設定結構成員的旗標，MCI 驅動程式會忽略該成員。 ) 例如，下列範例會從 **dwFrom** 指定的起始位置，播放電影至 **dwTo** 所指定的結束位置。</span><span class="sxs-lookup"><span data-stu-id="ceec0-106">(If your application does not set a flag for a structure member, MCI drivers ignore the member.) For example, the following example plays a movie from the starting position specified by **dwFrom** to the ending position specified by **dwTo**.</span></span> <span data-ttu-id="ceec0-107"> (如果任一位置為零，則會寫入範例，以避免使用位置。 ) </span><span class="sxs-lookup"><span data-stu-id="ceec0-107">(If either position is zero, the example is written so that the position is not used.)</span></span>


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



 

 