---
description: CancelNotification 方法會取消排程轉譯的計時器事件。
ms.assetid: 56ddf692-a2e3-40f2-848f-2d592601ec00
title: 'CBaseRenderer. CancelNotification 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CancelNotification
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3330f369c5fcc45fe051a1964a504d5d40fcd091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994347"
---
# <a name="cbaserenderercancelnotification-method"></a>CBaseRenderer. CancelNotification 方法

`CancelNotification`方法會取消排程轉譯的計時器事件。

## <a name="syntax"></a>語法


```C++
virtual HRESULT CancelNotification();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                             | Description                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 沒有暫止的計時器事件。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                          |



 

## <a name="remarks"></a>備註

當串流停止時，篩選會呼叫這個方法。 方法會取消任何已排程的呈現。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




