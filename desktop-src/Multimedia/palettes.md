---
title: 調色板
description: 調色板
ms.assetid: ee048f9a-3036-40dc-a6d7-f612b9ef767c
keywords:
- DrawDib，調色板
- DrawDibRealize 函式
- DrawDibDraw 函式
- DrawDibSetPalette 函式
- DrawDibGetPalette 函式
- DrawDibChangePalette 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5935831d8996c424a386f86082282f9cf7c1c12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933195"
---
# <a name="palettes"></a>調色板

DrawDib 函式要求應用程式必須回應兩個以元件為導向的訊息： [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) 和 [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged)。 如果您的應用程式不是可辨識的元件，您必須為每個訊息加入處理常式。 如需處理 **wm \_ QUERYNEWPALETTE** 和 **WM \_ PALETTECHANGED** 訊息的詳細資訊，請參閱 [加入調色板訊息處理常式](adding-palette-message-handlers.md)。

您可以使用 [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) 函式，將目前的 DrawDib 調色板實現到 DC。 您應該瞭解選擇區以回應 [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) 或 [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) 訊息，或是當您準備使用 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 函式來顯示影像序列時。

您可以使用 [**DrawDibSetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) 函式，繪製對應到另一個調色板的影像。 此函式會強制 DrawDib DC 使用指定的調色板，這可能會影響影像品質。 例如，具有調色板感知的應用程式可能已經實現了一個調色板，而且需要防止 DrawDib 取得自己的調色板。 應用程式可以使用 **DrawDibSetPalette** 通知 DrawDib 要使用的調色板。

您可以使用 [**DrawDibGetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetpalette) 函數來取得目前前景調色板的控制碼。 如果您的應用程式使用目前的前景調色板，它並不會獨佔使用此元件，而另一個應用程式可能會使調色板控制碼失效。 當您的應用程式使用完畢時，您的應用程式不應該釋出該調色板。 釋放調色板可能使另一個應用程式的調色板控制碼失效。

您可以使用 [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette) 函數來準備 DrawDib，以接收其調色板的新色彩值。 在 **DrawDibChangePalette** 之後的程式碼中，您可以為 [調色板色彩表] 指派新值。 當您呼叫 **DrawDibChangePalette** 時，如果 DrawDib DC 中未設定 **DDF \_ 動畫** 旗標，您可以使用 [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize)來實現調色板的變更。 然後，您可以使用 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 來重繪映射。 如果已在 DrawDib DC 中設定 **DDF \_ 動畫** 旗標，您可以使用 **DrawDibDraw** 或 **DrawDibRealize**，以動畫顯示調色板以及顯示點陣圖的色彩。 您可以使用 [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend)和 [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)函數來更新 **DDF \_ 動畫** 旗標。

> [!Note]  
> 如果您在 DC 選取 DrawDib 元件時將其釋出，當 DC 使用調色板時，會導致圖形裝置介面 (GDI) 錯誤。 相反地，您的應用程式應該使用 [**DrawDibSetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) 來變更 DrawDib DC，以使用預設的調色板或其他調色板。

 

[**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend)、 [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose)和 [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)函數可以釋放 DrawDib 調色板。 不過，只有當 DC 尚未選取元件時，才應該使用這些函數。 DrawDibDraw 函式使用相同的 DrawDib DC 時，也可以釋出調色板，但會指定不同的繪圖參數 (*lpbi*、 *dxDst*、 *dyDst*、 *dxSrc* 或 *dySrc*) 或不同的格式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影像轉譯](image-rendering.md)
</dt> </dl>

 

 