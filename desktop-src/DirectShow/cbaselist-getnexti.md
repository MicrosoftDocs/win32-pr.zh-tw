---
description: GetNextI 方法會在指定的位置抓取專案，並將位置往前移。
ms.assetid: 3ec217ec-b0f9-4ff4-bdb7-ac204df99010
title: 'CBaseList. GetNextI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetNextI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f96be8d8cdf286a4017e56af7050970d45e8a56e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992937"
---
# <a name="cbaselistgetnexti-method"></a>CBaseList. GetNextI 方法

`GetNextI`方法會在指定的位置抓取專案，並將位置往前移。

## <a name="syntax"></a>語法


```C++
void* GetNextI(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rp* \[裁判\]
</dt> <dd>

位置值的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回專案的指標。 如果 *rp* 為 **null**，則方法會傳回 **null**。

## <a name="remarks"></a>備註

這個方法會將位置指標往前移到下一個位置。 如果位置指標移動超過清單的結尾，則方法會將它設定為 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseList 類別**](cbaselist.md)
</dt> </dl>

 

 




