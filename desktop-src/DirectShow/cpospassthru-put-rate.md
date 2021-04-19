---
description: Put \_ rate 方法會設定播放速率。 這個方法會實 IMediaPosition：:p 的等比 \_ 特率方法。
ms.assetid: c077f344-de34-4f8a-8e08-6d7086a5a4f1
title: 'CPosPassThru.put_Rate 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21e7e654233f78adcda2addf73b87a178654872e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991517"
---
# <a name="cpospassthruput_rate-method"></a>CPosPassThru，put \_ Rate 方法

`put_Rate`方法會設定播放速率。 這個方法會實 [**IMediaPosition：:p 的 \_**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) 等位元速率方法。

## <a name="syntax"></a>語法


```C++
HRESULT put_Rate(
   double dRate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dRate* 
</dt> <dd>

播放速率。 不得為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果 *dRate* 為零，則傳回 E INVALIDARG。 否則，會從連接的 pin 傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

負比率表示反向播放。 並非所有媒體都支援反向播放。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPosPassThru 類別**](cpospassthru.md)
</dt> </dl>

 

 




