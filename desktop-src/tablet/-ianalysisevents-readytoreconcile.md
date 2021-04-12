---
description: 當 IInkAnalyzer 已準備好要將其背景分析結果與目前狀態協調時，就會發生此問題。
ms.assetid: 63cf48eb-9d1e-4017-a4eb-55d811f7e6cf
title: '_IAnalysisEvents：： ReadyToReconcile 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.ReadyToReconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f3144f34dc680f9bc31f51b9e6b4284a70fb9bc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195793"
---
# <a name="_ianalysiseventsreadytoreconcile-event"></a><span data-ttu-id="54cc8-103">\_IAnalysisEvents：： ReadyToReconcile 事件</span><span class="sxs-lookup"><span data-stu-id="54cc8-103">\_IAnalysisEvents::ReadyToReconcile event</span></span>

<span data-ttu-id="54cc8-104">當 [**IInkAnalyzer**](iinkanalyzer.md) 已準備好要將其背景分析結果與目前狀態協調時，就會發生此問題。</span><span class="sxs-lookup"><span data-stu-id="54cc8-104">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) is ready to reconcile its background analysis results with its current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="54cc8-105">語法</span><span class="sxs-lookup"><span data-stu-id="54cc8-105">Syntax</span></span>


```C++
HRESULT ReadyToReconcile();
```



## <a name="parameters"></a><span data-ttu-id="54cc8-106">參數</span><span class="sxs-lookup"><span data-stu-id="54cc8-106">Parameters</span></span>

<span data-ttu-id="54cc8-107">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="54cc8-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="54cc8-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="54cc8-108">Return value</span></span>

<span data-ttu-id="54cc8-109">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="54cc8-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="54cc8-110">備註</span><span class="sxs-lookup"><span data-stu-id="54cc8-110">Remarks</span></span>

<span data-ttu-id="54cc8-111">設定筆墨分析器的 **AnalysisModes \_ AutomaticReconciliation** 旗標時， [**IInkAnalyzer**](iinkanalyzer.md)會執行自動調整 (請參閱 [**IInkAnalyzer：： SetAnalysisModes 方法**](iinkanalyzer-setanalysismodes.md)) 。</span><span class="sxs-lookup"><span data-stu-id="54cc8-111">The [**IInkAnalyzer**](iinkanalyzer.md) performs automatic reconciliation when the ink analyzer's **AnalysisModes\_AutomaticReconciliation** flag is set (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)).</span></span> <span data-ttu-id="54cc8-112">未設定 **AnalysisModes \_ AutomaticReconciliation** 旗標時，您的應用程式需要手動協調背景分析結果。</span><span class="sxs-lookup"><span data-stu-id="54cc8-112">When the **AnalysisModes\_AutomaticReconciliation** flag is not set, your application needs to reconcile background analysis results manually.</span></span>

<span data-ttu-id="54cc8-113">若要執行手動對帳，請遵循下列步驟。</span><span class="sxs-lookup"><span data-stu-id="54cc8-113">To perform manual reconciliation, follow these steps.</span></span>

1.  <span data-ttu-id="54cc8-114">清除筆墨分析器的 **AnalysisModes \_ AutomaticReconciliation** 旗標。</span><span class="sxs-lookup"><span data-stu-id="54cc8-114">Clear the ink analyzer's **AnalysisModes\_AutomaticReconciliation** flag.</span></span>
2.  <span data-ttu-id="54cc8-115">處理 **\_ IAnalysisEvents：： ReadyToReconcile** 事件。</span><span class="sxs-lookup"><span data-stu-id="54cc8-115">Handle the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span>
3.  <span data-ttu-id="54cc8-116">若要調解分析結果，請從 **\_ IAnalysisEvents：： ReadyToReconcile** 事件的事件處理常式呼叫 [**IInkAnalyzer：：調解方法**](iinkanalyzer-reconcile.md)方法。</span><span class="sxs-lookup"><span data-stu-id="54cc8-116">To reconcile the analysis results, call the [**IInkAnalyzer::Reconcile Method**](iinkanalyzer-reconcile.md) method from the event handler for the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span> <span data-ttu-id="54cc8-117">若要取消目前的背景分析作業，請從 **\_ IAnalysisEvents：： ReadyToReconcile** 事件的事件處理常式呼叫 [**IInkAnalyzer：： Abort 方法**](iinkanalyzer-abort.md)方法。</span><span class="sxs-lookup"><span data-stu-id="54cc8-117">To cancel the current background analysis operation, call the [**IInkAnalyzer::Abort Method**](iinkanalyzer-abort.md) method from the event handler for the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span>

<span data-ttu-id="54cc8-118">[**IInkAnalyzer**](iinkanalyzer.md)會在引發 [**\_ IAnalysisProxyEvents：： InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md)事件之前引發此事件。</span><span class="sxs-lookup"><span data-stu-id="54cc8-118">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event before it raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span>

<span data-ttu-id="54cc8-119">如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="54cc8-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="54cc8-120">[**IInkAnalyzer**](iinkanalyzer.md)會在背景分析期間引發此事件。</span><span class="sxs-lookup"><span data-stu-id="54cc8-120">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event during background analysis.</span></span>

## <a name="requirements"></a><span data-ttu-id="54cc8-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="54cc8-121">Requirements</span></span>



| <span data-ttu-id="54cc8-122">需求</span><span class="sxs-lookup"><span data-stu-id="54cc8-122">Requirement</span></span> | <span data-ttu-id="54cc8-123">值</span><span class="sxs-lookup"><span data-stu-id="54cc8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54cc8-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54cc8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="54cc8-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54cc8-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="54cc8-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54cc8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="54cc8-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="54cc8-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="54cc8-128">標頭</span><span class="sxs-lookup"><span data-stu-id="54cc8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="54cc8-129"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="54cc8-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="54cc8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="54cc8-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54cc8-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54cc8-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="54cc8-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54cc8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54cc8-133">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="54cc8-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="54cc8-134">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="54cc8-134">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="54cc8-135">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="54cc8-135">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="54cc8-136">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="54cc8-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="54cc8-137">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="54cc8-137">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="54cc8-138">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="54cc8-138">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="54cc8-139">**IInkAnalyzer：：調解方法**</span><span class="sxs-lookup"><span data-stu-id="54cc8-139">**IInkAnalyzer::Reconcile Method**</span></span>](iinkanalyzer-reconcile.md)
</dt> <dt>

[<span data-ttu-id="54cc8-140">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="54cc8-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




