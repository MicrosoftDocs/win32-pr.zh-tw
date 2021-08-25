---
description: SynchronousBlockOutputPin 方法會封鎖釘選;在封鎖 pin 之前，不會返回。
ms.assetid: 10fdb788-bc72-4eda-b60b-af83f954d689
title: 'CDynamicOutputPin. SynchronousBlockOutputPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d8613a27d8af2dc2b69a93a1f324db17b054cf2dd312fdb0c9d6cd63e6c89ca8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916308"
---
# <a name="cdynamicoutputpinsynchronousblockoutputpin-method"></a>CDynamicOutputPin. SynchronousBlockOutputPin 方法

`SynchronousBlockOutputPin`方法會封鎖釘選; 在封鎖 pin 之前，不會傳回。

## <a name="syntax"></a>語法


```C++
HRESULT SynchronousBlockOutputPin();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                                                    | 描述                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                           | 成功。<br/>                                      |
| <dl> <dt>**VFW \_ E \_ PIN \_ 已 \_ 封鎖**</dt> </dl>                   | Pin 已在另一個執行緒上遭到封鎖。<br/>     |
| <dl> <dt>**\_ \_ \_ \_ \_ \_ 此執行緒上已封鎖 \_ VFW E PIN**</dt> </dl> | 呼叫執行緒上已封鎖 Pin。<br/> |



 

## <a name="remarks"></a>備註

請勿從串流執行緒呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




