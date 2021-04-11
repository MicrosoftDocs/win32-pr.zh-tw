---
description: 從記憶體中的檔案建立紋理。 這是比 D3DXCreateTextureFromFileInMemory 更先進的函式。
ms.assetid: e515697c-0e24-4d96-b58a-dc4f27683021
title: 'D3DXCreateTextureFromFileInMemoryEx 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da85af9e70a7971ba0bab1f76e9c3d30c3cc2884
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946106"
---
# <a name="d3dxcreatetexturefromfileinmemoryex-function"></a><span data-ttu-id="a2a9b-104">D3DXCreateTextureFromFileInMemoryEx 函式</span><span class="sxs-lookup"><span data-stu-id="a2a9b-104">D3DXCreateTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="a2a9b-105">從記憶體中的檔案建立紋理。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-105">Creates a texture from a file in memory.</span></span> <span data-ttu-id="a2a9b-106">這是比 [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md)更先進的函式。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-106">This is a more advanced function than [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2a9b-107">語法</span><span class="sxs-lookup"><span data-stu-id="a2a9b-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCVOID            pSrcData,
  _In_    UINT               SrcDataSize,
  _In_    UINT               Width,
  _In_    UINT               Height,
  _In_    UINT               MipLevels,
  _In_    DWORD              Usage,
  _In_    D3DFORMAT          Format,
  _In_    D3DPOOL            Pool,
  _In_    DWORD              Filter,
  _In_    DWORD              MipFilter,
  _In_    D3DCOLOR           ColorKey,
  _Inout_ D3DXIMAGE_INFO     *pSrcInfo,
  _Out_   PALETTEENTRY       *pPalette,
  _Out_   LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="a2a9b-108">參數</span><span class="sxs-lookup"><span data-stu-id="a2a9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2a9b-109">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2a9b-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a9b-110">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a2a9b-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a2a9b-111">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="a2a9b-112">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2a9b-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a9b-113">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2a9b-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2a9b-114">要從中建立材質之記憶體中的檔案指標。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-114">Pointer to the file in memory from which to create the texture.</span></span>

</dd> <dt>

<span data-ttu-id="a2a9b-115">*SrcDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2a9b-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a9b-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2a9b-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2a9b-117">檔案在記憶體中的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-117">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a2a9b-118">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2a9b-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a9b-119">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2a9b-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2a9b-120">寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-120">Width in pixels.</span></span> <span data-ttu-id="a2a9b-121">如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="a2a9b-122">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2a9b-122">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a9b-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2a9b-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2a9b-124">高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-124">Height, in pixels.</span></span> <span data-ttu-id="a2a9b-125">如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-125">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="a2a9b-126">*MipLevels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2a9b-126">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a9b-127">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2a9b-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2a9b-128">要求的 mip 層級數目。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-128">Number of mip levels requested.</span></span> <span data-ttu-id="a2a9b-129">如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-129">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="a2a9b-130">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="a2a9b-130">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a9b-131">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2a9b-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2a9b-132">0、D3DUSAGE \_ RENDERTARGET 或 D3DUSAGE \_ DYNAMIC。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-132">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="a2a9b-133">將此旗標設定為 D3DUSAGE \_ RENDERTARGET 表示介面要當做轉譯目標使用。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-133">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="a2a9b-134">然後，您可以將資源傳遞給 [**SetRenderTarget**](/windows/desktop/api)方法的 *pNewRenderTarget* 參數。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-134">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="a2a9b-135">如果 \_ 指定了 D3DUSAGE RENDERTARGET 或 D3DUSAGE \_ DYNAMIC，則必須將集區設定為 D3DPOOL \_ 預設值，而應用程式應藉由呼叫 [**CheckDeviceFormat**](/windows/desktop/api)來檢查裝置是否支援這項操作。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-135">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="a2a9b-136">如需使用動態紋理的詳細資訊，請參閱 [使用動態紋理](performance-optimizations.md)。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-136">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2a9b-137">*格式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2a9b-137">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a9b-138">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="a2a9b-138">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="a2a9b-139">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述紋理所要求的像素格式。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-139">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="a2a9b-140">傳回的材質可能與以 *格式* 指定的格式不同。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-140">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="a2a9b-141">應用程式應該檢查傳回的材質格式。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-141">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="a2a9b-142">如果 [D3DFMT \_ 未知](other-d3dx-constants.md)，就會從檔案中取得格式。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-142">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="a2a9b-143">如果從檔案 D3DFMT \_ \_ ，格式會與檔案中的格式完全相同，而且如果這違反裝置功能，呼叫就會失敗。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-143">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="a2a9b-144">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="a2a9b-144">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a9b-145">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="a2a9b-145">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="a2a9b-146">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置紋理的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-146">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="a2a9b-147">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2a9b-147">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a9b-148">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2a9b-148">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2a9b-149">一或多個旗標的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-149">Combination of one or more flags controlling how the image is filtered.</span></span> <span data-ttu-id="a2a9b-150">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-150">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="a2a9b-151">每個有效的篩選準則都必須包含 [D3DX \_ 篩選器](d3dx-filter.md)中的其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-151">Each valid filter must contain one of the flags in [D3DX\_FILTER](d3dx-filter.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2a9b-152">*MipFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2a9b-152">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a9b-153">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2a9b-153">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2a9b-154">一或多個旗標的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-154">Combination of one or more flags controlling how the image is filtered.</span></span> <span data-ttu-id="a2a9b-155">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選方塊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-155">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="a2a9b-156">每個有效的篩選準則都必須包含 [D3DX \_ 篩選器](d3dx-filter.md)中的其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-156">Each valid filter must contain one of the flags in [D3DX\_FILTER](d3dx-filter.md).</span></span> <span data-ttu-id="a2a9b-157">此外，使用 bits 27-31 來指定當將 dds 材質載入至記憶體時， (從 mipmap 鏈頂端跳過的 mip 層級數目) 。這可讓您略過32層級。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-157">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="a2a9b-158">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2a9b-158">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a9b-159">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="a2a9b-159">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="a2a9b-160">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-160">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="a2a9b-161">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-161">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="a2a9b-162">Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-162">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="a2a9b-163">因此，若是不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-163">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="a2a9b-164">*pSrcInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="a2a9b-164">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a9b-165">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="a2a9b-165">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="a2a9b-166">[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會以來源影像檔案中的資料描述來填滿，或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-166">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a2a9b-167">*pPalette* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a2a9b-167">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a9b-168">類型： **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="a2a9b-168">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="a2a9b-169">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，代表要填入的256色調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-169">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span> <span data-ttu-id="a2a9b-170">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-170">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a2a9b-171">*ppTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a2a9b-171">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a9b-172">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="a2a9b-172">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="a2a9b-173">[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面指標的位址，表示所建立的材質物件。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-173">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2a9b-174">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2a9b-174">Return value</span></span>

<span data-ttu-id="a2a9b-175">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a2a9b-175">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a2a9b-176">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-176">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a2a9b-177">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-177">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2a9b-178">備註</span><span class="sxs-lookup"><span data-stu-id="a2a9b-178">Remarks</span></span>

<span data-ttu-id="a2a9b-179">此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-179">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="a2a9b-180">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-180">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="a2a9b-181">如需 [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)的詳細資訊，請參閱 Platform SDK。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-181">For details about [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="a2a9b-182">請注意，從 DirectX 8.0 起， **PALETTEENTRY** 結構的 peFlags 成員無法如 Platform SDK 中所述運作。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-182">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="a2a9b-183">PeFlags 成員現在是8位調色盤格式的 Alpha 通道。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-183">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="a2a9b-184">在載入 dd 檔案時略過 mipmap 層級時，請使用 D3DX \_ SKIP \_ dds \_ MIP \_ 層級宏來產生 MipFilter 值。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-184">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="a2a9b-185">此宏會接受要略過的層級數目和篩選準則類型，並傳回篩選值，然後將其傳遞至 MipFilter 參數。</span><span class="sxs-lookup"><span data-stu-id="a2a9b-185">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2a9b-186">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2a9b-186">Requirements</span></span>



| <span data-ttu-id="a2a9b-187">需求</span><span class="sxs-lookup"><span data-stu-id="a2a9b-187">Requirement</span></span> | <span data-ttu-id="a2a9b-188">值</span><span class="sxs-lookup"><span data-stu-id="a2a9b-188">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2a9b-189">標頭</span><span class="sxs-lookup"><span data-stu-id="a2a9b-189">Header</span></span><br/>  | <dl> <span data-ttu-id="a2a9b-190"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="a2a9b-190"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a2a9b-191">程式庫</span><span class="sxs-lookup"><span data-stu-id="a2a9b-191">Library</span></span><br/> | <dl> <span data-ttu-id="a2a9b-192"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2a9b-192"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a2a9b-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2a9b-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2a9b-194">**D3DXCreateTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="a2a9b-194">**D3DXCreateTextureFromFileInMemory**</span></span>](d3dxcreatetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="a2a9b-195">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="a2a9b-195">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
