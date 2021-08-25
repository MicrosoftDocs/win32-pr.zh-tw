---
description: AddAfter 方法會在指定的位置之後插入專案，並使用 ' p ' 和 ' pObj ' 參數。
ms.assetid: 3e1f27c5-3e04-424a-8fe3-9bfde4e3824b
title: CGenericList. AddAfter 方法 (Wxlist .h) -p，pObj 參數
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
ms.openlocfilehash: 6de0037d76e63049294b0455c8ec1fbac82963d94febb35f7c9400ec8eae9ab5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697528"
---
# <a name="cgenericlistaddafter-method-wxlisth---p-pobj-parameters"></a>CGenericList. AddAfter 方法 (Wxlist .h) -p，pObj 參數

方法會在 `AddAfter` 指定的位置之後插入專案。

## <a name="syntax"></a>語法


```C++
POSITION AddAfter(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*p* 
</dt> <dd>

要在其後加入專案的位置。 如果 *p* 為 **Null**，則方法會將專案加入至清單的開頭。

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

 

 




