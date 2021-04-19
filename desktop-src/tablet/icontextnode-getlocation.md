---
description: 抓取 ICoNtextNode 物件的位置和大小。
ms.assetid: 40787a9b-1017-4209-aec8-09b7332bfa8a
title: 'ICoNtextNode：： GetLocation 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13366442399961eaba7a411b1b3c87171f0879b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970824"
---
# <a name="icontextnodegetlocation-method"></a><span data-ttu-id="c94e3-103">ICoNtextNode：： GetLocation 方法</span><span class="sxs-lookup"><span data-stu-id="c94e3-103">IContextNode::GetLocation method</span></span>

<span data-ttu-id="c94e3-104">抓取 [**ICoNtextNode**](icontextnode.md) 物件的位置和大小。</span><span class="sxs-lookup"><span data-stu-id="c94e3-104">Retrieves the position and size of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c94e3-105">語法</span><span class="sxs-lookup"><span data-stu-id="c94e3-105">Syntax</span></span>


```C++
HRESULT GetLocation(
  [out] IAnalysisRegion **ppIAnalysisRegion
);
```



## <a name="parameters"></a><span data-ttu-id="c94e3-106">參數</span><span class="sxs-lookup"><span data-stu-id="c94e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c94e3-107">*ppIAnalysisRegion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c94e3-107">*ppIAnalysisRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c94e3-108">[**ICoNtextNode**](icontextnode.md)物件之位置和大小的指標。</span><span class="sxs-lookup"><span data-stu-id="c94e3-108">A pointer to the position and size of the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c94e3-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c94e3-109">Return value</span></span>

<span data-ttu-id="c94e3-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="c94e3-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c94e3-111">備註</span><span class="sxs-lookup"><span data-stu-id="c94e3-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c94e3-112">若要避免記憶體流失，請在 ppIAnalysisRegion 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （ \* 當您不再需要流量分析區域時）。</span><span class="sxs-lookup"><span data-stu-id="c94e3-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppIAnalysisRegion* when you no longer need to use the analysis region.</span></span>

 

<span data-ttu-id="c94e3-113">容器節點的位置是藉由尋找所有分葉位置的聯集來決定。</span><span class="sxs-lookup"><span data-stu-id="c94e3-113">The location for a container node is determined by finding the union of all the leaf's locations.</span></span> <span data-ttu-id="c94e3-114">筆跡分葉節點的位置是藉由尋找相關聯筆劃之周框方塊的聯集來決定。</span><span class="sxs-lookup"><span data-stu-id="c94e3-114">The location for an ink leaf node is determined by finding the union of the bounding box of the associated strokes.</span></span> <span data-ttu-id="c94e3-115">當建立節點時，會設定非筆墨分葉節點的位置，並且可使用 [**ICoNtextNode：： SetLocation**](icontextnode-setlocation.md)進行更新。</span><span class="sxs-lookup"><span data-stu-id="c94e3-115">The location for a non-ink leaf node is set when the node is created and can be updated using [**IContextNode::SetLocation**](icontextnode-setlocation.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c94e3-116">範例</span><span class="sxs-lookup"><span data-stu-id="c94e3-116">Examples</span></span>

<span data-ttu-id="c94e3-117">下列範例顯示 helper 方法，此方法會抓取指定節點的相關資訊，也就是其 *pCoNtextNode* 參數。</span><span class="sxs-lookup"><span data-stu-id="c94e3-117">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="c94e3-118">此 helper 方法會傳回下列方法的資訊。</span><span class="sxs-lookup"><span data-stu-id="c94e3-118">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="c94e3-119">**ICoNtextNode：： GetId**</span><span class="sxs-lookup"><span data-stu-id="c94e3-119">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   [<span data-ttu-id="c94e3-120">**ICoNtextNode：： GetType**</span><span class="sxs-lookup"><span data-stu-id="c94e3-120">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   <span data-ttu-id="c94e3-121">**ICoNtextNode::GetLocation**</span><span class="sxs-lookup"><span data-stu-id="c94e3-121">**IContextNode::GetLocation**</span></span>
-   [<span data-ttu-id="c94e3-122">**ICoNtextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="c94e3-122">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


```C++
// Helper method for collecting information about a context node.
HRESULT CMyClass::GetNodeInformation(
    IContextNode *pContextNode,
    GUID *pNodeIdentifier,
    GUID *pContextNodeType,
    IAnalysisRegion **ppAnalysisRegion,
    IContextNode **ppParentNode,
    IContextNodes **ppSubNodes)
{
    // Get the identifier of the context node.
    HRESULT hr = pContextNode->GetId(pNodeIdentifier);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the type identifier for the context node.
    hr = pContextNode->GetType(pContextNodeType);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the location of the context node.
    hr = pContextNode->GetLocation(ppAnalysisRegion);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the parent node of the context node.
    hr = pContextNode->GetParentNode(ppParentNode);

    if (FAILED(hr))
    {
        if ((*ppAnalysisRegion) != NULL)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        return hr;
    }

    // Get the subnodes of the context node.
    hr = pContextNode->GetSubNodes(ppSubNodes);

    if (FAILED(hr))
    {
        if (*ppAnalysisRegion)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        if (*ppParentNode)
        {
            (*ppParentNode)->Release();
            (*ppParentNode) = NULL;
        }
        return hr;
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="c94e3-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c94e3-123">Requirements</span></span>



| <span data-ttu-id="c94e3-124">需求</span><span class="sxs-lookup"><span data-stu-id="c94e3-124">Requirement</span></span> | <span data-ttu-id="c94e3-125">值</span><span class="sxs-lookup"><span data-stu-id="c94e3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c94e3-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c94e3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c94e3-127">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c94e3-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c94e3-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c94e3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c94e3-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="c94e3-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c94e3-130">標頭</span><span class="sxs-lookup"><span data-stu-id="c94e3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c94e3-131"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="c94e3-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c94e3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c94e3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c94e3-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c94e3-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c94e3-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c94e3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c94e3-135">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="c94e3-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c94e3-136">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="c94e3-136">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="c94e3-137">**ICoNtextNode::SetLocation**</span><span class="sxs-lookup"><span data-stu-id="c94e3-137">**IContextNode::SetLocation**</span></span>](icontextnode-setlocation.md)
</dt> <dt>

[<span data-ttu-id="c94e3-138">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="c94e3-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

