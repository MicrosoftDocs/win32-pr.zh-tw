---
description: 設定 pin 的媒體類型時，會呼叫 SetMediaType 方法。
ms.assetid: 91d88523-006e-49fe-92f3-92825fbb323b
title: 'CBaseRenderer. SetMediaType 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d1ba935fc5476becaf5edd4001efe8e604a97fc5e3a3ee8e965b606568d01863
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043738"
---
# <a name="cbaserenderersetmediatype-method"></a>CBaseRenderer. SetMediaType 方法

`SetMediaType`當釘選的媒體類型設定時，就會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pmt* 
</dt> <dd>

指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

輸入 pin 會從它自己的 [**CRendererInputPin：： SetMediaType**](crendererinputpin-setmediatype.md) 方法呼叫這個方法。 這個方法不會在基類中執行任何動作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




