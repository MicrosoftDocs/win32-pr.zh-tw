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
ms.openlocfilehash: 117138e80db91529d6a2baf93577a6a4dfd542d2975bf2ce6f89124a3d7aefe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813838"
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

 

 




