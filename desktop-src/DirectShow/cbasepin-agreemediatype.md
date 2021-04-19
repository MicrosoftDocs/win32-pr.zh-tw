---
description: AgreeMediaType 方法會搜尋媒體類型，以建立 pin 連接。
ms.assetid: 545186d2-b5e8-4833-b0ff-11160c1dd53b
title: 'CBasePin. AgreeMediaType 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AgreeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e5cdea12cb8bca3319f908fe697251a3d4699d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998678"
---
# <a name="cbasepinagreemediatype-method"></a>CBasePin. AgreeMediaType 方法

此 `AgreeMediaType` 方法會搜尋媒體類型，以建立 pin 連接。

## <a name="syntax"></a>語法


```C++
virtual HRESULT AgreeMediaType(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pReceivePin* 
</dt> <dd>

接收釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。

</dd> <dt>

*Pmt* 
</dt> <dd>

指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標，或 **為 Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表中的值。



| 傳回碼                                                                                                  | Description                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                         | 成功。<br/>                            |
| <dl> <dt>**VFW \_ E \_ 沒有 \_ 可接受的 \_ 類型**</dt> </dl> | 找不到可接受的媒體類型。<br/> |



 

## <a name="remarks"></a>備註

如果 *pmt* 參數為非 **Null** ，且完整指定媒體類型，這個方法會嘗試使用該媒體類型的連接。 如果嘗試失敗，方法會傳回錯誤。

如果 *pmt* 參數為 **Null** 或指定部分媒體類型，這個方法會依下列順序嘗試媒體類型：

1.  接收釘選的慣用媒體類型。
2.  此 pin 的慣用媒體類型。

慣用的媒體類型會以 [**CBasePin：： EnumMediaTypes**](cbasepin-enummediatypes.md) 方法列舉，而產生的列舉值會傳遞至 [**CBasePin：： TryMediaTypes**](cbasepin-trymediatypes.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




