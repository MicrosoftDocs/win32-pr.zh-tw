---
description: AddTail 方法會將清單附加至清單結尾。
ms.assetid: 006cccc5-4fb2-4e3f-9481-5d10c090d24e
title: CGenericList. AddTail 方法 (Wxlist .h) -pList 參數
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
ms.openlocfilehash: 6695df796e54e85ba32dcd63cce2940e00a0199c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106984279"
---
# <a name="cgenericlistaddtail-method-wxlisth---plist-parameter"></a>CGenericList. AddTail 方法 (Wxlist .h) -pList 參數

方法會將 `AddTail` 清單附加至清單結尾。

## <a name="syntax"></a>語法


```C++
BOOL AddTail(
   CGenericList<OBJECT> pList
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pList* 
</dt> <dd>

要附加之清單的指標。

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

 

 




