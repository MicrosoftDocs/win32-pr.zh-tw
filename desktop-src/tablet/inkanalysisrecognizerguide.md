---
description: 指定用來繪製和辨識筆墨的節目表或區域。
ms.assetid: 5bd874ff-003b-4471-b4ef-50731007dc5a
title: 'InkAnalysisRecognizerGuide 結構 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerGuide
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: eab5b1d09354f021f2c0a7e66a41b53e761d51e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970801"
---
# <a name="inkanalysisrecognizerguide-structure"></a><span data-ttu-id="51f44-103">InkAnalysisRecognizerGuide 結構</span><span class="sxs-lookup"><span data-stu-id="51f44-103">InkAnalysisRecognizerGuide structure</span></span>

<span data-ttu-id="51f44-104">指定用來繪製和辨識筆墨的節目表或區域。</span><span class="sxs-lookup"><span data-stu-id="51f44-104">Specifies the guide, or area where ink is drawn and recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="51f44-105">語法</span><span class="sxs-lookup"><span data-stu-id="51f44-105">Syntax</span></span>


```C++
typedef struct InkAnalysisRecognizerGuide {
  RECT rectWritingBox;
  RECT rectDrawnBox;
  long cRows;
  long cColumns;
  long midline;
} InkAnalysisRecognizerGuide;
```



## <a name="members"></a><span data-ttu-id="51f44-106">成員</span><span class="sxs-lookup"><span data-stu-id="51f44-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="51f44-107">**rectWritingBox**</span><span class="sxs-lookup"><span data-stu-id="51f44-107">**rectWritingBox**</span></span>
</dt> <dd>

<span data-ttu-id="51f44-108">辨識指南中的不可見書寫區域，其實可以進行寫入。</span><span class="sxs-lookup"><span data-stu-id="51f44-108">The invisible writing area of the recognition guide in which writing can actually take place.</span></span>

</dd> <dt>

<span data-ttu-id="51f44-109">**rectDrawnBox**</span><span class="sxs-lookup"><span data-stu-id="51f44-109">**rectDrawnBox**</span></span>
</dt> <dd>

<span data-ttu-id="51f44-110">在平板電腦螢幕上繪製的矩形，以及進行寫入的位置。</span><span class="sxs-lookup"><span data-stu-id="51f44-110">The rectangle that is drawn on the tablet screen and in which writing takes place.</span></span>

</dd> <dt>

<span data-ttu-id="51f44-111">**烏鴉**</span><span class="sxs-lookup"><span data-stu-id="51f44-111">**cRows**</span></span>
</dt> <dd>

<span data-ttu-id="51f44-112">[辨識指南] 方塊中的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="51f44-112">The number of rows in the recognition guide box.</span></span>

</dd> <dt>

<span data-ttu-id="51f44-113">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="51f44-113">**cColumns**</span></span>
</dt> <dd>

<span data-ttu-id="51f44-114">[辨識指南] 方塊中的資料行數目。</span><span class="sxs-lookup"><span data-stu-id="51f44-114">The number of columns in the recognition guide box.</span></span>

</dd> <dt>

<span data-ttu-id="51f44-115">**中線**</span><span class="sxs-lookup"><span data-stu-id="51f44-115">**midline**</span></span>
</dt> <dd>

<span data-ttu-id="51f44-116">辨識指南方塊的中線高度。</span><span class="sxs-lookup"><span data-stu-id="51f44-116">The midline height of the recognition guide box.</span></span> <span data-ttu-id="51f44-117">中線高度是繪製方塊的距離，從基準到中線的距離。</span><span class="sxs-lookup"><span data-stu-id="51f44-117">The midline height is the distance from the baseline to the midline, of the drawn box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51f44-118">備註</span><span class="sxs-lookup"><span data-stu-id="51f44-118">Remarks</span></span>

<span data-ttu-id="51f44-119">**InkAnalysisRecognizerGuide** 會針對字元定義預期的輸入區域，例如行或方塊。</span><span class="sxs-lookup"><span data-stu-id="51f44-119">An **InkAnalysisRecognizerGuide** defines an expected area of input, such as a line or boxes, for characters.</span></span> <span data-ttu-id="51f44-120">**InkAnalysisRecognizerGuide** 結構只能在分析提示內容節點上設定 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 。</span><span class="sxs-lookup"><span data-stu-id="51f44-120">An **InkAnalysisRecognizerGuide** structure can be set only on an analysis hint context node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="51f44-121">[**IInkAnalyzer**](iinkanalyzer.md)會流量分析提示節點的位置和筆墨筆劃的位置，以將筆劃與分析提示節點產生關聯。</span><span class="sxs-lookup"><span data-stu-id="51f44-121">The [**IInkAnalyzer**](iinkanalyzer.md) uses the location of the analysis hint node and the locations of the ink strokes to associate a stroke with the analysis hint node.</span></span> <span data-ttu-id="51f44-122">如果 **IInkAnalyzer** 支援 **InkAnalysisRecognizerGuide**，則任何與分析提示節點相關聯的筆劃都將具有指定的 **InkAnalysisRecognizerGuide** ，以供 **IInkAnalyzer** 辨識。</span><span class="sxs-lookup"><span data-stu-id="51f44-122">Any strokes with an association to the analysis hint node will have the specified **InkAnalysisRecognizerGuide** used when recognized by an **IInkAnalyzer**, provided the **IInkAnalyzer** supports the **InkAnalysisRecognizerGuide**.</span></span> <span data-ttu-id="51f44-123">**InkAnalysisRecognizerGuide** 類別中表示的值一律相對於分析提示節點的位置，並且以筆墨空間座標指定。</span><span class="sxs-lookup"><span data-stu-id="51f44-123">The values expressed in the **InkAnalysisRecognizerGuide** class are always relative to the location of the analysis hint node and are specified in ink space coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="51f44-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="51f44-124">Requirements</span></span>



| <span data-ttu-id="51f44-125">需求</span><span class="sxs-lookup"><span data-stu-id="51f44-125">Requirement</span></span> | <span data-ttu-id="51f44-126">值</span><span class="sxs-lookup"><span data-stu-id="51f44-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51f44-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51f44-127">Minimum supported client</span></span><br/> | <span data-ttu-id="51f44-128">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51f44-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="51f44-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51f44-129">Minimum supported server</span></span><br/> | <span data-ttu-id="51f44-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="51f44-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="51f44-131">標頭</span><span class="sxs-lookup"><span data-stu-id="51f44-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="51f44-132"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="51f44-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51f44-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51f44-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51f44-134">分析提示屬性</span><span class="sxs-lookup"><span data-stu-id="51f44-134">Analysis Hint Properties</span></span>](analysis-hint-properties.md)
</dt> <dt>

[<span data-ttu-id="51f44-135">**IInkAnalyzer：： CreateAnalysisHint 方法**</span><span class="sxs-lookup"><span data-stu-id="51f44-135">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="51f44-136">**ICoNtextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="51f44-136">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="51f44-137">**ICoNtextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="51f44-137">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="51f44-138">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="51f44-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




