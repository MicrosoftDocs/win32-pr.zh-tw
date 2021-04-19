---
description: 插斷時間是系統自上次啟動以來的時間量（以 100-納秒間隔）。
ms.assetid: 56fe322e-53ea-4186-9b5e-352f69b09109
title: 停機時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6018d97ab0eecd1182c02b734357ca13fbe12632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970847"
---
# <a name="interrupt-time"></a><span data-ttu-id="2a7e0-103">停機時間</span><span class="sxs-lookup"><span data-stu-id="2a7e0-103">Interrupt Time</span></span>

<span data-ttu-id="2a7e0-104">插斷 *時間* 是系統自上次啟動以來的時間量（以 100-納秒間隔）。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-104">*Interrupt time* is the amount of time since the system was last started, in 100-nanosecond intervals.</span></span> <span data-ttu-id="2a7e0-105">當系統啟動時，停機時間計數會從零開始，而且會依時鐘滴答的長度，以每個時鐘中斷遞增。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-105">The interrupt-time count begins at zero when the system starts and is incremented at each clock interrupt by the length of a clock tick.</span></span> <span data-ttu-id="2a7e0-106">時鐘滴答的確切長度取決於基礎硬體，而且可能會因系統而異。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-106">The exact length of a clock tick depends on underlying hardware and can vary between systems.</span></span>

<span data-ttu-id="2a7e0-107">與 [系統時間](system-time.md)不同的是，停機時間計數並不受使用者或 Windows 時間服務的調整，因此更適合用來測量短暫的持續時間。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-107">Unlike [system time](system-time.md), the interrupt-time count is not subject to adjustments by users or the Windows time service, making it a better choice for measuring short durations.</span></span> <span data-ttu-id="2a7e0-108">需要比停機時間計數更高的精確度的應用程式應該使用 [高解析度計時器](../winmsg/about-timers.md)。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-108">Applications that require greater precision than the interrupt-time count should use a [high-resolution timer](../winmsg/about-timers.md).</span></span> <span data-ttu-id="2a7e0-109">您可以使用 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) 函式來取得高解析度計時器的頻率，並使用 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 函數來取出計數器的值。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-109">Use the [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) function to retrieve the frequency of the high-resolution timer and the [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) function to retrieve the counter's value.</span></span>

<span data-ttu-id="2a7e0-110">您可以使用 [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)、 [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)、 [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)和 [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) 函式來取得停機時間計數。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-110">The [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions can be used to retrieve the interrupt-time count.</span></span> <span data-ttu-id="2a7e0-111">無偏誤停機時間表示只會計算系統處於工作狀態的時間，因此，停機時間計數不會因為系統花在睡眠或休眠的時間而「偏誤」。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-111">Unbiased interrupt-time means that only time that the system is in the working state is counted—therefore, the interrupt-time count is not "biased" by time the system spends in sleep or hibernation.</span></span>

<span data-ttu-id="2a7e0-112">**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP/2000：** 從 Windows 7 和 Windows Server 2008 R2 開始，可以使用 [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) 函數。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-112">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:** The [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) function is available starting with Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="2a7e0-113">[**TimeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod)和 [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod)函數所設定的計時器解析度會影響 [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)和 [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)函式的解析度。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-113">The timer resolution set by the [**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) functions affects the resolution of the [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) and [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) functions.</span></span> <span data-ttu-id="2a7e0-114">但是，不建議增加計時器解析度，因為它可以降低整體系統效能，並藉由防止處理器進入省電狀態來提高耗電量。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-114">However, increasing the timer resolution is not recommended because it can reduce overall system performance and increase power consumption by preventing the processor from entering power-saving states.</span></span> <span data-ttu-id="2a7e0-115">相反地，應用程式應該使用高解析度計時器。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-115">Instead, applications should use a high-resolution timer.</span></span>

> [!Note]  
> <span data-ttu-id="2a7e0-116">[**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)、 [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)、 [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)和 [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)函式會在 ( 「已檢查」的 Windows ) 組建上產生不同的結果，因為停機時間計數和滴答計數大約是49天。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-116">The [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions produces different results on debug ("checked") builds of Windows, because the interrupt-time count and tick count are advanced by approximately 49 days.</span></span> <span data-ttu-id="2a7e0-117">這有助於識別在系統長時間執行之前可能不會發生的 bug。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-117">This helps to identify bugs that might not occur until the system has been running for a long time.</span></span> <span data-ttu-id="2a7e0-118">MSDN 訂閱者可透過 [Microsoft 開發人員 Network (msdn) ](https://msdn.microsoft.com/default.aspx) 網站取得已檢查的組建。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-118">The checked build is available to MSDN subscribers through the [Microsoft Developer Network (MSDN)](https://msdn.microsoft.com/default.aspx) Web site.</span></span>

 

<span data-ttu-id="2a7e0-119">下列範例顯示如何藉由呼叫 [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)、 [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)、 [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)和 [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) 函式來取得停機時間計數。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-119">The following example shows how to retrieve the interrupt-time count by calling the [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions.</span></span> <span data-ttu-id="2a7e0-120">當您建立呼叫這些函式的主控台應用程式時，連結至 OneCore .lib 程式庫。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-120">Link to the OneCore.lib library when you build a console application that calls these functions.</span></span>


```C++
#include "stdafx.h"
#include <windows.h>
#include <realtimeapiset.h>

void InterruptTimeTest()
{
    ULONGLONG InterruptTime;
    ULONGLONG PreciseInterruptTime;
    ULONGLONG UnbiasedInterruptTime;
    ULONGLONG PreciseUnbiasedInterruptTime;

        // The interrupt time that QueryInterruptTime reports is based on the 
        // latest tick of the system clock timer. The system clock timer is 
        // the hardware timer that periodically generates interrupts for the 
        // system clock. The uniform period between system clock timer 
        // interrupts is referred to as a system clock tick, and is typically 
        // in the range of 0.5 milliseconds to 15.625 milliseconds, depending 
        // on the hardware platform. The interrupt time value retrieved by 
        // QueryInterruptTime is accurate within a system clock tick.

    QueryInterruptTime(&InterruptTime);
    printf("Interrupt time: %.7f seconds\n", 
            (double)InterruptTime/(double)10000000);

        // Precise interrupt time is more precise than the interrupt time that
        // QueryInterruptTime reports because the functions that report  
        // precise interrupt time read the timer hardware directly.

    QueryInterruptTimePrecise(&PreciseInterruptTime);
    printf("Precise interrupt time: %.7f seconds\n", 
            (double)PreciseInterruptTime/(double)10000000);

        // Unbiased interrupt time means that only time that the system is in 
        // the working state is counted. Therefore, the interrupt-time count 
        // is not biased by time the system spends in sleep or hibernation.

    QueryUnbiasedInterruptTime(&UnbiasedInterruptTime);
    printf("Unbiased interrupt time: %.7f seconds\n", 
            (double)UnbiasedInterruptTime/(double)10000000);

        // QueryUnbiasedInterruptTimePrecise gets an interrupt-time count
        // that is both unbiased and precise, as defined in the comments
        // included earlier in this example.

    QueryUnbiasedInterruptTimePrecise(&PreciseUnbiasedInterruptTime);
    printf("Precise unbiased interrupt time: %.7f seconds\n", 
            (double)PreciseUnbiasedInterruptTime/(double)10000000);

}

int main(void)
{
    void InterruptTimeTime();

    InterruptTimeTest();
    return(0);
}
```



<span data-ttu-id="2a7e0-121">若要取出帳戶以進行睡眠或休眠的經過時間，請使用 [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) 或 [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) 函數，或使用 [系統執行時間] 效能計數器。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-121">To retrieve elapsed time that accounts for sleep or hibernation, use the [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) or [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) function, or use the System Up Time performance counter.</span></span> <span data-ttu-id="2a7e0-122">您可以從登錄機碼 **HKEY \_ 效能 \_ 資料** 的效能資料中抓取此效能計數器。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-122">This performance counter can be retrieved from the performance data in the registry key **HKEY\_PERFORMANCE\_DATA**.</span></span> <span data-ttu-id="2a7e0-123">傳回的值是8位元組值。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-123">The value returned is an 8-byte value.</span></span> <span data-ttu-id="2a7e0-124">如需相關資訊，請參閱 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal)。</span><span class="sxs-lookup"><span data-stu-id="2a7e0-124">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a7e0-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="2a7e0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a7e0-126">**QueryInterruptTime**</span><span class="sxs-lookup"><span data-stu-id="2a7e0-126">**QueryInterruptTime**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)
</dt> <dt>

[<span data-ttu-id="2a7e0-127">**QueryInterruptTimePrecise**</span><span class="sxs-lookup"><span data-stu-id="2a7e0-127">**QueryInterruptTimePrecise**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)
</dt> <dt>

[<span data-ttu-id="2a7e0-128">**QueryUnbiasedInterruptTime**</span><span class="sxs-lookup"><span data-stu-id="2a7e0-128">**QueryUnbiasedInterruptTime**</span></span>](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)
</dt> <dt>

[<span data-ttu-id="2a7e0-129">**QueryUnbiasedInterruptTimePrecise**</span><span class="sxs-lookup"><span data-stu-id="2a7e0-129">**QueryUnbiasedInterruptTimePrecise**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)
</dt> <dt>

[<span data-ttu-id="2a7e0-130">**timeBeginPeriod**</span><span class="sxs-lookup"><span data-stu-id="2a7e0-130">**timeBeginPeriod**</span></span>](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod)
</dt> <dt>

[<span data-ttu-id="2a7e0-131">**timeEndPeriod**</span><span class="sxs-lookup"><span data-stu-id="2a7e0-131">**timeEndPeriod**</span></span>](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod)
</dt> </dl>

 

 
