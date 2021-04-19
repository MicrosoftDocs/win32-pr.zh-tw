---
description: 時間軸 \_ 主要 \_ 類型列舉會指定物件的主要類型。
ms.assetid: 1a5fde83-2a0a-4bcf-bffe-340a9d914885
title: 'TIMELINE_MAJOR_TYPE 列舉 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TIMELINE_MAJOR_TYPE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 25c3e829aa73d1da78c110ffd148fb0ebaaebdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992556"
---
# <a name="timeline_major_type-enumeration"></a><span data-ttu-id="1d4db-103">時間軸 \_ 主要 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="1d4db-103">TIMELINE\_MAJOR\_TYPE enumeration</span></span>

> [!Note]  
> <span data-ttu-id="1d4db-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="1d4db-104">\[Deprecated.</span></span> <span data-ttu-id="1d4db-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="1d4db-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1d4db-106">`TIMELINE_MAJOR_TYPE`列舉會指定物件的主要類型。</span><span class="sxs-lookup"><span data-stu-id="1d4db-106">The `TIMELINE_MAJOR_TYPE` enumeration specifies the major type of an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d4db-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d4db-107">Syntax</span></span>


```C++
typedef enum  { 
  TIMELINE_MAJOR_TYPE_COMPOSITE   = 1,
  TIMELINE_MAJOR_TYPE_TRACK       = 2,
  TIMELINE_MAJOR_TYPE_SOURCE      = 4,
  TIMELINE_MAJOR_TYPE_TRANSITION  = 8,
  TIMELINE_MAJOR_TYPE_EFFECT      = 16,
  TIMELINE_MAJOR_TYPE_GROUP       = 128
} TIMELINE_MAJOR_TYPE;
```



## <a name="constants"></a><span data-ttu-id="1d4db-108">常數</span><span class="sxs-lookup"><span data-stu-id="1d4db-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1d4db-109"><span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**時間軸 \_ 主要 \_ 類型 \_ 複合**</span><span class="sxs-lookup"><span data-stu-id="1d4db-109"><span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**TIMELINE\_MAJOR\_TYPE\_COMPOSITE**</span></span>
</dt> <dd>

<span data-ttu-id="1d4db-110">綜合物件。</span><span class="sxs-lookup"><span data-stu-id="1d4db-110">Composite object.</span></span> <span data-ttu-id="1d4db-111">保存一或多個曲目。</span><span class="sxs-lookup"><span data-stu-id="1d4db-111">Holds one or more tracks.</span></span>

</dd> <dt>

<span data-ttu-id="1d4db-112"><span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**時間軸 \_ 主要 \_ 類型 \_ 追蹤**</span><span class="sxs-lookup"><span data-stu-id="1d4db-112"><span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**TIMELINE\_MAJOR\_TYPE\_TRACK**</span></span>
</dt> <dd>

<span data-ttu-id="1d4db-113">追蹤物件。</span><span class="sxs-lookup"><span data-stu-id="1d4db-113">Track object.</span></span> <span data-ttu-id="1d4db-114">保存一或多個來源。</span><span class="sxs-lookup"><span data-stu-id="1d4db-114">Holds one or more sources.</span></span>

</dd> <dt>

<span data-ttu-id="1d4db-115"><span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**時間軸 \_ 主要 \_ 類型 \_ 來源**</span><span class="sxs-lookup"><span data-stu-id="1d4db-115"><span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**TIMELINE\_MAJOR\_TYPE\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="1d4db-116">來源物件。</span><span class="sxs-lookup"><span data-stu-id="1d4db-116">Source object.</span></span> <span data-ttu-id="1d4db-117">包含媒體來源的參考。</span><span class="sxs-lookup"><span data-stu-id="1d4db-117">Contains a reference to a media source.</span></span>

</dd> <dt>

<span data-ttu-id="1d4db-118"><span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**時間軸 \_ 主要 \_ 類型 \_ 轉換**</span><span class="sxs-lookup"><span data-stu-id="1d4db-118"><span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**TIMELINE\_MAJOR\_TYPE\_TRANSITION**</span></span>
</dt> <dd>

<span data-ttu-id="1d4db-119">轉換物件。</span><span class="sxs-lookup"><span data-stu-id="1d4db-119">Transition object.</span></span> <span data-ttu-id="1d4db-120">定義複合、追蹤或來源之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="1d4db-120">Defines a transition between composites, tracks, or sources.</span></span>

</dd> <dt>

<span data-ttu-id="1d4db-121"><span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**時間軸 \_ 主要 \_ 類型 \_ 效果**</span><span class="sxs-lookup"><span data-stu-id="1d4db-121"><span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**TIMELINE\_MAJOR\_TYPE\_EFFECT**</span></span>
</dt> <dd>

<span data-ttu-id="1d4db-122">效果物件。</span><span class="sxs-lookup"><span data-stu-id="1d4db-122">Effect object.</span></span> <span data-ttu-id="1d4db-123">定義要套用至複合、追蹤或來源物件的單一輸入效果。</span><span class="sxs-lookup"><span data-stu-id="1d4db-123">Defines a single-input effect to be applied to a composite, track, or source object.</span></span>

</dd> <dt>

<span data-ttu-id="1d4db-124"><span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**時間軸 \_ 主要 \_ 類型 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="1d4db-124"><span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**TIMELINE\_MAJOR\_TYPE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="1d4db-125">群組物件。</span><span class="sxs-lookup"><span data-stu-id="1d4db-125">Group object.</span></span> <span data-ttu-id="1d4db-126">包含一或多個指定類型的軌跡。</span><span class="sxs-lookup"><span data-stu-id="1d4db-126">Contains one or more tracks of a given type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d4db-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d4db-127">Requirements</span></span>



| <span data-ttu-id="1d4db-128">需求</span><span class="sxs-lookup"><span data-stu-id="1d4db-128">Requirement</span></span> | <span data-ttu-id="1d4db-129">值</span><span class="sxs-lookup"><span data-stu-id="1d4db-129">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1d4db-130">標頭</span><span class="sxs-lookup"><span data-stu-id="1d4db-130">Header</span></span><br/> | <dl> <span data-ttu-id="1d4db-131"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="1d4db-131"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d4db-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d4db-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d4db-133">**IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="1d4db-133">**IAMTimeline**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="1d4db-134">**IAMTimelineComp::GetCountOfType**</span><span class="sxs-lookup"><span data-stu-id="1d4db-134">**IAMTimelineComp::GetCountOfType**</span></span>](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[<span data-ttu-id="1d4db-135">**IAMTimelineObj::GetTimelineType**</span><span class="sxs-lookup"><span data-stu-id="1d4db-135">**IAMTimelineObj::GetTimelineType**</span></span>](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




