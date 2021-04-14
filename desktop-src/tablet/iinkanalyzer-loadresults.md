---
description: 將儲存的分析結果載入 IInkAnalyzer 中。
ms.assetid: 7634dbe2-1857-497c-81b5-76b92fed862d
title: 'IInkAnalyzer：： LoadResults 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.LoadResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 76c7fed63b38f1b4fc058fbe7676a727c2d47f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469124"
---
# <a name="iinkanalyzerloadresults-method"></a><span data-ttu-id="6f1ea-103">IInkAnalyzer：： LoadResults 方法</span><span class="sxs-lookup"><span data-stu-id="6f1ea-103">IInkAnalyzer::LoadResults method</span></span>

<span data-ttu-id="6f1ea-104">將儲存的分析結果載入 [**IInkAnalyzer**](iinkanalyzer.md)中。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-104">Loads saved analysis results into the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f1ea-105">語法</span><span class="sxs-lookup"><span data-stu-id="6f1ea-105">Syntax</span></span>


```C++
HRESULT LoadResults(
  [in]          ULONG        ulDataSize,
  [in]          BYTE         *pbSerializedResults,
  [in]          ULONG        ulStrokeIdsCount,
  [in]          LONG         *plOriginalStrokeIds,
  [in]          LONG         *plNewStrokeIds,
  [out, retval] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="6f1ea-106">參數</span><span class="sxs-lookup"><span data-stu-id="6f1ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f1ea-107">*ulDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f1ea-107">*ulDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f1ea-108">*PbSerializedResults* 中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-108">The number of bytes in *pbSerializedResults*.</span></span>

</dd> <dt>

<span data-ttu-id="6f1ea-109">*pbSerializedResults* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f1ea-109">*pbSerializedResults* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f1ea-110">序列化分析結果。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-110">The serialized analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="6f1ea-111">*ulStrokeIdsCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f1ea-111">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f1ea-112">筆觸識別碼的數目。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-112">The number of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="6f1ea-113">*plOriginalStrokeIds* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f1ea-113">*plOriginalStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f1ea-114">原始筆觸識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-114">The array of original stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="6f1ea-115">*plNewStrokeIds* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f1ea-115">*plNewStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f1ea-116">新筆劃識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-116">The array of new stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="6f1ea-117">*pfSuccessful* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="6f1ea-117">*pfSuccessful* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6f1ea-118">**變異 \_** 如果載入成功則為 TRUE;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-118">**VARIANT\_TRUE** if loading was successful; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f1ea-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="6f1ea-119">Return value</span></span>

<span data-ttu-id="6f1ea-120">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6f1ea-121">備註</span><span class="sxs-lookup"><span data-stu-id="6f1ea-121">Remarks</span></span>

<span data-ttu-id="6f1ea-122">當 [**IInkAnalyzer**](iinkanalyzer.md) 從儲存的結果加入 [**ICoNtextNode**](icontextnode.md) 時，它會將新的全域唯一識別碼 (GUID) 指派給 **ICoNtextNode** (請參閱 [**ICoNtextNode：： GetPropertyData**](icontextnode-getpropertydata.md) 和 [內容節點屬性](context-node-properties.md)) 。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-122">When the [**IInkAnalyzer**](iinkanalyzer.md) adds a [**IContextNode**](icontextnode.md) from the saved results, it assigns a new globally unique identifier (GUID) to the **IContextNode** (see [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md) and [Context Node Properties](context-node-properties.md)).</span></span>

<span data-ttu-id="6f1ea-123">這個方法會將已儲存的分析結果新增至現有的 [**ICoNtextNode**](icontextnode.md) 樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-123">This method adds the saved analysis results to the existing [**IContextNode**](icontextnode.md) tree.</span></span> <span data-ttu-id="6f1ea-124">為了確保合併的結果順序正確，請將包含已載入內容節點的區域加入至 [**IInkAnalyzer**](iinkanalyzer.md) 物件的中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 和重新分析筆墨。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-124">To ensure that the combined results are ordered correctly, add the area containing the loaded context nodes to the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) and reanalyze the ink.</span></span>

<span data-ttu-id="6f1ea-125">[**IInkAnalyzer：： SaveResults 方法**](iinkanalyzer-saveresults.md)、 [**IInkAnalyzer：： SaveResultsForNodes 方法**](iinkanalyzer-saveresultsfornodes.md)和 [**IInkAnalyzer：： SaveResultsForStrokes 方法**](iinkanalyzer-saveresultsforstrokes.md)方法不會儲存封包資料和分析結果。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-125">The [**IInkAnalyzer::SaveResults Method**](iinkanalyzer-saveresults.md), [**IInkAnalyzer::SaveResultsForNodes Method**](iinkanalyzer-saveresultsfornodes.md), and [**IInkAnalyzer::SaveResultsForStrokes Method**](iinkanalyzer-saveresultsforstrokes.md) methods do not save the packet data along with the analysis results.</span></span>

<span data-ttu-id="6f1ea-126">*PlOriginalStrokeIds* 中的每個識別碼都是儲存分析結果中筆劃的筆觸識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-126">Each identifier in *plOriginalStrokeIds* is the stroke identifier for the stroke in the saved analysis results.</span></span> <span data-ttu-id="6f1ea-127">*PlNewStrokeIds* 中的每個識別碼都是新的識別碼，用來取代載入的分析結果中的原始識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-127">Each identifier in *plNewStrokeIds* is the new identifier with which to replace the original identifier in the loaded analysis results.</span></span>

<span data-ttu-id="6f1ea-128">如果已儲存的分析提示與現有的分析提示發生衝突，則 [**IInkAnalyzer**](iinkanalyzer.md) 不會載入儲存的提示，但會載入其餘的儲存結果。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-128">If a saved analysis hint conflicts with an existing analysis hint, the [**IInkAnalyzer**](iinkanalyzer.md) does not load the saved hint but does load the rest of the saved results.</span></span> <span data-ttu-id="6f1ea-129">但是，如果 **IInkAnalyzer** 在 **IInkAnalyzer** 未載入的已儲存分析提示區域內載入筆觸的結果，則 **IInkAnalyzer** 會將筆劃的周框方塊加入 **IInkAnalyzer** 物件的已變更區域。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-129">However, if the **IInkAnalyzer** loads results for a stroke that is within the area of a saved analysis hint that the **IInkAnalyzer** does not load, the **IInkAnalyzer** adds the bounding box of the stroke to the **IInkAnalyzer** object's dirty region.</span></span> <span data-ttu-id="6f1ea-130">此外，如果 **IInkAnalyzer** 為現有分析提示區域內的筆劃載入結果， **IInkAnalyzer** 也會將筆劃的周框方塊新增至 **IInkAnalyzer** 物件的已變更區域。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-130">Also, if the **IInkAnalyzer** loads results for a stroke that is within an existing analysis hint's area, the **IInkAnalyzer** also adds the bounding box of the stroke to the **IInkAnalyzer** object's dirty region.</span></span> <span data-ttu-id="6f1ea-131">如需有關分析提示的詳細資訊，請參閱 [分析提示屬性](analysis-hint-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-131">For more information about analysis hints, see [Analysis Hint Properties](analysis-hint-properties.md).</span></span>

<span data-ttu-id="6f1ea-132">當載入儲存的結果時，這個方法可能會引發 [**\_ IAnalysisProxyEvents：： CoNtextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md)、 [**\_ IAnalysisProxyEvents：： CoNtextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)和 [**\_ IAnalysisProxyEvents：： CoNtextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md)事件。</span><span class="sxs-lookup"><span data-stu-id="6f1ea-132">This method may raise the [**\_IAnalysisProxyEvents::ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md), and [**\_IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) events as it loads the saved results.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f1ea-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f1ea-133">Requirements</span></span>



| <span data-ttu-id="6f1ea-134">需求</span><span class="sxs-lookup"><span data-stu-id="6f1ea-134">Requirement</span></span> | <span data-ttu-id="6f1ea-135">值</span><span class="sxs-lookup"><span data-stu-id="6f1ea-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f1ea-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f1ea-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6f1ea-137">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f1ea-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6f1ea-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f1ea-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6f1ea-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="6f1ea-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6f1ea-140">標頭</span><span class="sxs-lookup"><span data-stu-id="6f1ea-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f1ea-141"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="6f1ea-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6f1ea-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6f1ea-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f1ea-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f1ea-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6f1ea-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f1ea-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f1ea-145">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="6f1ea-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="6f1ea-146">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="6f1ea-146">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="6f1ea-147">**IInkAnalyzer：： GetDirtyRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="6f1ea-147">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="6f1ea-148">**IInkAnalyzer：： SetDirtyRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="6f1ea-148">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="6f1ea-149">**IInkAnalyzer：： SaveResults 方法**</span><span class="sxs-lookup"><span data-stu-id="6f1ea-149">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="6f1ea-150">**IInkAnalyzer：： SaveResultsForNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="6f1ea-150">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="6f1ea-151">**IInkAnalyzer：： SaveResultsForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="6f1ea-151">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="6f1ea-152">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="6f1ea-152">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




