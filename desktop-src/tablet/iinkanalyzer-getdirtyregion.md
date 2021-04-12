---
description: 抓取自上次分析作業之後變更的區域。
ms.assetid: 0cd62775-59c6-41f5-957e-709a53a8c257
title: 'IInkAnalyzer：： GetDirtyRegion 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 56f980189e22f50bb832be904933ef0b26d9b54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191405"
---
# <a name="iinkanalyzergetdirtyregion-method"></a><span data-ttu-id="75b17-103">IInkAnalyzer：： GetDirtyRegion 方法</span><span class="sxs-lookup"><span data-stu-id="75b17-103">IInkAnalyzer::GetDirtyRegion method</span></span>

<span data-ttu-id="75b17-104">抓取自上次分析作業之後變更的區域。</span><span class="sxs-lookup"><span data-stu-id="75b17-104">Retrieves the area that has changed since the last analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="75b17-105">語法</span><span class="sxs-lookup"><span data-stu-id="75b17-105">Syntax</span></span>


```C++
HRESULT GetDirtyRegion(
  [out] IAnalysisRegion **ppDirtyRegion
);
```



## <a name="parameters"></a><span data-ttu-id="75b17-106">參數</span><span class="sxs-lookup"><span data-stu-id="75b17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75b17-107">*ppDirtyRegion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="75b17-107">*ppDirtyRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75b17-108">描述自上次分析作業之後變更之區域的 [**IAnalysisRegion**](ianalysisregion.md) 。</span><span class="sxs-lookup"><span data-stu-id="75b17-108">An [**IAnalysisRegion**](ianalysisregion.md) that describes the area that has changed since the last analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75b17-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="75b17-109">Return value</span></span>

<span data-ttu-id="75b17-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="75b17-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="75b17-111">備註</span><span class="sxs-lookup"><span data-stu-id="75b17-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="75b17-112">若要避免記憶體流失，請在 *ppDirtyRegion* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="75b17-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppDirtyRegion* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="75b17-113">這個方法會識別需要分析或重新分析的區域。</span><span class="sxs-lookup"><span data-stu-id="75b17-113">This method identifies the areas that need to be analyzed or reanalyzed.</span></span> <span data-ttu-id="75b17-114">新增、更新或移除筆劃資料的所有 [**IInkAnalyzer**](iinkanalyzer.md) 方法會更新已變更的區域。</span><span class="sxs-lookup"><span data-stu-id="75b17-114">All of the [**IInkAnalyzer**](iinkanalyzer.md) methods that add, update, or remove stroke data update the dirty region.</span></span> <span data-ttu-id="75b17-115">若要手動標記 reanalysis 的區域：</span><span class="sxs-lookup"><span data-stu-id="75b17-115">To manually mark an area for reanalysis:</span></span>

1.  <span data-ttu-id="75b17-116">使用 **IInkAnalyzer：： GetDirtyRegion 方法** 取得中途區域。</span><span class="sxs-lookup"><span data-stu-id="75b17-116">Get the dirty region using **IInkAnalyzer::GetDirtyRegion Method**.</span></span>
2.  <span data-ttu-id="75b17-117">使用 [**IAnalysisRegion：： UnionRegion 方法**](ianalysisregion-unionregion.md) 或 [**IAnalysisRegion：： UnionRectangle 方法**](ianalysisregion-unionrectangle.md) ，將區域新增至步驟1中的區域。</span><span class="sxs-lookup"><span data-stu-id="75b17-117">Use [**IAnalysisRegion::UnionRegion Method**](ianalysisregion-unionregion.md) or [**IAnalysisRegion::UnionRectangle Method**](ianalysisregion-unionrectangle.md) to add the area to the region from step 1.</span></span>
3.  <span data-ttu-id="75b17-118">使用 [**IInkAnalyzer：： SetDirtyRegion 方法**](iinkanalyzer-setdirtyregion.md) 來更新中途區域。</span><span class="sxs-lookup"><span data-stu-id="75b17-118">Use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to update the dirty region.</span></span>

<span data-ttu-id="75b17-119">[**IInkAnalyzer**](iinkanalyzer.md)會在呼叫 [**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)或 [**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)期間，分析其中途區域內的筆墨。</span><span class="sxs-lookup"><span data-stu-id="75b17-119">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span> <span data-ttu-id="75b17-120">不過， **IInkAnalyzer** 可能會擴充分析作業，以包含鄰近區域。</span><span class="sxs-lookup"><span data-stu-id="75b17-120">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="75b17-121">這個屬性可能包含不連續的區域。</span><span class="sxs-lookup"><span data-stu-id="75b17-121">This property may contain nonadjacent areas.</span></span>

<span data-ttu-id="75b17-122">當您完成時，請使用 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) 釋放 *ppDirtyRegion* 陣列中的記憶體。</span><span class="sxs-lookup"><span data-stu-id="75b17-122">Use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory from the *ppDirtyRegion* array when you are finished with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="75b17-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="75b17-123">Requirements</span></span>



| <span data-ttu-id="75b17-124">需求</span><span class="sxs-lookup"><span data-stu-id="75b17-124">Requirement</span></span> | <span data-ttu-id="75b17-125">值</span><span class="sxs-lookup"><span data-stu-id="75b17-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75b17-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75b17-126">Minimum supported client</span></span><br/> | <span data-ttu-id="75b17-127">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75b17-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="75b17-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75b17-128">Minimum supported server</span></span><br/> | <span data-ttu-id="75b17-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="75b17-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="75b17-130">標頭</span><span class="sxs-lookup"><span data-stu-id="75b17-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="75b17-131"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="75b17-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="75b17-132">DLL</span><span class="sxs-lookup"><span data-stu-id="75b17-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75b17-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75b17-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="75b17-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75b17-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b17-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="75b17-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="75b17-136">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="75b17-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="75b17-137">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="75b17-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="75b17-138">**IInkAnalyzer：： AddStroke 方法**</span><span class="sxs-lookup"><span data-stu-id="75b17-138">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="75b17-139">**IInkAnalyzer：： AddStrokeForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="75b17-139">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="75b17-140">**IInkAnalyzer：： AddStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="75b17-140">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="75b17-141">**IInkAnalyzer：： AddStrokesForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="75b17-141">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="75b17-142">**IInkAnalyzer：： RemoveStroke 方法**</span><span class="sxs-lookup"><span data-stu-id="75b17-142">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="75b17-143">**IInkAnalyzer：： RemoveStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="75b17-143">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="75b17-144">**IInkAnalyzer：： UpdateStrokesData 方法**</span><span class="sxs-lookup"><span data-stu-id="75b17-144">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="75b17-145">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="75b17-145">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

