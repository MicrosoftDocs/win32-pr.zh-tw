---
description: Init 方法會初始化串流執行緒。
ms.assetid: c746e595-de97-478c-8b22-5c4dd5594a8f
title: 'CSourceStream.Init 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3abf2b4637385616862c0613f72afd676f5b79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998894"
---
# <a name="csourcestreaminit-method"></a>CSourceStream.Init 方法

`Init`方法會初始化串流執行緒。

## <a name="syntax"></a>語法


```C++
HRESULT Init();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK，或另一個 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法必須是傳送至 [**CSourceStream：： ThreadProc**](csourcestream-threadproc.md) 方法的第一個執行緒要求。 [**CSourceStream：： Active**](csourcestream-active.md)方法會呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 




