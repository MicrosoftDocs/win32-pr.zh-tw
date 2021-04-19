---
description: 執行同步筆墨分析。
ms.assetid: 957845f3-96b4-4184-aaec-e266cbe47e46
title: 'IInkAnalyzer：：分析方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Analyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2867064067b902105508a7742c6fec88fdcd58be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971412"
---
# <a name="iinkanalyzeranalyze-method"></a><span data-ttu-id="0aa9c-103">IInkAnalyzer：：分析方法</span><span class="sxs-lookup"><span data-stu-id="0aa9c-103">IInkAnalyzer::Analyze method</span></span>

<span data-ttu-id="0aa9c-104">執行同步筆墨分析。</span><span class="sxs-lookup"><span data-stu-id="0aa9c-104">Performs synchronous ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aa9c-105">語法</span><span class="sxs-lookup"><span data-stu-id="0aa9c-105">Syntax</span></span>


```C++
HRESULT Analyze(
  [out] IAnalysisStatus **ppStatus
);
```



## <a name="parameters"></a><span data-ttu-id="0aa9c-106">參數</span><span class="sxs-lookup"><span data-stu-id="0aa9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aa9c-107">*ppStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0aa9c-107">*ppStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0aa9c-108">描述分析作業狀態之 [**IAnalysisStatus**](ianalysisstatus.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="0aa9c-108">A pointer to an [**IAnalysisStatus**](ianalysisstatus.md) that describes the status of the analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aa9c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0aa9c-109">Return value</span></span>

<span data-ttu-id="0aa9c-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="0aa9c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0aa9c-111">備註</span><span class="sxs-lookup"><span data-stu-id="0aa9c-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="0aa9c-112">若要避免記憶體流失，當您不再需要流量分析狀態時，請在 *ppStatus* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。</span><span class="sxs-lookup"><span data-stu-id="0aa9c-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppStatus* when you no longer need to use the analysis status.</span></span>

 

<span data-ttu-id="0aa9c-113">這個方法會啟動同步的筆墨分析作業。</span><span class="sxs-lookup"><span data-stu-id="0aa9c-113">This method starts a synchronous ink analysis operation.</span></span> <span data-ttu-id="0aa9c-114">筆墨分析包括版面配置分析、書寫和繪圖分類，以及手寫辨識。</span><span class="sxs-lookup"><span data-stu-id="0aa9c-114">Ink analysis includes layout analysis, writing and drawing classification, and handwriting recognition.</span></span> <span data-ttu-id="0aa9c-115">完成分析作業之後，這個方法會傳回。</span><span class="sxs-lookup"><span data-stu-id="0aa9c-115">This method returns after the analysis operation is complete.</span></span>

<span data-ttu-id="0aa9c-116">如果 *ppStatus* 為 **Null**，則這個方法會傳回 **E \_ 指標**。</span><span class="sxs-lookup"><span data-stu-id="0aa9c-116">This method returns **E\_POINTER** if *ppStatus* is **NULL**.</span></span>

<span data-ttu-id="0aa9c-117">在呼叫 **IInkAnalyzer：：分析方法** 或 [**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)期間， [**IInkAnalyzer**](iinkanalyzer.md) 會分析其中途區域內的筆墨 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 。</span><span class="sxs-lookup"><span data-stu-id="0aa9c-117">During a call to **IInkAnalyzer::Analyze Method** or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md), the [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span> <span data-ttu-id="0aa9c-118">不過， **IInkAnalyzer** 可能會擴充分析作業，以包含鄰近區域。</span><span class="sxs-lookup"><span data-stu-id="0aa9c-118">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="0aa9c-119">這個方法會將 [**IInkAnalyzer**](iinkanalyzer.md) 物件的中途區域設定為空白區域。</span><span class="sxs-lookup"><span data-stu-id="0aa9c-119">This method sets the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region to an empty region.</span></span> <span data-ttu-id="0aa9c-120">如果另一個執行緒已新增尚未分析的筆劃資料， **IInkAnalyzer** 會在分析的協調階段期間，將 unanalyzed 筆觸的周框方塊加入其中途區域中。</span><span class="sxs-lookup"><span data-stu-id="0aa9c-120">If another thread has added stroke data that has not been analyzed, the **IInkAnalyzer** adds the bounding box of the unanalyzed strokes to its dirty region during the reconcile phase of the analysis.</span></span>

<span data-ttu-id="0aa9c-121">如果您的應用程式不會處理 [**\_ IAnalysisEvents：： UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)事件，這個方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0aa9c-121">This method returns an error if your application does not handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span>

<span data-ttu-id="0aa9c-122">[**IInkAnalyzer**](iinkanalyzer.md)不會引發 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)和 [**\_ IAnalysisEvents：： IntermediateResults**](-ianalysisevents-intermediateresults.md)事件以回應這個方法。</span><span class="sxs-lookup"><span data-stu-id="0aa9c-122">The [**IInkAnalyzer**](iinkanalyzer.md) does not raise the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) and [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) events in response to this method.</span></span>

<span data-ttu-id="0aa9c-123">若要修改筆跡分析的執行方式，請使用 [**IInkAnalyzer：： SetAnalysisModes 方法**](iinkanalyzer-setanalysismodes.md)。</span><span class="sxs-lookup"><span data-stu-id="0aa9c-123">To modify the way ink analysis is performed, use [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md).</span></span>

<span data-ttu-id="0aa9c-124">如需筆跡分析的詳細資訊，請參閱 [筆墨分析總覽](ink-analysis-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="0aa9c-124">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0aa9c-125">範例</span><span class="sxs-lookup"><span data-stu-id="0aa9c-125">Examples</span></span>

<span data-ttu-id="0aa9c-126">下列範例會執行前景筆墨分析。</span><span class="sxs-lookup"><span data-stu-id="0aa9c-126">The following example performs foreground ink analysis.</span></span>


```C++
// Perform synchronous ink analysis.
IAnalysisStatus *pAnalysisStatus = NULL;
hr = this->m_spIInkAnalyzer->Analyze(&pAnalysisStatus);

if (SUCCEEDED(hr))
{
    // Insert code that processes the analysis results.
}

// Release this reference to the analysis status.
if (pAnalysisStatus != NULL)
{
    pAnalysisStatus->Release();
    pAnalysisStatus = NULL;
}
```



## <a name="requirements"></a><span data-ttu-id="0aa9c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="0aa9c-127">Requirements</span></span>



| <span data-ttu-id="0aa9c-128">需求</span><span class="sxs-lookup"><span data-stu-id="0aa9c-128">Requirement</span></span> | <span data-ttu-id="0aa9c-129">值</span><span class="sxs-lookup"><span data-stu-id="0aa9c-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa9c-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0aa9c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0aa9c-131">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0aa9c-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0aa9c-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0aa9c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0aa9c-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="0aa9c-133">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0aa9c-134">標頭</span><span class="sxs-lookup"><span data-stu-id="0aa9c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aa9c-135"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="0aa9c-135"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0aa9c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0aa9c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0aa9c-137"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0aa9c-137"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0aa9c-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0aa9c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aa9c-139">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="0aa9c-139">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="0aa9c-140">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="0aa9c-140">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="0aa9c-141">**IInkAnalyzer：： GetDirtyRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="0aa9c-141">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="0aa9c-142">**IInkAnalyzer：： SetDirtyRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="0aa9c-142">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="0aa9c-143">**IInkAnalyzer：： GetRootNode 方法**</span><span class="sxs-lookup"><span data-stu-id="0aa9c-143">**IInkAnalyzer::GetRootNode Method**</span></span>](iinkanalyzer-getrootnode.md)
</dt> <dt>

[<span data-ttu-id="0aa9c-144">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="0aa9c-144">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> </dl>

 

