---
description: '>getstate 方法會 (執行中、已停止或已暫停的) 來抓取篩選的狀態。 這個方法會實 IMediaFilter：： >getstate 方法。'
ms.assetid: e32e3a1d-857f-4db3-b52c-5b6b802ded42
title: 'CBaseFilter. >getstate 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c9470e5d71bf71f4e37e6eef84015becdf05f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987900"
---
# <a name="cbasefiltergetstate-method"></a><span data-ttu-id="51d8c-104">CBaseFilter. >getstate 方法</span><span class="sxs-lookup"><span data-stu-id="51d8c-104">CBaseFilter.GetState method</span></span>

<span data-ttu-id="51d8c-105">`GetState`方法會 (執行中、已停止或已暫停) 來抓取篩選的狀態。</span><span class="sxs-lookup"><span data-stu-id="51d8c-105">The `GetState` method retrieves the filters's state (running, stopped, or paused).</span></span> <span data-ttu-id="51d8c-106">這個方法會實 [**IMediaFilter：： >getstate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) 方法。</span><span class="sxs-lookup"><span data-stu-id="51d8c-106">This method implements the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="51d8c-107">語法</span><span class="sxs-lookup"><span data-stu-id="51d8c-107">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="51d8c-108">參數</span><span class="sxs-lookup"><span data-stu-id="51d8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51d8c-109">*dwMilliSecsTimeout*</span><span class="sxs-lookup"><span data-stu-id="51d8c-109">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="51d8c-110">逾時間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="51d8c-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="51d8c-111">*State*</span><span class="sxs-lookup"><span data-stu-id="51d8c-111">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="51d8c-112">變數的指標，此變數會接收 [**篩選準則 \_ 狀態**](/windows/win32/api/strmif/ne-strmif-filter_state) 列舉類型的成員，以指出篩選的狀態。</span><span class="sxs-lookup"><span data-stu-id="51d8c-112">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the filter's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51d8c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="51d8c-113">Return value</span></span>

<span data-ttu-id="51d8c-114">傳回 S \_ OK 或 E \_ 指標。</span><span class="sxs-lookup"><span data-stu-id="51d8c-114">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="51d8c-115">備註</span><span class="sxs-lookup"><span data-stu-id="51d8c-115">Remarks</span></span>

<span data-ttu-id="51d8c-116">在基類中，所有狀態轉換都是同步的，而 *dwMilliSecsTimeout* 參數則會被忽略。</span><span class="sxs-lookup"><span data-stu-id="51d8c-116">In the base class, all state transitions are synchronous and the *dwMilliSecsTimeout* parameter is ignored.</span></span> <span data-ttu-id="51d8c-117">如果衍生類別會執行非同步狀態轉換，它應該覆寫此方法以在狀態轉換期間等候，並在 *dwMilliSecsTimeout* 毫秒內等候。</span><span class="sxs-lookup"><span data-stu-id="51d8c-117">If a derived class performs asynchronous state transitions, it should override this method to wait during state transitions, with a time-out of *dwMilliSecsTimeout* milliseconds.</span></span>

<span data-ttu-id="51d8c-118">如果您的篩選準則不會在暫停時傳遞資料，請覆寫 `GetState` 方法，以傳回 VFW 時無法提示的值， \_ \_ \_ (請參閱 [傳遞範例](delivering-samples.md)) 。</span><span class="sxs-lookup"><span data-stu-id="51d8c-118">If your filter does not deliver data while paused, override the `GetState` method to return the value VFW\_S\_CANT\_CUE when the filter is paused (see [Delivering Samples](delivering-samples.md)).</span></span> <span data-ttu-id="51d8c-119">例如：</span><span class="sxs-lookup"><span data-stu-id="51d8c-119">For example:</span></span>


```C++
CMyFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
        return VFW_S_CANT_CUE;
    else
        return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="51d8c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="51d8c-120">Requirements</span></span>



| <span data-ttu-id="51d8c-121">需求</span><span class="sxs-lookup"><span data-stu-id="51d8c-121">Requirement</span></span> | <span data-ttu-id="51d8c-122">值</span><span class="sxs-lookup"><span data-stu-id="51d8c-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51d8c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="51d8c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="51d8c-124"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="51d8c-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="51d8c-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="51d8c-125">Library</span></span><br/> | <dl> <span data-ttu-id="51d8c-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="51d8c-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51d8c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51d8c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51d8c-128">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="51d8c-128">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




