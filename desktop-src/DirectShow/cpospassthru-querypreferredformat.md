---
description: QueryPreferredFormat 方法會抓取資料流程的慣用時間格式。 這個方法會實 IMediaSeeking：： QueryPreferredFormat 方法。
ms.assetid: 8637448f-6b53-4ec9-9671-43bc8b713668
title: 'CPosPassThru. QueryPreferredFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c22348a10e8b9e5f241e06252c025e2ec9593486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995751"
---
# <a name="cpospassthruquerypreferredformat-method"></a>CPosPassThru. QueryPreferredFormat 方法

方法會抓取 `QueryPreferredFormat` 資料流程的慣用時間格式。 這個方法會實 [**IMediaSeeking：： QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pformatetc 架構* 
</dt> <dd>

接收時間格式 GUID 之變數的指標。

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

 

 




