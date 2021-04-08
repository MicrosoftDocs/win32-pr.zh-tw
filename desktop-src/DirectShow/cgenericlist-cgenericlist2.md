---
description: 瞭解 CGenericList. CGenericList () Wxlist 的函式方法。 這個方法會使用 ' pName ' 參數。
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: CGenericList. CGenericList 函式 (Wxlist .h) -pName 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a2aa2347e963839c18d904f2819d50de8d6d9c3
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "103854100"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a>CGenericList. CGenericList 函式 (Wxlist .h) -pName 參數

函式方法。

## <a name="syntax"></a>語法


```C++
CGenericList(
   TCHAR *pName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

清單名稱的指標。

</dd> </dl>

## <a name="remarks"></a>備註

為了提高效率， `CGenericList` 類別會維護清單節點的快取。 此版本的函式會使用預設快取大小。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 標頭 | Wxlist (包含： .h)  |
| 程式庫|  (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CGenericList 類別**](cgenericlist.md)
</dt> </dl>

 

 




