---
description: 取消目前的分析作業。
ms.assetid: 909bfa66-b6df-4730-95b7-809fc2170e85
title: 'IInkAnalyzer：： Abort 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Abort
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eac96809bfbe41e7d6a070782da3ffd0f6407c60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998071"
---
# <a name="iinkanalyzerabort-method"></a><span data-ttu-id="b4f9c-103">IInkAnalyzer：： Abort 方法</span><span class="sxs-lookup"><span data-stu-id="b4f9c-103">IInkAnalyzer::Abort method</span></span>

<span data-ttu-id="b4f9c-104">取消目前的分析作業。</span><span class="sxs-lookup"><span data-stu-id="b4f9c-104">Cancels the current analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4f9c-105">語法</span><span class="sxs-lookup"><span data-stu-id="b4f9c-105">Syntax</span></span>


```C++
HRESULT Abort(
  [out] IAnalysisRegion **ppAbortedRegion
);
```



## <a name="parameters"></a><span data-ttu-id="b4f9c-106">參數</span><span class="sxs-lookup"><span data-stu-id="b4f9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4f9c-107">*ppAbortedRegion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b4f9c-107">*ppAbortedRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f9c-108">[**IAnalysisRegion**](ianalysisregion.md)的指標，代表中途區域 (參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 目前的分析作業。</span><span class="sxs-lookup"><span data-stu-id="b4f9c-108">A pointer to an [**IAnalysisRegion**](ianalysisregion.md) that represents the dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) of the current analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4f9c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4f9c-109">Return value</span></span>

<span data-ttu-id="b4f9c-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="b4f9c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b4f9c-111">備註</span><span class="sxs-lookup"><span data-stu-id="b4f9c-111">Remarks</span></span>

<span data-ttu-id="b4f9c-112">當您不再需要使用物件時，請在 *ppAbortedRegion* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。</span><span class="sxs-lookup"><span data-stu-id="b4f9c-112">Call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAbortedRegion* when you no longer need to use the object.</span></span>

<span data-ttu-id="b4f9c-113">這個方法會取消目前的分析作業。</span><span class="sxs-lookup"><span data-stu-id="b4f9c-113">This method cancels the current analysis operation.</span></span>

<span data-ttu-id="b4f9c-114">當 *ppAbortedRegion* 為 **Null** 時，這個方法會正常執行中止，因為這表示呼叫端對傳回值沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="b4f9c-114">When *ppAbortedRegion* is **NULL**, this method performs the abort as normal, because this indicates that the caller has no interest in the return value.</span></span>

<span data-ttu-id="b4f9c-115">**IInkAnalyzer：： Abort 方法** 會讓閉嘴目前分析作業的 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)和 [**\_ IAnalysisEvents：： Activity**](-ianalysisevents-activity.md)事件。</span><span class="sxs-lookup"><span data-stu-id="b4f9c-115">**IInkAnalyzer::Abort Method** silences the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) and [**\_IAnalysisEvents::Activity**](-ianalysisevents-activity.md) events for the current analysis operation.</span></span>

<span data-ttu-id="b4f9c-116">**IInkAnalyzer：： Abort 方法** 會以非同步方式執行，直到目前的背景分析作業取消為止。</span><span class="sxs-lookup"><span data-stu-id="b4f9c-116">**IInkAnalyzer::Abort Method** runs asynchronously until the current background analysis operation is canceled.</span></span> <span data-ttu-id="b4f9c-117">由於取消程式是非同步，因此應用程式可以在目前的分析操作就取消時執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="b4f9c-117">Because the cancellation process is asynchronous, the application can perform other tasks while the current analysis opertions is canceled.</span></span>

<span data-ttu-id="b4f9c-118">如果沒有進行中的分析作業，這個方法會傳回空白的分析區域。</span><span class="sxs-lookup"><span data-stu-id="b4f9c-118">If no analysis operations are in progress, this method returns an empty analysis region.</span></span>

<span data-ttu-id="b4f9c-119">如果有一個分析作業正在進行中，這個方法就會取消作業。</span><span class="sxs-lookup"><span data-stu-id="b4f9c-119">If one analysis operation is in progress, this method cancels the operation.</span></span>

<span data-ttu-id="b4f9c-120">如果同步和非同步分析作業正在進行中，此方法會取消同步作業。</span><span class="sxs-lookup"><span data-stu-id="b4f9c-120">If both synchronous and asynchronous analysis operations are in progress, this method cancels the synchronous operation.</span></span>

<span data-ttu-id="b4f9c-121">如果針對相同的分析作業呼叫這個方法一次以上，第一個呼叫會傳回作業的中途區域，而後續的呼叫會傳回空白區域。</span><span class="sxs-lookup"><span data-stu-id="b4f9c-121">If this method is called more than once for the same analysis operation, the first call returns the dirty region for the operation, and the subsequent calls return an empty region.</span></span>

<span data-ttu-id="b4f9c-122">如果您的應用程式維護本身與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理的資料結構，則呼叫 **IInkAnalyzer：： Abort 方法** 可能會讓您的檔具有部分結果。</span><span class="sxs-lookup"><span data-stu-id="b4f9c-122">If your application maintains its own data structure that is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), calling **IInkAnalyzer::Abort Method** can leave your document with partial results.</span></span> <span data-ttu-id="b4f9c-123">若要避免這種情況，請不要在 **IInkAnalyzer** 收到 [**\_ IAnalysisProxyEvents：： InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md)事件和 **IInkAnalyzer** 收到 [**\_ IAnalysisEvents：： IntermediateResults**](-ianalysisevents-intermediateresults.md)或 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件的時間之間呼叫 **IInkAnalyzer：： Abort 方法**。</span><span class="sxs-lookup"><span data-stu-id="b4f9c-123">To avoid this, do not call **IInkAnalyzer::Abort Method** between the time the **IInkAnalyzer** receives the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event and the time the **IInkAnalyzer** receives the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="b4f9c-124">如需有關同步處理您的應用程式資料與筆墨分析器的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="b4f9c-124">For more information about synchronizing your application data with the ink analyzer, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4f9c-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4f9c-125">Requirements</span></span>



| <span data-ttu-id="b4f9c-126">需求</span><span class="sxs-lookup"><span data-stu-id="b4f9c-126">Requirement</span></span> | <span data-ttu-id="b4f9c-127">值</span><span class="sxs-lookup"><span data-stu-id="b4f9c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f9c-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4f9c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b4f9c-129">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4f9c-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b4f9c-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4f9c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b4f9c-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="b4f9c-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b4f9c-132">標頭</span><span class="sxs-lookup"><span data-stu-id="b4f9c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4f9c-133"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="b4f9c-133"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b4f9c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b4f9c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4f9c-135"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4f9c-135"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b4f9c-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4f9c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4f9c-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b4f9c-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b4f9c-138">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="b4f9c-138">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="b4f9c-139">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="b4f9c-139">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="b4f9c-140">**IInkAnalyzer：： GetDirtyRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="b4f9c-140">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="b4f9c-141">**IInkAnalyzer：： SetDirtyRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="b4f9c-141">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="b4f9c-142">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="b4f9c-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

