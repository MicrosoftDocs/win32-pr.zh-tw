---
description: 下一個方法會抓取指定的媒體類型數目。 這個方法會實 IEnumMediaTypes：： Next 方法。
ms.assetid: d59dea48-e36c-4ee6-9935-5a47e8a12a9e
title: 'CEnumMediaTypes 下一個方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b5eaa75a52f88539438cec58f024919577518e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998886"
---
# <a name="cenummediatypesnext-method"></a>CEnumMediaTypes. Next 方法

方法會抓取 `Next` 指定的媒體類型數目。 這個方法會實 [**IEnumMediaTypes：： Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Next(
   ULONG         cMediaTypes,
   AM_MEDIA_TYPE **ppMediaTypes,
   ULONG         *pcFetched
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cMediaTypes* 
</dt> <dd>

要取出的媒體類型數目。

</dd> <dt>

*ppMediaTypes* 
</dt> <dd>

[**\_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構指標的陣列，大小為 *cPins*。

</dd> <dt>

*pcFetched* 
</dt> <dd>

變數的指標，此變數會接收此方法所傳回的媒體類型數目。 如果 *cMediaTypes* 是1，則可以是 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                                | Description                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | 未依要求抓取任何數量的媒體類型。<br/>                       |
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 成功。<br/>                                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | 無效引數。<br/>                                                        |
| <dl> <dt>**E \_ 指標**</dt> </dl>                  | **Null** 指標引數。<br/>                                               |
| <dl> <dt>**VFW \_ E \_ 列舉 \_ 不 \_ \_ 同步**</dt> </dl> | Pin 的狀態已變更，且現在與列舉值不一致。<br/> |



 

## <a name="remarks"></a>備註

如果方法成功， *ppMediaTypes* 所指定的陣列就會包含 \_ 媒體 \_ 類型結構的指標。 結構的數目等於 *\* pcFetched*。 藉由呼叫 [**DeleteMediaType**](deletemediatype.md) 函式來釋放每個媒體類型。

這個方法會呼叫釘選的 [**CBasePin：： GetMediaType**](cbasepin-getmediatype.md) 方法，以取得媒體類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CEnumMediaTypes 類別**](cenummediatypes.md)
</dt> </dl>

 

 




