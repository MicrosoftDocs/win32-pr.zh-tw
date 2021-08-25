---
title: 建立調色板的動畫
description: 建立調色板的動畫
ms.assetid: 89493cc3-eca9-407f-99c2-903fba16992c
keywords:
- DrawDib，調色板
- DrawDibRealize 函式
- DrawDibDraw 函式
- DrawDibChangePalette 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be9613e4e648fad0b1fafe5d48d091ab13c9b6c358eda4a858c1d5517ab8fc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808418"
---
# <a name="animating-a-palette"></a>建立調色板的動畫

下列範例會使用 [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize)、 [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)和 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 函式將調色板動畫。

您可以搭配 [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)使用 [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)函式，來變更點陣圖的色彩。 首先，若要允許元件變更，請 \_ 在 **DrawDibBegin** 的呼叫中指定 DDF 動畫旗標。 其次，使用 **DrawDibChangePalette** 設定調色板專案中的色彩資料表值。

例如，如果 *lppe* 是 [PALETTEENTRY](/previous-versions//ms532623(v=vs.85))陣列的位址，其中包含新的色彩，而 *lpbi* 是 [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)或 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw)中使用的 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構，則下列片段會更新 DIB 色彩表。


```C++
hdc = GetDC(hwnd); 
DrawDibBegin(hdd, ....., DDF_ANIMATE); 
DrawDibRealize(hdd, hdc, fBackground); 
DrawDibDraw(hdd, hdc, ...., DDF_SAME_DRAW|DDF_SAME_HDC); 
 
// Call to change color. 
DrawDibChangePalette(hDD, iStart, iLen, lppe); 
. 
. 
. 
ReleaseDC(hwnd, hdc); 

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DrawDib](using-drawdib.md)
</dt> </dl>

 

 