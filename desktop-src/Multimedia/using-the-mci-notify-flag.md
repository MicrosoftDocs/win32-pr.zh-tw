---
title: 使用 MCI_NOTIFY 旗標
description: 使用 MCI \_ 通知旗標
ms.assetid: 1d1803c8-f315-463e-ae0d-a258aa3af3c9
keywords:
- MCI_NOTIFY 旗標
- MCI_PLAY 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b0e7269ee7d80dd47372d9210fbdbc1332b3a88a96e2a17d6719c9945ab30aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136136"
---
# <a name="using-the-mci_notify-flag"></a>使用 MCI \_ 通知旗標

下列範例顯示如何搭配使用 mci \_ 通知旗標與 [**mci \_ PLAY**](mci-play.md) 命令。 將處理 [**MM \_ MCINOTIFY**](mm-mcinotify.md) 訊息之視窗程式的控制碼，會在 *hwnd* 中指定。


```C++
MCI_DGV_PLAY_PARMS mciPlay; 
DWORD dwFlags; 
 
mciPlay.dwCallback = MAKELONG(hwnd, 0); 
dwFlags = MCI_NOTIFY; 
 
mciSendCommand(wMCIDeviceID, MCI_PLAY, dwFlags, (DWORD)(LPSTR)&mciPlay); 
```



 

 




