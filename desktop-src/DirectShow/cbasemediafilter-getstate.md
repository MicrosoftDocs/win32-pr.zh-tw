---
description: '>getstate 方法會抓取物件的狀態 (執行中、已停止或已暫停) 。 這個方法會實 IMediaFilter：： >getstate 方法。'
ms.assetid: d4cc7e2b-5ea5-4165-842f-becc3a81cbce
title: 'CBaseMediaFilter. >getstate 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eeda91433e0e1474e936902da115e15c37e32e09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977432"
---
# <a name="cbasemediafiltergetstate-method"></a><span data-ttu-id="5bc18-104">CBaseMediaFilter. >getstate 方法</span><span class="sxs-lookup"><span data-stu-id="5bc18-104">CBaseMediaFilter.GetState method</span></span>

<span data-ttu-id="5bc18-105">方法會抓取 `GetState` 物件的狀態 (執行中、已停止或已暫停) 。</span><span class="sxs-lookup"><span data-stu-id="5bc18-105">The `GetState` method retrieves the object's state (running, stopped, or paused).</span></span> <span data-ttu-id="5bc18-106">這個方法會實 [**IMediaFilter：： >getstate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) 方法。</span><span class="sxs-lookup"><span data-stu-id="5bc18-106">This method implements the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc18-107">語法</span><span class="sxs-lookup"><span data-stu-id="5bc18-107">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="5bc18-108">參數</span><span class="sxs-lookup"><span data-stu-id="5bc18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bc18-109">*dwMilliSecsTimeout*</span><span class="sxs-lookup"><span data-stu-id="5bc18-109">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="5bc18-110">逾時間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5bc18-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="5bc18-111">*State*</span><span class="sxs-lookup"><span data-stu-id="5bc18-111">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="5bc18-112">變數的指標，此變數會接收 [**篩選準則 \_ 狀態**](/windows/win32/api/strmif/ne-strmif-filter_state) 列舉類型的成員，指出物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="5bc18-112">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the object's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bc18-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5bc18-113">Return value</span></span>

<span data-ttu-id="5bc18-114">傳回 S \_ OK 或 E \_ 指標。</span><span class="sxs-lookup"><span data-stu-id="5bc18-114">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bc18-115">備註</span><span class="sxs-lookup"><span data-stu-id="5bc18-115">Remarks</span></span>

<span data-ttu-id="5bc18-116">在基類中，所有狀態轉換都是同步的，而 *dwMilliSecsTimeout* 參數則會被忽略。</span><span class="sxs-lookup"><span data-stu-id="5bc18-116">In the base class, all state transitions are synchronous and the *dwMilliSecsTimeout* parameter is ignored.</span></span> <span data-ttu-id="5bc18-117">如果衍生類別會執行非同步狀態轉換，它應該覆寫此方法以在狀態轉換期間等候，並在 *dwMilliSecsTimeout* 毫秒內等候。</span><span class="sxs-lookup"><span data-stu-id="5bc18-117">If a derived class performs asynchronous state transitions, it should override this method to wait during state transitions, with a time-out of *dwMilliSecsTimeout* milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bc18-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5bc18-118">Requirements</span></span>



| <span data-ttu-id="5bc18-119">需求</span><span class="sxs-lookup"><span data-stu-id="5bc18-119">Requirement</span></span> | <span data-ttu-id="5bc18-120">值</span><span class="sxs-lookup"><span data-stu-id="5bc18-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc18-121">標頭</span><span class="sxs-lookup"><span data-stu-id="5bc18-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5bc18-122"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5bc18-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5bc18-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="5bc18-123">Library</span></span><br/> | <dl> <span data-ttu-id="5bc18-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5bc18-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bc18-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5bc18-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bc18-126">**CBaseMediaFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="5bc18-126">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




