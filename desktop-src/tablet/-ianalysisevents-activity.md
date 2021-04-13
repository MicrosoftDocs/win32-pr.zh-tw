---
description: 在呼叫 IInkAnalyzer：：分析方法或 IInkAnalyzer：： BackgroundAnalyze 方法時發生。
ms.assetid: 339b41c6-f388-4b81-b2bc-3705b39d9cc9
title: '_IAnalysisEvents：： Activity 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Activity
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f235d3414b0d514f32b4ebd197c04a8721968a2a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321703"
---
# <a name="_ianalysiseventsactivity-event"></a><span data-ttu-id="854ca-103">\_IAnalysisEvents：： Activity 事件</span><span class="sxs-lookup"><span data-stu-id="854ca-103">\_IAnalysisEvents::Activity event</span></span>

<span data-ttu-id="854ca-104">在呼叫 [**IInkAnalyzer：：分析**](iinkanalyzer-analyze.md) 方法或 [**IInkAnalyzer：： BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) 方法時發生。</span><span class="sxs-lookup"><span data-stu-id="854ca-104">Occurs when the [**IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md) method or [**IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="854ca-105">語法</span><span class="sxs-lookup"><span data-stu-id="854ca-105">Syntax</span></span>


```C++
HRESULT Activity();
```



## <a name="parameters"></a><span data-ttu-id="854ca-106">參數</span><span class="sxs-lookup"><span data-stu-id="854ca-106">Parameters</span></span>

<span data-ttu-id="854ca-107">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="854ca-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="854ca-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="854ca-108">Return value</span></span>

<span data-ttu-id="854ca-109">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="854ca-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="854ca-110">備註</span><span class="sxs-lookup"><span data-stu-id="854ca-110">Remarks</span></span>

<span data-ttu-id="854ca-111">此事件表示 [**IInkAnalyzer**](iinkanalyzer.md) 正在執行筆墨分析。</span><span class="sxs-lookup"><span data-stu-id="854ca-111">This event indicates that the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis.</span></span> <span data-ttu-id="854ca-112">此事件不會指出筆墨分析作業的進度。</span><span class="sxs-lookup"><span data-stu-id="854ca-112">This event does not indicate the progress of the ink analysis operation.</span></span>

<span data-ttu-id="854ca-113">若要執行下列任何一項，請執行 **\_ IAnalysisEvents：： Activity** 事件處理常式：</span><span class="sxs-lookup"><span data-stu-id="854ca-113">To do any of the following, implement an **\_IAnalysisEvents::Activity** event handler:</span></span>

-   <span data-ttu-id="854ca-114">向使用者指出筆墨分析器正在執行筆墨分析。</span><span class="sxs-lookup"><span data-stu-id="854ca-114">Indicate to the user that the ink analyzer is performing ink analysis.</span></span>
-   <span data-ttu-id="854ca-115">在同步分析期間處理使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="854ca-115">Process user input during synchronous analysis.</span></span>
-   <span data-ttu-id="854ca-116">在筆跡分析期間，接收系統要求的通知，例如重新繪製應用程式的視窗。</span><span class="sxs-lookup"><span data-stu-id="854ca-116">Receive notification of system requests, such as repainting of the application's window, during ink analysis.</span></span>

<span data-ttu-id="854ca-117">[**IInkAnalyzer**](iinkanalyzer.md)會在版面配置分析階段以及筆跡分析的書寫和繪圖分類階段，經常引發此事件。</span><span class="sxs-lookup"><span data-stu-id="854ca-117">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event frequently during the layout analysis phase and the writing and drawing classification phase of ink analysis.</span></span> <span data-ttu-id="854ca-118">**IInkAnalyzer** 會在存取筆跡辨識器之前和之後的手寫辨識階段期間引發此事件。</span><span class="sxs-lookup"><span data-stu-id="854ca-118">The **IInkAnalyzer** raises this event during the handwriting recognition phase before and after accessing an ink recognizer.</span></span>

<span data-ttu-id="854ca-119">[**IInkAnalyzer**](iinkanalyzer.md)產生的活動事件數目受下列影響：</span><span class="sxs-lookup"><span data-stu-id="854ca-119">The number of activity events an [**IInkAnalyzer**](iinkanalyzer.md) generates is affected by:</span></span>

-   <span data-ttu-id="854ca-120">[**IInkAnalyzer**](iinkanalyzer.md)適用于筆墨辨識的筆墨辨識器。</span><span class="sxs-lookup"><span data-stu-id="854ca-120">The ink recognizer that the [**IInkAnalyzer**](iinkanalyzer.md) applies to ink recognition.</span></span>
-   <span data-ttu-id="854ca-121">[**IInkAnalyzer**](iinkanalyzer.md)正在分析之筆劃的數目和長度。</span><span class="sxs-lookup"><span data-stu-id="854ca-121">The number and length of strokes that the [**IInkAnalyzer**](iinkanalyzer.md) is analyzing.</span></span>
-   <span data-ttu-id="854ca-122">分類為書寫的筆劃數目。</span><span class="sxs-lookup"><span data-stu-id="854ca-122">The number of strokes that are classified as writing.</span></span>

<span data-ttu-id="854ca-123">如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="854ca-123">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="854ca-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="854ca-124">Requirements</span></span>



| <span data-ttu-id="854ca-125">需求</span><span class="sxs-lookup"><span data-stu-id="854ca-125">Requirement</span></span> | <span data-ttu-id="854ca-126">值</span><span class="sxs-lookup"><span data-stu-id="854ca-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="854ca-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="854ca-127">Minimum supported client</span></span><br/> | <span data-ttu-id="854ca-128">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="854ca-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="854ca-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="854ca-129">Minimum supported server</span></span><br/> | <span data-ttu-id="854ca-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="854ca-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="854ca-131">標頭</span><span class="sxs-lookup"><span data-stu-id="854ca-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="854ca-132"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="854ca-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="854ca-133">DLL</span><span class="sxs-lookup"><span data-stu-id="854ca-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="854ca-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="854ca-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="854ca-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="854ca-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="854ca-136">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="854ca-136">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="854ca-137">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="854ca-137">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="854ca-138">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="854ca-138">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="854ca-139">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="854ca-139">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="854ca-140">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="854ca-140">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="854ca-141">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="854ca-141">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="854ca-142">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="854ca-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




