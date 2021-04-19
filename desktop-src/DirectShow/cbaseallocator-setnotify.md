---
description: SetNotify 方法會設定或移除配置器上的回呼。 配置器會在呼叫配置器的 IMemAllocator：： ReleaseBuffer 方法時呼叫回呼方法。
ms.assetid: ef9a6c66-d392-4130-b4fc-9eb6aecb6cbf
title: 'CBaseAllocator. SetNotify 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8269112325d470cae59cff6e615f04fbdfab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978466"
---
# <a name="cbaseallocatorsetnotify-method"></a><span data-ttu-id="002ab-104">CBaseAllocator. SetNotify 方法</span><span class="sxs-lookup"><span data-stu-id="002ab-104">CBaseAllocator.SetNotify method</span></span>

<span data-ttu-id="002ab-105">\[[**SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) 可能會在後續版本中變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="002ab-105">\[[**SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="002ab-106">方法會在配置器 `SetNotify` 上設定或移除回呼。</span><span class="sxs-lookup"><span data-stu-id="002ab-106">The `SetNotify` method sets or removes a callback on the allocator.</span></span> <span data-ttu-id="002ab-107">配置器會在呼叫配置器的 [**IMemAllocator：： ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) 方法時呼叫回呼方法。</span><span class="sxs-lookup"><span data-stu-id="002ab-107">The allocator calls the callback method whenever the allocator's [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="002ab-108">語法</span><span class="sxs-lookup"><span data-stu-id="002ab-108">Syntax</span></span>


```C++
HRESULT SetNotify(
   IMemAllocatorNotifyCallbackTemp *pNotify
);
```



## <a name="parameters"></a><span data-ttu-id="002ab-109">參數</span><span class="sxs-lookup"><span data-stu-id="002ab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="002ab-110">*pNotify*</span><span class="sxs-lookup"><span data-stu-id="002ab-110">*pNotify*</span></span> 
</dt> <dd>

<span data-ttu-id="002ab-111">將用於回呼的 [**IMemAllocatorNotifyCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="002ab-111">Pointer to the [**IMemAllocatorNotifyCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) interface that will be used for the callback.</span></span> <span data-ttu-id="002ab-112">呼叫端必須執行介面。</span><span class="sxs-lookup"><span data-stu-id="002ab-112">The caller must implement the interface.</span></span> <span data-ttu-id="002ab-113">使用 **Null** 值以移除回呼。</span><span class="sxs-lookup"><span data-stu-id="002ab-113">Use the value **NULL** to remove the callback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="002ab-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="002ab-114">Return value</span></span>

<span data-ttu-id="002ab-115">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="002ab-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="002ab-116">備註</span><span class="sxs-lookup"><span data-stu-id="002ab-116">Remarks</span></span>

<span data-ttu-id="002ab-117">這個方法會實 [**IMemAllocatorCallbackTemp：： SetNotify**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) 方法。</span><span class="sxs-lookup"><span data-stu-id="002ab-117">This method implements the [**IMemAllocatorCallbackTemp::SetNotify**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) method.</span></span> <span data-ttu-id="002ab-118">配置器不會公開 [**IMemAllocatorCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp)介面，除非 [**CBaseAllocator**](cbaseallocator.md)函式中的 *FEnableReleaseCallback* 旗標設為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="002ab-118">The allocator does not expose the [**IMemAllocatorCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) interface unless the *fEnableReleaseCallback* flag is set to **TRUE** in the [**CBaseAllocator**](cbaseallocator.md) constructor.</span></span>

<span data-ttu-id="002ab-119">這個方法會設定等於 *pNotify* 的 [**CBaseAllocator：： m \_ pNotify**](cbaseallocator-m-pnotify.md)成員變數，並遞增介面上的參考計數。</span><span class="sxs-lookup"><span data-stu-id="002ab-119">This method sets the [**CBaseAllocator::m\_pNotify**](cbaseallocator-m-pnotify.md) member variable equal to *pNotify* and increments the reference count on the interface.</span></span> <span data-ttu-id="002ab-120">如果 *m \_ pNotify* 為非 **Null**，配置器的 **ReleaseBuffer** 方法會呼叫 [**IMemAllocatorNotifyCallbackTemp：： NotifyRelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease)。</span><span class="sxs-lookup"><span data-stu-id="002ab-120">If *m\_pNotify* is non-**NULL**, the allocator's **ReleaseBuffer** method calls [**IMemAllocatorNotifyCallbackTemp::NotifyRelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease).</span></span> <span data-ttu-id="002ab-121">請參閱該方法中的「備註」一節，以取得執行回呼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="002ab-121">See the Remarks section in that method for information about implementing the callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="002ab-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="002ab-122">Requirements</span></span>



| <span data-ttu-id="002ab-123">需求</span><span class="sxs-lookup"><span data-stu-id="002ab-123">Requirement</span></span> | <span data-ttu-id="002ab-124">值</span><span class="sxs-lookup"><span data-stu-id="002ab-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="002ab-125">標頭</span><span class="sxs-lookup"><span data-stu-id="002ab-125">Header</span></span><br/>  | <dl> <span data-ttu-id="002ab-126"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="002ab-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="002ab-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="002ab-127">Library</span></span><br/> | <dl> <span data-ttu-id="002ab-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="002ab-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="002ab-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="002ab-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="002ab-130">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="002ab-130">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




