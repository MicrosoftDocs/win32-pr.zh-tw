---
description: CPosPassThru. ConvertTimeFormat 方法-ConvertTimeFormat 方法會將一段時間格式轉換成另一種格式。 這個方法會實 IMediaSeeking：： ConvertTimeFormat 方法。
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: 'CPosPassThru. ConvertTimeFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc463cb6dc891e677266289971a1dac8b335a8c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098956"
---
# <a name="cpospassthruconverttimeformat-method"></a>CPosPassThru. ConvertTimeFormat 方法

`ConvertTimeFormat`方法會從一種時間格式轉換成另一種格式。 這個方法會實 [**IMediaSeeking：： ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTarget* 
</dt> <dd>

接收轉換時間之變數的指標。

</dd> <dt>

*pTargetFormat* 
</dt> <dd>

目標格式之時間格式 GUID 的指標。 如果是 **Null**，則會使用目前的格式。

</dd> <dt>

*來源* 
</dt> <dd>

要轉換的時間值。

</dd> <dt>

*pSourceFormat* 
</dt> <dd>

要轉換之格式的時間格式 GUID 指標。 如果是 **Null**，則會使用目前的格式。

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

 

 




