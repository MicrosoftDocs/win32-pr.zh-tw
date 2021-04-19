---
description: DoSetWindowForeground 方法會將視窗帶入前景。
ms.assetid: 5aace88b-14c0-41ce-95a3-0e255ca56ae6
title: 'CBaseWindow. DoSetWindowForeground 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoSetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16a4c8bf41c042c99624289fa26fe252dee62747
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987011"
---
# <a name="cbasewindowdosetwindowforeground-method"></a>CBaseWindow. DoSetWindowForeground 方法

方法會將 `DoSetWindowForeground` 視窗帶到前景。

## <a name="syntax"></a>語法


```C++
void DoSetWindowForeground(
   BOOL bFocus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bFocus* 
</dt> <dd>

指定是否要提供視窗焦點的布林值。 如果值為 **TRUE**，則視窗會取得焦點。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




