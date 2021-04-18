---
description: DEXTERF \_ TRACK \_ 搜尋 \_ 旗標列舉會指定在時間軸中搜尋物件的界限條件。
ms.assetid: 9a66ea17-5c2c-41fd-8a7b-c9918b10c8c9
title: 'DEXTERF_TRACK_SEARCH_FLAGS 列舉 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTERF_TRACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 09923d6be01bdf4a213db645a34b038dda15d86f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976171"
---
# <a name="dexterf_track_search_flags-enumeration"></a><span data-ttu-id="9029b-103">DEXTERF \_ 追蹤 \_ 搜尋 \_ 旗標列舉</span><span class="sxs-lookup"><span data-stu-id="9029b-103">DEXTERF\_TRACK\_SEARCH\_FLAGS enumeration</span></span>

> [!Note]  
> <span data-ttu-id="9029b-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="9029b-104">\[Deprecated.</span></span> <span data-ttu-id="9029b-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="9029b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9029b-106">`DEXTERF_TRACK_SEARCH_FLAGS`列舉會指定在時間軸中搜尋物件的界限條件。</span><span class="sxs-lookup"><span data-stu-id="9029b-106">The `DEXTERF_TRACK_SEARCH_FLAGS` enumeration specifies the boundary conditions on a search for an object in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="9029b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9029b-107">Syntax</span></span>


```C++
typedef enum  { 
  DEXTERF_BOUNDING    = -1,
  DEXTERF_EXACTLY_AT  = 0,
  DEXTERF_FORWARDS    = 1
} DEXTERF_TRACK_SEARCH_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="9029b-108">常數</span><span class="sxs-lookup"><span data-stu-id="9029b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9029b-109"><span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**DEXTERF \_ 周框**</span><span class="sxs-lookup"><span data-stu-id="9029b-109"><span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**DEXTERF\_BOUNDING**</span></span>
</dt> <dd>

<span data-ttu-id="9029b-110">搜尋橫跨指定時間的物件。</span><span class="sxs-lookup"><span data-stu-id="9029b-110">Search for an object that spans the specified time.</span></span>

</dd> <dt>

<span data-ttu-id="9029b-111"><span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF \_ 正好 \_ 在**</span><span class="sxs-lookup"><span data-stu-id="9029b-111"><span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF\_EXACTLY\_AT**</span></span>
</dt> <dd>

<span data-ttu-id="9029b-112">搜尋正好在指定時間開始的物件。</span><span class="sxs-lookup"><span data-stu-id="9029b-112">Search for an object that starts exactly at the specified time.</span></span>

</dd> <dt>

<span data-ttu-id="9029b-113"><span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**DEXTERF \_ 轉送**</span><span class="sxs-lookup"><span data-stu-id="9029b-113"><span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**DEXTERF\_FORWARDS**</span></span>
</dt> <dd>

<span data-ttu-id="9029b-114">搜尋在指定時間或更新版本啟動的物件。</span><span class="sxs-lookup"><span data-stu-id="9029b-114">Search for an object that starts at the specified time or later.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9029b-115">備註</span><span class="sxs-lookup"><span data-stu-id="9029b-115">Remarks</span></span>

<span data-ttu-id="9029b-116">下表摘要說明這些界限條件。</span><span class="sxs-lookup"><span data-stu-id="9029b-116">These boundary conditions are summarized in the following table.</span></span>



| <span data-ttu-id="9029b-117">列舉值</span><span class="sxs-lookup"><span data-stu-id="9029b-117">Enumeration value</span></span>    | <span data-ttu-id="9029b-118">界限條件</span><span class="sxs-lookup"><span data-stu-id="9029b-118">Boundary condition</span></span>                        |
|----------------------|-------------------------------------------|
| <span data-ttu-id="9029b-119">DEXTERF \_ 周框</span><span class="sxs-lookup"><span data-stu-id="9029b-119">DEXTERF\_BOUNDING</span></span>    | <span data-ttu-id="9029b-120">開始 <= TimeStop > 時間</span><span class="sxs-lookup"><span data-stu-id="9029b-120">Start <= TimeStop > Time</span></span><br/> |
| <span data-ttu-id="9029b-121">DEXTERF \_ 正好 \_ 在</span><span class="sxs-lookup"><span data-stu-id="9029b-121">DEXTERF\_EXACTLY\_AT</span></span> | <span data-ttu-id="9029b-122">開始 = = 時間</span><span class="sxs-lookup"><span data-stu-id="9029b-122">Start == Time</span></span>                             |
| <span data-ttu-id="9029b-123">DEXTERF \_ 轉送</span><span class="sxs-lookup"><span data-stu-id="9029b-123">DEXTERF\_FORWARDS</span></span>    | <span data-ttu-id="9029b-124">開始 >= 時間</span><span class="sxs-lookup"><span data-stu-id="9029b-124">Start >= Time</span></span>                          |



 

-   <span data-ttu-id="9029b-125">Start：抓取物件的開始時間。</span><span class="sxs-lookup"><span data-stu-id="9029b-125">Start: start time of the retrieved object.</span></span>
-   <span data-ttu-id="9029b-126">停止：抓取物件的停止時間。</span><span class="sxs-lookup"><span data-stu-id="9029b-126">Stop: stop time of the retrieved object.</span></span>
-   <span data-ttu-id="9029b-127">時間：指定的搜尋時間。</span><span class="sxs-lookup"><span data-stu-id="9029b-127">Time: specified search time.</span></span>

## <a name="requirements"></a><span data-ttu-id="9029b-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="9029b-128">Requirements</span></span>



| <span data-ttu-id="9029b-129">需求</span><span class="sxs-lookup"><span data-stu-id="9029b-129">Requirement</span></span> | <span data-ttu-id="9029b-130">值</span><span class="sxs-lookup"><span data-stu-id="9029b-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9029b-131">標頭</span><span class="sxs-lookup"><span data-stu-id="9029b-131">Header</span></span><br/> | <dl> <span data-ttu-id="9029b-132"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="9029b-132"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9029b-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9029b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9029b-134">**IAMTimelineTrack::GetSrcAtTime**</span><span class="sxs-lookup"><span data-stu-id="9029b-134">**IAMTimelineTrack::GetSrcAtTime**</span></span>](iamtimelinetrack-getsrcattime.md)
</dt> </dl>

 

 




