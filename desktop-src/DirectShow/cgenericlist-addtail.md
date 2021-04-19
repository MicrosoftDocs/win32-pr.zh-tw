---
description: AddTail 方法會將專案附加至清單結尾。
ms.assetid: e365a23e-7447-42ec-b836-21dd68962db1
title: CGenericList. AddTail 方法 (Wxlist .h) -pObj 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f1e7cd3d8758107b9529114a75b3a90527937c6
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106993925"
---
# <a name="cgenericlistaddtail-method-wxlisth---pobj-parameter"></a>CGenericList. AddTail 方法 (Wxlist .h) -pObj 參數

方法會將 `AddTail` 專案附加至清單結尾。

## <a name="syntax"></a>語法


```C++
POSITION AddTail(
   OBJECT *pObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pObj* 
</dt> <dd>

**物件** 類型物件的指標， (範本類型) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回新結尾位置的位置值。 如果方法失敗，則會傳回 **Null**。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 標頭 | Wxlist (包含： .h)  |
| 程式庫|  (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CGenericList 類別**](cgenericlist.md)
</dt> </dl>

 

 




