---
description: IsEndOfStream 方法會查詢是否已收到資料流程結尾通知。
ms.assetid: 44f9b740-ff7d-4387-9c2c-a5b6b90f3295
title: 'CBaseRenderer. IsEndOfStream 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 50aab34fe73f617409ae3f1e33d132a45f8ea771722c42629d9f0e3df5ebb115
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872308"
---
# <a name="cbaserendererisendofstream-method"></a>CBaseRenderer. IsEndOfStream 方法

`IsEndOfStream`方法會查詢是否已收到資料流程結尾通知。

## <a name="syntax"></a>語法


```C++
BOOL IsEndOfStream();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**CBaseRenderer：： m \_ bEOS**](cbaserenderer-m-beos.md) 旗標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




