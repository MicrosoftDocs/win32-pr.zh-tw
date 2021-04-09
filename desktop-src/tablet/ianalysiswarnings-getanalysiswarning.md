---
description: 抓取位於指定之索引處的 IAnalysisWarning 物件。
ms.assetid: 8f5d5642-73ec-496e-bad7-9f636fc00217
title: 'IAnalysisWarnings：： GetAnalysisWarning 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings.GetAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 88ed3686ecf3861a2b097ebfc005214ab0cdd1c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026257"
---
# <a name="ianalysiswarningsgetanalysiswarning-method"></a><span data-ttu-id="e446f-103">IAnalysisWarnings：： GetAnalysisWarning 方法</span><span class="sxs-lookup"><span data-stu-id="e446f-103">IAnalysisWarnings::GetAnalysisWarning method</span></span>

<span data-ttu-id="e446f-104">抓取位於指定之索引處的 [**IAnalysisWarning**](ianalysiswarning.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e446f-104">Retrieves the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e446f-105">語法</span><span class="sxs-lookup"><span data-stu-id="e446f-105">Syntax</span></span>


```C++
HRESULT GetAnalysisWarning(
  [in]  ULONG            ulIndex,
  [out] IAnalysisWarning **ppWarning
);
```



## <a name="parameters"></a><span data-ttu-id="e446f-106">參數</span><span class="sxs-lookup"><span data-stu-id="e446f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e446f-107">*ulIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e446f-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e446f-108">要取得之 [**IAnalysisWarning**](ianalysiswarning.md) 物件的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="e446f-108">The zero-based index of the [**IAnalysisWarning**](ianalysiswarning.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="e446f-109">*ppWarning* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e446f-109">*ppWarning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e446f-110">位於指定索引處之 [**IAnalysisWarning**](ianalysiswarning.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="e446f-110">A pointer to the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e446f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e446f-111">Return value</span></span>

<span data-ttu-id="e446f-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="e446f-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e446f-113">備註</span><span class="sxs-lookup"><span data-stu-id="e446f-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="e446f-114">若要避免記憶體流失，當您不再需要使用警告時，請在 ppWarning 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \*  。</span><span class="sxs-lookup"><span data-stu-id="e446f-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppWarning* when you no longer need to use the warning.</span></span>

 

## <a name="examples"></a><span data-ttu-id="e446f-115">範例</span><span class="sxs-lookup"><span data-stu-id="e446f-115">Examples</span></span>

<span data-ttu-id="e446f-116">下列範例會顯示 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件的事件處理常式的大綱。</span><span class="sxs-lookup"><span data-stu-id="e446f-116">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="e446f-117">處理常式會檢查 [**IAnalysisStatus：： IsSuccessful**](ianalysisstatus-issuccessful.md)。</span><span class="sxs-lookup"><span data-stu-id="e446f-117">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="e446f-118">如果分析作業產生警告，處理常式會逐一查看 [**IAnalysisWarning**](ianalysiswarning.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="e446f-118">If the analysis operation generates warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="e446f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e446f-119">Requirements</span></span>



| <span data-ttu-id="e446f-120">需求</span><span class="sxs-lookup"><span data-stu-id="e446f-120">Requirement</span></span> | <span data-ttu-id="e446f-121">值</span><span class="sxs-lookup"><span data-stu-id="e446f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e446f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e446f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e446f-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e446f-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e446f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e446f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e446f-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="e446f-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e446f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e446f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e446f-127"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="e446f-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e446f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e446f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e446f-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e446f-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e446f-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e446f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e446f-131">**IAnalysisWarnings**</span><span class="sxs-lookup"><span data-stu-id="e446f-131">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="e446f-132">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="e446f-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

