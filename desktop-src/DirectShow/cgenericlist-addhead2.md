---
description: AddHead 方法會將清單新增至清單前端。
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: CGenericList. AddHead 方法 (Wxlist .h) -pList 參數
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
ms.openlocfilehash: c26667ce12af902f3d5cf355a6556dc95e5dd1f5e0cad77f944e663eeef8ce67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656144"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a>CGenericList. AddHead 方法 (Wxlist .h) -pList 參數

`AddHead`方法會將清單新增至清單前端。

## <a name="syntax"></a>語法


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pList* 
</dt> <dd>

要加入之專案清單的指標。

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

 

 




