---
description: QueryAccept 方法會判斷 pin 是否接受指定的媒體類型。 這個方法會實 IPin：： QueryAccept 方法。
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: 'CBasePin. QueryAccept 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryAccept
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2c4a982f583d1780dbab37d982fd9a54601e141
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995522"
---
# <a name="cbasepinqueryaccept-method"></a>CBasePin. QueryAccept 方法

`QueryAccept`方法會判斷 pin 是否接受指定的媒體類型。 這個方法會實 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pmt* 
</dt> <dd>

指定媒體類型之 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果媒體類型是可接受的，則傳回 S OK。 否則，會傳回 \_ FALSE。

## <a name="remarks"></a>備註

在基類中，這個方法會委派給 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法。 如果 **CheckMediaType** 失敗，會傳回 `QueryAccept` \_ FALSE。

這個方法不會保存釘選的重要區段 ([**CBasePin：： m \_ pLock**](cbasepin-m-plock.md)) 。 如果您的衍生類別動態修改了可接受的媒體類型集，您應該覆寫此方法以保存重要區段。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




