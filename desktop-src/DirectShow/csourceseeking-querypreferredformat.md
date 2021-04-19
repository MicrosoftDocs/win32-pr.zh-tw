---
description: QueryPreferredFormat 方法會抓取物件的慣用時間格式。 這個方法會實 IMediaSeeking：： QueryPreferredFormat 方法。
ms.assetid: 3b73b7cf-1ba7-47c5-8442-5f138b74f335
title: 'CSourceSeeking. QueryPreferredFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8916e23756279dd30eaf177ef839944a4c68d61a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993359"
---
# <a name="csourceseekingquerypreferredformat-method"></a>CSourceSeeking. QueryPreferredFormat 方法

方法會抓取 `QueryPreferredFormat` 物件的慣用時間格式。 這個方法會實 [**IMediaSeeking：： QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) 方法。

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

接收時間格式 GUID 之變數的指標。 請參閱 [**時間格式 guid**](time-format-guids.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所列的其中一個 **HRESULT** 值。



| 傳回碼                                                                               | Description                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | Success<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl> | **Null** 指標值<br/> |



 

## <a name="remarks"></a>備註

基類所支援的唯一時間格式是時間 \_ 格式 \_ 媒體 \_ 時間 (100-毫微秒單位) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




