---
description: 將多個筆劃的筆觸資料新增至 IInkAnalyzer，並將指定的文化特性識別碼指派給筆觸。
ms.assetid: 1274b24f-204b-4a84-a7c0-0205b6068ae8
title: 'IInkAnalyzer：： AddStrokesForLanguage 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7f1c8bde9f1fe9d9c7123fa3c40540d0fd2660ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191411"
---
# <a name="iinkanalyzeraddstrokesforlanguage-method"></a><span data-ttu-id="225b4-103">IInkAnalyzer：： AddStrokesForLanguage 方法</span><span class="sxs-lookup"><span data-stu-id="225b4-103">IInkAnalyzer::AddStrokesForLanguage method</span></span>

<span data-ttu-id="225b4-104">將多個筆劃的筆觸資料新增至 [**IInkAnalyzer**](iinkanalyzer.md) ，並將指定的文化特性識別碼指派給筆觸。</span><span class="sxs-lookup"><span data-stu-id="225b4-104">Adds stroke data for multiple strokes to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the specified culture identifier to the strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="225b4-105">語法</span><span class="sxs-lookup"><span data-stu-id="225b4-105">Syntax</span></span>


```C++
HRESULT AddStrokesForLanguage(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plIdofStrokesToAdd,
  [in]  LONG         lStrokesLCID,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="225b4-106">參數</span><span class="sxs-lookup"><span data-stu-id="225b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="225b4-107">*ulStrokeIdsCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="225b4-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="225b4-108">要加入的筆劃數目。</span><span class="sxs-lookup"><span data-stu-id="225b4-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="225b4-109">*plIdofStrokesToAdd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="225b4-109">*plIdofStrokesToAdd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="225b4-110">包含筆觸識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="225b4-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="225b4-111">*lStrokesLCID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="225b4-111">*lStrokesLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="225b4-112">值，表示要指派給筆劃的文化特性識別碼。</span><span class="sxs-lookup"><span data-stu-id="225b4-112">A value that represents the culture identifier to assign to the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="225b4-113">*ulStrokePacketDescriptionCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="225b4-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="225b4-114">每個封包中的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="225b4-114">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="225b4-115">*pStrokePacketDescriptionGuids* \[在\]</span><span class="sxs-lookup"><span data-stu-id="225b4-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="225b4-116">陣列，包含封包屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="225b4-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="225b4-117">*pulPacketDataCountPerStroke* \[在\]</span><span class="sxs-lookup"><span data-stu-id="225b4-117">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="225b4-118">陣列，其中包含每個筆劃中的封包數目。</span><span class="sxs-lookup"><span data-stu-id="225b4-118">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="225b4-119">*plStrokePacketData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="225b4-119">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="225b4-120">陣列，其中包含筆觸的封包資料。</span><span class="sxs-lookup"><span data-stu-id="225b4-120">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="225b4-121">*ppCoNtextNodeStrokeAddedTo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="225b4-121">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="225b4-122">筆跡分析器新增筆劃的 [**ICoNtextNode**](icontextnode.md) 。</span><span class="sxs-lookup"><span data-stu-id="225b4-122">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="225b4-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="225b4-123">Return value</span></span>

<span data-ttu-id="225b4-124">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="225b4-124">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="225b4-125">備註</span><span class="sxs-lookup"><span data-stu-id="225b4-125">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="225b4-126">若要避免記憶體流失，請在 *ppCoNtextNodeStrokeAddedTo* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="225b4-126">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="225b4-127">當 *ppCoNtextNodeStrokeAddedTo* 為 **Null** 時，表示呼叫端對方法的傳回值不感興趣。</span><span class="sxs-lookup"><span data-stu-id="225b4-127">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="225b4-128">[**IInkAnalyzer**](iinkanalyzer.md)會將筆劃新增至類型 UnclassifiedInk 的 [**ICoNtextNode**](icontextnode.md) (請參閱) 的 [內容節點類型](context-node-types.md)。</span><span class="sxs-lookup"><span data-stu-id="225b4-128">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="225b4-129">此節點位於根節點的子節點集合中 (請參閱 [**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md) 和 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md) 方法) 。</span><span class="sxs-lookup"><span data-stu-id="225b4-129">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="225b4-130">[**IInkAnalyzer**](iinkanalyzer.md)會將 *lStrokeLCID* 文化特性識別碼指派給筆觸，然後將筆劃新增至筆墨分析器根節點下的第一個 UnclassifiedInk 內容節點，其中包含具有相同文化特性識別碼的筆觸。</span><span class="sxs-lookup"><span data-stu-id="225b4-130">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the *lStrokeLCID* culture identifier to the strokes and adds the strokes to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="225b4-131">如果筆墨分析器沒有具有相同文化特性識別碼的節點，它會在其根節點下建立新的 UnclassifiedInk 內容節點，並將筆劃加入新的 UnclassifiedInk 內容節點。</span><span class="sxs-lookup"><span data-stu-id="225b4-131">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the strokes to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="225b4-132">*plStrokePacketData* 包含所有筆劃的封包資料。</span><span class="sxs-lookup"><span data-stu-id="225b4-132">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="225b4-133">*pStrokePacketDescriptionGuids* 包含 (guid) 的全域唯一識別碼，描述每個筆劃中每個點所包含的封包資料類型。</span><span class="sxs-lookup"><span data-stu-id="225b4-133">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="225b4-134">如需可用的封包屬性完整清單，請參閱 [PacketPropertyGuids 常數](packetpropertyguids-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="225b4-134">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="225b4-135">[**IInkAnalyzer：： AddStrokes 方法**](iinkanalyzer-addstrokes.md)的單一呼叫中只能新增具有相同封包描述的筆劃。</span><span class="sxs-lookup"><span data-stu-id="225b4-135">Only strokes with the same packet descriptions can be added in a single call to [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md).</span></span>

 

<span data-ttu-id="225b4-136">這個方法會將中途區域擴展至區域目前值的聯集，以及加入之筆劃的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="225b4-136">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="225b4-137">如果 [**IInkAnalyzer**](iinkanalyzer.md)已包含與要加入之其中一個筆劃具有相同識別碼的筆劃，則 **IInkAnalyzer** 會傳回 **E \_ INVALIDARG** 的 **HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="225b4-137">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="225b4-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="225b4-138">Requirements</span></span>



| <span data-ttu-id="225b4-139">需求</span><span class="sxs-lookup"><span data-stu-id="225b4-139">Requirement</span></span> | <span data-ttu-id="225b4-140">值</span><span class="sxs-lookup"><span data-stu-id="225b4-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="225b4-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="225b4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="225b4-142">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="225b4-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="225b4-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="225b4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="225b4-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="225b4-144">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="225b4-145">標頭</span><span class="sxs-lookup"><span data-stu-id="225b4-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="225b4-146"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="225b4-146"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="225b4-147">DLL</span><span class="sxs-lookup"><span data-stu-id="225b4-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="225b4-148"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="225b4-148"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="225b4-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="225b4-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="225b4-150">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="225b4-150">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="225b4-151">**IInkAnalyzer：： AddStroke 方法**</span><span class="sxs-lookup"><span data-stu-id="225b4-151">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="225b4-152">**IInkAnalyzer：： AddStrokeForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="225b4-152">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="225b4-153">**IInkAnalyzer：： AddStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="225b4-153">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="225b4-154">**IInkAnalyzer：： RemoveStroke 方法**</span><span class="sxs-lookup"><span data-stu-id="225b4-154">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="225b4-155">**IInkAnalyzer：： RemoveStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="225b4-155">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="225b4-156">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="225b4-156">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

