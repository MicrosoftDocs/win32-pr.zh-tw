---
description: GetDueHandle 方法會捕獲要發出信號的事件控制碼。
ms.assetid: 495ea76d-8b94-48a9-8025-06ab18b66693
title: 'CCmdQueue. GetDueHandle 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cb7c8c965c72abe6343a8a75863e0e6969dc5c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991527"
---
# <a name="ccmdqueuegetduehandle-method"></a>CCmdQueue. GetDueHandle 方法

`GetDueHandle`方法會捕獲要發出信號的事件控制碼。

## <a name="syntax"></a>語法


```C++
HANDLE GetDueHandle();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回事件控制碼。

## <a name="remarks"></a>備註

每當有延遲的命令要執行時，就會傳回事件控制碼 (當 [**CCmdQueue：： GetDueCommand**](ccmdqueue-getduecommand.md) 不會封鎖) 時。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCmdQueue 類別**](ccmdqueue.md)
</dt> </dl>

 

 




