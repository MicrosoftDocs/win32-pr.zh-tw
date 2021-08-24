---
description: WaitEvent 方法會等候，直到指定的事件發出信號為止。
ms.assetid: 64880f46-7b8f-4823-9d50-052e30ecf04b
title: 'CDynamicOutputPin. WaitEvent 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.WaitEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3797c9127d3e931cd64fa35e822eac3151acc7fa1a8c4c0c9e93d6a36c0dfe99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871927"
---
# <a name="cdynamicoutputpinwaitevent-method"></a>CDynamicOutputPin. WaitEvent 方法

`WaitEvent`方法會等候，直到指定的事件發出信號為止。

## <a name="syntax"></a>語法


```C++
static HRESULT WaitEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hEvent* 
</dt> <dd>

事件的控制代碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                  | 描述                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>          |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl> | 非預期的錯誤。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




