---
description: CopyMediaType 函式會將 AM \_ 媒體 \_ 類型結構複製到另一個結構，包括格式區塊
ms.assetid: 5b47e197-abb5-4b2c-ad65-a506c5e239be
title: 'CopyMediaType 函式 (Mtype) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CopyMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b193f64edb55a342546f26db1975080490f0e69b2caa91695b3bc63240750983
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634370"
---
# <a name="copymediatype-function"></a>CopyMediaType 函式

**CopyMediaType** 函式會將 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構複製到另一個結構，包括格式區塊

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI CopyMediaType(
         AM_MEDIA_TYPE *pmtTarget,
   const AM_MEDIA_TYPE *pmtSource
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pmtTarget* 
</dt> <dd>

[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的指標。 方法會將媒體類型複製到這個結構中。

</dd> <dt>

*pmtSource* 
</dt> <dd>

要複製之來源 [**\_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 \_ [確定] 或 [E \_ OUTOFMEMORY]。

## <a name="remarks"></a>備註

此函式會配置格式區塊的記憶體。 如果 *pmtTarget* 參數已經包含已配置的格式區塊，就會發生記憶體流失。 若要避免記憶體流失，請在呼叫此函式之前呼叫 [**FreeMediaType**](freemediatype.md) 。

在方法傳回之後，請在 *pmtTarget* 上呼叫 [**FreeMediaType**](freemediatype.md) ，以釋放格式區塊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**媒體類型函式**](media-type-functions.md)
</dt> </dl>

 

 




