---
description: CMemAllocator 配置方法-配置方法會為緩衝區配置記憶體。
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: 'CMemAllocator 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d7de755aa3b8007a122e43529d16f5e39ca0cb8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099036"
---
# <a name="cmemallocatoralloc-method"></a><span data-ttu-id="dbda1-103">CMemAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="dbda1-103">CMemAllocator.Alloc method</span></span>

<span data-ttu-id="dbda1-104">`Alloc`方法會為緩衝區配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="dbda1-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbda1-105">語法</span><span class="sxs-lookup"><span data-stu-id="dbda1-105">Syntax</span></span>


```C++
HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="dbda1-106">參數</span><span class="sxs-lookup"><span data-stu-id="dbda1-106">Parameters</span></span>

<span data-ttu-id="dbda1-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="dbda1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dbda1-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="dbda1-108">Return value</span></span>

<span data-ttu-id="dbda1-109">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="dbda1-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="dbda1-110">傳回碼</span><span class="sxs-lookup"><span data-stu-id="dbda1-110">Return code</span></span>                                                                                       | <span data-ttu-id="dbda1-111">Description</span><span class="sxs-lookup"><span data-stu-id="dbda1-111">Description</span></span>                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="dbda1-112"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="dbda1-112"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="dbda1-113">成功。</span><span class="sxs-lookup"><span data-stu-id="dbda1-113">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="dbda1-114"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="dbda1-114"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="dbda1-115">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="dbda1-115">Insufficient memory.</span></span><br/>              |
| <dl> <span data-ttu-id="dbda1-116"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="dbda1-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="dbda1-117">未設定緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="dbda1-117">Buffer requirements were not set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dbda1-118">備註</span><span class="sxs-lookup"><span data-stu-id="dbda1-118">Remarks</span></span>

<span data-ttu-id="dbda1-119">[**CBaseAllocator：： Commit**](cbaseallocator-commit.md)方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="dbda1-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span> <span data-ttu-id="dbda1-120">它會針對 [**CMemAllocator：： SetProperties**](cmemallocator-setproperties.md) 方法中提供的緩衝區需求，配置足夠的連續記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="dbda1-120">It allocates a contiguous block of memory sufficient for the buffer requirements given in the [**CMemAllocator::SetProperties**](cmemallocator-setproperties.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbda1-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbda1-121">Requirements</span></span>



| <span data-ttu-id="dbda1-122">需求</span><span class="sxs-lookup"><span data-stu-id="dbda1-122">Requirement</span></span> | <span data-ttu-id="dbda1-123">值</span><span class="sxs-lookup"><span data-stu-id="dbda1-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbda1-124">標頭</span><span class="sxs-lookup"><span data-stu-id="dbda1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="dbda1-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="dbda1-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dbda1-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="dbda1-126">Library</span></span><br/> | <dl> <span data-ttu-id="dbda1-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="dbda1-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbda1-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbda1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbda1-129">**CMemAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="dbda1-129">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




