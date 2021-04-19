---
description: Get \_ PrerollTime 方法會抓取在開始位置之前將排入佇列的資料量。 這個方法會實 IMediaPosition：： get \_ PrerollTime 方法。
ms.assetid: 37c12798-eb0d-4859-8b2e-52d6ae147863
title: 'CPosPassThru.get_PrerollTime 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55cb2cc37a18c9ea00b4eb7115590f472b8d467e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992578"
---
# <a name="cpospassthruget_prerolltime-method"></a>CPosPassThru. 取得 \_ PrerollTime 方法

`get_PrerollTime`方法會抓取在開始位置之前將排入佇列的資料量。 這個方法會實 [**IMediaPosition：： get \_ PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT get_PrerollTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pllTime* 
</dt> <dd>

變數的指標，此變數會接收預先計算的時間（以秒為單位）。

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

 

 




