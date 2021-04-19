---
description: Run 方法會通知串流執行緒執行。
ms.assetid: 9aef7801-dcfb-4597-bccb-5ba19327b2d5
title: 'CSourceStream： Run 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39093654677ab4828f8a1d5a01a8cf7deaf42507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994856"
---
# <a name="csourcestreamrun-method"></a>CSourceStream 方法

`Run`方法會通知串流執行緒執行。

## <a name="syntax"></a>語法


```C++
HRESULT Run();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 \_ [OK] 或 [E 未 \_ 預期]。

## <a name="remarks"></a>備註

在基類中，此方法的效果與 [**CSourceStream：:P ause**](csourcestream-pause.md) 要求相同，且不會使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 




