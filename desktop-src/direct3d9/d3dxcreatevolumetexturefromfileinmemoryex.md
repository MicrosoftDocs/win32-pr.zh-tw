---
description: 從檔案建立磁片區材質。 這是比 D3DXCreateVolumeTextureFromFileInMemory 更先進的函式。
ms.assetid: 1a43f906-1826-40a3-a7a9-a0536c977164
title: 'D3DXCreateVolumeTextureFromFileInMemoryEx 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f09439be9410b59ccaa446c2f00ee79963a21cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976486"
---
# <a name="d3dxcreatevolumetexturefromfileinmemoryex-function"></a><span data-ttu-id="ccc27-104">D3DXCreateVolumeTextureFromFileInMemoryEx 函式</span><span class="sxs-lookup"><span data-stu-id="ccc27-104">D3DXCreateVolumeTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="ccc27-105">從檔案建立磁片區材質。</span><span class="sxs-lookup"><span data-stu-id="ccc27-105">Creates a volume texture from a file.</span></span> <span data-ttu-id="ccc27-106">這是比 [**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md)更先進的函式。</span><span class="sxs-lookup"><span data-stu-id="ccc27-106">This is a more advanced function than [**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ccc27-107">語法</span><span class="sxs-lookup"><span data-stu-id="ccc27-107">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCVOID                  pSrcData,
  _In_    UINT                     SrcDataSize,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
  _In_    D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="ccc27-108">參數</span><span class="sxs-lookup"><span data-stu-id="ccc27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccc27-109">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccc27-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc27-110">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ccc27-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ccc27-111">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="ccc27-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="ccc27-112">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccc27-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc27-113">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ccc27-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ccc27-114">用來建立磁片區材質之記憶體中檔案的指標。</span><span class="sxs-lookup"><span data-stu-id="ccc27-114">Pointer to the file in memory from which to create the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="ccc27-115">*SrcDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccc27-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc27-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ccc27-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ccc27-117">檔案在記憶體中的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ccc27-117">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ccc27-118">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccc27-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc27-119">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ccc27-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ccc27-120">寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="ccc27-120">Width in pixels.</span></span> <span data-ttu-id="ccc27-121">如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。</span><span class="sxs-lookup"><span data-stu-id="ccc27-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="ccc27-122">驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。</span><span class="sxs-lookup"><span data-stu-id="ccc27-122">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="ccc27-123">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccc27-123">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc27-124">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ccc27-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ccc27-125">高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="ccc27-125">Height, in pixels.</span></span> <span data-ttu-id="ccc27-126">如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。</span><span class="sxs-lookup"><span data-stu-id="ccc27-126">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="ccc27-127">驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。</span><span class="sxs-lookup"><span data-stu-id="ccc27-127">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="ccc27-128">*深度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccc27-128">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc27-129">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ccc27-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ccc27-130">深度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="ccc27-130">Depth, in pixels.</span></span> <span data-ttu-id="ccc27-131">如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。</span><span class="sxs-lookup"><span data-stu-id="ccc27-131">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="ccc27-132">驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。</span><span class="sxs-lookup"><span data-stu-id="ccc27-132">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="ccc27-133">*MipLevels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccc27-133">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc27-134">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ccc27-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ccc27-135">要求的 mip 層級數目。</span><span class="sxs-lookup"><span data-stu-id="ccc27-135">Number of mip levels requested.</span></span> <span data-ttu-id="ccc27-136">如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="ccc27-136">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="ccc27-137">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="ccc27-137">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc27-138">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ccc27-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ccc27-139">0、D3DUSAGE \_ RENDERTARGET 或 D3DUSAGE \_ DYNAMIC。</span><span class="sxs-lookup"><span data-stu-id="ccc27-139">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="ccc27-140">將此旗標設定為 D3DUSAGE \_ RENDERTARGET 表示介面要當做轉譯目標使用。</span><span class="sxs-lookup"><span data-stu-id="ccc27-140">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="ccc27-141">然後，您可以將資源傳遞給 [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget)方法的 *pNewRenderTarget* 參數。</span><span class="sxs-lookup"><span data-stu-id="ccc27-141">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="ccc27-142">如果 \_ 指定了 D3DUSAGE RENDERTARGET 或 D3DUSAGE \_ DYNAMIC，則必須將集區設定為 D3DPOOL \_ 預設值，而應用程式應藉由呼叫 [**CheckDeviceFormat**](/windows/desktop/api)來檢查裝置是否支援這項操作。</span><span class="sxs-lookup"><span data-stu-id="ccc27-142">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="ccc27-143">D3DUSAGE \_ DYNAMIC 表示介面應該以動態方式處理。</span><span class="sxs-lookup"><span data-stu-id="ccc27-143">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="ccc27-144">如需使用動態紋理的詳細資訊，請參閱 [使用動態紋理](performance-optimizations.md)。</span><span class="sxs-lookup"><span data-stu-id="ccc27-144">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="ccc27-145">*格式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccc27-145">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc27-146">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ccc27-146">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="ccc27-147">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述紋理所要求的像素格式。</span><span class="sxs-lookup"><span data-stu-id="ccc27-147">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="ccc27-148">傳回的材質可能與以 *格式* 指定的格式不同。</span><span class="sxs-lookup"><span data-stu-id="ccc27-148">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="ccc27-149">應用程式應該檢查傳回的材質格式。</span><span class="sxs-lookup"><span data-stu-id="ccc27-149">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="ccc27-150">如果 [D3DFMT \_ 未知](other-d3dx-constants.md)，就會從檔案中取得格式。</span><span class="sxs-lookup"><span data-stu-id="ccc27-150">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="ccc27-151">如果從檔案 D3DFMT \_ \_ ，格式會與檔案中的格式完全相同，而且如果這違反裝置功能，呼叫就會失敗。</span><span class="sxs-lookup"><span data-stu-id="ccc27-151">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="ccc27-152">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="ccc27-152">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc27-153">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="ccc27-153">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="ccc27-154">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置紋理的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="ccc27-154">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="ccc27-155">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccc27-155">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc27-156">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ccc27-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ccc27-157">用來控制如何篩選影像的一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合。</span><span class="sxs-lookup"><span data-stu-id="ccc27-157">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="ccc27-158">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="ccc27-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="ccc27-159">*MipFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccc27-159">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc27-160">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ccc27-160">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ccc27-161">用來控制如何篩選影像的一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合。</span><span class="sxs-lookup"><span data-stu-id="ccc27-161">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="ccc27-162">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選方塊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ccc27-162">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="ccc27-163">此外，使用 bits 27-31 來指定當將 dds 材質載入至記憶體時， (從 mipmap 鏈頂端跳過的 mip 層級數目) 。這可讓您略過32層級。</span><span class="sxs-lookup"><span data-stu-id="ccc27-163">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="ccc27-164">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccc27-164">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc27-165">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="ccc27-165">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="ccc27-166">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。</span><span class="sxs-lookup"><span data-stu-id="ccc27-166">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="ccc27-167">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="ccc27-167">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="ccc27-168">Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。</span><span class="sxs-lookup"><span data-stu-id="ccc27-168">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="ccc27-169">因此，若是不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="ccc27-169">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="ccc27-170">*pSrcInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="ccc27-170">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc27-171">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ccc27-171">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="ccc27-172">要填入的 [**D3DXIMAGE \_ 資訊**](d3dximage-info.md) 結構的指標，其中包含來源影像檔案中的資料描述或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ccc27-172">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ccc27-173">*pPalette* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ccc27-173">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc27-174">類型： **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="ccc27-174">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="ccc27-175">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，代表要填入的256色調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ccc27-175">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ccc27-176">*ppVolumeTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ccc27-176">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc27-177">類型： **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="ccc27-177">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="ccc27-178">[**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)介面指標的位址，表示所建立的材質物件。</span><span class="sxs-lookup"><span data-stu-id="ccc27-178">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccc27-179">傳回值</span><span class="sxs-lookup"><span data-stu-id="ccc27-179">Return value</span></span>

<span data-ttu-id="ccc27-180">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ccc27-180">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ccc27-181">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="ccc27-181">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ccc27-182">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="ccc27-182">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccc27-183">備註</span><span class="sxs-lookup"><span data-stu-id="ccc27-183">Remarks</span></span>

<span data-ttu-id="ccc27-184">此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="ccc27-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="ccc27-185">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="ccc27-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="ccc27-186">在載入 dd 檔案時略過 mipmap 層級時，請使用 D3DX \_ SKIP \_ dds \_ MIP \_ 層級宏來產生 *MipFilter* 值。</span><span class="sxs-lookup"><span data-stu-id="ccc27-186">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the *MipFilter* value.</span></span> <span data-ttu-id="ccc27-187">此宏會接受要略過的層級數目和篩選準則類型，並傳回篩選值，然後將其傳遞至 *MipFilter* 參數。</span><span class="sxs-lookup"><span data-stu-id="ccc27-187">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the *MipFilter* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccc27-188">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccc27-188">Requirements</span></span>



| <span data-ttu-id="ccc27-189">需求</span><span class="sxs-lookup"><span data-stu-id="ccc27-189">Requirement</span></span> | <span data-ttu-id="ccc27-190">值</span><span class="sxs-lookup"><span data-stu-id="ccc27-190">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc27-191">標頭</span><span class="sxs-lookup"><span data-stu-id="ccc27-191">Header</span></span><br/>  | <dl> <span data-ttu-id="ccc27-192"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="ccc27-192"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ccc27-193">程式庫</span><span class="sxs-lookup"><span data-stu-id="ccc27-193">Library</span></span><br/> | <dl> <span data-ttu-id="ccc27-194"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccc27-194"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ccc27-195">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ccc27-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccc27-196">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="ccc27-196">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="ccc27-197">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="ccc27-197">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="ccc27-198">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="ccc27-198">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="ccc27-199">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="ccc27-199">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="ccc27-200">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="ccc27-200">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="ccc27-201">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="ccc27-201">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
