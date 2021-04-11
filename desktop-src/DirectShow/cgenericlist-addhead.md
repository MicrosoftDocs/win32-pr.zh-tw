---
description: AddHead 方法會將專案加入至清單的前方。
ms.assetid: 8f0012b7-bbc2-407c-ae5a-9843c2f692dc
title: CGenericList. AddHead 方法 (Wxlist .h) -pObj 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62a32eb177c80d10a876a4b163c8a1609104fbea
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104035450"
---
# <a name="cgenericlistaddhead-method-wxlisth---pobj-parameter"></a>CGenericList. AddHead 方法 (Wxlist .h) -pObj 參數

`AddHead`方法會將專案加入至清單的前方。

## <a name="syntax"></a>語法


```C++
POSITION AddHead(
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

傳回位置值，表示新的標頭位置。 如果方法失敗，則傳回值為 **Null**。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 標頭 | Wxlist (包含： .h)  |
| 程式庫|  (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CGenericList 類別**](cgenericlist.md)
</dt> </dl>

 

 




