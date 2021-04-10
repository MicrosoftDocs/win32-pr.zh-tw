---
description: 本主題說明如何將文字寫入至 XPS OM。
ms.assetid: 5552b7b0-1c95-43fa-ad06-c167c69c5a56
title: 將文字寫入至 XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cca953d5281620cf7b7d9b7b07c133bee0d4de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193611"
---
# <a name="write-text-to-an-xps-om"></a><span data-ttu-id="3549e-103">將文字寫入至 XPS OM</span><span class="sxs-lookup"><span data-stu-id="3549e-103">Write Text to an XPS OM</span></span>

<span data-ttu-id="3549e-104">本主題說明如何將文字寫入至 XPS OM。</span><span class="sxs-lookup"><span data-stu-id="3549e-104">This topic describes how to write text to an XPS OM.</span></span>

<span data-ttu-id="3549e-105">藉由建立 [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) 介面並設定其格式，然後將 **IXpsOMGlyphs** 介面加入至頁面的視覺物件清單或畫布清單中，以將文字置於 XPS OM 中。</span><span class="sxs-lookup"><span data-stu-id="3549e-105">Text is placed in an XPS OM by creating and formatting an [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface and then adding the **IXpsOMGlyphs** interface to the page's or canvas' list of visual objects.</span></span> <span data-ttu-id="3549e-106">每個 **IXpsOMGlyphs** 介面都代表一個圖像執行，這是共用通用格式的連續字元執行。</span><span class="sxs-lookup"><span data-stu-id="3549e-106">Each **IXpsOMGlyphs** interface represents a glyph run, which is a continuous run of characters that share a common format.</span></span> <span data-ttu-id="3549e-107">當字元格式元素 (例如字型類型或大小) 變更或換行時，必須建立新的 **IXpsOMGlyphs** 介面，並將其加入至視覺物件清單。</span><span class="sxs-lookup"><span data-stu-id="3549e-107">When a character format element (such as font type or size) changes or when a line breaks, a new **IXpsOMGlyphs** interface must be created and added to the list of visual objects.</span></span>

<span data-ttu-id="3549e-108">您可以使用 [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) 介面的方法來設定圖像執行的某些屬性。</span><span class="sxs-lookup"><span data-stu-id="3549e-108">Some of the properties of a glyph run can be set by using the methods of the [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface.</span></span> <span data-ttu-id="3549e-109">不過，某些屬性會與其他屬性互動，而且必須使用 [**IXpsOMGlyphsEditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor) 介面進行設定。</span><span class="sxs-lookup"><span data-stu-id="3549e-109">Some properties, however, interact with others and must be set by using an [**IXpsOMGlyphsEditor**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor) interface.</span></span>

<span data-ttu-id="3549e-110">在您的程式中使用下列程式碼範例之前，請閱讀 [一般 XPS 檔程式設計](common-xps-document-tasks.md)工作中的免責聲明。</span><span class="sxs-lookup"><span data-stu-id="3549e-110">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="3549e-111">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="3549e-111">Code Example</span></span>

### <a name="create-a-glyph-run-from-a-string"></a><span data-ttu-id="3549e-112">建立從字串執行的圖像</span><span class="sxs-lookup"><span data-stu-id="3549e-112">Create a glyph run from a string</span></span>

<span data-ttu-id="3549e-113">圖像執行通常會在數個步驟中建立，包括載入圖像執行所使用的字型資源、設定填滿筆刷、指定字型大小和起始位置，以及設定 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="3549e-113">A glyph run is commonly created in several steps that include loading the font resources that are used by the glyph run, setting a fill brush, specifying the font size and starting location, and setting the Unicode string.</span></span>

<span data-ttu-id="3549e-114">程式碼範例的下一節包含接受某些變數的常式，包括字型大小、色彩和位置，以及要寫入的字元。</span><span class="sxs-lookup"><span data-stu-id="3549e-114">The following section of the code example contains a routine that accepts some variables, including the font size, color and location, and the characters to be written.</span></span> <span data-ttu-id="3549e-115">然後，程式碼會建立一個圖像執行，然後將它加入至頁面。</span><span class="sxs-lookup"><span data-stu-id="3549e-115">The code then creates a glyph run and then adds it to a page.</span></span> <span data-ttu-id="3549e-116">此程式碼範例假設已發生 [初始化 XPS OM](xps-object-model-initialization.md) 中所述的初始化，而且檔至少有一個頁面。</span><span class="sxs-lookup"><span data-stu-id="3549e-116">The code example assumes that the initialization described in [Initialize an XPS OM](xps-object-model-initialization.md) has occurred and that the document has at least one page.</span></span> <span data-ttu-id="3549e-117">如需建立空白 XPS OM 的詳細資訊，請參閱 [建立空白的 XPS om](create-a-blank-xps-om.md)。</span><span class="sxs-lookup"><span data-stu-id="3549e-117">For more information about creating a blank XPS OM, refer to [Create a Blank XPS OM](create-a-blank-xps-om.md).</span></span>


```C++
// Write Text to an XPS OM
HRESULT
WriteText_AddTextToPage(
            // A pre-created object factory
    __in    IXpsOMObjectFactory   *xpsFactory,
            // The font resource to use for this run
    __in    IXpsOMFontResource    *xpsFont,
            // The font size
    __in    float                 fontEmSize,
            // The solid color brush to use for the font
    __in    IXpsOMSolidColorBrush *xpsBrush,
            // The starting location of this glyph run
    __in    XPS_POINT             *origin,
            // The text to use for this run
    __in    LPCWSTR               unicodeString,
            // The page on which to write this glyph run
    __inout IXpsOMPage            *xpsPage        
)
{
    // The data type definitions are included in this function
    // for the convenience of this code example. In an actual
    // implementation they would probably belong in a header file.
    HRESULT                       hr = S_OK;
    XPS_POINT                     glyphsOrigin = {origin->x, origin->y};
    IXpsOMGlyphsEditor            *glyphsEditor = NULL;
    IXpsOMGlyphs                  *xpsGlyphs = NULL;
    IXpsOMVisualCollection        *pageVisuals = NULL;

    // Create a new Glyphs object and set its properties.
    hr = xpsFactory->CreateGlyphs(xpsFont, &xpsGlyphs);
    hr = xpsGlyphs->SetOrigin(&glyphsOrigin);
    hr = xpsGlyphs->SetFontRenderingEmSize(fontEmSize);
    hr = xpsGlyphs->SetFillBrushLocal(xpsBrush);

    // Some properties are inter-dependent so they
    //    must be changed by using a GlyphsEditor.
    hr = xpsGlyphs->GetGlyphsEditor(&glyphsEditor);
    hr = glyphsEditor->SetUnicodeString(unicodeString);
    hr = glyphsEditor->ApplyEdits();

    // Add the new Glyphs object to the page
    hr = xpsPage->GetVisuals(&pageVisuals);
    hr = pageVisuals->Append(xpsGlyphs);

    // Release interface pointers.
    if (NULL != xpsGlyphs) xpsGlyphs->Release();
    if (NULL != glyphsEditor) glyphsEditor->Release();
    if (NULL != pageVisuals) pageVisuals->Release();

    return hr;
}
```



### <a name="load-and-create-resources"></a><span data-ttu-id="3549e-118">載入和建立資源</span><span class="sxs-lookup"><span data-stu-id="3549e-118">Load and create resources</span></span>

<span data-ttu-id="3549e-119">建立 [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) 介面需要字型資源。</span><span class="sxs-lookup"><span data-stu-id="3549e-119">Creation of an [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs) interface requires a font resource.</span></span> <span data-ttu-id="3549e-120">在許多情況下，文字區塊會使用相同的字型和色彩。</span><span class="sxs-lookup"><span data-stu-id="3549e-120">In many cases, a block of text uses the same font and color.</span></span> <span data-ttu-id="3549e-121">因此，程式碼範例的這個部分會建立將在頁面上放置文字的呼叫中使用的字型資源介面。</span><span class="sxs-lookup"><span data-stu-id="3549e-121">Hence, this section of the code example will create the font resource interfaces that will be used in the calls that place the text on the page.</span></span>


```C++
    // fontFileName is the name of the font file and it 
    //  is defined outside of this example.

    HRESULT                       hr = S_OK;

    GUID                          fontNameGuid;
    WCHAR                         guidString[128] = {0};
    WCHAR                         uriString[256] = {0};

    IStream                       *fontStream  = NULL;
    IOpcPartUri                   *fontUri = NULL;
    IXpsOMFontResource            *fontResource = NULL;
    IXpsOMVisualCollection        *pageVisuals = NULL;
    IXpsOMPage                    *page = NULL;
    IXpsOMVisual                  *canvasVisual = NULL;
    IXpsOMSolidColorBrush         *xpsTextColor = NULL;
    XPS_COLOR                     xpsColorBodyText;
 
    // Create font stream.
    hr = xpsFactory->CreateReadOnlyStreamOnFile ( 
        fontFileName, &fontStream );
    
    // Create new obfuscated part name for this resource using a GUID.
    hr = CoCreateGuid( &fontNameGuid );
    hr = StringFromGUID2( 
            fontNameGuid, 
            guidString, 
            ARRAYSIZE(guidString));

    // Create a URI string for this font resource that will place 
    //  the font part in the /Resources/Fonts folder of the package.
    wcscpy_s(uriString, ARRAYSIZE(uriString), L"/Resources/Fonts/");

    // Create the part name using the GUID string as the name and 
    //  ".odttf" as the extension GUID string start and ends with 
    //  curly braces so they are removed.
    wcsncat_s(uriString, ARRAYSIZE(uriString), 
        guidString + 1, wcslen(guidString) - 2); 
    wcscat_s(uriString, ARRAYSIZE(uriString), L".odttf");

    // Create the font URI interface.
    hr = xpsFactory->CreatePartUri(
        uriString,
        &fontUri);
    // Create the font resource.
    hr = xpsFactory->CreateFontResource(
        fontStream,
        XPS_FONT_EMBEDDING_OBFUSCATED,
        fontUri,
        FALSE,     // isObfSourceStream
        &fontResource);
    if (NULL != fontUri) fontUri->Release();

    // Create the brush to use for the font.
    xpsColorBodyText.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColorBodyText.value.sRGB.alpha = 0xFF;
    xpsColorBodyText.value.sRGB.red = 0x00;
    xpsColorBodyText.value.sRGB.green = 0x00;
    xpsColorBodyText.value.sRGB.blue = 0x00;

    hr = xpsFactory->CreateSolidColorBrush( 
        &xpsColorBodyText,
        NULL, // This color type does not use a color profile resource.             
        &xpsTextColor);

    // xpsTextColor is released after it has been used.
```



### <a name="draw-text-in-a-page"></a><span data-ttu-id="3549e-122">在頁面中繪製文字</span><span class="sxs-lookup"><span data-stu-id="3549e-122">Draw text in a page</span></span>

<span data-ttu-id="3549e-123">程式碼範例的最後一個區段會為每次執行類似格式化的文字建立圖像執行。</span><span class="sxs-lookup"><span data-stu-id="3549e-123">The final section of the code example creates the glyph runs for each run of similarly formatted text.</span></span> <span data-ttu-id="3549e-124">若要執行這個最後一節中的程式碼， **xpsFactory** 介面以及字型資源和文字色彩筆刷都是必要的，而且必須已經具現化並初始化。</span><span class="sxs-lookup"><span data-stu-id="3549e-124">To execute the code in this final section, the **xpsFactory** interface as well as the font resource and a text color brush are necessary and must have been instantiated and initialized.</span></span> <span data-ttu-id="3549e-125">在此範例中，第一個區段中所述的函式是用來建立圖像執行，並將其加入至頁面。</span><span class="sxs-lookup"><span data-stu-id="3549e-125">In this example, the function described in the first section is used to create the glyph runs and to add them to the page.</span></span>


```C++
    // The following interfaces are created outside of this example.

    // The page on which to place the text.
    IXpsOMPage                *page = NULL;

    // The object factory used by this program.
    IXpsOMObjectFactory       *xpsFactory = NULL;

    // The font resource created in the previous snippet.
    IXpsOMFontResource        *fontResource = NULL;

    // The color brush created in the previous snippet.
    IXpsOMSolidColorBrush     *xpsTextColor = NULL;

    // The following variables are defined outside of this example.

    // An array of pointers to the Unicode strings to write.
    LPCWSTR                   *textRuns = NULL;

    // An array of start points that correspond to the 
    //    strings in textRuns.
    XPS_POINT                 *startPoints = NULL;

    // The number of text runs to add to the page.
    UINT32                    numRuns = 0;            

    HRESULT                   hr = S_OK;

    FLOAT                     fontSize = 7.56f;
    UINT32                    thisRun;

    // Add all the text runs to the page.
    thisRun = 0;
    while (thisRun < numRuns) {  
        hr = WriteText_AddTextToPage(
            xpsFactory, 
            fontResource,
            fontSize,
            xpsTextColor,
            &startPoints[thisRun],
            textRuns[thisRun],
            page);
        thisRun++;
    }
```



## <a name="related-topics"></a><span data-ttu-id="3549e-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="3549e-126">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3549e-127">**後續步驟**</span><span class="sxs-lookup"><span data-stu-id="3549e-127">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="3549e-128">流覽 XPS OM</span><span class="sxs-lookup"><span data-stu-id="3549e-128">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="3549e-129">在 XPS OM 中繪製圖形</span><span class="sxs-lookup"><span data-stu-id="3549e-129">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="3549e-130">以 XPS OM 放置影像</span><span class="sxs-lookup"><span data-stu-id="3549e-130">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="3549e-131">將 XPS OM 寫入 XPS 檔</span><span class="sxs-lookup"><span data-stu-id="3549e-131">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[<span data-ttu-id="3549e-132">列印 XPS OM</span><span class="sxs-lookup"><span data-stu-id="3549e-132">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="3549e-133">**在本節中使用**</span><span class="sxs-lookup"><span data-stu-id="3549e-133">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="3549e-134">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="3549e-134">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="3549e-135">**IXpsOMFontResource**</span><span class="sxs-lookup"><span data-stu-id="3549e-135">**IXpsOMFontResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)
</dt> <dt>

[<span data-ttu-id="3549e-136">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="3549e-136">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)
</dt> <dt>

[<span data-ttu-id="3549e-137">**IXpsOMGlyphsEditor**</span><span class="sxs-lookup"><span data-stu-id="3549e-137">**IXpsOMGlyphsEditor**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphseditor)
</dt> <dt>

[<span data-ttu-id="3549e-138">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="3549e-138">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="3549e-139">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="3549e-139">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="3549e-140">**IXpsOMSolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="3549e-140">**IXpsOMSolidColorBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[<span data-ttu-id="3549e-141">**IXpsOMVisual**</span><span class="sxs-lookup"><span data-stu-id="3549e-141">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)
</dt> <dt>

[<span data-ttu-id="3549e-142">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="3549e-142">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="3549e-143">**詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="3549e-143">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="3549e-144">初始化 XPS OM</span><span class="sxs-lookup"><span data-stu-id="3549e-144">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="3549e-145">XPS 檔 API 參考</span><span class="sxs-lookup"><span data-stu-id="3549e-145">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="3549e-146">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="3549e-146">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
