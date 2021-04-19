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
# <a name="interrupt-time"></a>停機時間

插斷 *時間* 是系統自上次啟動以來的時間量（以 100-納秒間隔）。 當系統啟動時，停機時間計數會從零開始，而且會依時鐘滴答的長度，以每個時鐘中斷遞增。 時鐘滴答的確切長度取決於基礎硬體，而且可能會因系統而異。

與 [系統時間](system-time.md)不同的是，停機時間計數並不受使用者或 Windows 時間服務的調整，因此更適合用來測量短暫的持續時間。 需要比停機時間計數更高的精確度的應用程式應該使用 [高解析度計時器](../winmsg/about-timers.md)。 您可以使用 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) 函式來取得高解析度計時器的頻率，並使用 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 函數來取出計數器的值。

您可以使用 [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)、 [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)、 [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)和 [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) 函式來取得停機時間計數。 無偏誤停機時間表示只會計算系統處於工作狀態的時間，因此，停機時間計數不會因為系統花在睡眠或休眠的時間而「偏誤」。

**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP/2000：** 從 Windows 7 和 Windows Server 2008 R2 開始，可以使用 [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) 函數。

[**TimeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod)和 [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod)函數所設定的計時器解析度會影響 [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)和 [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)函式的解析度。 但是，不建議增加計時器解析度，因為它可以降低整體系統效能，並藉由防止處理器進入省電狀態來提高耗電量。 相反地，應用程式應該使用高解析度計時器。

> [!Note]  
> [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)、 [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)、 [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)和 [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)函式會在 ( 「已檢查」的 Windows ) 組建上產生不同的結果，因為停機時間計數和滴答計數大約是49天。 這有助於識別在系統長時間執行之前可能不會發生的 bug。 MSDN 訂閱者可透過 [Microsoft 開發人員 Network (msdn) ](https://msdn.microsoft.com/default.aspx) 網站取得已檢查的組建。

 

下列範例顯示如何藉由呼叫 [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)、 [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)、 [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)和 [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) 函式來取得停機時間計數。 當您建立呼叫這些函式的主控台應用程式時，連結至 OneCore .lib 程式庫。


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



若要取出帳戶以進行睡眠或休眠的經過時間，請使用 [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) 或 [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) 函數，或使用 [系統執行時間] 效能計數器。 您可以從登錄機碼 **HKEY \_ 效能 \_ 資料** 的效能資料中抓取此效能計數器。 傳回的值是8位元組值。 如需相關資訊，請參閱 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)
</dt> <dt>

[**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)
</dt> <dt>

[**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)
</dt> <dt>

[**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)
</dt> <dt>

[**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod)
</dt> <dt>

[**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod)
</dt> </dl>

 

 
