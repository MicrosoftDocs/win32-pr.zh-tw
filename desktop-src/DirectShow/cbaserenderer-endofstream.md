---
description: EndOfStream 方法會通知篩選輸入 pin 收到的資料流程結束通知。
ms.assetid: bdfd03f9-81e0-4d52-959e-82fd1a67e1c3
title: 'CBaseRenderer. EndOfStream 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e12da02ffbce99b29d324c1166b3d4cdf2265c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983081"
---
# <a name="cbaserendererendofstream-method"></a>CBaseRenderer. EndOfStream 方法

`EndOfStream`方法會通知篩選輸入 pin 收到的資料流程結束通知。

## <a name="syntax"></a>語法


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

篩選的輸入 pin 會在收到資料流程結束通知時呼叫這個方法。

這個方法會將 [**CBaseRenderer：： m \_ bEOS**](cbaserenderer-m-beos.md) 旗標設定為 **TRUE** ，並呼叫 [**CBaseRenderer：： SendEndOfStream**](cbaserenderer-sendendofstream.md) 方法來排定 [**EC \_ 完成**](ec-complete.md) 事件。 如果篩選已暫停且正在等候範例，這個方法會完成狀態轉換。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




