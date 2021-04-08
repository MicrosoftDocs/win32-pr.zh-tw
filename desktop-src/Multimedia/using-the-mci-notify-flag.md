---
title: 使用 MCI_NOTIFY 旗標
description: 使用 MCI \_ 通知旗標
ms.assetid: 1d1803c8-f315-463e-ae0d-a258aa3af3c9
keywords:
- MCI_NOTIFY 旗標
- MCI_PLAY 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472613d2e6efcd6b30c88ed64dfa7875b4742527
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839571"
---
# <a name="using-the-mci_notify-flag"></a><span data-ttu-id="874ad-105">使用 MCI \_ 通知旗標</span><span class="sxs-lookup"><span data-stu-id="874ad-105">Using the MCI\_NOTIFY Flag</span></span>

<span data-ttu-id="874ad-106">下列範例顯示如何搭配使用 mci \_ 通知旗標與 [**mci \_ PLAY**](mci-play.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="874ad-106">The following example shows how the MCI\_NOTIFY flag is used with the [**MCI\_PLAY**](mci-play.md) command.</span></span> <span data-ttu-id="874ad-107">將處理 [**MM \_ MCINOTIFY**](mm-mcinotify.md) 訊息之視窗程式的控制碼，會在 *hwnd* 中指定。</span><span class="sxs-lookup"><span data-stu-id="874ad-107">The handle to the window procedure that will process the [**MM\_MCINOTIFY**](mm-mcinotify.md) message is specified in *hwnd*.</span></span>


```C++
MCI_DGV_PLAY_PARMS mciPlay; 
DWORD dwFlags; 
 
mciPlay.dwCallback = MAKELONG(hwnd, 0); 
dwFlags = MCI_NOTIFY; 
 
mciSendCommand(wMCIDeviceID, MCI_PLAY, dwFlags, (DWORD)(LPSTR)&mciPlay); 
```



 

 




