---
title: 顯示對話方塊以設定影片特性
description: 顯示對話方塊以設定影片特性
ms.assetid: 8074f7d1-e8ab-46c3-acc2-a18be0eb4cc7
keywords:
- CAPDRIVERCAPS 結構
- capDriverGetCaps 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e6ebfa0f75f4bcec63a693636085f16c342e53761b2cb1e67a0e2536fa5cef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144471"
---
# <a name="displaying-dialog-boxes-to-set-video-characteristics"></a>顯示對話方塊以設定影片特性

每個 capture 驅動程式最多可提供三個不同的對話方塊，用來控制影片數位化和捕捉流程的各個層面。 下列範例示範如何顯示這些對話方塊。 在顯示每個對話方塊之前，此範例會呼叫 [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) 宏，並檢查傳回的 [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) 結構，以查看捕獲驅動程式是否可以顯示該結構。


```C++
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

CAPDRIVERCAPS CapDriverCaps = { }; 
CAPSTATUS     CapStatus = { };

capDriverGetCaps(hWndC, &CapDriverCaps, sizeof(CAPDRIVERCAPS)); 
 
// Video source dialog box. 
if (CapDriverCaps.fHasDlgVideoSource)
{
    capDlgVideoSource(hWndC); 
}
 
// Video format dialog box. 
if (CapDriverCaps.fHasDlgVideoFormat) 
{
    capDlgVideoFormat(hWndC); 

    // Are there new image dimensions?
    capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS));

    // If so, notify the parent of a size change.
} 
 
// Video display dialog box. 
if (CapDriverCaps.fHasDlgVideoDisplay)
{
    capDlgVideoDisplay(hWndC); 
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片捕獲](using-video-capture.md)
</dt> <dt>

[**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps)
</dt> </dl>

 

 




