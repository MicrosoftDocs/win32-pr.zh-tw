---
description: PERFINFO \_ DSHOW \_ AVREND 結構包含 GUID VIDEOREND 類型之追蹤事件的資料 \_ 。VMR 會在呈現框架之前立即記錄此事件。
ms.assetid: 95deda21-0ef4-4bf0-9fa3-826a813757b9
title: 'PERFINFO_DSHOW_AVREND 結構 (Perfstruct .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AVREND
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: ee2d944d086f9c1a4ea7944f023321dfbc06d547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999687"
---
# <a name="perfinfo_dshow_avrend-structure"></a><span data-ttu-id="5530e-103">PERFINFO \_ DSHOW \_ AVREND 結構</span><span class="sxs-lookup"><span data-stu-id="5530e-103">PERFINFO\_DSHOW\_AVREND structure</span></span>

<span data-ttu-id="5530e-104">`PERFINFO_DSHOW_AVREND`結構包含 GUID VIDEOREND 類型之追蹤事件的資料 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5530e-104">The `PERFINFO_DSHOW_AVREND` structure contains data for a trace event of type GUID\_VIDEOREND.</span></span>

<span data-ttu-id="5530e-105">VMR 會在呈現框架之前立即記錄此事件。</span><span class="sxs-lookup"><span data-stu-id="5530e-105">The VMR logs this event immediately before rendering a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="5530e-106">語法</span><span class="sxs-lookup"><span data-stu-id="5530e-106">Syntax</span></span>


```C++
typedef struct PERFINFO_DSHOW_AVREND {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
} PERFINFO_DSHOW_AVREND, *PPERFINFO_DSHOW_AVREND;
```



## <a name="members"></a><span data-ttu-id="5530e-107">成員</span><span class="sxs-lookup"><span data-stu-id="5530e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5530e-108">**cycleCounter**</span><span class="sxs-lookup"><span data-stu-id="5530e-108">**cycleCounter**</span></span>
</dt> <dd>

<span data-ttu-id="5530e-109">最新的頻率週期計數 (RDTSC 指令) 。</span><span class="sxs-lookup"><span data-stu-id="5530e-109">Latest clock cycle count (RDTSC instruction).</span></span>

</dd> <dt>

<span data-ttu-id="5530e-110">**dshowClock**</span><span class="sxs-lookup"><span data-stu-id="5530e-110">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="5530e-111">[**IReferenceClock：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime)方法所傳回的目前參考時間。</span><span class="sxs-lookup"><span data-stu-id="5530e-111">Current reference time, as returned by the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method.</span></span>

</dd> <dt>

<span data-ttu-id="5530e-112">**sampleTime**</span><span class="sxs-lookup"><span data-stu-id="5530e-112">**sampleTime**</span></span>
</dt> <dd>

<span data-ttu-id="5530e-113">範例的開始時間。</span><span class="sxs-lookup"><span data-stu-id="5530e-113">Start time of the sample.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5530e-114">備註</span><span class="sxs-lookup"><span data-stu-id="5530e-114">Remarks</span></span>

<span data-ttu-id="5530e-115">若要啟用此事件，您必須在 \_ 呼叫 **EnableTrace** 時，在 *ENABLEFLAG* 參數中設定 DXMPERF VIDEOREND 旗標。</span><span class="sxs-lookup"><span data-stu-id="5530e-115">To enable this event, you must set the DXMPERF\_VIDEOREND flag in the *EnableFlag* parameter when you call **EnableTrace**.</span></span> <span data-ttu-id="5530e-116">此旗標定義于 Dxmperf 標頭檔中，並包含在 DirectShow 基類中。</span><span class="sxs-lookup"><span data-stu-id="5530e-116">This flag is defined in the header file Dxmperf.h, which is included in the DirectShow base classes.</span></span>

<span data-ttu-id="5530e-117">若要從 DirectShow 篩選記錄此事件，請使用 **PERFLOG \_ VIDEOREND** 宏（定義于 Dxmperf 中）。</span><span class="sxs-lookup"><span data-stu-id="5530e-117">To log this event from a DirectShow filter, use the **PERFLOG\_VIDEOREND** macro, which is defined in Dxmperf.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="5530e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5530e-118">Requirements</span></span>



| <span data-ttu-id="5530e-119">需求</span><span class="sxs-lookup"><span data-stu-id="5530e-119">Requirement</span></span> | <span data-ttu-id="5530e-120">值</span><span class="sxs-lookup"><span data-stu-id="5530e-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5530e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="5530e-121">Header</span></span><br/> | <dl> <span data-ttu-id="5530e-122"><dt>Perfstruct。h</dt></span><span class="sxs-lookup"><span data-stu-id="5530e-122"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5530e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5530e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5530e-124">DirectShow 結構</span><span class="sxs-lookup"><span data-stu-id="5530e-124">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="5530e-125">DirectShow 中的事件追蹤</span><span class="sxs-lookup"><span data-stu-id="5530e-125">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="5530e-126">追蹤事件 Guid</span><span class="sxs-lookup"><span data-stu-id="5530e-126">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 




