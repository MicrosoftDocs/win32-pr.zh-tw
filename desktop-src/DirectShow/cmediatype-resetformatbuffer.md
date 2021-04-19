---
description: ResetFormatBuffer 方法會刪除格式區塊。 方法會將 AM 媒體類型結構的 cbFormat 和 pbFormat 成員設定 \_ \_ 為 Null。
ms.assetid: 5eb6dfc8-cfba-41dd-b422-8fe93ca904c1
title: 'CMediaType. ResetFormatBuffer 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.ResetFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25047060b956e2374964c1620c010dbdf458307c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987017"
---
# <a name="cmediatyperesetformatbuffer-method"></a>CMediaType. ResetFormatBuffer 方法

`ResetFormatBuffer`方法會刪除格式區塊。 方法會將 **AM \_ 媒體 \_ 類型** 結構的 **cbFormat** 和 **pbFormat** 成員設定為 **Null**。

## <a name="syntax"></a>語法


```C++
void ResetFormatBuffer();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 




