---
description: 從指定的資料流程讀取篩選的資料。
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: 'CPersistStream. ReadFromStream 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.ReadFromStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce6c037fbce9fbaeabf7491b1b840000f67e25d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985568"
---
# <a name="cpersiststreamreadfromstream-method"></a>CPersistStream. ReadFromStream 方法

從指定的資料流程讀取篩選的資料。

## <a name="syntax"></a>語法


```C++
virtual HRESULT ReadFromStream(
   IStream *pStream
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStream* 
</dt> <dd>

要從中讀取資料的 **IStream** 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。 衍生類別應該會傳回有效的 **HRESULT** 值。

## <a name="remarks"></a>備註

預設版本不會讀取任何內容;您可以覆寫它來讀取您類別的特定資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pstream (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPersistStream 類別**](cpersiststream.md)
</dt> </dl>

 

 




