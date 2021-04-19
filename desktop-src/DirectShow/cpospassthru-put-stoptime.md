---
description: Put \_ StopTime 方法會設定播放將停止的時間，相對於資料流程的持續時間。 這個方法會實 IMediaPosition：:p 的 \_ StopTime 方法。
ms.assetid: 0a344cad-df93-47f1-8c7f-5d5ef775b850
title: 'CPosPassThru.put_StopTime 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f5763700947596a0fb437ba3840df058d4d3239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999396"
---
# <a name="cpospassthruput_stoptime-method"></a>CPosPassThru. put \_ StopTime 方法

`put_StopTime`方法會設定播放將停止的時間（相對於資料流程的持續時間）。 這個方法會實 [**IMediaPosition：:p 的 \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT put_StopTime(
   REFTIME llTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*llTime* 
</dt> <dd>

以 **秒為單位的停止** 時間（以秒為單位）。

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

 

 




