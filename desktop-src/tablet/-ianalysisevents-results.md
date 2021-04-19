---
description: 在最後一個分析階段完成時發生。
ms.assetid: 97318c2d-980e-436c-b97d-e064bace5bf0
title: '_IAnalysisEvents：： Results 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Results
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bd52a5ce4563827fb22a00f79113fe1e80e852b3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106988114"
---
# <a name="_ianalysiseventsresults-event"></a><span data-ttu-id="5be73-103">\_IAnalysisEvents：： Results 事件</span><span class="sxs-lookup"><span data-stu-id="5be73-103">\_IAnalysisEvents::Results event</span></span>

<span data-ttu-id="5be73-104">在最後一個分析階段完成時發生。</span><span class="sxs-lookup"><span data-stu-id="5be73-104">Occurs when the final analysis stage is finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="5be73-105">語法</span><span class="sxs-lookup"><span data-stu-id="5be73-105">Syntax</span></span>


```C++
HRESULT Results(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a><span data-ttu-id="5be73-106">參數</span><span class="sxs-lookup"><span data-stu-id="5be73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5be73-107">*pInkAnalyzer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5be73-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5be73-108">產生分析結果的 [**IInkAnalyzer**](iinkanalyzer.md) 。</span><span class="sxs-lookup"><span data-stu-id="5be73-108">The [**IInkAnalyzer**](iinkanalyzer.md) that produces the analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="5be73-109">*pAnalysisStatus* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5be73-109">*pAnalysisStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5be73-110">代表分析狀態的 [**IAnalysisStatus**](ianalysisstatus.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="5be73-110">The [**IAnalysisStatus**](ianalysisstatus.md) object that represents the status of the analysis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5be73-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5be73-111">Return value</span></span>

<span data-ttu-id="5be73-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="5be73-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5be73-113">備註</span><span class="sxs-lookup"><span data-stu-id="5be73-113">Remarks</span></span>

<span data-ttu-id="5be73-114">[**IInkAnalyzer**](iinkanalyzer.md)會在對最終分析階段的結果進行協調之後引發此事件。</span><span class="sxs-lookup"><span data-stu-id="5be73-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it has reconciled the results for the final analysis stage.</span></span>

<span data-ttu-id="5be73-115">如果您的應用程式呼叫 [**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)，此事件會在分析結果就緒時發出信號。</span><span class="sxs-lookup"><span data-stu-id="5be73-115">If your application calls [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md), this event signals when analysis results are ready.</span></span>

<span data-ttu-id="5be73-116">如果您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理），此事件表示 **IInkAnalyzer** 已完成此分析階段的內部資料變更。</span><span class="sxs-lookup"><span data-stu-id="5be73-116">If your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), this event indicates that the **IInkAnalyzer** has finished making changes to its internal data for this analysis stage.</span></span>

<span data-ttu-id="5be73-117">當 [**IInkAnalyzer**](iinkanalyzer.md)引發 [**\_ IAnalysisProxyEvents：： InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md)事件時，請鎖定您的資料結構。</span><span class="sxs-lookup"><span data-stu-id="5be73-117">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span> <span data-ttu-id="5be73-118">在此分析階段中，資料結構的變更可能會導致筆跡分析和同步處理發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="5be73-118">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="5be73-119">當 **IInkAnalyzer** 引發 [**\_ IAnalysisEvents：： IntermediateResults**](-ianalysisevents-intermediateresults.md)或 **\_ IAnalysisEvents：： Results** 事件時，請解除鎖定您的資料結構。</span><span class="sxs-lookup"><span data-stu-id="5be73-119">Unlock your data structure when the **IInkAnalyzer** raises the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or **\_IAnalysisEvents::Results** event.</span></span>

<span data-ttu-id="5be73-120">如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="5be73-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5be73-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5be73-121">Requirements</span></span>



| <span data-ttu-id="5be73-122">需求</span><span class="sxs-lookup"><span data-stu-id="5be73-122">Requirement</span></span> | <span data-ttu-id="5be73-123">值</span><span class="sxs-lookup"><span data-stu-id="5be73-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5be73-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5be73-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5be73-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5be73-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5be73-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5be73-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5be73-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="5be73-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5be73-128">標頭</span><span class="sxs-lookup"><span data-stu-id="5be73-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5be73-129"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="5be73-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5be73-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5be73-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5be73-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5be73-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5be73-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5be73-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5be73-133">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="5be73-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="5be73-134">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="5be73-134">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="5be73-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="5be73-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="5be73-136">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="5be73-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="5be73-137">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="5be73-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="5be73-138">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="5be73-138">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="5be73-139">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="5be73-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




