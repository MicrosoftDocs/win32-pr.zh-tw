---
description: MatchesPartial 方法會判斷此媒體類型是否符合部分指定的媒體類型。
ms.assetid: 62d531f3-5aa2-4af2-b951-584a49a849fc
title: 'CMediaType. MatchesPartial 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.MatchesPartial
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4d2d4232b64857ca209e6b43cd7081a42495fee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994794"
---
# <a name="cmediatypematchespartial-method"></a>CMediaType. MatchesPartial 方法

`MatchesPartial`方法會判斷此媒體類型是否符合部分指定的媒體類型。

## <a name="syntax"></a>語法


```C++
BOOL MatchesPartial(
   const CMediaType *ppartial
) const;
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppartial* 
</dt> <dd>

要比對之媒體類型的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果媒體類型相符，則傳回 **TRUE** 。 否則，會傳回 **FALSE**。

## <a name="remarks"></a>備註

*Ppartial* 指定的媒體類型可以有 \_ 主要類型、子類型或格式類型的 GUID Null 值。 任何具有 GUID \_ Null 值的成員都不會進行測試。  (生效，GUID \_ null 可作為萬用字元。具有 guid null 以外值的 ) 成員 \_ 必須符合，才能讓媒體類型相符。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 




