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
# <a name="cbasestreamcontrolnotifyfilterstate-method"></a><span data-ttu-id="0a494-103">CBaseStreamControl. NotifyFilterState 方法</span><span class="sxs-lookup"><span data-stu-id="0a494-103">CBaseStreamControl.NotifyFilterState method</span></span>

<span data-ttu-id="0a494-104">`NotifyFilterState`當篩選準則的狀態變更時，方法會通知 pin。</span><span class="sxs-lookup"><span data-stu-id="0a494-104">The `NotifyFilterState` method notifies the pin when the filter's state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a494-105">語法</span><span class="sxs-lookup"><span data-stu-id="0a494-105">Syntax</span></span>


```C++
void NotifyFilterState(
   FILTER_STATE   new_state,
   REFERENCE_TIME tStart = 0
);
```



## <a name="parameters"></a><span data-ttu-id="0a494-106">參數</span><span class="sxs-lookup"><span data-stu-id="0a494-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a494-107">*新 \_ 狀態*</span><span class="sxs-lookup"><span data-stu-id="0a494-107">*new\_state*</span></span> 
</dt> <dd>

<span data-ttu-id="0a494-108">以 [**篩選 \_ 狀態**](/windows/win32/api/strmif/ne-strmif-filter_state) 列舉的成員來指定新的狀態。</span><span class="sxs-lookup"><span data-stu-id="0a494-108">Specifies the new state, as a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="0a494-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="0a494-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="0a494-110">指定開始時間。</span><span class="sxs-lookup"><span data-stu-id="0a494-110">Specifies the start time.</span></span> <span data-ttu-id="0a494-111">如果新的篩選準則狀態為 [正在執行] \_ ，請從 [**IMediaFilter：： Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) 方法傳入值。</span><span class="sxs-lookup"><span data-stu-id="0a494-111">If the new filter state is State\_Running, pass in the value from the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span> <span data-ttu-id="0a494-112">否則，請使用預設值。</span><span class="sxs-lookup"><span data-stu-id="0a494-112">Otherwise, use the default value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a494-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a494-113">Return value</span></span>

<span data-ttu-id="0a494-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0a494-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a494-115">備註</span><span class="sxs-lookup"><span data-stu-id="0a494-115">Remarks</span></span>

<span data-ttu-id="0a494-116">這個方法會導致 [**CBaseStreamControl：： CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) 方法停止等候。</span><span class="sxs-lookup"><span data-stu-id="0a494-116">This method causes the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method to stop waiting.</span></span> <span data-ttu-id="0a494-117">每當擁有篩選變更狀態時，呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="0a494-117">Call this method whenever the owning filter changes state.</span></span>

## <a name="examples"></a><span data-ttu-id="0a494-118">範例</span><span class="sxs-lookup"><span data-stu-id="0a494-118">Examples</span></span>


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



## <a name="requirements"></a><span data-ttu-id="0a494-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a494-119">Requirements</span></span>



| <span data-ttu-id="0a494-120">需求</span><span class="sxs-lookup"><span data-stu-id="0a494-120">Requirement</span></span> | <span data-ttu-id="0a494-121">值</span><span class="sxs-lookup"><span data-stu-id="0a494-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a494-122">標頭</span><span class="sxs-lookup"><span data-stu-id="0a494-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0a494-123"><dt>Strmctl (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0a494-123"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0a494-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="0a494-124">Library</span></span><br/> | <dl> <span data-ttu-id="0a494-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0a494-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a494-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a494-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a494-127">**CBaseStreamControl 類別**</span><span class="sxs-lookup"><span data-stu-id="0a494-127">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




