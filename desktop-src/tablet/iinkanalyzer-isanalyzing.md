---
description: 抓取值，指出 IInkAnalyzer 是否正在執行筆墨分析。
ms.assetid: 3f3f6f29-0c90-47e1-938c-f1ce6ed8df47
title: 'IInkAnalyzer：： IsAnalyzing 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.IsAnalyzing
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 94275d157b2936b7ad0ae16d4d70b62475f19af9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511653"
---
# <a name="iinkanalyzerisanalyzing-method"></a><span data-ttu-id="2096c-103">IInkAnalyzer：： IsAnalyzing 方法</span><span class="sxs-lookup"><span data-stu-id="2096c-103">IInkAnalyzer::IsAnalyzing method</span></span>

<span data-ttu-id="2096c-104">抓取值，指出 [**IInkAnalyzer**](iinkanalyzer.md) 是否正在執行筆墨分析。</span><span class="sxs-lookup"><span data-stu-id="2096c-104">Retrieves a value indicating whether the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="2096c-105">語法</span><span class="sxs-lookup"><span data-stu-id="2096c-105">Syntax</span></span>


```C++
HRESULT IsAnalyzing(
  [out] VARIANT_BOOL *pbAnalyzing
);
```



## <a name="parameters"></a><span data-ttu-id="2096c-106">參數</span><span class="sxs-lookup"><span data-stu-id="2096c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2096c-107">*pbAnalyzing* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2096c-107">*pbAnalyzing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2096c-108">**變異 \_** 如果 [**IInkAnalyzer**](iinkanalyzer.md)正在執行筆墨分析，則為 TRUE;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="2096c-108">**VARIANT\_TRUE** if the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2096c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="2096c-109">Return value</span></span>

<span data-ttu-id="2096c-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="2096c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2096c-111">備註</span><span class="sxs-lookup"><span data-stu-id="2096c-111">Remarks</span></span>

<span data-ttu-id="2096c-112">如果 [**IInkAnalyzer**](iinkanalyzer.md)正在執行同步或非同步分析，則這個屬性是 **VARIANT \_** 。</span><span class="sxs-lookup"><span data-stu-id="2096c-112">This property is **VARIANT\_TRUE** if the [**IInkAnalyzer**](iinkanalyzer.md) is performing synchronous or asynchronous analysis.</span></span>

## <a name="examples"></a><span data-ttu-id="2096c-113">範例</span><span class="sxs-lookup"><span data-stu-id="2096c-113">Examples</span></span>

<span data-ttu-id="2096c-114">下列範例顯示的方法會逐步解說筆墨分析器的 [**ICoNtextNode**](icontextnode.md) 結果樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="2096c-114">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="2096c-115">如果筆墨分析器目前未執行筆墨分析，則方法會執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="2096c-115">If the ink analyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="2096c-116">取得最前面的辨識字串。</span><span class="sxs-lookup"><span data-stu-id="2096c-116">Gets the top recognition string.</span></span>
-   <span data-ttu-id="2096c-117">取得筆墨分析器的根節點。</span><span class="sxs-lookup"><span data-stu-id="2096c-117">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="2096c-118">呼叫 helper 方法， `ExploreContextNode` 以檢查根節點和其子節點。</span><span class="sxs-lookup"><span data-stu-id="2096c-118">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2096c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="2096c-119">Requirements</span></span>



| <span data-ttu-id="2096c-120">需求</span><span class="sxs-lookup"><span data-stu-id="2096c-120">Requirement</span></span> | <span data-ttu-id="2096c-121">值</span><span class="sxs-lookup"><span data-stu-id="2096c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2096c-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2096c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2096c-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2096c-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2096c-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2096c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2096c-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="2096c-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2096c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="2096c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2096c-127"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="2096c-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2096c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2096c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2096c-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2096c-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2096c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2096c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2096c-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="2096c-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="2096c-132">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="2096c-132">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="2096c-133">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="2096c-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="2096c-134">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="2096c-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




