---
description: AddAfter 方法會在指定的位置之後插入清單，並使用 ' pos ' 和 ' plist ' 參數。
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: CGenericList. AddAfter 方法 (Wxlist .h) -pos，plist 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 846e37b961af8d2492b3aff032193e87fb3603eb1751c25f0e3ca8e0c5d38618
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697478"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a>CGenericList. AddAfter 方法 (Wxlist .h) -pos，plist 參數

方法會在 `AddAfter` 指定的位置之後插入清單。

## <a name="syntax"></a>語法


```C++
BOOL AddAfter(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pos* 
</dt> <dd>

要插入清單的位置。 此清單會插入此位置之後。

</dd> <dt>

*pList* 
</dt> <dd>

要插入之清單的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 標頭 | Wxlist (包含： .h)  |
| 程式庫|  (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CGenericList 類別**](cgenericlist.md)
</dt> </dl>

 

 




