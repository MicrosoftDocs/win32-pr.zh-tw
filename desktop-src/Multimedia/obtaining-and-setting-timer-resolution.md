---
title: 取得和設定計時器解析度
description: 取得和設定計時器解析度
ms.assetid: 237a6770-89b9-4922-b9e9-0e0bf3e0c9b6
keywords:
- 多媒體計時器，解析度
- 計時器，解決
- 最小計時器解析度
- 最大計時器解析度
- 多媒體計時器，最大解析度
- 計時器，最大解析度
- 多媒體計時器，最低解析度
- 計時器，最低解析度
- timeGetDevCaps 函式
- timeBeginPeriod 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af5feca59e6fb4c528d6042b00eb7aa23263245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968635"
---
# <a name="obtaining-and-setting-timer-resolution"></a><span data-ttu-id="2ef56-113">取得和設定計時器解析度</span><span class="sxs-lookup"><span data-stu-id="2ef56-113">Obtaining and Setting Timer Resolution</span></span>

<span data-ttu-id="2ef56-114">下列範例會呼叫 [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) 函數，以判斷計時器服務所支援的最小和最大計時器解析度。</span><span class="sxs-lookup"><span data-stu-id="2ef56-114">The following example calls the [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) function to determine the minimum and maximum timer resolutions supported by the timer services.</span></span> <span data-ttu-id="2ef56-115">在設定任何計時器事件之前，此範例會使用 [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) 函數來建立最小計時器解析度。</span><span class="sxs-lookup"><span data-stu-id="2ef56-115">Before it sets up any timer events, the example establishes the minimum timer resolution by using the [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) function.</span></span>


```C++
#define TARGET_RESOLUTION 1         // 1-millisecond target resolution

TIMECAPS tc;
UINT     wTimerRes;

if (timeGetDevCaps(&tc, sizeof(TIMECAPS)) != TIMERR_NOERROR) 
{
    // Error; application can't continue.
}

wTimerRes = min(max(tc.wPeriodMin, TARGET_RESOLUTION), tc.wPeriodMax);
timeBeginPeriod(wTimerRes); 
```



## <a name="related-topics"></a><span data-ttu-id="2ef56-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="2ef56-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ef56-117">使用多媒體計時器</span><span class="sxs-lookup"><span data-stu-id="2ef56-117">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 




