---
description: 包含物件的集合，這些物件會執行 IAnalysisWarning 介面，且為筆跡分析作業的結果。
ms.assetid: 2118c18b-d316-4e91-8652-62969115e8b5
title: 'IAnalysisWarnings 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 938d406ea90d86cc05ac84b69304b7a85e0e54fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986360"
---
# <a name="ianalysiswarnings-interface"></a><span data-ttu-id="7e131-103">IAnalysisWarnings 介面</span><span class="sxs-lookup"><span data-stu-id="7e131-103">IAnalysisWarnings interface</span></span>

<span data-ttu-id="7e131-104">包含物件的集合，這些物件會執行 [**IAnalysisWarning**](ianalysiswarning.md) 介面，且為筆跡分析作業的結果。</span><span class="sxs-lookup"><span data-stu-id="7e131-104">Contains a collection of objects that implement the [**IAnalysisWarning**](ianalysiswarning.md) interface and that are the result of an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="7e131-105">成員</span><span class="sxs-lookup"><span data-stu-id="7e131-105">Members</span></span>

<span data-ttu-id="7e131-106">**IAnalysisWarnings** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="7e131-106">The **IAnalysisWarnings** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7e131-107">**IAnalysisWarnings** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7e131-107">**IAnalysisWarnings** also has these types of members:</span></span>

-   [<span data-ttu-id="7e131-108">方法</span><span class="sxs-lookup"><span data-stu-id="7e131-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7e131-109">方法</span><span class="sxs-lookup"><span data-stu-id="7e131-109">Methods</span></span>

<span data-ttu-id="7e131-110">**IAnalysisWarnings** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7e131-110">The **IAnalysisWarnings** interface has these methods.</span></span>



| <span data-ttu-id="7e131-111">方法</span><span class="sxs-lookup"><span data-stu-id="7e131-111">Method</span></span>                                                             | <span data-ttu-id="7e131-112">描述</span><span class="sxs-lookup"><span data-stu-id="7e131-112">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e131-113">**GetAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="7e131-113">**GetAnalysisWarning**</span></span>](ianalysiswarnings-getanalysiswarning.md) | <span data-ttu-id="7e131-114">抓取位於指定之索引處的 [**IAnalysisWarning**](ianalysiswarning.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="7e131-114">Retrieves the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span><br/>                                       |
| [<span data-ttu-id="7e131-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="7e131-115">**GetCount**</span></span>](ianalysiswarnings-getcount.md)                     | <span data-ttu-id="7e131-116">捕獲 **IAnalysisWarnings** 集合中包含的 [**IAnalysisWarning**](ianalysiswarning.md)物件數目。</span><span class="sxs-lookup"><span data-stu-id="7e131-116">Retrieves the number of [**IAnalysisWarning**](ianalysiswarning.md) objects contained in the **IAnalysisWarnings** collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="7e131-117">範例</span><span class="sxs-lookup"><span data-stu-id="7e131-117">Examples</span></span>

<span data-ttu-id="7e131-118">下列範例會顯示 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件的事件處理常式的大綱。</span><span class="sxs-lookup"><span data-stu-id="7e131-118">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="7e131-119">處理常式會檢查 [**IAnalysisStatus：： IsSuccessful**](ianalysisstatus-issuccessful.md)。</span><span class="sxs-lookup"><span data-stu-id="7e131-119">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="7e131-120">如果分析作業產生警告，處理常式會逐一查看 [**IAnalysisWarning**](ianalysiswarning.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="7e131-120">If the analysis operation generated warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7e131-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e131-121">Requirements</span></span>



| <span data-ttu-id="7e131-122">需求</span><span class="sxs-lookup"><span data-stu-id="7e131-122">Requirement</span></span> | <span data-ttu-id="7e131-123">值</span><span class="sxs-lookup"><span data-stu-id="7e131-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e131-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e131-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7e131-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e131-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7e131-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e131-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7e131-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="7e131-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7e131-128">標頭</span><span class="sxs-lookup"><span data-stu-id="7e131-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e131-129"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="7e131-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7e131-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7e131-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e131-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e131-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7e131-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e131-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e131-133">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="7e131-133">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="7e131-134">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="7e131-134">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="7e131-135">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="7e131-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

