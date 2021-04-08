---
title: 計時器解析度
description: 計時器解析度
ms.assetid: 2e5e94fe-8175-417f-8c59-9d5cf052ea89
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
- timeEndPeriod 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e96f1b410f2e18203af794ea124bb6b83bccce
ms.sourcegitcommit: a0b531d335bc691100149830b256d5af7e136c24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/28/2019
ms.locfileid: "103670860"
---
# <a name="timer-resolution"></a><span data-ttu-id="250eb-114">計時器解析度</span><span class="sxs-lookup"><span data-stu-id="250eb-114">Timer Resolution</span></span>

<span data-ttu-id="250eb-115">若要判斷計時器服務所支援的最小和最大計時器解析度，請使用 [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) 函數。</span><span class="sxs-lookup"><span data-stu-id="250eb-115">To determine the minimum and maximum timer resolutions supported by the timer services, use the [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) function.</span></span> <span data-ttu-id="250eb-116">此函式會以最小和最大解析度填滿 [**TIMECAPS**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps)結構的 **wPeriodMin** 和 **wPeriodMax** 成員。</span><span class="sxs-lookup"><span data-stu-id="250eb-116">This function fills the **wPeriodMin** and **wPeriodMax** members of the [**TIMECAPS**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) structure with the minimum and maximum resolutions.</span></span> <span data-ttu-id="250eb-117">此範圍在電腦和 Windows 平臺上可能會有所不同。</span><span class="sxs-lookup"><span data-stu-id="250eb-117">This range can vary across computers and Windows platforms.</span></span>

<span data-ttu-id="250eb-118">判斷可用計時器解析度的最小和最大值之後，您必須建立應用程式所要使用的最小解析度。</span><span class="sxs-lookup"><span data-stu-id="250eb-118">After you determine the minimum and maximum available timer resolutions, you must establish the minimum resolution you want your application to use.</span></span> <span data-ttu-id="250eb-119">您可以使用 [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) 和 [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) 函數來設定和清除此解決方法。</span><span class="sxs-lookup"><span data-stu-id="250eb-119">Use the [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) functions to set and clear this resolution.</span></span> <span data-ttu-id="250eb-120">您必須使用 **timeEndPeriod** 的呼叫來比對 **timeBeginPeriod** 的每個呼叫，並在兩個呼叫中指定相同的最小解析度。</span><span class="sxs-lookup"><span data-stu-id="250eb-120">You must match each call to **timeBeginPeriod** with a call to **timeEndPeriod**, specifying the same minimum resolution in both calls.</span></span> <span data-ttu-id="250eb-121">只要每個呼叫都與 **timeEndPeriod** 的呼叫相符，應用程式就可以進行多個 **timeBeginPeriod** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="250eb-121">An application can make multiple **timeBeginPeriod** calls, as long as each call is matched with a call to **timeEndPeriod**.</span></span>

<span data-ttu-id="250eb-122">在 [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) 和 [**TimeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod)中， *uPeriod* 參數表示最小計時器解析度（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="250eb-122">In both [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod), the *uPeriod* parameter indicates the minimum timer resolution, in milliseconds.</span></span> <span data-ttu-id="250eb-123">您可以在計時器所支援的範圍內指定任何計時器解析度值。</span><span class="sxs-lookup"><span data-stu-id="250eb-123">You can specify any timer resolution value within the range supported by the timer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="250eb-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="250eb-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="250eb-125">關於多媒體計時器</span><span class="sxs-lookup"><span data-stu-id="250eb-125">About Multimedia Timers</span></span>](about-multimedia-timers.md)
</dt> </dl>

 

 




