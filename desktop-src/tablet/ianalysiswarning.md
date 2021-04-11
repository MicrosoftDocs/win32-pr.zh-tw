---
description: 表示筆墨分析作業期間發生的警告或錯誤。
ms.assetid: a9b0564b-8a49-44bc-9dbc-60a2fd5b60f2
title: 'IAnalysisWarning 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 79e865ac909d6f9ee1862926ffab06f538661d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113400"
---
# <a name="ianalysiswarning-interface"></a><span data-ttu-id="8a1c7-103">IAnalysisWarning 介面</span><span class="sxs-lookup"><span data-stu-id="8a1c7-103">IAnalysisWarning interface</span></span>

<span data-ttu-id="8a1c7-104">表示筆墨分析作業期間發生的警告或錯誤。</span><span class="sxs-lookup"><span data-stu-id="8a1c7-104">Represents a warning or error that occurs during an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="8a1c7-105">成員</span><span class="sxs-lookup"><span data-stu-id="8a1c7-105">Members</span></span>

<span data-ttu-id="8a1c7-106">**IAnalysisWarning** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="8a1c7-106">The **IAnalysisWarning** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8a1c7-107">**IAnalysisWarning** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8a1c7-107">**IAnalysisWarning** also has these types of members:</span></span>

-   [<span data-ttu-id="8a1c7-108">方法</span><span class="sxs-lookup"><span data-stu-id="8a1c7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8a1c7-109">方法</span><span class="sxs-lookup"><span data-stu-id="8a1c7-109">Methods</span></span>

<span data-ttu-id="8a1c7-110">**IAnalysisWarning** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8a1c7-110">The **IAnalysisWarning** interface has these methods.</span></span>



| <span data-ttu-id="8a1c7-111">方法</span><span class="sxs-lookup"><span data-stu-id="8a1c7-111">Method</span></span>                                                            | <span data-ttu-id="8a1c7-112">描述</span><span class="sxs-lookup"><span data-stu-id="8a1c7-112">Description</span></span>                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a1c7-113">**GetBackgroundError**</span><span class="sxs-lookup"><span data-stu-id="8a1c7-113">**GetBackgroundError**</span></span>](ianalysiswarning-getbackgrounderror.md) | <span data-ttu-id="8a1c7-114">如果發生錯誤，則捕獲背景筆墨分析作業的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8a1c7-114">Retrieves the error code for the background ink analysis operation if an error occurred.</span></span><br/>                                    |
| [<span data-ttu-id="8a1c7-115">**GetHint**</span><span class="sxs-lookup"><span data-stu-id="8a1c7-115">**GetHint**</span></span>](ianalysiswarning-gethint.md)                       | <span data-ttu-id="8a1c7-116">抓取造成此警告的分析提示</span><span class="sxs-lookup"><span data-stu-id="8a1c7-116">Retrieves the analysis hint that caused this warning</span></span><br/>                                                                        |
| [<span data-ttu-id="8a1c7-117">**GetNodeIds**</span><span class="sxs-lookup"><span data-stu-id="8a1c7-117">**GetNodeIds**</span></span>](ianalysiswarning-getnodeids.md)                 | <span data-ttu-id="8a1c7-118">抓取與此警告相關聯之任何相關內容節點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8a1c7-118">Retrieves the identifiers of any relevant context nodes that are associated with this warning.</span></span><br/>                              |
| [<span data-ttu-id="8a1c7-119">**GetWarningCode**</span><span class="sxs-lookup"><span data-stu-id="8a1c7-119">**GetWarningCode**</span></span>](ianalysiswarning-getwarningcode.md)         | <span data-ttu-id="8a1c7-120">使用 [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) 列舉來抓取發生的警告類型。</span><span class="sxs-lookup"><span data-stu-id="8a1c7-120">Retrieves the type of warning that occurred by using the [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) enumeration.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8a1c7-121">備註</span><span class="sxs-lookup"><span data-stu-id="8a1c7-121">Remarks</span></span>

<span data-ttu-id="8a1c7-122">[**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)列舉會描述可能發生的警告類型。</span><span class="sxs-lookup"><span data-stu-id="8a1c7-122">The types of warnings that can occur are described by the [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) enumeration.</span></span> <span data-ttu-id="8a1c7-123">當您嘗試使用 [**IInkAnalyzer**](iinkanalyzer.md)所使用的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)不支援的功能時，通常會發生警告。</span><span class="sxs-lookup"><span data-stu-id="8a1c7-123">Often warnings occur when you try to use a feature that is not supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that the [**IInkAnalyzer**](iinkanalyzer.md) is using.</span></span>

<span data-ttu-id="8a1c7-124">有些警告表示 [**IInkAnalyzer**](iinkanalyzer.md) 未完成分析作業。</span><span class="sxs-lookup"><span data-stu-id="8a1c7-124">Some warnings indicate that the [**IInkAnalyzer**](iinkanalyzer.md) did not complete the analysis operation.</span></span> <span data-ttu-id="8a1c7-125">如需詳細資訊，請參閱 [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)。</span><span class="sxs-lookup"><span data-stu-id="8a1c7-125">For more information, see [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).</span></span>

## <a name="examples"></a><span data-ttu-id="8a1c7-126">範例</span><span class="sxs-lookup"><span data-stu-id="8a1c7-126">Examples</span></span>

<span data-ttu-id="8a1c7-127">下列範例會顯示 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件的事件處理常式的大綱。</span><span class="sxs-lookup"><span data-stu-id="8a1c7-127">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="8a1c7-128">處理常式會檢查 [**IAnalysisStatus：： IsSuccessful**](ianalysisstatus-issuccessful.md)。</span><span class="sxs-lookup"><span data-stu-id="8a1c7-128">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="8a1c7-129">如果分析作業產生警告，處理常式會逐一查看 **IAnalysisWarning** 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="8a1c7-129">If the analysis operation generates warnings, the handler iterates through the collection of **IAnalysisWarning** objects.</span></span>


```C++
// _IAnalysisEvents::Results event handler.
STDMETHODIMP CMyClass::Results(
    IInkAnalyzer *pInkAnalyzer,
    IAnalysisStatus *pAnalysisStatus)
{
    // Check the status of the analysis operation.
    VARIANT_BOOL bResult = VARIANT_FALSE;
    HRESULT hr = pAnalysisStatus->IsSuccessful(&bResult);

    if( SUCCEEDED(hr) )
    {
        if( bResult )
        {
            // Insert code that handles a successful result.
        }
        else
        {
            // Get the analysis warnings.
            IAnalysisWarnings* pAnalysisWarnings = NULL;
            hr = pAnalysisStatus->GetWarnings(&pAnalysisWarnings);
            if (SUCCEEDED(hr))
            {
                // Iterate through the warning collection.
                ULONG warningCount = 0;
                hr = pAnalysisWarnings->GetCount(&warningCount);
                if (SUCCEEDED(hr))
                {
                    IAnalysisWarning *pAnalysisWarning = NULL;
                    AnalysisWarningCode analysisWarningCode;
                    for (ULONG index=0; index<warningCount; index++)
                    {
                        // Get an analysis warning.
                        hr = pAnalysisWarnings->GetAnalysisWarning(
                            index, &pAnalysisWarning);

                        if (SUCCEEDED(hr))
                        {
                            // Get the warning code for the warning.
                            hr = pAnalysisWarning->GetWarningCode(
                                &analysisWarningCode);

                            if (SUCCEEDED(hr))
                            {
                                // Insert code that handles each
                                // analysis warning.
                            }
                        }

                        // Release this reference to the analysis warning.
                        if (pAnalysisWarning != NULL)
                        {
                            pAnalysisWarning->Release();
                            pAnalysisWarning = NULL;
                        }

                        if (FAILED(hr))
                        {
                            break;
                        }
                    }
                }
            }

            // Release this reference to the analysis warnings collection.
            if (pAnalysisWarnings != NULL)
            {
                pAnalysisWarnings->Release();
                pAnalysisWarnings = NULL;
            }
        }
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="8a1c7-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a1c7-130">Requirements</span></span>



| <span data-ttu-id="8a1c7-131">需求</span><span class="sxs-lookup"><span data-stu-id="8a1c7-131">Requirement</span></span> | <span data-ttu-id="8a1c7-132">值</span><span class="sxs-lookup"><span data-stu-id="8a1c7-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1c7-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a1c7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8a1c7-134">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a1c7-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8a1c7-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a1c7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8a1c7-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="8a1c7-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8a1c7-137">標頭</span><span class="sxs-lookup"><span data-stu-id="8a1c7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a1c7-138"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="8a1c7-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8a1c7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="8a1c7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a1c7-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a1c7-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8a1c7-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a1c7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a1c7-142">**IAnalysisWarnings**</span><span class="sxs-lookup"><span data-stu-id="8a1c7-142">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="8a1c7-143">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="8a1c7-143">**AnalysisWarningCode**</span></span>](analysiswarningcode.md)
</dt> <dt>

[<span data-ttu-id="8a1c7-144">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="8a1c7-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

