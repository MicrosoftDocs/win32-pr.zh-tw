---
description: Exit 方法會通知串流執行緒結束。
ms.assetid: 1bb59848-e405-40f9-87ec-33de8754e2dd
title: CSourceStream， (Source. h) 的 Exit 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Exit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2c1c0de67eaa1067a4c72f3500674dddef65ddbb11af1b520973120d2df3c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687428"
---
# <a name="csourcestreamexit-method"></a>CSourceStream. Exit 方法

`Exit`方法會通知串流執行緒結束。

## <a name="syntax"></a>語法


```C++
HRESULT Exit();
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

 

 




