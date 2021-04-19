---
description: 取得 \_ 持續時間方法會抓取資料流程的持續時間。 這個方法會實 IMediaPosition：： get \_ Duration 方法。
ms.assetid: 326a8cd3-d05f-49d0-941d-08f9778e9a06
title: 'CPosPassThru.get_Duration 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df518a0691a4fe1a6c0443ba93a83e65577efe21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987944"
---
# <a name="cpospassthruget_duration-method"></a>CPosPassThru. 取得 \_ Duration 方法

`get_Duration`方法會捕獲資料流程的持續時間。 這個方法會實 [**IMediaPosition：： get \_ Duration**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT get_Duration(
   REFTIME *plength
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*plength* 
</dt> <dd>

接收資料流程長度總計（以秒為單位）之變數的指標。

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

 

 




