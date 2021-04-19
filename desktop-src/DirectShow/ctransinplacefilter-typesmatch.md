---
description: TypesMatch 方法會判斷輸入媒體類型是否符合輸出媒體類型。
ms.assetid: e814d532-70ce-4f9b-9ce3-172daea0dad5
title: 'CTransInPlaceFilter. TypesMatch 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.TypesMatch
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea8f3da122b8c8dbc6ba113d8088f71d5b19f104
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990690"
---
# <a name="ctransinplacefiltertypesmatch-method"></a>CTransInPlaceFilter. TypesMatch 方法

`TypesMatch`方法會判斷輸入媒體類型是否符合輸出媒體類型。

## <a name="syntax"></a>語法


```C++
BOOL TypesMatch();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果輸入和輸出媒體類型相同，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceFilter 類別**](ctransinplacefilter.md)
</dt> </dl>

 

 




