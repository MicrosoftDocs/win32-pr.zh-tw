---
description: UnblockOutputPin 方法會解除封鎖 pin。 當 pin 解除封鎖時，它可以傳遞範例、變更其輸出格式，以及重新連接本身。
ms.assetid: ea6e6312-8c7f-44db-ac7f-165dc45dec23
title: 'CDynamicOutputPin. UnblockOutputPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.UnblockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bcde3ccad01e19f3802e2cd19f0f6b873380ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994833"
---
# <a name="cdynamicoutputpinunblockoutputpin-method"></a>CDynamicOutputPin. UnblockOutputPin 方法

方法會解除 `UnblockOutputPin` 封鎖 pin。 當 pin 解除封鎖時，它可以傳遞範例、變更其輸出格式，以及重新連接本身。

## <a name="syntax"></a>語法


```C++
HRESULT UnblockOutputPin();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                             | Description                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Pin 已解除封鎖。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




