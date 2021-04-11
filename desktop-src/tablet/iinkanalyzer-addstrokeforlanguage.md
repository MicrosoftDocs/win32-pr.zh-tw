---
description: 將單一筆劃的筆觸資料新增至 IInkAnalyzer，並將特定文化特性識別碼指派給筆劃。
ms.assetid: 65eb805e-05ed-4144-b17e-872c47ab33fa
title: 'IInkAnalyzer：： AddStrokeForLanguage 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 674a58ef891d919d09f86f28a35748de3537db91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848083"
---
# <a name="iinkanalyzeraddstrokeforlanguage-method"></a><span data-ttu-id="534f0-103">IInkAnalyzer：： AddStrokeForLanguage 方法</span><span class="sxs-lookup"><span data-stu-id="534f0-103">IInkAnalyzer::AddStrokeForLanguage method</span></span>

<span data-ttu-id="534f0-104">將單一筆劃的筆觸資料新增至 [**IInkAnalyzer**](iinkanalyzer.md) ，並將特定文化特性識別碼指派給筆劃。</span><span class="sxs-lookup"><span data-stu-id="534f0-104">Adds stroke data for a single stroke to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns a specific culture identifier to the stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="534f0-105">語法</span><span class="sxs-lookup"><span data-stu-id="534f0-105">Syntax</span></span>


```C++
HRESULT AddStrokeForLanguage(
  [in]  LONG         lStrokeId,
  [in]  LONG         lStrokeLCID,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="534f0-106">參數</span><span class="sxs-lookup"><span data-stu-id="534f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="534f0-107">*lStrokeId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="534f0-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="534f0-108">要加入之筆劃的識別碼。</span><span class="sxs-lookup"><span data-stu-id="534f0-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="534f0-109">*lStrokeLCID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="534f0-109">*lStrokeLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="534f0-110">要指派給筆劃的文化特性識別碼。</span><span class="sxs-lookup"><span data-stu-id="534f0-110">The culture identifier to assign to the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="534f0-111">*ulStrokePacketDataCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="534f0-111">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="534f0-112">筆劃中的封包數目。</span><span class="sxs-lookup"><span data-stu-id="534f0-112">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="534f0-113">*plStrokePacketData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="534f0-113">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="534f0-114">陣列，其中包含筆劃的封包資料。</span><span class="sxs-lookup"><span data-stu-id="534f0-114">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="534f0-115">*ulStrokePacketDescriptionCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="534f0-115">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="534f0-116">每個封包中的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="534f0-116">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="534f0-117">*pStrokePacketDescriptionGuids* \[在\]</span><span class="sxs-lookup"><span data-stu-id="534f0-117">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="534f0-118">陣列，包含封包屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="534f0-118">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="534f0-119">*ppCoNtextNodeStrokeAddedTo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="534f0-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="534f0-120">指標，其值會設定為 [**ICoNtextNode**](icontextnode.md) 的指標，其中包含新增的筆劃。</span><span class="sxs-lookup"><span data-stu-id="534f0-120">A pointer whose value is set to the pointer of the [**IContextNode**](icontextnode.md) that contains the newly added stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="534f0-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="534f0-121">Return value</span></span>

<span data-ttu-id="534f0-122">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="534f0-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="534f0-123">備註</span><span class="sxs-lookup"><span data-stu-id="534f0-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="534f0-124">若要避免記憶體流失，請在 *ppCoNtextNodeStrokeAddedTo* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="534f0-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="534f0-125">當 *ppCoNtextNodeStrokeAddedTo* 為 **Null** 時，表示呼叫端對方法的傳回值不感興趣。</span><span class="sxs-lookup"><span data-stu-id="534f0-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="534f0-126">[**IInkAnalyzer**](iinkanalyzer.md)會將筆劃新增至類型 UnclassifiedInk 的 [**ICoNtextNode**](icontextnode.md) (請參閱) 的 [內容節點類型](context-node-types.md)。</span><span class="sxs-lookup"><span data-stu-id="534f0-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="534f0-127">此節點位於根節點的子節點集合中 (請參閱 [**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md) 和 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md) 方法) 。</span><span class="sxs-lookup"><span data-stu-id="534f0-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="534f0-128">[**IInkAnalyzer**](iinkanalyzer.md)會將 *lStrokeLCID* 文化特性識別碼指派給筆劃，然後將筆劃加入至筆墨分析器根節點下的第一個 UnclassifiedInk 內容節點，其中包含具有相同文化特性識別碼的筆觸。</span><span class="sxs-lookup"><span data-stu-id="534f0-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns *lStrokeLCID* culture identifier to the stroke and adds the stroke to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="534f0-129">如果筆墨分析器沒有具有相同文化特性識別碼的節點，它會在其根節點下建立新的 UnclassifiedInk 內容節點，並將筆劃加入新的 UnclassifiedInk 內容節點。</span><span class="sxs-lookup"><span data-stu-id="534f0-129">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the stroke to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="534f0-130">*plStrokePacketData* 包含筆劃中所有點的封包資料。</span><span class="sxs-lookup"><span data-stu-id="534f0-130">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="534f0-131">*pStrokePacketDescriptionGuids* 包含 (guid) 的全域唯一識別碼，描述筆劃中每個點所包含的封包資料類型。</span><span class="sxs-lookup"><span data-stu-id="534f0-131">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="534f0-132">如需可用的封包屬性完整清單，請參閱 [PacketPropertyGuids 常數](packetpropertyguids-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="534f0-132">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="534f0-133">這個方法會將中途區域展開至區域目前值的聯集，以及已加入筆劃的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="534f0-133">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="534f0-134">如果 [**IInkAnalyzer**](iinkanalyzer.md)已包含具有相同筆觸識別碼的筆劃，則 **IInkAnalyzer** 會傳回 **E \_ INVALIDARG** 的 **HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="534f0-134">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same stroke identifier, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="534f0-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="534f0-135">Requirements</span></span>



| <span data-ttu-id="534f0-136">需求</span><span class="sxs-lookup"><span data-stu-id="534f0-136">Requirement</span></span> | <span data-ttu-id="534f0-137">值</span><span class="sxs-lookup"><span data-stu-id="534f0-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="534f0-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="534f0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="534f0-139">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="534f0-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="534f0-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="534f0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="534f0-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="534f0-141">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="534f0-142">標頭</span><span class="sxs-lookup"><span data-stu-id="534f0-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="534f0-143"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="534f0-143"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="534f0-144">DLL</span><span class="sxs-lookup"><span data-stu-id="534f0-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="534f0-145"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="534f0-145"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="534f0-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="534f0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="534f0-147">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="534f0-147">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="534f0-148">**IInkAnalyzer：： AddStroke 方法**</span><span class="sxs-lookup"><span data-stu-id="534f0-148">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="534f0-149">**IInkAnalyzer：： AddStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="534f0-149">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="534f0-150">**IInkAnalyzer：： AddStrokesForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="534f0-150">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="534f0-151">**IInkAnalyzer：： RemoveStroke 方法**</span><span class="sxs-lookup"><span data-stu-id="534f0-151">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="534f0-152">**IInkAnalyzer：： RemoveStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="534f0-152">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="534f0-153">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="534f0-153">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

