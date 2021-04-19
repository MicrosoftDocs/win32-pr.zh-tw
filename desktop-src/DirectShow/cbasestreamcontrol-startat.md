---
description: StartAt 方法會在開始傳遞資料時通知 pin。 這個方法會實 IAMStreamControl：： StartAt 方法。
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: 'CBaseStreamControl. StartAt 方法 (Strmctl .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StartAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7adcf7cbd435992333bb8ae59d5ab1674056223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993937"
---
# <a name="cbasestreamcontrolstartat-method"></a>CBaseStreamControl. StartAt 方法

`StartAt`方法會在開始傳遞資料時通知 pin。 這個方法會實 [**IAMStreamControl：： StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT StartAt(
   const REFERENCE_TIME *ptStart = NULL,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ptStart* 
</dt> <dd>

[**參考 \_ 時間**](reference-time.md)值的指標，此值會指定 pin 應開始傳遞資料的時間。

</dd> <dt>

*dwCookie* 
</dt> <dd>

指定要連同開始通知一起傳送的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Strmctl (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseStreamControl 類別**](cbasestreamcontrol.md)
</dt> </dl>

 

 




