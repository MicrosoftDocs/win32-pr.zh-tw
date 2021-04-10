---
description: 針對分析提示節點的屬性，定義 (Guid) 的全域唯一識別碼 (請參閱 ICoNtextNode：： GetType) 。
ms.assetid: 8300c792-a741-49de-a03b-f4840ea5d647
title: 'Analysis 提示屬性 (Iaguid .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AHP_ALLOWPARTIALDICTIONARYTERMS
- GUID_AHP_ANALYSISHINTNAME
- GUID_AHP_COERCETOFACTOID
- GUID_AHP_ENABLEDUNICODECHARACTERRANGES
- GUID_AHP_FACTOID
- GUID_AHP_GUIDE
- GUID_AHP_PREFIXTEXT
- GUID_AHP_SUFFIXTEXT
- GUID_AHP_TOPINKBREAKSONLY
- GUID_AHP_WORDLIST
- GUID_AHP_WORDMODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8a7a25cfa94bb7f2354418ded2b35e3137364901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936546"
---
# <a name="analysis-hint-properties"></a><span data-ttu-id="79701-103">分析提示屬性</span><span class="sxs-lookup"><span data-stu-id="79701-103">Analysis Hint Properties</span></span>

<span data-ttu-id="79701-104">針對分析提示節點的屬性，定義 (Guid) 的全域唯一識別碼 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 。</span><span class="sxs-lookup"><span data-stu-id="79701-104">Defines globally unique identifiers (GUIDs) for properties of an analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

<span data-ttu-id="79701-105">下表描述每個常數所參考的資訊。</span><span class="sxs-lookup"><span data-stu-id="79701-105">The following table describes information referenced by each constant.</span></span>



| <span data-ttu-id="79701-106">常數</span><span class="sxs-lookup"><span data-stu-id="79701-106">Constant</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="79701-107">描述</span><span class="sxs-lookup"><span data-stu-id="79701-107">Description</span></span>                                                                                                                                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AHP_ALLOWPARTIALDICTIONARYTERMS"></span><span id="guid_ahp_allowpartialdictionaryterms"></span><dl> <span data-ttu-id="79701-108"><dt>**GUID \_ AHP \_ ALLOWPARTIALDICTIONARYTERMS**</dt></span><span class="sxs-lookup"><span data-stu-id="79701-108"><dt>**GUID\_AHP\_ALLOWPARTIALDICTIONARYTERMS**</dt></span></span> </dl>       | <span data-ttu-id="79701-109">分析提示是否允許部分字典詞彙。</span><span class="sxs-lookup"><span data-stu-id="79701-109">Whether partial dictionary terms are allowed on an analysis hint.</span></span><br/>                                                                              |
| <span id="GUID_AHP_ANALYSISHINTNAME"></span><span id="guid_ahp_analysishintname"></span><dl> <span data-ttu-id="79701-110"><dt>**GUID \_ AHP \_ ANALYSISHINTNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="79701-110"><dt>**GUID\_AHP\_ANALYSISHINTNAME**</dt></span></span> </dl>                                        | <span data-ttu-id="79701-111">分析提示的名稱。</span><span class="sxs-lookup"><span data-stu-id="79701-111">The name of an analysis hint.</span></span><br/>                                                                                                                  |
| <span id="GUID_AHP_COERCETOFACTOID"></span><span id="guid_ahp_coercetofactoid"></span><dl> <span data-ttu-id="79701-112"><dt>**GUID \_ AHP \_ COERCETOFACTOID**</dt></span><span class="sxs-lookup"><span data-stu-id="79701-112"><dt>**GUID\_AHP\_COERCETOFACTOID**</dt></span></span> </dl>                                           | <span data-ttu-id="79701-113">筆跡分析器是否會限制其在提示區域內的筆墨分析，以符合模擬。</span><span class="sxs-lookup"><span data-stu-id="79701-113">Whether the ink analyzer limits its analysis of ink within the hint's area to conform to the factoid.</span></span><br/>                                          |
| <span id="GUID_AHP_ENABLEDUNICODECHARACTERRANGES"></span><span id="guid_ahp_enabledunicodecharacterranges"></span><dl> <span data-ttu-id="79701-114"><dt>**GUID \_ AHP \_ ENABLEDUNICODECHARACTERRANGES**</dt></span><span class="sxs-lookup"><span data-stu-id="79701-114"><dt>**GUID\_AHP\_ENABLEDUNICODECHARACTERRANGES**</dt></span></span> </dl> | <span data-ttu-id="79701-115">提示包含字元陣列，這些字元代表此 InkRecognizer 支援的一組受限制的 unicode 字元集。</span><span class="sxs-lookup"><span data-stu-id="79701-115">The hint contains an array of characters that represent the restricted set of supported unicode character set supported by this InkRecognizer.</span></span><br/> |
| <span id="GUID_AHP_FACTOID"></span><span id="guid_ahp_factoid"></span><dl> <span data-ttu-id="79701-116"><dt>**GUID \_ AHP 的 \_ 模擬**</dt></span><span class="sxs-lookup"><span data-stu-id="79701-116"><dt>**GUID\_AHP\_FACTOID**</dt></span></span> </dl>                                                                   | <span data-ttu-id="79701-117">分析提示上的模擬程式。</span><span class="sxs-lookup"><span data-stu-id="79701-117">The factoid on an analysis hint.</span></span><br/>                                                                                                               |
| <span id="GUID_AHP_GUIDE"></span><span id="guid_ahp_guide"></span><dl> <span data-ttu-id="79701-118"><dt>**GUID \_ AHP \_ 指南**</dt></span><span class="sxs-lookup"><span data-stu-id="79701-118"><dt>**GUID\_AHP\_GUIDE**</dt></span></span> </dl>                                                                         | <span data-ttu-id="79701-119">[**InkAnalysisRecognizerGuide**](inkanalysisrecognizerguide.md)結構，表示分析提示的指南。</span><span class="sxs-lookup"><span data-stu-id="79701-119">The [**InkAnalysisRecognizerGuide**](inkanalysisrecognizerguide.md) structure that represents the guide for an analysis hint.</span></span><br/>                 |
| <span id="GUID_AHP_PREFIXTEXT"></span><span id="guid_ahp_prefixtext"></span><dl> <span data-ttu-id="79701-120"><dt>**GUID \_ AHP \_ PREFIXTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="79701-120"><dt>**GUID\_AHP\_PREFIXTEXT**</dt></span></span> </dl>                                                          | <span data-ttu-id="79701-121">分析提示的前置詞文字。</span><span class="sxs-lookup"><span data-stu-id="79701-121">The prefix text on an analysis hint.</span></span><br/>                                                                                                           |
| <span id="GUID_AHP_SUFFIXTEXT"></span><span id="guid_ahp_suffixtext"></span><dl> <span data-ttu-id="79701-122"><dt>**GUID \_ AHP \_ SUFFIXTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="79701-122"><dt>**GUID\_AHP\_SUFFIXTEXT**</dt></span></span> </dl>                                                          | <span data-ttu-id="79701-123">分析提示上的尾碼文字。</span><span class="sxs-lookup"><span data-stu-id="79701-123">The suffix text on an analysis hint.</span></span><br/>                                                                                                           |
| <span id="GUID_AHP_TOPINKBREAKSONLY"></span><span id="guid_ahp_topinkbreaksonly"></span><dl> <span data-ttu-id="79701-124"><dt>**GUID \_ AHP \_ TOPINKBREAKSONLY**</dt></span><span class="sxs-lookup"><span data-stu-id="79701-124"><dt>**GUID\_AHP\_TOPINKBREAKSONLY**</dt></span></span> </dl>                                        | <span data-ttu-id="79701-125">筆墨辨識結果中的多個 segmentations 是否已停用。</span><span class="sxs-lookup"><span data-stu-id="79701-125">Whether the multiple segmentations in the ink recognition results are disabled.</span></span><br/>                                                                |
| <span id="GUID_AHP_WORDLIST"></span><span id="guid_ahp_wordlist"></span><dl> <span data-ttu-id="79701-126"><dt>**GUID \_ AHP \_ 單詞表**</dt></span><span class="sxs-lookup"><span data-stu-id="79701-126"><dt>**GUID\_AHP\_WORDLIST**</dt></span></span> </dl>                                                                | <span data-ttu-id="79701-127">字串的陣列，表示分析提示的字組清單。</span><span class="sxs-lookup"><span data-stu-id="79701-127">The array of strings that represents the word list for an analysis hint.</span></span><br/>                                                                       |
| <span id="GUID_AHP_WORDMODE"></span><span id="guid_ahp_wordmode"></span><dl> <span data-ttu-id="79701-128"><dt>**GUID \_ AHP \_ WORDMODE**</dt></span><span class="sxs-lookup"><span data-stu-id="79701-128"><dt>**GUID\_AHP\_WORDMODE**</dt></span></span> </dl>                                                                | <span data-ttu-id="79701-129">筆跡分析器是否會針對分析提示的多重單字結果排列單一單字結果的優先順序。</span><span class="sxs-lookup"><span data-stu-id="79701-129">Whether the ink analyzer prioritizes single-word results over multiple-word results for an analysis hint.</span></span><br/>                                      |



## <a name="remarks"></a><span data-ttu-id="79701-130">備註</span><span class="sxs-lookup"><span data-stu-id="79701-130">Remarks</span></span>

<span data-ttu-id="79701-131">這些 Guid 是用來識別 [**IInkAnalyzer**](iinkanalyzer.md) 可在分析提示內容節點上設定的屬性 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 。</span><span class="sxs-lookup"><span data-stu-id="79701-131">These GUIDs are used to identify properties that the [**IInkAnalyzer**](iinkanalyzer.md) can set on an analysis hint context node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

<span data-ttu-id="79701-132">若要取得或設定 [**ICoNtextNode**](icontextnode.md) 的一般屬性，請參閱 [內容節點屬性](context-node-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="79701-132">To get or set properties of an [**IContextNode**](icontextnode.md) in general, see [Context Node Properties](context-node-properties.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="79701-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="79701-133">Requirements</span></span>



| <span data-ttu-id="79701-134">需求</span><span class="sxs-lookup"><span data-stu-id="79701-134">Requirement</span></span> | <span data-ttu-id="79701-135">值</span><span class="sxs-lookup"><span data-stu-id="79701-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="79701-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79701-136">Minimum supported client</span></span><br/> | <span data-ttu-id="79701-137">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79701-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="79701-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79701-138">Minimum supported server</span></span><br/> | <span data-ttu-id="79701-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="79701-139">None supported</span></span><br/>                                                           |
| <span data-ttu-id="79701-140">標頭</span><span class="sxs-lookup"><span data-stu-id="79701-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="79701-141"><dt>Iaguid。h</dt></span><span class="sxs-lookup"><span data-stu-id="79701-141"><dt>Iaguid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79701-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79701-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79701-143">內容節點屬性</span><span class="sxs-lookup"><span data-stu-id="79701-143">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="79701-144">內容節點類型</span><span class="sxs-lookup"><span data-stu-id="79701-144">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="79701-145">**IInkAnalyzer：： CreateAnalysisHint 方法**</span><span class="sxs-lookup"><span data-stu-id="79701-145">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="79701-146">**IInkAnalyzer：： GetAnalysisHintsByName 方法**</span><span class="sxs-lookup"><span data-stu-id="79701-146">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="79701-147">**ICoNtextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="79701-147">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="79701-148">**ICoNtextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="79701-148">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="79701-149">**ICoNtextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="79701-149">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="79701-150">**ICoNtextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="79701-150">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="79701-151">**ICoNtextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="79701-151">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="79701-152">**ICoNtextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="79701-152">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="79701-153">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="79701-153">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




