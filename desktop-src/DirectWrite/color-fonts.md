---
title: 色彩字型
description: 本主題說明色彩字型、其在 DirectWrite 和 Direct2D 方面的支援，以及如何在您的應用程式中使用它們。
ms.assetid: 74e096c4-9d1c-8854-e9ee-f8b11ac1c71a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6774089cc1f0bed1349edc940c6a1ae715d052c7
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "104565571"
---
# <a name="color-fonts"></a><span data-ttu-id="08829-103">色彩字型</span><span class="sxs-lookup"><span data-stu-id="08829-103">Color Fonts</span></span>

<span data-ttu-id="08829-104">本主題說明色彩字型、其在 DirectWrite 和 Direct2D 方面的支援，以及如何在您的應用程式中使用它們。</span><span class="sxs-lookup"><span data-stu-id="08829-104">This topic describes color fonts, their support in DirectWrite and Direct2D, and how to use them in your app.</span></span>

<span data-ttu-id="08829-105">本檔包含下列部分：</span><span class="sxs-lookup"><span data-stu-id="08829-105">This document contains the following parts:</span></span>

-   [<span data-ttu-id="08829-106">什麼是色彩字型？</span><span class="sxs-lookup"><span data-stu-id="08829-106">What are color fonts?</span></span>](#what-are-color-fonts)
-   [<span data-ttu-id="08829-107">為何要使用色彩字型？</span><span class="sxs-lookup"><span data-stu-id="08829-107">Why use color fonts?</span></span>](#why-use-color-fonts)
-   [<span data-ttu-id="08829-108">Windows 支援何種色彩字型？</span><span class="sxs-lookup"><span data-stu-id="08829-108">What kinds of color fonts does Windows support?</span></span>](#what-kinds-of-color-fonts-does-windows-support)
-   [<span data-ttu-id="08829-109">使用色彩字型</span><span class="sxs-lookup"><span data-stu-id="08829-109">Using color fonts</span></span>](#using-color-fonts)
    -   [<span data-ttu-id="08829-110">在 XAML 應用程式中使用色彩字型</span><span class="sxs-lookup"><span data-stu-id="08829-110">Using color fonts in a XAML app</span></span>](#using-color-fonts-in-a-xaml-app)
    -   [<span data-ttu-id="08829-111">在 Microsoft Edge 中使用色彩字型</span><span class="sxs-lookup"><span data-stu-id="08829-111">Using color fonts in Microsoft Edge</span></span>](#using-color-fonts-in-microsoft-edge)
    -   [<span data-ttu-id="08829-112">使用色彩字型搭配 DirectWrite 和 Direct2D</span><span class="sxs-lookup"><span data-stu-id="08829-112">Using color fonts with DirectWrite and Direct2D</span></span>](#using-color-fonts-with-directwrite-and-direct2d)
    -   [<span data-ttu-id="08829-113">使用色彩字型搭配 Win2D</span><span class="sxs-lookup"><span data-stu-id="08829-113">Using color fonts with Win2D</span></span>](#using-color-fonts-with-win2d)
-   [<span data-ttu-id="08829-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="08829-114">Related topics</span></span>](#related-topics)

## <a name="what-are-color-fonts"></a><span data-ttu-id="08829-115">什麼是色彩字型？</span><span class="sxs-lookup"><span data-stu-id="08829-115">What are color fonts?</span></span>

<span data-ttu-id="08829-116">色彩字型（也稱為彩色字型或彩色字型）是一種字型技術，可讓字型設計工具在每個圖像中使用多種色彩。</span><span class="sxs-lookup"><span data-stu-id="08829-116">Color fonts, also referred to as  multicolored fonts  or  chromatic fonts,  are a font technology that allows font designers to use multiple colors within each glyph.</span></span> <span data-ttu-id="08829-117">色彩字型可讓應用程式和網站中的彩色文字案例具有較少的程式碼和更健全的作業系統支援，而不是在文字轉譯系統之上執行的臨機操作技術。</span><span class="sxs-lookup"><span data-stu-id="08829-117">Color fonts enable multicolored text scenarios in apps and websites with less code and more robust operating system support than ad-hoc techniques implemented above the text rendering system.</span></span>

<span data-ttu-id="08829-118">您可能最熟悉的字型不是色彩字型。</span><span class="sxs-lookup"><span data-stu-id="08829-118">The fonts you are probably most familiar with are not color fonts.</span></span> <span data-ttu-id="08829-119">這些字型只會定義其所包含之字元的形狀，包括向量大綱或單色點陣圖。</span><span class="sxs-lookup"><span data-stu-id="08829-119">These fonts define only the shape of the glyphs they contain, either with vector outlines or monochromatic bitmaps.</span></span> <span data-ttu-id="08829-120">在繪圖時，文字轉譯器會使用單一色彩來填滿圖像圖形， (要轉譯的應用程式或檔所指定的字型色彩 ) 。</span><span class="sxs-lookup"><span data-stu-id="08829-120">At draw time, a text renderer fills the glyph shape using a single color (the  font color ) specified by the app or document being rendered.</span></span> <span data-ttu-id="08829-121">另一方面，色彩字型除了圖形資訊之外，還包含色彩資訊。</span><span class="sxs-lookup"><span data-stu-id="08829-121">Color fonts, on the other hand, contain color information in addition to shape information.</span></span> <span data-ttu-id="08829-122">某些方法可讓字型設計工具提供多個色彩調色板，以提供色彩字型藝術彈性。</span><span class="sxs-lookup"><span data-stu-id="08829-122">Some approaches allow font designers to offer multiple color palettes, giving the color font artistic flexibility.</span></span>

<span data-ttu-id="08829-123">下列範例會顯示 Segoe UI 表情色彩字型的圖像。</span><span class="sxs-lookup"><span data-stu-id="08829-123">The following example shows a glyph from the Segoe UI Emoji color font.</span></span> <span data-ttu-id="08829-124">圖像會在左邊以單色轉譯，右邊以色彩呈現。</span><span class="sxs-lookup"><span data-stu-id="08829-124">The glyph is rendered in monochrome on the left, and in color on the right.</span></span>

![顯示並排顯示的字元（以單色呈現的左圖像，在 Segoe U I 表情色彩字型中）。](images/color-font-cat.png)

<span data-ttu-id="08829-126">色彩字型通常包含不支援色彩字型的平臺或已停用色彩功能之案例的回溯資訊。</span><span class="sxs-lookup"><span data-stu-id="08829-126">Color fonts typically include fallback information for platforms that do not support color fonts or for scenarios in which color functionality has been disabled.</span></span> <span data-ttu-id="08829-127">在這些平臺上，色彩字型會轉譯為一般的單色字型。</span><span class="sxs-lookup"><span data-stu-id="08829-127">On those platforms, color fonts are rendered as regular monochromatic fonts.</span></span>

## <a name="why-use-color-fonts"></a><span data-ttu-id="08829-128">為何要使用色彩字型？</span><span class="sxs-lookup"><span data-stu-id="08829-128">Why use color fonts?</span></span>

<span data-ttu-id="08829-129">在過去，設計人員和開發人員已使用各種不同的技術來取得彩色文字。</span><span class="sxs-lookup"><span data-stu-id="08829-129">Historically, designers and developers have used a variety of techniques to achieve multicolored text.</span></span> <span data-ttu-id="08829-130">例如，網站通常會使用點陣影像而非文字，以顯示豐富的標頭。</span><span class="sxs-lookup"><span data-stu-id="08829-130">For example, websites often use raster images instead of text in order to display rich headers.</span></span> <span data-ttu-id="08829-131">這種方法可提供藝術彈性，但點陣圖形不會適當地調整成所有顯示大小，也不會提供與實際文字相同的協助工具功能。</span><span class="sxs-lookup"><span data-stu-id="08829-131">This approach enables artistic flexibility, but raster graphics do not scale well to all display sizes, nor do they provide the same accessibility features as real text.</span></span> <span data-ttu-id="08829-132">另一種常見的技術是以不同的字型色彩覆迭多個單色字型，但這通常需要額外的版面配置程式碼來管理。</span><span class="sxs-lookup"><span data-stu-id="08829-132">Another common technique is to overlay multiple monochromatic fonts in different font colors, but this typically requires extra layout code to manage.</span></span>

<span data-ttu-id="08829-133">色彩字型提供一種方式，可讓您使用一般字型的所有簡潔和功能來達成這些視覺效果。</span><span class="sxs-lookup"><span data-stu-id="08829-133">Color fonts offer a way to achieve these visual effects with all the simplicity and functionality of regular fonts.</span></span> <span data-ttu-id="08829-134">以色彩字型轉譯的文字與其他文字相同：可以複製和貼上、協助工具工具可以剖析它，依此類推。</span><span class="sxs-lookup"><span data-stu-id="08829-134">Text rendered in a color font is the same as other text: it can be copied and pasted, it can be parsed by accessibility tools, and so forth.</span></span>

## <a name="what-kinds-of-color-fonts-does-windows-support"></a><span data-ttu-id="08829-135">Windows 支援何種色彩字型？</span><span class="sxs-lookup"><span data-stu-id="08829-135">What kinds of color fonts does Windows support?</span></span>

<span data-ttu-id="08829-136">[OpenType 規格](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx)定義了數種在字型中內嵌色彩資訊的方式。</span><span class="sxs-lookup"><span data-stu-id="08829-136">The [OpenType specification](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) defines several ways to embed color information in a font.</span></span> <span data-ttu-id="08829-137">從 Windows 10 年度更新版開始，DirectWrite 和 Direct2D (和內建的 Windows framework) 支援所有這些方法。</span><span class="sxs-lookup"><span data-stu-id="08829-137">Starting in Windows 10 Anniversary Update, DirectWrite and Direct2D (and the Windows frameworks built on them) support all of these approaches.</span></span> <span data-ttu-id="08829-138">下表摘要說明這些摘要：</span><span class="sxs-lookup"><span data-stu-id="08829-138">They are summarized in the table below:</span></span>



| <span data-ttu-id="08829-139">技巧</span><span class="sxs-lookup"><span data-stu-id="08829-139">Technique</span></span>                                                                                                                        | <span data-ttu-id="08829-140">描述</span><span class="sxs-lookup"><span data-stu-id="08829-140">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08829-141">[COLR](/typography/opentype/spec/colr) /[CPAL](/typography/opentype/spec/cpal)資料表</span><span class="sxs-lookup"><span data-stu-id="08829-141">[COLR](/typography/opentype/spec/colr)/[CPAL](/typography/opentype/spec/cpal) tables</span></span> | <span data-ttu-id="08829-142">使用彩色向量的圖層，其形狀的定義方式與單一色彩圖像外框外。</span><span class="sxs-lookup"><span data-stu-id="08829-142">Uses layers of colored vectors, whose shapes are defined in the same way as single-color glyph outlines.</span></span> <span data-ttu-id="08829-143">**注意：** 從 Windows 8.1 開始支援。</span><span class="sxs-lookup"><span data-stu-id="08829-143">**Note:** Supported starting in Windows 8.1.</span></span> <br/>                                                                                                                                                 |
| <span data-ttu-id="08829-144">[SVG](/typography/opentype/spec/svg) 資料表</span><span class="sxs-lookup"><span data-stu-id="08829-144">[SVG](/typography/opentype/spec/svg) table</span></span>                                                                 | <span data-ttu-id="08829-145">使用以可擴充向量圖形格式撰寫的向量影像。</span><span class="sxs-lookup"><span data-stu-id="08829-145">Uses vector images authored in the Scalable Vector Graphics format.</span></span> <span data-ttu-id="08829-146">**注意：** 從 Windows 10 年度更新版，DirectWrite 支援完整 SVG 規格的子集。並非所有 SVG 內容都能以 OpenType SVG 字型呈現。</span><span class="sxs-lookup"><span data-stu-id="08829-146">**Note:** As of Windows 10 Anniversary Update, DirectWrite supports a subset of the full SVG spec. Not all SVG content is guaranteed to render in an OpenType SVG font.</span></span> <span data-ttu-id="08829-147">如需詳細資料，請參閱 [SVG 支援](../direct2d/svg-support.md) 。</span><span class="sxs-lookup"><span data-stu-id="08829-147">See [SVG Support](../direct2d/svg-support.md) for more details.</span></span> <br/> |
| <span data-ttu-id="08829-148">[CBDT](/typography/opentype/spec/cbdt) /[CBLC](/typography/opentype/spec/cblc)資料表</span><span class="sxs-lookup"><span data-stu-id="08829-148">[CBDT](/typography/opentype/spec/cbdt)/[CBLC](/typography/opentype/spec/cblc) tables</span></span> | <span data-ttu-id="08829-149">使用內嵌的色彩點陣圖影像。</span><span class="sxs-lookup"><span data-stu-id="08829-149">Uses embedded color bitmap images.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="08829-150">[sbix](/typography/opentype/spec/sbix) 資料表</span><span class="sxs-lookup"><span data-stu-id="08829-150">[sbix](/typography/opentype/spec/sbix) table</span></span>                                                               | <span data-ttu-id="08829-151">使用內嵌的色彩點陣圖影像。</span><span class="sxs-lookup"><span data-stu-id="08829-151">Uses embedded color bitmap images.</span></span>                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a><span data-ttu-id="08829-152">使用色彩字型</span><span class="sxs-lookup"><span data-stu-id="08829-152">Using color fonts</span></span>

<span data-ttu-id="08829-153">從使用者的觀點來看，色彩字型只是字型。</span><span class="sxs-lookup"><span data-stu-id="08829-153">From the user s perspective, color fonts are  just fonts .</span></span> <span data-ttu-id="08829-154">例如，通常可以透過與單色字型相同的方式，從系統安裝和卸載它們，而且它們會轉譯為一般、可選取的文字。</span><span class="sxs-lookup"><span data-stu-id="08829-154">For example, they can usually be installed and uninstalled from the system in the same way as monochromatic fonts, and they are rendered as regular, selectable text.</span></span>

<span data-ttu-id="08829-155">從開發人員的觀點來看，色彩字型的使用方式通常與單色字型相同。</span><span class="sxs-lookup"><span data-stu-id="08829-155">From the developer s perspective too, color fonts are usually used the same way as monochromatic fonts.</span></span> <span data-ttu-id="08829-156">在 XAML 和 Microsoft Edge framework 中，您可以使用色彩字型來將文字樣式的樣式與一般字型相同，而且根據預設，您的文字將會以色彩呈現。</span><span class="sxs-lookup"><span data-stu-id="08829-156">In the XAML and Microsoft Edge frameworks, you can style your text with color fonts the same way as regular fonts, and by default your text will be rendered in color.</span></span> <span data-ttu-id="08829-157">不過，如果您的應用程式直接呼叫 Direct2D Api (或 Win2D Api) 轉譯文字，則必須明確要求色彩字型轉譯。</span><span class="sxs-lookup"><span data-stu-id="08829-157">However, if your app directly calls Direct2D APIs (or Win2D APIs) to render text, it must explicitly request color font rendering.</span></span>

### <a name="using-color-fonts-in-a-xaml-app"></a><span data-ttu-id="08829-158">在 XAML 應用程式中使用色彩字型</span><span class="sxs-lookup"><span data-stu-id="08829-158">Using color fonts in a XAML app</span></span>

<span data-ttu-id="08829-159">XAML 平臺的 text 元素 (例如[TextBlock](/uwp/api/windows.ui.xaml.controls.textblock)、 [TextBox](/uwp/api/windows.ui.xaml.controls.textbox)、 [RichEditBox](/uwp/api/windows.ui.xaml.controls.richeditbox)、圖像和[FontIcon](/uwp/api/windows.ui.xaml.controls.fonticon)) 預設支援色彩[字型](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)。</span><span class="sxs-lookup"><span data-stu-id="08829-159">The XAML platform s text elements (such as [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [RichEditBox](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396), and [FontIcon](/uwp/api/windows.ui.xaml.controls.fonticon)) support color fonts by default.</span></span> <span data-ttu-id="08829-160">只要使用色彩字型來為您的文字加上樣式，就會以色彩轉譯任何色彩字型。</span><span class="sxs-lookup"><span data-stu-id="08829-160">Simply style your text with a color font, and any color glyphs will be rendered in color.</span></span> <span data-ttu-id="08829-161">下列程式碼範例示範使用以應用程式封裝的色彩字型來為 TextBlock 建立樣式的一種方式。</span><span class="sxs-lookup"><span data-stu-id="08829-161">The following code example shows one way to style a TextBlock with a color font packaged with your app.</span></span> <span data-ttu-id="08829-162">相同的技巧也適用于一般字型。</span><span class="sxs-lookup"><span data-stu-id="08829-162">The same technique applies to regular fonts.</span></span>


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



<span data-ttu-id="08829-163">如果您不想要讓 XAML 文字元素轉譯彩色文字，請將其 [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) 屬性設定為 false。</span><span class="sxs-lookup"><span data-stu-id="08829-163">If you never want your XAML text element to render multicolored text, set its [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) property to false.</span></span>

### <a name="using-color-fonts-in-microsoft-edge"></a><span data-ttu-id="08829-164">在 Microsoft Edge 中使用色彩字型</span><span class="sxs-lookup"><span data-stu-id="08829-164">Using color fonts in Microsoft Edge</span></span>

<span data-ttu-id="08829-165">色彩字型預設會在 Microsoft Edge 上執行的網站和 web 應用程式中轉譯，包括 XAML [web](/uwp/api/windows.ui.xaml.controls.webview) 程式控制項。</span><span class="sxs-lookup"><span data-stu-id="08829-165">Color fonts are rendered by default in websites and web apps running on Microsoft Edge, including the XAML [WebView](/uwp/api/windows.ui.xaml.controls.webview) control.</span></span> <span data-ttu-id="08829-166">只要使用 HTML 和 CSS 來為您的文字建立色彩字型的樣式，就會以色彩轉譯任何色彩圖像。</span><span class="sxs-lookup"><span data-stu-id="08829-166">Simply use HTML and CSS to style your text with a color font, and any color glyphs will be rendered in color.</span></span>

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a><span data-ttu-id="08829-167">使用色彩字型搭配 DirectWrite 和 Direct2D</span><span class="sxs-lookup"><span data-stu-id="08829-167">Using color fonts with DirectWrite and Direct2D</span></span>

<span data-ttu-id="08829-168">您的應用程式可以使用 Direct2D 的較高層級文字繪圖方法 ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) 和) [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout) ，也可以使用較低層級的技術來直接繪製圖像執行。</span><span class="sxs-lookup"><span data-stu-id="08829-168">Your app can use Direct2D s higher-level text drawing methods ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) and [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) or it can use lower-level techniques to draw glyph runs directly.</span></span> <span data-ttu-id="08829-169">無論是哪一種情況，您的應用程式都需要變更程式碼，才能正確處理色彩圖像。</span><span class="sxs-lookup"><span data-stu-id="08829-169">In either case, your app requires code changes in order to handle color glyphs correctly.</span></span> <span data-ttu-id="08829-170">如果您的應用程式使用 Direct2D s **DrawText** 和 **DrawTextLayout** api，請注意，這些預設不會轉譯色彩字型。</span><span class="sxs-lookup"><span data-stu-id="08829-170">If your app uses Direct2D s **DrawText** and **DrawTextLayout** APIs, note that these do not render color glyphs by default.</span></span> <span data-ttu-id="08829-171">這是為了避免在色彩字型支援之前設計的文字轉譯應用程式中發生非預期的行為變更。</span><span class="sxs-lookup"><span data-stu-id="08829-171">This is to avoid unexpected behavior changes in text rendering apps that were designed prior to color font support.</span></span>

<span data-ttu-id="08829-172">若要加入宣告色彩字元轉譯，請將 [**D2D1 \_ DRAW \_ TEXT \_ 選項 \_ 啟用 \_ 色彩 \_ 字型**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) 選項旗標傳遞至繪圖方法。</span><span class="sxs-lookup"><span data-stu-id="08829-172">To opt in to color glyph rendering, pass the [**D2D1\_DRAW\_TEXT\_OPTIONS\_ENABLE\_COLOR\_FONT**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) options flag to the drawing method.</span></span> <span data-ttu-id="08829-173">下列程式碼範例示範如何呼叫 Direct2D s DrawText 方法，以色彩字型呈現字串：</span><span class="sxs-lookup"><span data-stu-id="08829-173">The following code example shows how to call Direct2D s DrawText method to render a string in a color font:</span></span>


```C++
// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_defaultFillBrush. 
m_deviceContext->DrawText( 
    m_string->Data(), 
    m_string->Length(), 
    m_textFormat.Get(), 
    m_layoutRect, 
    m_defaultFillBrush.Get(), 
    D2D1_DRAW_TEXT_OPTIONS_ENABLE_COLOR_FONT 
    );  
    
```



<span data-ttu-id="08829-174">如果您的應用程式使用較低層級的 Api 來直接處理圖像執行，則它會在色彩字型存在時繼續運作，但無法在沒有其他邏輯的情況下繪製色彩圖像。</span><span class="sxs-lookup"><span data-stu-id="08829-174">If your app uses lower-level APIs to handle glyph runs directly, then it will continue to function in the presence of color fonts, but it will not be able to draw color glyphs without additional logic.</span></span>

<span data-ttu-id="08829-175">若要正確處理色彩字型，您的應用程式應該：</span><span class="sxs-lookup"><span data-stu-id="08829-175">To correctly handle color glyphs, your app should:</span></span>

1.  <span data-ttu-id="08829-176">將圖像執行資訊傳遞給 [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)，以及 [**DWRITE 影像處理 \_ \_ \_ 格式**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) 參數，指出應用程式準備處理的色彩圖像)  (的類型。</span><span class="sxs-lookup"><span data-stu-id="08829-176">Pass the glyph run information to [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), along with a [**DWRITE\_GLYPH\_IMAGE\_FORMATS**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) parameter that indicates which type(s) of color glyph the app is prepared to handle.</span></span> <span data-ttu-id="08829-177">如果有任何色彩圖像 (根據字型和要求的 **DWRITE \_ \_ 圖像影像 \_ 格式**) ，則 DirectWrite 會將主要圖像執行分割成個別的色彩圖像執行，您可以透過步驟4中傳回的 [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) 物件來存取這些文字。</span><span class="sxs-lookup"><span data-stu-id="08829-177">If any color glyphs are present (based on the font and the requested **DWRITE\_GLYPH\_IMAGE\_FORMATS**), then DirectWrite will split the primary glyph run into individual  color glyph runs  which can be accessed through the returned [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) object in Step 4.</span></span>
2.  <span data-ttu-id="08829-178">檢查 [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) 傳回的 HRESULT，以判斷是否偵測到任何色彩字元執行。</span><span class="sxs-lookup"><span data-stu-id="08829-178">Check the HRESULT returned by [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) to determine whether any color glyph runs were detected.</span></span> <span data-ttu-id="08829-179">**DWRITE \_ E \_ NOCOLOR** 的 **HRESULT** 指出沒有適用的色彩圖像執行。</span><span class="sxs-lookup"><span data-stu-id="08829-179">An **HRESULT** of **DWRITE\_E\_NOCOLOR** indicates no applicable color glyph run.</span></span>
3.  <span data-ttu-id="08829-180">如果 [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) 藉由傳回 **DWRITE \_ E \_ NOCOLOR**) 來 (未回報色彩字元執行，則會將整個圖像執行視為單色，而您的應用程式應該將它繪製為所需的 (例如，使用 [**ID2D1DeviceCoNtext：:D rawglyphrun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)) 。</span><span class="sxs-lookup"><span data-stu-id="08829-180">If [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) reported no color glyph runs (by returning **DWRITE\_E\_NOCOLOR**), then the whole glyph run is treated as monochromatic, and your app should draw it as desired (for example, using [**ID2D1DeviceContext::DrawGlyphRun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).</span></span>
4.  <span data-ttu-id="08829-181">如果 [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) 回報色彩圖像執行的存在，則您的應用程式應該忽略主要圖像執行，並改為使用 TranslateColorGlyphRun 所傳回的色彩字元執行 (s) 。</span><span class="sxs-lookup"><span data-stu-id="08829-181">If [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) does report the presence of color glyph runs, then your app should ignore the primary glyph run and instead use the color glyph run(s) returned by TranslateColorGlyphRun.</span></span> <span data-ttu-id="08829-182">若要這樣做，請逐一查看傳回的 [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) 物件，並依適當的圖像影像格式來繪製每個色彩圖像 (例如，您可以使用 [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) 和 [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) 來) 分別繪製色彩點陣圖字元和 SVG 圖像。</span><span class="sxs-lookup"><span data-stu-id="08829-182">To do so, iterate through the returned [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) object, retrieving each color glyph run and drawing it as appropriate for its glyph image format (for example, you can use [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) and [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) to draw color bitmap glyphs and SVG glyphs, respectively).</span></span>

<span data-ttu-id="08829-183">下列程式碼範例顯示此程式的一般結構：</span><span class="sxs-lookup"><span data-stu-id="08829-183">The following code example shows the general structure of this procedure:</span></span>


```C++
// An example code snippet demonstrating how to use TranslateColorGlyphRun 
// to handle different kinds of color glyphs. This code does not make any 
// actual drawing calls. 
HRESULT DrawGlyphRun( 
    FLOAT baselineOriginX, 
    FLOAT baselineOriginY, 
    DWRITE_MEASURING_MODE measuringMode, 
    _In_ DWRITE_GLYPH_RUN const* glyphRun, 
    _In_ DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription, 
) 
{ 
    // Specify the color glyph formats your app supports. In this example, 
    // the app requests only glyphs defined with PNG or SVG. 
    DWRITE_GLYPH_IMAGE_FORMATS requestedFormats = 
        DWRITE_GLYPH_IMAGE_FORMATS_PNG | DWRITE_GLYPH_IMAGE_FORMATS_SVG; 

    ComPtr<IDWriteColorGlyphRunEnumerator1> glyphRunEnumerator; 
    HRESULT hr = m_dwriteFactory->TranslateColorGlyphRun( 
        D2D1::Point2F(baselineOriginX, baselineOriginY), 
        glyphRun, 
        glyphRunDescription, 
        requestedFormats, // the glyph formats supported by this renderer 
        measuringMode, 
        nullptr, 
        0, 
        &glyphRunEnumerator // on return, may contain color glyph runs 
        ); 

    if (hr == DWRITE_E_NOCOLOR) 
    { 
        // The glyph run has no color glyphs. Draw it as a monochrome glyph 
        // run, for example using the DrawGlyphRun method on a Direct2D 
        // device context. 
    } 
    else 
    { 
        // The glyph run has one or more color glyphs. 
        DX::ThrowIfFailed(hr); 

        // Iterate through the color glyph runs and draw them. 
        for (;;) 
        { 
            BOOL haveRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->MoveNext(&haveRun)); 
            if (!haveRun) 
            { 
                break; 
            } 

            // Retrieve the color glyph run. 
            DWRITE_COLOR_GLYPH_RUN1 const* colorRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->GetCurrentRun(&colorRun)); 

            // Draw the color glyph run depending on its format. 
            switch (colorRun->glyphImageFormat) 
            { 
            case DWRITE_GLYPH_IMAGE_FORMATS_PNG: 
                // Draw the PNG glyph, for example with 
                // ID2D1DeviceContext4::DrawColorBitmapGlyphRun. 
                break; 

            case DWRITE_GLYPH_IMAGE_FORMATS_SVG: 
                // Draw the SVG glyph, for example with 
                // ID2D1DeviceContext4::DrawSvgGlyphRun. 
                break; 

                // ...etc. 
            } 
        } 
    } 

    return hr; 
} 
```



### <a name="using-color-fonts-with-win2d"></a><span data-ttu-id="08829-184">使用色彩字型搭配 Win2D</span><span class="sxs-lookup"><span data-stu-id="08829-184">Using color fonts with Win2D</span></span>

<span data-ttu-id="08829-185">類似于 Direct2D，Win2D s 文字繪製 Api 預設不會轉譯色彩字型。</span><span class="sxs-lookup"><span data-stu-id="08829-185">Similar to Direct2D, Win2D s text drawing APIs do not render color glyphs by default.</span></span> <span data-ttu-id="08829-186">若要加入宣告色彩字元轉譯，請在您的應用程式傳遞給文字繪圖方法的文字格式物件中設定 [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) 選項旗標。</span><span class="sxs-lookup"><span data-stu-id="08829-186">To opt in to color glyph rendering, set the [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) options flag in the text format object your app passes to the text drawing method.</span></span> <span data-ttu-id="08829-187">下列程式碼範例示範如何使用 Win2D，以色彩字型呈現字串：</span><span class="sxs-lookup"><span data-stu-id="08829-187">The following code example shows how to render a string in a color font using Win2D:</span></span>


```C++
// The text format that will be used to draw the text. (Declared elsewhere 
// and initialized elsewhere by the app to point to a color font.) 
CanvasTextFormat m_textFormat; 

// Set the EnableColorFont option. 
m_textFormat.Options = CanvasDrawTextOptions.EnableColorFont; 

// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_color. 
args.DrawingSession.DrawText( 
    m_string, 
    m_point, 
    m_color, 
    m_textFormat 
    ); 
```

## <a name="related-topics"></a><span data-ttu-id="08829-188">相關主題</span><span class="sxs-lookup"><span data-stu-id="08829-188">Related topics</span></span>

[<span data-ttu-id="08829-189">DirectWrite 彩色圖像範例</span><span class="sxs-lookup"><span data-stu-id="08829-189">DirectWrite colored glyph sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[<span data-ttu-id="08829-190">**IDWriteFontFace4 介面**</span><span class="sxs-lookup"><span data-stu-id="08829-190">**IDWriteFontFace4 interface**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[<span data-ttu-id="08829-191">**IDWriteFactory4：： TranslateColorGlyphRun 方法**</span><span class="sxs-lookup"><span data-stu-id="08829-191">**IDWriteFactory4::TranslateColorGlyphRun method**</span></span>](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[<span data-ttu-id="08829-192">**ID2D1DeviceCoNtext4：:D rawText 方法**</span><span class="sxs-lookup"><span data-stu-id="08829-192">**ID2D1DeviceContext4::DrawText method**</span></span>](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 

