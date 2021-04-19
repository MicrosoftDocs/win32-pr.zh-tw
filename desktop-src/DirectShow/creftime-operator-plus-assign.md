---
description: + = 運算子會新增兩個參考時間。
ms.assetid: 016d3dac-4d7c-490a-83aa-1d88a2080748
title: 'CRefTime. operator + = 方法 (Reftime .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b5e0d9a5a16a963b67643823e5e3b547a1076fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000453"
---
# <a name="creftimeoperator-method"></a>CRefTime. operator + = 方法

+ = 運算子會新增兩個參考時間。

## <a name="syntax"></a>語法


```C++
CRefTime& operator+=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rt* \[裁判\]
</dt> <dd>

**CRefTime** 物件的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回物件的參考。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Reftime (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




