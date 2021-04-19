---
description: 指定與 IInkAnalyzer 物件的分析步驟相關聯的事件。
ms.assetid: 8cb75f99-aa39-44d1-a055-dc1fb3f6b292
title: _IAnalysisEvents 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90e32669d8b542202f6166052c072f224bb2954a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988881"
---
# <a name="_ianalysisevents-interface"></a><span data-ttu-id="4e320-103">\_IAnalysisEvents 介面</span><span class="sxs-lookup"><span data-stu-id="4e320-103">\_IAnalysisEvents interface</span></span>

<span data-ttu-id="4e320-104">指定與 [**IInkAnalyzer**](iinkanalyzer.md) 物件的分析步驟相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="4e320-104">Specifies events associated with the analysis steps of an [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>

-   [<span data-ttu-id="4e320-105">事件</span><span class="sxs-lookup"><span data-stu-id="4e320-105">Events</span></span>](/windows)

### <a name="events"></a><span data-ttu-id="4e320-106">事件</span><span class="sxs-lookup"><span data-stu-id="4e320-106">Events</span></span>

<span data-ttu-id="4e320-107">**\_ IAnalysisEvents** 介面具有這些事件。</span><span class="sxs-lookup"><span data-stu-id="4e320-107">The **\_IAnalysisEvents** interface has these events.</span></span>



| <span data-ttu-id="4e320-108">事件</span><span class="sxs-lookup"><span data-stu-id="4e320-108">Event</span></span>                                                               | <span data-ttu-id="4e320-109">描述</span><span class="sxs-lookup"><span data-stu-id="4e320-109">Description</span></span>                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e320-110">**活動**</span><span class="sxs-lookup"><span data-stu-id="4e320-110">**Activity**</span></span>](-ianalysisevents-activity.md)                       | <span data-ttu-id="4e320-111">在呼叫 [**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md) 或 [**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md) 方法期間發生。</span><span class="sxs-lookup"><span data-stu-id="4e320-111">Occurs during calls to the [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) method.</span></span><br/> |
| [<span data-ttu-id="4e320-112">**IntermediateResults**</span><span class="sxs-lookup"><span data-stu-id="4e320-112">**IntermediateResults**</span></span>](-ianalysisevents-intermediateresults.md) | <span data-ttu-id="4e320-113">當目前的中繼分析階段完成時發生。</span><span class="sxs-lookup"><span data-stu-id="4e320-113">Occurs when the current intermediate analysis stage is finished.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="4e320-114">**ReadyToReconcile**</span><span class="sxs-lookup"><span data-stu-id="4e320-114">**ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)       | <span data-ttu-id="4e320-115">當 [**IInkAnalyzer**](iinkanalyzer.md) 已準備好要將其背景分析結果與目前狀態協調時，就會發生此問題。</span><span class="sxs-lookup"><span data-stu-id="4e320-115">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) is ready to reconcile its background analysis results with its current state.</span></span><br/>                                                  |
| [<span data-ttu-id="4e320-116">**結果**</span><span class="sxs-lookup"><span data-stu-id="4e320-116">**Results**</span></span>](-ianalysisevents-results.md)                         | <span data-ttu-id="4e320-117">在最後一個分析階段完成時發生。</span><span class="sxs-lookup"><span data-stu-id="4e320-117">Occurs when the final analysis stage is finished.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="4e320-118">**UpdateStrokesCache**</span><span class="sxs-lookup"><span data-stu-id="4e320-118">**UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)   | <span data-ttu-id="4e320-119">在 [**IInkAnalyzer**](iinkanalyzer.md) 存取筆劃資料之前發生。</span><span class="sxs-lookup"><span data-stu-id="4e320-119">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) accesses stroke data.</span></span><br/>                                                                                                        |



 

## <a name="requirements"></a><span data-ttu-id="4e320-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e320-120">Requirements</span></span>



| <span data-ttu-id="4e320-121">需求</span><span class="sxs-lookup"><span data-stu-id="4e320-121">Requirement</span></span> | <span data-ttu-id="4e320-122">值</span><span class="sxs-lookup"><span data-stu-id="4e320-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4e320-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e320-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4e320-124">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e320-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4e320-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e320-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4e320-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="4e320-126">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="4e320-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e320-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e320-128">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="4e320-128">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="4e320-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="4e320-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="4e320-130">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="4e320-130">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="4e320-131">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="4e320-131">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="4e320-132">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="4e320-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

