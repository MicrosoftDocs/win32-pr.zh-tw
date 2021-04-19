---
description: AddBefore 方法會在指定的位置之前插入清單。
ms.assetid: a4c0dbec-64a0-445b-95e5-000603cc0264
title: 'CBaseList. AddBefore 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3c25b2dd545b3e6698404bf00f82d1086bfb81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981295"
---
# <a name="cbaselistaddbefore-method"></a>CBaseList. AddBefore 方法

方法會在 `AddBefore` 指定的位置之前插入清單。

## <a name="syntax"></a>語法


```C++
BOOL AddBefore(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pos* 
</dt> <dd>

要插入清單的位置。

</dd> <dt>

*pList* 
</dt> <dd>

要插入之清單的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** 。 否則，會傳回 **FALSE**。

## <a name="remarks"></a>備註

現有的位置指標，包括 *pos* 參數中指定的指標，會保持有效。 如果此方法失敗，可能會加入一些專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseList 類別**](cbaselist.md)
</dt> </dl>

 

 




