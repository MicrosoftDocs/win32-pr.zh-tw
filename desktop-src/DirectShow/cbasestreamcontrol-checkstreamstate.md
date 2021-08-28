---
description: CheckStreamState 方法會判斷是否應該傳遞或捨棄媒體範例。
ms.assetid: 1533f4b9-e13e-458b-9614-96d733cef4ed
title: 'CBaseStreamControl. CheckStreamState 方法 (Strmctl .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CheckStreamState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59c74f6933929b54be7e4933220358105f2dbe6d7be5f74db13be7c3092ffe17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537378"
---
# <a name="cbasestreamcontrolcheckstreamstate-method"></a>CBaseStreamControl. CheckStreamState 方法

`CheckStreamState`方法會判斷是否應該傳遞或捨棄媒體範例。

## <a name="syntax"></a>語法


```C++
enum CheckStreamState(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSample* 
</dt> <dd>

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個值。



| 傳回碼                                                                                       | 描述                     |
|---------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**資料流程 \_ 捨棄**</dt> </dl> | 捨棄此範例。<br/> |
| <dl> <dt>**串流 \_ 流動**</dt> </dl>    | 傳遞此範例。<br/> |



 

## <a name="remarks"></a>備註

當您的 pin 收到範例時，請呼叫這個方法。 只有在傳回值為數據流流動時，才傳遞範例 \_ 。 如果傳回值為數據流 \_ 捨棄，請捨棄範例。

如果 pin 捨棄任何範例，則會呼叫 [**IMediaSample：： SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) 方法，將它所提供的下一個範例標示為不連續。

如果您的篩選準則會執行 [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) 介面，以計算所捨棄的畫面格數目，請勿將捨棄的框架計算為已卸載的框架。

當傳回值為數據流 \_ 捨棄時，方法會封鎖，直到參考時間到達樣本的開始時間。 這可防止您的 pin 太快捨棄樣本。 如果已暫停篩選，則等候時間是無限的，直到篩選執行、停止或清除資料為止。  (篩選狀態變更和串流處理會在個別的執行緒上執行，因此不會造成任何鎖死。 ) 

**CBaseStreamControl：： StreamControlState** 列舉的定義如下：


```C++
enum StreamControlState{ 
    STREAM_FLOWING = 0x1000,
    STREAM_DISCARDING
};
```



## <a name="examples"></a>範例

下列範例假設 pin 使用名為 m fLastSampleDiscarded 的成員變數 \_ 來追蹤不連續。


```C++
CMyPin::Receive(IMediaSample *pSample)
{
    if (!pSample) return E_POINTER;

    int iStreamState = CheckStreamState(pSample);
    if (iStreamState == STREAM_FLOWING) 
    {
        if (m_fLastSampleDiscarded)
            pSample->SetDiscontinuity(TRUE);
        m_fLastSampleDiscarded = FALSE;
        /* Deliver the sample. */
    } 
    else 
    {
        m_fLastSampleDiscarded = TRUE;  
       // Discard this sample. Do not deliver it.
    }
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Strmctl (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseStreamControl 類別**](cbasestreamcontrol.md)
</dt> </dl>

 

 




