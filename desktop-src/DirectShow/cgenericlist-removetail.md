---
description: RemoveTail 方法會移除清單中的最後一個專案。
ms.assetid: 377af676-8042-430e-87a6-b41c00482a90
title: 'CGenericList. RemoveTail 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed0b39d72eac68310dacdf2bfdc1d3c28bb35695b3d77230ba37f6fe81c417ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656153"
---
# <a name="cgenericlistremovetail-method"></a>CGenericList. RemoveTail 方法

`RemoveTail`方法會移除清單中的最後一個專案。

## <a name="syntax"></a>語法


```C++
OBJECT* RemoveTail();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回型別 **物件** 的物件指標 (範本型別) ，如果清單是空的，則為 **Null** 。

## <a name="remarks"></a>備註

這個方法會刪除清單節點，但不會刪除節點中包含的專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CGenericList 類別**](cgenericlist.md)
</dt> </dl>

 

 




