---
description: 這個運算子會多載指派運算子來複製媒體類型。
ms.assetid: 5b94191d-b5e4-42b2-b0c5-8c2da2483c54
title: CMediaType. CMediaType：： operator = method (Mtype. h) -Mtype 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa577c8c8cfcdbcb0b62287a80cd998ab8775c6
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "106980257"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh"></a>CMediaType. CMediaType：： operator = method (Mtype .h) 

這個運算子會多載指派運算子來複製媒體類型。

## <a name="syntax"></a>語法


```C++
CMediaType& CMediaType::operator=(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mtype* \[裁判\]
</dt> <dd>

[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回物件的參考。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaType 類別**](cmediatype.md)
</dt> </dl>

 

 




