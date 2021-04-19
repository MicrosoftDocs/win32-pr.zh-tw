---
description: RemoveHead 方法會移除清單中的第一個專案。
ms.assetid: 95902028-d2c2-4c16-9ca6-ef57174a9292
title: 'CGenericList. RemoveHead 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da9267d6b3e0c3196b3a9d1e873f222649b66684
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984326"
---
# <a name="cgenericlistremovehead-method"></a>CGenericList. RemoveHead 方法

`RemoveHead`方法會移除清單中的第一個專案。

## <a name="syntax"></a>語法


```C++
OBJECT* RemoveHead();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回型別 **物件** 的物件指標 (範本型別) ，如果清單是空的，則為 **Null** 。

## <a name="remarks"></a>備註

這個方法會刪除清單節點，但不會刪除節點所包含的專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CGenericList 類別**](cgenericlist.md)
</dt> </dl>

 

 




