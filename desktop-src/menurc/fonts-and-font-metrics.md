---
title: 字型和文字度量
description: 本主題討論 Windows 所提供的大綱字型、可能在 Windows 版本之間變更的字型計量值，以及如何在傳統型應用程式中使用字型計量的指引。
ms.assetid: B195154D-0168-4C5E-9CFB-AE7EF63D5F42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da27d4eb5f34f5a88e4a0e3e866f9a14784c3895
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933229"
---
# <a name="fonts-and-text-metrics"></a><span data-ttu-id="6e0d9-103">字型和文字度量</span><span class="sxs-lookup"><span data-stu-id="6e0d9-103">Fonts and text metrics</span></span>

<span data-ttu-id="6e0d9-104">本主題討論 Windows 所提供的大綱字型、可能在 Windows 版本之間變更的字型計量值，以及如何在傳統型應用程式中使用字型計量的指引。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-104">This topic discusses the outline fonts provided by Windows, font metric values that may change between versions of Windows, and guidance for how to use font metrics in your desktop apps.</span></span>

-   <span data-ttu-id="6e0d9-105">如需 DirectWrite 中字型度量的特定資訊，請參閱 [文字度量](/windows/desktop/DirectWrite/text-metrics)。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-105">For info specific to font metrics in DirectWrite, see [Text Metrics](/windows/desktop/DirectWrite/text-metrics).</span></span>
-   <span data-ttu-id="6e0d9-106">如需使用 GDI 來管理應用程式文字的詳細資訊，請參閱字型 [和文字](/windows/desktop/gdi/fonts-and-text)中的主題。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-106">For details on managing text in apps using GDI, see the topics in [Fonts and Text](/windows/desktop/gdi/fonts-and-text).</span></span>

<span data-ttu-id="6e0d9-107">如需字型使用方式和類型規格的詳細資訊，請參閱 [Microsoft 印刷樣式網站](https://www.microsoft.com/typography/default.mspx)。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-107">For more detailed information on font usage and type specifications, see the [Microsoft typography site](https://www.microsoft.com/typography/default.mspx).</span></span>

## <a name="available-fonts"></a><span data-ttu-id="6e0d9-108">可用的字型</span><span class="sxs-lookup"><span data-stu-id="6e0d9-108">Available fonts</span></span>

<span data-ttu-id="6e0d9-109">Windows 提供的大綱字型會以 OpenType 字型的形式傳遞， (Windows 也支援 CFF 格式) 的 OpenType 字型。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-109">The outline fonts supplied with Windows are delivered as OpenType fonts with TrueType outlines (Windows also supports OpenType fonts in the CFF format).</span></span> <span data-ttu-id="6e0d9-110">如需 Windows 所提供的所有字型清單，請參閱 [Microsoft 印刷樣式：依產品或系列](https://www.microsoft.com/typography/fonts/default.aspx)提供的字型。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-110">For lists of all fonts supplied by Windows, see [Microsoft typography: fonts by product or family](https://www.microsoft.com/typography/fonts/default.aspx).</span></span> <span data-ttu-id="6e0d9-111">所有的 Windows 大綱字型都符合最新版本的 [OpenType 規格](https://www.microsoft.com/typography/otspec/)。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-111">All Windows outline fonts conform to the latest version of the [OpenType specification](https://www.microsoft.com/typography/otspec/).</span></span>

<span data-ttu-id="6e0d9-112">如需所有目前和舊版 UI 字型的清單，請參閱下方的 [鎖定字型計量](#locked-font-metrics) 。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-112">For a list of all the current and legacy UI fonts, see [Locked font metrics](#locked-font-metrics) below.</span></span>

## <a name="font-modifications"></a><span data-ttu-id="6e0d9-113">字型修改</span><span class="sxs-lookup"><span data-stu-id="6e0d9-113">Font modifications</span></span>

<span data-ttu-id="6e0d9-114">為了確保回溯相容性，字型很少會從視窗中移除。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-114">To assure backwards compatibility, fonts are rarely removed from Windows.</span></span> <span data-ttu-id="6e0d9-115">不過，字型通常會經過修改。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-115">However, fonts are often modified.</span></span> <span data-ttu-id="6e0d9-116">修改可能包括新增字元、重新繪製現有的字元、修改提示，或是新增或修改先進 OpenType 功能和複雜字集成形的支援。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-116">Modifications may include adding characters, redrawing existing characters, modifying hints, or adding or modifying support for advanced OpenType features and complex script shaping.</span></span>

### <a name="locked-font-metrics"></a><span data-ttu-id="6e0d9-117">鎖定的字型計量</span><span class="sxs-lookup"><span data-stu-id="6e0d9-117">Locked font metrics</span></span>

<span data-ttu-id="6e0d9-118">請注意，某些與 Microsoft 應用程式中使用的 UI 字型和預設字型相關聯的值已鎖定。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-118">Note that some values associated with UI fonts and default fonts used in Microsoft apps are locked.</span></span> <span data-ttu-id="6e0d9-119">UI 字型可用來呈現 UI 專案，例如字幕、對話方塊和功能表。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-119">UI fonts are used to render UI elements like captions, dialogs, and menus.</span></span> <span data-ttu-id="6e0d9-120">對這些字型進行極少的變更，並提供其高可見度和頻繁使用。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-120">Very few changes are made to these fonts, given their high visibility and frequent use.</span></span> <span data-ttu-id="6e0d9-121">不過，因為與這些字型相關聯的報告值已鎖定，所以報告和實際字型值之間可能會有不一致的情況。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-121">However, because the reported values associated with these fonts are locked, there may be discrepancies between reported and actual font values.</span></span>

<span data-ttu-id="6e0d9-122">下列報告值會針對 UI 和預設字型鎖定，而且可能會被不准確地報告：</span><span class="sxs-lookup"><span data-stu-id="6e0d9-122">The following reported values are locked for UI and default fonts, and may be inaccurately reported:</span></span>

-   <span data-ttu-id="6e0d9-123">字型的 [OS/2 資料表](https://www.microsoft.com/typography/otspec/os2.htm)中的這些值：</span><span class="sxs-lookup"><span data-stu-id="6e0d9-123">These values from the font’s [OS/2 table](https://www.microsoft.com/typography/otspec/os2.htm):</span></span>
    -   <span data-ttu-id="6e0d9-124">xAvgCharWidth</span><span class="sxs-lookup"><span data-stu-id="6e0d9-124">xAvgCharWidth</span></span>
    -   <span data-ttu-id="6e0d9-125">sTypoLineGap</span><span class="sxs-lookup"><span data-stu-id="6e0d9-125">sTypoLineGap</span></span>
    -   <span data-ttu-id="6e0d9-126">sTypoAscender</span><span class="sxs-lookup"><span data-stu-id="6e0d9-126">sTypoAscender</span></span>
    -   <span data-ttu-id="6e0d9-127">sTypoDescender</span><span class="sxs-lookup"><span data-stu-id="6e0d9-127">sTypoDescender</span></span>
    -   <span data-ttu-id="6e0d9-128">usWinAscent</span><span class="sxs-lookup"><span data-stu-id="6e0d9-128">usWinAscent</span></span>
    -   <span data-ttu-id="6e0d9-129">usWinDescent</span><span class="sxs-lookup"><span data-stu-id="6e0d9-129">usWinDescent</span></span>
-   <span data-ttu-id="6e0d9-130">在字型標頭中設定的 [unitsPerEm](https://www.microsoft.com/typography/otspec/head.htm) 值</span><span class="sxs-lookup"><span data-stu-id="6e0d9-130">The [unitsPerEm](https://www.microsoft.com/typography/otspec/head.htm) value set in the font’s header</span></span>
-   <span data-ttu-id="6e0d9-131">[垂直裝置計量表中的值 (VDMX) ](https://www.microsoft.com/typography/otspec/vdmx.htm)</span><span class="sxs-lookup"><span data-stu-id="6e0d9-131">Values from the [Vertical Device metrics table (VDMX)](https://www.microsoft.com/typography/otspec/vdmx.htm)</span></span>
-   <span data-ttu-id="6e0d9-132">個別字元的前進寬度</span><span class="sxs-lookup"><span data-stu-id="6e0d9-132">The advance widths for individual glyphs</span></span>

<span data-ttu-id="6e0d9-133">以下是受鎖定值影響的 Windows 8.1 (所附的 UI 字型清單) ：</span><span class="sxs-lookup"><span data-stu-id="6e0d9-133">Here's a list of the UI fonts shipped with Windows 8.1 (affected by locked values):</span></span>

| <span data-ttu-id="6e0d9-134">指令碼名稱</span><span class="sxs-lookup"><span data-stu-id="6e0d9-134">Script name</span></span>                   | <span data-ttu-id="6e0d9-135">UI 字型</span><span class="sxs-lookup"><span data-stu-id="6e0d9-135">UI font</span></span>               |
|-------------------------------|-----------------------|
| <span data-ttu-id="6e0d9-136">阿拉伯文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-136">Arabic</span></span>                        | <span data-ttu-id="6e0d9-137">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-137">Segoe UI</span></span>              |
| <span data-ttu-id="6e0d9-138">亞美尼亞文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-138">Armenian</span></span>                      | <span data-ttu-id="6e0d9-139">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-139">Segoe UI</span></span>              |
| <span data-ttu-id="6e0d9-140">孟加拉國文 (先前為孟加拉國文) </span><span class="sxs-lookup"><span data-stu-id="6e0d9-140">Bangla (formerly Bengali)</span></span>     | <span data-ttu-id="6e0d9-141">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-141">Nirmala UI</span></span>            |
| <span data-ttu-id="6e0d9-142">符號</span><span class="sxs-lookup"><span data-stu-id="6e0d9-142">Bopomofo</span></span>                      | <span data-ttu-id="6e0d9-143">Microsoft JhengHei UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-143">Microsoft JhengHei UI</span></span> |
| <span data-ttu-id="6e0d9-144">盲文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-144">Braille</span></span>                       | <span data-ttu-id="6e0d9-145">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="6e0d9-145">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="6e0d9-146">布吉斯文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-146">Buginese</span></span>                      | <span data-ttu-id="6e0d9-147">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-147">Leelawadee UI</span></span>         |
| <span data-ttu-id="6e0d9-148">加拿大土著音節</span><span class="sxs-lookup"><span data-stu-id="6e0d9-148">Canadian Aboriginal Syllabics</span></span> | <span data-ttu-id="6e0d9-149">Gadugi</span><span class="sxs-lookup"><span data-stu-id="6e0d9-149">Gadugi</span></span>                |
| <span data-ttu-id="6e0d9-150">卻洛奇文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-150">Cherokee</span></span>                      | <span data-ttu-id="6e0d9-151">Gadugi</span><span class="sxs-lookup"><span data-stu-id="6e0d9-151">Gadugi</span></span>                |
| <span data-ttu-id="6e0d9-152">科普特文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-152">Coptic</span></span>                        | <span data-ttu-id="6e0d9-153">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="6e0d9-153">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="6e0d9-154">簡體中文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-154">Chinese (Simplified)</span></span>          | <span data-ttu-id="6e0d9-155">Microsoft YaHei UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-155">Microsoft YaHei UI</span></span>    |
| <span data-ttu-id="6e0d9-156">繁體中文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-156">Chinese (Traditional)</span></span>         | <span data-ttu-id="6e0d9-157">Microsoft JhengHei UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-157">Microsoft JhengHei UI</span></span> |
| <span data-ttu-id="6e0d9-158">古斯拉夫文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-158">Cyrillic</span></span>                      | <span data-ttu-id="6e0d9-159">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-159">Segoe UI</span></span>              |
| <span data-ttu-id="6e0d9-160">梵文字母</span><span class="sxs-lookup"><span data-stu-id="6e0d9-160">Devanagari</span></span>                    | <span data-ttu-id="6e0d9-161">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-161">Nirmala UI</span></span>            |
| <span data-ttu-id="6e0d9-162">萊特</span><span class="sxs-lookup"><span data-stu-id="6e0d9-162">Deseret</span></span>                       | <span data-ttu-id="6e0d9-163">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="6e0d9-163">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="6e0d9-164">文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-164">Ethiopic</span></span>                      | <span data-ttu-id="6e0d9-165">Ebrima</span><span class="sxs-lookup"><span data-stu-id="6e0d9-165">Ebrima</span></span>                |
| <span data-ttu-id="6e0d9-166">喬治亞文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-166">Georgian</span></span>                      | <span data-ttu-id="6e0d9-167">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-167">Segoe UI</span></span>              |
| <span data-ttu-id="6e0d9-168">文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-168">Glagolitic</span></span>                    | <span data-ttu-id="6e0d9-169">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="6e0d9-169">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="6e0d9-170">哥 特 式</span><span class="sxs-lookup"><span data-stu-id="6e0d9-170">Gothic</span></span>                        | <span data-ttu-id="6e0d9-171">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="6e0d9-171">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="6e0d9-172">希臘文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-172">Greek</span></span>                         | <span data-ttu-id="6e0d9-173">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-173">Segoe UI</span></span>              |
| <span data-ttu-id="6e0d9-174">古吉拉特文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-174">Gujarati</span></span>                      | <span data-ttu-id="6e0d9-175">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-175">Nirmala UI</span></span>            |
| <span data-ttu-id="6e0d9-176">古木基文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-176">Gurmukhi</span></span>                      | <span data-ttu-id="6e0d9-177">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-177">Nirmala UI</span></span>            |
| <span data-ttu-id="6e0d9-178">Hebrew</span><span class="sxs-lookup"><span data-stu-id="6e0d9-178">Hebrew</span></span>                        | <span data-ttu-id="6e0d9-179">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-179">Segoe UI</span></span>              |
| <span data-ttu-id="6e0d9-180">舊的斜體</span><span class="sxs-lookup"><span data-stu-id="6e0d9-180">Old Italic</span></span>                    | <span data-ttu-id="6e0d9-181">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="6e0d9-181">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="6e0d9-182">爪哇文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-182">Javanese</span></span>                      | <span data-ttu-id="6e0d9-183">爪哇文文字</span><span class="sxs-lookup"><span data-stu-id="6e0d9-183">Javanese Text</span></span>         |
| <span data-ttu-id="6e0d9-184">日文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-184">Japanese</span></span>                      | <span data-ttu-id="6e0d9-185">Meiryo UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-185">Meiryo UI</span></span>             |
| <span data-ttu-id="6e0d9-186">坎那達文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-186">Kannada</span></span>                       | <span data-ttu-id="6e0d9-187">Mirmala UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-187">Mirmala UI</span></span>            |
| <span data-ttu-id="6e0d9-188">高棉文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-188">Khmer</span></span>                         | <span data-ttu-id="6e0d9-189">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-189">Leelawadee UI</span></span>         |
| <span data-ttu-id="6e0d9-190">韓文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-190">Korean</span></span>                        | <span data-ttu-id="6e0d9-191">Malgun Gothic</span><span class="sxs-lookup"><span data-stu-id="6e0d9-191">Malgun Gothic</span></span>         |
| <span data-ttu-id="6e0d9-192">寮文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-192">Lao</span></span>                           | <span data-ttu-id="6e0d9-193">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-193">Leelawadee UI</span></span>         |
| <span data-ttu-id="6e0d9-194">拉丁文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-194">Latin</span></span>                         | <span data-ttu-id="6e0d9-195">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-195">Segoe UI</span></span>              |
| <span data-ttu-id="6e0d9-196">馬來亞拉姆文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-196">Malayalam</span></span>                     | <span data-ttu-id="6e0d9-197">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-197">Nirmala UI</span></span>            |
| <span data-ttu-id="6e0d9-198">蒙古文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-198">Mongolian</span></span>                     | <span data-ttu-id="6e0d9-199">Mongolian Baiti</span><span class="sxs-lookup"><span data-stu-id="6e0d9-199">Mongolian Baiti</span></span>       |
| <span data-ttu-id="6e0d9-200">緬甸</span><span class="sxs-lookup"><span data-stu-id="6e0d9-200">Myanmar</span></span>                       | <span data-ttu-id="6e0d9-201">Myanmar Text</span><span class="sxs-lookup"><span data-stu-id="6e0d9-201">Myanmar Text</span></span>          |
| <span data-ttu-id="6e0d9-202">西非書面</span><span class="sxs-lookup"><span data-stu-id="6e0d9-202">N'Ko</span></span>                          | <span data-ttu-id="6e0d9-203">Ebrima</span><span class="sxs-lookup"><span data-stu-id="6e0d9-203">Ebrima</span></span>                |
| <span data-ttu-id="6e0d9-204">豎</span><span class="sxs-lookup"><span data-stu-id="6e0d9-204">Ogham</span></span>                         | <span data-ttu-id="6e0d9-205">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="6e0d9-205">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="6e0d9-206">桑塔爾文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-206">Ol Chiki</span></span>                      | <span data-ttu-id="6e0d9-207">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-207">Nirmala UI</span></span>            |
| <span data-ttu-id="6e0d9-208">舊的土耳其文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-208">Old Turkic</span></span>                    | <span data-ttu-id="6e0d9-209">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="6e0d9-209">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="6e0d9-210"> (以前的奧裡亞文) </span><span class="sxs-lookup"><span data-stu-id="6e0d9-210">Odia (formerly Oriya)</span></span>         | <span data-ttu-id="6e0d9-211">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-211">Nirmala UI</span></span>            |
| <span data-ttu-id="6e0d9-212">文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-212">Osmanya</span></span>                       | <span data-ttu-id="6e0d9-213">Ebrima</span><span class="sxs-lookup"><span data-stu-id="6e0d9-213">Ebrima</span></span>                |
| <span data-ttu-id="6e0d9-214">八位 pa</span><span class="sxs-lookup"><span data-stu-id="6e0d9-214">Phags-pa</span></span>                      | <span data-ttu-id="6e0d9-215">Microsoft PhagsPa</span><span class="sxs-lookup"><span data-stu-id="6e0d9-215">Microsoft PhagsPa</span></span>     |
| <span data-ttu-id="6e0d9-216">符文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-216">Runic</span></span>                         | <span data-ttu-id="6e0d9-217">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="6e0d9-217">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="6e0d9-218">Sora Sompeng</span><span class="sxs-lookup"><span data-stu-id="6e0d9-218">Sora Sompeng</span></span>                  | <span data-ttu-id="6e0d9-219">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-219">Nirmala UI</span></span>            |
| <span data-ttu-id="6e0d9-220">僧伽羅文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-220">Sinhala</span></span>                       | <span data-ttu-id="6e0d9-221">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-221">Nirmala UI</span></span>            |
| <span data-ttu-id="6e0d9-222">敘利亞文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-222">Syriac</span></span>                        | <span data-ttu-id="6e0d9-223">Estrangelo Edessa</span><span class="sxs-lookup"><span data-stu-id="6e0d9-223">Estrangelo Edessa</span></span>     |
| <span data-ttu-id="6e0d9-224">泰 Le</span><span class="sxs-lookup"><span data-stu-id="6e0d9-224">Tai Le</span></span>                        | <span data-ttu-id="6e0d9-225">Microsoft Tai Le</span><span class="sxs-lookup"><span data-stu-id="6e0d9-225">Microsoft Tai Le</span></span>      |
| <span data-ttu-id="6e0d9-226">新傣文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-226">New Tai Lue</span></span>                   | <span data-ttu-id="6e0d9-227">Microsoft New Tai Lue</span><span class="sxs-lookup"><span data-stu-id="6e0d9-227">Microsoft New Tai Lue</span></span> |
| <span data-ttu-id="6e0d9-228">坦米爾文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-228">Tamil</span></span>                         | <span data-ttu-id="6e0d9-229">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-229">Nirmala UI</span></span>            |
| <span data-ttu-id="6e0d9-230">泰盧固文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-230">Telugu</span></span>                        | <span data-ttu-id="6e0d9-231">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-231">Nirmala UI</span></span>            |
| <span data-ttu-id="6e0d9-232">納</span><span class="sxs-lookup"><span data-stu-id="6e0d9-232">Tifinagh</span></span>                      | <span data-ttu-id="6e0d9-233">Ebrima</span><span class="sxs-lookup"><span data-stu-id="6e0d9-233">Ebrima</span></span>                |
| <span data-ttu-id="6e0d9-234">塔安那文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-234">Thaana</span></span>                        | <span data-ttu-id="6e0d9-235">MV Boli</span><span class="sxs-lookup"><span data-stu-id="6e0d9-235">MV Boli</span></span>               |
| <span data-ttu-id="6e0d9-236">泰文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-236">Thai</span></span>                          | <span data-ttu-id="6e0d9-237">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-237">Leelawadee UI</span></span>         |
| <span data-ttu-id="6e0d9-238">西藏文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-238">Tibetan</span></span>                       | <span data-ttu-id="6e0d9-239">Microsoft Himalaya</span><span class="sxs-lookup"><span data-stu-id="6e0d9-239">Microsoft Himalaya</span></span>    |
| <span data-ttu-id="6e0d9-240">范文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-240">Vai</span></span>                           | <span data-ttu-id="6e0d9-241">Ebrima</span><span class="sxs-lookup"><span data-stu-id="6e0d9-241">Ebrima</span></span>                |
| <span data-ttu-id="6e0d9-242">爨文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-242">Yi</span></span>                            | <span data-ttu-id="6e0d9-243">Microsoft Yi Baiti</span><span class="sxs-lookup"><span data-stu-id="6e0d9-243">Microsoft Yi Baiti</span></span>    |



 

<span data-ttu-id="6e0d9-244">以下是舊版 UI 字型的清單，這些字型也會受到鎖定值的影響：</span><span class="sxs-lookup"><span data-stu-id="6e0d9-244">Here's a list of the legacy UI fonts which are also affected by locked values:</span></span>

| <span data-ttu-id="6e0d9-245"> (舊版) 的腳本名稱</span><span class="sxs-lookup"><span data-stu-id="6e0d9-245">Script name (legacy)</span></span>          | <span data-ttu-id="6e0d9-246">舊版) 的 UI 字型 (</span><span class="sxs-lookup"><span data-stu-id="6e0d9-246">UI font (legacy)</span></span>               |
|-------------------------------|--------------------------------|
| <span data-ttu-id="6e0d9-247">孟加拉國文 (先前為孟加拉國文) </span><span class="sxs-lookup"><span data-stu-id="6e0d9-247">Bangla (formerly Bengali)</span></span>     | <span data-ttu-id="6e0d9-248">Vrinda</span><span class="sxs-lookup"><span data-stu-id="6e0d9-248">Vrinda</span></span>                         |
| <span data-ttu-id="6e0d9-249">加拿大土著音節</span><span class="sxs-lookup"><span data-stu-id="6e0d9-249">Canadian Aboriginal Syllabics</span></span> | <span data-ttu-id="6e0d9-250">Euphemia</span><span class="sxs-lookup"><span data-stu-id="6e0d9-250">Euphemia</span></span>                       |
| <span data-ttu-id="6e0d9-251">卻洛奇文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-251">Cherokee</span></span>                      | <span data-ttu-id="6e0d9-252">Plantagenet</span><span class="sxs-lookup"><span data-stu-id="6e0d9-252">Plantagenet</span></span>                    |
| <span data-ttu-id="6e0d9-253">簡體中文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-253">Chinese (Simplified)</span></span>          | <span data-ttu-id="6e0d9-254">Microsoft YaHei 和 SimSun</span><span class="sxs-lookup"><span data-stu-id="6e0d9-254">Microsoft YaHei and SimSun</span></span>     |
| <span data-ttu-id="6e0d9-255">繁體中文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-255">Chinese (Traditional)</span></span>         | <span data-ttu-id="6e0d9-256">MingLiU 和 Microsoft JhengHei</span><span class="sxs-lookup"><span data-stu-id="6e0d9-256">MingLiU and Microsoft JhengHei</span></span> |
| <span data-ttu-id="6e0d9-257">梵文字母</span><span class="sxs-lookup"><span data-stu-id="6e0d9-257">Devanagari</span></span>                    | <span data-ttu-id="6e0d9-258">莽</span><span class="sxs-lookup"><span data-stu-id="6e0d9-258">Mangal</span></span>                         |
| <span data-ttu-id="6e0d9-259">歐洲語言</span><span class="sxs-lookup"><span data-stu-id="6e0d9-259">European languages</span></span>            | <span data-ttu-id="6e0d9-260">Tahoma</span><span class="sxs-lookup"><span data-stu-id="6e0d9-260">Tahoma</span></span>                         |
| <span data-ttu-id="6e0d9-261">古吉拉特文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-261">Gujarati</span></span>                      | <span data-ttu-id="6e0d9-262">Shruti</span><span class="sxs-lookup"><span data-stu-id="6e0d9-262">Shruti</span></span>                         |
| <span data-ttu-id="6e0d9-263">古木基文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-263">Gurmukhi</span></span>                      | <span data-ttu-id="6e0d9-264">Raavi</span><span class="sxs-lookup"><span data-stu-id="6e0d9-264">Raavi</span></span>                          |
| <span data-ttu-id="6e0d9-265">日文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-265">Japanese</span></span>                      | <span data-ttu-id="6e0d9-266">Meiryo 和 MS Mt UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-266">Meiryo and MS Gothic UI</span></span>        |
| <span data-ttu-id="6e0d9-267">坎那達文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-267">Kannada</span></span>                       | <span data-ttu-id="6e0d9-268">Tunga</span><span class="sxs-lookup"><span data-stu-id="6e0d9-268">Tunga</span></span>                          |
| <span data-ttu-id="6e0d9-269">高棉文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-269">Khmer</span></span>                         | <span data-ttu-id="6e0d9-270">高棉文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-270">Khmer</span></span>                          |
| <span data-ttu-id="6e0d9-271">韓文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-271">Korean</span></span>                        | <span data-ttu-id="6e0d9-272">Gulim</span><span class="sxs-lookup"><span data-stu-id="6e0d9-272">Gulim</span></span>                          |
| <span data-ttu-id="6e0d9-273">寮文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-273">Lao</span></span>                           | <span data-ttu-id="6e0d9-274">老撾文 UI</span><span class="sxs-lookup"><span data-stu-id="6e0d9-274">Lao UI</span></span>                         |
| <span data-ttu-id="6e0d9-275">馬來亞拉姆文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-275">Malayalam</span></span>                     | <span data-ttu-id="6e0d9-276">Kartika</span><span class="sxs-lookup"><span data-stu-id="6e0d9-276">Kartika</span></span>                        |
| <span data-ttu-id="6e0d9-277">中東語言</span><span class="sxs-lookup"><span data-stu-id="6e0d9-277">Middle Eastern languages</span></span>      | <span data-ttu-id="6e0d9-278">Tahoma</span><span class="sxs-lookup"><span data-stu-id="6e0d9-278">Tahoma</span></span>                         |
| <span data-ttu-id="6e0d9-279"> (以前的奧裡亞文) </span><span class="sxs-lookup"><span data-stu-id="6e0d9-279">Odia (formerly Oriya)</span></span>         | <span data-ttu-id="6e0d9-280">Kalinga</span><span class="sxs-lookup"><span data-stu-id="6e0d9-280">Kalinga</span></span>                        |
| <span data-ttu-id="6e0d9-281">Sinhalese</span><span class="sxs-lookup"><span data-stu-id="6e0d9-281">Sinhalese</span></span>                     | <span data-ttu-id="6e0d9-282">Iskoola Pota</span><span class="sxs-lookup"><span data-stu-id="6e0d9-282">Iskoola Pota</span></span>                   |
| <span data-ttu-id="6e0d9-283">坦米爾文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-283">Tamil</span></span>                         | <span data-ttu-id="6e0d9-284">Latha 和 Vijaya</span><span class="sxs-lookup"><span data-stu-id="6e0d9-284">Latha and Vijaya</span></span>               |
| <span data-ttu-id="6e0d9-285">泰盧固文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-285">Telugu</span></span>                        | <span data-ttu-id="6e0d9-286">Gautami</span><span class="sxs-lookup"><span data-stu-id="6e0d9-286">Gautami</span></span>                        |
| <span data-ttu-id="6e0d9-287">泰文</span><span class="sxs-lookup"><span data-stu-id="6e0d9-287">Thai</span></span>                          | <span data-ttu-id="6e0d9-288">Leelawadee 和 Tahoma</span><span class="sxs-lookup"><span data-stu-id="6e0d9-288">Leelawadee and Tahoma</span></span>          |



 

<span data-ttu-id="6e0d9-289">在 Microsoft 應用程式中會使用這些字型作為預設值，而且也會受到鎖定值的影響：</span><span class="sxs-lookup"><span data-stu-id="6e0d9-289">These fonts are used as defaults in Microsoft apps and are also affected by locked values:</span></span>

-   <span data-ttu-id="6e0d9-290">Arial</span><span class="sxs-lookup"><span data-stu-id="6e0d9-290">Arial</span></span>
-   <span data-ttu-id="6e0d9-291">Calibri</span><span class="sxs-lookup"><span data-stu-id="6e0d9-291">Calibri</span></span>
-   <span data-ttu-id="6e0d9-292">Cambria</span><span class="sxs-lookup"><span data-stu-id="6e0d9-292">Cambria</span></span>
-   <span data-ttu-id="6e0d9-293">Consolas</span><span class="sxs-lookup"><span data-stu-id="6e0d9-293">Consolas</span></span>
-   <span data-ttu-id="6e0d9-294">Courier New</span><span class="sxs-lookup"><span data-stu-id="6e0d9-294">Courier New</span></span>
-   <span data-ttu-id="6e0d9-295">MS Mincho</span><span class="sxs-lookup"><span data-stu-id="6e0d9-295">MS Mincho</span></span>
-   <span data-ttu-id="6e0d9-296">Times New Roman</span><span class="sxs-lookup"><span data-stu-id="6e0d9-296">Times New Roman</span></span>
-   <span data-ttu-id="6e0d9-297">Verdana</span><span class="sxs-lookup"><span data-stu-id="6e0d9-297">Verdana</span></span>

### <a name="dynamic-font-metrics"></a><span data-ttu-id="6e0d9-298">動態字型計量</span><span class="sxs-lookup"><span data-stu-id="6e0d9-298">Dynamic font metrics</span></span>

<span data-ttu-id="6e0d9-299">除了上面所列的鎖定計量以外，也會正確地報告字型值。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-299">Other than the locked metrics listed above, font values are accurately reported.</span></span> <span data-ttu-id="6e0d9-300">如果在新版本的 Windows 中變更字型，則新的和舊的字型值會不同。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-300">If a font is changed in a new version of Windows, dynamic font values will differ between the new and old.</span></span> <span data-ttu-id="6e0d9-301">例如，當字型加入字型時，字型標頭中的值可能會變更。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-301">For example, when a glyph is added to a font, values in the font’s header may change.</span></span> <span data-ttu-id="6e0d9-302">如果這些值 (（包括 xMin、xMax、yMin 和 yMax），並報告字型) 中圖像的最小和最大周框方塊已鎖定，且未回報 true 值，則可能會產生裁剪。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-302">Clipping could result if these values (which include xMin, xMax, yMin, and yMax, and report the minimum and maximum bounding box for glyphs in the font) were locked and didn't report true values.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e0d9-303">如果您在應用程式中使用動態字型值 (與 [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)) 中的值相同，則在未來的 Windows 版本中修改字型時，這些值將會變更。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-303">If you use dynamic font values in your app (like those in [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)), these values will change if fonts are modified in future versions of Windows.</span></span> <span data-ttu-id="6e0d9-304">請勿在文字必須保持靜態的情況下使用這些實際值。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-304">Don't use these actual values in situations where text must stay static.</span></span>

 

## <a name="guidelines-for-using-font-metrics"></a><span data-ttu-id="6e0d9-305">使用字型計量的指導方針</span><span class="sxs-lookup"><span data-stu-id="6e0d9-305">Guidelines for using font metrics</span></span>

-   <span data-ttu-id="6e0d9-306">計算畫面計量和字型計量 (例如，應用程式啟動時的平均寬度) ，並使用這些值來配置您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-306">Compute screen metrics and font metrics (e.g., average width) when an app is launched, and use these values to lay out your app.</span></span> <span data-ttu-id="6e0d9-307">這會提供一致的精確轉譯，而您的版面配置會回應字型中的變更或容納字型的回復。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-307">This will provide consistently accurate rendering, and your layout will respond to changes in fonts or accommodate font fallback.</span></span> <span data-ttu-id="6e0d9-308">如需字型回復與字型連結的總覽，請參閱「 [全球化逐步解說：字型」](https://msdn.microsoft.com/goglobal/bb688134.aspx)。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-308">For an overview of font fallback and font linking, see [Globalization Step by Step: Fonts](https://msdn.microsoft.com/goglobal/bb688134.aspx).</span></span> <span data-ttu-id="6e0d9-309">請參閱 [使用字型](/windows/desktop/Intl/using-font-fallback) 回復來取得 Uniscribe 特定的資訊。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-309">See [Using Font Fallback](/windows/desktop/Intl/using-font-fallback) for Uniscribe-specific info.</span></span>
    -   <span data-ttu-id="6e0d9-310">若要計算基底度量，請針對您想要的語言/腳本轉譯代表性文字。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-310">To compute a base metric, render representative text for your intended language/script.</span></span>
    -   <span data-ttu-id="6e0d9-311">如果控制項只包含一行未包裝的文字，請將它們配置出來，以符合未修剪文字的全形。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-311">For controls that just contain a single line of unwrapped text, lay them out to fit the full width of the untrimmed text.</span></span>
    -   <span data-ttu-id="6e0d9-312">針對具有多行的控制項，取得總長度（除以字元長度），而且您可以使用純色寬度。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-312">For controls with multiple lines, get the total length, divide by the character length, and you’ve got a solid width to work with.</span></span> <span data-ttu-id="6e0d9-313">請注意，對於讀取器的單一「字元」可能是多個程式碼點的複雜字集而言，這會比較棘手。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-313">Note that this is trickier for complex scripts where a single ‘character’ to the reader may be multiple code points.</span></span>
-   <span data-ttu-id="6e0d9-314">使用 [OS/2 資料表](https://www.microsoft.com/typography/otspec/os2.htm)) 的 STypoAscender、STypoDescender 和 unitsPerEm (來計算垂直間距。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-314">Use sTypoAscender, sTypoDescender, and unitsPerEm (from the [OS/2 table](https://www.microsoft.com/typography/otspec/os2.htm)) to calculate vertical spacing.</span></span> <span data-ttu-id="6e0d9-315">sTypoAscender 是用來判斷從文字框架頂端到第一個基準的最佳位移，而 sTypoDescender 則會決定從文字框架底部到最後一個基準的最佳位移。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-315">sTypoAscender is used to determine the optimum offset from the top of a text frame to the first baseline and sTypoDescender determines the optimum offset from the bottom of a text frame to the last baseline.</span></span>
-   <span data-ttu-id="6e0d9-316">如果您使用的是 DirectWrite，請使用 [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)建立版面配置。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-316">If you’re using DirectWrite, create a layout using [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="6e0d9-317">**IDWriteTextLayout** 提供  +  自然配置中的 ascender **下行**  +  **lineGap** 。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-317">**IDWriteTextLayout** provides **ascender** + **descender** + **lineGap** in natural layout.</span></span> <span data-ttu-id="6e0d9-318">您可以使用 [**DWRITE \_ 字型 \_ 計量**](/windows/desktop/api/dwrite/ns-dwrite-dwrite_font_metrics)來存取這些特定的值。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-318">You can access these specific values with [**DWRITE\_FONT\_METRICS**](/windows/desktop/api/dwrite/ns-dwrite-dwrite_font_metrics).</span></span> <span data-ttu-id="6e0d9-319">如需此介面的詳細資訊，請參閱 [文字格式設定和](/windows/desktop/DirectWrite/text-formatting-and-layout)配置。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-319">For info on this interface, see [Text Formatting and Layout](/windows/desktop/DirectWrite/text-formatting-and-layout).</span></span>
-   <span data-ttu-id="6e0d9-320">如果您使用的是 GDI，則會在螢幕上呈現，然後檢查配置 (例如，每行的行長度或字元) ，然後重新計算實際轉譯中使用的最終版面配置參數。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-320">If you’re using GDI, render off screen, then inspect the layout (for example, the line length or characters per line) and recalculate the final layout parameters used in actual rendering.</span></span>
-   <span data-ttu-id="6e0d9-321">請勿根據特定字型版本的特定值，以靜態方式建立版面配置。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-321">Don’t build layouts statically based on particular values for particular versions of fonts.</span></span> <span data-ttu-id="6e0d9-322">實際值可能會隨著版本而變更。</span><span class="sxs-lookup"><span data-stu-id="6e0d9-322">Actual values may change from release to release.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e0d9-323">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e0d9-323">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6e0d9-324">**參考**</span><span class="sxs-lookup"><span data-stu-id="6e0d9-324">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6e0d9-325">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="6e0d9-325">**IDWriteTextLayout**</span></span>](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="6e0d9-326">**DWRITE \_ 字型 \_ 計量**</span><span class="sxs-lookup"><span data-stu-id="6e0d9-326">**DWRITE\_FONT\_METRICS**</span></span>](/windows/desktop/api/dwrite/ns-dwrite-dwrite_font_metrics)
</dt> <dt>

[<span data-ttu-id="6e0d9-327">**TEXTMETRIC**</span><span class="sxs-lookup"><span data-stu-id="6e0d9-327">**TEXTMETRIC**</span></span>](/windows/win32/api/wingdi/ns-wingdi-textmetrica)
</dt> <dt>

[<span data-ttu-id="6e0d9-328">unitsPerEm</span><span class="sxs-lookup"><span data-stu-id="6e0d9-328">unitsPerEm</span></span>](https://www.microsoft.com/typography/otspec/head.htm)
</dt> <dt>

[<span data-ttu-id="6e0d9-329">OS/2 資料表</span><span class="sxs-lookup"><span data-stu-id="6e0d9-329">OS/2 table</span></span>](https://www.microsoft.com/typography/otspec/os2.htm)
</dt> <dt>

[<span data-ttu-id="6e0d9-330">垂直裝置計量表 (VDMX) </span><span class="sxs-lookup"><span data-stu-id="6e0d9-330">Vertical Device metrics table (VDMX)</span></span>](https://www.microsoft.com/typography/otspec/vdmx.htm)
</dt> <dt>

[<span data-ttu-id="6e0d9-331">Microsoft 印刷樣式：依產品或家族的字型</span><span class="sxs-lookup"><span data-stu-id="6e0d9-331">Microsoft typography: fonts by product or family</span></span>](https://www.microsoft.com/typography/fonts/default.aspx)
</dt> <dt>

<span data-ttu-id="6e0d9-332">**概念**</span><span class="sxs-lookup"><span data-stu-id="6e0d9-332">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6e0d9-333">文字度量 (DirectWrite) </span><span class="sxs-lookup"><span data-stu-id="6e0d9-333">Text Metrics (DirectWrite)</span></span>](/windows/desktop/DirectWrite/text-metrics)
</dt> <dt>

[<span data-ttu-id="6e0d9-334"> (GDI) 的字型和文字 </span><span class="sxs-lookup"><span data-stu-id="6e0d9-334">Fonts and Text (GDI)</span></span>](/windows/desktop/gdi/fonts-and-text)
</dt> <dt>

[<span data-ttu-id="6e0d9-335">Microsoft Typography</span><span class="sxs-lookup"><span data-stu-id="6e0d9-335">Microsoft Typography</span></span>](https://www.microsoft.com/typography/default.mspx)
</dt> </dl>

 

 