---
description: 將筆劃資料從此 ICoNtextNode 移動到指定的 ICoNtextNode。
ms.assetid: 583f2de9-d32e-4177-83d1-4abbd0f9f960
title: 'ICoNtextNode：： ReparentStrokeByIdToNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ReparentStrokeByIdToNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3984153a0551de999563b8775ceb5acba1696e39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986359"
---
# <a name="icontextnodereparentstrokebyidtonode-method"></a><span data-ttu-id="b8f49-103">ICoNtextNode：： ReparentStrokeByIdToNode 方法</span><span class="sxs-lookup"><span data-stu-id="b8f49-103">IContextNode::ReparentStrokeByIdToNode method</span></span>

<span data-ttu-id="b8f49-104">將筆劃資料從此 [**ICoNtextNode**](icontextnode.md) 移動到指定的 **ICoNtextNode**。</span><span class="sxs-lookup"><span data-stu-id="b8f49-104">Moves stroke data from this [**IContextNode**](icontextnode.md) to the specified **IContextNode**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8f49-105">語法</span><span class="sxs-lookup"><span data-stu-id="b8f49-105">Syntax</span></span>


```C++
HRESULT ReparentStrokeByIdToNode(
  [in] LONG         lStrokeId,
  [in] IContextNode *pContextNodeDestination
);
```



## <a name="parameters"></a><span data-ttu-id="b8f49-106">參數</span><span class="sxs-lookup"><span data-stu-id="b8f49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8f49-107">*lStrokeId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8f49-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-108">要移動之筆劃的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8f49-108">The identifier of the stroke to move.</span></span>

</dd> <dt>

<span data-ttu-id="b8f49-109">*pCoNtextNodeDestination* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8f49-109">*pContextNodeDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8f49-110">要移動筆劃資料的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="b8f49-110">The [**IContextNode**](icontextnode.md) object to which to move the stroke data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8f49-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8f49-111">Return value</span></span>

<span data-ttu-id="b8f49-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="b8f49-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b8f49-113">備註</span><span class="sxs-lookup"><span data-stu-id="b8f49-113">Remarks</span></span>

<span data-ttu-id="b8f49-114">指定的 [**ICoNtextNode**](icontextnode.md) 物件必須是 [內容節點類型](context-node-types.md) 常數的下列其中一種類型： **InkWord**、 **InkDrawing**、 **InkBullet** 或 **UnclassifiedInk**。</span><span class="sxs-lookup"><span data-stu-id="b8f49-114">The specified [**IContextNode**](icontextnode.md) object must be one of the following types from the [Context Node Types](context-node-types.md) constants: **InkWord**, **InkDrawing**, **InkBullet**, or **UnclassifiedInk**.</span></span> <span data-ttu-id="b8f49-115">嘗試將筆劃移至任何其他類型的 **ICoNtextNode** 物件時，會產生 **E \_ INVALIDARG** 的傳回值。</span><span class="sxs-lookup"><span data-stu-id="b8f49-115">Attempting to move a stroke to any other type of **IContextNode** object results in a return value of **E\_INVALIDARG**.</span></span>

<span data-ttu-id="b8f49-116">您可以從任何 [**ICoNtextNode**](icontextnode.md) 物件呼叫這個方法，包括非筆墨分葉 **ICoNtextNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="b8f49-116">This method can be called from any [**IContextNode**](icontextnode.md) object, including non-ink leaf **IContextNode** objects.</span></span> <span data-ttu-id="b8f49-117">指定的筆劃必須由這個 **ICoNtextNode** 物件的其中一個下階參考，否則會傳回 **E \_ INVALIDARG** 。</span><span class="sxs-lookup"><span data-stu-id="b8f49-117">The specified stroke must be referenced by one of the descendants of this **IContextNode** object or **E\_INVALIDARG** is returned.</span></span>

<span data-ttu-id="b8f49-118">如果確認了此 [**ICoNtextNode**](icontextnode.md)或 *PCoNtextNodeDestination* 中的 **ICoNtextNode** ，則會傳回 **E \_ INVALIDARG** (請參閱 [**ICoNtextNode：： IsConfirmed**](icontextnode-isconfirmed.md)) 。</span><span class="sxs-lookup"><span data-stu-id="b8f49-118">If either this [**IContextNode**](icontextnode.md) or the **IContextNode** in *pContextNodeDestination* is confirmed, **E\_INVALIDARG** is returned (see [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)).</span></span>

<span data-ttu-id="b8f49-119">筆墨分析器不會從結果樹狀結構中刪除空的內容節點，以回應這個方法。</span><span class="sxs-lookup"><span data-stu-id="b8f49-119">The ink analyzer does not delete empty context nodes from its results tree in response to this method.</span></span>

-   <span data-ttu-id="b8f49-120">未參考任何筆觸資料的筆墨分葉節點是空的節點。</span><span class="sxs-lookup"><span data-stu-id="b8f49-120">An ink leaf node that does not reference any stroke data is an empty node.</span></span>
-   <span data-ttu-id="b8f49-121">未參考任何子節點的容器節點是空的節點。</span><span class="sxs-lookup"><span data-stu-id="b8f49-121">A container node that does not reference any child nodes is an empty node.</span></span>

<span data-ttu-id="b8f49-122">空白節點會在筆跡分析作業期間于樹狀結構中產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="b8f49-122">An empty node generates errors if it is in the tree during an ink analysis operation.</span></span> <span data-ttu-id="b8f49-123">若要從筆墨分析器的樹狀結構中移除節點，請呼叫父節點的 [**ICoNtextNode：:D eletesubnode**](icontextnode-deletesubnode.md) 方法 (查看 [**ICoNtextNode：： GetParentNode**](icontextnode-getparentnode.md)) 。</span><span class="sxs-lookup"><span data-stu-id="b8f49-123">To remove a node from the ink analyzer's tree, call the parent node's [**IContextNode::DeleteSubNode**](icontextnode-deletesubnode.md) method (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8f49-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8f49-124">Requirements</span></span>



| <span data-ttu-id="b8f49-125">需求</span><span class="sxs-lookup"><span data-stu-id="b8f49-125">Requirement</span></span> | <span data-ttu-id="b8f49-126">值</span><span class="sxs-lookup"><span data-stu-id="b8f49-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8f49-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8f49-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b8f49-128">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8f49-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b8f49-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8f49-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b8f49-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="b8f49-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b8f49-131">標頭</span><span class="sxs-lookup"><span data-stu-id="b8f49-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8f49-132"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="b8f49-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b8f49-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b8f49-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8f49-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8f49-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b8f49-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8f49-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f49-136">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="b8f49-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b8f49-137">**ICoNtextNode::SetStrokes**</span><span class="sxs-lookup"><span data-stu-id="b8f49-137">**IContextNode::SetStrokes**</span></span>](icontextnode-setstrokes.md)
</dt> <dt>

[<span data-ttu-id="b8f49-138">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="b8f49-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




