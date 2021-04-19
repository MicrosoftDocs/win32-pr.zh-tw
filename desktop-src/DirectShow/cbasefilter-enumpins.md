---
description: EnumPins 方法會列舉此篩選器上的釘選。 這個方法會實 IBaseFilter：： EnumPins 方法。
ms.assetid: c1015ed3-658f-4f96-a1fb-e04b81a9ddb5
title: 'CBaseFilter. EnumPins 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.EnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66a0f88a9749ba1dabb982e2f275da8a4be2a422
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983121"
---
# <a name="cbasefilterenumpins-method"></a>CBaseFilter. EnumPins 方法

`EnumPins`方法會列舉此篩選器上的釘選。 這個方法會實 [**IBaseFilter：： EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT EnumPins(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppEnum* 
</dt> <dd>

接收 [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) 介面指標之變數的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值。



| 傳回碼                                                                                   | Description                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | Success<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足<br/>       |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | **Null** 指標引數<br/> |



 

## <a name="remarks"></a>備註

這個方法會建立 [**CEnumPins**](cenumpins.md) 基類的實例，並將指標傳回給 **IEnumPins** 類型的物件。 **CEnumPins** 類別會呼叫篩選準則的 [**CBaseFilter：： GetPin**](cbasefilter-getpin.md)方法，以列舉篩選上的釘選。

如果此方法成功，則 **IEnumPins** 介面具有未處理的參考計數。 呼叫端必須釋放介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




