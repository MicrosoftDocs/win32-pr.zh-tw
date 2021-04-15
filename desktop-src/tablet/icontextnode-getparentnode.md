---
description: 在內容節點樹狀結構中，捕獲此 ICoNtextNode 的父節點。
ms.assetid: 782fd973-f8f3-4902-b8e0-cc5e70a66d28
title: 'ICoNtextNode：： GetParentNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetParentNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 50bba716486910802e91cbe6d3f003d172f1cb29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511680"
---
# <a name="icontextnodegetparentnode-method"></a><span data-ttu-id="90908-103">ICoNtextNode：： GetParentNode 方法</span><span class="sxs-lookup"><span data-stu-id="90908-103">IContextNode::GetParentNode method</span></span>

<span data-ttu-id="90908-104">在內容節點樹狀結構中，捕獲此 [**ICoNtextNode**](icontextnode.md) 的父節點。</span><span class="sxs-lookup"><span data-stu-id="90908-104">Retrieves the parent node of this [**IContextNode**](icontextnode.md) in the context node tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="90908-105">語法</span><span class="sxs-lookup"><span data-stu-id="90908-105">Syntax</span></span>


```C++
HRESULT GetParentNode(
  [out] IContextNode **ppParentContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="90908-106">參數</span><span class="sxs-lookup"><span data-stu-id="90908-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90908-107">*ppParentCoNtextNode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="90908-107">*ppParentContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90908-108">這個 [**ICoNtextNode**](icontextnode.md) 物件的父節點指標。</span><span class="sxs-lookup"><span data-stu-id="90908-108">A pointer to the parent node of this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90908-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="90908-109">Return value</span></span>

<span data-ttu-id="90908-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="90908-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="90908-111">備註</span><span class="sxs-lookup"><span data-stu-id="90908-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="90908-112">若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要使用父內容節點時，請在 *ppParentCoNtextNode* 上呼叫 IUnknown：： Release。</span><span class="sxs-lookup"><span data-stu-id="90908-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppParentContextNode* when you no longer need to use the parent context node.</span></span>

 

<span data-ttu-id="90908-113">如果這是根節點，則 *ppParentCoNtextNode* 參數會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="90908-113">If this is the root node, the *ppParentContextNode* parameter is set to **NULL**.</span></span>

## <a name="examples"></a><span data-ttu-id="90908-114">範例</span><span class="sxs-lookup"><span data-stu-id="90908-114">Examples</span></span>

<span data-ttu-id="90908-115">下列範例顯示 helper 方法，此方法會抓取指定節點的相關資訊，也就是其 *pCoNtextNode* 參數。</span><span class="sxs-lookup"><span data-stu-id="90908-115">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="90908-116">此 helper 方法會傳回下列方法的資訊。</span><span class="sxs-lookup"><span data-stu-id="90908-116">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="90908-117">**ICoNtextNode：： GetId**</span><span class="sxs-lookup"><span data-stu-id="90908-117">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   [<span data-ttu-id="90908-118">**ICoNtextNode：： GetType**</span><span class="sxs-lookup"><span data-stu-id="90908-118">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   [<span data-ttu-id="90908-119">**ICoNtextNode::GetLocation**</span><span class="sxs-lookup"><span data-stu-id="90908-119">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   <span data-ttu-id="90908-120">**ICoNtextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="90908-120">**IContextNode::GetParentNode**</span></span>


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



## <a name="requirements"></a><span data-ttu-id="90908-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="90908-121">Requirements</span></span>



| <span data-ttu-id="90908-122">需求</span><span class="sxs-lookup"><span data-stu-id="90908-122">Requirement</span></span> | <span data-ttu-id="90908-123">值</span><span class="sxs-lookup"><span data-stu-id="90908-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90908-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90908-124">Minimum supported client</span></span><br/> | <span data-ttu-id="90908-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90908-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="90908-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90908-126">Minimum supported server</span></span><br/> | <span data-ttu-id="90908-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="90908-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="90908-128">標頭</span><span class="sxs-lookup"><span data-stu-id="90908-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="90908-129"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="90908-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="90908-130">DLL</span><span class="sxs-lookup"><span data-stu-id="90908-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90908-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90908-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="90908-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90908-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90908-133">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="90908-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="90908-134">**ICoNtextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="90908-134">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="90908-135">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="90908-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

