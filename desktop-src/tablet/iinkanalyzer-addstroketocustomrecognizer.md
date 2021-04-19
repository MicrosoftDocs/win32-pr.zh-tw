---
description: 將單一筆觸的筆觸資料新增至自訂辨識器節點。
ms.assetid: ab43c9f8-15fe-49db-b9d1-57d34b95d99f
title: 'IInkAnalyzer：： AddStrokeToCustomRecognizer 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c04b60acd2f40b5ed3960c9932ce066b337d81cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973654"
---
# <a name="iinkanalyzeraddstroketocustomrecognizer-method"></a><span data-ttu-id="8baf9-103">IInkAnalyzer：： AddStrokeToCustomRecognizer 方法</span><span class="sxs-lookup"><span data-stu-id="8baf9-103">IInkAnalyzer::AddStrokeToCustomRecognizer method</span></span>

<span data-ttu-id="8baf9-104">將單一筆觸的筆觸資料新增至自訂辨識器節點。</span><span class="sxs-lookup"><span data-stu-id="8baf9-104">Adds stroke data for a single stroke to a custom recognizer node.</span></span>

## <a name="syntax"></a><span data-ttu-id="8baf9-105">語法</span><span class="sxs-lookup"><span data-stu-id="8baf9-105">Syntax</span></span>


```C++
HRESULT AddStrokeToCustomRecognizer(
  [in]  ULONG        ulStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="8baf9-106">參數</span><span class="sxs-lookup"><span data-stu-id="8baf9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8baf9-107">*ulStrokeId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8baf9-107">*ulStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8baf9-108">要加入之筆劃的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8baf9-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="8baf9-109">*ulStrokePacketDataCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8baf9-109">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8baf9-110">筆劃中的封包數目。</span><span class="sxs-lookup"><span data-stu-id="8baf9-110">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="8baf9-111">*plStrokePacketData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8baf9-111">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8baf9-112">陣列，其中包含筆劃的封包資料。</span><span class="sxs-lookup"><span data-stu-id="8baf9-112">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="8baf9-113">*ulStrokePacketDescriptionCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8baf9-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8baf9-114">每個封包中的封包屬性數目。</span><span class="sxs-lookup"><span data-stu-id="8baf9-114">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="8baf9-115">*pStrokePacketDescriptionGuids* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8baf9-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8baf9-116">陣列，包含封包屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="8baf9-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="8baf9-117">*pCustomRecognizer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8baf9-117">*pCustomRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8baf9-118">要加入筆劃之 **CustomRecognizer** 類型的 [**ICoNtextNode**](icontextnode.md) 。</span><span class="sxs-lookup"><span data-stu-id="8baf9-118">The [**IContextNode**](icontextnode.md) of type **CustomRecognizer** to which to add the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="8baf9-119">*ppCoNtextNodeStrokeAddedTo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8baf9-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8baf9-120">筆跡分析器新增筆劃的 [**ICoNtextNode**](icontextnode.md) 。</span><span class="sxs-lookup"><span data-stu-id="8baf9-120">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8baf9-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="8baf9-121">Return value</span></span>

<span data-ttu-id="8baf9-122">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="8baf9-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8baf9-123">備註</span><span class="sxs-lookup"><span data-stu-id="8baf9-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="8baf9-124">若要避免記憶體流失，請在 *ppCoNtextNodeStrokeAddedTo* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="8baf9-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="8baf9-125">當 *ppCoNtextNodeStrokeAddedTo* 為 **Null** 時，表示呼叫端對方法的傳回值不感興趣。</span><span class="sxs-lookup"><span data-stu-id="8baf9-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="8baf9-126">[**IInkAnalyzer**](iinkanalyzer.md)會將筆劃新增至類型 **CustomRecognizer** 的 [**ICoNtextNode**](icontextnode.md) (請參閱) 的 [內容節點類型](context-node-types.md)。</span><span class="sxs-lookup"><span data-stu-id="8baf9-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type **CustomRecognizer** (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="8baf9-127">此節點位於根節點的子節點集合中 (請參閱 [**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md) 和 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md) 方法) 。</span><span class="sxs-lookup"><span data-stu-id="8baf9-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="8baf9-128">[**IInkAnalyzer**](iinkanalyzer.md)會將使用中輸入執行緒的文化特性識別碼指派給筆劃，然後將筆劃加入至 **CustomRecognizer** 節點下的第一個 **UnclassifiedInk** 節點。</span><span class="sxs-lookup"><span data-stu-id="8baf9-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the stroke and adds the stroke to the first **UnclassifiedInk** node under the **CustomRecognizer** node.</span></span> <span data-ttu-id="8baf9-129">如果沒有 **UnclassifiedInk** 節點存在，則會建立它。</span><span class="sxs-lookup"><span data-stu-id="8baf9-129">If no **UnclassifiedInk** node exists, it is created.</span></span> <span data-ttu-id="8baf9-130">如果與 **CustomRecognizer** 節點相關聯的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)不支援文化特性識別碼，則 **IInkAnalyzer** 會繼續分析並產生 [**IAnalysisWarning**](ianalysiswarning.md)警告。</span><span class="sxs-lookup"><span data-stu-id="8baf9-130">If the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associated with the **CustomRecognizer** node does not support the culture identifier, the **IInkAnalyzer** continues analyzing and generates an [**IAnalysisWarning**](ianalysiswarning.md) warning.</span></span> <span data-ttu-id="8baf9-131">此警告的 [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) 值為 **AnalysisWarningCode \_ LanguageIdNotRespected**。</span><span class="sxs-lookup"><span data-stu-id="8baf9-131">This warning has an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_LanguageIdNotRespected**.</span></span>

<span data-ttu-id="8baf9-132">*plStrokePacketData* 包含筆劃中所有點的封包資料。</span><span class="sxs-lookup"><span data-stu-id="8baf9-132">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="8baf9-133">*pStrokePacketDescriptionGuids* 包含 (guid) 的全域唯一識別碼，描述每個筆劃中每個點所包含的封包資料類型。</span><span class="sxs-lookup"><span data-stu-id="8baf9-133">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="8baf9-134">如需可用的封包屬性完整清單，請參閱 [PacketPropertyGuids 常數](packetpropertyguids-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="8baf9-134">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="8baf9-135">這個方法會將中途區域展開至區域目前值的聯集，以及已加入筆劃的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="8baf9-135">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="8baf9-136">在下列情況下， [**IInkAnalyzer**](iinkanalyzer.md)會傳回 **E \_ INVALIDARG** 的 **HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="8baf9-136">The [**IInkAnalyzer**](iinkanalyzer.md) returns an **HRESULT** of **E\_INVALIDARG** under the following circumstances.</span></span>

-   <span data-ttu-id="8baf9-137">[**IInkAnalyzer**](iinkanalyzer.md)已包含與要加入之筆劃具有相同識別碼的筆劃。</span><span class="sxs-lookup"><span data-stu-id="8baf9-137">The [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as the stroke to be added.</span></span>
-   <span data-ttu-id="8baf9-138">*PCustomRecognizer* 參數包含與不同 [**IInkAnalyzer**](iinkanalyzer.md)物件相關聯的自訂辨識器節點。</span><span class="sxs-lookup"><span data-stu-id="8baf9-138">The *pCustomRecognizer* parameter contains a custom recognizer node that is associated with a different [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>
-   <span data-ttu-id="8baf9-139">*PCustomRecognizer* 參數包含的 [**ICoNtextNode**](icontextnode.md)不是 **CustomRecognizer** 類型。</span><span class="sxs-lookup"><span data-stu-id="8baf9-139">The *pCustomRecognizer* parameter contains an [**IContextNode**](icontextnode.md) that is not of type **CustomRecognizer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8baf9-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="8baf9-140">Requirements</span></span>



| <span data-ttu-id="8baf9-141">需求</span><span class="sxs-lookup"><span data-stu-id="8baf9-141">Requirement</span></span> | <span data-ttu-id="8baf9-142">值</span><span class="sxs-lookup"><span data-stu-id="8baf9-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8baf9-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8baf9-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8baf9-144">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8baf9-144">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8baf9-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8baf9-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8baf9-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="8baf9-146">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8baf9-147">標頭</span><span class="sxs-lookup"><span data-stu-id="8baf9-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="8baf9-148"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="8baf9-148"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8baf9-149">DLL</span><span class="sxs-lookup"><span data-stu-id="8baf9-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8baf9-150"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8baf9-150"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8baf9-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8baf9-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8baf9-152">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="8baf9-152">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8baf9-153">內容節點類型</span><span class="sxs-lookup"><span data-stu-id="8baf9-153">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="8baf9-154">**IInkAnalyzer：： AddStrokesToCustomRecognizer 方法**</span><span class="sxs-lookup"><span data-stu-id="8baf9-154">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="8baf9-155">**IInkAnalyzer：： CreateCustomRecognizer 方法**</span><span class="sxs-lookup"><span data-stu-id="8baf9-155">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="8baf9-156">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="8baf9-156">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

