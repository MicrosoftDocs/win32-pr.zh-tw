---
description: 建立空白 cube 材質，視需要調整呼叫參數。
ms.assetid: 96cf3fc1-9efc-4b97-a082-2956386145c7
title: 'D3DXCreateCubeTexture 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8fa31945cea5e65cdf00eae512059308090bcbab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989220"
---
# <a name="d3dxcreatecubetexture-function"></a><span data-ttu-id="8c0f9-103">D3DXCreateCubeTexture 函式</span><span class="sxs-lookup"><span data-stu-id="8c0f9-103">D3DXCreateCubeTexture function</span></span>

<span data-ttu-id="8c0f9-104">建立空白 cube 材質，視需要調整呼叫參數。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-104">Creates an empty cube texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c0f9-105">語法</span><span class="sxs-lookup"><span data-stu-id="8c0f9-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTexture(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="8c0f9-106">參數</span><span class="sxs-lookup"><span data-stu-id="8c0f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c0f9-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c0f9-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c0f9-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="8c0f9-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="8c0f9-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="8c0f9-110">*大小* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c0f9-110">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c0f9-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c0f9-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c0f9-112">立方體材質的寬度和高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-112">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="8c0f9-113">例如，如果 cube 材質是8圖元 x 8 圖元的 cube，此參數的值應該是8。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-113">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span>

</dd> <dt>

<span data-ttu-id="8c0f9-114">*MipLevels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c0f9-114">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c0f9-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c0f9-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c0f9-116">要求的 mip 層級數目。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-116">Number of mip levels requested.</span></span> <span data-ttu-id="8c0f9-117">如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-117">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="8c0f9-118">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="8c0f9-118">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c0f9-119">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c0f9-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c0f9-120">0、D3DUSAGE \_ RENDERTARGET 或 D3DUSAGE \_ DYNAMIC。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-120">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="8c0f9-121">將此旗標設定為 D3DUSAGE \_ RENDERTARGET 表示介面要當做轉譯目標使用。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-121">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="8c0f9-122">然後，您可以將資源傳遞給 [**SetRenderTarget**](/windows/desktop/api)方法的 *pNewRenderTarget* 參數。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-122">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="8c0f9-123">如果指定了 D3DUSAGE \_ RENDERTARGET，應用程式應該藉由呼叫 [**CheckDeviceFormat**](/windows/desktop/api)來檢查裝置是否支援這項操作。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-123">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="8c0f9-124">如需使用動態紋理的詳細資訊，請參閱 [使用動態紋理](performance-optimizations.md)。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-124">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c0f9-125">*格式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c0f9-125">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c0f9-126">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="8c0f9-126">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="8c0f9-127">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述 cube 材質所要求的像素格式。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-127">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="8c0f9-128">傳回的 cube 材質可能與以 *格式* 指定的格式不同。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-128">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="8c0f9-129">應用程式應該檢查傳回的 cube 材質格式。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-129">Applications should check the format of the returned cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="8c0f9-130">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="8c0f9-130">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c0f9-131">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="8c0f9-131">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="8c0f9-132">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置 cube 材質的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-132">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="8c0f9-133">*ppCubeTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8c0f9-133">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c0f9-134">類型： **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="8c0f9-134">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="8c0f9-135">[**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)介面指標的位址，表示已建立的 cube 紋理物件。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-135">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c0f9-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c0f9-136">Return value</span></span>

<span data-ttu-id="8c0f9-137">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8c0f9-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8c0f9-138">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8c0f9-139">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c0f9-140">備註</span><span class="sxs-lookup"><span data-stu-id="8c0f9-140">Remarks</span></span>

<span data-ttu-id="8c0f9-141">Cube 紋理不同于其他表面，因為它們是表面的集合。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-141">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span>

<span data-ttu-id="8c0f9-142">就內部而言，D3DXCreateCubeTexture 會使用 [**D3DXCheckCubeTextureRequirements**](d3dxcheckcubetexturerequirements.md) 來調整呼叫參數。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-142">Internally, D3DXCreateCubeTexture uses [**D3DXCheckCubeTextureRequirements**](d3dxcheckcubetexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="8c0f9-143">因此，呼叫 D3DXCreateCubeTexture 通常會成功，因為對 [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) 的呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="8c0f9-143">Therefore, calls to D3DXCreateCubeTexture will often succeed where calls to [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) would fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c0f9-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c0f9-144">Requirements</span></span>



| <span data-ttu-id="8c0f9-145">需求</span><span class="sxs-lookup"><span data-stu-id="8c0f9-145">Requirement</span></span> | <span data-ttu-id="8c0f9-146">值</span><span class="sxs-lookup"><span data-stu-id="8c0f9-146">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c0f9-147">標頭</span><span class="sxs-lookup"><span data-stu-id="8c0f9-147">Header</span></span><br/>  | <dl> <span data-ttu-id="8c0f9-148"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c0f9-148"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="8c0f9-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="8c0f9-149">Library</span></span><br/> | <dl> <span data-ttu-id="8c0f9-150"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c0f9-150"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8c0f9-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c0f9-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c0f9-152">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="8c0f9-152">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
