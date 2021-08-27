---
description: CPosPassThru. GetAvailable 方法-GetAvailable 方法會捕獲搜尋效率的範圍。 這個方法會實 IMediaSeeking：： GetAvailable 方法。
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: 'CPosPassThru. GetAvailable 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1db45b20264f192b2ade7d8863f9da86d5fc02159567611eff86e9cdfff1b10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084248"
---
# <a name="cpospassthrugetavailable-method"></a>CPosPassThru. GetAvailable 方法

`GetAvailable`方法會捕獲搜尋效率的範圍。 這個方法會實 [**IMediaSeeking：： GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pEarliest* 
</dt> <dd>

變數的指標，此變數會接收有效率搜尋的最早時間。

</dd> <dt>

*pLatest* 
</dt> <dd>

變數的指標，此變數會接收有效率搜尋的最新時間。

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

 

 




