---
description: Stop 方法會通知串流執行緒停止。
ms.assetid: 79bc528a-cf53-43f3-aa17-c459063c99ab
title: CSourceStream (Source. h) 的 Stop 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ac5eb7d6b066920210d4f955084afa46ddc71d1c17820fe0300acc66b53bb8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073162"
---
# <a name="csourcestreamstop-method"></a>CSourceStream. Stop 方法

`Stop`方法會通知串流執行緒停止。

## <a name="syntax"></a>語法


```C++
HRESULT Stop();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 \_ [OK] 或 [E 未 \_ 預期]。

## <a name="remarks"></a>備註

[**CSourceStream：：非**](csourcestream-inactive.md)使用中的方法會呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 




