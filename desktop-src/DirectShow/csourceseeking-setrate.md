---
description: SetRate 方法會設定播放速率。 這個方法會實 IMediaSeeking：： SetRate 方法。
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: 'CSourceSeeking. SetRate 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 718a38f3eff9cc1647d09cf142db784f53e4c755
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994719"
---
# <a name="csourceseekingsetrate-method"></a>CSourceSeeking. SetRate 方法

`SetRate`方法會設定播放速率。 這個方法會實 [**IMediaSeeking：： SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dRate* 
</dt> <dd>

播放速率。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法會更新 [**CSourceSeeking：： m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) 成員變數的值，然後呼叫純虛擬方法 [**CSourceSeeking：： ChangeRate**](csourceseeking-changerate.md)。 方法不會驗證 *dRate* 參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




