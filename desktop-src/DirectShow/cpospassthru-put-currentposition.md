---
description: Put \_ CurrentPosition 方法會設定目前的位置，相對於資料流程的總持續時間。 這個方法會實 IMediaPosition：:p 的 \_ CurrentPosition 方法。
ms.assetid: 22d7e9e4-47da-45b5-9be0-3c5128f90353
title: 'CPosPassThru.put_CurrentPosition 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85426636a34d0e197b36496d5a38a847c61b9501
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991020"
---
# <a name="cpospassthruput_currentposition-method"></a>CPosPassThru. put \_ CurrentPosition 方法

`put_CurrentPosition`方法會設定目前的位置，相對於資料流程的總持續時間。 這個方法會實 [**IMediaPosition：:p 的 \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT put_CurrentPosition(
   REFTIME llTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*llTime* 
</dt> <dd>

新位置（以秒為單位）。

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

 

 




