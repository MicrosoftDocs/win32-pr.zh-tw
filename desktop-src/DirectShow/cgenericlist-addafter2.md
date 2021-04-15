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
ms.openlocfilehash: c6bbe26e98acc999f067a7b0e96c3716e7e0c0c0
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104514729"
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

 

 




