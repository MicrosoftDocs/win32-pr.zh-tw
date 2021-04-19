---
description: 取得 IInkAnalyzer 物件的內容樹狀結構的根 ICoNtextNode。
ms.assetid: 6c073952-7962-4f38-89ae-f543e64e904f
title: 'IInkAnalyzer：： GetRootNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRootNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 280c1907558372d247f25a0f760990d7c3c53a07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970187"
---
# <a name="iinkanalyzergetrootnode-method"></a><span data-ttu-id="8499d-103">IInkAnalyzer：： GetRootNode 方法</span><span class="sxs-lookup"><span data-stu-id="8499d-103">IInkAnalyzer::GetRootNode method</span></span>

<span data-ttu-id="8499d-104">取得 [**IInkAnalyzer**](iinkanalyzer.md)物件的內容樹狀結構的根 [**ICoNtextNode**](icontextnode.md) 。</span><span class="sxs-lookup"><span data-stu-id="8499d-104">Gets the root [**IContextNode**](icontextnode.md) of the [**IInkAnalyzer**](iinkanalyzer.md) object's context tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="8499d-105">語法</span><span class="sxs-lookup"><span data-stu-id="8499d-105">Syntax</span></span>


```C++
HRESULT GetRootNode(
  [out] IContextNode **ppRootNode
);
```



## <a name="parameters"></a><span data-ttu-id="8499d-106">參數</span><span class="sxs-lookup"><span data-stu-id="8499d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8499d-107">*ppRootNode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8499d-107">*ppRootNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8499d-108">[**IInkAnalyzer**](iinkanalyzer.md)物件的內容樹狀結構的根 [**ICoNtextNode**](icontextnode.md) 。</span><span class="sxs-lookup"><span data-stu-id="8499d-108">The root [**IContextNode**](icontextnode.md) of the [**IInkAnalyzer**](iinkanalyzer.md) object's context tree.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8499d-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8499d-109">Return value</span></span>

<span data-ttu-id="8499d-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="8499d-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8499d-111">備註</span><span class="sxs-lookup"><span data-stu-id="8499d-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="8499d-112">若要避免記憶體流失，當您不再需要使用根節點時，請在 *ppRootNode* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。</span><span class="sxs-lookup"><span data-stu-id="8499d-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppRootNode* when you no longer need to use the root node.</span></span>

 

<span data-ttu-id="8499d-113">[**IInkAnalyzer**](iinkanalyzer.md)會維護 [**ICoNtextNode**](icontextnode.md)物件的樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="8499d-113">The [**IInkAnalyzer**](iinkanalyzer.md) maintains a tree of [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="8499d-114">這些物件包含用於分析的輸入，以及分析的結果。</span><span class="sxs-lookup"><span data-stu-id="8499d-114">These objects contain both input for analysis and the results of analysis.</span></span> <span data-ttu-id="8499d-115">當首次將筆劃加入至 **IInkAnalyzer** 時， **IInkAnalyzer** 會將它們指派給類型 UnclassifiedInk 的 **ICoNtextNode** (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [內容節點類型](context-node-types.md)) 。</span><span class="sxs-lookup"><span data-stu-id="8499d-115">When strokes are initially added to the **IInkAnalyzer**, the **IInkAnalyzer** assigns them to a **IContextNode** of type UnclassifiedInk (See [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="8499d-116">在分析筆劃之後， **IInkAnalyzer** 會將它們指派給樹狀結構中適當的 **ICoNtextNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="8499d-116">After the strokes are analyzed, the **IInkAnalyzer** assigns them to appropriate **IContextNode** objects in the tree.</span></span> <span data-ttu-id="8499d-117">如需使用 **IInkAnalyzer** 來分析筆墨的詳細資訊，請參閱 [筆墨分析總覽](ink-analysis-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="8499d-117">For more information about using the **IInkAnalyzer** to analyze ink, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8499d-118">範例</span><span class="sxs-lookup"><span data-stu-id="8499d-118">Examples</span></span>

<span data-ttu-id="8499d-119">下列範例顯示的方法會逐步解說筆墨分析器的 [**ICoNtextNode**](icontextnode.md) 結果樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="8499d-119">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="8499d-120">如果 IInkAnlyzer 目前未執行筆墨分析，則方法會執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="8499d-120">If the IInkAnlyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="8499d-121">取得最前面的辨識字串。</span><span class="sxs-lookup"><span data-stu-id="8499d-121">Gets the top recognition string.</span></span>
-   <span data-ttu-id="8499d-122">取得筆墨分析器的根節點。</span><span class="sxs-lookup"><span data-stu-id="8499d-122">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="8499d-123">呼叫 helper 方法， `ExploreContextNode` 以檢查根節點和其子節點。</span><span class="sxs-lookup"><span data-stu-id="8499d-123">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


```C++
// Helper method that explores the current analysis results of an ink analyzer.
HRESULT CMyClass::ExploreAnalysisResults(
    IInkAnalyzer *pInkAnalyzer)
{
    // Check that the ink analyzer is not currently analyzing ink.
    VARIANT_BOOL bIsAnalyzing;
    HRESULT hr = pInkAnalyzer->IsAnalyzing(&bIsAnalyzing);

    if (SUCCEEDED(hr))
    {
        if (bIsAnalyzing)
        {
            return E_PENDING;
        }

        // Get the ink analyzer's best-result string.
        BSTR recognizedString = NULL;
        hr = pInkAnalyzer->GetRecognizedString(&recognizedString);

        if (SUCCEEDED(hr))
        {
            // Insert code that records the ink analyzer's best-result string here.

            // Get the ink analyzer's root node.
            IContextNode *pRootNode = NULL;
            hr = pInkAnalyzer->GetRootNode(&pRootNode);

            if (SUCCEEDED(hr))
            {
                // Call a helper method that recursively explores context
                // nodes and their subnodes.
                hr = this->ExploreContextNode(pRootNode);
            }

            // Release this reference to the root node.
            if (pRootNode != NULL)
            {
                pRootNode->Release();
                pRootNode = NULL;
            }
        }

        // Free the system resources for the recognized string.
        SysFreeString(recognizedString);
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="8499d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="8499d-124">Requirements</span></span>



| <span data-ttu-id="8499d-125">需求</span><span class="sxs-lookup"><span data-stu-id="8499d-125">Requirement</span></span> | <span data-ttu-id="8499d-126">值</span><span class="sxs-lookup"><span data-stu-id="8499d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8499d-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8499d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8499d-128">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8499d-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8499d-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8499d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8499d-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="8499d-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8499d-131">標頭</span><span class="sxs-lookup"><span data-stu-id="8499d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8499d-132"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="8499d-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8499d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8499d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8499d-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8499d-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8499d-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8499d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8499d-136">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="8499d-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8499d-137">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="8499d-137">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="8499d-138">內容節點類型</span><span class="sxs-lookup"><span data-stu-id="8499d-138">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="8499d-139">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="8499d-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

