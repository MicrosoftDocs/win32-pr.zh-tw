---
description: Run 方法會執行物件。 這個方法會實 IMediaFilter：： Run 方法。
ms.assetid: a59180df-46b4-4c23-973f-2931d95ace55
title: 'CBaseMediaFilter： Run 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c4023be7731f9bae60576bc7002010eb0b51823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995193"
---
# <a name="cbasemediafilterrun-method"></a><span data-ttu-id="9efd2-104">CBaseMediaFilter 方法</span><span class="sxs-lookup"><span data-stu-id="9efd2-104">CBaseMediaFilter.Run method</span></span>

<span data-ttu-id="9efd2-105">`Run`方法會執行物件。</span><span class="sxs-lookup"><span data-stu-id="9efd2-105">The `Run` method runs the object.</span></span> <span data-ttu-id="9efd2-106">這個方法會實 [**IMediaFilter：： Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) 方法。</span><span class="sxs-lookup"><span data-stu-id="9efd2-106">This method implements the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9efd2-107">語法</span><span class="sxs-lookup"><span data-stu-id="9efd2-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="9efd2-108">參數</span><span class="sxs-lookup"><span data-stu-id="9efd2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9efd2-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="9efd2-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="9efd2-110">對應于資料流程時間0的參考時間。</span><span class="sxs-lookup"><span data-stu-id="9efd2-110">Reference time corresponding to stream time 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9efd2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9efd2-111">Return value</span></span>

<span data-ttu-id="9efd2-112">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="9efd2-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9efd2-113">備註</span><span class="sxs-lookup"><span data-stu-id="9efd2-113">Remarks</span></span>

<span data-ttu-id="9efd2-114">如果物件已停止，這個方法會藉由呼叫 [**CBaseMediaFilter：:P ause**](cbasemediafilter-pause.md) 方法來暫停物件。</span><span class="sxs-lookup"><span data-stu-id="9efd2-114">If the object is stopped, this method pauses the object by calling the [**CBaseMediaFilter::Pause**](cbasemediafilter-pause.md) method.</span></span> <span data-ttu-id="9efd2-115">然後，它會將 [**CBaseMediaFilter：： m \_ state**](cbasemediafilter-m-state.md) 成員變數設定為正在執行狀態 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9efd2-115">It then sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Running.</span></span>

<span data-ttu-id="9efd2-116">資料流程時間的計算方式為目前的參考時間減去 *tStart*。</span><span class="sxs-lookup"><span data-stu-id="9efd2-116">Stream time is calculated as the current reference time minus *tStart*.</span></span> <span data-ttu-id="9efd2-117">時間戳記為零的媒體範例應該在時間 *tStart* 時轉譯。</span><span class="sxs-lookup"><span data-stu-id="9efd2-117">A media sample with a time stamp of zero should be rendered at time *tStart*.</span></span>

## <a name="requirements"></a><span data-ttu-id="9efd2-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="9efd2-118">Requirements</span></span>



| <span data-ttu-id="9efd2-119">需求</span><span class="sxs-lookup"><span data-stu-id="9efd2-119">Requirement</span></span> | <span data-ttu-id="9efd2-120">值</span><span class="sxs-lookup"><span data-stu-id="9efd2-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9efd2-121">標頭</span><span class="sxs-lookup"><span data-stu-id="9efd2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9efd2-122"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9efd2-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9efd2-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="9efd2-123">Library</span></span><br/> | <dl> <span data-ttu-id="9efd2-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9efd2-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9efd2-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9efd2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9efd2-126">**CBaseMediaFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="9efd2-126">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




