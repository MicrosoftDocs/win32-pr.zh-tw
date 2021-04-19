---
description: 將多個筆劃的筆觸資料新增至自訂辨識器節點。
ms.assetid: 77ded896-8573-42de-a41e-4866894dfe2b
title: 'IInkAnalyzer：： AddStrokesToCustomRecognizer 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6df1b31957f3b4087b51fbad0e7b527c2ede799c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986357"
---
# <a name="iinkanalyzeraddstrokestocustomrecognizer-method"></a><span data-ttu-id="cb030-103">IInkAnalyzer：： AddStrokesToCustomRecognizer 方法</span><span class="sxs-lookup"><span data-stu-id="cb030-103">IInkAnalyzer::AddStrokesToCustomRecognizer method</span></span>

<span data-ttu-id="cb030-104">將多個筆劃的筆觸資料新增至自訂辨識器節點。</span><span class="sxs-lookup"><span data-stu-id="cb030-104">Adds stroke data for multiple strokes to a custom recognizer node.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb030-105">語法</span><span class="sxs-lookup"><span data-stu-id="cb030-105">Syntax</span></span>


```C++
HRESULT AddStrokesToCustomRecognizer(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="cb030-106">參數</span><span class="sxs-lookup"><span data-stu-id="cb030-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb030-107">*ulStrokeIdsCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb030-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb030-108">要加入的筆劃數目。</span><span class="sxs-lookup"><span data-stu-id="cb030-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="cb030-109">*plStrokeIds* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb030-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb030-110">包含筆觸識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="cb030-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="cb030-111">*ulStrokePacketDescriptionCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb030-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb030-112">每個封包中的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="cb030-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="cb030-113">*pStrokePacketDescriptionGuids* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb030-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb030-114">陣列，包含封包屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb030-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="cb030-115">*pulPacketDataCountPerStroke* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb030-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb030-116">陣列，其中包含每個筆劃中的封包數目。</span><span class="sxs-lookup"><span data-stu-id="cb030-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="cb030-117">*plStrokePacketData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb030-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb030-118">陣列，其中包含筆觸的封包資料。</span><span class="sxs-lookup"><span data-stu-id="cb030-118">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="cb030-119">*pCustomRecognizer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb030-119">*pCustomRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb030-120">要加入筆劃之 **CustomRecognizer** 類型的 [**ICoNtextNode**](icontextnode.md) 。</span><span class="sxs-lookup"><span data-stu-id="cb030-120">The [**IContextNode**](icontextnode.md) of type **CustomRecognizer** to which to add the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="cb030-121">*ppCoNtextNodeStrokeAddedTo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cb030-121">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb030-122">筆跡分析器新增筆劃的 [**ICoNtextNode**](icontextnode.md) 。</span><span class="sxs-lookup"><span data-stu-id="cb030-122">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb030-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb030-123">Return value</span></span>

<span data-ttu-id="cb030-124">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="cb030-124">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cb030-125">備註</span><span class="sxs-lookup"><span data-stu-id="cb030-125">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="cb030-126">若要避免記憶體流失，請在 *ppCoNtextNodeStrokeAddedTo* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="cb030-126">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="cb030-127">當 *ppCoNtextNodeStrokeAddedTo* 為 **Null** 時，表示呼叫端對方法的傳回值不感興趣。</span><span class="sxs-lookup"><span data-stu-id="cb030-127">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="cb030-128">[**IInkAnalyzer**](iinkanalyzer.md)會將筆劃新增至類型 **CustomRecognizer** 的 [**ICoNtextNode**](icontextnode.md) (請參閱) 的 [內容節點類型](context-node-types.md)。</span><span class="sxs-lookup"><span data-stu-id="cb030-128">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type **CustomRecognizer** (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="cb030-129">此節點位於根節點的子節點集合中 (請參閱 [**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md) 和 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md) 方法) 。</span><span class="sxs-lookup"><span data-stu-id="cb030-129">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="cb030-130">[**IInkAnalyzer**](iinkanalyzer.md)會將使用中輸入執行緒的文化特性識別碼指派給筆劃，然後將筆劃加入至 **CustomRecognizer** 節點下的第一個 **UnclassifiedInk** 節點。</span><span class="sxs-lookup"><span data-stu-id="cb030-130">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the strokes and adds the strokes to the first **UnclassifiedInk** node under the **CustomRecognizer** node.</span></span> <span data-ttu-id="cb030-131">如果沒有 **UnclassifiedInk** 節點存在，則會建立它。</span><span class="sxs-lookup"><span data-stu-id="cb030-131">If no **UnclassifiedInk** node exists, it is created.</span></span> <span data-ttu-id="cb030-132">如果與 **CustomRecognizer** 節點相關聯的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)不支援文化特性識別碼，則 **IInkAnalyzer** 會繼續分析並產生 [**IAnalysisWarning**](ianalysiswarning.md)警告。</span><span class="sxs-lookup"><span data-stu-id="cb030-132">If the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associated with the **CustomRecognizer** node does not support the culture identifier, the **IInkAnalyzer** continues analyzing and generates an [**IAnalysisWarning**](ianalysiswarning.md) warning.</span></span> <span data-ttu-id="cb030-133">此警告的 [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) 值為 **AnalysisWarningCode \_ LanguageIdNotRespected**。</span><span class="sxs-lookup"><span data-stu-id="cb030-133">This warning has an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_LanguageIdNotRespected**.</span></span>

<span data-ttu-id="cb030-134">*plStrokePacketData* 包含所有筆劃的封包資料。</span><span class="sxs-lookup"><span data-stu-id="cb030-134">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="cb030-135">*pStrokePacketDescriptionGuids* 包含 (guid) 的全域唯一識別碼，描述每個筆劃中每個點所包含的封包資料類型。</span><span class="sxs-lookup"><span data-stu-id="cb030-135">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="cb030-136">如需可用的封包屬性完整清單，請參閱 [PacketPropertyGuids 常數](packetpropertyguids-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="cb030-136">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="cb030-137">**IInkAnalyzer：： AddStrokesToCustomRecognizer 方法** 的單一呼叫中只能新增具有相同封包描述的筆劃。</span><span class="sxs-lookup"><span data-stu-id="cb030-137">Only strokes with the same packet descriptions can be added in a single call to **IInkAnalyzer::AddStrokesToCustomRecognizer Method**.</span></span>

 

<span data-ttu-id="cb030-138">這個方法會將中途區域擴展至區域目前值的聯集，以及加入之筆劃的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="cb030-138">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="cb030-139">在下列情況下， [**IInkAnalyzer**](iinkanalyzer.md)會傳回 **E \_ INVALIDARG** 的 **HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="cb030-139">The [**IInkAnalyzer**](iinkanalyzer.md) returns an **HRESULT** of **E\_INVALIDARG** under the following circumstances.</span></span>

-   <span data-ttu-id="cb030-140">[**IInkAnalyzer**](iinkanalyzer.md)已經包含一個筆觸，其識別碼與要加入的其中一個筆劃具有相同的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb030-140">The [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added.</span></span>
-   <span data-ttu-id="cb030-141">*PCustomRecognizer* 參數包含與不同 [**IInkAnalyzer**](iinkanalyzer.md)物件相關聯的自訂辨識器節點。</span><span class="sxs-lookup"><span data-stu-id="cb030-141">The *pCustomRecognizer* parameter contains a custom recognizer node that is associated with a different [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>
-   <span data-ttu-id="cb030-142">*PCustomRecognizer* 參數包含的 [**ICoNtextNode**](icontextnode.md)不是 **CustomRecognizer** 類型。</span><span class="sxs-lookup"><span data-stu-id="cb030-142">The *pCustomRecognizer* parameter contains an [**IContextNode**](icontextnode.md) that is not of type **CustomRecognizer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb030-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb030-143">Requirements</span></span>



| <span data-ttu-id="cb030-144">需求</span><span class="sxs-lookup"><span data-stu-id="cb030-144">Requirement</span></span> | <span data-ttu-id="cb030-145">值</span><span class="sxs-lookup"><span data-stu-id="cb030-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb030-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb030-146">Minimum supported client</span></span><br/> | <span data-ttu-id="cb030-147">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb030-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cb030-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb030-148">Minimum supported server</span></span><br/> | <span data-ttu-id="cb030-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="cb030-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cb030-150">標頭</span><span class="sxs-lookup"><span data-stu-id="cb030-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb030-151"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="cb030-151"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cb030-152">DLL</span><span class="sxs-lookup"><span data-stu-id="cb030-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb030-153"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb030-153"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cb030-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb030-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb030-155">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="cb030-155">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="cb030-156">內容節點類型</span><span class="sxs-lookup"><span data-stu-id="cb030-156">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="cb030-157">**IInkAnalyzer：： AddStrokeToCustomRecognizer 方法**</span><span class="sxs-lookup"><span data-stu-id="cb030-157">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="cb030-158">**IInkAnalyzer：： CreateCustomRecognizer 方法**</span><span class="sxs-lookup"><span data-stu-id="cb030-158">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="cb030-159">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="cb030-159">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

