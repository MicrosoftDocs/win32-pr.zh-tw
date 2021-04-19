---
description: QueryPinInfo 方法會抓取釘選的相關資訊。 這個方法會實 IPin：： QueryPinInfo 方法。
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: 'CBasePin. QueryPinInfo 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f69977a15deb7d84b3370bb6e08c02a4e5129212
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992929"
---
# <a name="cbasepinquerypininfo-method"></a>CBasePin. QueryPinInfo 方法

方法會抓取 `QueryPinInfo` 釘選的相關資訊。 這個方法會實 [**IPin：： QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT QueryPinInfo(
   PIN_INFO *pInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInfo* 
</dt> <dd>

接收釘選資訊之釘選資訊結構的指標。 [**\_**](/windows/win32/api/strmif/ns-strmif-pin_info)

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或 E \_ 指標。

## <a name="remarks"></a>備註

這個方法會針對 PIN 資訊結構的 **achName** 成員使用 [**CBasePin：： m \_ pName**](cbasepin-m-pname.md)成員變數 \_ 。

當方法傳回時，如果 PIN 資訊結構的 **pFilter** 成員 \_ 為非 **Null**，則會有未處理的參考計數。 當您完成時，請務必釋放介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




