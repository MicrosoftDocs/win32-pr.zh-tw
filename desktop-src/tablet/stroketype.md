---
description: 指出是否應該在繪圖中分析筆劃，或是做為書寫的一部分進行分析。
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: 'StrokeType 列舉 (IACom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrokeType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 3b59be130c6c7055bb7636760451dcadf5acf841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193944"
---
# <a name="stroketype-enumeration"></a><span data-ttu-id="fb275-103">StrokeType 列舉</span><span class="sxs-lookup"><span data-stu-id="fb275-103">StrokeType enumeration</span></span>

<span data-ttu-id="fb275-104">指出是否應該在繪圖中分析筆劃，或是做為書寫的一部分進行分析。</span><span class="sxs-lookup"><span data-stu-id="fb275-104">Indicates whether a stroke should be analyzed as part of a drawing or as part of writing.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb275-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb275-105">Syntax</span></span>


```C++
typedef enum StrokeType { 
  StrokeType_Unclassified  = 0,
  StrokeType_Writing       = 1,
  StrokeType_Drawing       = 2
} StrokeType;
```



## <a name="constants"></a><span data-ttu-id="fb275-106">常數</span><span class="sxs-lookup"><span data-stu-id="fb275-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fb275-107"><span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType 非 \_ 分類**</span><span class="sxs-lookup"><span data-stu-id="fb275-107"><span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType\_Unclassified**</span></span>
</dt> <dd>

<span data-ttu-id="fb275-108">筆劃可能是繪圖或部分書寫的一部分。</span><span class="sxs-lookup"><span data-stu-id="fb275-108">The stroke might be either part of a drawing or part of writing.</span></span>

</dd> <dt>

<span data-ttu-id="fb275-109"><span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**StrokeType \_ 撰寫**</span><span class="sxs-lookup"><span data-stu-id="fb275-109"><span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**StrokeType\_Writing**</span></span>
</dt> <dd>

<span data-ttu-id="fb275-110">筆劃是撰寫的一部分。</span><span class="sxs-lookup"><span data-stu-id="fb275-110">The stroke is part of writing.</span></span>

</dd> <dt>

<span data-ttu-id="fb275-111"><span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**StrokeType \_ 繪圖**</span><span class="sxs-lookup"><span data-stu-id="fb275-111"><span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**StrokeType\_Drawing**</span></span>
</dt> <dd>

<span data-ttu-id="fb275-112">筆觸是繪圖的一部分。</span><span class="sxs-lookup"><span data-stu-id="fb275-112">The stroke is part of a drawing.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="fb275-113">範例</span><span class="sxs-lookup"><span data-stu-id="fb275-113">Examples</span></span>

<span data-ttu-id="fb275-114">下列範例顯示的部分筆觸事件處理常式，是以類似于 [c + + 事件接收器範例](c---event-sinks-sample.md)的方式來執行。</span><span class="sxs-lookup"><span data-stu-id="fb275-114">The following example shows part of a stroke event handler, implemented in a similar fashion to the [C++ Event Sinks Sample](c---event-sinks-sample.md).</span></span> <span data-ttu-id="fb275-115">已檢查新增的筆觸，以查看其周框方塊的頂端是否已繪製在邊界下方 `drawingMargin` 。</span><span class="sxs-lookup"><span data-stu-id="fb275-115">The added stroke is checked to see if the top of its bounding box has been drawn below a margin, `drawingMargin`.</span></span> <span data-ttu-id="fb275-116">如果是，則[](iinkanalyzer.md) `m_spInkAnalyzer` 會將 IInkAnalyzer 物件設定為將筆劃分析為繪圖筆劃，而不是手寫筆劃。</span><span class="sxs-lookup"><span data-stu-id="fb275-116">If so, the [**IInkAnalyzer**](iinkanalyzer.md) object, `m_spInkAnalyzer`, is set to analyze the stroke as a drawing stroke, rather than as a handwriting stroke.</span></span> <span data-ttu-id="fb275-117">`CheckHResult` 是採用和字串的函式 `HRESULT` ，如果 `HRESULT` 不 **成功**，則會擲回以字串建立的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="fb275-117">`CheckHResult` is a function that takes an `HRESULT` and a string, and throws an exception created with the string if the `HRESULT` is not **SUCCESS**.</span></span>


```C++
IInkRectangle* bounds;
CheckHResult(pStroke->GetBoundingBox(IBBM_Default, &bounds), "IInkStrokeDisp::GetBoundingBox failed");
long top;
CheckHResult(bounds->get_Top(&top), "IInkRectangle::get_Top failed");
if (top > drawingMargin)
{
    long strokeId;
    CheckHResult(pStroke->get_ID(&strokeId), "IInkStrokeDisp::get_ID failed");
    m_pInkAnalyzer->SetStrokeType(strokeId, StrokeType_Drawing);
}
```



## <a name="requirements"></a><span data-ttu-id="fb275-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb275-118">Requirements</span></span>



| <span data-ttu-id="fb275-119">需求</span><span class="sxs-lookup"><span data-stu-id="fb275-119">Requirement</span></span> | <span data-ttu-id="fb275-120">值</span><span class="sxs-lookup"><span data-stu-id="fb275-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb275-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb275-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fb275-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb275-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fb275-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb275-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fb275-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="fb275-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fb275-125">標頭</span><span class="sxs-lookup"><span data-stu-id="fb275-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb275-126"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="fb275-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb275-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb275-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb275-128">**IInkAnalyzer：： SetStrokeType 方法**</span><span class="sxs-lookup"><span data-stu-id="fb275-128">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 




