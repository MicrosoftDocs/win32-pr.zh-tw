---
description: AsynchronousBlockOutputPin 方法會封鎖釘選。 在封鎖 pin 之前，方法可能會傳回。
ms.assetid: 14cdc973-f0d3-4d1b-8491-67c1421f630b
title: 'CDynamicOutputPin. AsynchronousBlockOutputPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.AsynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8999f6dbb42c55c036ee3d7fcd02dc34def4bd0a036cf0b5d908d3c280e297e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317788"
---
# <a name="cdynamicoutputpinasynchronousblockoutputpin-method"></a>CDynamicOutputPin. AsynchronousBlockOutputPin 方法

`AsynchronousBlockOutputPin`方法會封鎖釘選。 在封鎖 pin 之前，方法可能會傳回。

## <a name="syntax"></a>語法


```C++
HRESULT AsynchronousBlockOutputPin(
   HANDLE hNotifyCallerPinBlockedEvent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hNotifyCallerPinBlockedEvent* 
</dt> <dd>

事件的控制代碼。 封鎖輸出 pin 或呼叫端取消封鎖作業時，就會發出事件。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                                                    | Description                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                           | 成功。<br/>                                      |
| <dl> <dt>**VFW \_ E \_ PIN \_ 已 \_ 封鎖**</dt> </dl>                   | Pin 已在另一個執行緒上遭到封鎖。<br/>     |
| <dl> <dt>**\_ \_ \_ \_ \_ \_ 此執行緒上已封鎖 \_ VFW E PIN**</dt> </dl> | 呼叫執行緒上已封鎖 Pin。<br/> |



 

## <a name="remarks"></a>備註

請勿從串流執行緒呼叫這個方法。

如果沒有任何串流執行緒使用 pin，這個方法會立即封鎖 pin。 否則，它會將 pin 狀態設定為「擱置」，並傳回。 當串流作業完成時，串流執行緒會呼叫 [**CDynamicOutputPin：： StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) 方法，它會封鎖釘選併發出 **hNotifyCallerPinBlockedEvent** 事件的信號。 若要取消暫止的區塊，請呼叫 [**CDynamicOutputPin：： UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




