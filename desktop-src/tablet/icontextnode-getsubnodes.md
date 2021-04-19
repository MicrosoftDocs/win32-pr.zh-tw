---
description: 取得 ICoNtextNode 物件的直接子節點。
ms.assetid: 50ce2fa4-031e-42e9-8e47-c0d3c2d2b4df
title: 'ICoNtextNode：： GetSubNodes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetSubNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5c0526ca4a5b4db355c1f895a44ebbf634cb8bc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966725"
---
# <a name="icontextnodegetsubnodes-method"></a><span data-ttu-id="6c536-103">ICoNtextNode：： GetSubNodes 方法</span><span class="sxs-lookup"><span data-stu-id="6c536-103">IContextNode::GetSubNodes method</span></span>

<span data-ttu-id="6c536-104">取得 [**ICoNtextNode**](icontextnode.md) 物件的直接子節點。</span><span class="sxs-lookup"><span data-stu-id="6c536-104">Gets the direct child nodes of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c536-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c536-105">Syntax</span></span>


```C++
HRESULT GetSubNodes(
  [out] IContextNodes **ppSubContextNodes
);
```



## <a name="parameters"></a><span data-ttu-id="6c536-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c536-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c536-107">*ppSubCoNtextNodes* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6c536-107">*ppSubContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c536-108">[**ICoNtextNode**](icontextnode.md)物件的集合，這些物件是這個 **ICoNtextNode** 的直接子節點。</span><span class="sxs-lookup"><span data-stu-id="6c536-108">A collection of the [**IContextNode**](icontextnode.md) objects that are direct child nodes of this **IContextNode**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c536-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c536-109">Return value</span></span>

<span data-ttu-id="6c536-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="6c536-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6c536-111">備註</span><span class="sxs-lookup"><span data-stu-id="6c536-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="6c536-112">若要避免記憶體流失，當您不再需要使用子節點的集合時，請在 ppSubCoNtextNodes 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \*  。</span><span class="sxs-lookup"><span data-stu-id="6c536-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppSubContextNodes* when you no longer need to use the collection of subnodes.</span></span>

 

<span data-ttu-id="6c536-113">這只會傳回直接子節點，而不會傳回所有子系節點。</span><span class="sxs-lookup"><span data-stu-id="6c536-113">This returns only the direct child nodes, not all of the descendant nodes.</span></span>

## <a name="examples"></a><span data-ttu-id="6c536-114">範例</span><span class="sxs-lookup"><span data-stu-id="6c536-114">Examples</span></span>

<span data-ttu-id="6c536-115">此範例顯示 `ExploreContextNode` 檢查 [**ICoNtextNode**](icontextnode.md)的方法。</span><span class="sxs-lookup"><span data-stu-id="6c536-115">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="6c536-116">方法會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="6c536-116">The method does the following:</span></span>

-   <span data-ttu-id="6c536-117">取得內容節點的型別。</span><span class="sxs-lookup"><span data-stu-id="6c536-117">Gets the context node's type.</span></span>
-   <span data-ttu-id="6c536-118">如果內容節點是未分類的筆墨、分析提示或自訂辨識器節點，則會藉由呼叫 helper 方法來檢查節點類型的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="6c536-118">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="6c536-119">如果節點有子節點，則會呼叫本身來檢查每個子節點。</span><span class="sxs-lookup"><span data-stu-id="6c536-119">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="6c536-120">藉由呼叫 helper 方法，檢查節點的筆劃資料是否為筆墨分葉節點。</span><span class="sxs-lookup"><span data-stu-id="6c536-120">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="6c536-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c536-121">Requirements</span></span>



| <span data-ttu-id="6c536-122">需求</span><span class="sxs-lookup"><span data-stu-id="6c536-122">Requirement</span></span> | <span data-ttu-id="6c536-123">值</span><span class="sxs-lookup"><span data-stu-id="6c536-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c536-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c536-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6c536-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c536-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6c536-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c536-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6c536-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="6c536-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6c536-128">標頭</span><span class="sxs-lookup"><span data-stu-id="6c536-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c536-129"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="6c536-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6c536-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6c536-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c536-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c536-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6c536-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c536-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c536-133">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="6c536-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="6c536-134">**ICoNtextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="6c536-134">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="6c536-135">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="6c536-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

