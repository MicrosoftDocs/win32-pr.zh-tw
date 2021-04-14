---
description: 這是使用者執行的介面，可讓使用者從效果設定裝置狀態。
ms.assetid: ccd3e456-e27b-4128-b20b-99ff8dafcbe1
title: 'ID3DXEffectStateManager 介面 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fad9df739634625800c0a21fd9ba2a2823d70f8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323068"
---
# <a name="id3dxeffectstatemanager-interface"></a><span data-ttu-id="cff3a-103">ID3DXEffectStateManager 介面</span><span class="sxs-lookup"><span data-stu-id="cff3a-103">ID3DXEffectStateManager interface</span></span>

<span data-ttu-id="cff3a-104">這是使用者執行的介面，可讓使用者從效果設定裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="cff3a-104">This is a user-implemented interface that allows a user to set the device state from an effect.</span></span> <span data-ttu-id="cff3a-105">這個介面中的每個方法都必須由使用者執行，然後在發生下列任何一種情況時，用來作為應用程式的回呼：</span><span class="sxs-lookup"><span data-stu-id="cff3a-105">Each of the methods in this interface must be implemented by the user and will then be used as callbacks to the application when either of the following occur:</span></span>

-   <span data-ttu-id="cff3a-106">效果會呼叫 [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)。</span><span class="sxs-lookup"><span data-stu-id="cff3a-106">An effect calls [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="cff3a-107">藉由呼叫適當的狀態變更 API 來動態更新效果狀態。</span><span class="sxs-lookup"><span data-stu-id="cff3a-107">Effect state is dynamically updated by calling the appropriate state change API.</span></span> <span data-ttu-id="cff3a-108">請參閱個別的方法頁面以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cff3a-108">See individual method pages for details.</span></span>

<span data-ttu-id="cff3a-109">當應用程式使用狀態管理員來執行自訂回呼時，在呼叫 [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md) 和 [**ID3DXEffect：： EndPass**](id3dxeffect--endpass.md)時，效果不會再自動儲存和還原狀態。</span><span class="sxs-lookup"><span data-stu-id="cff3a-109">When an application uses the state manager to implement custom callbacks, an effect no longer automatically saves and restores state when calling [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md).</span></span> <span data-ttu-id="cff3a-110">因為應用程式已在回呼中執行自訂的儲存和還原行為，所以會略過這項自動行為。</span><span class="sxs-lookup"><span data-stu-id="cff3a-110">Because the application has implemented a custom save and restore behavior in the callbacks, this automatic behavior is bypassed.</span></span>

## <a name="members"></a><span data-ttu-id="cff3a-111">成員</span><span class="sxs-lookup"><span data-stu-id="cff3a-111">Members</span></span>

<span data-ttu-id="cff3a-112">**ID3DXEffectStateManager** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="cff3a-112">The **ID3DXEffectStateManager** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cff3a-113">**ID3DXEffectStateManager** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cff3a-113">**ID3DXEffectStateManager** also has these types of members:</span></span>

-   [<span data-ttu-id="cff3a-114">方法</span><span class="sxs-lookup"><span data-stu-id="cff3a-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cff3a-115">方法</span><span class="sxs-lookup"><span data-stu-id="cff3a-115">Methods</span></span>

<span data-ttu-id="cff3a-116">**ID3DXEffectStateManager** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="cff3a-116">The **ID3DXEffectStateManager** interface has these methods.</span></span>



| <span data-ttu-id="cff3a-117">方法</span><span class="sxs-lookup"><span data-stu-id="cff3a-117">Method</span></span>                                                                                | <span data-ttu-id="cff3a-118">描述</span><span class="sxs-lookup"><span data-stu-id="cff3a-118">Description</span></span>                                                                                                                  |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cff3a-119">**LightEnable**</span><span class="sxs-lookup"><span data-stu-id="cff3a-119">**LightEnable**</span></span>](id3dxeffectstatemanager--lightenable.md)                           | <span data-ttu-id="cff3a-120">必須由使用者執行以啟用/停用燈光的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="cff3a-120">A callback function that must be implemented by a user to enable/disable a light.</span></span><br/>                                 |
| [<span data-ttu-id="cff3a-121">**SetFVF**</span><span class="sxs-lookup"><span data-stu-id="cff3a-121">**SetFVF**</span></span>](id3dxeffectstatemanager--setfvf.md)                                     | <span data-ttu-id="cff3a-122">必須由使用者執行來設定 FVF 程式碼的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="cff3a-122">A callback function that must be implemented by a user to set a FVF code.</span></span><br/>                                         |
| [<span data-ttu-id="cff3a-123">**SetLight**</span><span class="sxs-lookup"><span data-stu-id="cff3a-123">**SetLight**</span></span>](id3dxeffectstatemanager--setlight.md)                                 | <span data-ttu-id="cff3a-124">必須由使用者執行以設定燈光的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="cff3a-124">A callback function that must be implemented by a user to set a light.</span></span><br/>                                            |
| [<span data-ttu-id="cff3a-125">**SetMaterial**</span><span class="sxs-lookup"><span data-stu-id="cff3a-125">**SetMaterial**</span></span>](id3dxeffectstatemanager--setmaterial.md)                           | <span data-ttu-id="cff3a-126">必須由使用者執行以設定材質狀態的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="cff3a-126">A callback function that must be implemented by a user to set material state.</span></span><br/>                                     |
| [<span data-ttu-id="cff3a-127">**SetNPatchMode**</span><span class="sxs-lookup"><span data-stu-id="cff3a-127">**SetNPatchMode**</span></span>](id3dxeffectstatemanager--setnpatchmode.md)                       | <span data-ttu-id="cff3a-128">必須由使用者執行的回呼函式，以設定 N 個修補程式的細分區段數目。</span><span class="sxs-lookup"><span data-stu-id="cff3a-128">A callback function that must be implemented by a user to set the number of subdivision segments for N-patches.</span></span><br/>   |
| [<span data-ttu-id="cff3a-129">**SetPixelShader**</span><span class="sxs-lookup"><span data-stu-id="cff3a-129">**SetPixelShader**</span></span>](id3dxeffectstatemanager--setpixelshader.md)                     | <span data-ttu-id="cff3a-130">必須由使用者執行以設定圖元著色器的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="cff3a-130">A callback function that must be implemented by a user to set a pixel shader.</span></span><br/>                                     |
| [<span data-ttu-id="cff3a-131">**SetPixelShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="cff3a-131">**SetPixelShaderConstantB**</span></span>](id3dxeffectstatemanager--setpixelshaderconstantb.md)   | <span data-ttu-id="cff3a-132">必須由使用者所執行的回呼函式，以設定頂點著色器布林值常數的陣列。</span><span class="sxs-lookup"><span data-stu-id="cff3a-132">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span><br/>        |
| [<span data-ttu-id="cff3a-133">**SetPixelShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="cff3a-133">**SetPixelShaderConstantF**</span></span>](id3dxeffectstatemanager--setpixelshaderconstantf.md)   | <span data-ttu-id="cff3a-134">必須由使用者所執行的回呼函式，以設定頂點著色器浮點數常數的陣列。</span><span class="sxs-lookup"><span data-stu-id="cff3a-134">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span><br/> |
| [<span data-ttu-id="cff3a-135">**SetPixelShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="cff3a-135">**SetPixelShaderConstantI**</span></span>](id3dxeffectstatemanager--setpixelshaderconstanti.md)   | <span data-ttu-id="cff3a-136">必須由使用者所執行的回呼函式，以設定頂點著色器整數常數的陣列。</span><span class="sxs-lookup"><span data-stu-id="cff3a-136">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span><br/>        |
| [<span data-ttu-id="cff3a-137">**Graphicsdevice**</span><span class="sxs-lookup"><span data-stu-id="cff3a-137">**SetRenderState**</span></span>](id3dxeffectstatemanager--setrenderstate.md)                     | <span data-ttu-id="cff3a-138">必須由使用者執行來設定轉譯狀態的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="cff3a-138">A callback function that must be implemented by a user to set render state.</span></span><br/>                                       |
| [<span data-ttu-id="cff3a-139">**SetSamplerState**</span><span class="sxs-lookup"><span data-stu-id="cff3a-139">**SetSamplerState**</span></span>](id3dxeffectstatemanager--setsamplerstate.md)                   | <span data-ttu-id="cff3a-140">必須由使用者所執行的回呼函式，以設定取樣器。</span><span class="sxs-lookup"><span data-stu-id="cff3a-140">A callback function that must be implemented by a user to set a sampler.</span></span><br/>                                          |
| [<span data-ttu-id="cff3a-141">**SetTexture**</span><span class="sxs-lookup"><span data-stu-id="cff3a-141">**SetTexture**</span></span>](id3dxeffectstatemanager--settexture.md)                             | <span data-ttu-id="cff3a-142">必須由使用者執行以設定材質的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="cff3a-142">A callback function that must be implemented by a user to set a texture.</span></span><br/>                                          |
| [<span data-ttu-id="cff3a-143">**SetTextureStageState**</span><span class="sxs-lookup"><span data-stu-id="cff3a-143">**SetTextureStageState**</span></span>](id3dxeffectstatemanager--settexturestagestate.md)         | <span data-ttu-id="cff3a-144">必須由使用者執行以設定材質階段狀態的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="cff3a-144">A callback function that must be implemented by a user to set the texture stage state.</span></span><br/>                            |
| [<span data-ttu-id="cff3a-145">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="cff3a-145">**SetTransform**</span></span>](id3dxeffectstatemanager--settransform.md)                         | <span data-ttu-id="cff3a-146">必須由使用者執行以設定轉換的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="cff3a-146">A callback function that must be implemented by a user to set a transform.</span></span><br/>                                        |
| [<span data-ttu-id="cff3a-147">**SetVertexShader**</span><span class="sxs-lookup"><span data-stu-id="cff3a-147">**SetVertexShader**</span></span>](id3dxeffectstatemanager--setvertexshader.md)                   | <span data-ttu-id="cff3a-148">必須由使用者執行以設定頂點著色器的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="cff3a-148">A callback function that must be implemented by a user to set a vertex shader.</span></span><br/>                                    |
| [<span data-ttu-id="cff3a-149">**SetVertexShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="cff3a-149">**SetVertexShaderConstantB**</span></span>](id3dxeffectstatemanager--setvertexshaderconstantb.md) | <span data-ttu-id="cff3a-150">必須由使用者所執行的回呼函式，以設定頂點著色器布林值常數的陣列。</span><span class="sxs-lookup"><span data-stu-id="cff3a-150">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span><br/>        |
| [<span data-ttu-id="cff3a-151">**SetVertexShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="cff3a-151">**SetVertexShaderConstantF**</span></span>](id3dxeffectstatemanager--setvertexshaderconstantf.md) | <span data-ttu-id="cff3a-152">必須由使用者所執行的回呼函式，以設定頂點著色器浮點數常數的陣列。</span><span class="sxs-lookup"><span data-stu-id="cff3a-152">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span><br/> |
| [<span data-ttu-id="cff3a-153">**SetVertexShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="cff3a-153">**SetVertexShaderConstantI**</span></span>](id3dxeffectstatemanager--setvertexshaderconstanti.md) | <span data-ttu-id="cff3a-154">必須由使用者所執行的回呼函式，以設定頂點著色器整數常數的陣列。</span><span class="sxs-lookup"><span data-stu-id="cff3a-154">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="cff3a-155">備註</span><span class="sxs-lookup"><span data-stu-id="cff3a-155">Remarks</span></span>

<span data-ttu-id="cff3a-156">使用者藉由實作為衍生自這個介面的類別，以及執行所有介面方法，來建立 ID3DXEffectStateManager 介面。</span><span class="sxs-lookup"><span data-stu-id="cff3a-156">A user creates an ID3DXEffectStateManager interface by implementing a class that derives from this interface, and implementing all the interface methods.</span></span> <span data-ttu-id="cff3a-157">建立介面之後，您可以使用 [**ID3DXEffect：： GetStateManager**](id3dxeffect--getstatemanager.md) 和 [**ID3DXEffect：： SetStateManager**](id3dxeffect--setstatemanager.md)，取得或設定效果內的狀態管理員。</span><span class="sxs-lookup"><span data-stu-id="cff3a-157">Once the interface is created, you can get or set the state manager within an effect using [**ID3DXEffect::GetStateManager**](id3dxeffect--getstatemanager.md) and [**ID3DXEffect::SetStateManager**](id3dxeffect--setstatemanager.md).</span></span>

<span data-ttu-id="cff3a-158">LPD3DXEFFECTSTATEMANAGER 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="cff3a-158">The LPD3DXEFFECTSTATEMANAGER type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectStateManager ID3DXEffectStateManager;
typedef interface ID3DXEffectStateManager *LPD3DXEFFECTSTATEMANAGER;
```



## <a name="requirements"></a><span data-ttu-id="cff3a-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="cff3a-159">Requirements</span></span>



| <span data-ttu-id="cff3a-160">需求</span><span class="sxs-lookup"><span data-stu-id="cff3a-160">Requirement</span></span> | <span data-ttu-id="cff3a-161">值</span><span class="sxs-lookup"><span data-stu-id="cff3a-161">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cff3a-162">標頭</span><span class="sxs-lookup"><span data-stu-id="cff3a-162">Header</span></span><br/>  | <dl> <span data-ttu-id="cff3a-163"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="cff3a-163"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="cff3a-164">程式庫</span><span class="sxs-lookup"><span data-stu-id="cff3a-164">Library</span></span><br/> | <dl> <span data-ttu-id="cff3a-165"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cff3a-165"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cff3a-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cff3a-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cff3a-167">效果介面</span><span class="sxs-lookup"><span data-stu-id="cff3a-167">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
