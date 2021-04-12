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
ms.openlocfilehash: 679990dce5977430eb2a46fc3cd06622246d357f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375240"
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

 

 