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
# <a name="adding-palette-message-handlers"></a><span data-ttu-id="2b133-106">加入調色板訊息處理常式</span><span class="sxs-lookup"><span data-stu-id="2b133-106">Adding Palette Message Handlers</span></span>

<span data-ttu-id="2b133-107">下列範例說明適用于 [**wm \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) 和 [**wm \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) 訊息的簡單訊息處理常式。</span><span class="sxs-lookup"><span data-stu-id="2b133-107">The following example illustrates simple message handlers for the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) messages.</span></span> <span data-ttu-id="2b133-108">此範例會使用 [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) 函數來處理 **WM \_ QUERYNEWPALETTE** 訊息。</span><span class="sxs-lookup"><span data-stu-id="2b133-108">The example uses the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) function to process the **WM\_QUERYNEWPALETTE** message.</span></span>

<span data-ttu-id="2b133-109">您的應用程式應藉由讓目的地視窗失效，讓 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw)函式重繪影像，來回應 [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette)訊息。</span><span class="sxs-lookup"><span data-stu-id="2b133-109">Your application should respond to the [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) message by invalidating the destination window to let the [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) function redraw an image.</span></span> <span data-ttu-id="2b133-110">您應使用 [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize)函式來實現該調色板，以回應 [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged)訊息。</span><span class="sxs-lookup"><span data-stu-id="2b133-110">You should respond to the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) message by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) function to realize the palette.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2b133-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="2b133-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b133-112">使用 DrawDib</span><span class="sxs-lookup"><span data-stu-id="2b133-112">Using DrawDib</span></span>](using-drawdib.md)
</dt> </dl>

 

 