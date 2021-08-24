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
ms.openlocfilehash: e0f10d533fff97064ba3c6a081a2f1d0aaa9e1b72011f2baa1ac3a6bd1a81d43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678718"
---
# <a name="drawing-a-display-context"></a>繪製顯示內容

下列範例會在點陣圖順序中顯示數個影像之前，先使用 [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) 函數來準備 DrawDib DC。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DrawDib](using-drawdib.md)
</dt> </dl>

 

 




