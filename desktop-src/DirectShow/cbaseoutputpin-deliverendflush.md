---
description: CBaseOutputPin. DeliverEndFlush 方法-DeliverEndFlush 方法會要求連接的輸入 pin，以結束清除作業。
ms.assetid: 9f1fd76c-dba7-41c5-b098-9735e4f2571b
title: 'CBaseOutputPin. DeliverEndFlush 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6225406d23dd409c9d2b1ff3dcb7669fa468d8f8cba6c49773dbe057c4545cc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076561"
---
# <a name="cbaseoutputpindeliverendflush-method"></a>CBaseOutputPin. DeliverEndFlush 方法

`DeliverEndFlush`方法會要求連接的輸入 pin 以結束排清作業。

## <a name="syntax"></a>語法


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                                           | 描述                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>              |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | Pin 未連接。<br/> |



 

## <a name="remarks"></a>備註

這個方法會呼叫輸入釘選上的 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseOutputPin 類別**](cbaseoutputpin.md)
</dt> </dl>

 

 




