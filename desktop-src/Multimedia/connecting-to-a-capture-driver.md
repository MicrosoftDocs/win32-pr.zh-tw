---
title: 連接至 Capture 驅動程式
description: 連接至 Capture 驅動程式
ms.assetid: ce83329f-de5a-4428-bc0d-be5f3d35ff1a
keywords:
- capDriverDisconnect 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34e606c439143400f1ea1845db37e7faf93009350254c173c4003400c3996f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144861"
---
# <a name="connecting-to-a-capture-driver"></a>連接至 Capture 驅動程式

下列範例會將 *hWndC* 的 capture 視窗連接至 MSVIDEO 驅動程式，然後使用 [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) 宏將其中斷連接：


```C++
fOK = SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0, 0L); 
// 
// Or, use the macro to connect to the MSVIDEO driver: 
// fOK = capDriverConnect(hWndC, 0); 
// 
// Place code to set up and capture video here. 
// 
capDriverDisconnect (hWndC); 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片捕獲](using-video-capture.md)
</dt> </dl>

 

 




