---
description: 從 IInkAnalyzer 中移除指定的筆觸。
ms.assetid: ea7c8a9f-a427-4781-b5ba-97ffd983dbe5
title: 'IInkAnalyzer：： RemoveStrokes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 00f065e01f9a4ff1459988d76fc9393ba24aa894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113333"
---
# <a name="iinkanalyzerremovestrokes-method"></a><span data-ttu-id="238aa-103">IInkAnalyzer：： RemoveStrokes 方法</span><span class="sxs-lookup"><span data-stu-id="238aa-103">IInkAnalyzer::RemoveStrokes method</span></span>

<span data-ttu-id="238aa-104">從 [**IInkAnalyzer**](iinkanalyzer.md)中移除指定的筆觸。</span><span class="sxs-lookup"><span data-stu-id="238aa-104">Removes the specified strokes from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="238aa-105">語法</span><span class="sxs-lookup"><span data-stu-id="238aa-105">Syntax</span></span>


```C++
HRESULT RemoveStrokes(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes
);
```



## <a name="parameters"></a><span data-ttu-id="238aa-106">參數</span><span class="sxs-lookup"><span data-stu-id="238aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="238aa-107">*ulStrokeIdCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="238aa-107">*ulStrokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="238aa-108">*PlStrokes* 中的筆觸識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="238aa-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="238aa-109">*plStrokes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="238aa-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="238aa-110">要移除之筆劃的識別碼。</span><span class="sxs-lookup"><span data-stu-id="238aa-110">The identifiers for the strokes to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="238aa-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="238aa-111">Return value</span></span>

<span data-ttu-id="238aa-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="238aa-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="238aa-113">備註</span><span class="sxs-lookup"><span data-stu-id="238aa-113">Remarks</span></span>

<span data-ttu-id="238aa-114">這個方法會從 [**IInkAnalyzer**](iinkanalyzer.md)中移除指定之筆劃的封包資料和參考。</span><span class="sxs-lookup"><span data-stu-id="238aa-114">This method removes the packet data for and references to the specified strokes from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="238aa-115">這個方法會從參考筆觸的分葉內容節點移除筆劃。</span><span class="sxs-lookup"><span data-stu-id="238aa-115">This method removes the strokes from the leaf context node that references the strokes.</span></span> <span data-ttu-id="238aa-116">如果任何 [**ICoNtextNode**](icontextnode.md) 不再參考任何筆劃，這個方法會刪除 **ICoNtextNode** ，以及不再有任何子節點的任何上階 **ICoNtextNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="238aa-116">If any [**IContextNode**](icontextnode.md) no longer references any strokes, this method deletes the **IContextNode** and any ancestor **IContextNode** objects that no longer have any child nodes.</span></span>

<span data-ttu-id="238aa-117">在這個方法從 [**ICoNtextNode**](icontextnode.md)中移除筆觸之後，它會更新 [**IInkAnalyzer**](iinkanalyzer.md) 物件的中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md) ，) 包含已移除筆劃的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="238aa-117">After this method removes the strokes from the [**IContextNode**](icontextnode.md), it updates the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) to include the bounding box of the removed strokes.</span></span>

<span data-ttu-id="238aa-118">如果在 *plStrokes* 中識別的筆劃沒有與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯，這個方法會忽略識別碼。</span><span class="sxs-lookup"><span data-stu-id="238aa-118">If a stroke identified in *plStrokes* is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="238aa-119">如果 *plStrokes* 中識別的筆劃都沒有與筆墨分析器相關聯，這個方法會傳回而不更新 [**IInkAnalyzer**](iinkanalyzer.md)。</span><span class="sxs-lookup"><span data-stu-id="238aa-119">If none of the strokes identified in *plStrokes* are associated with the ink analyzer, this method returns without updating the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="238aa-120">當 *plStrokes* 為 null 時，這個方法會傳回錯誤碼和錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="238aa-120">This method returns and error code when *plStrokes* is null.</span></span>

## <a name="requirements"></a><span data-ttu-id="238aa-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="238aa-121">Requirements</span></span>



| <span data-ttu-id="238aa-122">需求</span><span class="sxs-lookup"><span data-stu-id="238aa-122">Requirement</span></span> | <span data-ttu-id="238aa-123">值</span><span class="sxs-lookup"><span data-stu-id="238aa-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="238aa-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="238aa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="238aa-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="238aa-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="238aa-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="238aa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="238aa-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="238aa-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="238aa-128">標頭</span><span class="sxs-lookup"><span data-stu-id="238aa-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="238aa-129"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="238aa-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="238aa-130">DLL</span><span class="sxs-lookup"><span data-stu-id="238aa-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="238aa-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="238aa-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="238aa-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="238aa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="238aa-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="238aa-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="238aa-134">**IInkAnalyzer：： AddStroke 方法**</span><span class="sxs-lookup"><span data-stu-id="238aa-134">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="238aa-135">**IInkAnalyzer：： AddStrokeForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="238aa-135">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="238aa-136">**IInkAnalyzer：： AddStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="238aa-136">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="238aa-137">**IInkAnalyzer：： AddStrokesForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="238aa-137">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="238aa-138">**IInkAnalyzer：： RemoveStroke 方法**</span><span class="sxs-lookup"><span data-stu-id="238aa-138">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="238aa-139">**IInkAnalyzer：： GetDirtyRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="238aa-139">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="238aa-140">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="238aa-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




