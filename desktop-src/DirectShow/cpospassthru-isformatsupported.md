---
description: CPosPassThru. IsFormatSupported 方法-IsFormatSupported 方法會判斷是否支援指定的時間格式。 這個方法會實 IMediaSeeking：： IsFormatSupported 方法。
ms.assetid: dd8751d6-8439-4155-bdaf-b152a7c6cad4
title: 'CPosPassThru. IsFormatSupported 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d4ae6cee00879d9778380e76249ddc786f40be007081bb5aa8d78a4da2f4f58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084088"
---
# <a name="cpospassthruisformatsupported-method"></a>CPosPassThru. IsFormatSupported 方法

`IsFormatSupported`方法會判斷是否支援指定的時間格式。 這個方法會實 [**IMediaSeeking：： IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pformatetc 架構* 
</dt> <dd>

時間格式 GUID 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

從連接的 pin 傳回 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPosPassThru 類別**](cpospassthru.md)
</dt> <dt>

[**時間格式 Guid**](time-format-guids.md)
</dt> </dl>

 

 




