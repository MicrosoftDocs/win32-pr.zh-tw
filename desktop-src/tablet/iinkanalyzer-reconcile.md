---
description: 將背景筆墨分析作業的結果套用至應用程式在呼叫 IInkAnalyzer：： BackgroundAnalyze 方法之後，尚未修改之樹狀結構部分的內容節點樹狀結構。
ms.assetid: 60e15d4f-6e81-48b9-b7f3-97d2de5c0c1c
title: 'IInkAnalyzer：：調解方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Reconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33229c7da47f294f317d2216d9e9bf4f6b114599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970822"
---
# <a name="iinkanalyzerreconcile-method"></a><span data-ttu-id="643db-103">IInkAnalyzer：：調解方法</span><span class="sxs-lookup"><span data-stu-id="643db-103">IInkAnalyzer::Reconcile method</span></span>

<span data-ttu-id="643db-104">將背景筆墨分析作業的結果套用至應用程式在呼叫 [**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)之後，尚未修改之樹狀結構部分的內容節點樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="643db-104">Applies the results of a background ink analysis operation to the context node tree for the portions of the tree that have not been modified by the application since the call to [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="643db-105">語法</span><span class="sxs-lookup"><span data-stu-id="643db-105">Syntax</span></span>


```C++
HRESULT Reconcile();
```



## <a name="parameters"></a><span data-ttu-id="643db-106">參數</span><span class="sxs-lookup"><span data-stu-id="643db-106">Parameters</span></span>

<span data-ttu-id="643db-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="643db-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="643db-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="643db-108">Return value</span></span>

<span data-ttu-id="643db-109">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="643db-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="643db-110">備註</span><span class="sxs-lookup"><span data-stu-id="643db-110">Remarks</span></span>

<span data-ttu-id="643db-111">根據預設， [**IInkAnalyzer**](iinkanalyzer.md)會在引發 [**\_ IAnalysisEvents：： IntermediateResults**](-ianalysisevents-intermediateresults.md)和 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件之前立即執行自動調整階段。</span><span class="sxs-lookup"><span data-stu-id="643db-111">By default, the [**IInkAnalyzer**](iinkanalyzer.md) performs an automatic reconciliation phase immediately before raising the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) and [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) events.</span></span>

<span data-ttu-id="643db-112">若要停用自動調整，請清除筆墨分析器分析模式中的 **AnalysisModes \_ AutomaticReconciliation** 旗標 (查看 [**IInkAnalyzer：： SetAnalysisModes 方法**](iinkanalyzer-setanalysismodes.md) 和 [**AnalysisModes**](analysismodes.md)) 。</span><span class="sxs-lookup"><span data-stu-id="643db-112">To disable automatic reconciliation, clear the **AnalysisModes\_AutomaticReconciliation** flag from the ink analyzer's analysis modes (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md) and [**AnalysisModes**](analysismodes.md)).</span></span> <span data-ttu-id="643db-113">[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)方法會在停用自動調整時傳回錯誤，而您的應用程式不會處理 [**\_ IAnalysisEvents：： ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)事件。</span><span class="sxs-lookup"><span data-stu-id="643db-113">The [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) method returns an error when automatic reconciliation is disabled and your application does not handle the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span> <span data-ttu-id="643db-114">您的應用程式必須先呼叫 **IInkAnalyzer：：調解方法** 方法， [**IInkAnalyzer**](iinkanalyzer.md) 才能繼續處理結果，或繼續分析對應的分析階段。</span><span class="sxs-lookup"><span data-stu-id="643db-114">Your application must call the **IInkAnalyzer::Reconcile Method** method before the [**IInkAnalyzer**](iinkanalyzer.md) can continue to process the results or continue further analysis for the corresponding analysis stage.</span></span>

<span data-ttu-id="643db-115">在背景分析期間，您的應用程式可以在 [**IInkAnalyzer**](iinkanalyzer.md) 物件的內容節點樹狀結構中進行變更，例如新增或移除筆劃及變更筆觸資料。</span><span class="sxs-lookup"><span data-stu-id="643db-115">Your application can make changes, such as adding or removing strokes and changing stroke data, in the [**IInkAnalyzer**](iinkanalyzer.md) object's context node tree during background analysis.</span></span> <span data-ttu-id="643db-116">這類變更可能會使部分背景分析結果失效。</span><span class="sxs-lookup"><span data-stu-id="643db-116">Such changes can invalidate portions of the background analysis results.</span></span> <span data-ttu-id="643db-117">這個方法只會針對您的應用程式未變更的樹狀結構部分，將分析結果套用至分析器的內容節點樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="643db-117">This method applies analysis results only to the analyzer's context node tree for the portions of the tree that your application has not changed.</span></span> <span data-ttu-id="643db-118">這個方法也會將包含無效分析結果的區域新增至 **IInkAnalyzer** 物件的中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 。</span><span class="sxs-lookup"><span data-stu-id="643db-118">This method also adds regions containing invalidated analysis results to the **IInkAnalyzer** object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="643db-119">如需使用來分析筆墨的詳細資訊，請參閱 [筆墨分析總覽](ink-analysis-overview.md)。[**AnalysisModes**](analysismodes.md)</span><span class="sxs-lookup"><span data-stu-id="643db-119">For more information about using the to analyze ink, see [Ink Analysis Overview](ink-analysis-overview.md).[**AnalysisModes**](analysismodes.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="643db-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="643db-120">Requirements</span></span>



| <span data-ttu-id="643db-121">需求</span><span class="sxs-lookup"><span data-stu-id="643db-121">Requirement</span></span> | <span data-ttu-id="643db-122">值</span><span class="sxs-lookup"><span data-stu-id="643db-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="643db-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="643db-123">Minimum supported client</span></span><br/> | <span data-ttu-id="643db-124">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="643db-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="643db-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="643db-125">Minimum supported server</span></span><br/> | <span data-ttu-id="643db-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="643db-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="643db-127">標頭</span><span class="sxs-lookup"><span data-stu-id="643db-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="643db-128"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="643db-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="643db-129">DLL</span><span class="sxs-lookup"><span data-stu-id="643db-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="643db-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="643db-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="643db-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="643db-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="643db-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="643db-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="643db-133">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="643db-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="643db-134">**\_IAnalysisEvents::ReadyToReconcile**</span><span class="sxs-lookup"><span data-stu-id="643db-134">**\_IAnalysisEvents::ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[<span data-ttu-id="643db-135">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="643db-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




