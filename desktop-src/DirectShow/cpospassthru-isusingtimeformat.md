---
description: IsUsingTimeFormat 方法會判斷指定的時間格式是否為目前使用中的格式。 這個方法會實 IMediaSeeking：： IsUsingTimeFormat 方法。
ms.assetid: e377bcf0-0518-42b2-8975-e4c345e3fed4
title: 'CPosPassThru. IsUsingTimeFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64c240a0b1c269dde57e07e50bcbdbbd4d5d7e03d24a4e6d263662947f3d65de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954007"
---
# <a name="cpospassthruisusingtimeformat-method"></a>CPosPassThru. IsUsingTimeFormat 方法

`IsUsingTimeFormat`方法會判斷指定的時間格式是否為目前使用中的格式。 這個方法會實 [**IMediaSeeking：： IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT IsUsingTimeFormat(
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

 

 




