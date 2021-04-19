---
description: CreateMediaType 函式會配置新的 AM \_ 媒體 \_ 類型結構，包括格式區塊。
ms.assetid: 841a8c51-6027-49d6-b3d8-b5e21e3d5f13
title: 'CreateMediaType 函式 (Mtype) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03ea3eaee03ebf98ac22d702bde9a165fda21e51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999657"
---
# <a name="createmediatype-function"></a>CreateMediaType 函式

**CreateMediaType** 函式會配置新的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構，包括格式區塊。

## <a name="syntax"></a>語法


```C++
AM_MEDIA_TYPE* WINAPI CreateMediaType(
   AM_MEDIA_TYPE const *pSrc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.Psrc* 
</dt> <dd>

[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的指標。 方法會將此結構複製到新結構中。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回新的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構，如果發生錯誤則為 **Null** 。

## <a name="remarks"></a>備註

若要釋放此函數所配置的記憶體，請呼叫 [**DeleteMediaType**](deletemediatype.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**媒體類型函式**](media-type-functions.md)
</dt> </dl>

 

 




