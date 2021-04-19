---
description: 這個介面是用來控制動畫功能，連接動畫集與正在進行動畫的轉換框架。
ms.assetid: a485e4d2-82e1-45db-8496-dd743904c34d
title: 'ID3DXAnimationController 介面 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ed587be50ba41d4544152985285b20ab63bd745
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982889"
---
# <a name="id3dxanimationcontroller-interface"></a><span data-ttu-id="36249-103">ID3DXAnimationController 介面</span><span class="sxs-lookup"><span data-stu-id="36249-103">ID3DXAnimationController interface</span></span>

<span data-ttu-id="36249-104">這個介面是用來控制動畫功能，連接動畫集與正在進行動畫的轉換框架。</span><span class="sxs-lookup"><span data-stu-id="36249-104">This interface is used to control animation functionality, connecting animation sets with the transformation frames that are being animated.</span></span> <span data-ttu-id="36249-105">介面具有混合多個動畫的方法，並可在一段時間內修改混合參數，以啟用平滑轉換和其他效果。</span><span class="sxs-lookup"><span data-stu-id="36249-105">The interface has methods to mix multiple animations and to modify blending parameters over time to enable smooth transitions and other effects.</span></span>

## <a name="members"></a><span data-ttu-id="36249-106">成員</span><span class="sxs-lookup"><span data-stu-id="36249-106">Members</span></span>

<span data-ttu-id="36249-107">**ID3DXAnimationController** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="36249-107">The **ID3DXAnimationController** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="36249-108">**ID3DXAnimationController** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="36249-108">**ID3DXAnimationController** also has these types of members:</span></span>

-   [<span data-ttu-id="36249-109">方法</span><span class="sxs-lookup"><span data-stu-id="36249-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="36249-110">方法</span><span class="sxs-lookup"><span data-stu-id="36249-110">Methods</span></span>

<span data-ttu-id="36249-111">**ID3DXAnimationController** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="36249-111">The **ID3DXAnimationController** interface has these methods.</span></span>



| <span data-ttu-id="36249-112">方法</span><span class="sxs-lookup"><span data-stu-id="36249-112">Method</span></span>                                                                                   | <span data-ttu-id="36249-113">描述</span><span class="sxs-lookup"><span data-stu-id="36249-113">Description</span></span>                                                                                                                                             |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36249-114">**AdvanceTime**</span><span class="sxs-lookup"><span data-stu-id="36249-114">**AdvanceTime**</span></span>](id3dxanimationcontroller--advancetime.md)                             | <span data-ttu-id="36249-115">將網格繪製到動畫，並以指定的數量前進全域動畫時間。</span><span class="sxs-lookup"><span data-stu-id="36249-115">Animates the mesh and advances the global animation time by a specified amount.</span></span><br/>                                                              |
| [<span data-ttu-id="36249-116">**CloneAnimationController**</span><span class="sxs-lookup"><span data-stu-id="36249-116">**CloneAnimationController**</span></span>](id3dxanimationcontroller--cloneanimationcontroller.md)   | <span data-ttu-id="36249-117">複製或複製動畫控制器。</span><span class="sxs-lookup"><span data-stu-id="36249-117">Clones, or copies, an animation controller.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="36249-118">**GetAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="36249-118">**GetAnimationSet**</span></span>](id3dxanimationcontroller--getanimationset.md)                     | <span data-ttu-id="36249-119">取得動畫集。</span><span class="sxs-lookup"><span data-stu-id="36249-119">Gets an animation set.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="36249-120">**GetAnimationSetByName**</span><span class="sxs-lookup"><span data-stu-id="36249-120">**GetAnimationSetByName**</span></span>](id3dxanimationcontroller--getanimationsetbyname.md)         | <span data-ttu-id="36249-121">取得動畫集合，並指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="36249-121">Gets an animation set, given its name.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="36249-122">**GetCurrentPriorityBlend**</span><span class="sxs-lookup"><span data-stu-id="36249-122">**GetCurrentPriorityBlend**</span></span>](id3dxanimationcontroller--getcurrentpriorityblend.md)     | <span data-ttu-id="36249-123">傳回目前正在執行之優先順序 blend 事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="36249-123">Returns an event handle to a priority blend event that is currently running.</span></span><br/>                                                                 |
| [<span data-ttu-id="36249-124">**GetCurrentTrackEvent**</span><span class="sxs-lookup"><span data-stu-id="36249-124">**GetCurrentTrackEvent**</span></span>](id3dxanimationcontroller--getcurrenttrackevent.md)           | <span data-ttu-id="36249-125">傳回目前在指定動畫播放軌上執行的事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="36249-125">Returns an event handle to the event currently running on the specified animation track.</span></span><br/>                                                     |
| [<span data-ttu-id="36249-126">**GetEventDesc**</span><span class="sxs-lookup"><span data-stu-id="36249-126">**GetEventDesc**</span></span>](id3dxanimationcontroller--geteventdesc.md)                           | <span data-ttu-id="36249-127">取得指定動畫事件的描述。</span><span class="sxs-lookup"><span data-stu-id="36249-127">Gets a description of a specified animation event.</span></span><br/>                                                                                           |
| [<span data-ttu-id="36249-128">**GetMaxNumAnimationOutputs**</span><span class="sxs-lookup"><span data-stu-id="36249-128">**GetMaxNumAnimationOutputs**</span></span>](id3dxanimationcontroller--getmaxnumanimationoutputs.md) | <span data-ttu-id="36249-129">取得動畫控制器可支援的動畫輸出數目上限。</span><span class="sxs-lookup"><span data-stu-id="36249-129">Get the maximum number of animation outputs the animation controller can support.</span></span><br/>                                                            |
| [<span data-ttu-id="36249-130">**GetMaxNumAnimationSets**</span><span class="sxs-lookup"><span data-stu-id="36249-130">**GetMaxNumAnimationSets**</span></span>](id3dxanimationcontroller--getmaxnumanimationsets.md)       | <span data-ttu-id="36249-131">取得動畫控制器可支援的動畫集合數目上限。</span><span class="sxs-lookup"><span data-stu-id="36249-131">Gets the maximum number of animation sets the animation controller can support.</span></span><br/>                                                              |
| [<span data-ttu-id="36249-132">**GetMaxNumEvents**</span><span class="sxs-lookup"><span data-stu-id="36249-132">**GetMaxNumEvents**</span></span>](id3dxanimationcontroller--getmaxnumevents.md)                     | <span data-ttu-id="36249-133">取得動畫控制器可支援的事件數目上限。</span><span class="sxs-lookup"><span data-stu-id="36249-133">Gets the maximum number of events the animation controller can support.</span></span><br/>                                                                      |
| [<span data-ttu-id="36249-134">**GetMaxNumTracks**</span><span class="sxs-lookup"><span data-stu-id="36249-134">**GetMaxNumTracks**</span></span>](id3dxanimationcontroller--getmaxnumtracks.md)                     | <span data-ttu-id="36249-135">取得動畫控制器中的曲目數目上限。</span><span class="sxs-lookup"><span data-stu-id="36249-135">Gets the maximum number of tracks in the animation controller.</span></span><br/>                                                                               |
| [<span data-ttu-id="36249-136">**GetNumAnimationSets**</span><span class="sxs-lookup"><span data-stu-id="36249-136">**GetNumAnimationSets**</span></span>](id3dxanimationcontroller--getnumanimationsets.md)             | <span data-ttu-id="36249-137">傳回目前在動畫控制器中註冊的動畫集合數目。</span><span class="sxs-lookup"><span data-stu-id="36249-137">Returns the number of animation sets currently registered in the animation controller.</span></span><br/>                                                       |
| [<span data-ttu-id="36249-138">**GetPriorityBlend**</span><span class="sxs-lookup"><span data-stu-id="36249-138">**GetPriorityBlend**</span></span>](id3dxanimationcontroller--getpriorityblend.md)                   | <span data-ttu-id="36249-139">取得動畫控制器所使用的目前優先權混合權數。</span><span class="sxs-lookup"><span data-stu-id="36249-139">Gets the current priority blending weight used by the animation controller.</span></span><br/>                                                                  |
| [<span data-ttu-id="36249-140">**GetTime**</span><span class="sxs-lookup"><span data-stu-id="36249-140">**GetTime**</span></span>](id3dxanimationcontroller--gettime.md)                                     | <span data-ttu-id="36249-141">取得全域動畫時間。</span><span class="sxs-lookup"><span data-stu-id="36249-141">Gets the global animation time.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="36249-142">**GetTrackAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="36249-142">**GetTrackAnimationSet**</span></span>](id3dxanimationcontroller--gettrackanimationset.md)           | <span data-ttu-id="36249-143">取得指定之播放軌的動畫集。</span><span class="sxs-lookup"><span data-stu-id="36249-143">Gets the animation set for the given track.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="36249-144">**GetTrackDesc**</span><span class="sxs-lookup"><span data-stu-id="36249-144">**GetTrackDesc**</span></span>](id3dxanimationcontroller--gettrackdesc.md)                           | <span data-ttu-id="36249-145">取得追蹤描述。</span><span class="sxs-lookup"><span data-stu-id="36249-145">Gets the track description.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="36249-146">**GetUpcomingPriorityBlend**</span><span class="sxs-lookup"><span data-stu-id="36249-146">**GetUpcomingPriorityBlend**</span></span>](id3dxanimationcontroller--getupcomingpriorityblend.md)   | <span data-ttu-id="36249-147">傳回已排定在指定事件之後發生之下一個優先權 blend 事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="36249-147">Returns an event handle to the next priority blend event scheduled to occur after a specified event.</span></span><br/>                                         |
| [<span data-ttu-id="36249-148">**GetUpcomingTrackEvent**</span><span class="sxs-lookup"><span data-stu-id="36249-148">**GetUpcomingTrackEvent**</span></span>](id3dxanimationcontroller--getupcomingtrackevent.md)         | <span data-ttu-id="36249-149">傳回在動畫播放軌上指定的事件之後，排定要發生之下一個事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="36249-149">Returns an event handle to the next event scheduled to occur after a specified event on an animation track.</span></span><br/>                                  |
| [<span data-ttu-id="36249-150">**KeyPriorityBlend**</span><span class="sxs-lookup"><span data-stu-id="36249-150">**KeyPriorityBlend**</span></span>](id3dxanimationcontroller--keypriorityblend.md)                   | <span data-ttu-id="36249-151">設定指定動畫播放軌的混合事件索引鍵。</span><span class="sxs-lookup"><span data-stu-id="36249-151">Sets blending event keys for the specified animation track.</span></span><br/>                                                                                  |
| [<span data-ttu-id="36249-152">**KeyTrackEnable**</span><span class="sxs-lookup"><span data-stu-id="36249-152">**KeyTrackEnable**</span></span>](id3dxanimationcontroller--keytrackenable.md)                       | <span data-ttu-id="36249-153">設定可啟用或停用動畫播放軌的事件索引鍵。</span><span class="sxs-lookup"><span data-stu-id="36249-153">Sets an event key that enables or disables an animation track.</span></span><br/>                                                                               |
| [<span data-ttu-id="36249-154">**KeyTrackPosition**</span><span class="sxs-lookup"><span data-stu-id="36249-154">**KeyTrackPosition**</span></span>](id3dxanimationcontroller--keytrackposition.md)                   | <span data-ttu-id="36249-155">設定事件索引鍵，以變更動畫播放軌的當地時間。</span><span class="sxs-lookup"><span data-stu-id="36249-155">Sets an event key that changes the local time of an animation track.</span></span><br/>                                                                         |
| [<span data-ttu-id="36249-156">**KeyTrackSpeed**</span><span class="sxs-lookup"><span data-stu-id="36249-156">**KeyTrackSpeed**</span></span>](id3dxanimationcontroller--keytrackspeed.md)                         | <span data-ttu-id="36249-157">設定可變更動畫播放軌播放速率的事件索引鍵。</span><span class="sxs-lookup"><span data-stu-id="36249-157">Sets an event key that changes the rate of play of an animation track.</span></span><br/>                                                                       |
| [<span data-ttu-id="36249-158">**KeyTrackWeight**</span><span class="sxs-lookup"><span data-stu-id="36249-158">**KeyTrackWeight**</span></span>](id3dxanimationcontroller--keytrackweight.md)                       | <span data-ttu-id="36249-159">設定可變更動畫播放軌權數的事件索引鍵。將多個追蹤結合在一起時，權數會用來做為乘數。</span><span class="sxs-lookup"><span data-stu-id="36249-159">Sets an event key that changes the weight of an animation track. The weight is used as a multiplier when combining multiple tracks together.</span></span><br/> |
| [<span data-ttu-id="36249-160">**RegisterAnimationOutput**</span><span class="sxs-lookup"><span data-stu-id="36249-160">**RegisterAnimationOutput**</span></span>](id3dxanimationcontroller--registeranimationoutput.md)     | <span data-ttu-id="36249-161">將動畫輸出新增至動畫控制器，並註冊用於調整、旋轉和轉譯 (SRT) 轉換的指標。</span><span class="sxs-lookup"><span data-stu-id="36249-161">Adds an animation output to the animation controller and registers pointers for scale, rotate, and translate (SRT) transformations.</span></span><br/>          |
| [<span data-ttu-id="36249-162">**RegisterAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="36249-162">**RegisterAnimationSet**</span></span>](id3dxanimationcontroller--registeranimationset.md)           | <span data-ttu-id="36249-163">將動畫集加入至動畫控制器。</span><span class="sxs-lookup"><span data-stu-id="36249-163">Adds an animation set to the animation controller.</span></span><br/>                                                                                           |
| [<span data-ttu-id="36249-164">**ResetTime**</span><span class="sxs-lookup"><span data-stu-id="36249-164">**ResetTime**</span></span>](id3dxanimationcontroller--resettime.md)                                 | <span data-ttu-id="36249-165">將全域動畫的時間重設為零。</span><span class="sxs-lookup"><span data-stu-id="36249-165">Resets the global animation time to zero.</span></span> <span data-ttu-id="36249-166">任何暫止的事件將會保留其原始排程，但在新的時間範圍內。</span><span class="sxs-lookup"><span data-stu-id="36249-166">Any pending events will retain their original schedules, but in the new timeframe.</span></span><br/>                 |
| [<span data-ttu-id="36249-167">**SetPriorityBlend**</span><span class="sxs-lookup"><span data-stu-id="36249-167">**SetPriorityBlend**</span></span>](id3dxanimationcontroller--setpriorityblend.md)                   | <span data-ttu-id="36249-168">設定動畫控制器所使用的優先順序混合權數。</span><span class="sxs-lookup"><span data-stu-id="36249-168">Sets the priority blending weight used by the animation controller.</span></span><br/>                                                                          |
| [<span data-ttu-id="36249-169">**SetTrackAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="36249-169">**SetTrackAnimationSet**</span></span>](id3dxanimationcontroller--settrackanimationset.md)           | <span data-ttu-id="36249-170">將動畫集套用至指定的曲目。</span><span class="sxs-lookup"><span data-stu-id="36249-170">Applies the animation set to the specified track.</span></span><br/>                                                                                            |
| [<span data-ttu-id="36249-171">**SetTrackDesc**</span><span class="sxs-lookup"><span data-stu-id="36249-171">**SetTrackDesc**</span></span>](id3dxanimationcontroller--settrackdesc.md)                           | <span data-ttu-id="36249-172">設定追蹤描述。</span><span class="sxs-lookup"><span data-stu-id="36249-172">Sets the track description.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="36249-173">**SetTrackEnable**</span><span class="sxs-lookup"><span data-stu-id="36249-173">**SetTrackEnable**</span></span>](id3dxanimationcontroller--settrackenable.md)                       | <span data-ttu-id="36249-174">啟用或停用動畫控制器中的軌跡。</span><span class="sxs-lookup"><span data-stu-id="36249-174">Enables or disables a track in the animation controller.</span></span><br/>                                                                                     |
| [<span data-ttu-id="36249-175">**SetTrackPosition**</span><span class="sxs-lookup"><span data-stu-id="36249-175">**SetTrackPosition**</span></span>](id3dxanimationcontroller--settrackposition.md)                   | <span data-ttu-id="36249-176">將軌跡設定為指定的本機動畫時間。</span><span class="sxs-lookup"><span data-stu-id="36249-176">Sets the track to the specified local animation time.</span></span><br/>                                                                                        |
| [<span data-ttu-id="36249-177">**SetTrackPriority**</span><span class="sxs-lookup"><span data-stu-id="36249-177">**SetTrackPriority**</span></span>](id3dxanimationcontroller--settrackpriority.md)                   | <span data-ttu-id="36249-178">設定指定動畫播放軌的優先順序混合加權。</span><span class="sxs-lookup"><span data-stu-id="36249-178">Sets the priority blending weight for the specified animation track.</span></span><br/>                                                                         |
| [<span data-ttu-id="36249-179">**SetTrackSpeed**</span><span class="sxs-lookup"><span data-stu-id="36249-179">**SetTrackSpeed**</span></span>](id3dxanimationcontroller--settrackspeed.md)                         | <span data-ttu-id="36249-180">設定追蹤速度。</span><span class="sxs-lookup"><span data-stu-id="36249-180">Sets the track speed.</span></span> <span data-ttu-id="36249-181">追蹤速度類似于用來加速播放播放軌或減緩播放速度的乘數。</span><span class="sxs-lookup"><span data-stu-id="36249-181">The track speed is similar to a multiplier that is used to speed up or slow down the playback of the track.</span></span><br/>            |
| [<span data-ttu-id="36249-182">**SetTrackWeight**</span><span class="sxs-lookup"><span data-stu-id="36249-182">**SetTrackWeight**</span></span>](id3dxanimationcontroller--settrackweight.md)                       | <span data-ttu-id="36249-183">設定軌跡加權。</span><span class="sxs-lookup"><span data-stu-id="36249-183">Sets the track weight.</span></span> <span data-ttu-id="36249-184">權數用來決定如何將多個追蹤混合在一起。</span><span class="sxs-lookup"><span data-stu-id="36249-184">The weight is used to determine how to blend multiple tracks together.</span></span><br/>                                                |
| [<span data-ttu-id="36249-185">**UnkeyAllPriorityBlends**</span><span class="sxs-lookup"><span data-stu-id="36249-185">**UnkeyAllPriorityBlends**</span></span>](id3dxanimationcontroller--unkeyallpriorityblends.md)       | <span data-ttu-id="36249-186">從動畫控制器中移除所有排程的優先順序 blend 事件。</span><span class="sxs-lookup"><span data-stu-id="36249-186">Removes all scheduled priority blend events from the animation controller.</span></span><br/>                                                                   |
| [<span data-ttu-id="36249-187">**UnkeyAllTrackEvents**</span><span class="sxs-lookup"><span data-stu-id="36249-187">**UnkeyAllTrackEvents**</span></span>](id3dxanimationcontroller--unkeyalltrackevents.md)             | <span data-ttu-id="36249-188">從指定的動畫播放軌移除所有事件。</span><span class="sxs-lookup"><span data-stu-id="36249-188">Removes all events from a specified animation track.</span></span><br/>                                                                                         |
| [<span data-ttu-id="36249-189">**UnkeyEvent**</span><span class="sxs-lookup"><span data-stu-id="36249-189">**UnkeyEvent**</span></span>](id3dxanimationcontroller--unkeyevent.md)                               | <span data-ttu-id="36249-190">從動畫播放軌移除指定的事件，以防止事件的執行。</span><span class="sxs-lookup"><span data-stu-id="36249-190">Removes a specified event from an animation track, preventing the execution of the event.</span></span><br/>                                                    |
| [<span data-ttu-id="36249-191">**UnregisterAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="36249-191">**UnregisterAnimationSet**</span></span>](id3dxanimationcontroller--unregisteranimationset.md)       | <span data-ttu-id="36249-192">從動畫控制器移除動畫集。</span><span class="sxs-lookup"><span data-stu-id="36249-192">Removes an animation set from the animation controller.</span></span><br/>                                                                                      |
| [<span data-ttu-id="36249-193">**ValidateEvent**</span><span class="sxs-lookup"><span data-stu-id="36249-193">**ValidateEvent**</span></span>](id3dxanimationcontroller--validateevent.md)                         | <span data-ttu-id="36249-194">檢查指定的事件控制碼是否有效，以及動畫事件是否尚未完成。</span><span class="sxs-lookup"><span data-stu-id="36249-194">Checks whether a specified event handle is valid and the animation event has not yet completed.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="36249-195">備註</span><span class="sxs-lookup"><span data-stu-id="36249-195">Remarks</span></span>

<span data-ttu-id="36249-196">使用 [**D3DXCreateAnimationController**](d3dxcreateanimationcontroller.md)建立動畫控制器物件。</span><span class="sxs-lookup"><span data-stu-id="36249-196">Create an animation controller object with [**D3DXCreateAnimationController**](d3dxcreateanimationcontroller.md).</span></span>

<span data-ttu-id="36249-197">LPD3DXANIMATIONCONTROLLER 型別定義為 **ID3DXAnimationController** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="36249-197">The LPD3DXANIMATIONCONTROLLER type is defined as a pointer to the **ID3DXAnimationController** interface.</span></span>


```
typedef interface ID3DXAnimationController ID3DXAnimationController;
typedef interface ID3DXAnimationController *LPD3DXANIMATIONCONTROLLER;
```



<span data-ttu-id="36249-198">D3DXEVENTHANDLE 型別定義為動畫控制器事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="36249-198">The D3DXEVENTHANDLE type is defined as an event handle to animation controller events.</span></span>


```
typedef DWORD D3DXEVENTHANDLE;
```



<span data-ttu-id="36249-199">LPD3DXEVENTHANDLE 型別定義為動畫控制器事件的事件控制碼指標。</span><span class="sxs-lookup"><span data-stu-id="36249-199">The LPD3DXEVENTHANDLE type is defined as a pointer to an event handle to animation controller events.</span></span>


```
typedef D3DXEVENTHANDLE *LPD3DXEVENTHANDLE;
```



## <a name="requirements"></a><span data-ttu-id="36249-200">規格需求</span><span class="sxs-lookup"><span data-stu-id="36249-200">Requirements</span></span>



| <span data-ttu-id="36249-201">需求</span><span class="sxs-lookup"><span data-stu-id="36249-201">Requirement</span></span> | <span data-ttu-id="36249-202">值</span><span class="sxs-lookup"><span data-stu-id="36249-202">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36249-203">標頭</span><span class="sxs-lookup"><span data-stu-id="36249-203">Header</span></span><br/>  | <dl> <span data-ttu-id="36249-204"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="36249-204"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="36249-205">程式庫</span><span class="sxs-lookup"><span data-stu-id="36249-205">Library</span></span><br/> | <dl> <span data-ttu-id="36249-206"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="36249-206"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="36249-207">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36249-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36249-208">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="36249-208">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
