---
description: 用來設定和查詢效果，以及選擇技術。 效果物件可以包含多個技術來呈現相同的效果。
ms.assetid: bffc64ab-12e7-44e9-b296-262b0459a68a
title: 'ID3DXEffect 介面 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 275376234739964940d70381a34331ff5b89f2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986082"
---
# <a name="id3dxeffect-interface"></a><span data-ttu-id="9e87f-104">ID3DXEffect 介面</span><span class="sxs-lookup"><span data-stu-id="9e87f-104">ID3DXEffect interface</span></span>

<span data-ttu-id="9e87f-105">用來設定和查詢效果，以及選擇技術。</span><span class="sxs-lookup"><span data-stu-id="9e87f-105">Used to set and query effects, and to choose techniques.</span></span> <span data-ttu-id="9e87f-106">效果物件可以包含多個技術來呈現相同的效果。</span><span class="sxs-lookup"><span data-stu-id="9e87f-106">An effect object can contain multiple techniques to render the same effect.</span></span>

## <a name="members"></a><span data-ttu-id="9e87f-107">成員</span><span class="sxs-lookup"><span data-stu-id="9e87f-107">Members</span></span>

<span data-ttu-id="9e87f-108">**ID3DXEffect** 介面繼承自 [**ID3DXBaseEffect**](id3dxbaseeffect.md)。</span><span class="sxs-lookup"><span data-stu-id="9e87f-108">The **ID3DXEffect** interface inherits from [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span> <span data-ttu-id="9e87f-109">**ID3DXEffect** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9e87f-109">**ID3DXEffect** also has these types of members:</span></span>

-   [<span data-ttu-id="9e87f-110">方法</span><span class="sxs-lookup"><span data-stu-id="9e87f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9e87f-111">方法</span><span class="sxs-lookup"><span data-stu-id="9e87f-111">Methods</span></span>

<span data-ttu-id="9e87f-112">**ID3DXEffect** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9e87f-112">The **ID3DXEffect** interface has these methods.</span></span>



| <span data-ttu-id="9e87f-113">方法</span><span class="sxs-lookup"><span data-stu-id="9e87f-113">Method</span></span>                                                                | <span data-ttu-id="9e87f-114">描述</span><span class="sxs-lookup"><span data-stu-id="9e87f-114">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e87f-115">**ApplyParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="9e87f-115">**ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)       | <span data-ttu-id="9e87f-116">將狀態欄塊中的值套用至目前的效果系統狀態。</span><span class="sxs-lookup"><span data-stu-id="9e87f-116">Apply the values in a state block to the current effect system state.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="9e87f-117">**開始**</span><span class="sxs-lookup"><span data-stu-id="9e87f-117">**Begin**</span></span>](id3dxeffect--begin.md)                                   | <span data-ttu-id="9e87f-118">啟動使用中的技術。</span><span class="sxs-lookup"><span data-stu-id="9e87f-118">Starts an active technique.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="9e87f-119">**BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="9e87f-119">**BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)       | <span data-ttu-id="9e87f-120">開始在參數區塊中捕捉狀態變更。</span><span class="sxs-lookup"><span data-stu-id="9e87f-120">Start capturing state changes in a parameter block.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="9e87f-121">**BeginPass**</span><span class="sxs-lookup"><span data-stu-id="9e87f-121">**BeginPass**</span></span>](id3dxeffect--beginpass.md)                           | <span data-ttu-id="9e87f-122">在主動技術內開始進行。</span><span class="sxs-lookup"><span data-stu-id="9e87f-122">Begins a pass, within the active technique.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="9e87f-123">**CloneEffect**</span><span class="sxs-lookup"><span data-stu-id="9e87f-123">**CloneEffect**</span></span>](id3dxeffect--cloneeffect.md)                       | <span data-ttu-id="9e87f-124">建立效果的複本。</span><span class="sxs-lookup"><span data-stu-id="9e87f-124">Creates a copy of an effect.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="9e87f-125">**CommitChanges**</span><span class="sxs-lookup"><span data-stu-id="9e87f-125">**CommitChanges**</span></span>](id3dxeffect--commitchanges.md)                   | <span data-ttu-id="9e87f-126">在轉譯之前，將作用中傳遞內發生的狀態變更傳播至裝置。</span><span class="sxs-lookup"><span data-stu-id="9e87f-126">Propagate state changes that occur inside of an active pass to the device before rendering.</span></span><br/>                                                                                           |
| [<span data-ttu-id="9e87f-127">**DeleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="9e87f-127">**DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)     | <span data-ttu-id="9e87f-128">刪除參數區塊。</span><span class="sxs-lookup"><span data-stu-id="9e87f-128">Delete a parameter block.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="9e87f-129">**結束**</span><span class="sxs-lookup"><span data-stu-id="9e87f-129">**End**</span></span>](id3dxeffect--end.md)                                       | <span data-ttu-id="9e87f-130">結束使用中的技術。</span><span class="sxs-lookup"><span data-stu-id="9e87f-130">Ends an active technique.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="9e87f-131">**EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="9e87f-131">**EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)           | <span data-ttu-id="9e87f-132">停止捕獲效果參數狀態變更。</span><span class="sxs-lookup"><span data-stu-id="9e87f-132">Stop capturing effect parameter state changes.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="9e87f-133">**EndPass**</span><span class="sxs-lookup"><span data-stu-id="9e87f-133">**EndPass**</span></span>](id3dxeffect--endpass.md)                               | <span data-ttu-id="9e87f-134">結束主動傳遞。</span><span class="sxs-lookup"><span data-stu-id="9e87f-134">End an active pass.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="9e87f-135">**FindNextValidTechnique**</span><span class="sxs-lookup"><span data-stu-id="9e87f-135">**FindNextValidTechnique**</span></span>](id3dxeffect--findnextvalidtechnique.md) | <span data-ttu-id="9e87f-136">搜尋下一個有效的技巧，從指定技術之後的技巧開始。</span><span class="sxs-lookup"><span data-stu-id="9e87f-136">Searches for the next valid technique, starting at the technique after the specified technique.</span></span><br/>                                                                                       |
| [<span data-ttu-id="9e87f-137">**GetCurrentTechnique**</span><span class="sxs-lookup"><span data-stu-id="9e87f-137">**GetCurrentTechnique**</span></span>](id3dxeffect--getcurrenttechnique.md)       | <span data-ttu-id="9e87f-138">取得目前的技巧。</span><span class="sxs-lookup"><span data-stu-id="9e87f-138">Gets the current technique.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="9e87f-139">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="9e87f-139">**GetDevice**</span></span>](id3dxeffect--getdevice.md)                           | <span data-ttu-id="9e87f-140">捕獲與效果相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="9e87f-140">Retrieves the device associated with the effect.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="9e87f-141">**>pooloperations.getpool**</span><span class="sxs-lookup"><span data-stu-id="9e87f-141">**GetPool**</span></span>](id3dxeffect--getpool.md)                               | <span data-ttu-id="9e87f-142">取得共用參數集區的指標。</span><span class="sxs-lookup"><span data-stu-id="9e87f-142">Gets a pointer to the pool of shared parameters.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="9e87f-143">**GetStateManager**</span><span class="sxs-lookup"><span data-stu-id="9e87f-143">**GetStateManager**</span></span>](id3dxeffect--getstatemanager.md)               | <span data-ttu-id="9e87f-144">取得效果狀態管理員。</span><span class="sxs-lookup"><span data-stu-id="9e87f-144">Get the effect state manager.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="9e87f-145">**IsParameterUsed**</span><span class="sxs-lookup"><span data-stu-id="9e87f-145">**IsParameterUsed**</span></span>](id3dxeffect--isparameterused.md)               | <span data-ttu-id="9e87f-146">判斷技術是否使用參數。</span><span class="sxs-lookup"><span data-stu-id="9e87f-146">Determines if a parameter is used by the technique.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="9e87f-147">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="9e87f-147">**OnLostDevice**</span></span>](id3dxeffect--onlostdevice.md)                     | <span data-ttu-id="9e87f-148">您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。</span><span class="sxs-lookup"><span data-stu-id="9e87f-148">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="9e87f-149">只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="9e87f-149">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="9e87f-150">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="9e87f-150">**OnResetDevice**</span></span>](id3dxeffect--onresetdevice.md)                   | <span data-ttu-id="9e87f-151">您可以使用這個方法來重新取得資源，並儲存初始狀態。</span><span class="sxs-lookup"><span data-stu-id="9e87f-151">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="9e87f-152">**SetRawValue**</span><span class="sxs-lookup"><span data-stu-id="9e87f-152">**SetRawValue**</span></span>](id3dxeffect--setrawvalue.md)                       | <span data-ttu-id="9e87f-153">使用記憶體複製來設定著色器常數的連續範圍。</span><span class="sxs-lookup"><span data-stu-id="9e87f-153">Set a contiguous range of shader constants with a memory copy.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="9e87f-154">**SetStateManager**</span><span class="sxs-lookup"><span data-stu-id="9e87f-154">**SetStateManager**</span></span>](id3dxeffect--setstatemanager.md)               | <span data-ttu-id="9e87f-155">設定效果狀態管理員。</span><span class="sxs-lookup"><span data-stu-id="9e87f-155">Set the effect state manager.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="9e87f-156">**SetTechnique**</span><span class="sxs-lookup"><span data-stu-id="9e87f-156">**SetTechnique**</span></span>](id3dxeffect--settechnique.md)                     | <span data-ttu-id="9e87f-157">設定使用中的技術。</span><span class="sxs-lookup"><span data-stu-id="9e87f-157">Sets the active technique.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="9e87f-158">**ValidateTechnique**</span><span class="sxs-lookup"><span data-stu-id="9e87f-158">**ValidateTechnique**</span></span>](id3dxeffect--validatetechnique.md)           | <span data-ttu-id="9e87f-159">驗證技巧。</span><span class="sxs-lookup"><span data-stu-id="9e87f-159">Validate a technique.</span></span><br/>                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="9e87f-160">備註</span><span class="sxs-lookup"><span data-stu-id="9e87f-160">Remarks</span></span>

<span data-ttu-id="9e87f-161">ID3DXEffect 介面的取得方式是呼叫 [**D3DXCreateEffect**](d3dxcreateeffect.md)、 [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)或 [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)。</span><span class="sxs-lookup"><span data-stu-id="9e87f-161">The ID3DXEffect interface is obtained by calling [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md), or [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md).</span></span>

<span data-ttu-id="9e87f-162">LPD3DXEFFECT 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9e87f-162">The LPD3DXEFFECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffect ID3DXEffect;
typedef interface ID3DXEffect *LPD3DXEFFECT;
```



## <a name="requirements"></a><span data-ttu-id="9e87f-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e87f-163">Requirements</span></span>



| <span data-ttu-id="9e87f-164">需求</span><span class="sxs-lookup"><span data-stu-id="9e87f-164">Requirement</span></span> | <span data-ttu-id="9e87f-165">值</span><span class="sxs-lookup"><span data-stu-id="9e87f-165">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e87f-166">標頭</span><span class="sxs-lookup"><span data-stu-id="9e87f-166">Header</span></span><br/>  | <dl> <span data-ttu-id="9e87f-167"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="9e87f-167"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="9e87f-168">程式庫</span><span class="sxs-lookup"><span data-stu-id="9e87f-168">Library</span></span><br/> | <dl> <span data-ttu-id="9e87f-169"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e87f-169"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9e87f-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e87f-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e87f-171">**ID3DXBaseEffect**</span><span class="sxs-lookup"><span data-stu-id="9e87f-171">**ID3DXBaseEffect**</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="9e87f-172">效果介面</span><span class="sxs-lookup"><span data-stu-id="9e87f-172">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[<span data-ttu-id="9e87f-173">**D3DXCreateEffect**</span><span class="sxs-lookup"><span data-stu-id="9e87f-173">**D3DXCreateEffect**</span></span>](d3dxcreateeffect.md)
</dt> <dt>

[<span data-ttu-id="9e87f-174">**D3DXCreateEffectFromFile**</span><span class="sxs-lookup"><span data-stu-id="9e87f-174">**D3DXCreateEffectFromFile**</span></span>](d3dxcreateeffectfromfile.md)
</dt> <dt>

[<span data-ttu-id="9e87f-175">**D3DXCreateEffectFromResource**</span><span class="sxs-lookup"><span data-stu-id="9e87f-175">**D3DXCreateEffectFromResource**</span></span>](d3dxcreateeffectfromresource.md)
</dt> </dl>

 

 




