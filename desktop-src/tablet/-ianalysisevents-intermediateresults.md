---
description: 當目前的中繼分析階段完成時發生。
ms.assetid: 9ade61f4-bcfe-4c49-bda1-b60aaf780935
title: '_IAnalysisEvents：： IntermediateResults 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.IntermediateResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33430225746ddd1a4099f89112f14f99f2b6da84
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106986681"
---
# <a name="_ianalysiseventsintermediateresults-event"></a><span data-ttu-id="d76e9-103">\_IAnalysisEvents：： IntermediateResults 事件</span><span class="sxs-lookup"><span data-stu-id="d76e9-103">\_IAnalysisEvents::IntermediateResults event</span></span>

<span data-ttu-id="d76e9-104">當目前的中繼分析階段完成時發生。</span><span class="sxs-lookup"><span data-stu-id="d76e9-104">Occurs when the current intermediate analysis stage is finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="d76e9-105">語法</span><span class="sxs-lookup"><span data-stu-id="d76e9-105">Syntax</span></span>


```C++
HRESULT IntermediateResults(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a><span data-ttu-id="d76e9-106">參數</span><span class="sxs-lookup"><span data-stu-id="d76e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d76e9-107">*pInkAnalyzer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d76e9-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d76e9-108">正在執行分析的 [**IInkAnalyzer**](iinkanalyzer.md) 。</span><span class="sxs-lookup"><span data-stu-id="d76e9-108">The [**IInkAnalyzer**](iinkanalyzer.md) that is performing the analysis.</span></span>

</dd> <dt>

<span data-ttu-id="d76e9-109">*pAnalysisStatus* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d76e9-109">*pAnalysisStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d76e9-110">代表中繼結果狀態的 [**IAnalysisStatus**](ianalysisstatus.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d76e9-110">The [**IAnalysisStatus**](ianalysisstatus.md) object representing the status of the intermediate results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d76e9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d76e9-111">Return value</span></span>

<span data-ttu-id="d76e9-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="d76e9-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d76e9-113">備註</span><span class="sxs-lookup"><span data-stu-id="d76e9-113">Remarks</span></span>

<span data-ttu-id="d76e9-114">[**IInkAnalyzer**](iinkanalyzer.md)會在對目前分析階段的中繼結果進行協調之後引發此事件。</span><span class="sxs-lookup"><span data-stu-id="d76e9-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it has reconciled the intermediate results for the current analysis stage.</span></span>

<span data-ttu-id="d76e9-115">如果您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理），此事件表示 **IInkAnalyzer** 已完成此分析階段的內部資料變更。</span><span class="sxs-lookup"><span data-stu-id="d76e9-115">If your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), this event indicates that the **IInkAnalyzer** has finished making changes to its internal data for this analysis stage.</span></span>

<span data-ttu-id="d76e9-116">當 [**IInkAnalyzer**](iinkanalyzer.md)引發 [**\_ IAnalysisProxyEvents：： InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md)事件時，請鎖定您的資料結構。</span><span class="sxs-lookup"><span data-stu-id="d76e9-116">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span> <span data-ttu-id="d76e9-117">在此分析階段中，資料結構的變更可能會導致筆跡分析和同步處理發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="d76e9-117">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="d76e9-118">當 **IInkAnalyzer** 引發 **\_ IAnalysisEvents：： IntermediateResults** 或 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件時，您可以解除鎖定您的資料結構。</span><span class="sxs-lookup"><span data-stu-id="d76e9-118">You can unlock your data structure when the **IInkAnalyzer** raises the **\_IAnalysisEvents::IntermediateResults** or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="d76e9-119">如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="d76e9-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="d76e9-120">[**IInkAnalyzer**](iinkanalyzer.md)只會在其分析模式已設定 **AnalysisModes \_ IntermediateResults** 旗標時產生中繼結果 (請參閱 [**IInkAnalyzer：： GetAnalysisModes 方法**](iinkanalyzer-getanalysismodes.md)) 。</span><span class="sxs-lookup"><span data-stu-id="d76e9-120">The [**IInkAnalyzer**](iinkanalyzer.md) generates intermediate results only when its analysis modes has the **AnalysisModes\_IntermediateResults** flag set (see [**IInkAnalyzer::GetAnalysisModes Method**](iinkanalyzer-getanalysismodes.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="d76e9-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d76e9-121">Requirements</span></span>



| <span data-ttu-id="d76e9-122">需求</span><span class="sxs-lookup"><span data-stu-id="d76e9-122">Requirement</span></span> | <span data-ttu-id="d76e9-123">值</span><span class="sxs-lookup"><span data-stu-id="d76e9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d76e9-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d76e9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d76e9-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d76e9-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d76e9-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d76e9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d76e9-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="d76e9-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d76e9-128">標頭</span><span class="sxs-lookup"><span data-stu-id="d76e9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d76e9-129"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="d76e9-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d76e9-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d76e9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d76e9-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d76e9-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d76e9-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d76e9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d76e9-133">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="d76e9-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="d76e9-134">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="d76e9-134">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="d76e9-135">**\_IAnalysisEvents：： Results**</span><span class="sxs-lookup"><span data-stu-id="d76e9-135">**\_IAnalysisEvents::Results**</span></span>](-ianalysisevents-results.md)
</dt> <dt>

[<span data-ttu-id="d76e9-136">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="d76e9-136">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="d76e9-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="d76e9-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="d76e9-138">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="d76e9-138">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="d76e9-139">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="d76e9-139">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="d76e9-140">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="d76e9-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>
