---
description: SetRate 方法會設定播放速率。 這個方法會實 IMediaSeeking：： SetRate 方法。
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: 'CPosPassThru. SetRate 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ada5c8bc8d265b33e1d4b243bdfd0cf8bf03a7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977538"
---
# <a name="cpospassthrusetrate-method"></a>CPosPassThru. SetRate 方法

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

播放速率。 不得為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果 *dRate* 為零，則傳回 E INVALIDARG。 否則，會從連接的 pin 傳回 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPosPassThru 類別**](cpospassthru.md)
</dt> </dl>

 

 




