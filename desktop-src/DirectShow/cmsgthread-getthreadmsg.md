---
description: 抓取包含要求的佇列 CMsg 物件。
ms.assetid: 65b76121-c21c-4525-8dde-138783a4964e
title: 'CMsgThread. GetThreadMsg 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b1851ac36590992aca6fa4413119be1df7427bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984093"
---
# <a name="cmsgthreadgetthreadmsg-method"></a>CMsgThread. GetThreadMsg 方法

抓取包含要求的佇列 [**CMsg**](cmsg.md) 物件。

## <a name="syntax"></a>語法


```C++
virtual void GetThreadMsg(
   CMsg *msg
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*msg* 
</dt> <dd>

已配置之 [**CMsg**](cmsg.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

此成員函式會從背景工作執行緒的私用 [**ThreadProc**](camthread-threadproc.md) 函式呼叫，以取得下一個成員函式。 *Msg* 參數應指向已配置的 [**CMsg**](cmsg.md)物件，該物件將會填入佇列中下一個要求的參數。 如果沒有已排入佇列的要求，此成員函式會封鎖，直到下一個要求排入佇列 (呼叫 [**CMsgThread：:P utthreadmsg**](cmsgthread-putthreadmsg.md) 成員函數) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Msgthrd (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMsgThread 類別**](cmsgthread.md)
</dt> </dl>

 

 




