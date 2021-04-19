---
description: StreamingThreadUsingOutputPin 方法會判斷任何執行緒是否正在執行釘選的串流作業。
ms.assetid: b6432a11-4e8b-4eb4-ad8e-aaff9398641b
title: 'CDynamicOutputPin. StreamingThreadUsingOutputPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StreamingThreadUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 797dcb94e227861642de2a05e6edf24f675bb4e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990965"
---
# <a name="cdynamicoutputpinstreamingthreadusingoutputpin-method"></a>CDynamicOutputPin. StreamingThreadUsingOutputPin 方法

StreamingThreadUsingOutputPin 方法會判斷任何執行緒是否正在執行釘選的串流作業。

## <a name="syntax"></a>語法


```C++
virtual bool StreamingThreadUsingOutputPin();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果執行緒正在釘選上執行資料流程作業，則傳回 **TRUE** 。 否則，會傳回 **FALSE**。

## <a name="remarks"></a>備註

如果有任何執行緒成功從 [**CDynamicOutputPin：： StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) 方法傳回，而且尚未對 [**CDynamicOutputPin：： StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) 方法進行對應的呼叫，這個方法會傳回 **TRUE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




