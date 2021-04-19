---
description: 抓取包含指定筆劃之指定型別的所有 ICoNtextNode 物件。
ms.assetid: c674a03b-841c-4a9c-8268-302bc4038934
title: 'IInkAnalyzer：： FindNodesOfTypeForStrokes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dd98c72007a69521506e2be21ad10edeb46df27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970823"
---
# <a name="iinkanalyzerfindnodesoftypeforstrokes-method"></a><span data-ttu-id="c28bb-103">IInkAnalyzer：： FindNodesOfTypeForStrokes 方法</span><span class="sxs-lookup"><span data-stu-id="c28bb-103">IInkAnalyzer::FindNodesOfTypeForStrokes method</span></span>

<span data-ttu-id="c28bb-104">抓取包含指定筆劃之指定型別的所有 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="c28bb-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type that contain the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c28bb-105">語法</span><span class="sxs-lookup"><span data-stu-id="c28bb-105">Syntax</span></span>


```C++
HRESULT FindNodesOfTypeForStrokes(
  [in]  const GUID          *pNodeType,
  [in]        ULONG         ulStrokeIdsCount,
  [in]        LONG          *plStrokeIds,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="c28bb-106">參數</span><span class="sxs-lookup"><span data-stu-id="c28bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c28bb-107">*pNodeType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c28bb-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c28bb-108"> (GUID) 的全域唯一識別碼，可指定節點類型。</span><span class="sxs-lookup"><span data-stu-id="c28bb-108">The globally unique identifier (GUID) that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="c28bb-109">*ulStrokeIdsCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c28bb-109">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c28bb-110">傳入的筆觸識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="c28bb-110">The number of stroke identifiers passed in.</span></span>

</dd> <dt>

<span data-ttu-id="c28bb-111">*plStrokeIds* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c28bb-111">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c28bb-112">筆觸識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="c28bb-112">An array of the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="c28bb-113">*ppCoNtextNodesFound* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c28bb-113">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c28bb-114">[**ICoNtextNode**](icontextnode.md)物件的集合，其中包含 *pNodeType* 類型的所有節點，這些節點包含 *plStrokeIds* 陣列中具有識別碼的筆劃。</span><span class="sxs-lookup"><span data-stu-id="c28bb-114">The collection of [**IContextNode**](icontextnode.md) objects that contain all the nodes of type *pNodeType* that contain the strokes with identifiers in the *plStrokeIds* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c28bb-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c28bb-115">Return value</span></span>

<span data-ttu-id="c28bb-116">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="c28bb-116">For a description of return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c28bb-117">備註</span><span class="sxs-lookup"><span data-stu-id="c28bb-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c28bb-118">若要避免記憶體流失，請在 ppCoNtextNodesFound 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （ \* 當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="c28bb-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="c28bb-119">*PNodeType* 屬性必須包含來自 [內容節點類型](context-node-types.md)常數的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c28bb-119">The *pNodeType* property must contain a GUID from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="c28bb-120">如果指定的節點類型不是分葉節點，但其中一個節點的下階參考筆劃集合中的筆劃，則該節點會加入至所傳回的集合。</span><span class="sxs-lookup"><span data-stu-id="c28bb-120">If the specified node type is not a leaf node, but one of the node's descendants references a stroke in the strokes collection, that node is added to the collection that is returned.</span></span>

<span data-ttu-id="c28bb-121">如果 [**IInkAnalyzer**](iinkanalyzer.md) 未包含這類 [**ICoNtextNode**](icontextnode.md)，則會傳回空的 [**ICoNtextNodes**](icontextnodes.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="c28bb-121">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="c28bb-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c28bb-122">Requirements</span></span>



| <span data-ttu-id="c28bb-123">需求</span><span class="sxs-lookup"><span data-stu-id="c28bb-123">Requirement</span></span> | <span data-ttu-id="c28bb-124">值</span><span class="sxs-lookup"><span data-stu-id="c28bb-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c28bb-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c28bb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c28bb-126">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c28bb-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c28bb-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c28bb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c28bb-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="c28bb-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c28bb-129">標頭</span><span class="sxs-lookup"><span data-stu-id="c28bb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c28bb-130"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="c28bb-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c28bb-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c28bb-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c28bb-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c28bb-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c28bb-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c28bb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c28bb-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="c28bb-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c28bb-135">**IInkAnalyzer：： FindInkLeafNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="c28bb-135">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="c28bb-136">**IInkAnalyzer：： FindInkLeafNodesForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="c28bb-136">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="c28bb-137">**IInkAnalyzer：： FindLeafNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="c28bb-137">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="c28bb-138">**IInkAnalyzer：： FindNode 方法**</span><span class="sxs-lookup"><span data-stu-id="c28bb-138">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="c28bb-139">**IInkAnalyzer：： FindNodesOfType 方法**</span><span class="sxs-lookup"><span data-stu-id="c28bb-139">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="c28bb-140">**IInkAnalyzer：： FindNodesOfTypeInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="c28bb-140">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="c28bb-141">**IInkAnalyzer：： FindNodesWithCallBack 方法**</span><span class="sxs-lookup"><span data-stu-id="c28bb-141">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="c28bb-142">**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="c28bb-142">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="c28bb-143">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="c28bb-143">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

