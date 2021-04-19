---
description: 從檔案建立 cube 紋理。 這是比 D3DXCreateCubeTextureFromFile 更先進的函式。
ms.assetid: 77e64b33-9282-42fa-978c-a93fa9ba11fc
title: 'D3DXCreateCubeTextureFromFileEx 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b4f56ad3f8e314f7ceb5f4efb07562257efab5fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991488"
---
# <a name="d3dxcreatecubetexturefromfileex-function"></a><span data-ttu-id="47616-104">D3DXCreateCubeTextureFromFileEx 函式</span><span class="sxs-lookup"><span data-stu-id="47616-104">D3DXCreateCubeTextureFromFileEx function</span></span>

<span data-ttu-id="47616-105">從檔案建立 cube 紋理。</span><span class="sxs-lookup"><span data-stu-id="47616-105">Creates a cube texture from a file.</span></span> <span data-ttu-id="47616-106">這是比 [**D3DXCreateCubeTextureFromFile**](d3dxcreatecubetexturefromfile.md)更先進的函式。</span><span class="sxs-lookup"><span data-stu-id="47616-106">This is a more advanced function than [**D3DXCreateCubeTextureFromFile**](d3dxcreatecubetexturefromfile.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="47616-107">語法</span><span class="sxs-lookup"><span data-stu-id="47616-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileEx(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _In_  DWORD                  Filter,
  _In_  DWORD                  MipFilter,
  _In_  D3DCOLOR               ColorKey,
  _Out_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_ PALETTEENTRY           *pPalette,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="47616-108">參數</span><span class="sxs-lookup"><span data-stu-id="47616-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47616-109">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47616-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47616-110">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="47616-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="47616-111">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與 cube 材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="47616-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="47616-112">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47616-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47616-113">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47616-113">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47616-114">指定檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="47616-114">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="47616-115">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="47616-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="47616-116">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="47616-116">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="47616-117">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="47616-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="47616-118">*大小* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47616-118">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47616-119">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47616-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47616-120">立方體材質的寬度和高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="47616-120">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="47616-121">例如，如果 cube 材質是8圖元 x 8 圖元的 cube，此參數的值應該是8。</span><span class="sxs-lookup"><span data-stu-id="47616-121">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span> <span data-ttu-id="47616-122">如果這個值是0或 D3DX \_ 預設值，就會從檔案取得維度。</span><span class="sxs-lookup"><span data-stu-id="47616-122">If this value is 0 or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="47616-123">*MipLevels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47616-123">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47616-124">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47616-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47616-125">要求的 mip 層級數目。</span><span class="sxs-lookup"><span data-stu-id="47616-125">Number of mip levels requested.</span></span> <span data-ttu-id="47616-126">如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="47616-126">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="47616-127">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="47616-127">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47616-128">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47616-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47616-129">0或 D3DUSAGE \_ RENDERTARGET，或 D3DUSAGE \_ DYNAMIC。</span><span class="sxs-lookup"><span data-stu-id="47616-129">0 or D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="47616-130">將此旗標設定為 D3DUSAGE \_ RENDERTARGET 表示介面要當做轉譯目標使用。</span><span class="sxs-lookup"><span data-stu-id="47616-130">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="47616-131">然後，您可以將資源傳遞給 [**SetRenderTarget**](/windows/desktop/api)方法的 *pNewRenderTarget* 參數。</span><span class="sxs-lookup"><span data-stu-id="47616-131">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="47616-132">如果指定了 D3DUSAGE \_ RENDERTARGET，應用程式應該藉由呼叫 [**CheckDeviceFormat**](/windows/desktop/api)來檢查裝置是否支援這項操作。</span><span class="sxs-lookup"><span data-stu-id="47616-132">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="47616-133">D3DUSAGE \_ DYNAMIC 表示介面應該以動態方式處理。</span><span class="sxs-lookup"><span data-stu-id="47616-133">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="47616-134">如需使用動態紋理的詳細資訊，請參閱 [使用動態紋理](performance-optimizations.md)。</span><span class="sxs-lookup"><span data-stu-id="47616-134">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="47616-135">*格式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47616-135">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47616-136">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="47616-136">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="47616-137">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述 cube 材質所要求的像素格式。</span><span class="sxs-lookup"><span data-stu-id="47616-137">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="47616-138">傳回的 cube 材質可能與以 *格式* 指定的格式不同。</span><span class="sxs-lookup"><span data-stu-id="47616-138">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="47616-139">應用程式應該檢查傳回的 cube 材質格式。</span><span class="sxs-lookup"><span data-stu-id="47616-139">Applications should check the format of the returned cube texture.</span></span> <span data-ttu-id="47616-140">如果 [D3DFMT \_ 未知](other-d3dx-constants.md)，就會從檔案中取得格式。</span><span class="sxs-lookup"><span data-stu-id="47616-140">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="47616-141">如果從檔案 D3DFMT \_ \_ ，格式會與檔案中的格式完全相同，而且如果這違反裝置功能，呼叫就會失敗。</span><span class="sxs-lookup"><span data-stu-id="47616-141">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="47616-142">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="47616-142">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47616-143">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="47616-143">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="47616-144">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置 cube 材質的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="47616-144">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="47616-145">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47616-145">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47616-146">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47616-146">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47616-147">一或多個 [D3DX \_ 篩選準則](d3dx-filter.md) 常數的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="47616-147">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants, controlling how the image is filtered.</span></span> <span data-ttu-id="47616-148">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="47616-148">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="47616-149">*MipFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47616-149">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47616-150">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47616-150">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47616-151">一或多個 [D3DX \_ 篩選](d3dx-filter.md) 常數的組合，可控制如何篩選影像。</span><span class="sxs-lookup"><span data-stu-id="47616-151">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="47616-152">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選方塊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="47616-152">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="47616-153">此外，使用 bits 27-31 來指定當將 dds 材質載入至記憶體時， (從 mipmap 鏈頂端跳過的 mip 層級數目) 。這可讓您略過32層級。</span><span class="sxs-lookup"><span data-stu-id="47616-153">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="47616-154">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47616-154">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47616-155">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="47616-155">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="47616-156">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。</span><span class="sxs-lookup"><span data-stu-id="47616-156">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="47616-157">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="47616-157">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="47616-158">Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。</span><span class="sxs-lookup"><span data-stu-id="47616-158">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="47616-159">因此，若是不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="47616-159">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="47616-160">*pSrcInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="47616-160">*pSrcInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47616-161">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="47616-161">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="47616-162">[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會以來源影像檔案中的資料描述來填滿，或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="47616-162">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="47616-163">*pPalette* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="47616-163">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47616-164">類型： **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="47616-164">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="47616-165">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，代表要填入的256色調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="47616-165">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="47616-166">*ppCubeTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="47616-166">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47616-167">類型： **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="47616-167">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="47616-168">[**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)介面指標的位址，表示已建立的 cube 紋理物件。</span><span class="sxs-lookup"><span data-stu-id="47616-168">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47616-169">傳回值</span><span class="sxs-lookup"><span data-stu-id="47616-169">Return value</span></span>

<span data-ttu-id="47616-170">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="47616-170">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="47616-171">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="47616-171">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="47616-172">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="47616-172">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="47616-173">備註</span><span class="sxs-lookup"><span data-stu-id="47616-173">Remarks</span></span>

<span data-ttu-id="47616-174">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="47616-174">The compiler setting also determines the function version.</span></span> <span data-ttu-id="47616-175">如果已定義 Unicode，函式呼叫會解析為 **D3DXCreateCubeTextureFromFileExW**。</span><span class="sxs-lookup"><span data-stu-id="47616-175">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromFileExW**.</span></span> <span data-ttu-id="47616-176">否則，函式呼叫會解析為 **D3DXCreateCubeTextureFromFileExA** ，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="47616-176">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromFileExA** because ANSI strings are being used.</span></span>

<span data-ttu-id="47616-177">此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="47616-177">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="47616-178">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="47616-178">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="47616-179">Cube 紋理不同于其他表面，因為它們是表面的集合。</span><span class="sxs-lookup"><span data-stu-id="47616-179">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="47616-180">若要使用 cube 材質來呼叫 [**SetRenderTarget**](/windows/desktop/api) ，您必須使用 [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) 選取個別臉部，並將產生的介面傳遞至 **SetRenderTarget**。</span><span class="sxs-lookup"><span data-stu-id="47616-180">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

<span data-ttu-id="47616-181">**D3DXCreateCubeTextureFromFileEx** 會使用 DirectDraw 介面 (DDS) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="47616-181">**D3DXCreateCubeTextureFromFileEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="47616-182">[DirectX 材質編輯器] (Dxtex.exe) 可讓您從其他檔案格式產生 cube 對應，並以 DDS 檔案格式儲存。</span><span class="sxs-lookup"><span data-stu-id="47616-182">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="47616-183">您可以從 DirectX SDK 取得 Dxtex.exe 並瞭解它的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="47616-183">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="47616-184">如需有關 DirectX SDK 的資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)。</span><span class="sxs-lookup"><span data-stu-id="47616-184">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="47616-185">在載入 dd 檔案時略過 mipmap 層級時，請使用 D3DX \_ SKIP \_ dds \_ MIP \_ 層級宏來產生 MipFilter 值。</span><span class="sxs-lookup"><span data-stu-id="47616-185">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="47616-186">此宏會接受要略過的層級數目和篩選準則類型，並傳回篩選值，然後將其傳遞至 MipFilter 參數。</span><span class="sxs-lookup"><span data-stu-id="47616-186">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="47616-187">規格需求</span><span class="sxs-lookup"><span data-stu-id="47616-187">Requirements</span></span>



| <span data-ttu-id="47616-188">需求</span><span class="sxs-lookup"><span data-stu-id="47616-188">Requirement</span></span> | <span data-ttu-id="47616-189">值</span><span class="sxs-lookup"><span data-stu-id="47616-189">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47616-190">標頭</span><span class="sxs-lookup"><span data-stu-id="47616-190">Header</span></span><br/>  | <dl> <span data-ttu-id="47616-191"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="47616-191"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="47616-192">程式庫</span><span class="sxs-lookup"><span data-stu-id="47616-192">Library</span></span><br/> | <dl> <span data-ttu-id="47616-193"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="47616-193"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="47616-194">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47616-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47616-195">**D3DXCreateCubeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="47616-195">**D3DXCreateCubeTextureFromFile**</span></span>](d3dxcreatecubetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="47616-196">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="47616-196">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
