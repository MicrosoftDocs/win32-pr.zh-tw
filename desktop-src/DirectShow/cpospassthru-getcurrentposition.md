---
description: GetCurrentPosition 方法會抓取目前的位置，相對於資料流程的總持續時間。 這個方法會實 IMediaSeeking：： GetCurrentPosition 方法。
ms.assetid: 07020182-2199-4153-9bab-f30d112bc09f
title: 'CPosPassThru. GetCurrentPosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5cdbd93edf7630499f6585fbbf6e34a70bed68c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994754"
---
# <a name="cpospassthrugetcurrentposition-method"></a>CPosPassThru. GetCurrentPosition 方法

方法會抓取 `GetCurrentPosition` 目前的位置，相對於資料流程的總持續時間。 這個方法會實 [**IMediaSeeking：： GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCurrent* 
</dt> <dd>

變數的指標，此變數會接收目前的位置，以目前時間格式的單位為單位。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                               | Description                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 成功。<br/>                   |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl> | 不支援方法。<br/>   |
| <dl> <dt>**E \_ 指標**</dt> </dl> | **Null** 指標引數。<br/> |



 

## <a name="remarks"></a>備註

這個方法會呼叫 [**CPosPassThru：： GetMediaTime**](cpospassthru-getmediatime.md) 方法，以取得最新的位置。 如果 **GetMediaTime** 失敗，此方法會在連線的 pin 上呼叫 **IMediaSeeking：： GetCurrentPosition** 。

根據預設， **GetMediaTime** 方法會在基類中失敗。 如果您的篩選準則快取目前的位置，請覆寫 **GetMediaTime** 以傳回快取的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPosPassThru 類別**](cpospassthru.md)
</dt> </dl>

 

 




