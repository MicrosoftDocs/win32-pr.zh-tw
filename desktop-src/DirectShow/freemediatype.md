---
description: FreeMediaType 函式會刪除 AM \_ 媒體類型結構中的格式區塊 \_ 。
ms.assetid: b7ec335e-518d-4aa6-8cde-8cb92184d0b0
title: 'FreeMediaType 函式 (Mtype) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f332ccc9a60473a9d814481b759221dc6468d5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984809"
---
# <a name="freemediatype-function"></a>FreeMediaType 函式

**FreeMediaType** 函式會刪除 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構中的格式區塊。

## <a name="syntax"></a>語法


```C++
void FreeMediaType(
   AM_MEDIA_TYPE &mt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mt* \[裁判\]
</dt> <dd>

[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

格式區塊會配置在堆積上。 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)的 **pbFormat** 成員指向格式區塊。 使用此函式只釋出格式區塊。 若要刪除配置的 **AM \_ 媒體 \_ 類型** 結構，請呼叫 [**DeleteMediaType**](deletemediatype.md)。

此函式定義于 [DirectShow 基底類別](directshow-base-classes.md) 庫中。 如果您不想要連結至基底類別庫，您可以使用下列程式碼：


```C++
// Release the format block for a media type.

void _FreeMediaType(AM_MEDIA_TYPE& mt)
{
    if (mt.cbFormat != 0)
    {
        CoTaskMemFree((PVOID)mt.pbFormat);
        mt.cbFormat = 0;
        mt.pbFormat = NULL;
    }
    if (mt.pUnk != NULL)
    {
        // pUnk should not be used.
        mt.pUnk->Release();
        mt.pUnk = NULL;
    }
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DeleteMediaType**](deletemediatype.md)
</dt> <dt>

[**媒體類型函式**](media-type-functions.md)
</dt> </dl>

 

 




