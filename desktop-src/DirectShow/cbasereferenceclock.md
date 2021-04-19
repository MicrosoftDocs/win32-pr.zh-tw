---
description: CBaseReferenceClock 類別會實行參考時鐘。
ms.assetid: 898e1968-a9ab-4bb9-abf0-943bfae502e2
title: 'CBaseReferenceClock 類別 (Refclock) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1da55a57faac201a2dbf0ef4d8a9774157d9215d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977571"
---
# <a name="cbasereferenceclock-class"></a>CBaseReferenceClock 類別

![cbasereferenceclock 類別階層](images/rclock01.png)

類別會實 `CBaseReferenceClock` 作為參考時鐘。



| 受保護的成員變數                                                         | Description                                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ pSchedule**](cbasereferenceclock-m-pschedule.md)                            | 處理時鐘排程工作的 [**CAMSchedule**](camschedule.md)物件。 |
| 保護方法                                                                  | Description                                                                            |
| [**~ CBaseReferenceClock**](cbasereferenceclock--cbasereferenceclock.md)           | 函式方法。                                                                     |
| 公用方法                                                                     | Description                                                                            |
| [**CBaseReferenceClock**](cbasereferenceclock-cbasereferenceclock.md)             | 函式方法。                                                                    |
| [**GetPrivateTime**](cbasereferenceclock-getprivatetime.md)                       | 從時鐘取出即時時間。                                                |
| [**SetTimeDelta**](cbasereferenceclock-settimedelta.md)                           | 調整內部時鐘時間。                                                       |
| [**GetSchedule**](cbasereferenceclock-getschedule.md)                             | 抓取時鐘排程物件的指標。                                  |
| [**TriggerThread**](cbasereferenceclock-triggerthread.md)                         | 喚醒處理排程的背景工作執行緒。                                    |
| IReferenceClock 方法                                                            | Description                                                                            |
| [**GetTime**](cbasereferenceclock-gettime.md)                                     | 抓取目前的參考時間。                                                  |
| [**AdviseTime**](cbasereferenceclock-advisetime.md)                               | 建立一次性的建議要求。                                                     |
| [**AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md)                       | 建立週期性建議要求。                                                     |
| [**Unadvise**](cbasereferenceclock-unadvise.md)                                   | 移除暫止的建議要求。                                                      |
| IReferenceClockTimerControl 方法                                                | Description                                                                            |
| [**GetDefaultTimerResolution**](cbasereferenceclock-getdefaulttimerresolution.md) | 傳回目前的參考時鐘計時器解析度。                         |
| [**SetDefaultTimerResolution**](cbasereferenceclock-setdefaulttimerresolution.md) | 設定參考時鐘計時器的解析度。                                    |
| 輔助函式                                                                   | Description                                                                            |
| [**ConvertToMilliseconds**](converttomilliseconds.md)                             | 將參考時間轉換為毫秒。                                             |



 

## <a name="remarks"></a>備註

這個類別會執行支援 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) 和 [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) 介面的參考時鐘。 如果篩選器可以提供篩選圖形的參考時鐘，例如藉由存取硬體裝置，則可以使用這個類別來執行時鐘。

`CBaseReferenceClock`物件會維護兩個不同的時間值：

-   就內部而言， [**CBaseReferenceClock：： GetPrivateTime**](cbasereferenceclock-getprivatetime.md) 方法會傳回時鐘所保留的實際時間。
-   在外部， [**CBaseReferenceClock：： GetTime**](cbasereferenceclock-gettime.md) 方法會傳回篩選圖形的參考時間。

它適用于內部時鐘在短暫期間後執行。 例如，如果時鐘向前偏離，篩選可以向後調整。  (參閱 [**CBaseReferenceClock：： SetTimeDelta**](cbasereferenceclock-settimedelta.md)。 ) **GetTime** 方法會使用 **GetPrivateTime** 所報告的時間值。 不過，參考時間是單純增加的，換句話說，它永遠不會往後執行。 因此，如果內部時鐘回溯執行， **GetTime** 會繼續報告舊的時間，直到內部時鐘趕上為止。

例如，這兩個方法可能會傳回下列順序：

``` syntax
GetPrivateTime: 105, 106, 103, 104, 105, 106, 107, 108
GetTime:        105, 106, 106, 106, 106, 106, 107, 108
```

在第三個時鐘刻度上，內部時鐘會向前跳到103。 **GetTime** 方法會繼續報告106，直到內部時鐘趕上為止。

根據預設， **GetPrivateTime** 會透過呼叫 **timeGetTime** 函數來傳回系統時間。 提供來自外部裝置之參考時鐘的篩選準則，可以執行下列其中一項：

-   覆寫 **GetPrivateTime** 以傳回裝置的時間。
-   監視裝置時間與系統時間之間的差異，然後呼叫 **SetTimeDelta** 來進行修正。

這個類別會使用 [**CAMSchedule**](camschedule.md) 物件來處理建議要求的排程。 如需詳細資訊，請參閱 **CAMSchedule** 類別的檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Refclock (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




