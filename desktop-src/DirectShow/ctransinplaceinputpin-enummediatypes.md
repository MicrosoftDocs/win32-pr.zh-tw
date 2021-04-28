---
description: CTransInPlaceInputPin. EnumMediaTypes 方法-EnumMediaTypes 方法會列舉釘選的慣用媒體類型。 這個方法會實 IPin：： EnumMediaTypes 方法。
ms.assetid: 0c28b4b0-a45f-400f-a6d7-7668458f9642
title: 'CTransInPlaceInputPin. EnumMediaTypes 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f9e05d0e9db50cabc700da7b3803c1606efab78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094756"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a>CTransInPlaceInputPin. EnumMediaTypes 方法

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

接收 [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                           | Description                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | 記憶體不足。<br/>             |
| <dl> <dt>**E \_ 指標**</dt> </dl>             | **Null** 指標。<br/>                |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | 輸出針腳未連接。<br/> |



 

## <a name="remarks"></a>備註

這個方法會從下游輸入 pin 傳回 **IEnumMediaTypes** 介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceInputPin 類別**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




