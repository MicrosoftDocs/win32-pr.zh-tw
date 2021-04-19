---
description: IAMTimeline 介面提供操作時間軸的方法，也就是 Microsoft DirectShow 編輯服務 (DES) 中的中央物件。
ms.assetid: 6750efa0-946c-4ad3-b0df-de55872b94c3
title: 'IAMTimeline 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc4374a198232625b87448004b667ccd8ce0183b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995046"
---
# <a name="iamtimeline-interface"></a><span data-ttu-id="34c01-103">IAMTimeline 介面</span><span class="sxs-lookup"><span data-stu-id="34c01-103">IAMTimeline interface</span></span>

> [!Note]  
> <span data-ttu-id="34c01-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="34c01-104">\[Deprecated.</span></span> <span data-ttu-id="34c01-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="34c01-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="34c01-106">`IAMTimeline`介面提供操作時間軸的方法，也就是 Microsoft [DirectShow 編輯服務](directshow-editing-services.md) (DES) 中的中央物件。</span><span class="sxs-lookup"><span data-stu-id="34c01-106">The `IAMTimeline` interface provides methods for manipulating the timeline, the central object in Microsoft [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="34c01-107">時間軸是經過時間排序的元素集合，例如影片剪輯、音訊剪輯、效果和剪輯之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="34c01-107">A timeline is a collection of time-ordered elements, such as video clips, audio clips, effects, and transitions between clips.</span></span> <span data-ttu-id="34c01-108">轉譯引擎會使用時間軸來建立篩選圖形，應用程式可從中產生轉譯的輸出。</span><span class="sxs-lookup"><span data-stu-id="34c01-108">The render engine uses the timeline to create a filter graph, from which the application can generate the rendered output.</span></span>

<span data-ttu-id="34c01-109">`IAMTimeline` 執行三項基本服務。</span><span class="sxs-lookup"><span data-stu-id="34c01-109">`IAMTimeline` performs three basic services.</span></span> <span data-ttu-id="34c01-110">其</span><span class="sxs-lookup"><span data-stu-id="34c01-110">It</span></span>

-   <span data-ttu-id="34c01-111">在時間軸中建立物件。</span><span class="sxs-lookup"><span data-stu-id="34c01-111">Creates the objects in the timeline.</span></span>
-   <span data-ttu-id="34c01-112">作為這些物件的容器。</span><span class="sxs-lookup"><span data-stu-id="34c01-112">Acts as a container for those objects.</span></span>
-   <span data-ttu-id="34c01-113">設定和抓取時間軸的一般參數。</span><span class="sxs-lookup"><span data-stu-id="34c01-113">Sets and retrieves general parameters of the timeline.</span></span>

<span data-ttu-id="34c01-114">若要建立時程表物件，請使用類別識別碼 CLSID AMTimeline 來呼叫 **CoCreateInstance** \_ 。</span><span class="sxs-lookup"><span data-stu-id="34c01-114">To create the timeline object, call **CoCreateInstance** with the class identifier CLSID\_AMTimeline.</span></span>

## <a name="members"></a><span data-ttu-id="34c01-115">成員</span><span class="sxs-lookup"><span data-stu-id="34c01-115">Members</span></span>

<span data-ttu-id="34c01-116">**IAMTimeline** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="34c01-116">The **IAMTimeline** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="34c01-117">**IAMTimeline** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="34c01-117">**IAMTimeline** also has these types of members:</span></span>

-   [<span data-ttu-id="34c01-118">方法</span><span class="sxs-lookup"><span data-stu-id="34c01-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="34c01-119">方法</span><span class="sxs-lookup"><span data-stu-id="34c01-119">Methods</span></span>

<span data-ttu-id="34c01-120">**IAMTimeline** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="34c01-120">The **IAMTimeline** interface has these methods.</span></span>



| <span data-ttu-id="34c01-121">方法</span><span class="sxs-lookup"><span data-stu-id="34c01-121">Method</span></span>                                                             | <span data-ttu-id="34c01-122">描述</span><span class="sxs-lookup"><span data-stu-id="34c01-122">Description</span></span>                                                                                                                       |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34c01-123">**AddGroup**</span><span class="sxs-lookup"><span data-stu-id="34c01-123">**AddGroup**</span></span>](iamtimeline-addgroup.md)                           | <span data-ttu-id="34c01-124">將群組加入至時間軸。</span><span class="sxs-lookup"><span data-stu-id="34c01-124">Adds a group to the timeline.</span></span><br/>                                                                                          |
| [<span data-ttu-id="34c01-125">**ClearAllGroups**</span><span class="sxs-lookup"><span data-stu-id="34c01-125">**ClearAllGroups**</span></span>](iamtimeline-clearallgroups.md)               | <span data-ttu-id="34c01-126">從時間軸移除所有群組，以及這些群組中包含的所有物件。</span><span class="sxs-lookup"><span data-stu-id="34c01-126">Removes all groups from the timeline, along with all objects contained in those groups.</span></span><br/>                                |
| [<span data-ttu-id="34c01-127">**CreateEmptyNode**</span><span class="sxs-lookup"><span data-stu-id="34c01-127">**CreateEmptyNode**</span></span>](iamtimeline-createemptynode.md)             | <span data-ttu-id="34c01-128">建立新的時間軸物件。</span><span class="sxs-lookup"><span data-stu-id="34c01-128">Creates a new timeline object.</span></span><br/>                                                                                         |
| [<span data-ttu-id="34c01-129">**EffectsEnabled**</span><span class="sxs-lookup"><span data-stu-id="34c01-129">**EffectsEnabled**</span></span>](iamtimeline-effectsenabled.md)               | <span data-ttu-id="34c01-130">判斷是否已啟用效果。</span><span class="sxs-lookup"><span data-stu-id="34c01-130">Determines whether effects are enabled.</span></span><br/>                                                                                |
| [<span data-ttu-id="34c01-131">**EnableEffects**</span><span class="sxs-lookup"><span data-stu-id="34c01-131">**EnableEffects**</span></span>](iamtimeline-enableeffects.md)                 | <span data-ttu-id="34c01-132">啟用或停用時間軸中的所有效果。</span><span class="sxs-lookup"><span data-stu-id="34c01-132">Enables or disables all effects in the timeline.</span></span><br/>                                                                       |
| [<span data-ttu-id="34c01-133">**EnableTransitions**</span><span class="sxs-lookup"><span data-stu-id="34c01-133">**EnableTransitions**</span></span>](iamtimeline-enabletransitions.md)         | <span data-ttu-id="34c01-134">啟用或停用時間軸中的所有轉換。</span><span class="sxs-lookup"><span data-stu-id="34c01-134">Enables or disables all transitions in the timeline.</span></span><br/>                                                                   |
| [<span data-ttu-id="34c01-135">**GetCountOfType**</span><span class="sxs-lookup"><span data-stu-id="34c01-135">**GetCountOfType**</span></span>](iamtimeline-getcountoftype.md)               | <span data-ttu-id="34c01-136">抓取指定的群組及其所有子系中所包含之指定類型的物件數目。</span><span class="sxs-lookup"><span data-stu-id="34c01-136">Retrieves the number of objects of the specified type that are contained in a specified group and all of its children.</span></span><br/> |
| [<span data-ttu-id="34c01-137">**GetDefaultEffect**</span><span class="sxs-lookup"><span data-stu-id="34c01-137">**GetDefaultEffect**</span></span>](iamtimeline-getdefaulteffect.md)           | <span data-ttu-id="34c01-138">捕獲預設效果。</span><span class="sxs-lookup"><span data-stu-id="34c01-138">Retrieves the default effect.</span></span><br/>                                                                                          |
| [<span data-ttu-id="34c01-139">**GetDefaultEffectB**</span><span class="sxs-lookup"><span data-stu-id="34c01-139">**GetDefaultEffectB**</span></span>](iamtimeline-getdefaulteffectb.md)         | <span data-ttu-id="34c01-140">以 **BSTR** 值形式抓取預設效果。</span><span class="sxs-lookup"><span data-stu-id="34c01-140">Retrieves the default effect as a **BSTR** value.</span></span><br/>                                                                      |
| [<span data-ttu-id="34c01-141">**GetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="34c01-141">**GetDefaultFPS**</span></span>](iamtimeline-getdefaultfps.md)                 | <span data-ttu-id="34c01-142">抓取預設輸出畫面播放速率（以每秒畫面格速率為單位）。</span><span class="sxs-lookup"><span data-stu-id="34c01-142">Retrieves the default output frame rate, in frames per second.</span></span><br/>                                                         |
| [<span data-ttu-id="34c01-143">**GetDefaultTransition**</span><span class="sxs-lookup"><span data-stu-id="34c01-143">**GetDefaultTransition**</span></span>](iamtimeline-getdefaulttransition.md)   | <span data-ttu-id="34c01-144">捕獲預設轉換。</span><span class="sxs-lookup"><span data-stu-id="34c01-144">Retrieves the default transition.</span></span><br/>                                                                                      |
| [<span data-ttu-id="34c01-145">**GetDefaultTransitionB**</span><span class="sxs-lookup"><span data-stu-id="34c01-145">**GetDefaultTransitionB**</span></span>](iamtimeline-getdefaulttransitionb.md) | <span data-ttu-id="34c01-146">以 **BSTR** 值形式抓取預設轉換。</span><span class="sxs-lookup"><span data-stu-id="34c01-146">Retrieves the default transition as a **BSTR** value.</span></span><br/>                                                                  |
| [<span data-ttu-id="34c01-147">**GetDirtyRange**</span><span class="sxs-lookup"><span data-stu-id="34c01-147">**GetDirtyRange**</span></span>](iamtimeline-getdirtyrange.md)                 | <span data-ttu-id="34c01-148">不支援。</span><span class="sxs-lookup"><span data-stu-id="34c01-148">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="34c01-149">**GetDuration**</span><span class="sxs-lookup"><span data-stu-id="34c01-149">**GetDuration**</span></span>](iamtimeline-getduration.md)                     | <span data-ttu-id="34c01-150">抓取時間軸的持續時間。</span><span class="sxs-lookup"><span data-stu-id="34c01-150">Retrieves the timeline duration.</span></span><br/>                                                                                       |
| [<span data-ttu-id="34c01-151">**GetDuration2**</span><span class="sxs-lookup"><span data-stu-id="34c01-151">**GetDuration2**</span></span>](iamtimeline-getduration2.md)                   | <span data-ttu-id="34c01-152">以 **雙精度浮點數** 的形式抓取時間軸持續時間。</span><span class="sxs-lookup"><span data-stu-id="34c01-152">Retrieves the timeline duration as a **double**.</span></span><br/>                                                                       |
| [<span data-ttu-id="34c01-153">**GetGroup**</span><span class="sxs-lookup"><span data-stu-id="34c01-153">**GetGroup**</span></span>](iamtimeline-getgroup.md)                           | <span data-ttu-id="34c01-154">抓取指定的群組。</span><span class="sxs-lookup"><span data-stu-id="34c01-154">Retrieves a specified group.</span></span><br/>                                                                                           |
| [<span data-ttu-id="34c01-155">**GetGroupCount**</span><span class="sxs-lookup"><span data-stu-id="34c01-155">**GetGroupCount**</span></span>](iamtimeline-getgroupcount.md)                 | <span data-ttu-id="34c01-156">抓取時間軸中包含的群組數目。</span><span class="sxs-lookup"><span data-stu-id="34c01-156">Retrieves the number of groups that are contained in the timeline.</span></span><br/>                                                     |
| [<span data-ttu-id="34c01-157">**GetInsertMode**</span><span class="sxs-lookup"><span data-stu-id="34c01-157">**GetInsertMode**</span></span>](iamtimeline-getinsertmode.md)                 | <span data-ttu-id="34c01-158">不支援。</span><span class="sxs-lookup"><span data-stu-id="34c01-158">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="34c01-159">**IsDirty**</span><span class="sxs-lookup"><span data-stu-id="34c01-159">**IsDirty**</span></span>](iamtimeline-isdirty.md)                             | <span data-ttu-id="34c01-160">不支援。</span><span class="sxs-lookup"><span data-stu-id="34c01-160">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="34c01-161">**RemGroupFromList**</span><span class="sxs-lookup"><span data-stu-id="34c01-161">**RemGroupFromList**</span></span>](iamtimeline-remgroupfromlist.md)           | <span data-ttu-id="34c01-162">不支援。</span><span class="sxs-lookup"><span data-stu-id="34c01-162">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="34c01-163">**SetDefaultEffect**</span><span class="sxs-lookup"><span data-stu-id="34c01-163">**SetDefaultEffect**</span></span>](iamtimeline-setdefaulteffect.md)           | <span data-ttu-id="34c01-164">設定預設效果。</span><span class="sxs-lookup"><span data-stu-id="34c01-164">Sets the default effect.</span></span><br/>                                                                                               |
| [<span data-ttu-id="34c01-165">**SetDefaultEffectB**</span><span class="sxs-lookup"><span data-stu-id="34c01-165">**SetDefaultEffectB**</span></span>](iamtimeline-setdefaulteffectb.md)         | <span data-ttu-id="34c01-166">將預設效果設定為 **BSTR** 值。</span><span class="sxs-lookup"><span data-stu-id="34c01-166">Sets the default effect as a **BSTR** value.</span></span><br/>                                                                           |
| [<span data-ttu-id="34c01-167">**SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="34c01-167">**SetDefaultFPS**</span></span>](iamtimeline-setdefaultfps.md)                 | <span data-ttu-id="34c01-168">設定預設輸出畫面播放速率（以每秒畫面格速率為單位）。</span><span class="sxs-lookup"><span data-stu-id="34c01-168">Sets the default output frame rate, in frames per second.</span></span><br/>                                                              |
| [<span data-ttu-id="34c01-169">**SetDefaultTransition**</span><span class="sxs-lookup"><span data-stu-id="34c01-169">**SetDefaultTransition**</span></span>](iamtimeline-setdefaulttransition.md)   | <span data-ttu-id="34c01-170">設定預設轉換。</span><span class="sxs-lookup"><span data-stu-id="34c01-170">Sets the default transition.</span></span><br/>                                                                                           |
| [<span data-ttu-id="34c01-171">**SetDefaultTransitionB**</span><span class="sxs-lookup"><span data-stu-id="34c01-171">**SetDefaultTransitionB**</span></span>](iamtimeline-setdefaulttransitionb.md) | <span data-ttu-id="34c01-172">將預設轉換設定為 BSTR 值。</span><span class="sxs-lookup"><span data-stu-id="34c01-172">Sets the default transition as a BSTR value.</span></span><br/>                                                                           |
| [<span data-ttu-id="34c01-173">**SetInsertMode**</span><span class="sxs-lookup"><span data-stu-id="34c01-173">**SetInsertMode**</span></span>](iamtimeline-setinsertmode.md)                 | <span data-ttu-id="34c01-174">未實作。</span><span class="sxs-lookup"><span data-stu-id="34c01-174">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="34c01-175">**SetInterestRange**</span><span class="sxs-lookup"><span data-stu-id="34c01-175">**SetInterestRange**</span></span>](iamtimeline-setinterestrange.md)           | <span data-ttu-id="34c01-176">未實作。</span><span class="sxs-lookup"><span data-stu-id="34c01-176">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="34c01-177">**TransitionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="34c01-177">**TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)       | <span data-ttu-id="34c01-178">決定是否啟用轉換。</span><span class="sxs-lookup"><span data-stu-id="34c01-178">Determines whether transitions are enabled.</span></span><br/>                                                                            |
| [<span data-ttu-id="34c01-179">**ValidateSourceNames**</span><span class="sxs-lookup"><span data-stu-id="34c01-179">**ValidateSourceNames**</span></span>](iamtimeline-validatesourcenames.md)     | <span data-ttu-id="34c01-180">驗證時間軸中的來源名稱。</span><span class="sxs-lookup"><span data-stu-id="34c01-180">Validates source names in the timeline.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="34c01-181">備註</span><span class="sxs-lookup"><span data-stu-id="34c01-181">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="34c01-182">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="34c01-182">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="34c01-183">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="34c01-183">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="34c01-184">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="34c01-184">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="34c01-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="34c01-185">Requirements</span></span>



| <span data-ttu-id="34c01-186">需求</span><span class="sxs-lookup"><span data-stu-id="34c01-186">Requirement</span></span> | <span data-ttu-id="34c01-187">值</span><span class="sxs-lookup"><span data-stu-id="34c01-187">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34c01-188">標頭</span><span class="sxs-lookup"><span data-stu-id="34c01-188">Header</span></span><br/>  | <dl> <span data-ttu-id="34c01-189"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="34c01-189"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="34c01-190">程式庫</span><span class="sxs-lookup"><span data-stu-id="34c01-190">Library</span></span><br/> | <dl> <span data-ttu-id="34c01-191"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="34c01-191"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
