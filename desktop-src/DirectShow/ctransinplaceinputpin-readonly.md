---
description: ReadOnly 方法會指出輸入資料流程是否為唯讀。
ms.assetid: 25b8230d-be2b-4129-a1aa-f6b36e95199e
title: 'CTransInPlaceInputPin ReadOnly 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.ReadOnly
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f0dd3ae23da6832911b58e50cba67bcf8e6ec6092c3a31a193bd5a027c5566c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999088"
---
# <a name="ctransinplaceinputpinreadonly-method"></a>CTransInPlaceInputPin ReadOnly 方法

`ReadOnly`方法會指出輸入資料流程是否為唯讀。

## <a name="syntax"></a>語法


```C++
const BOOL ReadOnly();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**m \_ bReadOnly**](ctransinplaceinputpin-m-breadonly.md) 成員變數的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceInputPin 類別**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




