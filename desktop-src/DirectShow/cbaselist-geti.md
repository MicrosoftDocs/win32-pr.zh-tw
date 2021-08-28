---
description: GetI 方法會在指定的位置抓取專案。
ms.assetid: fc775230-491a-49b6-b631-e7d5b8c82d8c
title: 'CBaseList. GetI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f543a38c3394943e3ccb1eeb8bb97d29297a4ca230966940245a2f8a8c121b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087438"
---
# <a name="cbaselistgeti-method"></a>CBaseList. GetI 方法

`GetI`方法會在指定的位置抓取專案。

## <a name="syntax"></a>語法


```C++
void* GetI(
   POSITION pos
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pos* 
</dt> <dd>

要取得之專案的位置指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回專案的指標。

## <a name="remarks"></a>備註

如果 *pos* 是 **null**，則方法會傳回 **null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseList 類別**](cbaselist.md)
</dt> </dl>

 

 




