---
description: 從檔案建立紋理。 這是比 D3DXCreateTextureFromFile 更先進的函式。
ms.assetid: 820bbd77-98af-4051-a22e-825fa4dd87d8
title: 'D3DXCreateTextureFromFileEx 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4dba1424f98389a9282fdebf9dae55c7e1601f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103853988"
---
# <a name="d3dxcreatetexturefromfileex-function"></a><span data-ttu-id="89ee8-104">D3DXCreateTextureFromFileEx 函式</span><span class="sxs-lookup"><span data-stu-id="89ee8-104">D3DXCreateTextureFromFileEx function</span></span>

<span data-ttu-id="89ee8-105">從檔案建立紋理。</span><span class="sxs-lookup"><span data-stu-id="89ee8-105">Creates a texture from a file.</span></span> <span data-ttu-id="89ee8-106">這是比 [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)更先進的函式。</span><span class="sxs-lookup"><span data-stu-id="89ee8-106">This is a more advanced function than [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="89ee8-107">語法</span><span class="sxs-lookup"><span data-stu-id="89ee8-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCTSTR            pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="89ee8-108">參數</span><span class="sxs-lookup"><span data-stu-id="89ee8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89ee8-109">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89ee8-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ee8-110">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="89ee8-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="89ee8-111">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="89ee8-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="89ee8-112">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89ee8-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ee8-113">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89ee8-113">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="89ee8-114">指定檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="89ee8-114">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="89ee8-115">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="89ee8-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="89ee8-116">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="89ee8-116">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="89ee8-117">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="89ee8-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="89ee8-118">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89ee8-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ee8-119">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89ee8-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="89ee8-120">寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="89ee8-120">Width in pixels.</span></span> <span data-ttu-id="89ee8-121">如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度，並將其四捨五入為二的乘冪。</span><span class="sxs-lookup"><span data-stu-id="89ee8-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file and rounded up to a power of two.</span></span> <span data-ttu-id="89ee8-122">如果裝置支援2個材質的非電源，並指定 [D3DX \_ 預設 \_ NONPOW2](other-d3dx-constants.md) ，則不會將大小四捨五入。</span><span class="sxs-lookup"><span data-stu-id="89ee8-122">If the device supports non-power of 2 textures and [D3DX\_DEFAULT\_NONPOW2](other-d3dx-constants.md) is specified, the size will not be rounded.</span></span>

</dd> <dt>

<span data-ttu-id="89ee8-123">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89ee8-123">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ee8-124">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89ee8-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="89ee8-125">高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="89ee8-125">Height, in pixels.</span></span> <span data-ttu-id="89ee8-126">如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度，並將其四捨五入為二的乘冪。</span><span class="sxs-lookup"><span data-stu-id="89ee8-126">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file and rounded up to a power of two.</span></span> <span data-ttu-id="89ee8-127">如果裝置支援2個材質的非電源，且 [D3DX \_ 預設 \_ NONPOW2](other-d3dx-constants.md) 為所以，則不會將大小四捨五入。</span><span class="sxs-lookup"><span data-stu-id="89ee8-127">If the device supports non-power of 2 textures and [D3DX\_DEFAULT\_NONPOW2](other-d3dx-constants.md) is sepcified, the size will not be rounded.</span></span>

</dd> <dt>

<span data-ttu-id="89ee8-128">*MipLevels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89ee8-128">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ee8-129">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89ee8-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="89ee8-130">要求的 mip 層級數目。</span><span class="sxs-lookup"><span data-stu-id="89ee8-130">Number of mip levels requested.</span></span> <span data-ttu-id="89ee8-131">如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="89ee8-131">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="89ee8-132">如果從檔案 D3DX \_ \_ ，大小會與檔案中的大小相同，而且如果這違反裝置功能，則呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="89ee8-132">If D3DX\_FROM\_FILE, the size will be taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="89ee8-133">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="89ee8-133">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ee8-134">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89ee8-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="89ee8-135">0、 [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)或 **D3DUSAGE \_ DYNAMIC**。</span><span class="sxs-lookup"><span data-stu-id="89ee8-135">0, [**D3DUSAGE\_RENDERTARGET**](d3dusage.md), or **D3DUSAGE\_DYNAMIC**.</span></span> <span data-ttu-id="89ee8-136">將此旗標設定為 **D3DUSAGE \_ RENDERTARGET** 表示介面要當做轉譯目標使用。</span><span class="sxs-lookup"><span data-stu-id="89ee8-136">Setting this flag to **D3DUSAGE\_RENDERTARGET** indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="89ee8-137">然後，您可以將資源傳遞給 [**SetRenderTarget**](/windows/desktop/api)方法的 *pNewRenderTarget* 參數。</span><span class="sxs-lookup"><span data-stu-id="89ee8-137">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="89ee8-138">如果指定了 **D3DUSAGE \_ RENDERTARGET** 或 **D3DUSAGE \_ DYNAMIC** ，則 *必須將集區* 設定為 D3DPOOL \_ 預設值，而應用程式應藉由呼叫 [**CheckDeviceFormat**](/windows/desktop/api)來檢查裝置是否支援這項操作。</span><span class="sxs-lookup"><span data-stu-id="89ee8-138">If either **D3DUSAGE\_RENDERTARGET** or **D3DUSAGE\_DYNAMIC** is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="89ee8-139">**D3DUSAGE \_DYNAMIC** 表示介面應該以動態方式處理。</span><span class="sxs-lookup"><span data-stu-id="89ee8-139">**D3DUSAGE\_DYNAMIC** indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="89ee8-140">請參閱 [使用動態紋理](performance-optimizations.md)。</span><span class="sxs-lookup"><span data-stu-id="89ee8-140">See [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="89ee8-141">*格式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89ee8-141">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ee8-142">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="89ee8-142">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="89ee8-143">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述紋理所要求的像素格式。</span><span class="sxs-lookup"><span data-stu-id="89ee8-143">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="89ee8-144">傳回的材質可能與以 *格式* 指定的格式不同。</span><span class="sxs-lookup"><span data-stu-id="89ee8-144">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="89ee8-145">應用程式應該檢查傳回的材質格式。</span><span class="sxs-lookup"><span data-stu-id="89ee8-145">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="89ee8-146">如果 D3DFMT \_ 未知，就會從檔案中取得格式。</span><span class="sxs-lookup"><span data-stu-id="89ee8-146">If D3DFMT\_UNKNOWN, the format is taken from the file.</span></span> <span data-ttu-id="89ee8-147">如果從檔案 D3DFMT \_ \_ ，格式會與檔案中的格式完全相同，而且如果這違反裝置功能，呼叫就會失敗。</span><span class="sxs-lookup"><span data-stu-id="89ee8-147">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="89ee8-148">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="89ee8-148">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ee8-149">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="89ee8-149">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="89ee8-150">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置紋理的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="89ee8-150">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="89ee8-151">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89ee8-151">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ee8-152">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89ee8-152">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="89ee8-153">一或多個 [D3DX \_ 篩選](d3dx-filter.md) 常數的組合，可控制如何篩選影像。</span><span class="sxs-lookup"><span data-stu-id="89ee8-153">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="89ee8-154">指定此參數的 [D3DX \_ 預設值](other-d3dx-constants.md) ，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="89ee8-154">Specifying [D3DX\_DEFAULT](other-d3dx-constants.md) for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="89ee8-155">*MipFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89ee8-155">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ee8-156">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89ee8-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="89ee8-157">一或多個 [D3DX \_ 篩選](d3dx-filter.md) 常數的組合，可控制如何篩選影像。</span><span class="sxs-lookup"><span data-stu-id="89ee8-157">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="89ee8-158">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選方塊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="89ee8-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="89ee8-159">此外，使用 bits 27-31 來指定當將 dds 材質載入至記憶體時， (從 mipmap 鏈頂端跳過的 mip 層級數目) 。這可讓您略過32層級。</span><span class="sxs-lookup"><span data-stu-id="89ee8-159">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="89ee8-160">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89ee8-160">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89ee8-161">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="89ee8-161">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="89ee8-162">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用色彩索引鍵。</span><span class="sxs-lookup"><span data-stu-id="89ee8-162">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the color key.</span></span> <span data-ttu-id="89ee8-163">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="89ee8-163">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="89ee8-164">Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。</span><span class="sxs-lookup"><span data-stu-id="89ee8-164">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="89ee8-165">因此，若是不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="89ee8-165">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="89ee8-166">*pSrcInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="89ee8-166">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="89ee8-167">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="89ee8-167">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="89ee8-168">要填入的 [**D3DXIMAGE \_ 資訊**](d3dximage-info.md) 結構的指標，其中包含來源影像檔案中的資料描述或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="89ee8-168">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="89ee8-169">*pPalette* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="89ee8-169">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89ee8-170">類型： **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="89ee8-170">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="89ee8-171">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，代表要填入的256色調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="89ee8-171">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="89ee8-172">*ppTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="89ee8-172">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89ee8-173">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="89ee8-173">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="89ee8-174">[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面指標的位址，表示所建立的材質物件。</span><span class="sxs-lookup"><span data-stu-id="89ee8-174">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89ee8-175">傳回值</span><span class="sxs-lookup"><span data-stu-id="89ee8-175">Return value</span></span>

<span data-ttu-id="89ee8-176">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="89ee8-176">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="89ee8-177">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="89ee8-177">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="89ee8-178">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="89ee8-178">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="89ee8-179">備註</span><span class="sxs-lookup"><span data-stu-id="89ee8-179">Remarks</span></span>

<span data-ttu-id="89ee8-180">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="89ee8-180">The compiler setting also determines the function version.</span></span> <span data-ttu-id="89ee8-181">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateTextureFromFileExW。</span><span class="sxs-lookup"><span data-stu-id="89ee8-181">If Unicode is defined, the function call resolves to D3DXCreateTextureFromFileExW.</span></span> <span data-ttu-id="89ee8-182">否則，函式呼叫會解析為 D3DXCreateTextureFromFileExA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="89ee8-182">Otherwise, the function call resolves to D3DXCreateTextureFromFileExA because ANSI strings are being used.</span></span>

<span data-ttu-id="89ee8-183">使用 [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) 來判斷您的裝置是否可以支援指定目前狀態的材質。</span><span class="sxs-lookup"><span data-stu-id="89ee8-183">Use [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) to determine if your device can support the texture given the current state.</span></span>

<span data-ttu-id="89ee8-184">此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="89ee8-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="89ee8-185">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="89ee8-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="89ee8-186">Mipmapped 紋理會自動以載入的材質填滿每個層級。</span><span class="sxs-lookup"><span data-stu-id="89ee8-186">Mipmapped textures automatically have each level filled with the loaded texture.</span></span> <span data-ttu-id="89ee8-187">將影像載入 mipmapped 材質時，某些裝置無法進入1x1 影像，而且此函式將會失敗。</span><span class="sxs-lookup"><span data-stu-id="89ee8-187">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="89ee8-188">如果發生這種情況，則必須以手動方式載入映射。</span><span class="sxs-lookup"><span data-stu-id="89ee8-188">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="89ee8-189">若要在使用 **D3DXCreateTextureFromFileEx** 時獲得最佳效能：</span><span class="sxs-lookup"><span data-stu-id="89ee8-189">For the best performance when using **D3DXCreateTextureFromFileEx**:</span></span>

1.  <span data-ttu-id="89ee8-190">在載入時間進行映射調整和格式轉換可能會很慢。</span><span class="sxs-lookup"><span data-stu-id="89ee8-190">Doing image scaling and format conversion at load time can be slow.</span></span> <span data-ttu-id="89ee8-191">以將使用的格式和解析度儲存影像。</span><span class="sxs-lookup"><span data-stu-id="89ee8-191">Store images in the format and resolution they will be used.</span></span> <span data-ttu-id="89ee8-192">如果目標硬體需要2個維度的電源，請使用2個維度的電源來建立和儲存影像。</span><span class="sxs-lookup"><span data-stu-id="89ee8-192">If the target hardware requires power of 2 dimensions, then create and store images using power of 2 dimensions.</span></span>
2.  <span data-ttu-id="89ee8-193">若要在載入期間建立 mipmap 映射，請 [使用 \_ D3DX \_ 篩選](d3dx-filter.md)方塊進行篩選。</span><span class="sxs-lookup"><span data-stu-id="89ee8-193">For mipmap image creation at load time, filter using [D3DX\_FILTER\_BOX](d3dx-filter.md).</span></span> <span data-ttu-id="89ee8-194">Box 篩選比其他篩選器類型（例如 D3DX 濾波器三角形）更快 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="89ee8-194">A box filter is much faster than other filter types such as D3DX\_FILTER\_TRIANGLE.</span></span>
3.  <span data-ttu-id="89ee8-195">請考慮使用 DDS 檔。</span><span class="sxs-lookup"><span data-stu-id="89ee8-195">Consider using DDS files.</span></span> <span data-ttu-id="89ee8-196">由於 DDS 檔案可以用來代表任何 Direct3D 9 材質格式，因此很容易就能 D3DX 閱讀。</span><span class="sxs-lookup"><span data-stu-id="89ee8-196">Since DDS files can be used to represent any Direct3D 9 texture format, they are very easy for D3DX to read.</span></span> <span data-ttu-id="89ee8-197">此外，他們也可以儲存 mipmap，讓任何 mipmap 產生的演算法都能用來撰寫映射。</span><span class="sxs-lookup"><span data-stu-id="89ee8-197">Also, they can store mipmaps, so any mipmap-generation algorithms can be used to author the images.</span></span>

<span data-ttu-id="89ee8-198">在載入 dd 檔案時略過 mipmap 層級時，請使用 D3DX \_ SKIP \_ dds \_ MIP \_ 層級宏來產生 MipFilter 值。</span><span class="sxs-lookup"><span data-stu-id="89ee8-198">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="89ee8-199">此宏會接受要略過的層級數目和篩選準則類型，並傳回篩選值，然後將其傳遞至 MipFilter 參數。</span><span class="sxs-lookup"><span data-stu-id="89ee8-199">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="89ee8-200">規格需求</span><span class="sxs-lookup"><span data-stu-id="89ee8-200">Requirements</span></span>



| <span data-ttu-id="89ee8-201">需求</span><span class="sxs-lookup"><span data-stu-id="89ee8-201">Requirement</span></span> | <span data-ttu-id="89ee8-202">值</span><span class="sxs-lookup"><span data-stu-id="89ee8-202">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89ee8-203">標頭</span><span class="sxs-lookup"><span data-stu-id="89ee8-203">Header</span></span><br/>  | <dl> <span data-ttu-id="89ee8-204"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="89ee8-204"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="89ee8-205">程式庫</span><span class="sxs-lookup"><span data-stu-id="89ee8-205">Library</span></span><br/> | <dl> <span data-ttu-id="89ee8-206"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="89ee8-206"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="89ee8-207">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89ee8-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89ee8-208">**D3DXCreateTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="89ee8-208">**D3DXCreateTextureFromFile**</span></span>](d3dxcreatetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="89ee8-209">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="89ee8-209">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
