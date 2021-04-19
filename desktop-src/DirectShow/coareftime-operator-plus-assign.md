---
description: 這個運算子會新增兩個參考時間，並將此物件設定為結果。
ms.assetid: 6d29014b-0e31-497e-8326-e3fefc022227
title: 'COARefTime. operator + = 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a03d9e98c3c2f2ca09c3f90f2cb0867d976e02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999418"
---
# <a name="coareftimeoperator-method"></a>COARefTime. operator + = 方法

這個運算子會新增兩個參考時間，並將此物件設定為結果。

## <a name="syntax"></a>語法


```C++
COARefTime& operator+=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rt* \[裁判\]
</dt> <dd>

要加入之 **COARefTime** 物件的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回物件的參考。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COARefTime 類別**](coareftime.md)
</dt> </dl>

 

 




