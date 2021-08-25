---
description: EndOfStream 方法會向篩選發出通知，指出輸入 pin 不需要任何其他資料。
ms.assetid: b8fc3976-e3d4-4f16-82b0-3900ad6a740c
title: 'CTransformFilter. EndOfStream 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade419666b1df36e851d5d945e14d9035c1377145cecd472244c9178758f45f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907628"
---
# <a name="ctransformfilterendofstream-method"></a>CTransformFilter. EndOfStream 方法

`EndOfStream`方法會向篩選通知，輸入 pin 不需要任何其他資料。

## <a name="syntax"></a>語法


```C++
virtual HRESULT EndOfStream();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或其他 **HRESULT** 值。

## <a name="remarks"></a>備註

輸入釘選的 [**CTransformInputPin：： EndOfStream**](ctransforminputpin-endofstream.md) 方法會呼叫這個方法。 這個方法會傳遞下游的資料流程結束通知。 如果衍生類別使用背景工作執行緒來傳遞媒體範例，則應該覆寫這個方法，並將資料流程結束通知排入佇列。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




