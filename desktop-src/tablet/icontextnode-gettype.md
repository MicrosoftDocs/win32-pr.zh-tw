---
description: 捕獲 ICoNtextNode 物件的型別。
ms.assetid: 285384ce-5cdc-47f5-a1c4-6c6d7f18e215
title: 'ICoNtextNode：： GetType 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 68b657d9acd6f25f7c067e339ec42c6994a34c48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113377"
---
# <a name="icontextnodegettype-method"></a><span data-ttu-id="c6f01-103">ICoNtextNode：： GetType 方法</span><span class="sxs-lookup"><span data-stu-id="c6f01-103">IContextNode::GetType method</span></span>

<span data-ttu-id="c6f01-104">捕獲 [**ICoNtextNode**](icontextnode.md) 物件的型別。</span><span class="sxs-lookup"><span data-stu-id="c6f01-104">Retrieves the type of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6f01-105">語法</span><span class="sxs-lookup"><span data-stu-id="c6f01-105">Syntax</span></span>


```C++
HRESULT GetType(
  [out] GUID *pContextNodeType
);
```



## <a name="parameters"></a><span data-ttu-id="c6f01-106">參數</span><span class="sxs-lookup"><span data-stu-id="c6f01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6f01-107">*pCoNtextNodeType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c6f01-107">*pContextNodeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6f01-108">[**ICoNtextNode**](icontextnode.md)物件的類型。</span><span class="sxs-lookup"><span data-stu-id="c6f01-108">The type of the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6f01-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6f01-109">Return value</span></span>

<span data-ttu-id="c6f01-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="c6f01-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c6f01-111">備註</span><span class="sxs-lookup"><span data-stu-id="c6f01-111">Remarks</span></span>

<span data-ttu-id="c6f01-112">節點的類型會在 [內容節點類型](context-node-types.md) 常數中描述。</span><span class="sxs-lookup"><span data-stu-id="c6f01-112">Types of nodes are described in the [Context Node Types](context-node-types.md) constants.</span></span>

## <a name="examples"></a><span data-ttu-id="c6f01-113">範例</span><span class="sxs-lookup"><span data-stu-id="c6f01-113">Examples</span></span>

<span data-ttu-id="c6f01-114">下列範例顯示 helper 方法，此方法會抓取指定節點的相關資訊，也就是其 *pCoNtextNode* 參數。</span><span class="sxs-lookup"><span data-stu-id="c6f01-114">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="c6f01-115">此 helper 方法會傳回下列方法的資訊。</span><span class="sxs-lookup"><span data-stu-id="c6f01-115">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="c6f01-116">**ICoNtextNode：： GetId**</span><span class="sxs-lookup"><span data-stu-id="c6f01-116">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   <span data-ttu-id="c6f01-117">**ICoNtextNode：： GetType**</span><span class="sxs-lookup"><span data-stu-id="c6f01-117">**IContextNode::GetType**</span></span>
-   [<span data-ttu-id="c6f01-118">**ICoNtextNode::GetLocation**</span><span class="sxs-lookup"><span data-stu-id="c6f01-118">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   [<span data-ttu-id="c6f01-119">**ICoNtextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="c6f01-119">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


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



## <a name="requirements"></a><span data-ttu-id="c6f01-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6f01-120">Requirements</span></span>



| <span data-ttu-id="c6f01-121">需求</span><span class="sxs-lookup"><span data-stu-id="c6f01-121">Requirement</span></span> | <span data-ttu-id="c6f01-122">值</span><span class="sxs-lookup"><span data-stu-id="c6f01-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f01-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6f01-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c6f01-124">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6f01-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c6f01-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6f01-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c6f01-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="c6f01-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c6f01-127">標頭</span><span class="sxs-lookup"><span data-stu-id="c6f01-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6f01-128"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="c6f01-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c6f01-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c6f01-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6f01-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6f01-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c6f01-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6f01-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6f01-132">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="c6f01-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c6f01-133">內容節點類型</span><span class="sxs-lookup"><span data-stu-id="c6f01-133">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="c6f01-134">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="c6f01-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




