---
description: CTransformInputPin. EndFlush 方法-EndFlush 方法會結束清除作業。 這個方法會實 IPin：： EndFlush 方法。
ms.assetid: ebc70df3-e99d-4292-990b-99b79ff06461
title: 'CTransformInputPin. EndFlush 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bca2231f36c3d37f58bb740ddf55132d1c63babba6054629b2a76cc5d7866646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687218"
---
# <a name="ctransforminputpinendflush-method"></a>CTransformInputPin. EndFlush 方法

`EndFlush`方法會結束清除作業。 這個方法會實 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                           | 描述                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>                     |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | 輸出 pin 未連接。<br/> |



 

## <a name="remarks"></a>備註

這個方法會呼叫篩選準則的 [**CTransformFilter：： EndFlush**](ctransformfilter-endflush.md) 方法，以傳遞下游的呼叫。 然後，它會呼叫釘選的 [**CBaseInputPin：： EndFlush**](cbaseinputpin-endflush.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




