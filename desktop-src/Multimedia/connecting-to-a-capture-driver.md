---
title: 連接至 Capture 驅動程式
description: 連接至 Capture 驅動程式
ms.assetid: ce83329f-de5a-4428-bc0d-be5f3d35ff1a
keywords:
- capDriverDisconnect 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2161279f5b8b8dc528ee548d0a6a8ad6e9b397f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969652"
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

 

 




