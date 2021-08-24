---
description: NewSegment 方法會將新的區段傳遞給輸入圖釘。
ms.assetid: 53189729-9f47-425e-9df6-faea01dd4482
title: 'COutputQueue. NewSegment 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4057cafa3962c85fbca9342debbf7bb0e92355fc083e693889df298e53509259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768138"
---
# <a name="coutputqueuenewsegment-method"></a>COutputQueue. NewSegment 方法

方法會將 `NewSegment` 新的區段傳遞給輸入圖釘。

## <a name="syntax"></a>語法


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*tStart* 
</dt> <dd>

區段的開始媒體位置，以 100-毫微秒單位表示。

</dd> <dt>

*tStop* 
</dt> <dd>

區段的結束媒體位置，以 100-毫微秒單位表示。

</dd> <dt>

*dRate* 
</dt> <dd>

此區段的處理速率（以原始費率的百分比表示）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

如果物件使用執行緒，則會依序將下列專案排入佇列：

-   新的 \_ 區段控制訊息。
-   區段資料。

新的 \_ 區段訊息會通知執行緒，佇列中的下一個專案將包含區段資料。 區段資料會組合在結構中，如下所示：


```C++
struct NewSegmentPacket {
    REFERENCE_TIME tStart;
    REFERENCE_TIME tStop;
    double dRate;
}; 
```



執行緒會使用結構中指定的資料，在輸入釘選上呼叫 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) 方法。

如果物件未使用執行緒，則會呼叫 [**COutputQueue：： SendAnyway**](coutputqueue-sendanyway.md) 方法來傳遞任何暫止的範例。 然後，它會在輸入 pin 上呼叫 **IPin：： NewSegment** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




