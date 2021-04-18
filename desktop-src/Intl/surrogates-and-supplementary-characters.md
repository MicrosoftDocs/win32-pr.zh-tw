---
description: 代理和補充字元
ms.assetid: 0dea39e2-a2b4-47fc-b44a-56af8ba1e346
title: 代理和補充字元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8d6b738955c8b8de4f6cb0ae43c78f86752a928
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971197"
---
# <a name="surrogates-and-supplementary-characters"></a><span data-ttu-id="13a36-103">代理和補充字元</span><span class="sxs-lookup"><span data-stu-id="13a36-103">Surrogates and Supplementary Characters</span></span>

<span data-ttu-id="13a36-104">Windows 應用程式通常會使用 UTF-16 來代表 [Unicode](unicode.md) 字元資料。</span><span class="sxs-lookup"><span data-stu-id="13a36-104">Windows applications normally use UTF-16 to represent [Unicode](unicode.md) character data.</span></span> <span data-ttu-id="13a36-105">使用16個位可直接表示65536的唯一字元，但這個基本多語系平面 (BMP) 幾乎不足以涵蓋人類語言中使用的所有符號。</span><span class="sxs-lookup"><span data-stu-id="13a36-105">The use of 16 bits allows direct representation of 65,536 unique characters, but this Basic Multilingual Plane (BMP) is not nearly enough to cover all the symbols used in human languages.</span></span> <span data-ttu-id="13a36-106">Unicode 4.1 版包含超過97000個字元，且僅適用于中文的超過70000個字元。</span><span class="sxs-lookup"><span data-stu-id="13a36-106">Unicode version 4.1 includes over 97,000 characters, with over 70,000 characters for Chinese alone.</span></span>

<span data-ttu-id="13a36-107">Unicode 標準已建立16個字元的額外「平面」，每個字元的大小都與 BMP 相同。</span><span class="sxs-lookup"><span data-stu-id="13a36-107">The Unicode standard has established 16 additional "planes" of characters, each the same size as the BMP.</span></span> <span data-ttu-id="13a36-108">當然，除了 BMP 以外的大部分程式碼點尚未指派字元給它們，但平面的定義讓 Unicode 有可能定義1114112字元 (也就是在程式 \* 代碼點範圍 u + 0000 到 u + 10FFFF 內，2¹⁶17個) 字元。</span><span class="sxs-lookup"><span data-stu-id="13a36-108">Naturally, most code points beyond the BMP do not yet have characters assigned to them, but definition of the planes gives Unicode the potential to define 1,114,112 characters (that is, 2¹⁶ \* 17 characters) within the code point range U+0000 to U+10FFFF.</span></span> <span data-ttu-id="13a36-109">若為 UTF-16 以表示這組較大的字元組，Unicode 標準會定義「增補字元」。</span><span class="sxs-lookup"><span data-stu-id="13a36-109">For UTF-16 to represent this larger set of characters, the Unicode Standard defines "supplementary characters".</span></span>

## <a name="about-supplementary-characters"></a><span data-ttu-id="13a36-110">關於補充字元</span><span class="sxs-lookup"><span data-stu-id="13a36-110">About Supplementary Characters</span></span>

<span data-ttu-id="13a36-111">補充字元是位在 BMP 以外的字元，而「代理」是 UTF-16 程式碼值。</span><span class="sxs-lookup"><span data-stu-id="13a36-111">A supplementary character is a character located beyond the BMP, and a "surrogate" is a UTF-16 code value.</span></span> <span data-ttu-id="13a36-112">若為 UTF-16，則需要「代理配對」以表示單一補充字元。</span><span class="sxs-lookup"><span data-stu-id="13a36-112">For UTF-16, a "surrogate pair" is required to represent a single supplementary character.</span></span> <span data-ttu-id="13a36-113">第一個 (high) 代理是16位的代碼值，範圍 U + D800 到 U + DBFF。</span><span class="sxs-lookup"><span data-stu-id="13a36-113">The first (high) surrogate is a 16-bit code value in the range U+D800 to U+DBFF.</span></span> <span data-ttu-id="13a36-114">第二個 (低) 代理是16位的代碼值（範圍 U + DC00 到 U + DFFF）。</span><span class="sxs-lookup"><span data-stu-id="13a36-114">The second (low) surrogate is a 16-bit code value in the range U+DC00 to U+DFFF.</span></span> <span data-ttu-id="13a36-115">使用代理機制，UTF-16 可以支援所有1114112可能的 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="13a36-115">Using the surrogate mechanism, UTF-16 can support all 1,114,112 potential Unicode characters.</span></span> <span data-ttu-id="13a36-116">如需有關增補字元、代理程式和代理組的詳細資訊，請參閱 [Unicode 標準](https://www.unicode.org/standard/standard.html)。</span><span class="sxs-lookup"><span data-stu-id="13a36-116">For more details about supplementary characters, surrogates, and surrogate pairs, refer to [The Unicode Standard](https://www.unicode.org/standard/standard.html).</span></span>

> [!Note]  
> <span data-ttu-id="13a36-117">Windows 2000 引進了基本輸入、輸出，以及補充字元的簡單排序支援。</span><span class="sxs-lookup"><span data-stu-id="13a36-117">Windows 2000 introduces support for basic input, output, and simple sorting of supplementary characters.</span></span> <span data-ttu-id="13a36-118">不過，並非所有系統元件都與補充字元相容。</span><span class="sxs-lookup"><span data-stu-id="13a36-118">However, not all system components are compatible with supplementary characters.</span></span>

 

<span data-ttu-id="13a36-119">作業系統可透過下列方式支援補充字元：</span><span class="sxs-lookup"><span data-stu-id="13a36-119">The operating system supports supplementary characters in the following ways:</span></span>

-   <span data-ttu-id="13a36-120">OpenType 字型 cmap 資料表的格式12直接支援4位元組字元碼。</span><span class="sxs-lookup"><span data-stu-id="13a36-120">Format 12 of the OpenType font cmap table directly supports the 4-byte character code.</span></span> <span data-ttu-id="13a36-121">如需詳細資訊，請參閱 [OpenType 字型規格](/typography/opentype/spec/)。</span><span class="sxs-lookup"><span data-stu-id="13a36-121">For more information, see the [OpenType font specification](/typography/opentype/spec/).</span></span>
-   <span data-ttu-id="13a36-122">Windows 支援已啟用代理功能的 [輸入方法編輯器 (ime) ](../dxtecharts/installing-and-using-input-method-editors.md)。</span><span class="sxs-lookup"><span data-stu-id="13a36-122">Windows supports surrogate-enabled [input method editors (IMEs)](../dxtecharts/installing-and-using-input-method-editors.md).</span></span>
-   <span data-ttu-id="13a36-123">[WINDOWS GDI](../gdi/windows-gdi.md) API 支援在字型中格式化12個 cmap 資料表，讓代理程式可以正確顯示。</span><span class="sxs-lookup"><span data-stu-id="13a36-123">The [Windows GDI](../gdi/windows-gdi.md) API supports format 12 cmap tables in fonts so that surrogates can be displayed correctly.</span></span>
-   <span data-ttu-id="13a36-124">[Uniscribe](uniscribe.md) API 支援補充字元。</span><span class="sxs-lookup"><span data-stu-id="13a36-124">The [Uniscribe](uniscribe.md) API supports supplementary characters.</span></span>
-   <span data-ttu-id="13a36-125">[Windows 控制項](../controls/window-controls.md)（包括 [編輯](../controls/edit-controls.md) 和 [Rich edit](../controls/rich-edit-controls.md)）支援補充字元。</span><span class="sxs-lookup"><span data-stu-id="13a36-125">[Windows controls](../controls/window-controls.md), including [Edit](../controls/edit-controls.md) and [Rich Edit](../controls/rich-edit-controls.md), support supplementary characters.</span></span>
-   <span data-ttu-id="13a36-126">HTML 引擎支援包含補充字元的 HTML 網頁，可透過 Outlook Express) 和表單提交來顯示、編輯 (。</span><span class="sxs-lookup"><span data-stu-id="13a36-126">The HTML engine supports HTML pages that include supplementary characters for display, editing (through Outlook Express), and forms submission.</span></span>
-   <span data-ttu-id="13a36-127">作業系統排序表支援補充字元。</span><span class="sxs-lookup"><span data-stu-id="13a36-127">The operating system sorting table supports supplementary characters.</span></span>

## <a name="general-guidelines-for-software-development-using-supplementary-characters"></a><span data-ttu-id="13a36-128">使用補充字元進行軟體發展的一般指導方針</span><span class="sxs-lookup"><span data-stu-id="13a36-128">General Guidelines for Software Development Using Supplementary Characters</span></span>

<span data-ttu-id="13a36-129">UTF-16 會將補充字元處理為代理組。</span><span class="sxs-lookup"><span data-stu-id="13a36-129">UTF-16 handles supplementary characters as surrogate pairs.</span></span> <span data-ttu-id="13a36-130">作業系統會以類似于處理非 [間距標記](using-nonspacing-characters-and-diacritics.md)的方式來處理代理配對。</span><span class="sxs-lookup"><span data-stu-id="13a36-130">The operating system processes a surrogate pair similarly to the way it processes [nonspacing marks](using-nonspacing-characters-and-diacritics.md).</span></span> <span data-ttu-id="13a36-131">在顯示時間，代理字組會透過 Unicode 標準所規定，以 Uniscribe 的方式顯示為一個圖像。</span><span class="sxs-lookup"><span data-stu-id="13a36-131">At display time, the surrogate pair displays as one glyph by means of Uniscribe, as prescribed by the Unicode Standard.</span></span>

<span data-ttu-id="13a36-132">Windows Vista 引進了三個新宏，以協助識別 UTF-16 字串中的代理和代理配對。</span><span class="sxs-lookup"><span data-stu-id="13a36-132">Windows Vista introduces three new macros to help identify surrogates and surrogate pairs in UTF-16 strings.</span></span> <span data-ttu-id="13a36-133">這些都 [**是 \_ 高 \_ 代理**](/windows/win32/api/Winnls/nf-winnls-is_high_surrogate)、 [**\_ 低 \_ 代理**](/windows/win32/api/Winnls/nf-winnls-is_low_surrogate)和 [**\_ 代理 \_ 配對**](/windows/win32/api/Winnls/nf-winnls-is_surrogate_pair)。</span><span class="sxs-lookup"><span data-stu-id="13a36-133">These are [**IS\_HIGH\_SURROGATE**](/windows/win32/api/Winnls/nf-winnls-is_high_surrogate), [**IS\_LOW\_SURROGATE**](/windows/win32/api/Winnls/nf-winnls-is_low_surrogate), and [**IS\_SURROGATE\_PAIR**](/windows/win32/api/Winnls/nf-winnls-is_surrogate_pair).</span></span>

<span data-ttu-id="13a36-134">如果應用程式支援 Unicode 並使用系統控制項和標準 API 函式（例如 [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) 和 [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)），則會自動支援補充字元。</span><span class="sxs-lookup"><span data-stu-id="13a36-134">Applications automatically support supplementary characters if they support Unicode and use system controls and standard API functions, such as [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) and [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="13a36-135">因此，如果您的應用程式使用標準系統控制項，或使用一般 [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)類型呼叫來顯示，補充字元應該可以運作，而不需要任何特殊的編碼。</span><span class="sxs-lookup"><span data-stu-id="13a36-135">Thus, if your application uses standard system controls or uses general [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)-type calls to display, supplementary characters should work without any special coding.</span></span>

<span data-ttu-id="13a36-136">以自訂方式來處理圖像位置的應用程式，可以使用 Uniscribe 進行所有文字處理，藉此實現自己的編輯支援。</span><span class="sxs-lookup"><span data-stu-id="13a36-136">Applications that implement their own editing support by working out glyph positions in a customized way can use Uniscribe for all text processing.</span></span> <span data-ttu-id="13a36-137">Uniscribe 有不同的函式來處理複雜的腳本處理，例如文字顯示、點擊測試和資料指標移動。</span><span class="sxs-lookup"><span data-stu-id="13a36-137">Uniscribe has separate functions to deal with complex script processing, such as text display, hit testing, and cursor movement.</span></span> <span data-ttu-id="13a36-138">應用程式必須專門呼叫 Uniscribe 函式，才能取得這些先進的功能。</span><span class="sxs-lookup"><span data-stu-id="13a36-138">An application must call the Uniscribe functions specifically to get these advanced features.</span></span> <span data-ttu-id="13a36-139">請注意，使用 Uniscribe 函式的應用程式完全是多語系的，但這會造成效能上的負面影響。</span><span class="sxs-lookup"><span data-stu-id="13a36-139">Note that applications using the Uniscribe functions are fully multilingual, but this imposes a performance penalty.</span></span> <span data-ttu-id="13a36-140">因此，有些應用程式應該自行處理補充字元。</span><span class="sxs-lookup"><span data-stu-id="13a36-140">Thus some applications should do their own processing of supplementary characters.</span></span>

<span data-ttu-id="13a36-141">因為代表補充字元的代理機制是妥善定義的，所以您的應用程式可以包含程式碼來處理 UTF-16 代理文字處理。</span><span class="sxs-lookup"><span data-stu-id="13a36-141">Because the surrogate mechanism to represent supplementary characters is well-defined, your application can include code to handle UTF-16 surrogate text processing.</span></span> <span data-ttu-id="13a36-142">當應用程式從較低的保留代理範圍 (低代理) 或較高的保留代理範圍（ (高代理) ）遇到分隔的 UTF-16 值時，此值必須是代理配對的一半。</span><span class="sxs-lookup"><span data-stu-id="13a36-142">When the application encounters a separated UTF-16 value from either the lower reserved surrogate range (a low surrogate) or the upper reserved surrogate range (a high surrogate), the value must be one half of a surrogate pair.</span></span> <span data-ttu-id="13a36-143">因此，應用程式可以藉由執行簡單的範圍檢查，來偵測代理程式配對。</span><span class="sxs-lookup"><span data-stu-id="13a36-143">Thus, the application can detect a surrogate pair by doing simple range checking.</span></span> <span data-ttu-id="13a36-144">如果它在較低或上限的範圍內遇到 UTF-16 值，它必須向前或向後再追蹤 1 16 位的寬度，才能取得字元的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="13a36-144">If it encounters a UTF-16 value in the lower or upper range, it must track backward or forward one 16-bit width to get the rest of the character.</span></span> <span data-ttu-id="13a36-145">撰寫您的應用程式時，請記住， [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta) 和 [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva) 是由16位程式碼點移動，而不是由代理配對所移動。</span><span class="sxs-lookup"><span data-stu-id="13a36-145">When writing your application, keep in mind that [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta) and [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva) move by 16-bit code points, not by surrogate pairs.</span></span>

> [!Note]  
> <span data-ttu-id="13a36-146">獨立代理程式碼點具有高代理（沒有連續的低代理），反之亦然。</span><span class="sxs-lookup"><span data-stu-id="13a36-146">Standalone surrogate code points have either a high surrogate without an adjacent low surrogate, or vice versa.</span></span> <span data-ttu-id="13a36-147">這些程式碼點無效，且不受支援。</span><span class="sxs-lookup"><span data-stu-id="13a36-147">These code points are invalid and are not supported.</span></span> <span data-ttu-id="13a36-148">它們的行為未定義。</span><span class="sxs-lookup"><span data-stu-id="13a36-148">Their behavior is undefined.</span></span>

 

<span data-ttu-id="13a36-149">如果您正在開發字型或 IME 提供者，請注意 Windows 之前的 XP 作業系統預設會停用補充字元支援。</span><span class="sxs-lookup"><span data-stu-id="13a36-149">If you are developing a font or IME provider, note that pre-Windows XP operating systems disable supplementary character support by default.</span></span> <span data-ttu-id="13a36-150">Windows XP 和更新版本預設會啟用補充字元。</span><span class="sxs-lookup"><span data-stu-id="13a36-150">Windows XP and later enable supplementary characters by default.</span></span> <span data-ttu-id="13a36-151">如果您提供的字型和 IME 套件需要補充字元，則您的應用程式必須設定下列登錄值：</span><span class="sxs-lookup"><span data-stu-id="13a36-151">If you provide a font and IME package that requires supplementary characters, your application must set the following registry values:</span></span>


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\LanguagePack]
SURROGATE=(REG_DWORD)0x00000002

[HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\International\Scripts\42]
IEFixedFontName=[Surrogate Font Face Name]
IEPropFontName=[Surrogate Font Face Name]
```



## <a name="related-topics"></a><span data-ttu-id="13a36-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="13a36-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13a36-153">字元集</span><span class="sxs-lookup"><span data-stu-id="13a36-153">Character Sets</span></span>](character-sets.md)
</dt> </dl>

 

 
