---
description: 在此集合中的指定索引處，抓取 ICoNtextNode 物件。
ms.assetid: 4b266512-9e58-43d2-8430-68310230fc27
title: 'ICoNtextNodes：： GetCoNtextNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.GetContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ec907fdcac5a1ed18cca54c79a876959868f2ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469136"
---
# <a name="icontextnodesgetcontextnode-method"></a><span data-ttu-id="367a9-103">ICoNtextNodes：： GetCoNtextNode 方法</span><span class="sxs-lookup"><span data-stu-id="367a9-103">IContextNodes::GetContextNode method</span></span>

<span data-ttu-id="367a9-104">在此集合中的指定索引處，抓取 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="367a9-104">Retrieves the [**IContextNode**](icontextnode.md) object at the specified index within this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="367a9-105">語法</span><span class="sxs-lookup"><span data-stu-id="367a9-105">Syntax</span></span>


```C++
HRESULT GetContextNode(
  [in]  ULONG        ulIndex,
  [out] IContextNode **ppContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="367a9-106">參數</span><span class="sxs-lookup"><span data-stu-id="367a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="367a9-107">*ulIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="367a9-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="367a9-108">要取得之 [**ICoNtextNode**](icontextnode.md) 物件的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="367a9-108">The zero-based index of the [**IContextNode**](icontextnode.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="367a9-109">*ppCoNtextNode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="367a9-109">*ppContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="367a9-110">指定之索引處所參考 [**ICoNtextNode**](icontextnode.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="367a9-110">Pointer to the [**IContextNode**](icontextnode.md) referenced at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="367a9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="367a9-111">Return value</span></span>

<span data-ttu-id="367a9-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="367a9-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="367a9-113">備註</span><span class="sxs-lookup"><span data-stu-id="367a9-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="367a9-114">若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要使用內容節點時，請在 *ppCoNtextNode* 上呼叫 IUnknown：： Release。</span><span class="sxs-lookup"><span data-stu-id="367a9-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNode* when you no longer need to use the context node.</span></span>

 

## <a name="examples"></a><span data-ttu-id="367a9-115">範例</span><span class="sxs-lookup"><span data-stu-id="367a9-115">Examples</span></span>

<span data-ttu-id="367a9-116">此範例顯示 `ExploreContextNode` 檢查 [**ICoNtextNode**](icontextnode.md)的方法。</span><span class="sxs-lookup"><span data-stu-id="367a9-116">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="367a9-117">方法會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="367a9-117">The method does the following:</span></span>

-   <span data-ttu-id="367a9-118">取得內容節點的型別。</span><span class="sxs-lookup"><span data-stu-id="367a9-118">Gets the context node's type.</span></span>
-   <span data-ttu-id="367a9-119">如果內容節點是未分類的筆墨、分析提示或自訂辨識器節點，則會藉由呼叫 helper 方法來檢查節點類型的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="367a9-119">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="367a9-120">如果節點有子節點，則會呼叫本身來檢查每個子節點。</span><span class="sxs-lookup"><span data-stu-id="367a9-120">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="367a9-121">藉由呼叫 helper 方法，檢查節點的筆劃資料是否為筆墨分葉節點。</span><span class="sxs-lookup"><span data-stu-id="367a9-121">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="367a9-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="367a9-122">Requirements</span></span>



| <span data-ttu-id="367a9-123">需求</span><span class="sxs-lookup"><span data-stu-id="367a9-123">Requirement</span></span> | <span data-ttu-id="367a9-124">值</span><span class="sxs-lookup"><span data-stu-id="367a9-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="367a9-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="367a9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="367a9-126">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="367a9-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="367a9-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="367a9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="367a9-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="367a9-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="367a9-129">標頭</span><span class="sxs-lookup"><span data-stu-id="367a9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="367a9-130"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="367a9-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="367a9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="367a9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="367a9-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="367a9-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="367a9-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="367a9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="367a9-134">**ICoNtextNodes**</span><span class="sxs-lookup"><span data-stu-id="367a9-134">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="367a9-135">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="367a9-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

