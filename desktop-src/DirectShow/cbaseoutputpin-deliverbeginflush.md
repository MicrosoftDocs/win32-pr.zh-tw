---
description: CBaseOutputPin. DeliverBeginFlush 方法-DeliverBeginFlush 方法會要求連接的輸入 pin，以開始進行清除操作。
ms.assetid: 0d7c7bd7-2a7a-42a4-a0de-60205b62e49c
title: 'CBaseOutputPin. DeliverBeginFlush 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22dbd2bccf33d9f203d1505106184500b8cae3ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099516"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a>CBaseOutputPin. DeliverBeginFlush 方法

`DeliverBeginFlush`方法會要求連接的輸入 pin，以開始進行清除操作。

## <a name="syntax"></a>語法


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                                           | Description                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>              |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | Pin 未連接。<br/> |



 

## <a name="remarks"></a>備註

這個方法會呼叫輸入釘選上的 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseOutputPin 類別**](cbaseoutputpin.md)
</dt> </dl>

 

 




