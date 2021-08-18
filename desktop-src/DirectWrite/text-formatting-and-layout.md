---
title: 文字格式設定和版面配置
description: DirectWrite 提供兩個介面來格式化文字 IDWriteTextFormat 和 IDWriteTextLayout。
ms.assetid: a68963a6-e486-4881-8ad6-873173396fca
keywords:
- DirectWrite，文字格式設定
- DirectWrite，版面配置
- DirectWrite，IDWriteTextFormat 介面
- DirectWrite，IDWriteTextLayout 介面
- IDWriteTextFormat 介面
- IDWriteTextLayout 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e67b4c59a7e8ba47a2811021b54ebe1e5b8867b30d07e143163c3d03ac3cdf22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329348"
---
# <a name="text-formatting-and-layout"></a>文字格式設定和版面配置

[DirectWrite](direct-write-portal.md)提供兩個用於格式化文字的介面： [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)和 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)。 **IDWriteTextFormat** 只會解說文字的格式，而且在整個字串是相同的字型大小、樣式、粗細等情況下使用。 另一方面， **IDWriteTextLayout** 會同時封裝文字字串和指定範圍的字串格式。 本檔將說明每個介面及其用途。 如需這些介面的建立和方法的詳細資訊，請參閱 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 和 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 參考頁面。

本檔包含下列部分：

-   [IDWriteTextFormat](#modifying-an-idwritetextformat)
    -   [修改 IDWriteTextFormat](#modifying-an-idwritetextformat)
-   [IDWriteTextLayout](#idwritetextlayout)
    -   [格式化文字範圍](#formatting-a-range-of-text)
    -   [轉譯選項](#rendering-options)

## <a name="idwritetextformat"></a>IDWriteTextFormat

[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)物件是用來：

-   描述轉譯時整個字串的格式。 若要轉譯具有多種格式的字串，請使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件。
-   建立 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件時，指定預設文字格式。

若要建立 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 物件，請使用 [**IDWriteFactory：： CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) 方法，並在 dip) 、地區設定名稱中指定字型系列、字型集合、字型粗細、字型大小 (。

### <a name="modifying-an-idwritetextformat"></a>修改 IDWriteTextFormat

一旦建立 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 介面之後，就無法變更部分值：字型系列、集合、粗細和大小，以及地區設定名稱。 若要變更這些值，必須建立新的 **IDWriteTextFormat** 物件。

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 可讓您變更上述屬性，而不需要重新建立任何內容。 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 可讓您進行套用至整個文字的格式變更，例如文字對齊。 如果您想要將格式設定套用至特定字元範圍，您應該使用 **IDWriteTextLayout**。

[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 提供的方法可設定文字對齊、流動方向、累加式定位停駐點、行間距、段落對齊、修剪和自動換行。 這些屬性可以在建立 **IDWriteTextFormat** 物件之後隨時變更。

## <a name="idwritetextlayout"></a>IDWriteTextLayout

與 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)不同的是， [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)介面代表一段文字和相關的格式。 **IDWriteTextFormat** 代表初始格式資訊。 下列範例顯示如何使用 [**IDWriteFactory：： CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)建立 **IDWriteTextLayout** 物件。


```C++
// Create a text layout using the text format.
if (SUCCEEDED(hr))
{
    RECT rect;
    GetClientRect(hwnd_, &rect); 
    float width  = rect.right  / dpiScaleX_;
    float height = rect.bottom / dpiScaleY_;

    hr = pDWriteFactory_->CreateTextLayout(
        wszText_,      // The string to be laid out and formatted.
        cTextLength_,  // The length of the string.
        pTextFormat_,  // The text format to apply to the string (contains font information, etc).
        width,         // The width of the layout box.
        height,        // The height of the layout box.
        &pTextLayout_  // The IDWriteTextLayout interface pointer.
        );
}

```



一旦建立物件之後，就無法變更 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件中的文字。 若要變更文字，您必須刪除現有的物件，並建立新的 **IDWriteTextLayout** 物件。

您可以使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 來格式化指定的文字範圍。 **IDWriteTextLayout** 也提供方法來變更字型樣式和權數，以及新增 OpenType 字型功能和點擊測試。 如需詳細資訊和完整的方法清單，請參閱 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 參考頁面。

### <a name="formatting-a-range-of-text"></a>格式化文字範圍

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 提供數種方式來格式化文字範圍。 這些方法的每一個都採用 [**DWRITE \_ 文字 \_ 範圍**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) 結構作為參數，以指定字串內的起始文字位置，以及要格式化的範圍長度。 下列範例顯示如何將文字範圍的字型粗細設定為粗體。


```C++
// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 5};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

```



### <a name="rendering-options"></a>轉譯選項

只有 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 物件所描述之格式設定的文字可以使用 [Direct2D](../direct2d/direct2d-portal.md)來呈現，不過，有幾個選項可以呈現 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件。

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)物件描述的字串可以使用下列方法來呈現。

1.  [使用 Direct2D](rendering-by-using-direct2d.md)轉譯。
2.  [使用自訂文字](how-to-implement-a-custom-text-renderer.md)轉譯器進行轉譯。
3.  轉譯[為 GDI 表面](render-to-a-gdi-surface.md)。

 

 
