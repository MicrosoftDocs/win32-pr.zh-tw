---
description: AddBefore 方法會在指定的位置之前插入清單。 這個方法會使用 ' pos ' 和 ' pList ' 參數。
ms.assetid: 0fdb2a59-d9de-4dbb-8536-8e10726201d0
title: CGenericList. AddBefore 方法 (Wxlist .h) -pos，pList 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f05d67477bb7e6c89eddfe0a68ad47d83760762fc68cddf6f73c731886f88d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697448"
---
# <a name="cgenericlistaddbefore-method-wxlisth---pos-plist-parameters"></a>CGenericList. AddBefore 方法 (Wxlist .h) -pos，pList 參數

方法會在 `AddBefore` 指定的位置之前插入清單。

## <a name="syntax"></a>語法


```C++
BOOL AddBefore(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pos* 
</dt> <dd>

要插入清單的位置。 此清單會插入此位置之前。

</dd> <dt>

*pList* 
</dt> <dd>

要插入之清單的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** 。 否則，會傳回 **FALSE**。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 標頭 | Wxlist (包含： .h)  |
| 程式庫|  (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CGenericList 類別**](cgenericlist.md)
</dt> </dl>

 

 




