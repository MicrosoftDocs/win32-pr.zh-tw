---
description: SetSubtype 方法會指定子類型。
ms.assetid: cf52e0dc-d75b-408e-a63c-481d55151d4a
title: 'CMediaType. SetSubtype 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSubtype
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6474777b1b2e91ce0b676fdc7dbd572d7c622f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989783"
---
# <a name="cmediatypesetsubtype-method"></a>CMediaType. SetSubtype 方法

`SetSubtype`方法會指定子類型。

## <a name="syntax"></a>語法


```C++
void SetSubtype(
   const GUID *psubtype
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*psubtype* 
</dt> <dd>

指定子類型之 **GUID** 的指標。

</dd> </dl>

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

 

 




