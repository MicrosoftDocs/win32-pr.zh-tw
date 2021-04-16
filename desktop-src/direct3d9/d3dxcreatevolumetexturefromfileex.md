---
description: 從檔案建立磁片區材質。
ms.assetid: fa11706a-83cc-4795-957d-6d0e1faf2a8f
title: 'D3DXCreateVolumeTextureFromFileEx 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4d63377394dc123defac565cd11a0d40324a28a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322936"
---
# <a name="d3dxcreatevolumetexturefromfileex-function"></a><span data-ttu-id="c3141-103">D3DXCreateVolumeTextureFromFileEx 函式</span><span class="sxs-lookup"><span data-stu-id="c3141-103">D3DXCreateVolumeTextureFromFileEx function</span></span>

<span data-ttu-id="c3141-104">從檔案建立磁片區材質。</span><span class="sxs-lookup"><span data-stu-id="c3141-104">Creates a volume texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3141-105">語法</span><span class="sxs-lookup"><span data-stu-id="c3141-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCTSTR                  pSrcFile,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
          D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="c3141-106">參數</span><span class="sxs-lookup"><span data-stu-id="c3141-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3141-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3141-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3141-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c3141-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c3141-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="c3141-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="c3141-110">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3141-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3141-111">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3141-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3141-112">指定檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="c3141-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="c3141-113">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="c3141-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="c3141-114">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="c3141-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="c3141-115">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="c3141-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c3141-116">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3141-116">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3141-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3141-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3141-118">寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="c3141-118">Width in pixels.</span></span> <span data-ttu-id="c3141-119">如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。</span><span class="sxs-lookup"><span data-stu-id="c3141-119">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="c3141-120">驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。</span><span class="sxs-lookup"><span data-stu-id="c3141-120">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="c3141-121">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3141-121">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3141-122">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3141-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3141-123">高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="c3141-123">Height, in pixels.</span></span> <span data-ttu-id="c3141-124">如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。</span><span class="sxs-lookup"><span data-stu-id="c3141-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="c3141-125">驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。</span><span class="sxs-lookup"><span data-stu-id="c3141-125">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="c3141-126">*深度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3141-126">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3141-127">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3141-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3141-128">深度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="c3141-128">Depth, in pixels.</span></span> <span data-ttu-id="c3141-129">如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。</span><span class="sxs-lookup"><span data-stu-id="c3141-129">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="c3141-130">驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。</span><span class="sxs-lookup"><span data-stu-id="c3141-130">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="c3141-131">*MipLevels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3141-131">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3141-132">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3141-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3141-133">要求的 mip 層級數目。</span><span class="sxs-lookup"><span data-stu-id="c3141-133">Number of mip levels requested.</span></span> <span data-ttu-id="c3141-134">如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="c3141-134">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="c3141-135">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="c3141-135">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3141-136">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3141-136">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3141-137">0、D3DUSAGE \_ RENDERTARGET 或 D3DUSAGE \_ DYNAMIC。</span><span class="sxs-lookup"><span data-stu-id="c3141-137">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="c3141-138">將此旗標設定為 D3DUSAGE \_ RENDERTARGET 表示介面要當做轉譯目標使用。</span><span class="sxs-lookup"><span data-stu-id="c3141-138">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="c3141-139">然後，您可以將資源傳遞給 [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget)方法的 *pNewRenderTarget* 參數。</span><span class="sxs-lookup"><span data-stu-id="c3141-139">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="c3141-140">如果 \_ 指定了 D3DUSAGE RENDERTARGET 或 D3DUSAGE \_ DYNAMIC，則必須將集區設定為 D3DPOOL \_ 預設值，而應用程式應藉由呼叫 [**CheckDeviceFormat**](/windows/desktop/api)來檢查裝置是否支援這項操作。</span><span class="sxs-lookup"><span data-stu-id="c3141-140">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="c3141-141">D3DUSAGE \_ DYNAMIC 表示介面應該以動態方式處理。</span><span class="sxs-lookup"><span data-stu-id="c3141-141">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="c3141-142">如需使用動態紋理的詳細資訊，請參閱 [使用動態紋理](performance-optimizations.md)。</span><span class="sxs-lookup"><span data-stu-id="c3141-142">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3141-143">*格式*</span><span class="sxs-lookup"><span data-stu-id="c3141-143">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="c3141-144">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="c3141-144">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="c3141-145">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述紋理所要求的像素格式。</span><span class="sxs-lookup"><span data-stu-id="c3141-145">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="c3141-146">傳回的材質可能與以 *格式* 指定的格式不同。</span><span class="sxs-lookup"><span data-stu-id="c3141-146">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="c3141-147">應用程式應該檢查傳回的材質格式。</span><span class="sxs-lookup"><span data-stu-id="c3141-147">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="c3141-148">如果 [D3DFMT \_ 未知](other-d3dx-constants.md)，就會從檔案中取得格式。</span><span class="sxs-lookup"><span data-stu-id="c3141-148">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="c3141-149">如果從檔案 D3DFMT \_ \_ ，格式會與檔案中的格式完全相同，而且如果這違反裝置功能，呼叫就會失敗。</span><span class="sxs-lookup"><span data-stu-id="c3141-149">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="c3141-150">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="c3141-150">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3141-151">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="c3141-151">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="c3141-152">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置紋理的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="c3141-152">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="c3141-153">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3141-153">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3141-154">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3141-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3141-155">一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="c3141-155">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="c3141-156">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="c3141-156">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="c3141-157">*MipFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3141-157">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3141-158">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3141-158">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3141-159">一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="c3141-159">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="c3141-160">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選方塊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c3141-160">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="c3141-161">此外，使用 bits 27-31 來指定當將 dds 材質載入至記憶體時， (從 mipmap 鏈頂端跳過的 mip 層級數目) 。這可讓您略過32層級。</span><span class="sxs-lookup"><span data-stu-id="c3141-161">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="c3141-162">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3141-162">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3141-163">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="c3141-163">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="c3141-164">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。</span><span class="sxs-lookup"><span data-stu-id="c3141-164">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="c3141-165">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="c3141-165">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="c3141-166">Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。</span><span class="sxs-lookup"><span data-stu-id="c3141-166">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="c3141-167">因此，若是不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="c3141-167">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="c3141-168">*pSrcInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c3141-168">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3141-169">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3141-169">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="c3141-170">要填入的 [**D3DXIMAGE \_ 資訊**](d3dximage-info.md) 結構的指標，其中包含來源影像檔案中的資料描述或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c3141-170">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c3141-171">*pPalette* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c3141-171">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3141-172">類型： **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="c3141-172">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="c3141-173">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，代表要填入的256色調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c3141-173">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c3141-174">*ppTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c3141-174">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3141-175">類型： **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="c3141-175">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="c3141-176">[**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)介面指標的位址，表示所建立的材質物件。</span><span class="sxs-lookup"><span data-stu-id="c3141-176">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3141-177">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3141-177">Return value</span></span>

<span data-ttu-id="c3141-178">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3141-178">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3141-179">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="c3141-179">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c3141-180">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="c3141-180">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3141-181">備註</span><span class="sxs-lookup"><span data-stu-id="c3141-181">Remarks</span></span>

<span data-ttu-id="c3141-182">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="c3141-182">The compiler setting also determines the function version.</span></span> <span data-ttu-id="c3141-183">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateVolumeTextureFromFileExW。</span><span class="sxs-lookup"><span data-stu-id="c3141-183">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromFileExW.</span></span> <span data-ttu-id="c3141-184">否則，函式呼叫會解析為 D3DXCreateVolumeTextureFromFileExA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="c3141-184">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromFileExA because ANSI strings are being used.</span></span>

<span data-ttu-id="c3141-185">此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="c3141-185">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="c3141-186">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="c3141-186">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="c3141-187">Mipmapped 紋理會自動以載入的音量材質填滿每個層級。</span><span class="sxs-lookup"><span data-stu-id="c3141-187">Mipmapped textures automatically have each level filled with the loaded volume texture.</span></span> <span data-ttu-id="c3141-188">將影像載入 mipmapped 材質時，某些裝置無法進入1x1 影像，而且此函式將會失敗。</span><span class="sxs-lookup"><span data-stu-id="c3141-188">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="c3141-189">如果發生這種情況，則必須以手動方式載入映射。</span><span class="sxs-lookup"><span data-stu-id="c3141-189">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="c3141-190">在載入 dd 檔案時略過 mipmap 層級時，請使用 D3DX \_ SKIP \_ dds \_ MIP \_ 層級宏來產生 *MipFilter* 值。</span><span class="sxs-lookup"><span data-stu-id="c3141-190">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the *MipFilter* value.</span></span> <span data-ttu-id="c3141-191">此宏會接受要略過的層級數目和篩選準則類型，並傳回篩選值，然後將其傳遞至 *MipFilter* 參數。</span><span class="sxs-lookup"><span data-stu-id="c3141-191">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the *MipFilter* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3141-192">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3141-192">Requirements</span></span>



| <span data-ttu-id="c3141-193">需求</span><span class="sxs-lookup"><span data-stu-id="c3141-193">Requirement</span></span> | <span data-ttu-id="c3141-194">值</span><span class="sxs-lookup"><span data-stu-id="c3141-194">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3141-195">標頭</span><span class="sxs-lookup"><span data-stu-id="c3141-195">Header</span></span><br/>  | <dl> <span data-ttu-id="c3141-196"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="c3141-196"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c3141-197">程式庫</span><span class="sxs-lookup"><span data-stu-id="c3141-197">Library</span></span><br/> | <dl> <span data-ttu-id="c3141-198"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3141-198"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c3141-199">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3141-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3141-200">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="c3141-200">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="c3141-201">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="c3141-201">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="c3141-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="c3141-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="c3141-203">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="c3141-203">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="c3141-204">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="c3141-204">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="c3141-205">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="c3141-205">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
