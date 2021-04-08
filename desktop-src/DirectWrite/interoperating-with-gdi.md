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
# <a name="interoperating-with-gdi"></a><span data-ttu-id="e2289-108">與 GDI 交互操作</span><span class="sxs-lookup"><span data-stu-id="e2289-108">Interoperating with GDI</span></span>

<span data-ttu-id="e2289-109">[DirectWrite](direct-write-portal.md) 會提供的遷移路徑，以及與 GDI 的字型模型之間的互通性，以及將文字轉譯成可在視窗上繪製之點陣圖的介面。</span><span class="sxs-lookup"><span data-stu-id="e2289-109">[DirectWrite](direct-write-portal.md) provides a migration path from, and some interoperability with, GDI's font model, as well as interfaces for rendering text to a bitmap that can then be drawn on a window.</span></span>

<span data-ttu-id="e2289-110">本總覽包含下列部分：</span><span class="sxs-lookup"><span data-stu-id="e2289-110">This overview contains the following parts:</span></span>

-   [<span data-ttu-id="e2289-111">簡介</span><span class="sxs-lookup"><span data-stu-id="e2289-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="e2289-112">第1部分： IDWriteGdiInterop</span><span class="sxs-lookup"><span data-stu-id="e2289-112">Part 1: IDWriteGdiInterop</span></span>](#part-1-idwritegdiinterop)
-   [<span data-ttu-id="e2289-113">第2部分：字型物件</span><span class="sxs-lookup"><span data-stu-id="e2289-113">Part 2: Font Objects</span></span>](#part-2-font-objects)
-   [<span data-ttu-id="e2289-114">第3部分：轉譯</span><span class="sxs-lookup"><span data-stu-id="e2289-114">Part 3: Rendering</span></span>](#part-3-rendering)

## <a name="introduction"></a><span data-ttu-id="e2289-115">簡介</span><span class="sxs-lookup"><span data-stu-id="e2289-115">Introduction</span></span>

<span data-ttu-id="e2289-116">[DirectWrite](direct-write-portal.md) 提供在 GDI 的 LOGFONT 結構與 DirectWrite 字型介面之間進行轉換的方法。</span><span class="sxs-lookup"><span data-stu-id="e2289-116">[DirectWrite](direct-write-portal.md) provides methods for converting between GDI's LOGFONT structure and DirectWrite font interfaces.</span></span> <span data-ttu-id="e2289-117">這可讓您針對部分或所有字型列舉和選取專案使用 GDI，同時利用 DirectWrite 的改良功能和效能。</span><span class="sxs-lookup"><span data-stu-id="e2289-117">This allows you to use GDI for some or all of the font enumeration and selection, while taking advantage of the improved functionality and performance of DirectWrite.</span></span> <span data-ttu-id="e2289-118">如果您想要在 GDI 介面上顯示文字，DirectWrite 也有介面可轉譯為點陣圖。</span><span class="sxs-lookup"><span data-stu-id="e2289-118">DirectWrite also has interfaces for rendering to a bitmap if you want to display text on a GDI surface.</span></span>

## <a name="part-1-idwritegdiinterop"></a><span data-ttu-id="e2289-119">第1部分： IDWriteGdiInterop</span><span class="sxs-lookup"><span data-stu-id="e2289-119">Part 1: IDWriteGdiInterop</span></span>

<span data-ttu-id="e2289-120">[**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop)介面是用來在 GDI 字型結構和 [DirectWrite](direct-write-portal.md)字型介面之間轉換，也可以建立 [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)物件。</span><span class="sxs-lookup"><span data-stu-id="e2289-120">The [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) interface is used to convert between GDI font structures and [DirectWrite](direct-write-portal.md) font interfaces, and also to create an [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object.</span></span> <span data-ttu-id="e2289-121">使用 [**IDWriteFactory：： GetGdiInterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop)方法取得 **IDWriteGdiInterop** 物件，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="e2289-121">Get an **IDWriteGdiInterop** object by using the [**IDWriteFactory::GetGdiInterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) method, as shown in the following code.</span></span>


```C++
// Create a GDI interop interface.
if (SUCCEEDED(hr))
{
    hr = g_pDWriteFactory->GetGdiInterop(&g_pGdiInterop);
}
```



## <a name="part-2-font-objects"></a><span data-ttu-id="e2289-122">第2部分：字型物件</span><span class="sxs-lookup"><span data-stu-id="e2289-122">Part 2: Font Objects</span></span>

<span data-ttu-id="e2289-123">GDI 會使用 LOGFONT 結構來儲存字型和文字樣式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e2289-123">GDI uses the LOGFONT structure to store information about the font and style of text.</span></span> <span data-ttu-id="e2289-124">[**IDWriteGdiInterop：： CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)方法會將 LOGFONT 結構轉換成 [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)物件，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="e2289-124">The [**IDWriteGdiInterop::CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) method will convert a LOGFONT structure to an [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object, as seen in the following code.</span></span>


```C++
// Convert to a DirectWrite font.
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateFontFromLOGFONT(&lf, &pFont);
}
```



<span data-ttu-id="e2289-125">但是， [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) 不會封裝 LOGFONT 所做的所有相同資訊。</span><span class="sxs-lookup"><span data-stu-id="e2289-125">However, [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) does not encapsulate all of the same information that a LOGFONT does.</span></span> <span data-ttu-id="e2289-126">LOGFONT 結構包含字型大小、粗細、樣式、底線、刪除線、字型名稱和一些其他資訊。</span><span class="sxs-lookup"><span data-stu-id="e2289-126">A LOGFONT structure contains the font size, weight, style, underline, strikeout, font face name, and some other information.</span></span> <span data-ttu-id="e2289-127">**IDWriteFont** 物件包含字型及其粗細和樣式的相關資訊，但不包含字型大小、底線等等。</span><span class="sxs-lookup"><span data-stu-id="e2289-127">**IDWriteFont** objects contain information about a font and its weight and style, but not the font size, underline, and so on.</span></span> <span data-ttu-id="e2289-128">使用 [DirectWrite](direct-write-portal.md)，格式資訊專案（例如這些專案）會由 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 物件封裝，或是針對特定範圍的文字（ [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件）封裝。</span><span class="sxs-lookup"><span data-stu-id="e2289-128">With [DirectWrite](direct-write-portal.md), formatting information elements such as these are encapsulated by an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object or, for specific ranges of text, an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="e2289-129">您可以使用 [**IDWriteGdiInterop：： ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)，選擇將 [**IDWRITEFONT**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)轉換成 LOGFONT。</span><span class="sxs-lookup"><span data-stu-id="e2289-129">You do have the option to convert a [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) to a LOGFONT by using the [**IDWriteGdiInterop::ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).</span></span>

## <a name="part-3-rendering"></a><span data-ttu-id="e2289-130">第3部分：轉譯</span><span class="sxs-lookup"><span data-stu-id="e2289-130">Part 3: Rendering</span></span>

<span data-ttu-id="e2289-131">若要將 DirectWrite 的文字轉譯成 GDI 介面，請使用自訂文字轉譯器。</span><span class="sxs-lookup"><span data-stu-id="e2289-131">To render DirectWrite text to a GDI surface you use a custom text renderer.</span></span> <span data-ttu-id="e2289-132">請參閱「轉譯 [為 GDI 介面](render-to-a-gdi-surface.md) 」主題。</span><span class="sxs-lookup"><span data-stu-id="e2289-132">See the [Render to a GDI Surface](render-to-a-gdi-surface.md) topic.</span></span>

 

 