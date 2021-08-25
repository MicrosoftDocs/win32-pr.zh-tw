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
ms.openlocfilehash: d91d49f2517a3d3b9efc50d70ace1b75562b50df8acda7c48826e7c088439928
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055088"
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

 

 




