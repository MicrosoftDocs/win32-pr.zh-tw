---
description: SetFilterGraph 方法會指定資料流程控制事件的事件接收。
ms.assetid: a4c3dca6-6c80-4eca-87d6-875e746e9ed3
title: 'CBaseStreamControl. SetFilterGraph 方法 (Strmctl .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1cf8b571ee5d017acd056e00a06af54cd90b943a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986146"
---
# <a name="cbasestreamcontrolsetfiltergraph-method"></a>CBaseStreamControl. SetFilterGraph 方法

`SetFilterGraph`方法會指定資料流程控制事件的事件接收。

## <a name="syntax"></a>語法


```C++
void SetFilterGraph(
   IMediaEventSink *pSink
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSink* 
</dt> <dd>

篩選圖形管理員 [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) 介面的指標，或在篩選離開篩選圖形時 **為 Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

從篩選的 [**IBaseFilter：： JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) 方法內部呼叫這個方法。 **CBaseStreamControl** 類別會使用 **IMediaEventSink** 介面來傳送 [**ec \_ 資料流程 \_ 控制項 \_**](ec-stream-control-started.md) ，以及使用 [**ec \_ stream \_ control \_ 已停止**](ec-stream-control-stopped.md)事件。

如果您的篩選衍生自 **CBaseFilter**，請先呼叫 [**CBaseFilter：： JoinFilterGraph**](cbasefilter-joinfiltergraph.md) 方法，它會設定 [**CBaseFilter：： m \_ pSink**](cbasefilter-m-psink.md) 成員變數。 然後將 **m \_ pSink** 傳遞給 `SetFilterGraph` 方法。 請注意，當篩選離開圖形時， **m \_ PSink** 為 **Null** ，這是正確的。

## <a name="examples"></a>範例


```C++
STDMETHODIMP CMyFilter::JoinFilterGraph(IFilterGraph * pGraph, LPCWSTR pName)
{
    // Note: It's OK if pGraph is NULL.

    HRESULT hr = CBaseFilter::JoinFilterGraph(pGraph, pName);
    if (SUCCEEDED(hr)) 
    {
        m_pMyPin->SetFilterGraph(m_pSink);
    }
    return hr;
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

 

 




