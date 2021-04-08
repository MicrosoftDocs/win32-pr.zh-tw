---
description: 針對 IInkAnalyzer 中的整個內容節點樹狀結構，抓取辨識作業的最佳結果字串。
ms.assetid: 4aa57f41-3122-47a9-a60d-4a229e23f63c
title: 'IInkAnalyzer：： GetRecognizedString 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 67afe9909fcabb8df880706b2b077ea602ccade6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690580"
---
# <a name="iinkanalyzergetrecognizedstring-method"></a><span data-ttu-id="41383-103">IInkAnalyzer：： GetRecognizedString 方法</span><span class="sxs-lookup"><span data-stu-id="41383-103">IInkAnalyzer::GetRecognizedString method</span></span>

<span data-ttu-id="41383-104">針對 [**IInkAnalyzer**](iinkanalyzer.md)中的整個內容節點樹狀結構，抓取辨識作業的最佳結果字串。</span><span class="sxs-lookup"><span data-stu-id="41383-104">Retrieves the best-result string of the recognition operation for the entire context node tree in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="41383-105">語法</span><span class="sxs-lookup"><span data-stu-id="41383-105">Syntax</span></span>


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a><span data-ttu-id="41383-106">參數</span><span class="sxs-lookup"><span data-stu-id="41383-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41383-107">*pbstrRecognizedString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="41383-107">*pbstrRecognizedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41383-108">[**IInkAnalyzer**](iinkanalyzer.md)中整個內容節點樹狀結構之辨識作業的最佳結果字串。</span><span class="sxs-lookup"><span data-stu-id="41383-108">The best-result string of the recognition operation for the entire context node tree in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41383-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="41383-109">Return value</span></span>

<span data-ttu-id="41383-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="41383-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="41383-111">備註</span><span class="sxs-lookup"><span data-stu-id="41383-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="41383-112">若要避免記憶體流失，當您不再需要使用此字串時，請呼叫 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 進行 *pbstrRecognizedString* 。</span><span class="sxs-lookup"><span data-stu-id="41383-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) for *pbstrRecognizedString* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="41383-113">這個方法會傳回與所辨識字串的根節點屬性資料相同的值。</span><span class="sxs-lookup"><span data-stu-id="41383-113">This method returns the same value as the root node's property data for the recognized string.</span></span> <span data-ttu-id="41383-114"> (參閱 [**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md)、 [**ICoNtextNode：： GetPropertyData**](icontextnode-getpropertydata.md)和 [內容節點屬性](context-node-properties.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="41383-114">(See [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md), [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md), and [Context Node Properties](context-node-properties.md).)</span></span>

## <a name="examples"></a><span data-ttu-id="41383-115">範例</span><span class="sxs-lookup"><span data-stu-id="41383-115">Examples</span></span>

<span data-ttu-id="41383-116">下列範例顯示的方法會逐步解說筆墨分析器的 [**ICoNtextNode**](icontextnode.md) 結果樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="41383-116">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="41383-117">如果 IInkAnlyzer 目前未執行筆墨分析，則方法會執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="41383-117">If the IInkAnlyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="41383-118">取得最前面的辨識字串。</span><span class="sxs-lookup"><span data-stu-id="41383-118">Gets the top recognition string.</span></span>
-   <span data-ttu-id="41383-119">取得筆墨分析器的根節點。</span><span class="sxs-lookup"><span data-stu-id="41383-119">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="41383-120">呼叫 helper 方法， `ExploreContextNode` 以檢查根節點和其子節點。</span><span class="sxs-lookup"><span data-stu-id="41383-120">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="41383-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="41383-121">Requirements</span></span>



| <span data-ttu-id="41383-122">需求</span><span class="sxs-lookup"><span data-stu-id="41383-122">Requirement</span></span> | <span data-ttu-id="41383-123">值</span><span class="sxs-lookup"><span data-stu-id="41383-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41383-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41383-124">Minimum supported client</span></span><br/> | <span data-ttu-id="41383-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41383-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="41383-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41383-126">Minimum supported server</span></span><br/> | <span data-ttu-id="41383-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="41383-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="41383-128">標頭</span><span class="sxs-lookup"><span data-stu-id="41383-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="41383-129"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="41383-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="41383-130">DLL</span><span class="sxs-lookup"><span data-stu-id="41383-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41383-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41383-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="41383-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41383-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41383-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="41383-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="41383-134">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="41383-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

