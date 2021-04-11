---
description: 從記憶體中的檔案建立 cube 紋理。 這是比 D3DXCreateCubeTextureFromFileInMemory 更先進的函式。
ms.assetid: 598016eb-9ea9-4dca-a297-5708a957da6a
title: 'D3DXCreateCubeTextureFromFileInMemoryEx 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7813d4532bbde18a5fc7fd7d1d090dc72eccd61f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035416"
---
# <a name="d3dxcreatecubetexturefromfileinmemoryex-function"></a><span data-ttu-id="351e5-104">D3DXCreateCubeTextureFromFileInMemoryEx 函式</span><span class="sxs-lookup"><span data-stu-id="351e5-104">D3DXCreateCubeTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="351e5-105">從記憶體中的檔案建立 cube 紋理。</span><span class="sxs-lookup"><span data-stu-id="351e5-105">Creates a cube texture from a file in memory.</span></span> <span data-ttu-id="351e5-106">這是比 [**D3DXCreateCubeTextureFromFileInMemory**](d3dxcreatecubetexturefromfileinmemory.md)更先進的函式。</span><span class="sxs-lookup"><span data-stu-id="351e5-106">This is a more advanced function than [**D3DXCreateCubeTextureFromFileInMemory**](d3dxcreatecubetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="351e5-107">語法</span><span class="sxs-lookup"><span data-stu-id="351e5-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    LPCVOID                pSrcData,
  _In_    UINT                   SrcDataSize,
  _In_    UINT                   Size,
  _In_    UINT                   MipLevels,
  _In_    DWORD                  Usage,
  _In_    D3DFORMAT              Format,
  _In_    D3DPOOL                Pool,
  _In_    DWORD                  Filter,
  _In_    DWORD                  MipFilter,
  _In_    D3DCOLOR               ColorKey,
  _Inout_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_   PALETTEENTRY           *pPalette,
  _Out_   LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="351e5-108">參數</span><span class="sxs-lookup"><span data-stu-id="351e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="351e5-109">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="351e5-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="351e5-110">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="351e5-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="351e5-111">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與 cube 材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="351e5-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="351e5-112">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="351e5-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="351e5-113">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="351e5-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="351e5-114">記憶體中要建立 cube 材質之檔案的指標。</span><span class="sxs-lookup"><span data-stu-id="351e5-114">Pointer to the file in memory from which to create the cube texture.</span></span> <span data-ttu-id="351e5-115">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="351e5-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="351e5-116">*SrcDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="351e5-116">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="351e5-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="351e5-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="351e5-118">檔案在記憶體中的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="351e5-118">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="351e5-119">*大小* \[在\]</span><span class="sxs-lookup"><span data-stu-id="351e5-119">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="351e5-120">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="351e5-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="351e5-121">寬度 (或高度) （以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="351e5-121">Width (or height) in pixels.</span></span> <span data-ttu-id="351e5-122">如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。</span><span class="sxs-lookup"><span data-stu-id="351e5-122">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="351e5-123">*MipLevels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="351e5-123">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="351e5-124">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="351e5-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="351e5-125">要求的 mip 層級數目。</span><span class="sxs-lookup"><span data-stu-id="351e5-125">Number of mip levels requested.</span></span> <span data-ttu-id="351e5-126">如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="351e5-126">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="351e5-127">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="351e5-127">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="351e5-128">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="351e5-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="351e5-129">0、D3DUSAGE \_ RENDERTARGET 或 D3DUSAGE \_ DYNAMIC。</span><span class="sxs-lookup"><span data-stu-id="351e5-129">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="351e5-130">將此旗標設定為 D3DUSAGE \_ RENDERTARGET 表示介面要當做轉譯目標使用。</span><span class="sxs-lookup"><span data-stu-id="351e5-130">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="351e5-131">然後，您可以將資源傳遞給 [**SetRenderTarget**](/windows/desktop/api)方法的 *pNewRenderTarget* 參數。</span><span class="sxs-lookup"><span data-stu-id="351e5-131">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="351e5-132">如果指定了 D3DUSAGE \_ RENDERTARGET，應用程式應該藉由呼叫 [**CheckDeviceFormat**](/windows/desktop/api)來檢查裝置是否支援這項操作。</span><span class="sxs-lookup"><span data-stu-id="351e5-132">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="351e5-133">如需使用動態紋理的詳細資訊，請參閱 [使用動態紋理](performance-optimizations.md)。</span><span class="sxs-lookup"><span data-stu-id="351e5-133">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="351e5-134">*格式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="351e5-134">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="351e5-135">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="351e5-135">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="351e5-136">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述 cube 材質所要求的像素格式。</span><span class="sxs-lookup"><span data-stu-id="351e5-136">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="351e5-137">傳回的材質可能與以 *格式* 指定的格式不同。</span><span class="sxs-lookup"><span data-stu-id="351e5-137">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="351e5-138">應用程式應該檢查傳回的材質格式。</span><span class="sxs-lookup"><span data-stu-id="351e5-138">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="351e5-139">如果 [D3DFMT \_ 未知](other-d3dx-constants.md)，就會從檔案中取得格式。</span><span class="sxs-lookup"><span data-stu-id="351e5-139">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="351e5-140">如果從檔案 D3DFMT \_ \_ ，格式會與檔案中的格式完全相同，而且如果這違反裝置功能，呼叫就會失敗。</span><span class="sxs-lookup"><span data-stu-id="351e5-140">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="351e5-141">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="351e5-141">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="351e5-142">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="351e5-142">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="351e5-143">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置 cube 材質的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="351e5-143">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="351e5-144">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="351e5-144">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="351e5-145">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="351e5-145">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="351e5-146">一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="351e5-146">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="351e5-147">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="351e5-147">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="351e5-148">*MipFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="351e5-148">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="351e5-149">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="351e5-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="351e5-150">一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="351e5-150">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="351e5-151">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選方塊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="351e5-151">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="351e5-152">此外，使用 bits 27-31 來指定當將 dds 材質載入至記憶體時， (從 mipmap 鏈頂端跳過的 mip 層級數目) 。這可讓您略過32層級。</span><span class="sxs-lookup"><span data-stu-id="351e5-152">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="351e5-153">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="351e5-153">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="351e5-154">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="351e5-154">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="351e5-155">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。</span><span class="sxs-lookup"><span data-stu-id="351e5-155">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="351e5-156">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="351e5-156">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="351e5-157">Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。</span><span class="sxs-lookup"><span data-stu-id="351e5-157">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="351e5-158">因此，若是不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="351e5-158">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="351e5-159">*pSrcInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="351e5-159">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="351e5-160">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="351e5-160">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="351e5-161">[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會以來源影像檔案中的資料描述來填滿，或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="351e5-161">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="351e5-162">*pPalette* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="351e5-162">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="351e5-163">類型： **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="351e5-163">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="351e5-164">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，代表要填入的256色調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="351e5-164">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span> <span data-ttu-id="351e5-165">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="351e5-165">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="351e5-166">*ppCubeTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="351e5-166">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="351e5-167">類型： **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="351e5-167">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="351e5-168">[**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)介面指標的位址，表示已建立的 cube 紋理物件。</span><span class="sxs-lookup"><span data-stu-id="351e5-168">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="351e5-169">傳回值</span><span class="sxs-lookup"><span data-stu-id="351e5-169">Return value</span></span>

<span data-ttu-id="351e5-170">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="351e5-170">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="351e5-171">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="351e5-171">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="351e5-172">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="351e5-172">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="351e5-173">備註</span><span class="sxs-lookup"><span data-stu-id="351e5-173">Remarks</span></span>

<span data-ttu-id="351e5-174">此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="351e5-174">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="351e5-175">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="351e5-175">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="351e5-176">Cube 紋理不同于其他表面，因為它們是表面的集合。</span><span class="sxs-lookup"><span data-stu-id="351e5-176">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="351e5-177">若要使用 cube 材質來呼叫 [**SetRenderTarget**](/windows/desktop/api) ，您必須使用 [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) 選取個別臉部，並將產生的介面傳遞至 **SetRenderTarget** 。</span><span class="sxs-lookup"><span data-stu-id="351e5-177">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget** .</span></span>

<span data-ttu-id="351e5-178">這個方法是設計用來載入儲存為 RT RCDATA 的影像檔 \_ ，這是應用程式定義的資源， (原始資料) 。</span><span class="sxs-lookup"><span data-stu-id="351e5-178">This method is designed to be used for loading image files stored as RT\_RCDATA, which is an application-defined resource (raw data).</span></span> <span data-ttu-id="351e5-179">否則，此方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="351e5-179">Otherwise this method will fail.</span></span>

<span data-ttu-id="351e5-180">如需 [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)的詳細資訊，請參閱 Platform SDK。</span><span class="sxs-lookup"><span data-stu-id="351e5-180">For details on [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="351e5-181">請注意，從 DirectX 8.0 起， **PALETTEENTRY** 結構的 peFlags 成員無法如 Platform SDK 中所述運作。</span><span class="sxs-lookup"><span data-stu-id="351e5-181">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="351e5-182">PeFlags 成員現在是8位調色盤格式的 Alpha 通道。</span><span class="sxs-lookup"><span data-stu-id="351e5-182">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="351e5-183">**D3DXCreateCubeTextureFromFileInMemoryEx** 會使用 DirectDraw 介面 (DDS) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="351e5-183">**D3DXCreateCubeTextureFromFileInMemoryEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="351e5-184">[DirectX 材質編輯器] (Dxtex.exe) 可讓您從其他檔案格式產生 cube 對應，並以 DDS 檔案格式儲存。</span><span class="sxs-lookup"><span data-stu-id="351e5-184">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="351e5-185">您可以從 DirectX SDK 取得 Dxtex.exe 並瞭解它的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="351e5-185">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="351e5-186">如需有關 DirectX SDK 的資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)。</span><span class="sxs-lookup"><span data-stu-id="351e5-186">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="351e5-187">在載入 dd 檔案時略過 mipmap 層級時，請使用 D3DX \_ SKIP \_ dds \_ MIP \_ 層級宏來產生 MipFilter 值。</span><span class="sxs-lookup"><span data-stu-id="351e5-187">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="351e5-188">此宏會接受要略過的層級數目和篩選準則類型，並傳回篩選值，然後將其傳遞至 MipFilter 參數。</span><span class="sxs-lookup"><span data-stu-id="351e5-188">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="351e5-189">規格需求</span><span class="sxs-lookup"><span data-stu-id="351e5-189">Requirements</span></span>



| <span data-ttu-id="351e5-190">需求</span><span class="sxs-lookup"><span data-stu-id="351e5-190">Requirement</span></span> | <span data-ttu-id="351e5-191">值</span><span class="sxs-lookup"><span data-stu-id="351e5-191">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="351e5-192">標頭</span><span class="sxs-lookup"><span data-stu-id="351e5-192">Header</span></span><br/>  | <dl> <span data-ttu-id="351e5-193"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="351e5-193"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="351e5-194">程式庫</span><span class="sxs-lookup"><span data-stu-id="351e5-194">Library</span></span><br/> | <dl> <span data-ttu-id="351e5-195"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="351e5-195"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="351e5-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="351e5-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="351e5-197">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="351e5-197">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
