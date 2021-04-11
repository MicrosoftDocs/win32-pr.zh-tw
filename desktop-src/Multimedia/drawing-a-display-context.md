---
title: 繪製顯示內容
description: 繪製顯示內容
ms.assetid: c3328375-faa3-4b29-a155-8a25cc62269f
keywords:
- 'DrawDib，裝置內容 (DC) '
- DrawDib，繪製 Dc
- DrawDibRealize 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1c79c2b7bb938cc34527b23cfc66fda6d19503
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021416"
---
# <a name="drawing-a-display-context"></a><span data-ttu-id="4458f-106">繪製顯示內容</span><span class="sxs-lookup"><span data-stu-id="4458f-106">Drawing a Display Context</span></span>

<span data-ttu-id="4458f-107">下列範例會在點陣圖順序中顯示數個影像之前，先使用 [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) 函數來準備 DrawDib DC。</span><span class="sxs-lookup"><span data-stu-id="4458f-107">The following example prepares a DrawDib DC by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) function prior to displaying several images in a bitmap sequence.</span></span>


```C++
hdc = GetDC(hwnd); 
DrawDibBegin(hdd, hdc, dxDest, dyDest, lpbi, dxSrc, dySrc, NULL); 
DrawDibRealize(hdd, hdc, fBackground); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
DrawDibDraw(hdd, hdc, xDst, yDst, dxDst, dyDst, lpbi, lpBits, 
    xSrc, ySrc, dxSrc, dySrc, DDF_SAME_DRAW|DDF_SAME_HDC); 
ReleaseDC(hwnd, hdc); 

```



## <a name="related-topics"></a><span data-ttu-id="4458f-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="4458f-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4458f-109">使用 DrawDib</span><span class="sxs-lookup"><span data-stu-id="4458f-109">Using DrawDib</span></span>](using-drawdib.md)
</dt> </dl>

 

 




