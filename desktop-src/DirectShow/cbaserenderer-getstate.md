---
description: '>getstate 方法會 (執行中、已停止或已暫停的) 來抓取篩選的狀態。'
ms.assetid: 5d35824c-2509-499a-bbb1-1fb916b51808
title: 'CBaseRenderer. >getstate 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 451078a6167ff7ca89ad4153c416826af8ac6d05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997643"
---
# <a name="cbaserenderergetstate-method"></a><span data-ttu-id="849a4-103">CBaseRenderer. >getstate 方法</span><span class="sxs-lookup"><span data-stu-id="849a4-103">CBaseRenderer.GetState method</span></span>

<span data-ttu-id="849a4-104">`GetState`方法會 (執行中、已停止或已暫停) 來抓取篩選的狀態。</span><span class="sxs-lookup"><span data-stu-id="849a4-104">The `GetState` method retrieves the filters's state (running, stopped, or paused).</span></span>

## <a name="syntax"></a><span data-ttu-id="849a4-105">語法</span><span class="sxs-lookup"><span data-stu-id="849a4-105">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="849a4-106">參數</span><span class="sxs-lookup"><span data-stu-id="849a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="849a4-107">*dwMilliSecsTimeout*</span><span class="sxs-lookup"><span data-stu-id="849a4-107">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="849a4-108">逾時間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="849a4-108">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="849a4-109">*State*</span><span class="sxs-lookup"><span data-stu-id="849a4-109">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="849a4-110">變數的指標，此變數會接收 [**篩選準則 \_ 狀態**](/windows/win32/api/strmif/ne-strmif-filter_state) 列舉類型的成員，以指出篩選的狀態。</span><span class="sxs-lookup"><span data-stu-id="849a4-110">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the filter's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="849a4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="849a4-111">Return value</span></span>

<span data-ttu-id="849a4-112">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="849a4-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="849a4-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="849a4-113">Return code</span></span>                                                                                                | <span data-ttu-id="849a4-114">Description</span><span class="sxs-lookup"><span data-stu-id="849a4-114">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="849a4-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="849a4-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="849a4-116">成功。</span><span class="sxs-lookup"><span data-stu-id="849a4-116">Success.</span></span><br/>                                            |
| <dl> <span data-ttu-id="849a4-117"><dt>**VFW \_ S \_ 州 \_ 中繼**</dt></span><span class="sxs-lookup"><span data-stu-id="849a4-117"><dt>**VFW\_S\_STATE\_INTERMEDIATE**</dt></span></span> </dl> | <span data-ttu-id="849a4-118">篩選正在轉換成指定的狀態。</span><span class="sxs-lookup"><span data-stu-id="849a4-118">The filter is transitioning to the indicated state.</span></span><br/> |
| <dl> <span data-ttu-id="849a4-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="849a4-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="849a4-120">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="849a4-120">**NULL** pointer argument.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="849a4-121">備註</span><span class="sxs-lookup"><span data-stu-id="849a4-121">Remarks</span></span>

<span data-ttu-id="849a4-122">這個方法會覆寫 [**CBaseFilter：： >getstate**](cbasefilter-getstate.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="849a4-122">This method overrides the [**CBaseFilter::GetState**](cbasefilter-getstate.md) method.</span></span> <span data-ttu-id="849a4-123">當轉譯器暫停時，它不會完成狀態轉換，直到它收到要轉譯的樣本為止。</span><span class="sxs-lookup"><span data-stu-id="849a4-123">When the renderer is paused, it does not complete the state transition until it receives a sample to render.</span></span> <span data-ttu-id="849a4-124">如果超時時間在狀態轉換完成之前過期，則方法會傳回 VFW \_ S \_ 狀態 \_ 中繼。</span><span class="sxs-lookup"><span data-stu-id="849a4-124">If the time-out expires before the state transition is complete, the method returns VFW\_S\_STATE\_INTERMEDIATE.</span></span>

## <a name="requirements"></a><span data-ttu-id="849a4-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="849a4-125">Requirements</span></span>



| <span data-ttu-id="849a4-126">需求</span><span class="sxs-lookup"><span data-stu-id="849a4-126">Requirement</span></span> | <span data-ttu-id="849a4-127">值</span><span class="sxs-lookup"><span data-stu-id="849a4-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="849a4-128">標頭</span><span class="sxs-lookup"><span data-stu-id="849a4-128">Header</span></span><br/>  | <dl> <span data-ttu-id="849a4-129"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="849a4-129"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="849a4-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="849a4-130">Library</span></span><br/> | <dl> <span data-ttu-id="849a4-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="849a4-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="849a4-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="849a4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="849a4-133">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="849a4-133">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




