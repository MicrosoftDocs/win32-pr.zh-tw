---
description: 從資源建立紋理。 這是比 D3DXCreateTextureFromResource 更先進的函式。
ms.assetid: 6015e2fa-9deb-4e6a-a401-f10fb05f40b7
title: 'D3DXCreateTextureFromResourceEx 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 26298f8a63ccfde2171578c27e9208011c16dd28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514601"
---
# <a name="d3dxcreatetexturefromresourceex-function"></a><span data-ttu-id="30cf6-104">D3DXCreateTextureFromResourceEx 函式</span><span class="sxs-lookup"><span data-stu-id="30cf6-104">D3DXCreateTextureFromResourceEx function</span></span>

<span data-ttu-id="30cf6-105">從資源建立紋理。</span><span class="sxs-lookup"><span data-stu-id="30cf6-105">Creates a texture from a resource.</span></span> <span data-ttu-id="30cf6-106">這是比 [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md)更先進的函式。</span><span class="sxs-lookup"><span data-stu-id="30cf6-106">This is a more advanced function than [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="30cf6-107">語法</span><span class="sxs-lookup"><span data-stu-id="30cf6-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    HMODULE            hSrcModule,
  _In_    LPCTSTR            pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="30cf6-108">參數</span><span class="sxs-lookup"><span data-stu-id="30cf6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30cf6-109">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30cf6-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30cf6-110">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="30cf6-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="30cf6-111">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="30cf6-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="30cf6-112">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30cf6-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30cf6-113">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30cf6-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30cf6-114">資源所在之模組的控制碼，或與作業系統用來建立目前進程的映射相關聯的模組的 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="30cf6-114">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="30cf6-115">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30cf6-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30cf6-116">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30cf6-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30cf6-117">指定資源名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="30cf6-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="30cf6-118">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="30cf6-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="30cf6-119">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="30cf6-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="30cf6-120">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="30cf6-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="30cf6-121">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30cf6-121">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30cf6-122">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30cf6-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30cf6-123">寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="30cf6-123">Width in pixels.</span></span> <span data-ttu-id="30cf6-124">如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。</span><span class="sxs-lookup"><span data-stu-id="30cf6-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="30cf6-125">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30cf6-125">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30cf6-126">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30cf6-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30cf6-127">高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="30cf6-127">Height, in pixels.</span></span> <span data-ttu-id="30cf6-128">如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。</span><span class="sxs-lookup"><span data-stu-id="30cf6-128">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="30cf6-129">*MipLevels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30cf6-129">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30cf6-130">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30cf6-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30cf6-131">要求的 mip 層級數目。</span><span class="sxs-lookup"><span data-stu-id="30cf6-131">Number of mip levels requested.</span></span> <span data-ttu-id="30cf6-132">如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="30cf6-132">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="30cf6-133">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="30cf6-133">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30cf6-134">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30cf6-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30cf6-135">0、D3DUSAGE \_ RENDERTARGET 或 D3DUSAGE \_ DYNAMIC。</span><span class="sxs-lookup"><span data-stu-id="30cf6-135">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="30cf6-136">將此旗標設定為 D3DUSAGE \_ RENDERTARGET 表示介面要當做轉譯目標使用。</span><span class="sxs-lookup"><span data-stu-id="30cf6-136">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="30cf6-137">然後，您可以將資源傳遞給 [**SetRenderTarget**](/windows/desktop/api)方法的 *pNewRenderTarget* 參數。</span><span class="sxs-lookup"><span data-stu-id="30cf6-137">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="30cf6-138">如果 \_ 指定了 D3DUSAGE RENDERTARGET 或 D3DUSAGE，則必須將集區設定為 D3DPOOL \_ 預設值，而應用程式應藉由呼叫 [**CheckDeviceFormat**](/windows/desktop/api)來檢查裝置是否支援這項作業。</span><span class="sxs-lookup"><span data-stu-id="30cf6-138">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="30cf6-139">D3DUSAGE \_ DYNAMIC 表示介面應該以動態方式處理。</span><span class="sxs-lookup"><span data-stu-id="30cf6-139">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="30cf6-140">如需使用動態紋理的詳細資訊，請參閱使用動態紋理 [ (Direct3D 9) 效能優化 ](performance-optimizations.md)。</span><span class="sxs-lookup"><span data-stu-id="30cf6-140">For more information about using dynamic textures, see [Performance Optimizations (Direct3D 9)](performance-optimizations.md)Using Dynamic Textures.</span></span>

</dd> <dt>

<span data-ttu-id="30cf6-141">*格式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30cf6-141">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30cf6-142">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="30cf6-142">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="30cf6-143">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述紋理所要求的像素格式。</span><span class="sxs-lookup"><span data-stu-id="30cf6-143">A member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="30cf6-144">傳回的材質可能與以 *格式* 指定的格式不同。</span><span class="sxs-lookup"><span data-stu-id="30cf6-144">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="30cf6-145">應用程式應該檢查傳回的材質格式。</span><span class="sxs-lookup"><span data-stu-id="30cf6-145">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="30cf6-146">如果 [D3DFMT \_ 未知](other-d3dx-constants.md)，就會從檔案中取得格式。</span><span class="sxs-lookup"><span data-stu-id="30cf6-146">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="30cf6-147">如果從檔案 D3DFMT \_ \_ ，格式會與檔案中的格式完全相同，而且如果這違反裝置功能，呼叫就會失敗。</span><span class="sxs-lookup"><span data-stu-id="30cf6-147">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="30cf6-148">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="30cf6-148">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30cf6-149">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="30cf6-149">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="30cf6-150">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置紋理的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="30cf6-150">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="30cf6-151">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30cf6-151">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30cf6-152">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30cf6-152">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30cf6-153">一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="30cf6-153">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="30cf6-154">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="30cf6-154">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="30cf6-155">*MipFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30cf6-155">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30cf6-156">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30cf6-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30cf6-157">一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="30cf6-157">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="30cf6-158">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選方塊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="30cf6-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="30cf6-159">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30cf6-159">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30cf6-160">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="30cf6-160">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="30cf6-161">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。</span><span class="sxs-lookup"><span data-stu-id="30cf6-161">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="30cf6-162">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="30cf6-162">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="30cf6-163">Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。</span><span class="sxs-lookup"><span data-stu-id="30cf6-163">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="30cf6-164">因此，若是不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="30cf6-164">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="30cf6-165">*pSrcInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="30cf6-165">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="30cf6-166">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="30cf6-166">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="30cf6-167">[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會以來源影像檔案中的資料描述來填滿，或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="30cf6-167">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="30cf6-168">*pPalette* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="30cf6-168">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30cf6-169">類型： **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="30cf6-169">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="30cf6-170">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，代表要填入的256色調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="30cf6-170">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="30cf6-171">*ppTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="30cf6-171">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30cf6-172">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="30cf6-172">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="30cf6-173">[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面指標的位址，表示所建立的材質物件。</span><span class="sxs-lookup"><span data-stu-id="30cf6-173">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30cf6-174">傳回值</span><span class="sxs-lookup"><span data-stu-id="30cf6-174">Return value</span></span>

<span data-ttu-id="30cf6-175">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30cf6-175">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30cf6-176">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="30cf6-176">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="30cf6-177">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="30cf6-177">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="30cf6-178">備註</span><span class="sxs-lookup"><span data-stu-id="30cf6-178">Remarks</span></span>

<span data-ttu-id="30cf6-179">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="30cf6-179">The compiler setting also determines the function version.</span></span> <span data-ttu-id="30cf6-180">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateTextureFromResourceExW。</span><span class="sxs-lookup"><span data-stu-id="30cf6-180">If Unicode is defined, the function call resolves to D3DXCreateTextureFromResourceExW.</span></span> <span data-ttu-id="30cf6-181">否則，函式呼叫會解析為 D3DXCreateTextureFromResourceExA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="30cf6-181">Otherwise, the function call resolves to D3DXCreateTextureFromResourceExA because ANSI strings are being used.</span></span>

<span data-ttu-id="30cf6-182">要載入的資源必須是 RT \_ 點陣圖或 rt RCDATA 類型 \_ 。</span><span class="sxs-lookup"><span data-stu-id="30cf6-182">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="30cf6-183">資源類型 RT \_ RCDATA 可用來載入點陣圖以外的格式 (例如 tga、.jpg 和 dds) 。</span><span class="sxs-lookup"><span data-stu-id="30cf6-183">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="30cf6-184">此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="30cf6-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="30cf6-185">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="30cf6-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30cf6-186">規格需求</span><span class="sxs-lookup"><span data-stu-id="30cf6-186">Requirements</span></span>



| <span data-ttu-id="30cf6-187">需求</span><span class="sxs-lookup"><span data-stu-id="30cf6-187">Requirement</span></span> | <span data-ttu-id="30cf6-188">值</span><span class="sxs-lookup"><span data-stu-id="30cf6-188">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30cf6-189">標頭</span><span class="sxs-lookup"><span data-stu-id="30cf6-189">Header</span></span><br/>  | <dl> <span data-ttu-id="30cf6-190"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="30cf6-190"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="30cf6-191">程式庫</span><span class="sxs-lookup"><span data-stu-id="30cf6-191">Library</span></span><br/> | <dl> <span data-ttu-id="30cf6-192"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="30cf6-192"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="30cf6-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30cf6-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30cf6-194">**D3DXCreateTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="30cf6-194">**D3DXCreateTextureFromResource**</span></span>](d3dxcreatetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="30cf6-195">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="30cf6-195">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
