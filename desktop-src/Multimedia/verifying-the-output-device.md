---
title: 驗證輸出裝置
description: 驗證輸出裝置
ms.assetid: b5a45edd-8f35-44ae-964d-0451f100ca80
keywords:
- MCI_ STATUS 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1774eb3df2a45f98558862a15349007cd299d142
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932330"
---
# <a name="verifying-the-output-device"></a><span data-ttu-id="e5764-104">驗證輸出裝置</span><span class="sxs-lookup"><span data-stu-id="e5764-104">Verifying the Output Device</span></span>

<span data-ttu-id="e5764-105">開啟排序器之後，您應該檢查是否有可使用的 MIDI 對應工具，並將其選取為輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="e5764-105">After opening the sequencer, you should check whether the MIDI mapper was available and selected as the output device.</span></span> <span data-ttu-id="e5764-106">下列範例會使用 [**mci \_ STATUS**](mci-status.md) 命令，確認 MIDI 對應程式是 MCI sequencer 的輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="e5764-106">The following example uses the [**MCI\_ STATUS**](mci-status.md) command to verify that the MIDI mapper is the output device for the MCI sequencer.</span></span>


```C++
UINT wDeviceID;      // valid MCI sequencer ID
DWORD dwReturn;
MCI_STATUS_PARMS mciStatusParms;

// Make sure the opened device is the MIDI mapper.

mciStatusParms.dwItem = MCI_SEQ_STATUS_PORT;

if (dwReturn = mciSendCommand(wDeviceID, MCI_STATUS, MCI_STATUS_ITEM,
    (DWORD)(LPVOID) &mciStatusParms))
{
    
    // Error sending MCI_STATUS command. 
    
    return;
}
if (LOWORD(mciStatusParms.dwReturn) == MIDI_MAPPER)
{
    
    // The MIDI mapper is the output device. 
    
}
Else
{
    
    // The MIDI mapper is not the output device. 
    
} 
```



 

 




