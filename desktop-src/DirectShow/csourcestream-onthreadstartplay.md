---
description: 在 CSourceStream：:D oBufferProcessingLoop 方法的開頭呼叫 OnThreadStartPlay 方法。
ms.assetid: 16d3b28f-bfae-49af-b8e4-8cc8cb15ecab
title: 'CSourceStream. OnThreadStartPlay 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadStartPlay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fcd1ccf4b507570e0219854d1f5044c1d95db63d04b8f9049449beb3941e95d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073172"
---
# <a name="csourcestreamonthreadstartplay-method"></a>CSourceStream. OnThreadStartPlay 方法

`OnThreadStartPlay`方法是在 [**CSourceStream：:D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md)方法的開頭呼叫。

## <a name="syntax"></a>語法


```C++
virtual HRESULT OnThreadStartPlay();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法不會在基類中執行任何動作;它可供衍生類別覆寫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 




