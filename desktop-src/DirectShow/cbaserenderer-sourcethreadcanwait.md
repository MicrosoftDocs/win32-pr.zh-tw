---
description: SourceThreadCanWait 方法會保存或釋放串流執行緒。
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: 'CBaseRenderer. SourceThreadCanWait 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SourceThreadCanWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f01be304ec2b5f845ea61c9609808c6e2f39fca9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001203"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a>CBaseRenderer. SourceThreadCanWait 方法

`SourceThreadCanWait`方法會保存或釋放串流執行緒。

## <a name="syntax"></a>語法


```C++
virtual HRESULT SourceThreadCanWait(
   BOOL bCanWait
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bCanWait* 
</dt> <dd>

指出是否要保存串流執行緒的布林值。 若 **為 TRUE**，則會在篩選等候轉譯下一個範例時封鎖串流執行緒。 如果 **為 FALSE**，則會釋放串流處理執行緒。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

`SourceThreadCanWait`使用值 **FALSE** 來呼叫方法，會強制篩選從封鎖的 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)呼叫傳回。 當篩選準則正在執行時，它會封鎖 **接收** 呼叫，直到目前樣本的呈現時間為止。 當篩選暫停時，它會無限期地封鎖 **接收** 呼叫。 此行為會控制資料流程中的資料流程。 不過，當篩選準則停止或清除時，不應封鎖。

封鎖是由 [**CBaseRenderer：： WaitForRenderTime**](cbaserenderer-waitforrendertime.md) 方法所控制，它會等候兩個事件： [**CBaseRenderer：： m \_ RenderEvent**](cbaserenderer-m-renderevent.md) 和 [**CBaseRenderer：： m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md)。 當呈現時間到達時， **m \_ RenderEvent** 事件就會收到信號。 以 FALSE 值呼叫時，會發出 **m \_ ThreadSignal** 事件的信號 `SourceThreadCanWait` 。  `SourceThreadCanWait`使用值 **TRUE** 來呼叫會重設事件。

[**CBaseRenderer：： Stop**](cbaserenderer-stop.md)和 [**CBaseRenderer：： BeginFlush**](cbaserenderer-beginflush.md)方法呼叫 `SourceThreadCanWait` 值 **為 FALSE** (釋放串流執行緒) 。 [**CBaseRenderer：:P ause**](cbaserenderer-pause.md)、 [**CBaseRenderer：： Run**](cbaserenderer-run.md)和 [**CBaseRenderer：： EndFlush**](cbaserenderer-endflush.md)方法會 `SourceThreadCanWait` 使用值 **TRUE** 來呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




