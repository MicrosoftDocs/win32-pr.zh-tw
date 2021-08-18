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
ms.openlocfilehash: c0594eed7f253f7e540f843dfc3c3de6481d7dbede3f25d1534e52181ef0585b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057518"
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

 

 




