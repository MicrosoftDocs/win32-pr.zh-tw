---
description: CBasePin. CheckMediaType 方法-CheckMediaType 方法會判斷 pin 是否接受特定的媒體類型。
ms.assetid: 6a138679-02b7-4ccc-8881-a0d496f84f93
title: 'CBasePin. CheckMediaType 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afe39f3a7aac155f3cc87fa6d58f402043861d1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099395"
---
# <a name="cbasepincheckmediatype-method"></a>CBasePin. CheckMediaType 方法

`CheckMediaType`方法會判斷 pin 是否接受特定的媒體類型。

## <a name="syntax"></a>語法


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pmt* 
</dt> <dd>

[**CMediaType**](cmediatype.md)物件的指標，該物件包含建議的媒體類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果建議的媒體類型是可接受的，則傳回 S OK。 否則，會傳回 \_ FALSE 或錯誤碼。

## <a name="remarks"></a>備註

衍生的類別必須覆寫此純虛擬方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




