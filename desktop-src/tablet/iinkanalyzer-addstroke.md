---
description: 將單一筆劃的筆觸資料新增至 IInkAnalyzer，並將使用中輸入執行緒的文化特性識別碼指派給筆劃。
ms.assetid: 0e603e5a-d722-4ab8-bc59-605e131c863b
title: 'IInkAnalyzer：： AddStroke 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc946e7975772eb7be6fff54d01bb1a6dae8ebe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191412"
---
# <a name="iinkanalyzeraddstroke-method"></a><span data-ttu-id="a1e2c-103">IInkAnalyzer：： AddStroke 方法</span><span class="sxs-lookup"><span data-stu-id="a1e2c-103">IInkAnalyzer::AddStroke method</span></span>

<span data-ttu-id="a1e2c-104">將單一筆劃的筆觸資料新增至 [**IInkAnalyzer**](iinkanalyzer.md) ，並將使用中輸入執行緒的文化特性識別碼指派給筆劃。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-104">Adds stroke data for a single stroke to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the active input thread's culture identifier to the stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1e2c-105">語法</span><span class="sxs-lookup"><span data-stu-id="a1e2c-105">Syntax</span></span>


```C++
HRESULT AddStroke(
  [in]  LONG         lStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="a1e2c-106">參數</span><span class="sxs-lookup"><span data-stu-id="a1e2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1e2c-107">*lStrokeId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1e2c-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1e2c-108">要加入之筆劃的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="a1e2c-109">*ulStrokePacketDataCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1e2c-109">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1e2c-110">筆劃中的封包數目。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-110">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="a1e2c-111">*plStrokePacketData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1e2c-111">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1e2c-112">陣列，其中包含筆劃的封包資料。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-112">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="a1e2c-113">*ulStrokePacketDescriptionCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1e2c-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1e2c-114">每個封包中的封包屬性數目。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-114">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="a1e2c-115">*pStrokePacketDescriptionGuids* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1e2c-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1e2c-116">陣列，包含封包屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="a1e2c-117">*ppCoNtextNodeStrokeAddedTo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a1e2c-117">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1e2c-118">[**IInkAnalyzer**](iinkanalyzer.md)加入筆劃之 [**ICoNtextNode**](icontextnode.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-118">A pointer to the [**IContextNode**](icontextnode.md) to which the [**IInkAnalyzer**](iinkanalyzer.md) added the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1e2c-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1e2c-119">Return value</span></span>

<span data-ttu-id="a1e2c-120">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a1e2c-121">備註</span><span class="sxs-lookup"><span data-stu-id="a1e2c-121">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a1e2c-122">若要避免記憶體流失，請在 *ppCoNtextNodeStrokeAddedTo* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-122">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="a1e2c-123">當 *ppCoNtextNodeStrokeAddedTo* 為 **Null** 時，表示呼叫端對方法的傳回值不感興趣。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-123">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="a1e2c-124">[**IInkAnalyzer**](iinkanalyzer.md)會將筆劃新增至類型 UnclassifiedInk 的 [**ICoNtextNode**](icontextnode.md) (請參閱) 的 [內容節點類型](context-node-types.md)。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-124">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="a1e2c-125">此節點位於根節點的子節點集合中 (請參閱 [**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md) 和 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md) 方法) 。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-125">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="a1e2c-126">[**IInkAnalyzer**](iinkanalyzer.md)會將使用中輸入執行緒的文化特性識別碼指派給筆劃，然後將筆劃加入至筆墨分析器根節點下的第一個 UnclassifiedInk 內容節點，其中包含具有相同文化特性識別碼的筆觸。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-126">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the stroke and adds the stroke to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="a1e2c-127">如果筆墨分析器沒有具有相同文化特性識別碼的節點，它會在其根節點下建立新的 UnclassifiedInk 內容節點，並將筆劃加入新的 UnclassifiedInk 內容節點。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-127">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the stroke to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="a1e2c-128">*plStrokePacketData* 包含筆劃中所有點的封包資料。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-128">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="a1e2c-129">*pStrokePacketDescriptionGuids* 包含 (guid) 的全域唯一識別碼，描述筆劃中每個點所包含的封包資料類型。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-129">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="a1e2c-130">如需可用的封包屬性完整清單，請參閱 [PacketPropertyGuids 常數](packetpropertyguids-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-130">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="a1e2c-131">這個方法會將中途區域展開至區域目前值的聯集，以及已加入筆劃的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-131">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="a1e2c-132">如果 [**IInkAnalyzer**](iinkanalyzer.md)已包含具有相同筆觸識別碼的筆劃，則 **IInkAnalyzer** 會傳回 **E \_ INVALIDARG** 的 **HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="a1e2c-132">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same stroke identifier, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1e2c-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1e2c-133">Requirements</span></span>



| <span data-ttu-id="a1e2c-134">需求</span><span class="sxs-lookup"><span data-stu-id="a1e2c-134">Requirement</span></span> | <span data-ttu-id="a1e2c-135">值</span><span class="sxs-lookup"><span data-stu-id="a1e2c-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e2c-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1e2c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a1e2c-137">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1e2c-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a1e2c-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1e2c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a1e2c-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="a1e2c-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a1e2c-140">標頭</span><span class="sxs-lookup"><span data-stu-id="a1e2c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1e2c-141"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="a1e2c-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a1e2c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a1e2c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1e2c-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1e2c-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a1e2c-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1e2c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1e2c-145">**InkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a1e2c-145">**InkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a1e2c-146">**IInkAnalyzer：： AddStrokeForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="a1e2c-146">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="a1e2c-147">**IInkAnalyzer：： AddStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="a1e2c-147">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="a1e2c-148">**IInkAnalyzer：： AddStrokesForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="a1e2c-148">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="a1e2c-149">**IInkAnalyzer：： RemoveStroke 方法**</span><span class="sxs-lookup"><span data-stu-id="a1e2c-149">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="a1e2c-150">**IInkAnalyzer：： RemoveStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="a1e2c-150">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="a1e2c-151">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="a1e2c-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

