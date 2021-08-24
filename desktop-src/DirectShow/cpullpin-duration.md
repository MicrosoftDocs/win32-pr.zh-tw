---
description: Duration 方法會捕獲資料流程的持續時間。
ms.assetid: 82fbd7f5-36dc-4e81-9ce5-9ee28adf73ef
title: 'CPullPin Duration 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fdc944400bc80fbd5228ac06e2ba1c01f7315305071f7a24c0b38eb125ee1399
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767978"
---
# <a name="cpullpinduration-method"></a>CPullPin Duration 方法

`Duration`方法會捕獲資料流程的持續時間。

## <a name="syntax"></a>語法


```C++
HRESULT Duration(
   REFERENCE_TIME *ptDuration
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ptDuration* 
</dt> <dd>

接收持續時間之變數的指標，以位元組乘以10000000。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

在呼叫 [**CPullPin：：連線**](cpullpin-connect.md)方法之前，持續時間為不定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pullpin。h</dt> </dl>                                                                                                       |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPullPin 類別**](cpullpin.md)
</dt> </dl>

 

 




