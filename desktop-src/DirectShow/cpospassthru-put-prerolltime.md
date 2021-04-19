---
description: Put \_ PrerollTime 方法會設定要在開始位置之前排入佇列的資料量。 這個方法會實 IMediaPosition：:p 的 \_ PrerollTime 方法。
ms.assetid: 5c35fb1d-2296-493f-8104-601127d7dd9f
title: 'CPosPassThru.put_PrerollTime 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bd4eddc7688373386147ea7999fdbd17f9af6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993412"
---
# <a name="cpospassthruput_prerolltime-method"></a>CPosPassThru. put \_ PrerollTime 方法

`put_PrerollTime`方法會設定要在開始位置之前排入佇列的資料量。 這個方法會實 [**IMediaPosition：:p 的 \_ PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT put_PrerollTime(
   REFTIME llTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*llTime* 
</dt> <dd>

預先計算的時間（以秒為單位）。

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

 

 




