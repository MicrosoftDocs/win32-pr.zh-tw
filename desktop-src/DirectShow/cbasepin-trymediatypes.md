---
description: 根據媒體類型的清單，TryMediaTypes 方法會嘗試使用這些類型的其中之一來完成連接。
ms.assetid: cc437e44-bc59-494e-8669-7f539353a794
title: 'CBasePin. TryMediaTypes 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.TryMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a4d4e33ca339c1ade344bb2ca9531bea381d14b4381773673b07e522437e90a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108618"
---
# <a name="cbasepintrymediatypes-method"></a>CBasePin. TryMediaTypes 方法

根據媒體類型的清單，方法會 `TryMediaTypes` 嘗試使用這些類型的其中之一來完成連接。

## <a name="syntax"></a>語法


```C++
virtual HRESULT TryMediaTypes(
         IPin            *pReceivePin,
   const CMediaType      *pmt,
         IEnumMediaTypes *pEnum
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

[**CMediaType**](cmediatype.md)物件的指標，該物件會限制可能的媒體類型或 **Null**。

</dd> <dt>

*pEnum* 
</dt> <dd>

[**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)介面的指標，用來列舉媒體類型的清單。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表中的值。



| 傳回碼                                                                                                  | 描述                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                         | 成功。<br/>                               |
| <dl> <dt>**VFW \_ E \_ 沒有 \_ 可接受的 \_ 類型**</dt> </dl> | 找不到可接受的媒體類型。<br/> |



 

## <a name="remarks"></a>備註

針對 **IEnumMediaTypes** 介面所傳回的每個媒體類型，這個方法會呼叫 [**CBasePin：： AttemptConnection**](cbasepin-attemptconnection.md) 方法來嘗試連接。

如果 *pmt* 參數為非 **Null**，則 pin 會略過不符合此類型的媒體類型。 *Pmt* 參數可以指定部分媒體類型。 部分媒體類型的值為 \_ [主要類型]、[子類型] 或 [格式] 的 GUID Null。 GUID \_ Null 值符合任何類型，類似于 "萬用字元" 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




