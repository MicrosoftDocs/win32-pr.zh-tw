---
description: RemoveTailI 方法會移除清單中的最後一個專案。
ms.assetid: 3e9f88a5-a681-4494-8977-d9a6ec62a849
title: 'CBaseList. RemoveTailI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17c4e151426b54667ea3b9e4cb88be9526e2054b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001114"
---
# <a name="cbaselistremovetaili-method"></a>CBaseList. RemoveTailI 方法

`RemoveTailI`方法會移除清單中的最後一個專案。

## <a name="syntax"></a>語法


```C++
void* RemoveTailI();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回專案的指標，如果清單是空的，則為 **Null** 。

## <a name="remarks"></a>備註

這個方法會刪除清單節點，但不會刪除節點中包含的專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseList 類別**](cbaselist.md)
</dt> </dl>

 

 




