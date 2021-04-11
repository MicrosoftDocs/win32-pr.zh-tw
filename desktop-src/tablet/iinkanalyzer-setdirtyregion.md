---
description: 修改自上次分析作業之後變更的區域。
ms.assetid: 1484fd96-2791-4583-b13b-e5a8275ecb0e
title: 'IInkAnalyzer：： SetDirtyRegion 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 72278dd9fe1d772d4ef340d25694d42f9c48ed7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113324"
---
# <a name="iinkanalyzersetdirtyregion-method"></a><span data-ttu-id="68dc1-103">IInkAnalyzer：： SetDirtyRegion 方法</span><span class="sxs-lookup"><span data-stu-id="68dc1-103">IInkAnalyzer::SetDirtyRegion method</span></span>

<span data-ttu-id="68dc1-104">修改自上次分析作業之後變更的區域。</span><span class="sxs-lookup"><span data-stu-id="68dc1-104">Modifies the area that has changed since the last analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="68dc1-105">語法</span><span class="sxs-lookup"><span data-stu-id="68dc1-105">Syntax</span></span>


```C++
HRESULT SetDirtyRegion(
  [in] IAnalysisRegion *pDirtyRegion
);
```



## <a name="parameters"></a><span data-ttu-id="68dc1-106">參數</span><span class="sxs-lookup"><span data-stu-id="68dc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68dc1-107">*pDirtyRegion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68dc1-107">*pDirtyRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68dc1-108">描述自上次分析作業之後變更之區域的 [**IAnalysisRegion**](ianalysisregion.md) 。</span><span class="sxs-lookup"><span data-stu-id="68dc1-108">An [**IAnalysisRegion**](ianalysisregion.md) that describes the area that has changed since the last analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68dc1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="68dc1-109">Return value</span></span>

<span data-ttu-id="68dc1-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="68dc1-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="68dc1-111">備註</span><span class="sxs-lookup"><span data-stu-id="68dc1-111">Remarks</span></span>

<span data-ttu-id="68dc1-112">這個方法會識別需要分析或重新分析的區域。</span><span class="sxs-lookup"><span data-stu-id="68dc1-112">This method identifies the areas that need to be analyzed or reanalyzed.</span></span> <span data-ttu-id="68dc1-113">新增、更新或移除筆劃資料的所有 [**IInkAnalyzer**](iinkanalyzer.md) 方法會更新已變更的區域。</span><span class="sxs-lookup"><span data-stu-id="68dc1-113">All of the [**IInkAnalyzer**](iinkanalyzer.md) methods that add, update, or remove stroke data update the dirty region.</span></span> <span data-ttu-id="68dc1-114">若要手動標記 reanalysis 的區域：</span><span class="sxs-lookup"><span data-stu-id="68dc1-114">To manually mark an area for reanalysis:</span></span>

1.  <span data-ttu-id="68dc1-115">使用 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)取得中途區域。</span><span class="sxs-lookup"><span data-stu-id="68dc1-115">Get the dirty region using [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md).</span></span>
2.  <span data-ttu-id="68dc1-116">使用 [**IAnalysisRegion：： UnionRegion 方法**](ianalysisregion-unionregion.md) 或 [**IAnalysisRegion：： UnionRectangle 方法**](ianalysisregion-unionrectangle.md) ，將區域新增至步驟1中的區域。</span><span class="sxs-lookup"><span data-stu-id="68dc1-116">Use [**IAnalysisRegion::UnionRegion Method**](ianalysisregion-unionregion.md) or [**IAnalysisRegion::UnionRectangle Method**](ianalysisregion-unionrectangle.md) to add the area to the region from step 1.</span></span>
3.  <span data-ttu-id="68dc1-117">使用 **IInkAnalyzer：： SetDirtyRegion 方法** 來更新中途區域。</span><span class="sxs-lookup"><span data-stu-id="68dc1-117">Use **IInkAnalyzer::SetDirtyRegion Method** to update the dirty region.</span></span>

<span data-ttu-id="68dc1-118">[**IInkAnalyzer**](iinkanalyzer.md)會在呼叫 [**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)或 [**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)期間，分析其中途區域內的筆墨。</span><span class="sxs-lookup"><span data-stu-id="68dc1-118">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span> <span data-ttu-id="68dc1-119">不過， **IInkAnalyzer** 可能會擴充分析作業，以包含鄰近區域。</span><span class="sxs-lookup"><span data-stu-id="68dc1-119">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

## <a name="requirements"></a><span data-ttu-id="68dc1-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="68dc1-120">Requirements</span></span>



| <span data-ttu-id="68dc1-121">需求</span><span class="sxs-lookup"><span data-stu-id="68dc1-121">Requirement</span></span> | <span data-ttu-id="68dc1-122">值</span><span class="sxs-lookup"><span data-stu-id="68dc1-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68dc1-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68dc1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="68dc1-124">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68dc1-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="68dc1-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68dc1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="68dc1-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="68dc1-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="68dc1-127">標頭</span><span class="sxs-lookup"><span data-stu-id="68dc1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="68dc1-128"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="68dc1-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="68dc1-129">DLL</span><span class="sxs-lookup"><span data-stu-id="68dc1-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68dc1-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68dc1-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="68dc1-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68dc1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68dc1-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="68dc1-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="68dc1-133">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="68dc1-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="68dc1-134">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="68dc1-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="68dc1-135">**IInkAnalyzer：： AddStroke 方法**</span><span class="sxs-lookup"><span data-stu-id="68dc1-135">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="68dc1-136">**IInkAnalyzer：： AddStrokeForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="68dc1-136">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="68dc1-137">**IInkAnalyzer：： AddStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="68dc1-137">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="68dc1-138">**IInkAnalyzer：： AddStrokesForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="68dc1-138">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="68dc1-139">**IInkAnalyzer：： RemoveStroke 方法**</span><span class="sxs-lookup"><span data-stu-id="68dc1-139">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="68dc1-140">**IInkAnalyzer：： RemoveStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="68dc1-140">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="68dc1-141">**IInkAnalyzer：： UpdateStrokesData 方法**</span><span class="sxs-lookup"><span data-stu-id="68dc1-141">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="68dc1-142">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="68dc1-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




