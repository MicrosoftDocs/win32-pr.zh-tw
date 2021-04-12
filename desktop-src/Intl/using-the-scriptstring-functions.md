---
description: 如果應用程式處理未格式化的文字，Uniscribe 會提供 ScriptString \* 函數。
ms.assetid: bfbba5df-ce06-4012-a7b1-55d8ea580942
title: 使用 ScriptString 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93a2df5e7515bd605ad48cc7a246941e9b6f08f2
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104024286"
---
# <a name="using-the-scriptstring-functions"></a><span data-ttu-id="a7ec6-103">使用 ScriptString 函數</span><span class="sxs-lookup"><span data-stu-id="a7ec6-103">Using the ScriptString Functions</span></span>

<span data-ttu-id="a7ec6-104">如果應用程式處理未格式化的文字，Uniscribe 會 **提供 \* ScriptString** 函數。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-104">For an application dealing with unformatted text, Uniscribe provides the **ScriptString\*** functions.</span></span> <span data-ttu-id="a7ec6-105">這些函式類似于 [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)、 [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)和 [**GetTextExtent**](/cpp/mfc/reference/cdc-class#gettextextent)，但它們提供完整的複雜字集支援，包括插入號放置。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-105">These functions are similar to [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext), and [**GetTextExtent**](/cpp/mfc/reference/cdc-class#gettextextent), but they provide full complex script support, including caret placement.</span></span> <span data-ttu-id="a7ec6-106">這些函式類似于其他 Uniscribe 函式，但會針對純文字處理的較簡單需求量身打造。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-106">These functions are similar to the other Uniscribe functions, but are tailored to the simpler requirements of plain text processing.</span></span>

<span data-ttu-id="a7ec6-107">下表詳細說明 **ScriptString \*** 函數以及其他 Uniscribe 函數中的任何對應項。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-107">The following table details the **ScriptString\*** functions and any counterparts in the other Uniscribe functions.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a7ec6-108">函式</span><span class="sxs-lookup"><span data-stu-id="a7ec6-108">Function</span></span></th>
<th><span data-ttu-id="a7ec6-109">描述</span><span class="sxs-lookup"><span data-stu-id="a7ec6-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7ec6-110"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>ScriptStringAnalyse</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-110"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>ScriptStringAnalyse</strong></a></span></span></td>
<td><span data-ttu-id="a7ec6-111">分析純文字。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-111">Analyzes plain text.</span></span> <span data-ttu-id="a7ec6-112">此函式對應至下列函式：</span><span class="sxs-lookup"><span data-stu-id="a7ec6-112">This function corresponds to the following functions:</span></span><br/> <dl><span data-ttu-id="a7ec6-113"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>ScriptItemize</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-113"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>ScriptItemize</strong></a></span></span><br /><span data-ttu-id="a7ec6-114">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>ScriptShape</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-114">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>ScriptShape</strong></a></span></span><br /><span data-ttu-id="a7ec6-115">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>ScriptPlace</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-115">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>ScriptPlace</strong></a></span></span><br /><span data-ttu-id="a7ec6-116">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>ScriptBreak</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-116">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>ScriptBreak</strong></a></span></span><br /><span data-ttu-id="a7ec6-117">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-117">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a></span></span><br /><span data-ttu-id="a7ec6-118">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>ScriptJustify</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-118">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>ScriptJustify</strong></a></span></span><br /><span data-ttu-id="a7ec6-119">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>ScriptLayout</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-119">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>ScriptLayout</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7ec6-120"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>ScriptStringCPtoX</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-120"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>ScriptStringCPtoX</strong></a></span></span></td>
<td><span data-ttu-id="a7ec6-121">抓取字元位置的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-121">Retrieves the x coordinate for a character position.</span></span> <span data-ttu-id="a7ec6-122">此函式對應于 <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>ScriptCPtoX</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-122">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>ScriptCPtoX</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7ec6-123"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>ScriptStringFree</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-123"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>ScriptStringFree</strong></a></span></span></td>
<td><span data-ttu-id="a7ec6-124">釋出 <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> 結構。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-124">Frees a <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7ec6-125"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>ScriptStringGetLogicalWidths</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-125"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>ScriptStringGetLogicalWidths</strong></a></span></span></td>
<td><span data-ttu-id="a7ec6-126">將視覺效果寬度轉換成邏輯寬度。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-126">Converts visual widths to logical widths.</span></span> <span data-ttu-id="a7ec6-127">此函式對應于 <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>ScriptGetLogicalWidths</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-127">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>ScriptGetLogicalWidths</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7ec6-128"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>ScriptStringGetOrder</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-128"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>ScriptStringGetOrder</strong></a></span></span></td>
<td><span data-ttu-id="a7ec6-129">以類似的方式將字元圖像位置對應至 <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>，僅供舊版使用。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-129">Maps character glyph positions in a similar way to <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>, for legacy use only.</span></span> <span data-ttu-id="a7ec6-130">此函式不適用於每個程式碼點產生一個以上圖像的腳本。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-130">This function does not work well with scripts that generate more than one glyph per code point.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7ec6-131"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>ScriptStringOut</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-131"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>ScriptStringOut</strong></a></span></span></td>
<td><span data-ttu-id="a7ec6-132">顯示純文字。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-132">Displays plain text.</span></span> <span data-ttu-id="a7ec6-133">此函式對應于 <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>ScriptTextOut</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-133">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>ScriptTextOut</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7ec6-134"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-134"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></span></span></td>
<td><span data-ttu-id="a7ec6-135">傳回裁剪的純文字字串長度的指標。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-135">Returns a pointer to the length of a clipped plain text string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7ec6-136"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-136"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></span></span></td>
<td><span data-ttu-id="a7ec6-137">傳回已分析之純文字字串的邏輯屬性緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-137">Returns a pointer to the logical attributes buffer for an analyzed plain text string.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7ec6-138"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-138"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></span></span></td>
<td><span data-ttu-id="a7ec6-139">傳回已分析之純文字字串的大小 (寬度和高度) 的指標。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-139">Returns a pointer to the size (width and height) for an analyzed plain text string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7ec6-140"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>ScriptStringValidate</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-140"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>ScriptStringValidate</strong></a></span></span></td>
<td><span data-ttu-id="a7ec6-141">在指定的腳本中識別不正確程式碼點序列。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-141">Identifies code point sequences not valid in the given script.</span></span> <span data-ttu-id="a7ec6-142">這個函式與 <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a>不同，它會識別字型中不存在的程式碼點。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-142">This function is different from <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a>, which identifies code points not present in a font.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7ec6-143"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>ScriptStringXtoCP</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7ec6-143"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>ScriptStringXtoCP</strong></a></span></span></td>
<td><span data-ttu-id="a7ec6-144">將 x 座標轉換成字元位置。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-144">Converts an x coordinate to a character position.</span></span> <span data-ttu-id="a7ec6-145">此函式對應于 <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>ScriptXtoCP</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-145">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>ScriptXtoCP</strong></a>.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a7ec6-146">若只要顯示純文字而不進行任何修改，應用程式應該呼叫 [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)、 [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)，然後 [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree)。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-146">To only display plain text without any modifications, an application should call [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout), and then [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree).</span></span> <span data-ttu-id="a7ec6-147">其他函式是用來在顯示前修改純文字。</span><span class="sxs-lookup"><span data-stu-id="a7ec6-147">The other functions are used to modify the plain text before display.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7ec6-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="a7ec6-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7ec6-149">使用 Uniscribe</span><span class="sxs-lookup"><span data-stu-id="a7ec6-149">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 
