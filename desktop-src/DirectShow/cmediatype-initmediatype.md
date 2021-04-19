---
description: InitMediaType 方法會初始化媒體類型。
ms.assetid: 141ced68-11ed-4567-b2e1-82c040d3b4a4
title: " (Mtype 的 CMediaType.InitMediaType 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.InitMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3bbe170c6d896f3b28d9b85cf49f18269341d50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999070"
---
# <a name="cmediatypeinitmediatype-method"></a>CMediaType.InitMediaType 方法

`InitMediaType`方法會初始化媒體類型。

## <a name="syntax"></a>語法


```C++
void InitMediaType();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會將物件的記憶體設為零，將固定大小樣本大小的屬性設定為 **TRUE**，並將樣本大小設定為1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 




