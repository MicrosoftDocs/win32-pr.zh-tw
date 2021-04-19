---
description: 傳回使用 AnalysisWarningCode 列舉時所發生之警告的型別。
ms.assetid: ec67a5ac-a7a2-4805-b9b5-915ea956d228
title: 'IAnalysisWarning：： GetWarningCode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetWarningCode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8e129b410de9e8ca9e3944b6a371fe0cac673fc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972646"
---
# <a name="ianalysiswarninggetwarningcode-method"></a><span data-ttu-id="ee9b6-103">IAnalysisWarning：： GetWarningCode 方法</span><span class="sxs-lookup"><span data-stu-id="ee9b6-103">IAnalysisWarning::GetWarningCode method</span></span>

<span data-ttu-id="ee9b6-104">傳回使用 [**AnalysisWarningCode**](analysiswarningcode.md) 列舉時所發生之警告的型別。</span><span class="sxs-lookup"><span data-stu-id="ee9b6-104">Returns the type of warning that occurred by using the [**AnalysisWarningCode**](analysiswarningcode.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee9b6-105">語法</span><span class="sxs-lookup"><span data-stu-id="ee9b6-105">Syntax</span></span>


```C++
HRESULT GetWarningCode(
  [out] AnalysisWarningCode *pWarningCode
);
```



## <a name="parameters"></a><span data-ttu-id="ee9b6-106">參數</span><span class="sxs-lookup"><span data-stu-id="ee9b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee9b6-107">*pWarningCode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ee9b6-107">*pWarningCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee9b6-108">發生的警告類型。</span><span class="sxs-lookup"><span data-stu-id="ee9b6-108">The type of warning that occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee9b6-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee9b6-109">Return value</span></span>

<span data-ttu-id="ee9b6-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="ee9b6-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ee9b6-111">範例</span><span class="sxs-lookup"><span data-stu-id="ee9b6-111">Examples</span></span>

<span data-ttu-id="ee9b6-112">下列範例會顯示 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件的事件處理常式的大綱。</span><span class="sxs-lookup"><span data-stu-id="ee9b6-112">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="ee9b6-113">處理常式會檢查 [**IAnalysisStatus：： IsSuccessful**](ianalysisstatus-issuccessful.md)。</span><span class="sxs-lookup"><span data-stu-id="ee9b6-113">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="ee9b6-114">如果分析作業產生警告，處理常式會逐一查看 [**IAnalysisWarning**](ianalysiswarning.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="ee9b6-114">If the analysis operation generated warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ee9b6-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee9b6-115">Requirements</span></span>



| <span data-ttu-id="ee9b6-116">需求</span><span class="sxs-lookup"><span data-stu-id="ee9b6-116">Requirement</span></span> | <span data-ttu-id="ee9b6-117">值</span><span class="sxs-lookup"><span data-stu-id="ee9b6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee9b6-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee9b6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ee9b6-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee9b6-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ee9b6-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee9b6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ee9b6-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="ee9b6-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ee9b6-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ee9b6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee9b6-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="ee9b6-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ee9b6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ee9b6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee9b6-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee9b6-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ee9b6-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee9b6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee9b6-127">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="ee9b6-127">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="ee9b6-128">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="ee9b6-128">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="ee9b6-129">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="ee9b6-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

