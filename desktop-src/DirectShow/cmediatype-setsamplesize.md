---
description: SetSampleSize 方法會指定固定樣本大小，或指定樣本具有變數大小。
ms.assetid: b0f9dd7b-4ff9-4d11-9c13-b52d7b1549b5
title: 'CMediaType. SetSampleSize 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0992afd0576c1039397e6ecaa2119a989283136e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001896"
---
# <a name="cmediatypesetsamplesize-method"></a>CMediaType. SetSampleSize 方法

`SetSampleSize`方法會指定固定樣本大小，或指定樣本具有變數大小。

## <a name="syntax"></a>語法


```C++
void SetSampleSize(
   ULONG sz
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*深圳* 
</dt> <dd>

樣本大小（以位元組為單位）或零。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果 *sz* 的值為零，則媒體類型會使用變數樣本大小。 否則，範例大小會固定為 *sz* 個位元組。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 




