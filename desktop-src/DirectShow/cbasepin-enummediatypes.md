---
description: EnumMediaTypes 方法會列舉釘選的慣用媒體類型。 這個方法會實 IPin：： EnumMediaTypes 方法。
ms.assetid: 0360f9fc-6876-4a54-8de1-bf289e0e10ae
title: 'CBasePin. EnumMediaTypes 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54aaddbbcde26791b6c55665bfbbb7ff62048238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976104"
---
# <a name="cbasepinenummediatypes-method"></a>CBasePin. EnumMediaTypes 方法

`EnumMediaTypes`方法會列舉釘選的慣用媒體類型。 這個方法會實 [**IPin：： EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppEnum* 
</dt> <dd>

接收 [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) 介面指標之變數的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表中的值。



| 傳回碼                                                                                   | Description                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 成功。<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>       |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | **Null** 指標引數。<br/> |



 

## <a name="remarks"></a>備註

輸入 pin 不需要列舉任何慣用的類型。 輸出 pin 必須列舉至少一個慣用的類型。 否則，這兩個 pin 可能缺乏慣用的類型，因此無法進行連線。

**IEnumMediaTypes** 介面的運作方式就像標準 COM 列舉值一樣。 如需詳細資訊，請參閱 [列舉篩選圖形中的物件](enumerating-objects-in-a-filter-graph.md)。 如果方法成功，則 **IEnumMediaTypes** 介面具有未處理的參考計數。 當您完成時，請務必放開。

[**CEnumMediaTypes**](cenummediatypes.md)基底類別會執行 **IEnumMediaTypes**。 它會呼叫釘選的 [**CBasePin：： GetMediaType**](cbasepin-getmediatype.md) 方法來列舉媒體類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




