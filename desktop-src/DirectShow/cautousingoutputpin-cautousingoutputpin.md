---
description: 函式方法。 此函式會取得指定之 pin 的存取權。
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: 'CAutoUsingOutputPin. CAutoUsingOutputPin (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin.CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94bafcdcb6e44a07afdccea382d783c20a9ad2ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001155"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a>CAutoUsingOutputPin. CAutoUsingOutputPin 函數

函式方法。 此函式會取得指定之 pin 的存取權。

## <a name="syntax"></a>語法


```C++
CAutoUsingOutputPin(
   CDynamicOutputPin *pOutputPin,
   HRESULT           *phr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pOutputPin* 
</dt> <dd>

[**CDynamicOutputPin**](cdynamicoutputpin.md)物件的指標。

</dd> <dt>

*phr* 
</dt> <dd>

包含 **HRESULT** 值之變數的指標。 值必須為 S \_ OK。

</dd> </dl>

## <a name="remarks"></a>備註

當方法傳回時， *\* phr* 的值會指出方法的成功或失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAutoUsingOutputPin 類別**](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 




