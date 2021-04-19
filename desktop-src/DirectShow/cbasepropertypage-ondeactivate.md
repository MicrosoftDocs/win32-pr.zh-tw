---
description: 終結對話方塊視窗時，會呼叫 OnDeactivate 方法。
ms.assetid: 47320e61-324f-4f64-abe1-38fe70e82787
title: 'CBasePropertyPage. OnDeactivate 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDeactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27191e4895c911d3d13a795306eee2b0ad6989ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993656"
---
# <a name="cbasepropertypageondeactivate-method"></a>CBasePropertyPage. OnDeactivate 方法

`OnDeactivate`當對話方塊視窗終結時，會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT OnDeactivate();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

基底類別執行會傳回 S \_ OK。

## <a name="remarks"></a>備註

[**CBasePropertyPage：:D eactivate**](cbasepropertypage-deactivate.md)方法會呼叫 `OnDeactivate` 方法。 覆寫 `OnDeactivate` 以釋放衍生類別在 [**CBasePropertyPage：： OnActivate**](cbasepropertypage-onactivate.md) 方法中取得的任何資源，或視需要執行其他工作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Cprop (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePropertyPage 類別**](cbasepropertypage.md)
</dt> </dl>

 

 




