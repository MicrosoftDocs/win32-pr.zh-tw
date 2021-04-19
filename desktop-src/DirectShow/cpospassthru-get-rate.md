---
description: 取得 \_ 速率方法會抓取播放速率。 這個方法會實 IMediaPosition：： get \_ 速率方法。
ms.assetid: 216cbcef-4874-4565-abb0-8c8bf67fe23c
title: 'CPosPassThru.get_Rate 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 46e565f51d7c549f524f9e478b2a8326daf690a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998808"
---
# <a name="cpospassthruget_rate-method"></a>CPosPassThru. 取得 \_ 率方法

`get_Rate`方法會捕獲播放速率。 這個方法會實 [**IMediaPosition：： get \_ 速率**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT get_Rate(
   double *pdRate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdRate* 
</dt> <dd>

接收播放速率之變數的指標。

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

 

 




