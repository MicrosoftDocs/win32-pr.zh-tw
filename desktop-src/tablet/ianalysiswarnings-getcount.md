---
description: 取得包含在 IAnalysisWarnings 集合中的 IAnalysisWarning 物件數目。
ms.assetid: a0ad46d5-fb1b-40f6-bfc1-28ea1bf4eb44
title: 'IAnalysisWarnings：： GetCount 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc795d310f4bc532a39e2c1a2b4d2ba68f0401f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971016"
---
# <a name="ianalysiswarningsgetcount-method"></a><span data-ttu-id="ec883-103">IAnalysisWarnings：： GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="ec883-103">IAnalysisWarnings::GetCount method</span></span>

<span data-ttu-id="ec883-104">取得包含在 [**IAnalysisWarnings**](ianalysiswarnings.md)集合中的 [**IAnalysisWarning**](ianalysiswarning.md)物件數目。</span><span class="sxs-lookup"><span data-stu-id="ec883-104">Gets the number of [**IAnalysisWarning**](ianalysiswarning.md) objects contained in the [**IAnalysisWarnings**](ianalysiswarnings.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec883-105">語法</span><span class="sxs-lookup"><span data-stu-id="ec883-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="ec883-106">參數</span><span class="sxs-lookup"><span data-stu-id="ec883-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec883-107">*pulCount* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="ec883-107">*pulCount* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ec883-108">包含在 [**IAnalysisWarnings**](ianalysiswarnings.md)集合中的 [**IAnalysisWarning**](ianalysiswarning.md)物件數目。</span><span class="sxs-lookup"><span data-stu-id="ec883-108">The number of [**IAnalysisWarning**](ianalysiswarning.md) objects contained in the [**IAnalysisWarnings**](ianalysiswarnings.md) collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec883-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec883-109">Return value</span></span>

<span data-ttu-id="ec883-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="ec883-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ec883-111">範例</span><span class="sxs-lookup"><span data-stu-id="ec883-111">Examples</span></span>

<span data-ttu-id="ec883-112">下列範例會顯示 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件的事件處理常式的大綱。</span><span class="sxs-lookup"><span data-stu-id="ec883-112">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="ec883-113">處理常式會檢查 [**IAnalysisStatus：： IsSuccessful**](ianalysisstatus-issuccessful.md)。</span><span class="sxs-lookup"><span data-stu-id="ec883-113">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="ec883-114">如果分析作業產生警告，處理常式會逐一查看 [**IAnalysisWarning**](ianalysiswarning.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="ec883-114">If the analysis operation generates warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ec883-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec883-115">Requirements</span></span>



| <span data-ttu-id="ec883-116">需求</span><span class="sxs-lookup"><span data-stu-id="ec883-116">Requirement</span></span> | <span data-ttu-id="ec883-117">值</span><span class="sxs-lookup"><span data-stu-id="ec883-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec883-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec883-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ec883-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec883-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ec883-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec883-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ec883-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="ec883-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ec883-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ec883-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec883-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="ec883-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ec883-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ec883-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec883-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec883-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ec883-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec883-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec883-127">**IAnalysisWarnings**</span><span class="sxs-lookup"><span data-stu-id="ec883-127">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="ec883-128">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="ec883-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




