---
description: 當篩選準則的狀態變更時，NotifyFilterState 方法會通知 pin。
ms.assetid: 0eb3b0e5-9c44-464e-b4ca-bcded731e813
title: 'CBaseStreamControl. NotifyFilterState 方法 (Strmctl .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.NotifyFilterState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ccb96361c8f4938bd95ffdc29229a035a239cc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997024"
---
# <a name="cbasestreamcontrolnotifyfilterstate-method"></a>CBaseStreamControl. NotifyFilterState 方法

`NotifyFilterState`當篩選準則的狀態變更時，方法會通知 pin。

## <a name="syntax"></a>語法


```C++
void NotifyFilterState(
   FILTER_STATE   new_state,
   REFERENCE_TIME tStart = 0
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*新 \_ 狀態* 
</dt> <dd>

以 [**篩選 \_ 狀態**](/windows/win32/api/strmif/ne-strmif-filter_state) 列舉的成員來指定新的狀態。

</dd> <dt>

*tStart* 
</dt> <dd>

指定開始時間。 如果新的篩選準則狀態為 [正在執行] \_ ，請從 [**IMediaFilter：： Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) 方法傳入值。 否則，請使用預設值。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會導致 [**CBaseStreamControl：： CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) 方法停止等候。 每當擁有篩選變更狀態時，呼叫這個方法。

## <a name="examples"></a>範例


```C++
STDMETHODIMP CMyFilter::Run(REFERENCE_TIME tStart)
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Running, tStart);
   return CBaseFilter::Run(tStart); // Call the filter base class.
}

STDMETHODIMP CMyFilter::Pause()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Paused);
   return CBaseFilter::Pause();
}

STDMETHODIMP CMyFilter::Stop()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Stopped);
   return CBaseFilter::Stop();
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

 

 




