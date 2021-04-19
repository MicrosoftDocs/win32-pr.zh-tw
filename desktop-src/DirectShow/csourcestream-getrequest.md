---
description: GetRequest 方法會等候下一個執行緒要求。
ms.assetid: 2938374b-174f-4276-98a2-20a084bd9bbd
title: 'CSourceStream. GetRequest 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f45e6f6cf269f7aca6741d8e1c150c7054b07f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981307"
---
# <a name="csourcestreamgetrequest-method"></a>CSourceStream. GetRequest 方法

`GetRequest`方法會等候下一個執行緒要求。

## <a name="syntax"></a>語法


```C++
Command GetRequest();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下一個執行緒要求。

## <a name="remarks"></a>備註

這個方法會覆寫 [**CAMThread：： GetRequest**](camthread-getrequest.md) 方法。 傳回值會轉換成下列列舉型別：


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 




