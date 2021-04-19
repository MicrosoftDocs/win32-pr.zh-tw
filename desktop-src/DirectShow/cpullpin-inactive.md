---
description: 非使用中的方法會關閉從輸出釘選資料的背景工作執行緒。 這個方法也會解除配置器。
ms.assetid: 90b91686-b9a8-4196-b559-de924334f11c
title: 'CPullPin：非使用中方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f32084428a36032152d3c3297b1fc9419e51cb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990749"
---
# <a name="cpullpininactive-method"></a>CPullPin 方法

`Inactive`方法會關閉從輸出圖釘提取資料的背景工作執行緒。 這個方法也會解除配置器。

## <a name="syntax"></a>語法


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

當擁有篩選變成非使用中時，請呼叫這個方法。  (如果您的輸入 pin 衍生自 [**CBasePin**](cbasepin.md)，請覆寫 [**CBasePin：：非**](cbasepin-inactive.md) 使用中的方法。 ) 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pullpin。h</dt> </dl>                                                                                                       |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPullPin 類別**](cpullpin.md)
</dt> </dl>

 

 




