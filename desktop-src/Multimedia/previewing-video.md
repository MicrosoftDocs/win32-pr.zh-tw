---
title: " (Windows 多媒體) 預覽影片"
description: 此 Windows 多媒體範例中的範例會使用 capPreviewRate 來設定預覽模式與 capPreview 的畫面顯示速率，以將 [捕捉] 視窗置於預覽模式。
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- capPreview 宏
- capPreviewRate 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc3aaeb9a8ff0f040218fca4822af93ab8bfe29
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405541"
---
# <a name="previewing-video-windows-multimedia"></a> (Windows 多媒體) 預覽影片

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

 

 




