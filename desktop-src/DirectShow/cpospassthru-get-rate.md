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
ms.openlocfilehash: 4fa8014d23bc488b4f0b8b0cc9b872dfdf4a56cced396cc22eefab5912df1706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073532"
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

 

 




