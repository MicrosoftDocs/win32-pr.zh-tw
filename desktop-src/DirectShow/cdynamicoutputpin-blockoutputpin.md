---
description: BlockOutputPin 方法會封鎖釘選。
ms.assetid: 49f6b8da-a8b2-482d-b70d-2c68a1b45a10
title: 'CDynamicOutputPin. BlockOutputPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.BlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3998774550363b7d22e05ca491f1d76ba7f2ff2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999400"
---
# <a name="cdynamicoutputpinblockoutputpin-method"></a>CDynamicOutputPin. BlockOutputPin 方法

`BlockOutputPin`方法會封鎖釘選。 當 pin 遭到封鎖時， [**CDynamicOutputPin：： StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) 方法會等候 pin 變成解除封鎖。 封鎖狀態可防止輸出圖釘傳遞範例、變更其輸出格式，或自行重新連接。

## <a name="syntax"></a>語法


```C++
void BlockOutputPin();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在呼叫這個方法之前，請先保留 [**CDynamicOutputPin：： m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) 重要區段。 如果串流執行緒正在使用 pin，以傳遞資料或變更連接，請勿呼叫這個方法。 若要檢查串流執行緒是否正在使用 pin，請呼叫 [**CDynamicOutputPin：： StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




