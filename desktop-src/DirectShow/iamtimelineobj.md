---
description: IAMTimelineObj 介面提供在 DirectShow 編輯服務 (DES) 中操作時間軸物件的方法。
ms.assetid: ae8a778d-00b3-4b88-98dd-16e0a8645127
title: 'IAMTimelineObj 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e968ec01d937aeac9a5838b75462a6d23a632512
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995656"
---
# <a name="iamtimelineobj-interface"></a><span data-ttu-id="73ff3-103">IAMTimelineObj 介面</span><span class="sxs-lookup"><span data-stu-id="73ff3-103">IAMTimelineObj interface</span></span>

> [!Note]  
> <span data-ttu-id="73ff3-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="73ff3-104">\[Deprecated.</span></span> <span data-ttu-id="73ff3-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="73ff3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="73ff3-106">`IAMTimelineObj`介面提供在[DirectShow 編輯服務](directshow-editing-services.md) (DES) 中操作時間軸物件的方法。</span><span class="sxs-lookup"><span data-stu-id="73ff3-106">The `IAMTimelineObj` interface provides methods for manipulating timeline objects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="73ff3-107">所有時程表物件都會執行此方法，包括來源、效果、轉換、追蹤、群組和組合物件。</span><span class="sxs-lookup"><span data-stu-id="73ff3-107">All timeline objects implement this method, including source, effect, transition, track, group, and composition objects.</span></span> <span data-ttu-id="73ff3-108">藉由呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) 方法來建立時間軸物件。</span><span class="sxs-lookup"><span data-stu-id="73ff3-108">Create a timeline object by calling the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="73ff3-109">成員</span><span class="sxs-lookup"><span data-stu-id="73ff3-109">Members</span></span>

<span data-ttu-id="73ff3-110">**IAMTimelineObj** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="73ff3-110">The **IAMTimelineObj** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="73ff3-111">**IAMTimelineObj** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="73ff3-111">**IAMTimelineObj** also has these types of members:</span></span>

-   [<span data-ttu-id="73ff3-112">方法</span><span class="sxs-lookup"><span data-stu-id="73ff3-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="73ff3-113">方法</span><span class="sxs-lookup"><span data-stu-id="73ff3-113">Methods</span></span>

<span data-ttu-id="73ff3-114">**IAMTimelineObj** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="73ff3-114">The **IAMTimelineObj** interface has these methods.</span></span>



| <span data-ttu-id="73ff3-115">方法</span><span class="sxs-lookup"><span data-stu-id="73ff3-115">Method</span></span>                                                          | <span data-ttu-id="73ff3-116">描述</span><span class="sxs-lookup"><span data-stu-id="73ff3-116">Description</span></span>                                                                                                                            |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73ff3-117">**ClearDirty**</span><span class="sxs-lookup"><span data-stu-id="73ff3-117">**ClearDirty**</span></span>](iamtimelineobj-cleardirty.md)                 | <span data-ttu-id="73ff3-118">不支援。</span><span class="sxs-lookup"><span data-stu-id="73ff3-118">Not supported.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="73ff3-119">**FixTimes**</span><span class="sxs-lookup"><span data-stu-id="73ff3-119">**FixTimes**</span></span>](iamtimelineobj-fixtimes.md)                     | <span data-ttu-id="73ff3-120">將指定的開始和停止時間四捨五入至最接近的框架界限。</span><span class="sxs-lookup"><span data-stu-id="73ff3-120">Rounds the specified start and stop times to the nearest frame boundaries.</span></span><br/>                                                  |
| [<span data-ttu-id="73ff3-121">**FixTimes2**</span><span class="sxs-lookup"><span data-stu-id="73ff3-121">**FixTimes2**</span></span>](iamtimelineobj-fixtimes2.md)                   | <span data-ttu-id="73ff3-122">將指定的開始和停止時間（指定為 [**REFTIME**](reftime.md) 值）四捨五入到最接近的框架界限。</span><span class="sxs-lookup"><span data-stu-id="73ff3-122">Rounds the specified start and stop times, specified as [**REFTIME**](reftime.md) values, to the nearest frame boundaries.</span></span><br/> |
| [<span data-ttu-id="73ff3-123">**GetDirtyRange**</span><span class="sxs-lookup"><span data-stu-id="73ff3-123">**GetDirtyRange**</span></span>](iamtimelineobj-getdirtyrange.md)           | <span data-ttu-id="73ff3-124">不支援。</span><span class="sxs-lookup"><span data-stu-id="73ff3-124">Not supported.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="73ff3-125">**GetDirtyRange2**</span><span class="sxs-lookup"><span data-stu-id="73ff3-125">**GetDirtyRange2**</span></span>](iamtimelineobj-getdirtyrange2.md)         | <span data-ttu-id="73ff3-126">不支援。</span><span class="sxs-lookup"><span data-stu-id="73ff3-126">Not supported.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="73ff3-127">**GetEmbedDepth**</span><span class="sxs-lookup"><span data-stu-id="73ff3-127">**GetEmbedDepth**</span></span>](iamtimelineobj-getembeddepth.md)           | <span data-ttu-id="73ff3-128">不支援。</span><span class="sxs-lookup"><span data-stu-id="73ff3-128">Not supported.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="73ff3-129">**GetGenID**</span><span class="sxs-lookup"><span data-stu-id="73ff3-129">**GetGenID**</span></span>](iamtimelineobj-getgenid.md)                     | <span data-ttu-id="73ff3-130">抓取物件所產生的識別碼。</span><span class="sxs-lookup"><span data-stu-id="73ff3-130">Retrieves the object's generated identifier.</span></span><br/>                                                                                |
| [<span data-ttu-id="73ff3-131">**GetGroupIBelongTo**</span><span class="sxs-lookup"><span data-stu-id="73ff3-131">**GetGroupIBelongTo**</span></span>](iamtimelineobj-getgroupibelongto.md)   | <span data-ttu-id="73ff3-132">不支援。</span><span class="sxs-lookup"><span data-stu-id="73ff3-132">Not supported.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="73ff3-133">**GetLocked**</span><span class="sxs-lookup"><span data-stu-id="73ff3-133">**GetLocked**</span></span>](iamtimelineobj-getlocked.md)                   | <span data-ttu-id="73ff3-134">抓取物件的編輯狀態 (鎖定或解除鎖定) 。</span><span class="sxs-lookup"><span data-stu-id="73ff3-134">Retrieves the object's editing state (locked or unlocked).</span></span><br/>                                                                  |
| [<span data-ttu-id="73ff3-135">**GetMuted**</span><span class="sxs-lookup"><span data-stu-id="73ff3-135">**GetMuted**</span></span>](iamtimelineobj-getmuted.md)                     | <span data-ttu-id="73ff3-136">抓取物件的已靜音狀態。</span><span class="sxs-lookup"><span data-stu-id="73ff3-136">Retrieves the object's muted state.</span></span><br/>                                                                                         |
| [<span data-ttu-id="73ff3-137">**GetPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="73ff3-137">**GetPropertySetter**</span></span>](iamtimelineobj-getpropertysetter.md)   | <span data-ttu-id="73ff3-138">抓取物件的屬性 setter。</span><span class="sxs-lookup"><span data-stu-id="73ff3-138">Retrieves the object's property setter.</span></span><br/>                                                                                     |
| [<span data-ttu-id="73ff3-139">**GetStartStop**</span><span class="sxs-lookup"><span data-stu-id="73ff3-139">**GetStartStop**</span></span>](iamtimelineobj-getstartstop.md)             | <span data-ttu-id="73ff3-140">抓取物件的開始和停止時間，相對於物件的父系。</span><span class="sxs-lookup"><span data-stu-id="73ff3-140">Retrieves the object's start and stop times, relative to the object's parent.</span></span><br/>                                               |
| [<span data-ttu-id="73ff3-141">**GetStartStop2**</span><span class="sxs-lookup"><span data-stu-id="73ff3-141">**GetStartStop2**</span></span>](iamtimelineobj-getstartstop2.md)           | <span data-ttu-id="73ff3-142">以 [**REFTIME**](reftime.md) 值形式抓取物件的開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="73ff3-142">Retrieves the object's start and stop times, as [**REFTIME**](reftime.md) values.</span></span><br/>                                          |
| [<span data-ttu-id="73ff3-143">**GetSubObject**</span><span class="sxs-lookup"><span data-stu-id="73ff3-143">**GetSubObject**</span></span>](iamtimelineobj-getsubobject.md)             | <span data-ttu-id="73ff3-144">捕獲與這個物件相關聯的子物件。</span><span class="sxs-lookup"><span data-stu-id="73ff3-144">Retrieves the subobject associated with this object.</span></span><br/>                                                                        |
| [<span data-ttu-id="73ff3-145">**GetSubObjectGUID**</span><span class="sxs-lookup"><span data-stu-id="73ff3-145">**GetSubObjectGUID**</span></span>](iamtimelineobj-getsubobjectguid.md)     | <span data-ttu-id="73ff3-146">抓取與這個時間軸物件相關聯的子物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="73ff3-146">Retrieves the GUID of the subobject associated with this timeline object.</span></span><br/>                                                   |
| [<span data-ttu-id="73ff3-147">**GetSubObjectGUIDB**</span><span class="sxs-lookup"><span data-stu-id="73ff3-147">**GetSubObjectGUIDB**</span></span>](iamtimelineobj-getsubobjectguidb.md)   | <span data-ttu-id="73ff3-148">以 **BSTR** 值形式抓取子物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="73ff3-148">Retrieves the GUID of the subobject as a **BSTR** value.</span></span><br/>                                                                    |
| [<span data-ttu-id="73ff3-149">**GetSubObjectLoaded**</span><span class="sxs-lookup"><span data-stu-id="73ff3-149">**GetSubObjectLoaded**</span></span>](iamtimelineobj-getsubobjectloaded.md) | <span data-ttu-id="73ff3-150">判斷是否已設定物件的子物件指標。</span><span class="sxs-lookup"><span data-stu-id="73ff3-150">Determines whether the object's subobject pointer has been set.</span></span><br/>                                                             |
| [<span data-ttu-id="73ff3-151">**GetTimelineNoRef**</span><span class="sxs-lookup"><span data-stu-id="73ff3-151">**GetTimelineNoRef**</span></span>](iamtimelineobj-gettimelinenoref.md)     | <span data-ttu-id="73ff3-152">不支援。</span><span class="sxs-lookup"><span data-stu-id="73ff3-152">Not supported.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="73ff3-153">**GetTimelineType**</span><span class="sxs-lookup"><span data-stu-id="73ff3-153">**GetTimelineType**</span></span>](iamtimelineobj-gettimelinetype.md)       | <span data-ttu-id="73ff3-154">抓取物件的型別。</span><span class="sxs-lookup"><span data-stu-id="73ff3-154">Retrieves the object's type.</span></span><br/>                                                                                                |
| [<span data-ttu-id="73ff3-155">**GetUserData**</span><span class="sxs-lookup"><span data-stu-id="73ff3-155">**GetUserData**</span></span>](iamtimelineobj-getuserdata.md)               | <span data-ttu-id="73ff3-156">抓取應用程式定義的持續性資料。</span><span class="sxs-lookup"><span data-stu-id="73ff3-156">Retrieves the application-defined persistent data.</span></span><br/>                                                                          |
| [<span data-ttu-id="73ff3-157">**GetUserID**</span><span class="sxs-lookup"><span data-stu-id="73ff3-157">**GetUserID**</span></span>](iamtimelineobj-getuserid.md)                   | <span data-ttu-id="73ff3-158">抓取物件的應用程式定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="73ff3-158">Retrieves the object's application-defined identifier.</span></span><br/>                                                                      |
| [<span data-ttu-id="73ff3-159">**GetUserName**</span><span class="sxs-lookup"><span data-stu-id="73ff3-159">**GetUserName**</span></span>](iamtimelineobj-getusername.md)               | <span data-ttu-id="73ff3-160">抓取物件的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="73ff3-160">Retrieves the object's application-defined name.</span></span><br/>                                                                            |
| [<span data-ttu-id="73ff3-161">**移除**</span><span class="sxs-lookup"><span data-stu-id="73ff3-161">**Remove**</span></span>](iamtimelineobj-remove.md)                         | <span data-ttu-id="73ff3-162">從時間軸移除此物件，以便在其他地方 reinsertion。</span><span class="sxs-lookup"><span data-stu-id="73ff3-162">Removes this object from the timeline, for reinsertion elsewhere.</span></span><br/>                                                           |
| [<span data-ttu-id="73ff3-163">**RemoveAll**</span><span class="sxs-lookup"><span data-stu-id="73ff3-163">**RemoveAll**</span></span>](iamtimelineobj-removeall.md)                   | <span data-ttu-id="73ff3-164">從時間軸中永久移除這個物件，包括子物件和子系。</span><span class="sxs-lookup"><span data-stu-id="73ff3-164">Permanently removes this object from the timeline, including subobjects and children.</span></span><br/>                                       |
| [<span data-ttu-id="73ff3-165">**SetDirtyRange**</span><span class="sxs-lookup"><span data-stu-id="73ff3-165">**SetDirtyRange**</span></span>](iamtimelineobj-setdirtyrange.md)           | <span data-ttu-id="73ff3-166">未實作。</span><span class="sxs-lookup"><span data-stu-id="73ff3-166">Not implemented.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="73ff3-167">**SetDirtyRange2**</span><span class="sxs-lookup"><span data-stu-id="73ff3-167">**SetDirtyRange2**</span></span>](iamtimelineobj-setdirtyrange2.md)         | <span data-ttu-id="73ff3-168">未實作。</span><span class="sxs-lookup"><span data-stu-id="73ff3-168">Not implemented.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="73ff3-169">**SetLocked**</span><span class="sxs-lookup"><span data-stu-id="73ff3-169">**SetLocked**</span></span>](iamtimelineobj-setlocked.md)                   | <span data-ttu-id="73ff3-170">將物件的編輯狀態設定為 [已鎖定] 或 [已解除鎖定]。</span><span class="sxs-lookup"><span data-stu-id="73ff3-170">Sets the object's editing state to locked or unlocked.</span></span><br/>                                                                      |
| [<span data-ttu-id="73ff3-171">**SetMuted**</span><span class="sxs-lookup"><span data-stu-id="73ff3-171">**SetMuted**</span></span>](iamtimelineobj-setmuted.md)                     | <span data-ttu-id="73ff3-172">設定物件的已靜音狀態。</span><span class="sxs-lookup"><span data-stu-id="73ff3-172">Sets the object's muted state.</span></span><br/>                                                                                              |
| [<span data-ttu-id="73ff3-173">**SetPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="73ff3-173">**SetPropertySetter**</span></span>](iamtimelineobj-setpropertysetter.md)   | <span data-ttu-id="73ff3-174">設定物件的屬性 setter。</span><span class="sxs-lookup"><span data-stu-id="73ff3-174">Sets the object's property setter.</span></span><br/>                                                                                          |
| [<span data-ttu-id="73ff3-175">**SetStartStop**</span><span class="sxs-lookup"><span data-stu-id="73ff3-175">**SetStartStop**</span></span>](iamtimelineobj-setstartstop.md)             | <span data-ttu-id="73ff3-176">設定物件的開始和停止時間（相對於時程表）。</span><span class="sxs-lookup"><span data-stu-id="73ff3-176">Sets the object's start and stop times, relative to the timeline.</span></span><br/>                                                           |
| [<span data-ttu-id="73ff3-177">**SetStartStop2**</span><span class="sxs-lookup"><span data-stu-id="73ff3-177">**SetStartStop2**</span></span>](iamtimelineobj-setstartstop2.md)           | <span data-ttu-id="73ff3-178">將物件的開始和停止時間設定為 **REFTIME** 值。</span><span class="sxs-lookup"><span data-stu-id="73ff3-178">Sets the object's start and stop times, as **REFTIME** values.</span></span><br/>                                                              |
| [<span data-ttu-id="73ff3-179">**SetSubObject**</span><span class="sxs-lookup"><span data-stu-id="73ff3-179">**SetSubObject**</span></span>](iamtimelineobj-setsubobject.md)             | <span data-ttu-id="73ff3-180">不支援。</span><span class="sxs-lookup"><span data-stu-id="73ff3-180">Not supported.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="73ff3-181">**SetSubObjectGUID**</span><span class="sxs-lookup"><span data-stu-id="73ff3-181">**SetSubObjectGUID**</span></span>](iamtimelineobj-setsubobjectguid.md)     | <span data-ttu-id="73ff3-182">指定與這個物件相關聯之子物件的全域唯一識別碼 (GUID) 。</span><span class="sxs-lookup"><span data-stu-id="73ff3-182">Specifies the globally unique identifier (GUID) of the subobject associated with this object.</span></span><br/>                               |
| [<span data-ttu-id="73ff3-183">**SetSubObjectGUIDB**</span><span class="sxs-lookup"><span data-stu-id="73ff3-183">**SetSubObjectGUIDB**</span></span>](iamtimelineobj-setsubobjectguidb.md)   | <span data-ttu-id="73ff3-184">將子物件的 GUID 指定為 **BSTR** 值。</span><span class="sxs-lookup"><span data-stu-id="73ff3-184">Specifies the GUID of the subobject as a **BSTR** value.</span></span><br/>                                                                    |
| [<span data-ttu-id="73ff3-185">**SetTimelineType**</span><span class="sxs-lookup"><span data-stu-id="73ff3-185">**SetTimelineType**</span></span>](iamtimelineobj-settimelinetype.md)       | <span data-ttu-id="73ff3-186">不支援。</span><span class="sxs-lookup"><span data-stu-id="73ff3-186">Not supported.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="73ff3-187">**SetUserData**</span><span class="sxs-lookup"><span data-stu-id="73ff3-187">**SetUserData**</span></span>](iamtimelineobj-setuserdata.md)               | <span data-ttu-id="73ff3-188">設定應用程式定義的持續性資料。</span><span class="sxs-lookup"><span data-stu-id="73ff3-188">Sets application-defined persistent data.</span></span><br/>                                                                                   |
| [<span data-ttu-id="73ff3-189">**SetUserID**</span><span class="sxs-lookup"><span data-stu-id="73ff3-189">**SetUserID**</span></span>](iamtimelineobj-setuserid.md)                   | <span data-ttu-id="73ff3-190">設定物件的應用程式定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="73ff3-190">Sets an application-defined identifier for the object.</span></span><br/>                                                                      |
| [<span data-ttu-id="73ff3-191">**SetUserName**</span><span class="sxs-lookup"><span data-stu-id="73ff3-191">**SetUserName**</span></span>](iamtimelineobj-setusername.md)               | <span data-ttu-id="73ff3-192">設定物件的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="73ff3-192">Sets an application-defined name for the object.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="73ff3-193">備註</span><span class="sxs-lookup"><span data-stu-id="73ff3-193">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="73ff3-194">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="73ff3-194">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="73ff3-195">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="73ff3-195">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="73ff3-196">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="73ff3-196">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="73ff3-197">規格需求</span><span class="sxs-lookup"><span data-stu-id="73ff3-197">Requirements</span></span>



| <span data-ttu-id="73ff3-198">需求</span><span class="sxs-lookup"><span data-stu-id="73ff3-198">Requirement</span></span> | <span data-ttu-id="73ff3-199">值</span><span class="sxs-lookup"><span data-stu-id="73ff3-199">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73ff3-200">標頭</span><span class="sxs-lookup"><span data-stu-id="73ff3-200">Header</span></span><br/>  | <dl> <span data-ttu-id="73ff3-201"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="73ff3-201"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="73ff3-202">程式庫</span><span class="sxs-lookup"><span data-stu-id="73ff3-202">Library</span></span><br/> | <dl> <span data-ttu-id="73ff3-203"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="73ff3-203"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
