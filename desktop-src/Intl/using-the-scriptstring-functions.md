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
# <a name="using-the-scriptstring-functions"></a>使用 ScriptString 函數

如果應用程式處理未格式化的文字，Uniscribe 會 **提供 \* ScriptString** 函數。 這些函式類似于 [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)、 [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)和 [**GetTextExtent**](/cpp/mfc/reference/cdc-class#gettextextent)，但它們提供完整的複雜字集支援，包括插入號放置。 這些函式類似于其他 Uniscribe 函式，但會針對純文字處理的較簡單需求量身打造。

下表詳細說明 **ScriptString \*** 函數以及其他 Uniscribe 函數中的任何對應項。



<table>
<thead>
<tr class="header">
<th>函式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>ScriptStringAnalyse</strong></a></td>
<td>分析純文字。 此函式對應至下列函式：<br/> <dl><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>ScriptItemize</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>ScriptShape</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>ScriptPlace</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>ScriptBreak</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>ScriptJustify</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>ScriptLayout</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>ScriptStringCPtoX</strong></a></td>
<td>抓取字元位置的 x 座標。 此函式對應于 <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>ScriptCPtoX</strong></a>。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>ScriptStringFree</strong></a></td>
<td>釋出 <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> 結構。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>ScriptStringGetLogicalWidths</strong></a></td>
<td>將視覺效果寬度轉換成邏輯寬度。 此函式對應于 <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>ScriptGetLogicalWidths</strong></a>。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>ScriptStringGetOrder</strong></a></td>
<td>以類似的方式將字元圖像位置對應至 <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>，僅供舊版使用。 此函式不適用於每個程式碼點產生一個以上圖像的腳本。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>ScriptStringOut</strong></a></td>
<td>顯示純文字。 此函式對應于 <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>ScriptTextOut</strong></a>。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></td>
<td>傳回裁剪的純文字字串長度的指標。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></td>
<td>傳回已分析之純文字字串的邏輯屬性緩衝區指標。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></td>
<td>傳回已分析之純文字字串的大小 (寬度和高度) 的指標。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>ScriptStringValidate</strong></a></td>
<td>在指定的腳本中識別不正確程式碼點序列。 這個函式與 <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a>不同，它會識別字型中不存在的程式碼點。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>ScriptStringXtoCP</strong></a></td>
<td>將 x 座標轉換成字元位置。 此函式對應于 <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>ScriptXtoCP</strong></a>。</td>
</tr>
</tbody>
</table>

若只要顯示純文字而不進行任何修改，應用程式應該呼叫 [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)、 [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)，然後 [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree)。 其他函式是用來在顯示前修改純文字。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
