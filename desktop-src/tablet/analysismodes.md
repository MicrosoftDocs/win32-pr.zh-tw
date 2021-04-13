---
description: 指定 IInkAnalyzer 執行筆墨分析的方式。
ms.assetid: bc526445-0c9c-4c53-8b02-32cf758266e6
title: 'AnalysisModes 列舉 (IACom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisModes
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b9fdebd3ef3cd505b49ff6c82f7609bc339af0a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386014"
---
# <a name="analysismodes-enumeration"></a><span data-ttu-id="1fe09-103">AnalysisModes 列舉</span><span class="sxs-lookup"><span data-stu-id="1fe09-103">AnalysisModes enumeration</span></span>

<span data-ttu-id="1fe09-104">指定 [**IInkAnalyzer**](iinkanalyzer.md) 執行筆墨分析的方式。</span><span class="sxs-lookup"><span data-stu-id="1fe09-104">Specifies how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fe09-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fe09-105">Syntax</span></span>


```C++
typedef enum AnalysisModes { 
  AnalysisModes_None                     = 0x0000,
  AnalysisModes_AutomaticReconciliation  = 0x0002,
  AnalysisModes_StrokeCacheAutoCleanup   = 0x0004,
  AnalysisModes_PersonalizationEnabled   = 0x0008,
  AnalysisModes_Default                  = 0x000d
} AnalysisModes;
```



## <a name="constants"></a><span data-ttu-id="1fe09-106">常數</span><span class="sxs-lookup"><span data-stu-id="1fe09-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1fe09-107"><span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes \_ 無**</span><span class="sxs-lookup"><span data-stu-id="1fe09-107"><span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes\_None**</span></span>
</dt> <dd>

<span data-ttu-id="1fe09-108">未指定任何模式。</span><span class="sxs-lookup"><span data-stu-id="1fe09-108">No modes are specified.</span></span>

</dd> <dt>

<span data-ttu-id="1fe09-109"><span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**AnalysisModes \_ AutomaticReconciliation**</span><span class="sxs-lookup"><span data-stu-id="1fe09-109"><span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**AnalysisModes\_AutomaticReconciliation**</span></span>
</dt> <dd>

<span data-ttu-id="1fe09-110">[**IInkAnalyzer**](iinkanalyzer.md)是否會在中繼或最終結果就緒時，立即自動啟動對帳作業。</span><span class="sxs-lookup"><span data-stu-id="1fe09-110">Whether the [**IInkAnalyzer**](iinkanalyzer.md) automatically starts the reconciliation operation as soon as the intermediate or final results are ready.</span></span>

<span data-ttu-id="1fe09-111">如果啟用此模式，則不會引發 [**\_ IAnalysisEvents：： ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)事件。</span><span class="sxs-lookup"><span data-stu-id="1fe09-111">If this mode is enabled, the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event is not raised.</span></span> <span data-ttu-id="1fe09-112">如果停用此模式，則會引發 **\_ IAnalysisEvents：： ReadyToReconcile** 事件。</span><span class="sxs-lookup"><span data-stu-id="1fe09-112">If this mode is disabled, the **\_IAnalysisEvents::ReadyToReconcile** event is raised.</span></span>

</dd> <dt>

<span data-ttu-id="1fe09-113"><span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**AnalysisModes \_ StrokeCacheAutoCleanup**</span><span class="sxs-lookup"><span data-stu-id="1fe09-113"><span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**AnalysisModes\_StrokeCacheAutoCleanup**</span></span>
</dt> <dd>

<span data-ttu-id="1fe09-114">[**IInkAnalyzer**](iinkanalyzer.md)是否會在執行分析之前，自動從筆劃快取清除不需要的筆觸。</span><span class="sxs-lookup"><span data-stu-id="1fe09-114">Whether the [**IInkAnalyzer**](iinkanalyzer.md) automatically clears unneeded strokes from the stroke cache before performing analysis.</span></span>

<span data-ttu-id="1fe09-115">如果啟用此模式， [**IInkAnalyzer**](iinkanalyzer.md) 會在執行分析之前清除筆觸資料。</span><span class="sxs-lookup"><span data-stu-id="1fe09-115">If this mode is enabled, the [**IInkAnalyzer**](iinkanalyzer.md) clears the stroke data before performing analysis.</span></span> <span data-ttu-id="1fe09-116">您的程式碼也必須處理 [**\_ IAnalysisEvents：： UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)事件。</span><span class="sxs-lookup"><span data-stu-id="1fe09-116">Your code must also then handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span> <span data-ttu-id="1fe09-117">如果未處理 **\_ IAnalysisEvents：： UpdateStrokesCache** 事件，則會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="1fe09-117">If the **\_IAnalysisEvents::UpdateStrokesCache** event is not handled, an exception is raised.</span></span> <span data-ttu-id="1fe09-118">這項檢查是在 [分析 (] 或 [BackgroundAnalyze]) 和 [對帳] 階段完成。</span><span class="sxs-lookup"><span data-stu-id="1fe09-118">This check is done both at the Analyze (or BackgroundAnalyze) and Reconciliation phases.</span></span>

<span data-ttu-id="1fe09-119">如果停用此模式，則 [**IInkAnalyzer**](iinkanalyzer.md) 不會清除筆觸資料。</span><span class="sxs-lookup"><span data-stu-id="1fe09-119">If this mode is disabled, the [**IInkAnalyzer**](iinkanalyzer.md) does not clear the stroke data.</span></span> <span data-ttu-id="1fe09-120">若要清除筆觸資料，請呼叫 [**IInkAnalyzer：： ClearStrokeData 方法**](iinkanalyzer-clearstrokedata.md)。</span><span class="sxs-lookup"><span data-stu-id="1fe09-120">To clear the stroke data, call [**IInkAnalyzer::ClearStrokeData Method**](iinkanalyzer-clearstrokedata.md).</span></span> <span data-ttu-id="1fe09-121">如果此模式已停用，則會引發 [**\_ IAnalysisEvents：： UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)事件，讓 **IInkAnalyzer** 可以針對已清除快取的任何筆劃取得最新的筆劃資料。</span><span class="sxs-lookup"><span data-stu-id="1fe09-121">If this mode is disabled, the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event is raised so the **IInkAnalyzer** can retrieve the latest stroke data for any strokes that have had their cache cleared.</span></span> <span data-ttu-id="1fe09-122">如果已清除筆觸快取，但未處理 **\_ IAnalysisEvents：： UpdateStrokesCache** 事件，則會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="1fe09-122">If the stroke cache is cleared, but the **\_IAnalysisEvents::UpdateStrokesCache** event is not handled, an exception is raised.</span></span>

</dd> <dt>

<span data-ttu-id="1fe09-123"><span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes \_ PersonalizationEnabled**</span><span class="sxs-lookup"><span data-stu-id="1fe09-123"><span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes\_PersonalizationEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="1fe09-124">已啟用手寫辨識的個人化。</span><span class="sxs-lookup"><span data-stu-id="1fe09-124">Personalization of handwriting recognition is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="1fe09-125"><span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**AnalysisModes \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="1fe09-125"><span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**AnalysisModes\_Default**</span></span>
</dt> <dd>

<span data-ttu-id="1fe09-126">所有模式都會啟用。</span><span class="sxs-lookup"><span data-stu-id="1fe09-126">All modes are enabled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fe09-127">備註</span><span class="sxs-lookup"><span data-stu-id="1fe09-127">Remarks</span></span>

<span data-ttu-id="1fe09-128">此列舉允許其成員值的位元組合。</span><span class="sxs-lookup"><span data-stu-id="1fe09-128">This enumeration allows a bitwise combination of its member values.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fe09-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fe09-129">Requirements</span></span>



| <span data-ttu-id="1fe09-130">需求</span><span class="sxs-lookup"><span data-stu-id="1fe09-130">Requirement</span></span> | <span data-ttu-id="1fe09-131">值</span><span class="sxs-lookup"><span data-stu-id="1fe09-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fe09-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1fe09-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1fe09-133">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1fe09-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1fe09-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1fe09-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1fe09-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="1fe09-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1fe09-136">標頭</span><span class="sxs-lookup"><span data-stu-id="1fe09-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fe09-137"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="1fe09-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fe09-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fe09-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fe09-139">**IInkAnalyzer：： GetAnalysisModes 方法**</span><span class="sxs-lookup"><span data-stu-id="1fe09-139">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="1fe09-140">**IInkAnalyzer：： SetAnalysisModes 方法**</span><span class="sxs-lookup"><span data-stu-id="1fe09-140">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="1fe09-141">**\_IAnalysisEvents::IntermediateResults**</span><span class="sxs-lookup"><span data-stu-id="1fe09-141">**\_IAnalysisEvents::IntermediateResults**</span></span>](-ianalysisevents-intermediateresults.md)
</dt> <dt>

[<span data-ttu-id="1fe09-142">**\_IAnalysisEvents::ReadyToReconcile**</span><span class="sxs-lookup"><span data-stu-id="1fe09-142">**\_IAnalysisEvents::ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[<span data-ttu-id="1fe09-143">**\_IAnalysisEvents::UpdateStrokesCache**</span><span class="sxs-lookup"><span data-stu-id="1fe09-143">**\_IAnalysisEvents::UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[<span data-ttu-id="1fe09-144">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="1fe09-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




