---
description: DoCreateWindow 方法會建立視窗。
ms.assetid: bbe38a71-bbf7-4380-96a3-074b992a1d1e
title: " (Winutil 的 CBaseWindow.DoCreateWindow 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoCreateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76bea1523f48a6e22a3c2d9370fa32bcea022621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994193"
---
# <a name="cbasewindowdocreatewindow-method"></a>CBaseWindow.DoCreateWindow 方法

`DoCreateWindow`方法會建立視窗。

## <a name="syntax"></a>語法


```C++
HRESULT DoCreateWindow();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

\_如果成功，則傳回，否則會傳回指出失敗原因的 **HRESULT** 值。

## <a name="remarks"></a>備註

[**CBaseWindow：:P reparewindow**](cbasewindow-preparewindow.md)方法會呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




