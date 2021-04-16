---
description: 從 IInkAnalyzer 中移除指定的筆觸。
ms.assetid: e182ae35-854e-401d-8e26-aee645c05430
title: 'IInkAnalyzer：： RemoveStroke 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 03952e6e14679c53f7b65f21463fc0457f302b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511652"
---
# <a name="iinkanalyzerremovestroke-method"></a><span data-ttu-id="c71e5-103">IInkAnalyzer：： RemoveStroke 方法</span><span class="sxs-lookup"><span data-stu-id="c71e5-103">IInkAnalyzer::RemoveStroke method</span></span>

<span data-ttu-id="c71e5-104">從 [**IInkAnalyzer**](iinkanalyzer.md)中移除指定的筆觸。</span><span class="sxs-lookup"><span data-stu-id="c71e5-104">Removes the specified stroke from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c71e5-105">語法</span><span class="sxs-lookup"><span data-stu-id="c71e5-105">Syntax</span></span>


```C++
HRESULT RemoveStroke(
  [in] LONG *plStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="c71e5-106">參數</span><span class="sxs-lookup"><span data-stu-id="c71e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c71e5-107">*plStrokeId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c71e5-107">*plStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c71e5-108">筆觸識別碼。</span><span class="sxs-lookup"><span data-stu-id="c71e5-108">The stroke identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c71e5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c71e5-109">Return value</span></span>

<span data-ttu-id="c71e5-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="c71e5-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c71e5-111">備註</span><span class="sxs-lookup"><span data-stu-id="c71e5-111">Remarks</span></span>

<span data-ttu-id="c71e5-112">這個方法會從 [**IInkAnalyzer**](iinkanalyzer.md)中移除指定之筆劃的封包資料和參考。</span><span class="sxs-lookup"><span data-stu-id="c71e5-112">This method removes the packet data for, and references to, the specified stroke from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="c71e5-113">這個方法會從參考筆劃的分葉內容節點移除筆劃。</span><span class="sxs-lookup"><span data-stu-id="c71e5-113">This method removes the stroke from the leaf context node that references the stroke.</span></span> <span data-ttu-id="c71e5-114">如果 [**ICoNtextNode**](icontextnode.md) 不再參考任何筆劃，這個方法會刪除 **ICoNtextNode** ，以及不再有任何子節點的任何上階 **ICoNtextNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="c71e5-114">If the [**IContextNode**](icontextnode.md) no longer references any strokes, this method deletes the **IContextNode** and any ancestor **IContextNode** objects that no longer have any child nodes.</span></span>

<span data-ttu-id="c71e5-115">在這個方法從 [**ICoNtextNode**](icontextnode.md)中移除筆觸之後，它會更新 [**IInkAnalyzer**](iinkanalyzer.md) 物件的中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md) ，) 包含已移除筆劃的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="c71e5-115">After this method removes the stroke from the [**IContextNode**](icontextnode.md), it updates the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) to include the bounding box of the removed stroke.</span></span>

<span data-ttu-id="c71e5-116">如果 *plStrokeId* 未識別與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯的筆劃，這個方法會傳回而不更新筆墨分析器。</span><span class="sxs-lookup"><span data-stu-id="c71e5-116">If *plStrokeId* does not identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the ink analyzer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c71e5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c71e5-117">Requirements</span></span>



| <span data-ttu-id="c71e5-118">需求</span><span class="sxs-lookup"><span data-stu-id="c71e5-118">Requirement</span></span> | <span data-ttu-id="c71e5-119">值</span><span class="sxs-lookup"><span data-stu-id="c71e5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c71e5-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c71e5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c71e5-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c71e5-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c71e5-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c71e5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c71e5-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="c71e5-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c71e5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c71e5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c71e5-125"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="c71e5-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c71e5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c71e5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c71e5-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c71e5-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c71e5-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c71e5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c71e5-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="c71e5-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c71e5-130">**IInkAnalyzer：： AddStroke 方法**</span><span class="sxs-lookup"><span data-stu-id="c71e5-130">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="c71e5-131">**IInkAnalyzer：： AddStrokeForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="c71e5-131">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="c71e5-132">**IInkAnalyzer：： AddStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="c71e5-132">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="c71e5-133">**IInkAnalyzer：： AddStrokesForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="c71e5-133">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="c71e5-134">**IInkAnalyzer：： RemoveStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="c71e5-134">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="c71e5-135">**IInkAnalyzer：： GetDirtyRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="c71e5-135">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="c71e5-136">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="c71e5-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




