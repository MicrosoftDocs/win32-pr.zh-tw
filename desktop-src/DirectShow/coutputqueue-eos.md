---
description: EOS 方法會將結束資料流程呼叫傳遞給輸入的 pin。
ms.assetid: 65e8db14-6ca8-4c4f-8bd8-2442f743499e
title: 'COutputQueue 的 Outputq 方法 (. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab05d4ab3f2620c11bd62d566be851e16b28cecd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998650"
---
# <a name="coutputqueueeos-method"></a>COutputQueue. EOS 方法

方法會將 `EOS` 結束資料流程呼叫傳遞給輸入的 pin。

## <a name="syntax"></a>語法


```C++
void EOS();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果物件使用執行緒，則會將 EOS \_ 封包控制訊息排在佇列中。 執行緒會傳遞任何暫止的範例，並在輸入的 pin 上呼叫 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 方法。

如果物件未使用執行緒，則會呼叫 [**COutputQueue：： SendAnyway**](coutputqueue-sendanyway.md) 方法來傳遞任何暫止的範例。 然後，它會在輸入 pin 上呼叫 **IPin：： EndOfStream** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




