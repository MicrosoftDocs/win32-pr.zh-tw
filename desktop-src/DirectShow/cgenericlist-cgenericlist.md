---
description: 瞭解 CGenericList. CGenericList () Wxlist 的函式方法。 這個方法會使用 ' pName ' 和 ' iItems ' 參數。
ms.assetid: 2258ecd6-7594-4ff8-961b-9e5e1ae9ff82
title: 'CGenericList. CGenericList (Wxlist. h) '
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
ms.openlocfilehash: 77a3dd932872b9d96c754ac5b1db184dcf99cf03
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104323456"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-iitems-parameters"></a>CGenericList. CGenericList (Wxlist .h) -pName，iItems 參數

函式方法。

## <a name="syntax"></a>語法


```C++
CGenericList(
   TCHAR *pName,
   INT   iItems,
   BOOL  bLock,
   BOOL  bAlert
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

清單名稱的指標。

</dd> <dt>

*iItems* 
</dt> <dd>

節點快取的大小。

</dd> <dt>

*塊* 
</dt> <dd>

未使用。

</dd> <dt>

*bAlert* 
</dt> <dd>

未使用。

</dd> </dl>

## <a name="remarks"></a>備註

為了提高效率， `CGenericList` 類別會維護清單節點的快取。 如果您知道清單將保留多少專案，請使用此版本的函式。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 標頭 | Wxlist (包含： .h)  |
| 程式庫|  (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CGenericList 類別**](cgenericlist.md)
</dt> </dl>

 

 




