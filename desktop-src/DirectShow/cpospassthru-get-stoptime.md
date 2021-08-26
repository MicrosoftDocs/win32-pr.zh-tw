---
description: Get \_ StopTime 方法會捕獲播放將停止的時間，相對於資料流程的持續時間。 這個方法會實 IMediaPosition：： get \_ StopTime 方法。
ms.assetid: 0ca3f047-ac43-419e-a1ed-b406f89f7af7
title: 'CPosPassThru.get_StopTime 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea233d7e3a148088edd0f6963f45aeb0b483b41317481a95733fdc73c242027d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108298"
---
# <a name="cpospassthruget_stoptime-method"></a>CPosPassThru. 取得 \_ StopTime 方法

`get_StopTime`方法會抓取播放將停止的時間，相對於資料流程的持續時間。 這個方法會實 [**IMediaPosition：： get \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT get_StopTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pllTime* 
</dt> <dd>

接收停止時間之變數的指標（以秒為單位）。

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
</dt> </dl>

 

 




