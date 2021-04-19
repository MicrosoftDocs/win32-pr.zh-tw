---
description: CCritSec 類別提供執行緒鎖定。
ms.assetid: ecc60afe-15d0-4780-8133-1dfc558c6325
title: 'CCritSec 類別 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8db0243ecfecd47655f547d40390e602c04d5b88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000388"
---
# <a name="ccritsec-class"></a><span data-ttu-id="87cdd-103">CCritSec 類別</span><span class="sxs-lookup"><span data-stu-id="87cdd-103">CCritSec class</span></span>

<span data-ttu-id="87cdd-104">**CCritSec** 類別提供執行緒鎖定。</span><span class="sxs-lookup"><span data-stu-id="87cdd-104">The **CCritSec** class provides a thread lock.</span></span>

<span data-ttu-id="87cdd-105">這個類別是 Windows **重要 \_ 區段** 物件的精簡型包裝函式。</span><span class="sxs-lookup"><span data-stu-id="87cdd-105">This class is a thin wrapper for a Windows **CRITICAL\_SECTION** object.</span></span> <span data-ttu-id="87cdd-106">您可以藉由呼叫 [**CCritSec：： lock**](ccritsec-lock.md) 和 [**CCritSec：： unlock**](ccritsec-unlock.md) 方法來鎖定和解除鎖定執行緒。</span><span class="sxs-lookup"><span data-stu-id="87cdd-106">You can lock and unlock the thread by calling the [**CCritSec::Lock**](ccritsec-lock.md) and [**CCritSec::Unlock**](ccritsec-unlock.md) methods.</span></span> <span data-ttu-id="87cdd-107">但是，將此類別與 [**CAutoLock**](cautolock.md) 類別搭配使用會比較安全。</span><span class="sxs-lookup"><span data-stu-id="87cdd-107">However, it is safer to use this class in conjunction with the [**CAutoLock**](cautolock.md) class.</span></span> <span data-ttu-id="87cdd-108">當 **CAutoLock** 類別超出範圍時，會自動將 **CCritSec** 物件解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="87cdd-108">When the **CAutoLock** class goes out of scope, it automatically unlocks the **CCritSec** object.</span></span> <span data-ttu-id="87cdd-109">此外，它也會編譯成有效率的內嵌程式碼。</span><span class="sxs-lookup"><span data-stu-id="87cdd-109">Moreover, it compiles to efficient inline code.</span></span>



| <span data-ttu-id="87cdd-110">Public 成員變數</span><span class="sxs-lookup"><span data-stu-id="87cdd-110">Public Member Variables</span></span>                            | <span data-ttu-id="87cdd-111">Description</span><span class="sxs-lookup"><span data-stu-id="87cdd-111">Description</span></span>                                              |
|----------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="87cdd-112">**m \_ currentOwner**</span><span class="sxs-lookup"><span data-stu-id="87cdd-112">**m\_currentOwner**</span></span>](ccritsec-m-currentowner.md) | <span data-ttu-id="87cdd-113">擁有線程的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="87cdd-113">Thread identifier of the owning thread.</span></span>                  |
| [<span data-ttu-id="87cdd-114">**m \_ lockCount**</span><span class="sxs-lookup"><span data-stu-id="87cdd-114">**m\_lockCount**</span></span>](ccritsec-m-lockcount.md)       | <span data-ttu-id="87cdd-115">此物件上的未完成鎖定數目。</span><span class="sxs-lookup"><span data-stu-id="87cdd-115">Number of outstanding locks on this object.</span></span>              |
| [<span data-ttu-id="87cdd-116">**m \_ fTrace**</span><span class="sxs-lookup"><span data-stu-id="87cdd-116">**m\_fTrace**</span></span>](ccritsec-m-ftrace.md)             | <span data-ttu-id="87cdd-117">指定是否要追蹤此鎖定的布林值。</span><span class="sxs-lookup"><span data-stu-id="87cdd-117">Boolean value that specifies whether to trace this lock.</span></span> |
| <span data-ttu-id="87cdd-118">公用方法</span><span class="sxs-lookup"><span data-stu-id="87cdd-118">Public Methods</span></span>                                     | <span data-ttu-id="87cdd-119">Description</span><span class="sxs-lookup"><span data-stu-id="87cdd-119">Description</span></span>                                              |
| [<span data-ttu-id="87cdd-120">**CCritSec**</span><span class="sxs-lookup"><span data-stu-id="87cdd-120">**CCritSec**</span></span>](ccritsec-ccritsec.md)              | <span data-ttu-id="87cdd-121">函式方法。</span><span class="sxs-lookup"><span data-stu-id="87cdd-121">Constructor method.</span></span>                                      |
| [<span data-ttu-id="87cdd-122">**~ CCritSec**</span><span class="sxs-lookup"><span data-stu-id="87cdd-122">**~CCritSec**</span></span>](ccritsec--ccritsec.md)            | <span data-ttu-id="87cdd-123">函式方法。</span><span class="sxs-lookup"><span data-stu-id="87cdd-123">Destructor method.</span></span>                                       |
| [<span data-ttu-id="87cdd-124">**鎖定**</span><span class="sxs-lookup"><span data-stu-id="87cdd-124">**Lock**</span></span>](ccritsec-lock.md)                      | <span data-ttu-id="87cdd-125">鎖定重要區段物件。</span><span class="sxs-lookup"><span data-stu-id="87cdd-125">Locks the critical section object.</span></span>                       |
| [<span data-ttu-id="87cdd-126">**Unlock**</span><span class="sxs-lookup"><span data-stu-id="87cdd-126">**Unlock**</span></span>](ccritsec-unlock.md)                  | <span data-ttu-id="87cdd-127">解除鎖定重要區段物件。</span><span class="sxs-lookup"><span data-stu-id="87cdd-127">Unlocks the critical section object.</span></span>                     |



 

## <a name="requirements"></a><span data-ttu-id="87cdd-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="87cdd-128">Requirements</span></span>



| <span data-ttu-id="87cdd-129">需求</span><span class="sxs-lookup"><span data-stu-id="87cdd-129">Requirement</span></span> | <span data-ttu-id="87cdd-130">值</span><span class="sxs-lookup"><span data-stu-id="87cdd-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87cdd-131">標頭</span><span class="sxs-lookup"><span data-stu-id="87cdd-131">Header</span></span><br/>  | <dl> <span data-ttu-id="87cdd-132"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="87cdd-132"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="87cdd-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="87cdd-133">Library</span></span><br/> | <dl> <span data-ttu-id="87cdd-134"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="87cdd-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87cdd-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87cdd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87cdd-136">重要區段物件</span><span class="sxs-lookup"><span data-stu-id="87cdd-136">Critical Section Objects</span></span>](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[<span data-ttu-id="87cdd-137">DirectShow 基類參考</span><span class="sxs-lookup"><span data-stu-id="87cdd-137">DirectShow Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

