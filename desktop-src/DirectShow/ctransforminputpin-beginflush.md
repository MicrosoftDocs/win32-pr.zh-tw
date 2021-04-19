---
description: BeginFlush 方法會開始進行清除作業。 這個方法會實 IPin：： BeginFlush 方法。
ms.assetid: 7c76ca06-dc3c-4f9a-9761-32aea7db4c7e
title: 'CTransformInputPin. BeginFlush 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4d028634364ca59ae293d9ebb60a464974ccd74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998405"
---
# <a name="ctransforminputpinbeginflush-method"></a>CTransformInputPin. BeginFlush 方法

`BeginFlush`方法會開始清除作業。 這個方法會實 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                           | Description                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>                     |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | 輸出 pin 未連接。<br/> |



 

## <a name="remarks"></a>備註

這個方法會呼叫釘選的 [**CBaseInputPin：： BeginFlush**](cbaseinputpin-beginflush.md) 方法。 然後，它會呼叫篩選器的 [**CTransformFilter：： BeginFlush**](ctransformfilter-beginflush.md) 方法，以傳遞下游的呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




