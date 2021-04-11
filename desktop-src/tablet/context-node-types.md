---
description: 這些常數會定義值，這些值會指定 ICoNtextNode 物件的類型。
ms.assetid: 333db79e-f503-4545-84fd-7c1a39a96728
title: '內容節點類型 (Iaguid .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNT_ANALYSISHINT
- GUID_CNT_CUSTOMRECOGNIZER
- GUID_CNT_IMAGE
- GUID_CNT_INKBULLET
- GUID_CNT_INKDRAWING
- GUID_CNT_INKWORD
- GUID_CNT_LINE
- GUID_CNT_OBJECT
- GUID_CNT_PARAGRAPH
- GUID_CNT_ROOT
- GUID_CNT_TEXTWORD
- GUID_CNT_UNCLASSIFIEDINKNODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 918b7cf818ebcedc98f45bff7c41ee66ad4d1592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111700"
---
# <a name="context-node-types"></a>內容節點類型

這些常數會定義值，這些值會指定 [**ICoNtextNode**](icontextnode.md) 物件的類型。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">常數/值</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_ANALYSISHINT"></span><span id="guid_cnt_analysishint"></span><dl> <dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt> (ANALYSISHINT) </dt> </dl></td>
<td style="text-align: left;">代表節點，其中包含 <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> 用來改善其分析之區域的其他內容資訊。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_CUSTOMRECOGNIZER"></span><span id="guid_cnt_customrecognizer"></span><dl> <dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt> (CUSTOMRECOGNIZER) </dt> </dl></td>
<td style="text-align: left;">表示用於單一識別作業的節點。<br/> 獨立辨識作業會辨識自訂辨識器節點內的所有筆劃和節點，而且 <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>不會進行分析。<br/> 自訂辨識器節點必須是筆跡分析器根節點的直接子系。<br/> 自訂辨識器節點可包含下列類型的子項目：<br/>
<ul>
<li>任何數目的 UnclassifiedInk 節點。</li>
<li>任何數目的物件節點。</li>
<li>任何數目的行節點。</li>
<li>任何數目的 InkWord 節點。</li>
<li>具有未知 Guid 值的任何節點數目。</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_IMAGE"></span><span id="guid_cnt_image"></span><dl> <dt><strong>GUID_CNT_IMAGE</strong></dt> <dt> (映射) </dt> </dl></td>
<td style="text-align: left;">表示二維區域的節點，其中任何非筆跡影像都可以存在於檔中。<br/> <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>不會產生影像節點。 使用 <a href="icontextnode-createsubnode.md"><strong>ICoNtextNode：： CreateSubNode</strong></a> 將影像節點新增至內容節點樹狀結構。 然後， <strong>IInkAnalyzer</strong> 會使用影像節點所定義的區域，來判斷是否有任何筆墨標注非筆墨影像。<br/> 映射節點不能有任何子項目。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKBULLET"></span><span id="guid_cnt_inkbullet"></span><dl> <dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt> (INKBULLET) </dt> </dl></td>
<td style="text-align: left;">InkBullet CoNtextNodeType 代表以項目符號清單組成專案符號的筆劃集合。<br/> InkBullet 類型的 CoNtextNode 不能有任何子系。 它只能是段落 CoNtextNode 的子系。 只有一個 InkBullet 可以出現在單一段落 CoNtextNode 中。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_INKDRAWING"></span><span id="guid_cnt_inkdrawing"></span><dl> <dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt> (INKDRAWING) </dt> </dl></td>
<td style="text-align: left;">代表組成繪圖之筆劃集合的節點。<br/> 繪圖是決定為圖形或抽象化草圖的筆觸。 它們通常是未分類為書寫筆劃的任何筆觸。<br/> 筆墨繪圖節點不能有任何子項目。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKWORD"></span><span id="guid_cnt_inkword"></span><dl> <dt><strong>GUID_CNT_INKWORD</strong></dt> <dt> (INKWORD) </dt> </dl></td>
<td style="text-align: left;">表示筆劃集合的節點，這些筆觸組成邏輯群組以形成可辨識的字組。<br/> 筆墨單位元組點不能包含任何子項目。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_LINE"></span><span id="guid_cnt_line"></span><dl> <dt><strong>GUID_CNT_LINE</strong></dt> <dt> (行) </dt> </dl></td>
<td style="text-align: left;">表示文字行的節點。<br/> 行節點可包含下列類型的子項目：<br/>
<ul>
<li>任意數目的筆墨單位元組點。</li>
<li>任意數目的文字字組節點。</li>
<li>具有未知 <strong>GUID</strong> 值的任何節點數目。</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_OBJECT"></span><span id="guid_cnt_object"></span><dl> <dt><strong>GUID_CNT_OBJECT</strong></dt> <dt> (物件) </dt> </dl></td>
<td style="text-align: left;">表示從 &quot; 物件自訂辨識器傳回之物件的節點 &quot; 。<br/> 物件節點不能包含任何子項目。<br/> 只有自訂辨識器節點可以包含物件節點。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_PARAGRAPH"></span><span id="guid_cnt_paragraph"></span><dl> <dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt> (段落) </dt> </dl></td>
<td style="text-align: left;">代表節點集合的節點，這些節點組成行的邏輯群組。<br/> 段落的確切定義取決於分析引擎。 一般而言，如果包含線條的方塊已調整大小，段落就會包含會一起重新排列的線條群組。<br/> 段落節點可包含下列類型的子項目：<br/>
<ul>
<li>任意數目的筆墨專案符號節點。</li>
<li>任何數目的行節點。</li>
<li>具有未知 <strong>GUID</strong> 值的任何節點數目。</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_ROOT"></span><span id="guid_cnt_root"></span><dl> <dt><strong>GUID_CNT_ROOT</strong></dt> <dt> (根) </dt> </dl></td>
<td style="text-align: left;">代表節點樹狀結構的最上層節點節點，這些節點會描述筆跡分析的結果。<br/> 根節點通常是從 <a href="iinkanalyzer-getrootnode.md"><strong>IInkAnalyzer：： GetRootNode 方法</strong></a> 方法取得。<br/> 根節點可包含下列類型的子項目：<br/>
<ul>
<li>任何數目的分析提示節點。</li>
<li>任意數目的自訂辨識器節點。</li>
<li>任意數目的影像節點。</li>
<li>任意數目的筆墨繪圖節點。</li>
<li>任意數目的寫入區域節點。</li>
<li>任意數目的未分類筆墨節點。</li>
<li>具有未知 <strong>GUID</strong> 值的任何節點數目。</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_TEXTWORD"></span><span id="guid_cnt_textword"></span><dl> <dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt> (TEXTWORD) </dt> </dl></td>
<td style="text-align: left;">代表二維區域的節點，其中任何非筆墨文字都可以存在於檔中。<br/> <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>不會產生文字字組節點。 使用 <a href="icontextnode-createsubnode.md"><strong>ICoNtextNode：： CreateSubNode</strong></a> 將文字文位元組點加入至內容節點樹狀結構。 然後， <strong>IInkAnalyzer</strong> 會使用文字位元組點所定義的區域，來判斷是否有任何筆墨標注非筆墨文字。<br/> 未來的辨識器可能會使用文字位元組點所定義的區域，判斷是否有任何筆墨標注非筆墨字。<br/> 文字位元組點不能有任何子項目<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_UNCLASSIFIEDINKNODE"></span><span id="guid_cnt_unclassifiedinknode"></span><dl> <dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt> (UnclassifiedInk) </dt> </dl></td>
<td style="text-align: left;">代表尚未分類或辨識之任何筆劃的節點。<br/> 未分類的筆墨節點不能有任何子項目。<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>備註

如需不同內容節點類型的詳細資訊，請參閱 [筆墨分析總覽](ink-analysis-overview.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Iaguid。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**ICoNtextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[**ICoNtextNode：： GetType**](icontextnode-gettype.md)
</dt> <dt>

[**IInkAnalyzer：： CreateAnalysisHint 方法**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer：： CreateCustomRecognizer 方法**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesOfType 方法**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesOfTypeForStrokes 方法**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**IInkAnalyzer：： FindNodesOfTypeInSubTree 方法**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




