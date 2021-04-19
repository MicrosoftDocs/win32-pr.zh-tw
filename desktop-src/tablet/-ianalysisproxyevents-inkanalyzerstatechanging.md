---
description: 發生于 IInkAnalyzer 協調分析結果之前，讓應用程式可以與 IInkAnalyzer 同步處理資料。
ms.assetid: 9daa8723-5234-40d9-ac41-6dcca988a8b4
title: '_IAnalysisProxyEvents：： InkAnalyzerStateChanging 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.InkAnalyzerStateChanging
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 92535c34b5d107fb1e435e9abe229df46204f236
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106992651"
---
# <a name="_ianalysisproxyeventsinkanalyzerstatechanging-event"></a><span data-ttu-id="b1a2b-103">\_IAnalysisProxyEvents：： InkAnalyzerStateChanging 事件</span><span class="sxs-lookup"><span data-stu-id="b1a2b-103">\_IAnalysisProxyEvents::InkAnalyzerStateChanging event</span></span>

<span data-ttu-id="b1a2b-104">發生于 [**IInkAnalyzer**](iinkanalyzer.md) 協調分析結果之前，讓應用程式可以與 **IInkAnalyzer** 同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="b1a2b-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) reconciles analysis results so that an application can synchronize data with the **IInkAnalyzer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1a2b-105">語法</span><span class="sxs-lookup"><span data-stu-id="b1a2b-105">Syntax</span></span>


```C++
HRESULT InkAnalyzerStateChanging(
  [in] IInkAnalyzer *pInkAnalyzer
);
```



## <a name="parameters"></a><span data-ttu-id="b1a2b-106">參數</span><span class="sxs-lookup"><span data-stu-id="b1a2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1a2b-107">*pInkAnalyzer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b1a2b-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a2b-108">即將協調其分析結果的 [**IInkAnalyzer**](iinkanalyzer.md) 。</span><span class="sxs-lookup"><span data-stu-id="b1a2b-108">The [**IInkAnalyzer**](iinkanalyzer.md) that is about to reconcile its analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1a2b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1a2b-109">Return value</span></span>

<span data-ttu-id="b1a2b-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="b1a2b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b1a2b-111">備註</span><span class="sxs-lookup"><span data-stu-id="b1a2b-111">Remarks</span></span>

<span data-ttu-id="b1a2b-112">當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用此事件。</span><span class="sxs-lookup"><span data-stu-id="b1a2b-112">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="b1a2b-113">當 **IInkAnalyzer** 引發這個事件時，您的應用程式應該填入筆墨分析器根節點的子節點 (請參閱 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md) 和 [**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md)) 。</span><span class="sxs-lookup"><span data-stu-id="b1a2b-113">When the **IInkAnalyzer** raises this event, your application should populate the subnodes of the ink analyzer's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

<span data-ttu-id="b1a2b-114">[**IInkAnalyzer**](iinkanalyzer.md)引發 [**\_ IAnalysisEvents：： ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)事件之後，就會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="b1a2b-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it raises the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span> <span data-ttu-id="b1a2b-115">只有在執行背景分析時，才會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="b1a2b-115">It raises this event only while performing background analysis.</span></span>

<span data-ttu-id="b1a2b-116">當 [**IInkAnalyzer**](iinkanalyzer.md)引發 **\_ IAnalysisProxyEvents：： InkAnalyzerStateChanging** 事件時，請鎖定您的資料結構。</span><span class="sxs-lookup"><span data-stu-id="b1a2b-116">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the **\_IAnalysisProxyEvents::InkAnalyzerStateChanging** event.</span></span> <span data-ttu-id="b1a2b-117">在此分析階段中，資料結構的變更可能會導致筆跡分析和同步處理發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="b1a2b-117">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="b1a2b-118">當 **IInkAnalyzer** 引發 [**\_ IAnalysisEvents：： IntermediateResults**](-ianalysisevents-intermediateresults.md)或 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件時，請解除鎖定您的資料結構。</span><span class="sxs-lookup"><span data-stu-id="b1a2b-118">Unlock your data structure when the **IInkAnalyzer** raises the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="b1a2b-119">如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="b1a2b-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1a2b-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1a2b-120">Requirements</span></span>



| <span data-ttu-id="b1a2b-121">需求</span><span class="sxs-lookup"><span data-stu-id="b1a2b-121">Requirement</span></span> | <span data-ttu-id="b1a2b-122">值</span><span class="sxs-lookup"><span data-stu-id="b1a2b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a2b-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1a2b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b1a2b-124">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1a2b-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b1a2b-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1a2b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b1a2b-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="b1a2b-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b1a2b-127">標頭</span><span class="sxs-lookup"><span data-stu-id="b1a2b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1a2b-128"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="b1a2b-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b1a2b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b1a2b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1a2b-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1a2b-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b1a2b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1a2b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1a2b-132">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="b1a2b-132">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="b1a2b-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b1a2b-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b1a2b-134">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="b1a2b-134">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b1a2b-135">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="b1a2b-135">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="b1a2b-136">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="b1a2b-136">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="b1a2b-137">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="b1a2b-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




