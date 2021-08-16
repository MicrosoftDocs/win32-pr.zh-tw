---
description: CreateAudioMediaType 函式會從 WAVEFORMATEX 結構初始化媒體類型。
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: 'CreateAudioMediaType 函式 (Mtype) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateAudioMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2eb9dc01a398a498252cca2f1f3af012608f8e0ca80c62800c56e4026c0b0a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908818"
---
# <a name="createaudiomediatype-function"></a>CreateAudioMediaType 函式

**CreateAudioMediaType** 函式會從 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構初始化媒體類型。

## <a name="syntax"></a>語法


```C++
HRESULT STDAPI CreateAudioMediaType(
   const WAVEFORMATEX  *pwfx,
         AM_MEDIA_TYPE *pmt,
         BOOL          bSetFormat
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pwfx* 
</dt> <dd>

所提供 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構的指標。

</dd> <dt>

*Pmt* 
</dt> <dd>

要初始化的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構指標。

</dd> <dt>

*bSetFormat* 
</dt> <dd>

指出是否要初始化格式區塊的旗標。 指定 **TRUE** 表示將它初始化，否則為 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果無法配置記憶體給格式資料，則傳回 E \_ OUTOFMEMORY;\_否則為 [否]。

## <a name="remarks"></a>備註

如果 *bSetFormat* 參數為 **TRUE**，方法會配置格式區塊的記憶體。 如果 *pmt* 參數已經包含配置的格式區塊，就會發生記憶體流失。 若要避免記憶體流失，請在呼叫此函式之前呼叫 [**FreeMediaType**](freemediatype.md) 。 在方法傳回之後，再次呼叫 **FreeMediaType** ，以釋放格式區塊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**媒體類型函式**](media-type-functions.md)
</dt> </dl>

 

