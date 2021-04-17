---
description: 取得與 ICoNtextNode 物件相關聯的筆劃數目。
ms.assetid: bb3c1cb3-dcf6-4465-b1bc-5c613e9747da
title: 'ICoNtextNode：： GetStrokeCount 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2652168fa2846995aeb17ec23c194f908f22e5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469140"
---
# <a name="icontextnodegetstrokecount-method"></a><span data-ttu-id="029fd-103">ICoNtextNode：： GetStrokeCount 方法</span><span class="sxs-lookup"><span data-stu-id="029fd-103">IContextNode::GetStrokeCount method</span></span>

<span data-ttu-id="029fd-104">取得與 [**ICoNtextNode**](icontextnode.md) 物件相關聯的筆劃數目。</span><span class="sxs-lookup"><span data-stu-id="029fd-104">Gets the number of strokes associated with the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="029fd-105">語法</span><span class="sxs-lookup"><span data-stu-id="029fd-105">Syntax</span></span>


```C++
HRESULT GetStrokeCount(
  [out] ULONG *pulStrokeCount
);
```



## <a name="parameters"></a><span data-ttu-id="029fd-106">參數</span><span class="sxs-lookup"><span data-stu-id="029fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="029fd-107">*pulStrokeCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="029fd-107">*pulStrokeCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="029fd-108">與 [**ICoNtextNode**](icontextnode.md) 物件相關聯的筆劃數目。</span><span class="sxs-lookup"><span data-stu-id="029fd-108">The number of strokes associated with the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="029fd-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="029fd-109">Return value</span></span>

<span data-ttu-id="029fd-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="029fd-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="029fd-111">備註</span><span class="sxs-lookup"><span data-stu-id="029fd-111">Remarks</span></span>

<span data-ttu-id="029fd-112">只有筆墨分葉內容節點有相關聯的筆劃資料 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 。</span><span class="sxs-lookup"><span data-stu-id="029fd-112">Only ink leaf context nodes have associated stroke data (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

## <a name="examples"></a><span data-ttu-id="029fd-113">範例</span><span class="sxs-lookup"><span data-stu-id="029fd-113">Examples</span></span>

<span data-ttu-id="029fd-114">此範例顯示 `ExploreContextNode` 檢查 [**ICoNtextNode**](icontextnode.md)的方法。</span><span class="sxs-lookup"><span data-stu-id="029fd-114">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="029fd-115">方法會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="029fd-115">The method does the following:</span></span>

-   <span data-ttu-id="029fd-116">取得內容節點的型別。</span><span class="sxs-lookup"><span data-stu-id="029fd-116">Gets the context node's type.</span></span>
-   <span data-ttu-id="029fd-117">如果內容節點是未分類的筆墨、分析提示或自訂辨識器節點，則會藉由呼叫 helper 方法來檢查節點類型的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="029fd-117">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="029fd-118">如果節點有子節點，則會呼叫本身來檢查每個子節點。</span><span class="sxs-lookup"><span data-stu-id="029fd-118">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="029fd-119">藉由呼叫 helper 方法，檢查節點的筆劃資料是否為筆墨分葉節點。</span><span class="sxs-lookup"><span data-stu-id="029fd-119">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="029fd-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="029fd-120">Requirements</span></span>



| <span data-ttu-id="029fd-121">需求</span><span class="sxs-lookup"><span data-stu-id="029fd-121">Requirement</span></span> | <span data-ttu-id="029fd-122">值</span><span class="sxs-lookup"><span data-stu-id="029fd-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="029fd-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="029fd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="029fd-124">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="029fd-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="029fd-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="029fd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="029fd-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="029fd-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="029fd-127">標頭</span><span class="sxs-lookup"><span data-stu-id="029fd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="029fd-128"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="029fd-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="029fd-129">DLL</span><span class="sxs-lookup"><span data-stu-id="029fd-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="029fd-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="029fd-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="029fd-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="029fd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="029fd-132">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="029fd-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="029fd-133">**ICoNtextNode::GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="029fd-133">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="029fd-134">**ICoNtextNode::GetStrokeId**</span><span class="sxs-lookup"><span data-stu-id="029fd-134">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="029fd-135">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="029fd-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




