---
title: 開啟播放視窗
description: 開啟播放視窗
ms.assetid: 180f3fb9-cdcb-49ec-a708-84a597295b2f
keywords:
- MCI_OPEN 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11aed7802a3536beb069c1fd7048b66be217d21f0dd3e47fa21caaad80d854e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806168"
---
# <a name="opening-the-playback-window"></a>開啟播放視窗

下列範例示範如何使用 [**MCI \_ OPEN**](mci-open.md) 命令來設定父視窗，並建立該視窗的子系。


```C++
MCI_DGV_OPEN_PARMS    mciOpen; 
 
mciOpen.lpstrElementName = lpstrFile;  // Set the filename.
mciOpen.dwStyle = WS_CHILD;            // Set the style. 
mciOpen.hWndParent = hWnd;             // Give a window handle. 
 
if (mciSendCommand(0, MCI_OPEN, 
   (DWORD)(MCI_OPEN_ELEMENT|MCI_DGV_OPEN_PARENT|MCI_DGV_OPEN), 
   (DWORD)(LPSTR)&mciOpen) == 0)
{ 
    // Open operation is successful. Continue. 
} 
```



 

 




