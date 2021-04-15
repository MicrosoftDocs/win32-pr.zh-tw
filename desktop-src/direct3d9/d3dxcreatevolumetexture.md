---
description: 建立空的磁片區材質，視需要調整呼叫參數。
ms.assetid: 8fc515cd-2fb3-40c7-8192-a41d93ac1e99
title: 'D3DXCreateVolumeTexture 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 50baf125d2e5375bddb63a41a0d10ae063a57b78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946103"
---
# <a name="d3dxcreatevolumetexture-function"></a><span data-ttu-id="701b0-103">D3DXCreateVolumeTexture 函式</span><span class="sxs-lookup"><span data-stu-id="701b0-103">D3DXCreateVolumeTexture function</span></span>

<span data-ttu-id="701b0-104">建立空的磁片區材質，視需要調整呼叫參數。</span><span class="sxs-lookup"><span data-stu-id="701b0-104">Creates an empty volume texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="701b0-105">語法</span><span class="sxs-lookup"><span data-stu-id="701b0-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTexture(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  UINT                     Width,
  _In_  UINT                     Height,
  _In_  UINT                     Depth,
  _In_  UINT                     MipLevels,
  _In_  DWORD                    Usage,
  _In_  D3DFORMAT                Format,
  _In_  D3DPOOL                  Pool,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="701b0-106">參數</span><span class="sxs-lookup"><span data-stu-id="701b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="701b0-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="701b0-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="701b0-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="701b0-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="701b0-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與磁片區材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="701b0-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="701b0-110">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="701b0-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="701b0-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="701b0-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="701b0-112">寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="701b0-112">Width in pixels.</span></span> <span data-ttu-id="701b0-113">此值必須為非零。</span><span class="sxs-lookup"><span data-stu-id="701b0-113">This value must be nonzero.</span></span> <span data-ttu-id="701b0-114">驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。</span><span class="sxs-lookup"><span data-stu-id="701b0-114">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="701b0-115">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="701b0-115">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="701b0-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="701b0-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="701b0-117">高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="701b0-117">Height in pixels.</span></span> <span data-ttu-id="701b0-118">此值必須為非零。</span><span class="sxs-lookup"><span data-stu-id="701b0-118">This value must be nonzero.</span></span> <span data-ttu-id="701b0-119">驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。</span><span class="sxs-lookup"><span data-stu-id="701b0-119">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="701b0-120">*深度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="701b0-120">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="701b0-121">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="701b0-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="701b0-122">以圖元為單位的深度。</span><span class="sxs-lookup"><span data-stu-id="701b0-122">Depth in pixels.</span></span> <span data-ttu-id="701b0-123">此值必須為非零。</span><span class="sxs-lookup"><span data-stu-id="701b0-123">This value must be nonzero.</span></span> <span data-ttu-id="701b0-124">驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。</span><span class="sxs-lookup"><span data-stu-id="701b0-124">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="701b0-125">*MipLevels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="701b0-125">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="701b0-126">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="701b0-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="701b0-127">要求的 mip 層級數目。</span><span class="sxs-lookup"><span data-stu-id="701b0-127">Number of mip levels requested.</span></span> <span data-ttu-id="701b0-128">如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="701b0-128">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="701b0-129">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="701b0-129">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="701b0-130">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="701b0-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="701b0-131">0或 D3DUSAGE \_ 動態。</span><span class="sxs-lookup"><span data-stu-id="701b0-131">0 or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="701b0-132">如需使用動態紋理的詳細資訊，請參閱 [使用動態紋理](performance-optimizations.md)。</span><span class="sxs-lookup"><span data-stu-id="701b0-132">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="701b0-133">*格式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="701b0-133">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="701b0-134">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="701b0-134">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="701b0-135">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述磁片區材質所要求的像素格式。</span><span class="sxs-lookup"><span data-stu-id="701b0-135">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the volume texture.</span></span> <span data-ttu-id="701b0-136">傳回的磁片區材質可能與以格式指定的格式不同。</span><span class="sxs-lookup"><span data-stu-id="701b0-136">The returned volume texture might have a different format from that specified by Format.</span></span> <span data-ttu-id="701b0-137">應用程式應該檢查所傳回之磁片區材質的格式。</span><span class="sxs-lookup"><span data-stu-id="701b0-137">Applications should check the format of the returned volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="701b0-138">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="701b0-138">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="701b0-139">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="701b0-139">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="701b0-140">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置磁片區材質的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="701b0-140">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the volume texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="701b0-141">*ppVolumeTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="701b0-141">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="701b0-142">類型： **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="701b0-142">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="701b0-143">[**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)介面指標的位址，表示已建立的磁片區材質物件。</span><span class="sxs-lookup"><span data-stu-id="701b0-143">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created volume texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="701b0-144">傳回值</span><span class="sxs-lookup"><span data-stu-id="701b0-144">Return value</span></span>

<span data-ttu-id="701b0-145">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="701b0-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="701b0-146">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="701b0-146">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="701b0-147">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DERR \_ INVALIDCALL、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="701b0-147">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, E\_OUTOFMEMORY .</span></span>

## <a name="remarks"></a><span data-ttu-id="701b0-148">備註</span><span class="sxs-lookup"><span data-stu-id="701b0-148">Remarks</span></span>

<span data-ttu-id="701b0-149">就內部而言，D3DXCreateVolumeTexture 會使用 [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) 來調整呼叫參數。</span><span class="sxs-lookup"><span data-stu-id="701b0-149">Internally, D3DXCreateVolumeTexture uses [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="701b0-150">因此，呼叫 D3DXCreateVolumeTexture 通常會成功，因為對 [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) 的呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="701b0-150">Therefore, calls to D3DXCreateVolumeTexture will often succeed where calls to [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) would fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="701b0-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="701b0-151">Requirements</span></span>



| <span data-ttu-id="701b0-152">需求</span><span class="sxs-lookup"><span data-stu-id="701b0-152">Requirement</span></span> | <span data-ttu-id="701b0-153">值</span><span class="sxs-lookup"><span data-stu-id="701b0-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="701b0-154">標頭</span><span class="sxs-lookup"><span data-stu-id="701b0-154">Header</span></span><br/>  | <dl> <span data-ttu-id="701b0-155"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="701b0-155"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="701b0-156">程式庫</span><span class="sxs-lookup"><span data-stu-id="701b0-156">Library</span></span><br/> | <dl> <span data-ttu-id="701b0-157"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="701b0-157"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="701b0-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="701b0-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="701b0-159">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="701b0-159">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
