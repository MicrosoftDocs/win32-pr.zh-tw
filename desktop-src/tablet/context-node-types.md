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
# <a name="context-node-types"></a><span data-ttu-id="7ab23-103">內容節點類型</span><span class="sxs-lookup"><span data-stu-id="7ab23-103">Context Node Types</span></span>

<span data-ttu-id="7ab23-104">這些常數會定義值，這些值會指定 [**ICoNtextNode**](icontextnode.md) 物件的類型。</span><span class="sxs-lookup"><span data-stu-id="7ab23-104">These constants define values that specify the type of [**IContextNode**](icontextnode.md) objects.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="7ab23-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="7ab23-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="7ab23-106">Description</span><span class="sxs-lookup"><span data-stu-id="7ab23-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_ANALYSISHINT"></span><span id="guid_cnt_analysishint"></span><dl> <span data-ttu-id="7ab23-107"><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt> (ANALYSISHINT) </dt> </span><span class="sxs-lookup"><span data-stu-id="7ab23-107"><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt>(AnalysisHint)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7ab23-108">代表節點，其中包含 <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> 用來改善其分析之區域的其他內容資訊。</span><span class="sxs-lookup"><span data-stu-id="7ab23-108">Represents a node that contains additional context information for a region that the <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> uses to improve its analysis.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_CUSTOMRECOGNIZER"></span><span id="guid_cnt_customrecognizer"></span><dl> <span data-ttu-id="7ab23-109"><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt> (CUSTOMRECOGNIZER) </dt> </span><span class="sxs-lookup"><span data-stu-id="7ab23-109"><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt>(CustomRecognizer)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7ab23-110">表示用於單一識別作業的節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-110">Represents a node used for a single recognition operation.</span></span><br/> <span data-ttu-id="7ab23-111">獨立辨識作業會辨識自訂辨識器節點內的所有筆劃和節點，而且 <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>不會進行分析。</span><span class="sxs-lookup"><span data-stu-id="7ab23-111">All strokes and nodes that are within a custom recognizer node are recognized by an independent recognition operation and are not analyzed by the <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>.</span></span><br/> <span data-ttu-id="7ab23-112">自訂辨識器節點必須是筆跡分析器根節點的直接子系。</span><span class="sxs-lookup"><span data-stu-id="7ab23-112">A custom recognizer node must be the direct child of ink analyzer's root node.</span></span><br/> <span data-ttu-id="7ab23-113">自訂辨識器節點可包含下列類型的子項目：</span><span class="sxs-lookup"><span data-stu-id="7ab23-113">A custom recognizer node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="7ab23-114">任何數目的 UnclassifiedInk 節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-114">Any number of UnclassifiedInk nodes.</span></span></li>
<li><span data-ttu-id="7ab23-115">任何數目的物件節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-115">Any number of Object nodes.</span></span></li>
<li><span data-ttu-id="7ab23-116">任何數目的行節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-116">Any number of Line nodes.</span></span></li>
<li><span data-ttu-id="7ab23-117">任何數目的 InkWord 節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-117">Any number of InkWord nodes.</span></span></li>
<li><span data-ttu-id="7ab23-118">具有未知 Guid 值的任何節點數目。</span><span class="sxs-lookup"><span data-stu-id="7ab23-118">Any number of nodes with an unknown Guid value.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_IMAGE"></span><span id="guid_cnt_image"></span><dl> <span data-ttu-id="7ab23-119"><dt><strong>GUID_CNT_IMAGE</strong></dt> <dt> (映射) </dt> </span><span class="sxs-lookup"><span data-stu-id="7ab23-119"><dt><strong>GUID_CNT_IMAGE</strong></dt> <dt>(Image)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7ab23-120">表示二維區域的節點，其中任何非筆跡影像都可以存在於檔中。</span><span class="sxs-lookup"><span data-stu-id="7ab23-120">Represents a node for a two-dimensional region where any non-ink images can exist in the document.</span></span><br/> <span data-ttu-id="7ab23-121"><a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>不會產生影像節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-121">The <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> does not produce image nodes.</span></span> <span data-ttu-id="7ab23-122">使用 <a href="icontextnode-createsubnode.md"><strong>ICoNtextNode：： CreateSubNode</strong></a> 將影像節點新增至內容節點樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="7ab23-122">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode</strong></a> to add an image node to the context node tree.</span></span> <span data-ttu-id="7ab23-123">然後， <strong>IInkAnalyzer</strong> 會使用影像節點所定義的區域，來判斷是否有任何筆墨標注非筆墨影像。</span><span class="sxs-lookup"><span data-stu-id="7ab23-123">The <strong>IInkAnalyzer</strong> then uses the regions defined by the image node to determine if any ink annotates the non-ink image.</span></span><br/> <span data-ttu-id="7ab23-124">映射節點不能有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="7ab23-124">An image node cannot have any child elements.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKBULLET"></span><span id="guid_cnt_inkbullet"></span><dl> <span data-ttu-id="7ab23-125"><dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt> (INKBULLET) </dt> </span><span class="sxs-lookup"><span data-stu-id="7ab23-125"><dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt>(InkBullet)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7ab23-126">InkBullet CoNtextNodeType 代表以項目符號清單組成專案符號的筆劃集合。</span><span class="sxs-lookup"><span data-stu-id="7ab23-126">The InkBullet ContextNodeType represents a collection of strokes that make up a bullet in a bulleted list.</span></span><br/> <span data-ttu-id="7ab23-127">InkBullet 類型的 CoNtextNode 不能有任何子系。</span><span class="sxs-lookup"><span data-stu-id="7ab23-127">A ContextNode of type InkBullet cannot have any children.</span></span> <span data-ttu-id="7ab23-128">它只能是段落 CoNtextNode 的子系。</span><span class="sxs-lookup"><span data-stu-id="7ab23-128">It can only be a child of a Paragraph ContextNode.</span></span> <span data-ttu-id="7ab23-129">只有一個 InkBullet 可以出現在單一段落 CoNtextNode 中。</span><span class="sxs-lookup"><span data-stu-id="7ab23-129">Only one InkBullet can appear in a single Paragraph ContextNode.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_INKDRAWING"></span><span id="guid_cnt_inkdrawing"></span><dl> <span data-ttu-id="7ab23-130"><dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt> (INKDRAWING) </dt> </span><span class="sxs-lookup"><span data-stu-id="7ab23-130"><dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt>(InkDrawing)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7ab23-131">代表組成繪圖之筆劃集合的節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-131">Represents a node for a collection of strokes that constitutes a drawing.</span></span><br/> <span data-ttu-id="7ab23-132">繪圖是決定為圖形或抽象化草圖的筆觸。</span><span class="sxs-lookup"><span data-stu-id="7ab23-132">Drawings are strokes that are determined to be shapes or abstract sketches.</span></span> <span data-ttu-id="7ab23-133">它們通常是未分類為書寫筆劃的任何筆觸。</span><span class="sxs-lookup"><span data-stu-id="7ab23-133">They are generally any strokes that are not classified as writing strokes.</span></span><br/> <span data-ttu-id="7ab23-134">筆墨繪圖節點不能有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="7ab23-134">An ink drawing node cannot have any child elements.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKWORD"></span><span id="guid_cnt_inkword"></span><dl> <span data-ttu-id="7ab23-135"><dt><strong>GUID_CNT_INKWORD</strong></dt> <dt> (INKWORD) </dt> </span><span class="sxs-lookup"><span data-stu-id="7ab23-135"><dt><strong>GUID_CNT_INKWORD</strong></dt> <dt>(InkWord)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7ab23-136">表示筆劃集合的節點，這些筆觸組成邏輯群組以形成可辨識的字組。</span><span class="sxs-lookup"><span data-stu-id="7ab23-136">Represents a node for a collection of strokes that constitutes a logical grouping to form a recognizable word.</span></span><br/> <span data-ttu-id="7ab23-137">筆墨單位元組點不能包含任何子項目。</span><span class="sxs-lookup"><span data-stu-id="7ab23-137">An ink word node cannot contain any child elements.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_LINE"></span><span id="guid_cnt_line"></span><dl> <span data-ttu-id="7ab23-138"><dt><strong>GUID_CNT_LINE</strong></dt> <dt> (行) </dt> </span><span class="sxs-lookup"><span data-stu-id="7ab23-138"><dt><strong>GUID_CNT_LINE</strong></dt> <dt>(Line)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7ab23-139">表示文字行的節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-139">Represents a node for a line of words.</span></span><br/> <span data-ttu-id="7ab23-140">行節點可包含下列類型的子項目：</span><span class="sxs-lookup"><span data-stu-id="7ab23-140">A line node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="7ab23-141">任意數目的筆墨單位元組點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-141">Any number of ink word nodes.</span></span></li>
<li><span data-ttu-id="7ab23-142">任意數目的文字字組節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-142">Any number of text word nodes.</span></span></li>
<li><span data-ttu-id="7ab23-143">具有未知 <strong>GUID</strong> 值的任何節點數目。</span><span class="sxs-lookup"><span data-stu-id="7ab23-143">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_OBJECT"></span><span id="guid_cnt_object"></span><dl> <span data-ttu-id="7ab23-144"><dt><strong>GUID_CNT_OBJECT</strong></dt> <dt> (物件) </dt> </span><span class="sxs-lookup"><span data-stu-id="7ab23-144"><dt><strong>GUID_CNT_OBJECT</strong></dt> <dt>(Object)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7ab23-145">表示從 &quot; 物件自訂辨識器傳回之物件的節點 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="7ab23-145">Represents a node for an object that is returned from an &quot;object&quot; custom recognizer.</span></span><br/> <span data-ttu-id="7ab23-146">物件節點不能包含任何子項目。</span><span class="sxs-lookup"><span data-stu-id="7ab23-146">An object node cannot contain any child elements.</span></span><br/> <span data-ttu-id="7ab23-147">只有自訂辨識器節點可以包含物件節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-147">Only custom recognizer nodes can contain object nodes.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_PARAGRAPH"></span><span id="guid_cnt_paragraph"></span><dl> <span data-ttu-id="7ab23-148"><dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt> (段落) </dt> </span><span class="sxs-lookup"><span data-stu-id="7ab23-148"><dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt>(Paragraph)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7ab23-149">代表節點集合的節點，這些節點組成行的邏輯群組。</span><span class="sxs-lookup"><span data-stu-id="7ab23-149">Represents a node for a collection of nodes that constitutes a logical grouping of lines.</span></span><br/> <span data-ttu-id="7ab23-150">段落的確切定義取決於分析引擎。</span><span class="sxs-lookup"><span data-stu-id="7ab23-150">The exact definition of a paragraph is determined by the analyzing engines.</span></span> <span data-ttu-id="7ab23-151">一般而言，如果包含線條的方塊已調整大小，段落就會包含會一起重新排列的線條群組。</span><span class="sxs-lookup"><span data-stu-id="7ab23-151">In general, a paragraph contains groups of lines that would reflow together if the box that contains the lines were resized.</span></span><br/> <span data-ttu-id="7ab23-152">段落節點可包含下列類型的子項目：</span><span class="sxs-lookup"><span data-stu-id="7ab23-152">A paragraph node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="7ab23-153">任意數目的筆墨專案符號節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-153">Any number of ink bullet nodes.</span></span></li>
<li><span data-ttu-id="7ab23-154">任何數目的行節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-154">Any number of line nodes.</span></span></li>
<li><span data-ttu-id="7ab23-155">具有未知 <strong>GUID</strong> 值的任何節點數目。</span><span class="sxs-lookup"><span data-stu-id="7ab23-155">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_ROOT"></span><span id="guid_cnt_root"></span><dl> <span data-ttu-id="7ab23-156"><dt><strong>GUID_CNT_ROOT</strong></dt> <dt> (根) </dt> </span><span class="sxs-lookup"><span data-stu-id="7ab23-156"><dt><strong>GUID_CNT_ROOT</strong></dt> <dt>(Root)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7ab23-157">代表節點樹狀結構的最上層節點節點，這些節點會描述筆跡分析的結果。</span><span class="sxs-lookup"><span data-stu-id="7ab23-157">Represents a node for the top node of a tree of nodes that describe the results of ink analysis.</span></span><br/> <span data-ttu-id="7ab23-158">根節點通常是從 <a href="iinkanalyzer-getrootnode.md"><strong>IInkAnalyzer：： GetRootNode 方法</strong></a> 方法取得。</span><span class="sxs-lookup"><span data-stu-id="7ab23-158">Root nodes are generally obtained from the <a href="iinkanalyzer-getrootnode.md"><strong>IInkAnalyzer::GetRootNode Method</strong></a> method.</span></span><br/> <span data-ttu-id="7ab23-159">根節點可包含下列類型的子項目：</span><span class="sxs-lookup"><span data-stu-id="7ab23-159">A root node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="7ab23-160">任何數目的分析提示節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-160">Any number of analysis hint nodes.</span></span></li>
<li><span data-ttu-id="7ab23-161">任意數目的自訂辨識器節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-161">Any number of custom recognizer nodes.</span></span></li>
<li><span data-ttu-id="7ab23-162">任意數目的影像節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-162">Any number of image nodes.</span></span></li>
<li><span data-ttu-id="7ab23-163">任意數目的筆墨繪圖節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-163">Any number of ink drawing nodes.</span></span></li>
<li><span data-ttu-id="7ab23-164">任意數目的寫入區域節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-164">Any number of writing region nodes.</span></span></li>
<li><span data-ttu-id="7ab23-165">任意數目的未分類筆墨節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-165">Any number of unclassified ink nodes.</span></span></li>
<li><span data-ttu-id="7ab23-166">具有未知 <strong>GUID</strong> 值的任何節點數目。</span><span class="sxs-lookup"><span data-stu-id="7ab23-166">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_TEXTWORD"></span><span id="guid_cnt_textword"></span><dl> <span data-ttu-id="7ab23-167"><dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt> (TEXTWORD) </dt> </span><span class="sxs-lookup"><span data-stu-id="7ab23-167"><dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt>(TextWord)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7ab23-168">代表二維區域的節點，其中任何非筆墨文字都可以存在於檔中。</span><span class="sxs-lookup"><span data-stu-id="7ab23-168">Represents a node for the two-dimensional region where any non-ink text can exist in the document.</span></span><br/> <span data-ttu-id="7ab23-169"><a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>不會產生文字字組節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-169">The <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> does not produce text word nodes.</span></span> <span data-ttu-id="7ab23-170">使用 <a href="icontextnode-createsubnode.md"><strong>ICoNtextNode：： CreateSubNode</strong></a> 將文字文位元組點加入至內容節點樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="7ab23-170">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode</strong></a> to add a text word node to the context node tree.</span></span> <span data-ttu-id="7ab23-171">然後， <strong>IInkAnalyzer</strong> 會使用文字位元組點所定義的區域，來判斷是否有任何筆墨標注非筆墨文字。</span><span class="sxs-lookup"><span data-stu-id="7ab23-171">The <strong>IInkAnalyzer</strong> then uses the regions defined by the text word node to determine if any ink annotates the non-ink text.</span></span><br/> <span data-ttu-id="7ab23-172">未來的辨識器可能會使用文字位元組點所定義的區域，判斷是否有任何筆墨標注非筆墨字。</span><span class="sxs-lookup"><span data-stu-id="7ab23-172">Future recognizers may use the region defined by a text word node to determine if any ink annotates the non-ink word.</span></span><br/> <span data-ttu-id="7ab23-173">文字位元組點不能有任何子項目</span><span class="sxs-lookup"><span data-stu-id="7ab23-173">A text word node cannot have any child elements</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_UNCLASSIFIEDINKNODE"></span><span id="guid_cnt_unclassifiedinknode"></span><dl> <span data-ttu-id="7ab23-174"><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt> (UnclassifiedInk) </dt> </span><span class="sxs-lookup"><span data-stu-id="7ab23-174"><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt>(UnclassifiedInk)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="7ab23-175">代表尚未分類或辨識之任何筆劃的節點。</span><span class="sxs-lookup"><span data-stu-id="7ab23-175">Represents a node for any strokes that have not yet been classified or recognized.</span></span><br/> <span data-ttu-id="7ab23-176">未分類的筆墨節點不能有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="7ab23-176">An unclassified ink node cannot have any child elements.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="7ab23-177">備註</span><span class="sxs-lookup"><span data-stu-id="7ab23-177">Remarks</span></span>

<span data-ttu-id="7ab23-178">如需不同內容節點類型的詳細資訊，請參閱 [筆墨分析總覽](ink-analysis-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="7ab23-178">For more information about the different context node types, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ab23-179">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ab23-179">Requirements</span></span>



| <span data-ttu-id="7ab23-180">需求</span><span class="sxs-lookup"><span data-stu-id="7ab23-180">Requirement</span></span> | <span data-ttu-id="7ab23-181">值</span><span class="sxs-lookup"><span data-stu-id="7ab23-181">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab23-182">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ab23-182">Minimum supported client</span></span><br/> | <span data-ttu-id="7ab23-183">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ab23-183">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7ab23-184">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ab23-184">Minimum supported server</span></span><br/> | <span data-ttu-id="7ab23-185">都不支援</span><span class="sxs-lookup"><span data-stu-id="7ab23-185">None supported</span></span><br/>                                                           |
| <span data-ttu-id="7ab23-186">標頭</span><span class="sxs-lookup"><span data-stu-id="7ab23-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ab23-187"><dt>Iaguid。h</dt></span><span class="sxs-lookup"><span data-stu-id="7ab23-187"><dt>Iaguid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ab23-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ab23-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ab23-189">**ICoNtextNode::CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="7ab23-189">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="7ab23-190">**ICoNtextNode::CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="7ab23-190">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="7ab23-191">**ICoNtextNode：： GetType**</span><span class="sxs-lookup"><span data-stu-id="7ab23-191">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
</dt> <dt>

[<span data-ttu-id="7ab23-192">**IInkAnalyzer：： CreateAnalysisHint 方法**</span><span class="sxs-lookup"><span data-stu-id="7ab23-192">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="7ab23-193">**IInkAnalyzer：： CreateCustomRecognizer 方法**</span><span class="sxs-lookup"><span data-stu-id="7ab23-193">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="7ab23-194">**IInkAnalyzer：： FindNodesOfType 方法**</span><span class="sxs-lookup"><span data-stu-id="7ab23-194">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="7ab23-195">**IInkAnalyzer：： FindNodesOfTypeForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="7ab23-195">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="7ab23-196">**IInkAnalyzer：： FindNodesOfTypeInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="7ab23-196">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="7ab23-197">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="7ab23-197">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




