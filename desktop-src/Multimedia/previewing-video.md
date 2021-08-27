---
title: 預覽 Windows 多媒體) 的影片 (
description: Windows 多媒體中的這個範例會使用 capPreviewRate 來設定預覽模式與 capPreview 的畫面顯示速率，以將 [捕捉] 視窗置於預覽模式。
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- capPreview 宏
- capPreviewRate 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e70d0520af3bb71906c6b0ea4d1c0a61464559eedfd2385753b228841fa6af4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037908"
---
# <a name="previewing-video-windows-multimedia"></a>預覽 Windows 多媒體) 的影片 (

下列範例會使用 [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) 宏將預覽模式的畫面格顯示速率設定為每個畫面的66毫秒，然後使用 [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) 宏將 [capture] 視窗置於預覽模式。


```C++
// Create the capture window.
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

capPreviewRate(hWndC, 66);     // rate, in milliseconds
capPreview(hWndC, TRUE);       // starts preview 

// Preview

capPreview(hWndC, FALSE);        // disables preview 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片捕獲](using-video-capture.md)
</dt> </dl>

 

 




