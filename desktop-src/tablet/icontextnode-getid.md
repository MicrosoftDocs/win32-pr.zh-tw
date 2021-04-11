---
description: 捕獲 ICoNtextNode 物件的識別碼。
ms.assetid: 7578bcc1-7c69-45fc-b3c2-7350ce4df99c
title: 'ICoNtextNode：： GetId 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ef316111c7464bac0339a4888b887bc5cf20b93f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848091"
---
# <a name="icontextnodegetid-method"></a><span data-ttu-id="88b45-103">ICoNtextNode：： GetId 方法</span><span class="sxs-lookup"><span data-stu-id="88b45-103">IContextNode::GetId method</span></span>

<span data-ttu-id="88b45-104">捕獲 [**ICoNtextNode**](icontextnode.md) 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="88b45-104">Retrieves the identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="88b45-105">語法</span><span class="sxs-lookup"><span data-stu-id="88b45-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] GUID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="88b45-106">參數</span><span class="sxs-lookup"><span data-stu-id="88b45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88b45-107">*pId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="88b45-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88b45-108">[**ICoNtextNode**](icontextnode.md)物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="88b45-108">The identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88b45-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="88b45-109">Return value</span></span>

<span data-ttu-id="88b45-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="88b45-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="88b45-111">備註</span><span class="sxs-lookup"><span data-stu-id="88b45-111">Remarks</span></span>

<span data-ttu-id="88b45-112">筆墨分析器會將唯一識別碼指派給它所建立的所有內容節點。</span><span class="sxs-lookup"><span data-stu-id="88b45-112">The ink analyzer assigns a unique identifier to all context nodes it creates.</span></span> <span data-ttu-id="88b45-113">在筆跡分析期間，筆墨分析器可能會變更內容節點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="88b45-113">During ink analysis, the ink analyzer may change the identifier for a context node.</span></span> <span data-ttu-id="88b45-114">例如，筆跡分析器可以將一個單位元組點重新分類為兩個單位元組點，然後將原始識別碼指派給另一個，並將新的識別碼指派給另一個。</span><span class="sxs-lookup"><span data-stu-id="88b45-114">For example, the ink analyzer may reclassify one word node as two word nodes and then assign the original identifier to one and a new identifier to the other.</span></span> <span data-ttu-id="88b45-115">或者，筆跡分析器可以將兩個單位元組點重新分類為一個單位元組點，並將其中一個原始識別碼指派給新的單位元組點。</span><span class="sxs-lookup"><span data-stu-id="88b45-115">Or, the ink analyzer may reclassify two word nodes as one word node and assign one of the original identifiers to the new word node.</span></span>

## <a name="examples"></a><span data-ttu-id="88b45-116">範例</span><span class="sxs-lookup"><span data-stu-id="88b45-116">Examples</span></span>

<span data-ttu-id="88b45-117">下列範例顯示 helper 方法，此方法會抓取指定節點的相關資訊，也就是其 *pCoNtextNode* 參數。</span><span class="sxs-lookup"><span data-stu-id="88b45-117">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="88b45-118">此 helper 方法會傳回下列方法的資訊。</span><span class="sxs-lookup"><span data-stu-id="88b45-118">This helper method returns information from the following methods.</span></span>

-   <span data-ttu-id="88b45-119">**ICoNtextNode：： GetId**</span><span class="sxs-lookup"><span data-stu-id="88b45-119">**IContextNode::GetId**</span></span>
-   [<span data-ttu-id="88b45-120">**ICoNtextNode：： GetType**</span><span class="sxs-lookup"><span data-stu-id="88b45-120">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   [<span data-ttu-id="88b45-121">**ICoNtextNode::GetLocation**</span><span class="sxs-lookup"><span data-stu-id="88b45-121">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   [<span data-ttu-id="88b45-122">**ICoNtextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="88b45-122">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


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



## <a name="requirements"></a><span data-ttu-id="88b45-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="88b45-123">Requirements</span></span>



| <span data-ttu-id="88b45-124">需求</span><span class="sxs-lookup"><span data-stu-id="88b45-124">Requirement</span></span> | <span data-ttu-id="88b45-125">值</span><span class="sxs-lookup"><span data-stu-id="88b45-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b45-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88b45-126">Minimum supported client</span></span><br/> | <span data-ttu-id="88b45-127">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88b45-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="88b45-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88b45-128">Minimum supported server</span></span><br/> | <span data-ttu-id="88b45-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="88b45-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="88b45-130">標頭</span><span class="sxs-lookup"><span data-stu-id="88b45-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="88b45-131"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="88b45-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="88b45-132">DLL</span><span class="sxs-lookup"><span data-stu-id="88b45-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88b45-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88b45-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="88b45-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88b45-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88b45-135">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="88b45-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="88b45-136">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="88b45-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




