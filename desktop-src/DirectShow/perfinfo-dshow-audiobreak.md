---
description: PERFINFO \_ DSHOW \_ AUDIOBREAK 結構包含 GUID AUDIOBREAK 類型之追蹤事件的資料 \_ 。當音訊資料流程中出現中斷時，DirectSound 轉譯器篩選器會記錄此事件。
ms.assetid: 9e7abdca-7d4c-4006-997f-9605f8d18e1d
title: 'PERFINFO_DSHOW_AUDIOBREAK 結構 (Perfstruct .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AUDIOBREAK
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 599befea67b28acbedffd5c98ebce84aadf70838
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991198"
---
# <a name="perfinfo_dshow_audiobreak-structure"></a><span data-ttu-id="77c25-103">PERFINFO \_ DSHOW \_ AUDIOBREAK 結構</span><span class="sxs-lookup"><span data-stu-id="77c25-103">PERFINFO\_DSHOW\_AUDIOBREAK structure</span></span>

<span data-ttu-id="77c25-104">`PERFINFO_DSHOW_AUDIOBREAK`結構包含 GUID AUDIOBREAK 類型之追蹤事件的資料 \_ 。</span><span class="sxs-lookup"><span data-stu-id="77c25-104">The `PERFINFO_DSHOW_AUDIOBREAK` structure contains data for a trace event of type GUID\_AUDIOBREAK.</span></span>

<span data-ttu-id="77c25-105">當音訊資料流程中出現中斷時， [DirectSound](directsound-renderer-filter.md) 轉譯器篩選器會記錄此事件。</span><span class="sxs-lookup"><span data-stu-id="77c25-105">The [DirectSound Renderer](directsound-renderer-filter.md) filter logs this event when there is a break in the audio stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="77c25-106">語法</span><span class="sxs-lookup"><span data-stu-id="77c25-106">Syntax</span></span>


```C++
typedef struct PERFINFO_DSHOW_AUDIOBREAK {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
  ULONGLONG sampleDuration;
} PERFINFO_DSHOW_AUDIOBREAK, *PPERFINFO_DSHOW_AUDIOBREAK;
```



## <a name="members"></a><span data-ttu-id="77c25-107">成員</span><span class="sxs-lookup"><span data-stu-id="77c25-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="77c25-108">**cycleCounter**</span><span class="sxs-lookup"><span data-stu-id="77c25-108">**cycleCounter**</span></span>
</dt> <dd>

<span data-ttu-id="77c25-109">最新的頻率週期計數 (RDTSC 指令) 。</span><span class="sxs-lookup"><span data-stu-id="77c25-109">Latest clock cycle count (RDTSC instruction).</span></span>

</dd> <dt>

<span data-ttu-id="77c25-110">**dshowClock**</span><span class="sxs-lookup"><span data-stu-id="77c25-110">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="77c25-111">DirectSound 緩衝區中的目前寫入位置。</span><span class="sxs-lookup"><span data-stu-id="77c25-111">Current write position in the DirectSound buffer.</span></span>

</dd> <dt>

<span data-ttu-id="77c25-112">**sampleTime**</span><span class="sxs-lookup"><span data-stu-id="77c25-112">**sampleTime**</span></span>
</dt> <dd>

<span data-ttu-id="77c25-113">DirectSound 緩衝區中的音訊中斷開頭。</span><span class="sxs-lookup"><span data-stu-id="77c25-113">Start of the audio break in the DirectSound buffer.</span></span>

</dd> <dt>

<span data-ttu-id="77c25-114">**sampleDuration**</span><span class="sxs-lookup"><span data-stu-id="77c25-114">**sampleDuration**</span></span>
</dt> <dd>

<span data-ttu-id="77c25-115">中斷的持續時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="77c25-115">Duration of the break, in milliseconds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77c25-116">備註</span><span class="sxs-lookup"><span data-stu-id="77c25-116">Remarks</span></span>

<span data-ttu-id="77c25-117">若要啟用此事件，您必須在 \_ 呼叫 **EnableTrace** 時，在 *ENABLEFLAG* 參數中設定 AUDIOBREAK 位旗標。</span><span class="sxs-lookup"><span data-stu-id="77c25-117">To enable this event, you must set the AUDIOBREAK\_BIT flag in the *EnableFlag* parameter when you call **EnableTrace**.</span></span> <span data-ttu-id="77c25-118">此旗標定義于 Dxmperf 標頭檔中，並包含在 DirectShow 基類中。</span><span class="sxs-lookup"><span data-stu-id="77c25-118">This flag is defined in the header file Dxmperf.h, which is included in the DirectShow base classes.</span></span>

<span data-ttu-id="77c25-119">若要從 DirectShow 篩選記錄此事件，請使用 **PERFLOG \_ AUDIOBREAK** 宏（定義于 Dxmperf 中）。</span><span class="sxs-lookup"><span data-stu-id="77c25-119">To log this event from a DirectShow filter, use the **PERFLOG\_AUDIOBREAK** macro, which is defined in Dxmperf.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="77c25-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="77c25-120">Requirements</span></span>



| <span data-ttu-id="77c25-121">需求</span><span class="sxs-lookup"><span data-stu-id="77c25-121">Requirement</span></span> | <span data-ttu-id="77c25-122">值</span><span class="sxs-lookup"><span data-stu-id="77c25-122">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77c25-123">標頭</span><span class="sxs-lookup"><span data-stu-id="77c25-123">Header</span></span><br/> | <dl> <span data-ttu-id="77c25-124"><dt>Perfstruct。h</dt></span><span class="sxs-lookup"><span data-stu-id="77c25-124"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77c25-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77c25-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77c25-126">DirectShow 結構</span><span class="sxs-lookup"><span data-stu-id="77c25-126">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="77c25-127">DirectShow 中的事件追蹤</span><span class="sxs-lookup"><span data-stu-id="77c25-127">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="77c25-128">追蹤事件 Guid</span><span class="sxs-lookup"><span data-stu-id="77c25-128">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 




