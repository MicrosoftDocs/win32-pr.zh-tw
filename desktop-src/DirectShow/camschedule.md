---
description: CAMSchedule 類別會實作為參考時鐘的排程器。
ms.assetid: 67aacffb-b781-4323-8973-355a76821401
title: 'CAMSchedule 類別 (Dsschedule) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bef8ad07347284c53a3490c21032070788fa3ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983128"
---
# <a name="camschedule-class"></a>CAMSchedule 類別

類別會實作為參考時鐘的排程器 `CAMSchedule` 。



| 公用方法                                             | Description                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**CAMSchedule**](camschedule-camschedule.md)             | 函式方法。                                                                  |
| [**~ CAMSchedule**](camschedule--camschedule.md)           | 函式方法。 虛擬。                                                          |
| [**GetAdviseCount**](camschedule-getadvisecount.md)       | 抓取暫止的建議要求數目。                                     |
| [**GetNextAdviseTime**](camschedule-getnextadvisetime.md) | 抓取下一個建議要求的時間。                                       |
| [**AddAdvisePacket**](camschedule-addadvisepacket.md)     | 將建議要求新增至暫止的要求清單。                              |
| [**Unadvise**](camschedule-unadvise.md)                   | 移除建議要求。                                                           |
| [**建議**](camschedule-advise.md)                       | 分派排程于指定時間或更早時間的所有要求。          |
| [**GetEvent**](camschedule-getevent.md)                   | 抓取事件控制碼，此控制碼可用來在下一個建議時間中通知變更。 |



 

## <a name="remarks"></a>備註

此 helper 物件會維護參考時鐘的建議要求清單。 [**CBaseReferenceClock**](cbasereferenceclock.md)類別會使用它來協助排程建議的要求。 時鐘會以下列方式使用此物件：

1.  時鐘會建立背景工作執行緒來處理排程。
2.  背景工作執行緒會呼叫 [**CAMSchedule：： GetEvent**](camschedule-getevent.md) 方法，以從排程器取出事件控制碼。 它會等候這個事件，一開始會有無限的超時時間。
3.  為了排程新的建議要求，時鐘會呼叫 [**CAMSchedule：： AddAdvisePacket**](camschedule-addadvisepacket.md) 方法。 建議要求可以是一次或週期性要求。 排程器會以時間順序保留要求清單。
4.  如果要求已加入清單的前面，則排程器會發出事件的信號。  (清單一開始是空的，因此第一個要求會保證事件的信號。 ) 
5.  當事件收到信號時，背景工作執行緒會呼叫 [**CAMSchedule：： Advise**](camschedule-advise.md) 方法，並指定目前的參考時間。 如果有任何擱置的要求過期，排程器就會分派它們。
6.  「建議」方法會傳回下一個要求的時間。 背景工作執行緒會使用這個值來計算新的超時值。
7.  步驟 2 6 會無限期地重複。
8.  若要終止背景工作執行緒，時鐘會設定內部旗標，並為事件發出信號。

在步驟2中，可能是因為事件已發出信號，或等候超時。如果事件收到信號，表示新的要求已新增至清單前端。 工作者執行緒必須計算新的超時值。 另一方面，如果等候時間很大，則表示提出要求已到期且必須分派。 在步驟5中的建議呼叫會處理這兩種情況。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Dsschedule (包含： .h) </dt> </dl>                                                                                |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




