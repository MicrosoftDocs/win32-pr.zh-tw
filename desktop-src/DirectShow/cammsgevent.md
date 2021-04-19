---
description: CAMMsgEvent 類別是執行訊息處理之事件物件的包裝函式。
ms.assetid: 4b94febe-169f-4f04-be93-043a8c75e3b4
title: 'CAMMsgEvent 類別 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ebac7aae11f7a7b7d6b846e262e93b5759210b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997004"
---
# <a name="cammsgevent-class"></a>CAMMsgEvent 類別

![cammsgevent 類別階層](images/util06.png)

`CAMMsgEvent`類別是執行訊息處理之事件物件的包裝函式。

這個類別衍生自 [**CAMEvent**](camevent.md) 物件。 它會新增一個方法 [**CAMMsgEvent：： WaitMsg**](cammsgevent-waitmsg.md)，這會在等候時分派傳入訊息。



| 公用方法                                 | Description                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| [**CAMMsgEvent**](cammsgevent-cammsgevent.md) | 建構函式。                                                         |
| [**WaitMsg**](cammsgevent-waitmsg.md)         | 在分派傳送的訊息時，等候事件收到信號。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




