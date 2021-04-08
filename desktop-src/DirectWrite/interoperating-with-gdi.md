---
title: 與 GDI 交互操作
description: DirectWrite 會提供的遷移路徑，以及與 GDI 的字型模型之間的互通性，以及將文字轉譯成可在視窗上繪製之點陣圖的介面。
ms.assetid: fb73e07b-60fb-4726-bd5b-c14d61ace186
keywords:
- DirectWrite，GDI 交互操作
- DirectWrite，互通性
- 互通性
- '圖形裝置介面 (GDI) '
- 'GDI (圖形裝置介面) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41c7c99e6bfac0aabddd4a1568b64cd425ccb25b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023518"
---
# <a name="interoperating-with-gdi"></a>與 GDI 交互操作

[DirectWrite](direct-write-portal.md) 會提供的遷移路徑，以及與 GDI 的字型模型之間的互通性，以及將文字轉譯成可在視窗上繪製之點陣圖的介面。

本總覽包含下列部分：

-   [簡介](#introduction)
-   [第1部分： IDWriteGdiInterop](#part-1-idwritegdiinterop)
-   [第2部分：字型物件](#part-2-font-objects)
-   [第3部分：轉譯](#part-3-rendering)

## <a name="introduction"></a>簡介

[DirectWrite](direct-write-portal.md) 提供在 GDI 的 LOGFONT 結構與 DirectWrite 字型介面之間進行轉換的方法。 這可讓您針對部分或所有字型列舉和選取專案使用 GDI，同時利用 DirectWrite 的改良功能和效能。 如果您想要在 GDI 介面上顯示文字，DirectWrite 也有介面可轉譯為點陣圖。

## <a name="part-1-idwritegdiinterop"></a>第1部分： IDWriteGdiInterop

[**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop)介面是用來在 GDI 字型結構和 [DirectWrite](direct-write-portal.md)字型介面之間轉換，也可以建立 [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)物件。 使用 [**IDWriteFactory：： GetGdiInterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop)方法取得 **IDWriteGdiInterop** 物件，如下列程式碼所示。


```C++
// Create a GDI interop interface.
if (SUCCEEDED(hr))
{
    hr = g_pDWriteFactory->GetGdiInterop(&g_pGdiInterop);
}
```



## <a name="part-2-font-objects"></a>第2部分：字型物件

GDI 會使用 LOGFONT 結構來儲存字型和文字樣式的相關資訊。 [**IDWriteGdiInterop：： CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)方法會將 LOGFONT 結構轉換成 [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)物件，如下列程式碼所示。


```C++
// Convert to a DirectWrite font.
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateFontFromLOGFONT(&lf, &pFont);
}
```



但是， [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) 不會封裝 LOGFONT 所做的所有相同資訊。 LOGFONT 結構包含字型大小、粗細、樣式、底線、刪除線、字型名稱和一些其他資訊。 **IDWriteFont** 物件包含字型及其粗細和樣式的相關資訊，但不包含字型大小、底線等等。 使用 [DirectWrite](direct-write-portal.md)，格式資訊專案（例如這些專案）會由 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 物件封裝，或是針對特定範圍的文字（ [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件）封裝。

您可以使用 [**IDWriteGdiInterop：： ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)，選擇將 [**IDWRITEFONT**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)轉換成 LOGFONT。

## <a name="part-3-rendering"></a>第3部分：轉譯

若要將 DirectWrite 的文字轉譯成 GDI 介面，請使用自訂文字轉譯器。 請參閱「轉譯 [為 GDI 介面](render-to-a-gdi-surface.md) 」主題。

 

 