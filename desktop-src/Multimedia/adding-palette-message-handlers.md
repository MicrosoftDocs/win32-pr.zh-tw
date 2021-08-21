---
title: 加入調色板訊息處理常式
description: 加入調色板訊息處理常式
ms.assetid: bfd77f42-6a9d-4195-b1a0-1688e44358e3
keywords:
- DrawDib，調色板
- DrawDibRealize 函式
- DrawDibDraw 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b17512025cadf0e457b596a3bfc07399db4eb9185195f4c836ee154d5ff64a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808628"
---
# <a name="adding-palette-message-handlers"></a>加入調色板訊息處理常式

下列範例說明適用于 [**wm \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) 和 [**wm \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) 訊息的簡單訊息處理常式。 此範例會使用 [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) 函數來處理 **WM \_ QUERYNEWPALETTE** 訊息。

您的應用程式應藉由讓目的地視窗失效，讓 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw)函式重繪影像，來回應 [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette)訊息。 您應使用 [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize)函式來實現該調色板，以回應 [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged)訊息。


```C++
case WM_PALETTECHANGED: 
    if ((HWND)wParam == hwnd) 
        break; 
case WM_QUERYNEWPALETTE: 
    hdc = GetDC(hwnd); 
    f = DrawDibRealize(hdd, hdc, FALSE) > 0; 
    ReleaseDC(hwnd, hdc); 
    if (f) 
        InvalidateRect(hwnd, NULL, TRUE); 
    break; 

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DrawDib](using-drawdib.md)
</dt> </dl>

 

 