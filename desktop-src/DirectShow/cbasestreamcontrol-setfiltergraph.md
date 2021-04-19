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
# <a name="cbasestreamcontrolsetfiltergraph-method"></a><span data-ttu-id="3a063-103">CBaseStreamControl. SetFilterGraph 方法</span><span class="sxs-lookup"><span data-stu-id="3a063-103">CBaseStreamControl.SetFilterGraph method</span></span>

<span data-ttu-id="3a063-104">`SetFilterGraph`方法會指定資料流程控制事件的事件接收。</span><span class="sxs-lookup"><span data-stu-id="3a063-104">The `SetFilterGraph` method specifies the event sink for stream control events.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a063-105">語法</span><span class="sxs-lookup"><span data-stu-id="3a063-105">Syntax</span></span>


```C++
void SetFilterGraph(
   IMediaEventSink *pSink
);
```



## <a name="parameters"></a><span data-ttu-id="3a063-106">參數</span><span class="sxs-lookup"><span data-stu-id="3a063-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a063-107">*pSink*</span><span class="sxs-lookup"><span data-stu-id="3a063-107">*pSink*</span></span> 
</dt> <dd>

<span data-ttu-id="3a063-108">篩選圖形管理員 [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) 介面的指標，或在篩選離開篩選圖形時 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="3a063-108">Pointer to the Filter Graph Manager's [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface, or **NULL** when the filter leaves the filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a063-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a063-109">Return value</span></span>

<span data-ttu-id="3a063-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3a063-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a063-111">備註</span><span class="sxs-lookup"><span data-stu-id="3a063-111">Remarks</span></span>

<span data-ttu-id="3a063-112">從篩選的 [**IBaseFilter：： JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) 方法內部呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="3a063-112">Call this method from inside the filter's [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span> <span data-ttu-id="3a063-113">**CBaseStreamControl** 類別會使用 **IMediaEventSink** 介面來傳送 [**ec \_ 資料流程 \_ 控制項 \_**](ec-stream-control-started.md) ，以及使用 [**ec \_ stream \_ control \_ 已停止**](ec-stream-control-stopped.md)事件。</span><span class="sxs-lookup"><span data-stu-id="3a063-113">The **CBaseStreamControl** class uses the **IMediaEventSink** interface to send [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) events.</span></span>

<span data-ttu-id="3a063-114">如果您的篩選衍生自 **CBaseFilter**，請先呼叫 [**CBaseFilter：： JoinFilterGraph**](cbasefilter-joinfiltergraph.md) 方法，它會設定 [**CBaseFilter：： m \_ pSink**](cbasefilter-m-psink.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="3a063-114">If your filter derives from **CBaseFilter**, first call the [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) method, which sets the [**CBaseFilter::m\_pSink**](cbasefilter-m-psink.md) member variable.</span></span> <span data-ttu-id="3a063-115">然後將 **m \_ pSink** 傳遞給 `SetFilterGraph` 方法。</span><span class="sxs-lookup"><span data-stu-id="3a063-115">Then pass **m\_pSink** to the `SetFilterGraph` method.</span></span> <span data-ttu-id="3a063-116">請注意，當篩選離開圖形時， **m \_ PSink** 為 **Null** ，這是正確的。</span><span class="sxs-lookup"><span data-stu-id="3a063-116">Note that **m\_pSink** is **NULL** when the filter leaves the graph, which is correct.</span></span>

## <a name="examples"></a><span data-ttu-id="3a063-117">範例</span><span class="sxs-lookup"><span data-stu-id="3a063-117">Examples</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3a063-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a063-118">Requirements</span></span>



| <span data-ttu-id="3a063-119">需求</span><span class="sxs-lookup"><span data-stu-id="3a063-119">Requirement</span></span> | <span data-ttu-id="3a063-120">值</span><span class="sxs-lookup"><span data-stu-id="3a063-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a063-121">標頭</span><span class="sxs-lookup"><span data-stu-id="3a063-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3a063-122"><dt>Strmctl (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3a063-122"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3a063-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="3a063-123">Library</span></span><br/> | <dl> <span data-ttu-id="3a063-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3a063-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a063-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a063-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a063-126">**CBaseStreamControl 類別**</span><span class="sxs-lookup"><span data-stu-id="3a063-126">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




