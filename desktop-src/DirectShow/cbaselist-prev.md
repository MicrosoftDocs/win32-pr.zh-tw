---
description: 前一個方法會抓取清單中先前的位置。
ms.assetid: 537c3019-373a-4974-a42e-72150da72767
title: 'CBaseList 前一個方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Prev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03c35a89754b27aa67a5bba33ee694433d74c0fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976096"
---
# <a name="cbaselistprev-method"></a>CBaseList. 上一方法

方法會抓取 `Prev` 清單中先前的位置。

## <a name="syntax"></a>語法


```C++
POSITION Prev(
   POSITION pos
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pos* 
</dt> <dd>

位置值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回在 *pos* 中指定位置之前的位置指標。

## <a name="remarks"></a>備註

如果 *pos* 是清單中的第一個位置，則方法會傳回 **Null**。 如果 *pos* 是 **Null**，則方法會傳回清單中的最後一個位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseList 類別**](cbaselist.md)
</dt> </dl>

 

 




