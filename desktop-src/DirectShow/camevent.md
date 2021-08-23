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
ms.openlocfilehash: ea87239628f001feaa82f84ca8c50941b56d3eb99f486934b551e832d1f588c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955527"
---
# <a name="camevent-class"></a>CAMEvent 類別

![camevent 類別階層](images/util06.png)

**CAMEvent** 類別是手動重設和自動重設事件的包裝函式。

此類別提供便利的方式來管理事件，而不是呼叫像是 [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)、 [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)和 [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent)等函數。



| 受保護的成員變數                          | 描述                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [**m \_ hEvent**](camevent-m-hevent.md)              | 事件控制碼。                                                   |
| 公用方法                                      | 描述                                                     |
| [**CAMEvent**](camevent-camevent.md)               | 函式方法。                                             |
| [**~ CAMEvent**](camevent--camevent.md)             | 函式方法。                                              |
| [**勾選**](camevent-check.md)                     | 檢查是否已設定事件，而不封鎖。              |
| [**重設**](camevent-reset.md)                     | 將事件的狀態設定為未收到信號。                     |
| [**設置**](camevent-set.md)                         | 通知事件。                                              |
| [**等候**](camevent-wait.md)                       | 封鎖直到事件收到信號，或直到發生超時為止。 |
| 運算子                                           | 說明                                                     |
| [**運算子控制碼**](camevent-operator-handle.md) | 捕獲事件控制碼。                                     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

