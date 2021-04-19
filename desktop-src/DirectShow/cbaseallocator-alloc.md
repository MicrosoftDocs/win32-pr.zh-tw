---
description: 配置方法會為緩衝區配置記憶體。
ms.assetid: a22c97ef-6a8d-4cad-b5a5-3e6b225f5c81
title: 'CBaseAllocator 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b7510a108e69eb218a894b67dd5b62d94bfdbe6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985731"
---
# <a name="cbaseallocatoralloc-method"></a><span data-ttu-id="a9357-103">CBaseAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="a9357-103">CBaseAllocator.Alloc method</span></span>

<span data-ttu-id="a9357-104">`Alloc`方法會為緩衝區配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="a9357-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9357-105">語法</span><span class="sxs-lookup"><span data-stu-id="a9357-105">Syntax</span></span>


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="a9357-106">參數</span><span class="sxs-lookup"><span data-stu-id="a9357-106">Parameters</span></span>

<span data-ttu-id="a9357-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a9357-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9357-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9357-108">Return value</span></span>

<span data-ttu-id="a9357-109">傳回下列其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="a9357-109">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="a9357-110">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a9357-110">Return code</span></span>                                                                                       | <span data-ttu-id="a9357-111">Description</span><span class="sxs-lookup"><span data-stu-id="a9357-111">Description</span></span>                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="a9357-112"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="a9357-112"><dt>**S\_FALSE**</dt></span></span> </dl>           | <span data-ttu-id="a9357-113">緩衝區需求未變更。</span><span class="sxs-lookup"><span data-stu-id="a9357-113">Buffer requirements have not changed.</span></span><br/> |
| <dl> <span data-ttu-id="a9357-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a9357-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="a9357-115">緩衝區需求已變更。</span><span class="sxs-lookup"><span data-stu-id="a9357-115">Buffer requirements have changed.</span></span><br/>     |
| <dl> <span data-ttu-id="a9357-116"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="a9357-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="a9357-117">未設定緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="a9357-117">Buffer requirements were not set.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="a9357-118">備註</span><span class="sxs-lookup"><span data-stu-id="a9357-118">Remarks</span></span>

<span data-ttu-id="a9357-119">[**CBaseAllocator：： Commit**](cbaseallocator-commit.md)方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="a9357-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span>

<span data-ttu-id="a9357-120">在基類中，此方法不會配置任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="a9357-120">In the base class, this method does not allocate any memory.</span></span> <span data-ttu-id="a9357-121">如果未設定緩衝區需求，則會傳回錯誤， \_ 如果需求沒有變更，則傳回 FALSE， \_ 如果需求已變更，則傳回 [確定]。</span><span class="sxs-lookup"><span data-stu-id="a9357-121">It returns an error if the buffer requirements were not set, S\_FALSE if the requirements have not changed, and S\_OK if the requirements have changed.</span></span>

<span data-ttu-id="a9357-122">衍生類別應該覆寫這個方法，以執行實際的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="a9357-122">A derived class should override this method to perform the actual memory allocation.</span></span> <span data-ttu-id="a9357-123">一般而言，衍生類別會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="a9357-123">Typically, the derived class will perform the following steps:</span></span>

1.  <span data-ttu-id="a9357-124">呼叫基類執行，以判斷記憶體是否真的需要配置。</span><span class="sxs-lookup"><span data-stu-id="a9357-124">Call the base class implementation, to determine whether the memory truly needs allocating.</span></span>
2.  <span data-ttu-id="a9357-125">配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="a9357-125">Allocate memory.</span></span>
3.  <span data-ttu-id="a9357-126">建立 [**CMediaSample**](cmediasample.md) 物件，其中包含步驟2中的記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="a9357-126">Create [**CMediaSample**](cmediasample.md) objects that contain chunks of memory from step 2.</span></span>
4.  <span data-ttu-id="a9357-127">將每個 **CMediaSample** 物件新增至免費範例清單， ([**CBaseAllocator：： m \_ lFree**](cbaseallocator-m-lfree.md)) 。</span><span class="sxs-lookup"><span data-stu-id="a9357-127">Add each **CMediaSample** object to the list of free samples ([**CBaseAllocator::m\_lFree**](cbaseallocator-m-lfree.md)).</span></span>

<span data-ttu-id="a9357-128">如需範例，請參閱 [**CMemAllocator：：分配**](cmemallocator-alloc.md)。</span><span class="sxs-lookup"><span data-stu-id="a9357-128">For an example, see [**CMemAllocator::Alloc**](cmemallocator-alloc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9357-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9357-129">Requirements</span></span>



| <span data-ttu-id="a9357-130">需求</span><span class="sxs-lookup"><span data-stu-id="a9357-130">Requirement</span></span> | <span data-ttu-id="a9357-131">值</span><span class="sxs-lookup"><span data-stu-id="a9357-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9357-132">標頭</span><span class="sxs-lookup"><span data-stu-id="a9357-132">Header</span></span><br/>  | <dl> <span data-ttu-id="a9357-133"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a9357-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a9357-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="a9357-134">Library</span></span><br/> | <dl> <span data-ttu-id="a9357-135"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a9357-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9357-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9357-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9357-137">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="a9357-137">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




