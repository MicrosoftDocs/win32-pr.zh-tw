---
description: Find 方法會抓取保留指定專案的第一個位置。
ms.assetid: 8e2a3e5d-96e6-4f40-8e2a-4dc8c21088cd
title: 'CGenericList： Find 方法 (Wxlist) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Find
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a21f16e25d8a2ebba4494a850bc456a7b579f2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989876"
---
# <a name="cgenericlistfind-method"></a>CGenericList，Find 方法

`Find`方法會抓取保留指定專案的第一個位置。

## <a name="syntax"></a>語法


```C++
POSITION Find(
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

傳回位置值，如果專案不在清單中，則 **為 Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CGenericList 類別**](cgenericlist.md)
</dt> </dl>

 

 




