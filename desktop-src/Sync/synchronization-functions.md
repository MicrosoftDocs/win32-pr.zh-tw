---
description: 同步處理會使用下列函數。
ms.assetid: 9b6359c2-0113-49b6-83d0-316ad95aba1b
title: 同步處理函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f259b71e7bf76dc7f23d092f827d16af908c74a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849438"
---
# <a name="synchronization-functions"></a>同步處理函式

同步處理會使用下列函數。

-   [非同步函式](#asynchronous-functions)
-   [Condition 變數和 SRW lock 函數](#condition-variable-and-srw-lock-functions)
-   [重要區段函數](#critical-section-functions)
-   [事件函數](#event-functions)
-   [單次初始化函數](#one-time-initialization-functions)
-   [連鎖函數](#interlocked-functions)
-   [Mutex 函數](#mutex-functions)
-   [私用命名空間函數](#private-namespace-functions)
-   [信號函數](#semaphore-functions)
-   [單一連結清單函數](#singly-linked-list-functions)
-   [同步處理屏障函數](#synchronization-barrier-functions)
-   [計時器佇列計時器函式](#timer-queue-timer-functions)
-   [Wait 函式](#wait-functions)
-   [可等候-計時器函數](#waitable-timer-functions)

## <a name="asynchronous-functions"></a>非同步函式



| 非同步函式                                  | Description                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**APCProc**](/windows/win32/api/winnt/nc-winnt-papcfunc)                             | 搭配 [**QueueUserAPC**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queueuserapc) 函式使用的應用程式定義回呼函數。 |
| [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult)     | 抓取重迭運算的結果。                                                     |
| [**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex) | 在指定的逾時間隔內，抓取重迭運算的結果。                 |
| [**QueueUserAPC**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queueuserapc)                   | 將 (APC) 物件的使用者模式非同步程序呼叫新增至指定執行緒的 APC 佇列。   |



 

## <a name="condition-variable-and-srw-lock-functions"></a>Condition 變數和 SRW lock 函數



| Condition 變數和 SRW lock 函數                           | Description                                                                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive)         | 取得超薄的讀取器/寫入器 (在獨佔模式中 SRW) 鎖定。                                                                                       |
| [**AcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockshared)               | 取得輕巧的讀取器/寫入器 (在共用模式中 SRW) 鎖定。                                                                                          |
| [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | 初始化條件變數。                                                                                                                 |
| [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock)                     | 初始化超薄讀取器/寫入器 (SRW) 鎖定。                                                                                                       |
| [**ReleaseSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockexclusive)         | 釋出以獨佔模式取得的 (SRW) 鎖定，以釋放輕巧的讀取器/寫入器。                                                                     |
| [**ReleaseSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockshared)               | 釋放在共用模式中取得 (SRW) 鎖定的輕巧讀取器/寫入器。                                                                        |
| [**SleepConditionVariableCS**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | 在指定的條件變數上進入睡眠狀態，並以不可部分完成的作業形式釋放指定的重要區段。                                    |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | 在指定的條件變數上進入睡眠狀態，並以不可部分完成的作業形式釋放指定的鎖定。                                                |
| [**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)   | 嘗試取得超薄的讀取器/寫入器 (在獨佔模式中 SRW) 鎖定。 如果呼叫成功，呼叫的執行緒就會取得鎖定的擁有權。 |
| [**TryAcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)         | 嘗試取得輕巧的讀取器/寫入器 (在共用模式中 SRW) 鎖定。 如果呼叫成功，呼叫的執行緒就會取得鎖定的擁有權。    |
| [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | 喚醒所有等候指定條件變數的執行緒。                                                                                     |
| [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | 喚醒等候指定條件變數的單一執行緒。                                                                                 |



 

## <a name="critical-section-functions"></a>重要區段函數



| Critical 區段函數                                                              | Description                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**DeleteCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-deletecriticalsection)                                 | 釋放由無人擁有的重要區段物件所使用的所有資源。                      |
| [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection)                                   | 等候指定之重要區段物件的擁有權。                           |
| [**InitializeCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsection)                         | 初始化重要區段物件。                                                  |
| [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) | 初始化重要區段物件，並設定重要區段的微調計數。 |
| [**InitializeCriticalSectionEx**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionex)                     | 使用微調計數和選擇性旗標，初始化重要區段物件。             |
| [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection)                                   | 釋放指定之重要區段物件的擁有權。                            |
| [**SetCriticalSectionSpinCount**](/windows/win32/api/synchapi/nf-synchapi-setcriticalsectionspincount)                     | 設定指定之重要區段的微調計數。                                 |
| [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection)                             | 嘗試進入重要區段而不封鎖。                                  |



 

## <a name="event-functions"></a>事件函數



| Event 函數                         | Description                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)     | 建立或開啟已命名或未命名的事件物件。                                                                                                            |
| [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa) | 建立或開啟已命名或未命名的事件物件，並將控制碼傳回物件。                                                                         |
| [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa)         | 開啟現有的已命名事件物件。                                                                                                                        |
| [**PulseEvent**](/windows/desktop/api/WinBase/nf-winbase-pulseevent)       | 將指定的事件物件設定為已發出信號的狀態，然後在釋放適當的等候執行緒數目之後，將它重設為未收到信號狀態。 |
| [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent)       | 將指定的事件物件設定為未收到信號狀態。                                                                                                    |
| [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent)           | 將指定的事件物件設定為已發出信號的狀態。                                                                                                       |



 

## <a name="one-time-initialization-functions"></a>單次初始化函數



| 單次初始化函數                           | Description                                                                                                                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) | 開始一次初始化。                                                                                                                                                                             |
| [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete)               | 完成一次初始化。                                                                                                                                                                          |
| [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce)         | 成功執行指定的函式一次。 當目前的執行緒正在執行這個函式時，沒有其他指定相同一次性初始化結構的執行緒可以執行此函數。 |
| [**InitOnceInitialize**](/windows/win32/api/synchapi/nf-synchapi-initonceinitialize)           | 初始化一次性初始化結構。                                                                                                                                                            |



 

## <a name="interlocked-functions"></a>連鎖函數



| 連鎖函數                                                                         | Description                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InterlockedAdd**](/windows/desktop/api/Winnt/nf-winnt-interlockedadd)                                                     | 在指定的 **LONG** 值上執行不可部分完成的加法運算。                                                                                                                                                                                                                   |
| [**InterlockedAddAcquire**](/windows/win32/api/winnt/nf-winnt-_inlineinterlockedadd)                                       | 在指定的 **LONG** 值上執行不可部分完成的加法運算。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                |
| [**InterlockedAddRelease**](/previous-versions/windows/desktop/legacy/ms683513(v=vs.85))                                       | 在指定的 **LONG** 值上執行不可部分完成的加法運算。 作業會使用發行記憶體順序的語法來執行。                                                                                                                                                |
| [**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))                                       | 在指定的 **LONG** 值上執行不可部分完成的加法運算。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                          |
| [**InterlockedAdd64**](/windows/win32/api/winnt/nf-winnt-_inlineinterlockedadd64)                                                 | 在指定的 **LONGLONG** 值上執行不可部分完成的加法運算。                                                                                                                                                                                                               |
| [**InterlockedAddAcquire64**](/previous-versions/windows/desktop/legacy/ms683510(v=vs.85))                                   | 在指定的 **LONGLONG** 值上執行不可部分完成的加法運算。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                            |
| [**InterlockedAddRelease64**](/previous-versions/windows/desktop/legacy/ms683514(v=vs.85))                                   | 在指定的 **LONGLONG** 值上執行不可部分完成的加法運算。 作業會使用發行記憶體順序的語法來執行。                                                                                                                                            |
| [**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))                                   | 在指定的 **LONGLONG** 值上執行不可部分完成的加法運算。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                      |
| [**InterlockedAnd**](/windows/desktop/api/WinBase/nf-winbase-interlockedand)                                                     | 在指定的 **LONG** 值上執行不可部分完成的運算。                                                                                                                                                                                                                        |
| [**InterlockedAndAcquire**](/previous-versions/windows/desktop/legacy/ms683539(v=vs.85))                                       | 在指定的 **LONG** 值上執行不可部分完成的運算。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                     |
| [**InterlockedAndRelease**](/previous-versions/windows/desktop/legacy/ms683543(v=vs.85))                                       | 在指定的 **LONG** 值上執行不可部分完成的運算。 作業會使用發行記憶體順序的語法來執行。                                                                                                                                                     |
| [**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))                                       | 在指定的 **LONG** 值上執行不可部分完成的運算。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                               |
| [**InterlockedAnd8**](/windows/win32/api/winnt/nf-winnt-interlockedand8)                                                   | 在指定的 **char** 值上執行不可部分完成的運算。                                                                                                                                                                                                                        |
| [**InterlockedAnd8Acquire**](/previous-versions/windows/desktop/legacy/ms683535(v=vs.85))                                     | 在指定的 **char** 值上執行不可部分完成的運算。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                     |
| [**InterlockedAnd8Release**](/previous-versions/windows/desktop/legacy/ms683537(v=vs.85))                                     | 在指定的 **char** 值上執行不可部分完成的運算。 作業會使用發行記憶體順序的語法來執行。                                                                                                                                                     |
| [**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))                                     | 在指定的 **char** 值上執行不可部分完成的運算。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                               |
| [**InterlockedAnd16**](/windows/win32/api/winnt/nf-winnt-interlockedand16)                                                 | 對指定的 **短** 值執行不可部分完成的運算。                                                                                                                                                                                                                       |
| [**InterlockedAnd16Acquire**](/previous-versions/windows/desktop/legacy/ms683521(v=vs.85))                                   | 對指定的 **短** 值執行不可部分完成的運算。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                    |
| [**InterlockedAnd16Release**](/previous-versions/windows/desktop/legacy/ms683525(v=vs.85))                                   | 對指定的 **短** 值執行不可部分完成的運算。 作業會使用發行記憶體順序的語法來執行。                                                                                                                                                    |
| [**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))                                   | 對指定的 **短** 值執行不可部分完成的運算。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                              |
| [**InterlockedAnd64**](/windows/win32/api/winnt/nf-winnt-interlockedand64)                                                 | 在指定的 **LONGLONG** 值上執行不可部分完成的運算。                                                                                                                                                                                                                    |
| [**InterlockedAnd64Acquire**](/previous-versions/windows/desktop/legacy/ms683529(v=vs.85))                                   | 在指定的 **LONGLONG** 值上執行不可部分完成的運算。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                 |
| [**InterlockedAnd64Release**](/previous-versions/windows/desktop/legacy/ms683530(v=vs.85))                                   | 在指定的 **LONGLONG** 值上執行不可部分完成的運算。 作業會使用發行記憶體順序的語法來執行。                                                                                                                                                 |
| [**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))                                   | 在指定的 **LONGLONG** 值上執行不可部分完成的運算。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                           |
| [**InterlockedBitTestAndComplement**](/previous-versions/windows/desktop/legacy/hh802759(v=vs.85))                   | 測試指定之 **LONG** 值的指定位，並加以補充。                                                                                                                                                                                                               |
| [**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))               | 測試指定之 **LONG64** 值的指定位，並加以補充。 作業是不可部分完成的                                                                                                                                                                                     |
| [**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))               | 測試指定之 **LONG** 值的指定位並將它設定為0。 作業是不可部分完成的，而且會使用取得記憶體順序語義來執行                                                                                                                             |
| [**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))               | 測試指定之 **LONG** 值的指定位並將它設定為0。 作業是不可部分完成的，而且會使用記憶體釋放語義來執行                                                                                                                                     |
| [**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))                   | 測試指定之 **LONG** 值的指定位並將它設定為1。 作業是不可部分完成的，而且會使用取得記憶體順序語義來執行                                                                                                                             |
| [**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))                   | 測試指定之 **LONG** 值的指定位並將它設定為1。 作業是不可部分完成的，而且會使用發行記憶體順序語義來執行                                                                                                                             |
| [**InterlockedBitTestAndReset**](/windows/win32/api/winnt/nf-winnt-_interlockedbittestandreset)                             | 測試指定之 **LONG** 值的指定位並將它設定為0。                                                                                                                                                                                                                 |
| [**InterlockedBitTestAndReset64**](/windows/win32/api/winnt/nf-winnt-_interlockedbittestandreset64)                         | 測試指定之 **LONG64** 值的指定位並將它設定為0。                                                                                                                                                                                                               |
| [**InterlockedBitTestAndSet**](/windows/win32/api/winnt/nf-winnt-_interlockedbittestandset)                                 | 測試指定之 **LONG** 值的指定位並將它設定為1。                                                                                                                                                                                                                 |
| [**InterlockedBitTestAndSet64**](/windows/win32/api/winnt/nf-winnt-_interlockedbittestandset)                               | 測試指定之 **LONG64** 值的指定位並將它設定為1。                                                                                                                                                                                                               |
| [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85))                   | 在指定的值上執行不可部分完成的比較與交換作業。 函數會根據比較結果，比較指定的64位值與指定的128位值交換。                                                                       |
| [**InterlockedCompare64ExchangeAcquire128**](/previous-versions/windows/desktop/legacy/ms683557(v=vs.85))     | 在指定的值上執行不可部分完成的比較與交換作業。 函數會根據比較結果，比較指定的64位值與指定的128位值交換。 執行作業時，會使用取得記憶體順序的語法。    |
| [**InterlockedCompare64ExchangeRelease128**](/previous-versions/windows/desktop/legacy/ms683558(v=vs.85))     | 在指定的值上執行不可部分完成的比較與交換作業。 函數會根據比較結果，比較指定的64位值與指定的128位值交換。 作業會使用發行記憶體順序的語法來執行。    |
| [**InterlockedCompareExchange**](/windows/desktop/api/WinBase/nf-winbase-interlockedcompareexchange)                             | 在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的32位值，並根據比較結果與另一個32位值交換。                                                                              |
| [**InterlockedCompareExchangeAcquire**](/previous-versions/windows/desktop/legacy/ms683564(v=vs.85))               | 在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的32位值，並根據比較結果與另一個32位值交換。 執行作業時，會使用取得記憶體順序的語法。           |
| [**InterlockedCompareExchangeRelease**](/previous-versions/windows/desktop/legacy/ms683574(v=vs.85))               | 在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的32位值，並根據比較結果與另一個32位值交換。 交換會以發行記憶體順序的語法來執行。            |
| [**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))               | 在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的32位值，並根據比較結果與另一個32位值交換。 作業會以程式方式執行，但不會使用記憶體阻礙     |
| [**InterlockedCompareExchange64**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange64)                         | 在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的64位值，並根據比較結果與另一個64位值交換。                                                                              |
| [**InterlockedCompareExchangeAcquire64**](/previous-versions/windows/desktop/legacy/ms683566(v=vs.85))           | 在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的64位值，並根據比較結果與另一個64位值交換。 交換會以取得記憶體順序的語法來執行。            |
| [**InterlockedCompareExchangeRelease64**](/previous-versions/windows/desktop/legacy/ms683576(v=vs.85))           | 在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的64位值，並根據比較結果與另一個64位值交換。 交換會以發行記憶體順序的語法來執行。            |
| [**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))           | 在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的64位值，並根據比較結果與另一個64位值交換。 作業會以程式方式執行，但不會使用記憶體阻礙     |
| [**InterlockedCompareExchange16**](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange16)                         | 在指定的值上執行不可部分完成的比較與交換作業。 此函式會比較兩個指定的16位值，並根據比較結果，與另一個16位值交換。                                                                               |
| [**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))           | 在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的16位值，並根據比較結果與另一個16位值交換。 使用取得記憶體順序語義來執行作業            |
| [**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))           | 在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的16位值，並根據比較結果與另一個16位值交換。 使用發行記憶體順序語義來執行交換             |
| [**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))           | 在指定的值上執行不可部分完成的比較與交換作業。 函數會比較兩個指定的16位值，並根據比較結果與另一個16位值交換。 作業會以程式方式執行，但不會使用記憶體阻礙     |
| [**InterlockedCompareExchange128**](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange128)                       | 在指定的值上執行不可部分完成的比較與交換作業。 此函式會比較兩個指定的128位值，並根據比較結果與另一個128位值交換。                                                                             |
| [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer)               | 在指定的指標值上執行不可部分完成的比較與交換作業。 此函式會比較兩個指定的指標值，並根據比較結果與另一個指標值交換。                                                                    |
| [**InterlockedCompareExchangePointerAcquire**](/previous-versions/windows/desktop/legacy/ms683570(v=vs.85)) | 在指定的指標值上執行不可部分完成的比較與交換作業。 此函式會比較兩個指定的指標值，並根據比較結果與另一個指標值交換。 執行作業時，會使用取得記憶體順序的語法。 |
| [**InterlockedCompareExchangePointerRelease**](/previous-versions/windows/desktop/legacy/ms683571(v=vs.85)) | 在指定的指標值上執行不可部分完成的比較與交換作業。 此函式會比較兩個指定的指標值，並根據比較結果與另一個指標值交換。 作業會使用發行記憶體順序的語法來執行。 |
| [**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85)) | 在指定的值上執行不可部分完成的比較與交換作業。 此函式會比較兩個指定的指標值，並根據比較結果與另一個指標值交換。 作業會以程式方式執行，但不會使用記憶體阻礙   |
| [**InterlockedDecrement**](/windows/desktop/api/WinBase/nf-winbase-interlockeddecrement)                                         | 遞減 (會以一) 指定的32位變數值做為不可部分完成的作業來減少。                                                                                                                                                                                          |
| [**InterlockedDecrementAcquire**](/previous-versions/windows/desktop/legacy/ms683583(v=vs.85))                           | 遞減 (會以一) 指定的32位變數值做為不可部分完成的作業來減少。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                       |
| [**InterlockedDecrementRelease**](/previous-versions/windows/desktop/legacy/ms683586(v=vs.85))                           | 遞減 (會以一) 指定的32位變數值做為不可部分完成的作業來減少。 作業會使用發行記憶體順序的語法來執行。                                                                                                                       |
| [**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))                           | 遞減 (會以一) 指定的32位變數值做為不可部分完成的作業來減少。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                 |
| [**InterlockedDecrement16**](/windows/desktop/api/Winnt/nf-winnt-interlockeddecrement16)                                     | 遞減 (減少一) 指定的16位變數值為不可部分完成的作業                                                                                                                                                                                           |
| [**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))                       | 遞減 (會將指定的16位變數值減少一) 為不可部分完成的作業。 使用取得記憶體順序語義來執行作業                                                                                                                        |
| [**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))                       | 遞減 (會將指定的16位變數值減少一) 為不可部分完成的作業。 使用發行記憶體順序語義來執行作業                                                                                                                        |
| [**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))                       | 遞減 (會將指定的16位變數值減少一) 為不可部分完成的作業。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                 |
| [**InterlockedDecrement64**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement64)                                     | 遞減 (會以一) 指定的64位變數值做為不可部分完成的作業來減少。                                                                                                                                                                                          |
| [**InterlockedDecrementAcquire64**](/previous-versions/windows/desktop/legacy/ms683585(v=vs.85))                       | 遞減 (會以一) 指定的64位變數值做為不可部分完成的作業來減少。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                       |
| [**InterlockedDecrementRelease64**](/previous-versions/windows/desktop/legacy/ms683588(v=vs.85))                       | 遞減 (會以一) 指定的64位變數值做為不可部分完成的作業來減少。 作業會使用發行記憶體順序的語法來執行。                                                                                                                       |
| [**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))                       | 遞減 (會以一) 指定的64位變數值做為不可部分完成的作業來減少。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                 |
| [**InterlockedExchange**](/windows/desktop/api/WinBase/nf-winbase-interlockedexchange)                                           | 將32位變數設定為指定的值，作為不可部分完成的作業。                                                                                                                                                                                                                     |
| [**InterlockedExchangeAcquire**](/previous-versions/windows/desktop/legacy/ms683594(v=vs.85))                             | 將32位變數設定為指定的值，作為不可部分完成的作業。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                  |
| [**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))                             | 將64位變數設定為指定的值，作為不可部分完成的作業。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                            |
| [**InterlockedExchange8**](/windows/desktop/api/Winnt/nf-winnt-interlockedexchange8)                                         | 將8位變數設定為指定的值，作為不可部分完成的作業                                                                                                                                                                                                                      |
| [**InterlockedExchange16**](/windows/desktop/api/Winnt/nf-winnt-interlockedexchange16)                                       | 將16位變數設定為指定的值，作為不可部分完成的作業。                                                                                                                                                                                                                     |
| [**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))                         | 將16位變數設定為指定的值，作為不可部分完成的作業。 作業是使用取得記憶體順序語義來執行                                                                                                                                                  |
| [**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))                         | 將16位變數設定為指定的值，作為不可部分完成的作業。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                            |
| [**InterlockedExchange64**](/windows/win32/api/winnt/nf-winnt-interlockedexchange64)                                       | 將64位變數設定為指定的值，作為不可部分完成的作業。                                                                                                                                                                                                                     |
| [**InterlockedExchangeAcquire64**](/previous-versions/windows/desktop/legacy/ms683596(v=vs.85))                         | 將32位變數設定為指定的值，作為不可部分完成的作業。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                  |
| [**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))                         | 將64位變數設定為指定的值，作為不可部分完成的作業。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                            |
| [**InterlockedExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedexchangepointer)                             | 以不可部分完成的方式交換一對指標值。                                                                                                                                                                                                                                            |
| [**InterlockedExchangePointerAcquire**](/previous-versions/windows/desktop/legacy/ms683611(v=vs.85))               | 以不可部分完成的方式交換一對指標值。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                                         |
| [**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))               | 以不可部分完成的方式交換一對位址。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                                                        |
| [**InterlockedExchangeSubtract**](/windows/desktop/api/WinBase/nf-winbase-interlockedexchangesubtract)                           | 執行兩個值的不可部分完成減法運算。                                                                                                                                                                                                                                             |
| [**InterlockedExchangeAdd**](/windows/desktop/api/WinBase/nf-winbase-interlockedexchangeadd)                                     | 執行 2 32 位值的不可部分完成加法。                                                                                                                                                                                                                                         |
| [**InterlockedExchangeAddAcquire**](/previous-versions/windows/desktop/legacy/ms683601(v=vs.85))                       | 執行 2 32 位值的不可部分完成加法。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                                      |
| [**InterlockedExchangeAddRelease**](/previous-versions/windows/desktop/legacy/ms683605(v=vs.85))                       | 執行 2 32 位值的不可部分完成加法。 作業會使用發行記憶體順序的語法來執行。                                                                                                                                                                      |
| [**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))                       | 執行 2 32 位值的不可部分完成加法。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                                                |
| [**InterlockedExchangeAdd64**](/windows/win32/api/winnt/nf-winnt-interlockedexchangeadd64)                                 | 執行 2 64 位值的不可部分完成加法。                                                                                                                                                                                                                                         |
| [**InterlockedExchangeAddAcquire64**](/previous-versions/windows/desktop/legacy/ms683604(v=vs.85))                   | 執行 2 64 位值的不可部分完成加法。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                                      |
| [**InterlockedExchangeAddRelease64**](/previous-versions/windows/desktop/legacy/ms683607(v=vs.85))                   | 執行 2 64 位值的不可部分完成加法。 作業會使用發行記憶體順序的語法來執行。                                                                                                                                                                      |
| [**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))                   | 執行 2 64 位值的不可部分完成加法。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                                                |
| [**InterlockedIncrement**](/windows/desktop/api/WinBase/nf-winbase-interlockedincrement)                                         | 遞增 (會以一) 指定的32位變數值為不可部分完成的作業增加。                                                                                                                                                                                          |
| [**InterlockedIncrementAcquire**](/previous-versions/windows/desktop/legacy/ms683618(v=vs.85))                           | 遞增 (會以一) 指定的32位變數值為不可部分完成的作業增加。 作業是使用取得記憶體順序語義來執行。                                                                                                                      |
| [**InterlockedIncrementRelease**](/previous-versions/windows/desktop/legacy/ms683622(v=vs.85))                           | 遞增 (會以一) 指定的32位變數值為不可部分完成的作業增加。 作業是使用發行記憶體順序的語法來執行。                                                                                                                      |
| [**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))                           | 遞增 (會以一) 指定的32位變數值為不可部分完成的作業增加。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                 |
| [**InterlockedIncrement16**](/windows/desktop/api/Winnt/nf-winnt-interlockedincrement16)                                     | 遞增 (增加一) 指定的16位變數值為不可部分完成的作業                                                                                                                                                                                           |
| [**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))                       | 遞增 (增加一個) 指定的16位變數值為不可部分完成的作業。 作業是使用取得記憶體順序語義來執行                                                                                                                       |
| [**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))                       | 遞增 (增加一個) 指定的16位變數值為不可部分完成的作業。 作業是使用發行記憶體順序語義來執行                                                                                                                       |
| [**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))                       | 遞增 (增加一個) 指定的16位變數值為不可部分完成的作業。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                 |
| [**InterlockedIncrement64**](/windows/win32/api/winnt/nf-winnt-interlockedincrement64)                                     | 遞增 (會以一) 指定的64位變數值為不可部分完成的作業增加。                                                                                                                                                                                          |
| [**InterlockedIncrementAcquire64**](/previous-versions/windows/desktop/legacy/ms683620(v=vs.85))                       | 遞增 (會以一) 指定的64位變數值為不可部分完成的作業增加。 作業是使用取得記憶體順序語義來執行。                                                                                                                      |
| [**InterlockedIncrementRelease64**](/previous-versions/windows/desktop/legacy/ms683624(v=vs.85))                       | 遞增 (會以一) 指定的64位變數值為不可部分完成的作業增加。 作業是使用發行記憶體順序的語法來執行。                                                                                                                      |
| [**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))                       | 遞增 (會以一) 指定的64位變數值為不可部分完成的作業增加。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                 |
| [**InterlockedOr**](/windows/desktop/api/WinBase/nf-winbase-interlockedor)                                                       | 在指定的 **LONG** 值上執行不可部分完成的或運算。                                                                                                                                                                                                                         |
| [**InterlockedOrAcquire**](/previous-versions/windows/desktop/legacy/ms683643(v=vs.85))                                         | 在指定的 **LONG** 值上執行不可部分完成的或運算。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                      |
| [**InterlockedOrRelease**](/previous-versions/windows/desktop/legacy/ms683646(v=vs.85))                                         | 在指定的 **LONG** 值上執行不可部分完成的或運算。 作業會使用發行記憶體順序的語法來執行。                                                                                                                                                      |
| [**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))                                         | 在指定的 **LONG** 值上執行不可部分完成的或運算。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                                |
| [**InterlockedOr8**](/windows/win32/api/winnt/nf-winnt-interlockedor8)                                                     | 在指定的 **char** 值上執行不可部分完成的或運算。                                                                                                                                                                                                                         |
| [**InterlockedOr8Acquire**](/previous-versions/windows/desktop/legacy/ms683639(v=vs.85))                                       | 在指定的 **char** 值上執行不可部分完成的或運算。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                      |
| [**InterlockedOr8Release**](/previous-versions/windows/desktop/legacy/ms683640(v=vs.85))                                       | 在指定的 **char** 值上執行不可部分完成的或運算。 作業會使用發行記憶體順序的語法來執行。                                                                                                                                                      |
| [**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))                                       | 在指定的 **char** 值上執行不可部分完成的或運算。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                                |
| [**InterlockedOr16**](/windows/win32/api/winnt/nf-winnt-interlockedor16)                                                   | 對指定的 **短** 值執行不可部分完成的或運算。                                                                                                                                                                                                                        |
| [**InterlockedOr16Acquire**](/previous-versions/windows/desktop/legacy/ms683629(v=vs.85))                                     | 對指定的 **短** 值執行不可部分完成的或運算。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                     |
| [**InterlockedOr16Release**](/previous-versions/windows/desktop/legacy/ms683631(v=vs.85))                                     | 對指定的 **短** 值執行不可部分完成的或運算。 作業會使用發行記憶體順序的語法來執行。                                                                                                                                                     |
| [**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))                                     | 對指定的 **短** 值執行不可部分完成的或運算。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                               |
| [**InterlockedOr64**](/windows/win32/api/winnt/nf-winnt-interlockedor64)                                                   | 在指定的 **LONGLONG** 值上執行不可部分完成的或運算。                                                                                                                                                                                                                     |
| [**InterlockedOr64Acquire**](/previous-versions/windows/desktop/legacy/ms683634(v=vs.85))                                     | 在指定的 **LONGLONG** 值上執行不可部分完成的或運算。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                  |
| [**InterlockedOr64Release**](/previous-versions/windows/desktop/legacy/ms683636(v=vs.85))                                     | 在指定的 **LONGLONG** 值上執行不可部分完成的或運算。 作業會使用發行記憶體順序的語法來執行。                                                                                                                                                  |
| [**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))                                     | 在指定的 **LONGLONG** 值上執行不可部分完成的或運算。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                            |
| [**InterlockedXor**](/windows/desktop/api/WinBase/nf-winbase-interlockedxor)                                                     | 在指定的 **LONG** 值上執行不可部分完成 XOR 運算。                                                                                                                                                                                                                        |
| [**InterlockedXorAcquire**](/previous-versions/windows/desktop/legacy/ms684117(v=vs.85))                                       | 在指定的 **LONG** 值上執行不可部分完成 XOR 運算。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                     |
| [**InterlockedXorRelease**](/previous-versions/windows/desktop/legacy/ms684118(v=vs.85))                                       | 在指定的 **LONG** 值上執行不可部分完成 XOR 運算。 作業會使用發行記憶體順序的語法來執行。                                                                                                                                                     |
| [**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))                                       | 在指定的 **LONG** 值上執行不可部分完成 XOR 運算。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                               |
| [**InterlockedXor8**](/windows/win32/api/winnt/nf-winnt-interlockedxor8)                                                   | 在指定的 **char** 值上執行不可部分完成 XOR 運算。                                                                                                                                                                                                                        |
| [**InterlockedXor8Acquire**](/previous-versions/windows/desktop/legacy/ms684112(v=vs.85))                                     | 在指定的 **char** 值上執行不可部分完成 XOR 運算。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                     |
| [**InterlockedXor8Release**](/previous-versions/windows/desktop/legacy/ms684113(v=vs.85))                                     | 在指定的 **char** 值上執行不可部分完成 XOR 運算。 作業會使用發行記憶體順序的語法來執行。                                                                                                                                                     |
| [**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))                                     | 在指定的 **char** 值上執行不可部分完成 XOR 運算。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                               |
| [**InterlockedXor16**](/windows/win32/api/winnt/nf-winnt-interlockedxor16)                                                 | 在指定的 **短** 值上執行不可部分完成的 XOR 運算。                                                                                                                                                                                                                       |
| [**InterlockedXor16Acquire**](/previous-versions/windows/desktop/legacy/ms684026(v=vs.85))                                   | 在指定的 **短** 值上執行不可部分完成的 XOR 運算。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                    |
| [**InterlockedXor16Release**](/previous-versions/windows/desktop/legacy/ms684033(v=vs.85))                                   | 在指定的 **短** 值上執行不可部分完成的 XOR 運算。 作業會使用發行記憶體順序的語法來執行。                                                                                                                                                    |
| [**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))                                   | 在指定的 **短** 值上執行不可部分完成的 XOR 運算。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                              |
| [**InterlockedXor64**](/windows/win32/api/winnt/nf-winnt-interlockedxor64)                                                 | 在指定的 **LONGLONG** 值上執行不可部分完成的 XOR 運算。                                                                                                                                                                                                                    |
| [**InterlockedXor64Acquire**](/previous-versions/windows/desktop/legacy/ms684107(v=vs.85))                                   | 在指定的 **LONGLONG** 值上執行不可部分完成的 XOR 運算。 執行作業時，會使用取得記憶體順序的語法。                                                                                                                                                 |
| [**InterlockedXor64Release**](/previous-versions/windows/desktop/legacy/ms684108(v=vs.85))                                   | 在指定的 **LONGLONG** 值上執行不可部分完成的 XOR 運算。 作業會使用發行記憶體順序的語法來執行。                                                                                                                                                 |
| [**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))                                   | 在指定的 **LONGLONG** 值上執行不可部分完成的 XOR 運算。 作業會以程式方式執行，但不會使用記憶體阻礙                                                                                                                                           |



 

## <a name="mutex-functions"></a>Mutex 函數



| Mutex 函數                         | Description                                                                          |
|----------------------------------------|--------------------------------------------------------------------------------------|
| [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa)     | 建立或開啟已命名或未命名的 mutex 物件。                                    |
| [**CreateMutexEx**](/windows/win32/api/synchapi/nf-synchapi-createmutexexa) | 建立或開啟已命名或未命名的 mutex 物件，並將控制碼傳回物件。 |
| [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw)         | 開啟現有的已命名 mutex 物件。                                                |
| [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex)   | 釋放指定之 mutex 物件的擁有權。                                    |



 

## <a name="private-namespace-functions"></a>私用命名空間函數



| 私用命名空間函數                                                             | Description                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**AddSIDToBoundaryDescriptor**](/windows/win32/api/namespaceapi/nf-namespaceapi-addsidtoboundarydescriptor)                       | 將新的安全識別碼 (SID) 新增至指定的界限描述項。          |
| [**AddIntegrityLabelToBoundaryDescriptor**](/windows/desktop/api/WinBase/nf-winbase-addintegritylabeltoboundarydescriptor) | 將新的必要安全識別碼 (SID) 新增至指定的界限描述項。 |
| [**ClosePrivateNamespace**](/windows/win32/api/namespaceapi/nf-namespaceapi-closeprivatenamespace)                                 | 關閉開啟的命名空間控制碼。                                                    |
| [**CreateBoundaryDescriptor**](/windows/desktop/api/WinBase/nf-winbase-createboundarydescriptora)                           | 建立界限描述項。                                                      |
| [**CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea)                               | 建立私用命名空間。                                                        |
| [**DeleteBoundaryDescriptor**](/windows/win32/api/namespaceapi/nf-namespaceapi-deleteboundarydescriptor)                           | 刪除指定的界限描述項。                                          |
| [**OpenPrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea)                                   | 開啟私人命名空間。                                                          |



 

## <a name="semaphore-functions"></a>信號函數



| 信號函數                             | Description                                                                              |
|------------------------------------------------|------------------------------------------------------------------------------------------|
| [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)     | 建立或開啟已命名或未命名的信號物件。                                    |
| [**CreateSemaphoreEx**](/windows/desktop/api/WinBase/nf-winbase-createsemaphoreexa) | 建立或開啟已命名或未命名的信號物件，並將控制碼傳回物件。 |
| [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)         | 開啟現有的已命名信號物件。                                                |
| [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore)   | 以指定的數量增加指定之信號物件的計數。             |



 

## <a name="singly-linked-list-functions"></a>單一連結清單函數



| 單一連結清單函數                                          | Description                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InitializeSListHead**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead)                   | 初始化單一連結清單的標頭。                                                                                                                                                                                                                |
| [**InterlockedFlushSList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedflushslist)               | 清除單一連結清單中的整個專案清單。                                                                                                                                                                                                    |
| [**InterlockedPopEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)         | 移除單一連結清單前面的專案。                                                                                                                                                                                                      |
| [**InterlockedPushEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)       | 將專案插入單向連結清單的前面。                                                                                                                                                                                                        |
| [**InterlockedPushListSList**](/previous-versions/windows/desktop/legacy/hh448545(v=vs.85))         | 在另一個單一連結清單的前方插入單一連結清單。                                                                                                                                                                                     |
| [**InterlockedPushListSListEx**](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)     | 在另一個單一連結清單的前方插入單一連結清單。 系統會在多處理器系統上同步處理清單的存取。 此版本的方法不會使用[ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx)呼叫慣例 |
| [**QueryDepthSList**](/windows/win32/api/interlockedapi/nf-interlockedapi-querydepthslist)                           | 抓取指定的單向連結清單中的專案數。                                                                                                                                                                                         |
| [**RtlFirstEntrySList**](/windows/desktop/api/WinNT/nf-winnt-rtlfirstentryslist)                     | 抓取單一連結清單中的第一個專案。                                                                                                                                                                                                           |
| [**RtlInitializeSListHead**](/windows/desktop/api/Winnt/nf-winnt-rtlinitializeslisthead)             | 初始化單一連結清單的標頭。 應用程式應該改為呼叫 [**InitializeSListHead**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead) 。                                                                                                                           |
| [**RtlInterlockedFlushSList**](/windows/desktop/api/Winnt/nf-winnt-rtlinterlockedflushslist)         | 清除單一連結清單中的整個專案清單。 應用程式應該改為呼叫 [**InterlockedFlushSList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedflushslist) 。                                                                                                           |
| [**RtlInterlockedPopEntrySList**](/windows/desktop/api/Winnt/nf-winnt-rtlinterlockedpopentryslist)   | 移除單一連結清單前面的專案。 應用程式應該改為呼叫 [**InterlockedPopEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist) 。                                                                                                       |
| [**RtlInterlockedPushEntrySList**](/windows/desktop/api/Winnt/nf-winnt-rtlinterlockedpushentryslist) | 將專案插入單向連結清單的前面。 應用程式應該改為呼叫 [**InterlockedPushEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist) 。                                                                                                       |
| [**RtlQueryDepthSList**](/windows/desktop/api/Winnt/nf-winnt-rtlquerydepthslist)                     | 抓取指定的單向連結清單中的專案數。 應用程式應該改為呼叫 [**QueryDepthSList**](/windows/win32/api/interlockedapi/nf-interlockedapi-querydepthslist) 。                                                                                                            |



 

## <a name="synchronization-barrier-functions"></a>同步處理屏障函數



| 同步處理屏障函數                                             | Description                                                                                                    |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**DeleteSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier)         | 刪除同步處理屏障。                                                                             |
| [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)           | 進入同步處理屏障，並等待適當數目的執行緒在關卡上會合。 |
| [**InitializeSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-initializesynchronizationbarrier) | 初始化新的同步處理屏障。                                                                     |



 

## <a name="timer-queue-timer-functions"></a>計時器佇列計時器函式



| 計時器-佇列計時器函式                             | Description                  |
|--------------------------------------------------------|------------------------------|
| [**ChangeTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) | 更新計時器佇列計時器。 |
| [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue)           | 建立計時器的佇列。  |
| [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) | 建立計時器佇列計時器。 |
| [**DeleteTimerQueue**](/windows/desktop/api/WinBase/nf-winbase-deletetimerqueue)           | 刪除計時器佇列。       |
| [**DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex)       | 刪除計時器佇列。       |
| [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) | 取消計時器佇列計時器。 |



 

## <a name="wait-functions"></a>Wait 函式



| Wait 函式                                                      | Description                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects)     | 等候一個或所有指定的物件處於已發出信號的狀態，或超過逾時間隔。 這些物件可以包含輸入事件物件。                                                                                                   |
| [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) | 等候一或所有指定的物件處於已發出信號的狀態， (APC) 的 i/o 完成常式或非同步程序呼叫會排入執行緒的佇列中，或經過逾時間隔。 物件的陣列可以包含輸入事件物件。 |
| [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) | 指示執行緒集區中的等候執行緒等候物件。                                                                                                                                                                                            |
| [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)                 | 表示一個物件，並等候另一個物件做為單一作業。                                                                                                                                                                                      |
| [**UnregisterWait**](/windows/desktop/api/WinBase/nf-winbase-unregisterwait)                           | 取消已註冊的等候作業。                                                                                                                                                                                                                       |
| [**UnregisterWaitEx**](unregisterwaitex.md)                       | 取消已註冊的等候作業。                                                                                                                                                                                                                       |
| [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects)           | 等候一個或所有指定的物件處於已發出信號的狀態，或超過逾時間隔。                                                                                                                                                |
| [**WaitForMultipleObjectsEx**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjectsex)       | 等候一或所有指定的物件處於已發出信號的狀態， (APC) 的 i/o 完成常式或非同步程序呼叫會排入執行緒的佇列中，或經過逾時間隔。                                                       |
| [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject)                 | 等候指定的物件處於已發出信號的狀態或逾時間隔。                                                                                                                                                                |
| [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex)             | 等到指定的物件處於已發出信號的狀態， (APC) 的 i/o 完成常式或非同步程序呼叫會排入執行緒或逾時間隔。                                                                       |
| [**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress)                             | 等候指定之位址的值變更。                                                                                                                                                                                                    |
| [**WaitOrTimerCallback**](/previous-versions/windows/desktop/legacy/ms687066(v=vs.85))                 | 應用程式定義的函式，作為計時器回呼或已註冊等候回呼的起始位址。                                                                                                                                    |
| [**WakeByAddressAll**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall)                       | 喚醒所有等候位址值變更的執行緒。                                                                                                                                                                                           |
| [**WakeByAddressSingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle)                 | 喚醒等候位址值變更的執行緒。                                                                                                                                                                                              |



 

## <a name="waitable-timer-functions"></a>可等候-計時器函數



| 可等候-timer 函數                                | Description                                                                                                       |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**CancelWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer)     | 將指定的可等候計時器設定為非作用中狀態。                                                          |
| [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)     | 建立或開啟可等候計時器物件。                                                                         |
| [**CreateWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerexw) | 建立或開啟可等候計時器物件，並將控制碼傳回物件。                                      |
| [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw)         | 開啟現有的已命名可等候計時器物件。                                                                    |
| [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer)           | 啟用指定的可等候計時器。                                                                           |
| [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)       | 啟用指定的可等候計時器，並提供計時器的內容資訊。 .                          |
| [**TimerAPCProc**](/windows/win32/api/synchapi/nc-synchapi-ptimerapcroutine)                   | 搭配 [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) 函數使用的應用程式定義計時器完成常式。 |



 

 

 
