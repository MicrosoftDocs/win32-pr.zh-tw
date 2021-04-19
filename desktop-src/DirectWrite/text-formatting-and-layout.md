---
title: 文字格式設定和版面配置
description: DirectWrite 提供兩個介面來格式化 text IDWriteTextFormat 和 IDWriteTextLayout。
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
ms.openlocfilehash: e9e5790742a3d3caf7f962a6b5e2b3111c626f28
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380752"
---
# <a name="text-formatting-and-layout"></a><span data-ttu-id="d53f8-109">文字格式設定和版面配置</span><span class="sxs-lookup"><span data-stu-id="d53f8-109">Text Formatting and Layout</span></span>

<span data-ttu-id="d53f8-110">[DirectWrite](direct-write-portal.md) 提供兩種用於格式化文字的介面： [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 和 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)。</span><span class="sxs-lookup"><span data-stu-id="d53f8-110">[DirectWrite](direct-write-portal.md) provides two interfaces for formatting text: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="d53f8-111">**IDWriteTextFormat** 只會解說文字的格式，而且在整個字串是相同的字型大小、樣式、粗細等情況下使用。</span><span class="sxs-lookup"><span data-stu-id="d53f8-111">**IDWriteTextFormat** describes only the format for text and is used in cases when an entire string is to be the same font size, style, weight and so on.</span></span> <span data-ttu-id="d53f8-112">另一方面， **IDWriteTextLayout** 會同時封裝文字字串和指定範圍的字串格式。</span><span class="sxs-lookup"><span data-stu-id="d53f8-112">On the other hand, **IDWriteTextLayout** encapsulates both a text string and the formatting for specified ranges of the string.</span></span> <span data-ttu-id="d53f8-113">本檔將說明每個介面及其用途。</span><span class="sxs-lookup"><span data-stu-id="d53f8-113">This document describes each interface and their uses.</span></span> <span data-ttu-id="d53f8-114">如需這些介面的建立和方法的詳細資訊，請參閱 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 和 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 參考頁面。</span><span class="sxs-lookup"><span data-stu-id="d53f8-114">For more information about the creation and methods of these interfaces, see the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference pages.</span></span>

<span data-ttu-id="d53f8-115">本檔包含下列部分：</span><span class="sxs-lookup"><span data-stu-id="d53f8-115">This document contains the following parts:</span></span>

-   [<span data-ttu-id="d53f8-116">IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="d53f8-116">IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
    -   [<span data-ttu-id="d53f8-117">修改 IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="d53f8-117">Modifying an IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
-   [<span data-ttu-id="d53f8-118">IDWriteTextLayout</span><span class="sxs-lookup"><span data-stu-id="d53f8-118">IDWriteTextLayout</span></span>](#idwritetextlayout)
    -   [<span data-ttu-id="d53f8-119">格式化文字範圍</span><span class="sxs-lookup"><span data-stu-id="d53f8-119">Formatting a range of text</span></span>](#formatting-a-range-of-text)
    -   [<span data-ttu-id="d53f8-120">轉譯選項</span><span class="sxs-lookup"><span data-stu-id="d53f8-120">Rendering Options</span></span>](#rendering-options)

## <a name="idwritetextformat"></a><span data-ttu-id="d53f8-121">IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="d53f8-121">IDWriteTextFormat</span></span>

<span data-ttu-id="d53f8-122">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)物件是用來：</span><span class="sxs-lookup"><span data-stu-id="d53f8-122">An [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object is used to:</span></span>

-   <span data-ttu-id="d53f8-123">描述轉譯時整個字串的格式。</span><span class="sxs-lookup"><span data-stu-id="d53f8-123">Describe the format for an entire string when rendering.</span></span> <span data-ttu-id="d53f8-124">若要轉譯具有多種格式的字串，請使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件。</span><span class="sxs-lookup"><span data-stu-id="d53f8-124">To render a string with multiple formats, use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>
-   <span data-ttu-id="d53f8-125">建立 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件時，指定預設文字格式。</span><span class="sxs-lookup"><span data-stu-id="d53f8-125">Specify the default text format when creating an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="d53f8-126">若要建立 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 物件，請使用 [**IDWriteFactory：： CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) 方法，並在 dip) 、地區設定名稱中指定字型系列、字型集合、字型粗細、字型大小 (。</span><span class="sxs-lookup"><span data-stu-id="d53f8-126">To create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object, you use the [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) method and specify the font family, font collection, font weight, font size (in DIPs), locale name.</span></span>

### <a name="modifying-an-idwritetextformat"></a><span data-ttu-id="d53f8-127">修改 IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="d53f8-127">Modifying an IDWriteTextFormat</span></span>

<span data-ttu-id="d53f8-128">一旦建立 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 介面之後，就無法變更部分值：字型系列、集合、粗細和大小，以及地區設定名稱。</span><span class="sxs-lookup"><span data-stu-id="d53f8-128">Once an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface is created, some values cannot be changed: the font family, collection, weight, and size, as well the locale name.</span></span> <span data-ttu-id="d53f8-129">若要變更這些值，必須建立新的 **IDWriteTextFormat** 物件。</span><span class="sxs-lookup"><span data-stu-id="d53f8-129">To change these values, a new **IDWriteTextFormat** object must be created.</span></span>

<span data-ttu-id="d53f8-130">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 可讓您變更上述屬性，而不需要重新建立任何內容。</span><span class="sxs-lookup"><span data-stu-id="d53f8-130">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) enables you to change the properties above without recreating anything.</span></span> <span data-ttu-id="d53f8-131">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 可讓您進行套用至整個文字的格式變更，例如文字對齊。</span><span class="sxs-lookup"><span data-stu-id="d53f8-131">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) enables you to make format changes that apply to the entire text, such as text alignment.</span></span> <span data-ttu-id="d53f8-132">如果您想要將格式設定套用至特定字元範圍，您應該使用 **IDWriteTextLayout**。</span><span class="sxs-lookup"><span data-stu-id="d53f8-132">If you want to apply formatting to specific character ranges, you should do so by using a **IDWriteTextLayout**.</span></span>

<span data-ttu-id="d53f8-133">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 提供的方法可設定文字對齊、流動方向、累加式定位停駐點、行間距、段落對齊、修剪和自動換行。</span><span class="sxs-lookup"><span data-stu-id="d53f8-133">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) provides methods to set the text alignment, flow direction, incremental tab stop, line spacing, paragraph alignment, trimming, and word wrapping.</span></span> <span data-ttu-id="d53f8-134">這些屬性可以在建立 **IDWriteTextFormat** 物件之後隨時變更。</span><span class="sxs-lookup"><span data-stu-id="d53f8-134">These properties can be changed at any time after the creation of the **IDWriteTextFormat** object.</span></span>

## <a name="idwritetextlayout"></a><span data-ttu-id="d53f8-135">IDWriteTextLayout</span><span class="sxs-lookup"><span data-stu-id="d53f8-135">IDWriteTextLayout</span></span>

<span data-ttu-id="d53f8-136">與 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)不同的是， [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)介面代表一段文字和相關的格式。</span><span class="sxs-lookup"><span data-stu-id="d53f8-136">The [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface, unlike [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), represents both a block of text and the associated formatting.</span></span> <span data-ttu-id="d53f8-137">**IDWriteTextFormat** 代表初始格式資訊。</span><span class="sxs-lookup"><span data-stu-id="d53f8-137">**IDWriteTextFormat** represents initial formatting information.</span></span> <span data-ttu-id="d53f8-138">下列範例顯示如何使用 [**IDWriteFactory：： CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)建立 **IDWriteTextLayout** 物件。</span><span class="sxs-lookup"><span data-stu-id="d53f8-138">The following example shows how to create an **IDWriteTextLayout** object using [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).</span></span>


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



<span data-ttu-id="d53f8-139">一旦建立物件之後，就無法變更 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件中的文字。</span><span class="sxs-lookup"><span data-stu-id="d53f8-139">The text in an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object cannot be changed once the object is created.</span></span> <span data-ttu-id="d53f8-140">若要變更文字，您必須刪除現有的物件，並建立新的 **IDWriteTextLayout** 物件。</span><span class="sxs-lookup"><span data-stu-id="d53f8-140">To change the text you must delete the existing object and create a new **IDWriteTextLayout** object.</span></span>

<span data-ttu-id="d53f8-141">您可以使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 來格式化指定的文字範圍。</span><span class="sxs-lookup"><span data-stu-id="d53f8-141">You can use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) to format specified ranges of text.</span></span> <span data-ttu-id="d53f8-142">**IDWriteTextLayout** 也提供方法來變更字型樣式和權數，以及新增 OpenType 字型功能和點擊測試。</span><span class="sxs-lookup"><span data-stu-id="d53f8-142">**IDWriteTextLayout** also provides methods for changing font style and weight, and adding OpenType font features and hit testing.</span></span> <span data-ttu-id="d53f8-143">如需詳細資訊和完整的方法清單，請參閱 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 參考頁面。</span><span class="sxs-lookup"><span data-stu-id="d53f8-143">For more information and a complete list of methods see the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference page.</span></span>

### <a name="formatting-a-range-of-text"></a><span data-ttu-id="d53f8-144">格式化文字範圍</span><span class="sxs-lookup"><span data-stu-id="d53f8-144">Formatting a range of text</span></span>

<span data-ttu-id="d53f8-145">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 提供數種方式來格式化文字範圍。</span><span class="sxs-lookup"><span data-stu-id="d53f8-145">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) provides several methods to format ranges of text.</span></span> <span data-ttu-id="d53f8-146">這些方法的每一個都採用 [**DWRITE \_ 文字 \_ 範圍**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) 結構作為參數，以指定字串內的起始文字位置，以及要格式化的範圍長度。</span><span class="sxs-lookup"><span data-stu-id="d53f8-146">Each of these methods takes a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) structure as a parameter to specify the starting text position within the string and the length of the range to format.</span></span> <span data-ttu-id="d53f8-147">下列範例顯示如何將文字範圍的字型粗細設定為粗體。</span><span class="sxs-lookup"><span data-stu-id="d53f8-147">The following example shows how to set the font weight of a range of text to bold.</span></span>


```C++
// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 5};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

```



### <a name="rendering-options"></a><span data-ttu-id="d53f8-148">轉譯選項</span><span class="sxs-lookup"><span data-stu-id="d53f8-148">Rendering Options</span></span>

<span data-ttu-id="d53f8-149">只有 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 物件所描述之格式設定的文字可以使用 [Direct2D](../direct2d/direct2d-portal.md)來呈現，不過，有幾個選項可以呈現 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件。</span><span class="sxs-lookup"><span data-stu-id="d53f8-149">Text with formatting described by only a [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object can be rendered with [Direct2D](../direct2d/direct2d-portal.md), however, there are a few more options for rendering an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="d53f8-150">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)物件描述的字串可以使用下列方法來呈現。</span><span class="sxs-lookup"><span data-stu-id="d53f8-150">The string described by an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object can be rendered using the methods below.</span></span>

1.  <span data-ttu-id="d53f8-151">[使用 Direct2D](rendering-by-using-direct2d.md)轉譯。</span><span class="sxs-lookup"><span data-stu-id="d53f8-151">[Render using Direct2D](rendering-by-using-direct2d.md).</span></span>
2.  <span data-ttu-id="d53f8-152">[使用自訂文字](how-to-implement-a-custom-text-renderer.md)轉譯器進行轉譯。</span><span class="sxs-lookup"><span data-stu-id="d53f8-152">[Render using a custom text renderer](how-to-implement-a-custom-text-renderer.md).</span></span>
3.  <span data-ttu-id="d53f8-153">轉譯[為 GDI 表面](render-to-a-gdi-surface.md)。</span><span class="sxs-lookup"><span data-stu-id="d53f8-153">[Render to a GDI surface](render-to-a-gdi-surface.md).</span></span>

 

 
