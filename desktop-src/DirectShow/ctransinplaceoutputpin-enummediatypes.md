---
description: CTransInPlaceOutputPin. EnumMediaTypes 方法-EnumMediaTypes 方法會列舉釘選的慣用媒體類型。 這個方法會實 IPin：： EnumMediaTypes 方法。
ms.assetid: 942c6594-3053-484a-a0f7-286dcd3f7550
title: 'CTransInPlaceOutputPin. EnumMediaTypes 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7a351f947b0526b8daf77b0b15ea0d2a2894ef6ff90390be484b5d0ce4b7fa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076168"
---
# <a name="ctransinplaceoutputpinenummediatypes-method"></a>CTransInPlaceOutputPin. EnumMediaTypes 方法

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



| 傳回碼                                                                                           | 描述                                         |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | 記憶體不足。<br/>                     |
| <dl> <dt>**E \_ 指標**</dt> </dl>             | **Null** 指標。<br/>                        |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | 篩選的輸入 pin 未連接。<br/> |



 

## <a name="remarks"></a>備註

這個方法會從上游輸出釘選傳回 **IEnumMediaTypes** 介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceOutputPin 類別**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




