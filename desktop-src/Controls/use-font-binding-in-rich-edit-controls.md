---
title: 如何在 Rich Edit 控制項中使用字型系結
description: Microsoft Rich Edit 3.0 會根據其內容將字元集指派為純文字字元。
ms.assetid: 975B9C33-6766-4FF1-A93E-2169C140CEE9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea17c2f8e0e8c1b57611839a5bbf992f9af6bf65
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "103842000"
---
# <a name="how-to-use-font-binding-in-rich-edit-controls"></a><span data-ttu-id="bb4fd-103">如何在 Rich Edit 控制項中使用字型系結</span><span class="sxs-lookup"><span data-stu-id="bb4fd-103">How to Use Font Binding in Rich Edit Controls</span></span>

<span data-ttu-id="bb4fd-104">Microsoft Rich Edit 3.0 會根據其內容將字元集指派為純文字字元。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-104">Microsoft Rich Edit 3.0 assigns a character set to plain-text characters depending on their context.</span></span> <span data-ttu-id="bb4fd-105">部分範例如下：</span><span class="sxs-lookup"><span data-stu-id="bb4fd-105">Some examples are:</span></span>

-   <span data-ttu-id="bb4fd-106">希臘文字元是被指派的 **希臘文 \_ 字元集**。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-106">Greek characters are assigned **GREEK\_CHARSET**.</span></span>
-   <span data-ttu-id="bb4fd-107">韓文符號是指派給 **韓文 \_ 字元集**。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-107">Hangul symbols are assigned **HANGUL\_CHARSET**.</span></span>
-   <span data-ttu-id="bb4fd-108">如果找到附近的假名字元，則會將 **SHIFTJIS \_ 字元集** 指派給中文字元，如果附近找不到假名，則為 **GB2312 \_ 字元集** 。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-108">Chinese characters are assigned **SHIFTJIS\_CHARSET** if kana characters are found nearby, or **GB2312\_CHARSET** if no kana are found nearby.</span></span>
-   <span data-ttu-id="bb4fd-109">在任何事件中，會將 **ansi \_ 字元集** 指派為非中性 ansi 字元。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-109">Non-neutral ANSI characters are assigned **ANSI\_CHARSET** in any event.</span></span>

> [!Note]  
> <span data-ttu-id="bb4fd-110">Rich edit 控制項會在內部使用 Unicode，因此這種字元集的使用方式與字型規格中使用的原始字元集不同。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-110">The rich edit control uses Unicode internally, so this use of character sets differs from the original one used in font specifications.</span></span> <span data-ttu-id="bb4fd-111">但是 [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) 結構具有妥善定義的字元集位置。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-111">But the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure has a well-defined place for the character set.</span></span>

 

<span data-ttu-id="bb4fd-112">空白和數位等中性字元會根據其內容指派一個字元集。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-112">Neutral characters like blanks and digits are assigned a character set depending on their context.</span></span> <span data-ttu-id="bb4fd-113">例如，以相同字元集的字元括住的空白會取得該字元集。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-113">For example, a blank surrounded by characters of the same character set gets that character set.</span></span> <span data-ttu-id="bb4fd-114">雙向文字所使用的 Neutrals 和位數，是以 Unicode 雙向演算法為基礎的指定字元集。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-114">Neutrals and digits used for bidirectional text are assigned character sets in a way that is based on the Unicode bidirectional algorithm.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bb4fd-115">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="bb4fd-115">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bb4fd-116">技術</span><span class="sxs-lookup"><span data-stu-id="bb4fd-116">Technologies</span></span>

-   [<span data-ttu-id="bb4fd-117">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="bb4fd-117">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="bb4fd-118">必要條件</span><span class="sxs-lookup"><span data-stu-id="bb4fd-118">Prerequisites</span></span>

-   <span data-ttu-id="bb4fd-119">C/C++</span><span class="sxs-lookup"><span data-stu-id="bb4fd-119">C/C++</span></span>
-   <span data-ttu-id="bb4fd-120">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="bb4fd-120">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="bb4fd-121">指示</span><span class="sxs-lookup"><span data-stu-id="bb4fd-121">Instructions</span></span>

### <a name="use-font-binding-in-a-rich-edit-control"></a><span data-ttu-id="bb4fd-122">在 Rich Edit 控制項中使用字型系結</span><span class="sxs-lookup"><span data-stu-id="bb4fd-122">Use Font Binding in a Rich Edit Control</span></span>

<span data-ttu-id="bb4fd-123">在指派字元集之後，Rich Edit 會向前和向後掃描插入點周圍的文字，以找出最接近用於字元集的字型。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-123">After character sets are assigned, Rich Edit scans the text around the insertion point forward and backward to find the nearest fonts that have been used for the character sets.</span></span> <span data-ttu-id="bb4fd-124">如果找不到字元集的字型，Rich Edit 會使用用戶端為該字元集所選擇的字型。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-124">If no font is found for a character set, Rich Edit uses the font chosen by the client for that character set.</span></span> <span data-ttu-id="bb4fd-125">如果用戶端尚未指定字元集的字型，Rich Edit 會針對該字元集使用預設字型。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-125">If the client hasn't specified a font for the character set, Rich Edit uses the default font for that character set.</span></span> <span data-ttu-id="bb4fd-126">如果用戶端想要使用其他字型，用戶端一律可以變更它，但這種方法大部分的時候都能運作。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-126">If the client wants some other font, the client can always change it, but this approach will work most of the time.</span></span> <span data-ttu-id="bb4fd-127">目前的預設字型選項是以下表為基礎。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-127">The current default font choices are based on the following table.</span></span> <span data-ttu-id="bb4fd-128">請注意，預設字型是針對每個進程設定的，而且有不同的 UI 使用方式和非 UI 用法清單。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-128">Note that the default fonts are set per-process, and there are separate lists for UI usage and for non-UI usage.</span></span>



| <span data-ttu-id="bb4fd-129">語言</span><span class="sxs-lookup"><span data-stu-id="bb4fd-129">Language</span></span>                    | <span data-ttu-id="bb4fd-130">UI 字型名稱</span><span class="sxs-lookup"><span data-stu-id="bb4fd-130">UI font name</span></span>  | <span data-ttu-id="bb4fd-131">UI 字型大小</span><span class="sxs-lookup"><span data-stu-id="bb4fd-131">UI font size</span></span> | <span data-ttu-id="bb4fd-132">非 UI 字型名稱</span><span class="sxs-lookup"><span data-stu-id="bb4fd-132">non-UI font name</span></span> | <span data-ttu-id="bb4fd-133">非 UI 的字型大小</span><span class="sxs-lookup"><span data-stu-id="bb4fd-133">non-UI font size</span></span> |
|-----------------------------|---------------|--------------|------------------|------------------|
| <span data-ttu-id="bb4fd-134">西方、CE、我、越南文</span><span class="sxs-lookup"><span data-stu-id="bb4fd-134">Western, CE, ME, Vietnamese</span></span> | <span data-ttu-id="bb4fd-135">Tahoma</span><span class="sxs-lookup"><span data-stu-id="bb4fd-135">Tahoma</span></span>        | <span data-ttu-id="bb4fd-136">8</span><span class="sxs-lookup"><span data-stu-id="bb4fd-136">8</span></span>            | <span data-ttu-id="bb4fd-137">Arial</span><span class="sxs-lookup"><span data-stu-id="bb4fd-137">Arial</span></span>            | <span data-ttu-id="bb4fd-138">10</span><span class="sxs-lookup"><span data-stu-id="bb4fd-138">10</span></span>               |
| <span data-ttu-id="bb4fd-139">日文</span><span class="sxs-lookup"><span data-stu-id="bb4fd-139">Japanese</span></span>                    | <span data-ttu-id="bb4fd-140">MS UI Mt</span><span class="sxs-lookup"><span data-stu-id="bb4fd-140">MS UI Gothic</span></span>  | <span data-ttu-id="bb4fd-141">9</span><span class="sxs-lookup"><span data-stu-id="bb4fd-141">9</span></span>            | <span data-ttu-id="bb4fd-142">MS P Mt</span><span class="sxs-lookup"><span data-stu-id="bb4fd-142">MS P Gothic</span></span>      | <span data-ttu-id="bb4fd-143">10</span><span class="sxs-lookup"><span data-stu-id="bb4fd-143">10</span></span>               |
| <span data-ttu-id="bb4fd-144">韓文</span><span class="sxs-lookup"><span data-stu-id="bb4fd-144">Korean</span></span>                      | <span data-ttu-id="bb4fd-145">Gulim</span><span class="sxs-lookup"><span data-stu-id="bb4fd-145">Gulim</span></span>         | <span data-ttu-id="bb4fd-146">9</span><span class="sxs-lookup"><span data-stu-id="bb4fd-146">9</span></span>            | <span data-ttu-id="bb4fd-147">Gulim</span><span class="sxs-lookup"><span data-stu-id="bb4fd-147">Gulim</span></span>            | <span data-ttu-id="bb4fd-148">9</span><span class="sxs-lookup"><span data-stu-id="bb4fd-148">9</span></span>                |
| <span data-ttu-id="bb4fd-149">簡體中文</span><span class="sxs-lookup"><span data-stu-id="bb4fd-149">Simplified Chinese</span></span>          | <span data-ttu-id="bb4fd-150">Simsun</span><span class="sxs-lookup"><span data-stu-id="bb4fd-150">Simsun</span></span>        | <span data-ttu-id="bb4fd-151">9</span><span class="sxs-lookup"><span data-stu-id="bb4fd-151">9</span></span>            | <span data-ttu-id="bb4fd-152">SimSun</span><span class="sxs-lookup"><span data-stu-id="bb4fd-152">SimSun</span></span>           | <span data-ttu-id="bb4fd-153">10</span><span class="sxs-lookup"><span data-stu-id="bb4fd-153">10</span></span>               |
| <span data-ttu-id="bb4fd-154">繁體中文</span><span class="sxs-lookup"><span data-stu-id="bb4fd-154">Traditional Chinese</span></span>         | <span data-ttu-id="bb4fd-155">Simsun</span><span class="sxs-lookup"><span data-stu-id="bb4fd-155">PMingLiU</span></span>      | <span data-ttu-id="bb4fd-156">9</span><span class="sxs-lookup"><span data-stu-id="bb4fd-156">9</span></span>            | <span data-ttu-id="bb4fd-157">Simsun</span><span class="sxs-lookup"><span data-stu-id="bb4fd-157">PMingLiU</span></span>         | <span data-ttu-id="bb4fd-158">9</span><span class="sxs-lookup"><span data-stu-id="bb4fd-158">9</span></span>                |
| <span data-ttu-id="bb4fd-159">泰文</span><span class="sxs-lookup"><span data-stu-id="bb4fd-159">Thai</span></span>                        | <span data-ttu-id="bb4fd-160">MS Sans Serif</span><span class="sxs-lookup"><span data-stu-id="bb4fd-160">MS Sans Serif</span></span> | <span data-ttu-id="bb4fd-161">8</span><span class="sxs-lookup"><span data-stu-id="bb4fd-161">8</span></span>            | <span data-ttu-id="bb4fd-162">Tahoma</span><span class="sxs-lookup"><span data-stu-id="bb4fd-162">Tahoma</span></span>           | <span data-ttu-id="bb4fd-163">14</span><span class="sxs-lookup"><span data-stu-id="bb4fd-163">14</span></span>               |
| <span data-ttu-id="bb4fd-164">符號</span><span class="sxs-lookup"><span data-stu-id="bb4fd-164">Symbols</span></span>                     | <span data-ttu-id="bb4fd-165">Wingdings 應有盡有</span><span class="sxs-lookup"><span data-stu-id="bb4fd-165">Wingdings</span></span>     | <span data-ttu-id="bb4fd-166">8</span><span class="sxs-lookup"><span data-stu-id="bb4fd-166">8</span></span>            | <span data-ttu-id="bb4fd-167">Wingdings 應有盡有</span><span class="sxs-lookup"><span data-stu-id="bb4fd-167">Wingdings</span></span>        | <span data-ttu-id="bb4fd-168">10</span><span class="sxs-lookup"><span data-stu-id="bb4fd-168">10</span></span>               |
| <span data-ttu-id="bb4fd-169">梵文字母</span><span class="sxs-lookup"><span data-stu-id="bb4fd-169">Devanagari</span></span>                  | <span data-ttu-id="bb4fd-170">莽</span><span class="sxs-lookup"><span data-stu-id="bb4fd-170">Mangal</span></span>        | <span data-ttu-id="bb4fd-171">8</span><span class="sxs-lookup"><span data-stu-id="bb4fd-171">8</span></span>            | <span data-ttu-id="bb4fd-172">莽</span><span class="sxs-lookup"><span data-stu-id="bb4fd-172">Mangal</span></span>           | <span data-ttu-id="bb4fd-173">10</span><span class="sxs-lookup"><span data-stu-id="bb4fd-173">10</span></span>               |
| <span data-ttu-id="bb4fd-174">坦米爾文</span><span class="sxs-lookup"><span data-stu-id="bb4fd-174">Tamil</span></span>                       | <span data-ttu-id="bb4fd-175">Latha</span><span class="sxs-lookup"><span data-stu-id="bb4fd-175">Latha</span></span>         | <span data-ttu-id="bb4fd-176">8</span><span class="sxs-lookup"><span data-stu-id="bb4fd-176">8</span></span>            | <span data-ttu-id="bb4fd-177">Latha</span><span class="sxs-lookup"><span data-stu-id="bb4fd-177">Latha</span></span>            | <span data-ttu-id="bb4fd-178">10</span><span class="sxs-lookup"><span data-stu-id="bb4fd-178">10</span></span>               |
| <span data-ttu-id="bb4fd-179">格魯吉亞文，亞美尼亞文</span><span class="sxs-lookup"><span data-stu-id="bb4fd-179">Georgian, Armenian</span></span>          | <span data-ttu-id="bb4fd-180">Arial Unicode</span><span class="sxs-lookup"><span data-stu-id="bb4fd-180">Arial Unicode</span></span> | <span data-ttu-id="bb4fd-181">8</span><span class="sxs-lookup"><span data-stu-id="bb4fd-181">8</span></span>            | <span data-ttu-id="bb4fd-182">Arial Unicode</span><span class="sxs-lookup"><span data-stu-id="bb4fd-182">Arial Unicode</span></span>    | <span data-ttu-id="bb4fd-183">10</span><span class="sxs-lookup"><span data-stu-id="bb4fd-183">10</span></span>               |



 

<span data-ttu-id="bb4fd-184">因此，在預設的字型系結表中 (專案具有字元集、字型名稱和大小) ，Rich Edit 可讓 ANSI \_ 字元集符合數個字元集，而適當的字元集則符合其他字型的一對一基礎。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-184">Therefore, in the default font-binding table (entries have a character set, font name, and size), Rich Edit allows ANSI\_CHARSET to match several character sets, while the appropriate character set matches other fonts on a one-to-one basis.</span></span> <span data-ttu-id="bb4fd-185">更精確地說， \_ 如果找不到其他替代方案，rich edit 會使用 ANSI 字元集選擇。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-185">More precisely, rich edit uses the ANSI\_CHARSET choice whenever no other alternative is found.</span></span> <span data-ttu-id="bb4fd-186">您將能指定比這個更細微的資料細微性;例如，指派阿拉伯文執行的特定阿拉伯文 \_ 字元集、希臘文執行的特定希臘文字型等等。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-186">You will be able to specify a finer granularity than this; for example, assign a specific ARABIC\_CHARSET for Arabic runs, a specific Greek font for Greek runs, and so on.</span></span> <span data-ttu-id="bb4fd-187">如果在字型系結的區域之前，在檔的某處找到具有所需字元集戳記的字型，也會使用這個更細微的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-187">This finer granularity will also be used if a font with the desired character set stamp is found somewhere in the document before the area that is being font-bound.</span></span>

<span data-ttu-id="bb4fd-188">請注意，Rich Edit 目前不會處理支援字元集的字型中遺失的圖像，但不完整。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-188">Note that Rich Edit does not currently handle a missing glyph in a font that claims to support a character set but is incomplete.</span></span> <span data-ttu-id="bb4fd-189">在複雜字集中的顯示時間，Rich Edit 最後會知道這類圖像遺失，但不會導致備份存放區使用新的字型。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-189">At display time in a complex script, Rich Edit does end up knowing that such a glyph is missing, but it does not cause the backing store to use a new font.</span></span> <span data-ttu-id="bb4fd-190">一般而言，作業系統的基礎字型連結將會完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-190">Normally, the underlying font linking of the operating system will accomplish this.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb4fd-191">備註</span><span class="sxs-lookup"><span data-stu-id="bb4fd-191">Remarks</span></span>

<span data-ttu-id="bb4fd-192">**Rich Edit 4.1：** 若要設定腳本的預設字型，請使用 [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)呼叫 [**EM \_ SETCHARFORMAT**](em-setcharformat.md) ，指定 **yHeight**、 **bCharSet**、 **bPitchAndFamily**、 **szFaceName** 和 **lcid** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-192">**Rich Edit 4.1:** To set the default font for a script, call [**EM\_SETCHARFORMAT**](em-setcharformat.md) with [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a), specifying values for the **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName**, and **lcid** members.</span></span> <span data-ttu-id="bb4fd-193">此外，若要取得特定字碼頁的預設字型，請使用 **CHARFORMAT2** 呼叫 [**EM \_ GETCHARFORMAT**](em-getcharformat.md) ，指定 **bCharSet** 和 **lcid** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="bb4fd-193">Also, to get the default font for a specific code page, call [**EM\_GETCHARFORMAT**](em-getcharformat.md) with **CHARFORMAT2**, specifying values for the **bCharSet** and **lcid** members.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb4fd-194">相關主題</span><span class="sxs-lookup"><span data-stu-id="bb4fd-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb4fd-195">使用 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="bb4fd-195">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="bb4fd-196">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="bb4fd-196">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




