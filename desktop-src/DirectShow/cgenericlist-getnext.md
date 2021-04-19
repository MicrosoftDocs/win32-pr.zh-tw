---
description: GetNext 方法會在指定的位置抓取專案，並將位置往前移。
ms.assetid: d24d3388-1af9-4a62-bdb6-d3d3f5b0b97a
title: 'CGenericList. GetNext 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.GetNext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9491e58d817ce2c9dc4fb59fafa9bf96812a013a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978774"
---
# <a name="cgenericlistgetnext-method"></a>CGenericList. GetNext 方法

`GetNext`方法會在指定的位置抓取專案，並將位置往前移。

## <a name="syntax"></a>語法


```C++
OBJECT* GetNext(
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

傳回)  (範本型別 **物件** 之物件的指標。

## <a name="remarks"></a>備註

這個方法會將位置指標往前移到下一個位置。 如果位置指標移動超過清單的結尾，則方法會將它設定為 **Null**。

如果 *rp* 為 **null**，則方法會傳回 **null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CGenericList 類別**](cgenericlist.md)
</dt> </dl>

 

 




