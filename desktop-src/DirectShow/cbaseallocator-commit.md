---
description: Commit 方法會為緩衝區配置記憶體。 這個方法會實 IMemAllocator：： Commit 方法。
ms.assetid: e8c36276-0229-428f-b030-978651ab7534
title: 'CBaseAllocator 的 Commit 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Commit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b49fae72e5588105b1235c1f0c461d5cc45cfa2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983046"
---
# <a name="cbaseallocatorcommit-method"></a><span data-ttu-id="89120-104">CBaseAllocator Commit 方法</span><span class="sxs-lookup"><span data-stu-id="89120-104">CBaseAllocator.Commit method</span></span>

<span data-ttu-id="89120-105">方法會配置 `Commit` 緩衝區的記憶體。</span><span class="sxs-lookup"><span data-stu-id="89120-105">The `Commit` method allocates the memory for the buffers.</span></span> <span data-ttu-id="89120-106">這個方法會實 [**IMemAllocator：： Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) 方法。</span><span class="sxs-lookup"><span data-stu-id="89120-106">This method implements the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="89120-107">語法</span><span class="sxs-lookup"><span data-stu-id="89120-107">Syntax</span></span>


```C++
HRESULT Commit();
```



## <a name="parameters"></a><span data-ttu-id="89120-108">參數</span><span class="sxs-lookup"><span data-stu-id="89120-108">Parameters</span></span>

<span data-ttu-id="89120-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="89120-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="89120-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="89120-110">Return value</span></span>

<span data-ttu-id="89120-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="89120-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="89120-112">可能的值包括下列清單中的值。</span><span class="sxs-lookup"><span data-stu-id="89120-112">Possible values include those in the following list.</span></span>



| <span data-ttu-id="89120-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="89120-113">Return code</span></span>                                                                                       | <span data-ttu-id="89120-114">Description</span><span class="sxs-lookup"><span data-stu-id="89120-114">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="89120-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="89120-115"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="89120-116">成功。</span><span class="sxs-lookup"><span data-stu-id="89120-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="89120-117"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="89120-117"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="89120-118">未指定緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="89120-118">Buffer requirements were not specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="89120-119">備註</span><span class="sxs-lookup"><span data-stu-id="89120-119">Remarks</span></span>

<span data-ttu-id="89120-120">在呼叫這個方法之前，請先呼叫 [**CBaseAllocator：： SetProperties**](cbaseallocator-setproperties.md) 方法來指定緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="89120-120">Before calling this method, call the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method to specify the buffer requirements.</span></span>

<span data-ttu-id="89120-121">這個方法會呼叫虛擬方法 [**CBaseAllocator：：**](cbaseallocator-alloc.md) allocate 來配置緩衝區的記憶體。</span><span class="sxs-lookup"><span data-stu-id="89120-121">This method calls the virtual method [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) to allocate the memory for the buffers.</span></span> <span data-ttu-id="89120-122">衍生類別可以覆寫 **分配**。</span><span class="sxs-lookup"><span data-stu-id="89120-122">Derived classes can override **Alloc**.</span></span> <span data-ttu-id="89120-123">如果取消認可作業暫止，則會將其取消。</span><span class="sxs-lookup"><span data-stu-id="89120-123">If a decommit operation is pending, it is canceled.</span></span>

<span data-ttu-id="89120-124">您必須在呼叫 [**CBaseAllocator：： GetBuffer**](cbaseallocator-getbuffer.md) 方法之前呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="89120-124">You must call this method before calling the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="89120-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="89120-125">Requirements</span></span>



| <span data-ttu-id="89120-126">需求</span><span class="sxs-lookup"><span data-stu-id="89120-126">Requirement</span></span> | <span data-ttu-id="89120-127">值</span><span class="sxs-lookup"><span data-stu-id="89120-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89120-128">標頭</span><span class="sxs-lookup"><span data-stu-id="89120-128">Header</span></span><br/>  | <dl> <span data-ttu-id="89120-129"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="89120-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="89120-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="89120-130">Library</span></span><br/> | <dl> <span data-ttu-id="89120-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="89120-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89120-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89120-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89120-133">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="89120-133">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




