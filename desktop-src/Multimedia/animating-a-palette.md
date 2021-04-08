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
ms.openlocfilehash: e023ba8ee2c4791ebc8c3f2ac7ebf9a198f4a5ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682214"
---
# <a name="animating-a-palette"></a><span data-ttu-id="e2f4a-107">建立調色板的動畫</span><span class="sxs-lookup"><span data-stu-id="e2f4a-107">Animating a Palette</span></span>

<span data-ttu-id="e2f4a-108">下列範例會使用 [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize)、 [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)和 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 函式將調色板動畫。</span><span class="sxs-lookup"><span data-stu-id="e2f4a-108">The following example animates a palette by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize), [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette), and [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) functions.</span></span>

<span data-ttu-id="e2f4a-109">您可以搭配 [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)使用 [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)函式，來變更點陣圖的色彩。</span><span class="sxs-lookup"><span data-stu-id="e2f4a-109">You can change the colors of a bitmap by using the [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) function in combination with [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette).</span></span> <span data-ttu-id="e2f4a-110">首先，若要允許元件變更，請 \_ 在 **DrawDibBegin** 的呼叫中指定 DDF 動畫旗標。</span><span class="sxs-lookup"><span data-stu-id="e2f4a-110">First, to allow palette changes, specify the DDF\_ANIMATE flag in the call to **DrawDibBegin**.</span></span> <span data-ttu-id="e2f4a-111">其次，使用 **DrawDibChangePalette** 設定調色板專案中的色彩資料表值。</span><span class="sxs-lookup"><span data-stu-id="e2f4a-111">Second, set the color table values from the palette entries by using **DrawDibChangePalette**.</span></span>

<span data-ttu-id="e2f4a-112">例如，如果 *lppe* 是 [PALETTEENTRY](/previous-versions//ms532623(v=vs.85))陣列的位址，其中包含新的色彩，而 *lpbi* 是 [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)或 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw)中使用的 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構，則下列片段會更新 DIB 色彩表。</span><span class="sxs-lookup"><span data-stu-id="e2f4a-112">For example, if *lppe* is an address of the [PALETTEENTRY](/previous-versions//ms532623(v=vs.85)) array containing the new colors, and *lpbi* is the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure used in [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) or [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw), the following fragment updates the DIB color table.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e2f4a-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="e2f4a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2f4a-114">使用 DrawDib</span><span class="sxs-lookup"><span data-stu-id="e2f4a-114">Using DrawDib</span></span>](using-drawdib.md)
</dt> </dl>

 

 