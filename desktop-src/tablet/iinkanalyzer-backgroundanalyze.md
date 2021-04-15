---
description: 執行非同步筆跡分析。
ms.assetid: 36427b80-5e3b-4c9a-bb49-e6b7f9301cbd
title: 'IInkAnalyzer：： BackgroundAnalyze 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.BackgroundAnalyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 606e1444f66884564a6b9f2007adfc26b2eb2ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511664"
---
# <a name="iinkanalyzerbackgroundanalyze-method"></a><span data-ttu-id="51e5d-103">IInkAnalyzer：： BackgroundAnalyze 方法</span><span class="sxs-lookup"><span data-stu-id="51e5d-103">IInkAnalyzer::BackgroundAnalyze method</span></span>

<span data-ttu-id="51e5d-104">執行非同步筆跡分析。</span><span class="sxs-lookup"><span data-stu-id="51e5d-104">Performs asynchronous ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e5d-105">語法</span><span class="sxs-lookup"><span data-stu-id="51e5d-105">Syntax</span></span>


```C++
HRESULT BackgroundAnalyze();
```



## <a name="parameters"></a><span data-ttu-id="51e5d-106">參數</span><span class="sxs-lookup"><span data-stu-id="51e5d-106">Parameters</span></span>

<span data-ttu-id="51e5d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="51e5d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="51e5d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="51e5d-108">Return value</span></span>

<span data-ttu-id="51e5d-109">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="51e5d-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="51e5d-110">備註</span><span class="sxs-lookup"><span data-stu-id="51e5d-110">Remarks</span></span>

<span data-ttu-id="51e5d-111">當呼叫這個方法時， [**IInkAnalyzer**](iinkanalyzer.md) 會在背景執行緒上執行筆墨分析。</span><span class="sxs-lookup"><span data-stu-id="51e5d-111">When this method is called, the [**IInkAnalyzer**](iinkanalyzer.md) performs the ink analysis on a background thread.</span></span>

<span data-ttu-id="51e5d-112">這個方法會 **傳回 \_ FALSE** ，而且在下列情況下並不會啟動新的背景分析作業。</span><span class="sxs-lookup"><span data-stu-id="51e5d-112">This method returns **S\_FALSE** and does not start a new background analysis operation under the following circumstances.</span></span>

-   <span data-ttu-id="51e5d-113">[**IInkAnalyzer**](iinkanalyzer.md)目前正在執行背景分析。</span><span class="sxs-lookup"><span data-stu-id="51e5d-113">The [**IInkAnalyzer**](iinkanalyzer.md) is currently performing background analysis.</span></span>
-   <span data-ttu-id="51e5d-114">中途區域 (參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 代表空白區域。</span><span class="sxs-lookup"><span data-stu-id="51e5d-114">the dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) represents an empty area.</span></span>

<span data-ttu-id="51e5d-115">[**IInkAnalyzer**](iinkanalyzer.md)會在呼叫 [**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)或 **IInkAnalyzer：： BackgroundAnalyze 方法** 期間，分析其中途區域內的筆墨。</span><span class="sxs-lookup"><span data-stu-id="51e5d-115">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or **IInkAnalyzer::BackgroundAnalyze Method**.</span></span> <span data-ttu-id="51e5d-116">不過， **IInkAnalyzer** 可能會擴充分析作業，以包含鄰近區域。</span><span class="sxs-lookup"><span data-stu-id="51e5d-116">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="51e5d-117">這個方法會將中途區域設定為空白區域。</span><span class="sxs-lookup"><span data-stu-id="51e5d-117">This method sets the dirty region to an empty region.</span></span>

<span data-ttu-id="51e5d-118">如果在呼叫 **IInkAnalyzer：： BackgroundAnalyze 方法** 之後將筆劃資料加入至 [**IInkAnalyzer**](iinkanalyzer.md) ， **IInkAnalyzer** 可能會在筆跡分析的協調階段期間更新中途區域。</span><span class="sxs-lookup"><span data-stu-id="51e5d-118">If stroke data was added to the [**IInkAnalyzer**](iinkanalyzer.md) after the call to **IInkAnalyzer::BackgroundAnalyze Method**, the **IInkAnalyzer** may update the dirty region during the reconcile phase of ink analysis.</span></span>

<span data-ttu-id="51e5d-119">分析模式設定 (請參閱 [**IInkAnalyzer：： GetAnalysisModes 方法**](iinkanalyzer-getanalysismodes.md)) 指定 [**IInkAnalyzer**](iinkanalyzer.md) 執行背景分析的方式。</span><span class="sxs-lookup"><span data-stu-id="51e5d-119">The analysis modes setting (see [**IInkAnalyzer::GetAnalysisModes Method**](iinkanalyzer-getanalysismodes.md)) specifies how the [**IInkAnalyzer**](iinkanalyzer.md) performs background analysis.</span></span> <span data-ttu-id="51e5d-120">如需筆跡分析的詳細資訊，請參閱 [筆墨分析總覽](ink-analysis-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="51e5d-120">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

<span data-ttu-id="51e5d-121">在下列情況下，這個方法會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="51e5d-121">This method returns an error code under the following circumstances.</span></span>

-   <span data-ttu-id="51e5d-122">您的應用程式已在 [**IInkAnalyzer**](iinkanalyzer.md) (中設定 [**AnalysisModes**](analysismodes.md)值 **AnalysisModes \_ IntermediateResults** ，請參閱 [**IInkAnalyzer：： SetAnalysisModes 方法**](iinkanalyzer-setanalysismodes.md)) ，而且不會處理 [**\_ IAnalysisEvents：： IntermediateResults**](-ianalysisevents-intermediateresults.md)事件。</span><span class="sxs-lookup"><span data-stu-id="51e5d-122">Your application has set [**AnalysisModes**](analysismodes.md) value **AnalysisModes\_IntermediateResults** in the [**IInkAnalyzer**](iinkanalyzer.md) (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) and does not handle the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) event.</span></span>
-   <span data-ttu-id="51e5d-123">您的應用程式已清除 [**IInkAnalyzer**](iinkanalyzer.md)中的 [**AnalysisModes**](analysismodes.md)值 **AnalysisModes \_ AutomaticReconciliation** (請參閱 [**IInkAnalyzer：： SetAnalysisModes 方法**](iinkanalyzer-setanalysismodes.md)) ，而且不會處理 [**\_ IAnalysisEvents：： ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)事件。</span><span class="sxs-lookup"><span data-stu-id="51e5d-123">Your application has cleared [**AnalysisModes**](analysismodes.md) value **AnalysisModes\_AutomaticReconciliation** in the [**IInkAnalyzer**](iinkanalyzer.md) (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) and does not handle the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span>
-   <span data-ttu-id="51e5d-124">您的應用程式不會處理 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件。</span><span class="sxs-lookup"><span data-stu-id="51e5d-124">Your application does not handle the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>
-   <span data-ttu-id="51e5d-125">您的應用程式不會處理 [**\_ IAnalysisEvents：： UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)事件。</span><span class="sxs-lookup"><span data-stu-id="51e5d-125">Your application does not handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span>

## <a name="examples"></a><span data-ttu-id="51e5d-126">範例</span><span class="sxs-lookup"><span data-stu-id="51e5d-126">Examples</span></span>

<span data-ttu-id="51e5d-127">下列範例會檢查筆墨分析器的中途區域，然後在中途區域不是空的情況下起始背景筆墨分析。</span><span class="sxs-lookup"><span data-stu-id="51e5d-127">The following example checks the ink analyzer's dirty region, and then initiates background ink analysis if the dirty region is not empty.</span></span>


```C++
// Check that the ink analyzer's dirty region is not empty.
IAnalysisRegion *pDirtyRegion;
hr = this->m_spIInkAnalyzer->GetDirtyRegion(&pDirtyRegion);

if (SUCCEEDED(hr))
{
    VARIANT_BOOL bIsEmpty;
    hr = pDirtyRegion->IsEmpty(&bIsEmpty);

    if (SUCCEEDED(hr))
    {
        if (!bIsEmpty)
        {
            // Insert code that prepares the application for background
            // ink analysis here.

            // Start background ink analysis. The _IAnalysisEvents::Results
            // event signals when background ink analysis is complete.
            hr = this->m_spIInkAnalyzer->BackgroundAnalyze();
        }
    }
}

// Free the memory for the dirty region.
if (pDirtyRegion != NULL)
{
    pDirtyRegion->Release();
}
```



## <a name="requirements"></a><span data-ttu-id="51e5d-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="51e5d-128">Requirements</span></span>



| <span data-ttu-id="51e5d-129">需求</span><span class="sxs-lookup"><span data-stu-id="51e5d-129">Requirement</span></span> | <span data-ttu-id="51e5d-130">值</span><span class="sxs-lookup"><span data-stu-id="51e5d-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51e5d-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51e5d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="51e5d-132">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51e5d-132">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="51e5d-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51e5d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="51e5d-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="51e5d-134">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="51e5d-135">標頭</span><span class="sxs-lookup"><span data-stu-id="51e5d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="51e5d-136"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="51e5d-136"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="51e5d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="51e5d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51e5d-138"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51e5d-138"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="51e5d-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51e5d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51e5d-140">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="51e5d-140">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="51e5d-141">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="51e5d-141">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="51e5d-142">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="51e5d-142">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="51e5d-143">**IInkAnalyzer：： GetAnalysisModes 方法**</span><span class="sxs-lookup"><span data-stu-id="51e5d-143">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="51e5d-144">**IInkAnalyzer：： SetAnalysisModes 方法**</span><span class="sxs-lookup"><span data-stu-id="51e5d-144">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="51e5d-145">**IInkAnalyzer：： GetDirtyRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="51e5d-145">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="51e5d-146">**IInkAnalyzer：： SetDirtyRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="51e5d-146">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="51e5d-147">**IInkAnalyzer：： GetRootNode 方法**</span><span class="sxs-lookup"><span data-stu-id="51e5d-147">**IInkAnalyzer::GetRootNode Method**</span></span>](iinkanalyzer-getrootnode.md)
</dt> <dt>

[<span data-ttu-id="51e5d-148">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="51e5d-148">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




