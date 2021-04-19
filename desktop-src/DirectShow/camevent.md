---
description: CAMEvent 類別是手動重設和自動重設事件的包裝函式。
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: 'CAMEvent 類別 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bde2db8adf2bb713df665e06eb2cc5f8d2a9a00f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978654"
---
# <a name="camevent-class"></a>CAMEvent 類別

![camevent 類別階層](images/util06.png)

**CAMEvent** 類別是手動重設和自動重設事件的包裝函式。

此類別提供便利的方式來管理事件，而不是呼叫像是 [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)、 [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)和 [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent)等函數。



| 受保護的成員變數                          | Description                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [**m \_ hEvent**](camevent-m-hevent.md)              | 事件控制碼。                                                   |
| 公用方法                                      | Description                                                     |
| [**CAMEvent**](camevent-camevent.md)               | 函式方法。                                             |
| [**~ CAMEvent**](camevent--camevent.md)             | 函式方法。                                              |
| [**勾選**](camevent-check.md)                     | 檢查是否已設定事件，而不封鎖。              |
| [**重設**](camevent-reset.md)                     | 將事件的狀態設定為未收到信號。                     |
| [**設定**](camevent-set.md)                         | 通知事件。                                              |
| [**等候**](camevent-wait.md)                       | 封鎖直到事件收到信號，或直到發生超時為止。 |
| 運算子                                           | 說明                                                     |
| [**運算子控制碼**](camevent-operator-handle.md) | 捕獲事件控制碼。                                     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

