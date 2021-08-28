---
description: IsPartiallySpecified 方法會判斷是否已部分定義媒體類型。 如果主要類型、子類型或格式類型為 GUID Null，則媒體類型為 [部分] \_ 。
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: 'CMediaType. IsPartiallySpecified 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsPartiallySpecified
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c2e7bdbbc43195222b4054f71ec05ebe3c8a7e15ac8c634d57fba61e45bf319
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084468"
---
# <a name="cmediatypeispartiallyspecified-method"></a>CMediaType. IsPartiallySpecified 方法

`IsPartiallySpecified`方法會判斷是否已部分定義媒體類型。 如果主要類型、子類型或格式類型為 GUID Null，則媒體類型為 [ *部分* ] \_ 。

## <a name="syntax"></a>語法


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果媒體類型為部分指定，則傳回 **TRUE** 。 否則，會傳回 **FALSE**。

## <a name="remarks"></a>備註

[**IPin：：連線**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect)方法可以接受部分媒體類型。

其實作並不會實際測試子類型。 如果有指定的格式類型，即使子類型為 GUID Null，也不會將媒體類型視為部分 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 




