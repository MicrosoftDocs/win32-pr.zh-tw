---
title: 多媒體計時器參考
description: 多媒體計時器參考
ms.assetid: e96bc9a6-4e9d-4231-9e35-4a6ff59e6521
keywords:
- Windows 多媒體，計時器參考
- 多媒體、計時器參考
- 多媒體輸入，計時器參考
- 多媒體計時器，參考
- 計時器，參考
- 計時器參考，關於
- 計時器參考，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d926f7a76e6f16b95eaf3308db5c8da7371a11fd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933151"
---
# <a name="multimedia-timer-reference"></a><span data-ttu-id="aca05-110">多媒體計時器參考</span><span class="sxs-lookup"><span data-stu-id="aca05-110">Multimedia Timer Reference</span></span>

<span data-ttu-id="aca05-111">本節說明與多媒體計時器服務相關聯的函式和結構。</span><span class="sxs-lookup"><span data-stu-id="aca05-111">This section describes the functions and structures associated with multimedia timer services.</span></span> <span data-ttu-id="aca05-112">這些元素的分組方式如下。</span><span class="sxs-lookup"><span data-stu-id="aca05-112">These elements are grouped as follows.</span></span>

## <a name="retrieving-the-system-time"></a><span data-ttu-id="aca05-113">取出系統時間</span><span class="sxs-lookup"><span data-stu-id="aca05-113">Retrieving the System Time</span></span>

-   <span data-ttu-id="aca05-114">[**MMTIME**](/previous-versions//dd757347(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aca05-114">[**MMTIME**](/previous-versions//dd757347(v=vs.85))</span></span>
-   [<span data-ttu-id="aca05-115">**timeGetSystemTime**</span><span class="sxs-lookup"><span data-stu-id="aca05-115">**timeGetSystemTime**</span></span>](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime)
-   [<span data-ttu-id="aca05-116">**timeGetTime**</span><span class="sxs-lookup"><span data-stu-id="aca05-116">**timeGetTime**</span></span>](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime)

## <a name="retrieving-timer-information"></a><span data-ttu-id="aca05-117">正在抓取計時器資訊</span><span class="sxs-lookup"><span data-stu-id="aca05-117">Retrieving Timer Information</span></span>

-   [<span data-ttu-id="aca05-118">**TIMECAPS**</span><span class="sxs-lookup"><span data-stu-id="aca05-118">**TIMECAPS**</span></span>](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps)
-   [<span data-ttu-id="aca05-119">**timeGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="aca05-119">**timeGetDevCaps**</span></span>](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps)

## <a name="time-events"></a><span data-ttu-id="aca05-120">時間事件</span><span class="sxs-lookup"><span data-stu-id="aca05-120">Time Events</span></span>

-   <span data-ttu-id="aca05-121">[**timeKillEvent**](/previous-versions//dd757630(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aca05-121">[**timeKillEvent**](/previous-versions//dd757630(v=vs.85))</span></span>
-   <span data-ttu-id="aca05-122">[**TimeProc**](/previous-versions//dd757631(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aca05-122">[**TimeProc**](/previous-versions//dd757631(v=vs.85))</span></span>
-   <span data-ttu-id="aca05-123">[**timeSetEvent**](/previous-versions//dd757634(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aca05-123">[**timeSetEvent**](/previous-versions//dd757634(v=vs.85))</span></span>

## <a name="time-periods"></a><span data-ttu-id="aca05-124">時間週期</span><span class="sxs-lookup"><span data-stu-id="aca05-124">Time Periods</span></span>

-   [<span data-ttu-id="aca05-125">**timeBeginPeriod**</span><span class="sxs-lookup"><span data-stu-id="aca05-125">**timeBeginPeriod**</span></span>](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod)
-   [<span data-ttu-id="aca05-126">**timeEndPeriod**</span><span class="sxs-lookup"><span data-stu-id="aca05-126">**timeEndPeriod**</span></span>](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod)

## <a name="related-topics"></a><span data-ttu-id="aca05-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="aca05-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aca05-128">多媒體計時器</span><span class="sxs-lookup"><span data-stu-id="aca05-128">Multimedia Timers</span></span>](multimedia-timers.md)
</dt> </dl>

 

 