---
description: QueryId 方法會抓取 pin 識別碼。 這個方法會實 IPin：： QueryId 方法。
ms.assetid: b365a574-61b4-454c-b062-8826cbe10f03
title: 'CBasePin. QueryId 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa14fb933c89da0b0b6d2eebfab480b5508a3666
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989609"
---
# <a name="cbasepinqueryid-method"></a>CBasePin. QueryId 方法

方法會抓取 `QueryId` pin 識別碼。 這個方法會實 [**IPin：： QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*識別碼* 
</dt> <dd>

Pin 識別碼的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表中的值。



| 傳回碼                                                                                   | Description                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 成功。<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>       |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | **Null** 指標引數。<br/> |



 

## <a name="remarks"></a>備註

這個方法會傳回 [**CBasePin：： m \_ pName**](cbasepin-m-pname.md) 成員變數的複本。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




