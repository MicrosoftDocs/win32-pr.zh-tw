---
description: CBaseMediaFilter 類別會實 IMediaFilter 介面。
ms.assetid: 45c8973b-d0b3-4aeb-96e7-be47f8d7f4a7
title: 'CBaseMediaFilter 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e594fd941fffecc836af26bd3d70cced82ddcaa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000732"
---
# <a name="cbasemediafilter-class"></a><span data-ttu-id="213fa-103">CBaseMediaFilter 類別</span><span class="sxs-lookup"><span data-stu-id="213fa-103">CBaseMediaFilter class</span></span>

![cbasemediafilter](images/filter05.png)

<span data-ttu-id="213fa-105">類別會實 `CBaseMediaFilter` [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) 介面。</span><span class="sxs-lookup"><span data-stu-id="213fa-105">The `CBaseMediaFilter` class implements the [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) interface.</span></span> <span data-ttu-id="213fa-106">針對外掛程式散發者或其他需要支援 **IMediaFilter** 而不支援 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面的物件，請使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="213fa-106">Use this class for plug-in distributors or other objects that need to support **IMediaFilter** without supporting the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="213fa-107">請勿將這個類別用於篩選。</span><span class="sxs-lookup"><span data-stu-id="213fa-107">Do not use this class for filters.</span></span> <span data-ttu-id="213fa-108">請改為使用 [**CBaseFilter**](cbasefilter.md) 類別或衍生自 **CBaseFilter** 的基類。</span><span class="sxs-lookup"><span data-stu-id="213fa-108">Instead, use the [**CBaseFilter**](cbasefilter.md) class, or a base class derived from **CBaseFilter**.</span></span>



| <span data-ttu-id="213fa-109">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="213fa-109">Protected Member Variables</span></span>                                       | <span data-ttu-id="213fa-110">Description</span><span class="sxs-lookup"><span data-stu-id="213fa-110">Description</span></span>                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="213fa-111">**m \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="213fa-111">**m\_State**</span></span>](cbasemediafilter-m-state.md)                     | <span data-ttu-id="213fa-112">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="213fa-112">Current state of the object.</span></span>                                 |
| [<span data-ttu-id="213fa-113">**m \_ pClock**</span><span class="sxs-lookup"><span data-stu-id="213fa-113">**m\_pClock**</span></span>](cbasemediafilter-m-pclock.md)                   | <span data-ttu-id="213fa-114">物件參考時鐘的指標。</span><span class="sxs-lookup"><span data-stu-id="213fa-114">Pointer to the object's reference clock.</span></span>                     |
| [<span data-ttu-id="213fa-115">**m \_ tStart**</span><span class="sxs-lookup"><span data-stu-id="213fa-115">**m\_tStart**</span></span>](cbasemediafilter-m-tstart.md)                   | <span data-ttu-id="213fa-116">對應于資料流程時間0的參考時間。</span><span class="sxs-lookup"><span data-stu-id="213fa-116">Reference time that corresponds to stream time 0.</span></span>            |
| [<span data-ttu-id="213fa-117">**m \_ clsid**</span><span class="sxs-lookup"><span data-stu-id="213fa-117">**m\_clsid**</span></span>](cbasemediafilter-m-clsid.md)                     | <span data-ttu-id="213fa-118">物件 (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="213fa-118">Class identifier (CLSID) of the object.</span></span>                      |
| [<span data-ttu-id="213fa-119">**m \_ pLock**</span><span class="sxs-lookup"><span data-stu-id="213fa-119">**m\_pLock**</span></span>](cbasemediafilter-m-plock.md)                     | <span data-ttu-id="213fa-120">重要區段的指標。</span><span class="sxs-lookup"><span data-stu-id="213fa-120">Pointer to a critical section.</span></span>                               |
| <span data-ttu-id="213fa-121">公用方法</span><span class="sxs-lookup"><span data-stu-id="213fa-121">Public Methods</span></span>                                                   | <span data-ttu-id="213fa-122">Description</span><span class="sxs-lookup"><span data-stu-id="213fa-122">Description</span></span>                                                  |
| [<span data-ttu-id="213fa-123">**CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="213fa-123">**CBaseMediaFilter**</span></span>](cbasemediafilter-cbasemediafilter.md)    | <span data-ttu-id="213fa-124">函式方法。</span><span class="sxs-lookup"><span data-stu-id="213fa-124">Constructor method.</span></span>                                          |
| [<span data-ttu-id="213fa-125">**~ CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="213fa-125">**~ CBaseMediaFilter**</span></span>](cbasemediafilter--cbasemediafilter.md) | <span data-ttu-id="213fa-126">函式方法。</span><span class="sxs-lookup"><span data-stu-id="213fa-126">Destructor method.</span></span> <span data-ttu-id="213fa-127">虛擬。</span><span class="sxs-lookup"><span data-stu-id="213fa-127">Virtual.</span></span>                                  |
| [<span data-ttu-id="213fa-128">**StreamTime**</span><span class="sxs-lookup"><span data-stu-id="213fa-128">**StreamTime**</span></span>](cbasemediafilter-streamtime.md)                | <span data-ttu-id="213fa-129">抓取目前的資料流程時間。</span><span class="sxs-lookup"><span data-stu-id="213fa-129">Retrieves the current stream time.</span></span> <span data-ttu-id="213fa-130">虛擬。</span><span class="sxs-lookup"><span data-stu-id="213fa-130">Virtual.</span></span>                  |
| [<span data-ttu-id="213fa-131">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="213fa-131">**IsActive**</span></span>](cbasemediafilter-isactive.md)                    | <span data-ttu-id="213fa-132">判斷物件是否為作用中， (執行中或已暫停) 。</span><span class="sxs-lookup"><span data-stu-id="213fa-132">Determines whether the object is active (running or paused).</span></span> |
| <span data-ttu-id="213fa-133">IPersist 方法</span><span class="sxs-lookup"><span data-stu-id="213fa-133">IPersist Methods</span></span>                                                 | <span data-ttu-id="213fa-134">Description</span><span class="sxs-lookup"><span data-stu-id="213fa-134">Description</span></span>                                                  |
| [<span data-ttu-id="213fa-135">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="213fa-135">**GetClassID**</span></span>](cbasemediafilter-getclassid.md)                | <span data-ttu-id="213fa-136">捕獲類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="213fa-136">Retrieves the class identifier.</span></span>                              |
| <span data-ttu-id="213fa-137">IMediaFilter 方法</span><span class="sxs-lookup"><span data-stu-id="213fa-137">IMediaFilter Methods</span></span>                                             | <span data-ttu-id="213fa-138">Description</span><span class="sxs-lookup"><span data-stu-id="213fa-138">Description</span></span>                                                  |
| [<span data-ttu-id="213fa-139">**GetState**</span><span class="sxs-lookup"><span data-stu-id="213fa-139">**GetState**</span></span>](cbasemediafilter-getstate.md)                    | <span data-ttu-id="213fa-140">抓取物件的狀態 (執行中、已停止或已暫停) 。</span><span class="sxs-lookup"><span data-stu-id="213fa-140">Retrieves the object's state (running, stopped, or paused).</span></span>  |
| [<span data-ttu-id="213fa-141">**SetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="213fa-141">**SetSyncSource**</span></span>](cbasemediafilter-setsyncsource.md)          | <span data-ttu-id="213fa-142">設定物件的參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="213fa-142">Sets a reference clock for the object.</span></span>                       |
| [<span data-ttu-id="213fa-143">**GetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="213fa-143">**GetSyncSource**</span></span>](cbasemediafilter-getsyncsource.md)          | <span data-ttu-id="213fa-144">抓取物件正在使用的參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="213fa-144">Retrieves the reference clock that the object is using.</span></span>      |
| [<span data-ttu-id="213fa-145">**停止**</span><span class="sxs-lookup"><span data-stu-id="213fa-145">**Stop**</span></span>](cbasemediafilter-stop.md)                            | <span data-ttu-id="213fa-146">停止物件。</span><span class="sxs-lookup"><span data-stu-id="213fa-146">Stops the object.</span></span>                                            |
| [<span data-ttu-id="213fa-147">**暫停**</span><span class="sxs-lookup"><span data-stu-id="213fa-147">**Pause**</span></span>](cbasemediafilter-pause.md)                          | <span data-ttu-id="213fa-148">暫停物件。</span><span class="sxs-lookup"><span data-stu-id="213fa-148">Pauses the object.</span></span>                                           |
| [<span data-ttu-id="213fa-149">**執行**</span><span class="sxs-lookup"><span data-stu-id="213fa-149">**Run**</span></span>](cbasemediafilter-run.md)                              | <span data-ttu-id="213fa-150">執行物件。</span><span class="sxs-lookup"><span data-stu-id="213fa-150">Runs the object.</span></span>                                             |



 

## <a name="requirements"></a><span data-ttu-id="213fa-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="213fa-151">Requirements</span></span>



| <span data-ttu-id="213fa-152">需求</span><span class="sxs-lookup"><span data-stu-id="213fa-152">Requirement</span></span> | <span data-ttu-id="213fa-153">值</span><span class="sxs-lookup"><span data-stu-id="213fa-153">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="213fa-154">標頭</span><span class="sxs-lookup"><span data-stu-id="213fa-154">Header</span></span><br/>  | <dl> <span data-ttu-id="213fa-155"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="213fa-155"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="213fa-156">程式庫</span><span class="sxs-lookup"><span data-stu-id="213fa-156">Library</span></span><br/> | <dl> <span data-ttu-id="213fa-157"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="213fa-157"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




