---
description: AddBefore 方法會在指定的位置之前插入專案。 這個方法會使用 ' p ' 和 ' pObj ' 參數。
ms.assetid: ec10fd08-6bb9-4357-830c-78b3d3a32e03
title: CGenericList. AddBefore 方法 (Wxlist .h) -p，pObj 參數
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
ms.openlocfilehash: a79c0edb8938e3d3d5a89b4a84a418846b9f1986
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "103946282"
---
# <a name="cgenericlistaddbefore-method-wxlisth---p-pobj-parameters"></a>CGenericList. AddBefore 方法 (Wxlist .h) -p，pObj 參數

方法會在 `AddBefore` 指定的位置之前插入專案。

## <a name="syntax"></a>語法


```C++
POSITION AddBefore(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*P* 
</dt> <dd>

要插入清單的位置。 如果 *p* 是 **Null**，這個方法會將專案加入至清單的結尾。

</dd> <dt>

*pObj* 
</dt> <dd>

**物件** 類型物件的指標， (範本類型) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回所插入專案的位置指標。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 標頭 | Wxlist (包含： .h)  |
| 程式庫|  (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CGenericList 類別**](cgenericlist.md)
</dt> </dl>

 

 




