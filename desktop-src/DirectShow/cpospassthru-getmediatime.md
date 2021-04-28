---
description: CPosPassThru. GetMediaTime 方法-GetMediaTime 方法會抓取目前樣本上的時間戳記。
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: 'CPosPassThru. GetMediaTime 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 328a0ae09c80a687863cfedb994f5a80cebebf14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095256"
---
# <a name="cpospassthrugetmediatime-method"></a>CPosPassThru. GetMediaTime 方法

方法會抓取 `GetMediaTime` 目前樣本上的時間戳記。

## <a name="syntax"></a>語法


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStartTime* 
</dt> <dd>

接收開始時間之變數的指標，以目前時間格式的單位為單位。

</dd> <dt>

*pEndTime* 
</dt> <dd>

接收結束時間之變數的指標，以目前時間格式的單位為單位。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 E \_ 失敗。

## <a name="remarks"></a>備註

如果您的篩選準則會快取它所接收之範例的時間戳記，請覆寫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPosPassThru 類別**](cpospassthru.md)
</dt> </dl>

 

 




