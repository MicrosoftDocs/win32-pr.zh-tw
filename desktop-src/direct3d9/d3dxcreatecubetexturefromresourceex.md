---
description: 從字串所指定的資源建立 cube 紋理。 這是比 D3DXCreateCubeTextureFromResource 更先進的函式。
ms.assetid: 4d263386-8270-4967-8ef5-e9ac69e502a5
title: 'D3DXCreateCubeTextureFromResourceEx 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ed77556681e2ad43302b8608dc213b3ad0f0209
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323247"
---
# <a name="d3dxcreatecubetexturefromresourceex-function"></a><span data-ttu-id="54b0f-104">D3DXCreateCubeTextureFromResourceEx 函式</span><span class="sxs-lookup"><span data-stu-id="54b0f-104">D3DXCreateCubeTextureFromResourceEx function</span></span>

<span data-ttu-id="54b0f-105">從字串所指定的資源建立 cube 紋理。</span><span class="sxs-lookup"><span data-stu-id="54b0f-105">Creates a cube texture from a resource specified by a string.</span></span> <span data-ttu-id="54b0f-106">這是比 [**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md)更先進的函式。</span><span class="sxs-lookup"><span data-stu-id="54b0f-106">This is a more advanced function than [**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="54b0f-107">語法</span><span class="sxs-lookup"><span data-stu-id="54b0f-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    HMODULE                hSrcModule,
  _In_    LPCTSTR                pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="54b0f-108">參數</span><span class="sxs-lookup"><span data-stu-id="54b0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54b0f-109">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="54b0f-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54b0f-110">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="54b0f-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="54b0f-111">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與 cube 材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="54b0f-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="54b0f-112">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="54b0f-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54b0f-113">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54b0f-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54b0f-114">資源所在模組的控制碼，或與作業系統用來建立目前進程的映射相關聯的模組之 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="54b0f-114">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="54b0f-115">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="54b0f-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54b0f-116">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54b0f-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54b0f-117">指定資源名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="54b0f-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="54b0f-118">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="54b0f-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="54b0f-119">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="54b0f-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="54b0f-120">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="54b0f-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="54b0f-121">*大小* \[在\]</span><span class="sxs-lookup"><span data-stu-id="54b0f-121">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54b0f-122">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54b0f-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54b0f-123">立方體材質的寬度和高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="54b0f-123">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="54b0f-124">例如，如果 cube 材質是8圖元 x 8 圖元的 cube，此參數的值應該是8。</span><span class="sxs-lookup"><span data-stu-id="54b0f-124">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span> <span data-ttu-id="54b0f-125">如果這個值是0或 D3DX \_ 預設值，就會從檔案取得維度。</span><span class="sxs-lookup"><span data-stu-id="54b0f-125">If this value is 0 or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="54b0f-126">*MipLevels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="54b0f-126">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54b0f-127">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54b0f-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54b0f-128">要求的 mip 層級數目。</span><span class="sxs-lookup"><span data-stu-id="54b0f-128">Number of mip levels requested.</span></span> <span data-ttu-id="54b0f-129">如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="54b0f-129">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="54b0f-130">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="54b0f-130">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54b0f-131">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54b0f-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54b0f-132">0或 D3DUSAGE \_ RENDERTARGET，或 D3DUSAGE \_ DYNAMIC。</span><span class="sxs-lookup"><span data-stu-id="54b0f-132">0 or D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="54b0f-133">將此旗標設定為 D3DUSAGE \_ RENDERTARGET 表示介面要當做轉譯目標使用。</span><span class="sxs-lookup"><span data-stu-id="54b0f-133">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="54b0f-134">然後，您可以將資源傳遞給 [**SetRenderTarget**](/windows/desktop/api)方法的 *pNewRenderTarget* 參數。</span><span class="sxs-lookup"><span data-stu-id="54b0f-134">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="54b0f-135">如果指定了 D3DUSAGE \_ RENDERTARGET，應用程式應該藉由呼叫 [**CheckDeviceFormat**](/windows/desktop/api)來檢查裝置是否支援這項操作。</span><span class="sxs-lookup"><span data-stu-id="54b0f-135">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="54b0f-136">D3DUSAGE \_ DYNAMIC 表示介面應該以動態方式處理。</span><span class="sxs-lookup"><span data-stu-id="54b0f-136">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="54b0f-137">如需使用動態紋理的詳細資訊，請參閱 [使用動態紋理](performance-optimizations.md)。</span><span class="sxs-lookup"><span data-stu-id="54b0f-137">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="54b0f-138">*格式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="54b0f-138">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54b0f-139">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="54b0f-139">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="54b0f-140">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述 cube 材質所要求的像素格式。</span><span class="sxs-lookup"><span data-stu-id="54b0f-140">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="54b0f-141">傳回的 cube 材質可能與以 *格式* 指定的格式不同。</span><span class="sxs-lookup"><span data-stu-id="54b0f-141">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="54b0f-142">應用程式應該檢查傳回的 cube 材質格式。</span><span class="sxs-lookup"><span data-stu-id="54b0f-142">Applications should check the format of the returned cube texture.</span></span> <span data-ttu-id="54b0f-143">如果 [D3DFMT \_ 未知](other-d3dx-constants.md)，就會從檔案中取得格式。</span><span class="sxs-lookup"><span data-stu-id="54b0f-143">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="54b0f-144">如果從檔案 D3DFMT \_ \_ ，格式會與檔案中的格式完全相同，而且如果這違反裝置功能，呼叫就會失敗。</span><span class="sxs-lookup"><span data-stu-id="54b0f-144">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="54b0f-145">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="54b0f-145">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54b0f-146">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="54b0f-146">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="54b0f-147">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置 cube 材質的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="54b0f-147">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="54b0f-148">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="54b0f-148">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54b0f-149">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54b0f-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54b0f-150">一或多個 [D3DX \_ 篩選](d3dx-filter.md)的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="54b0f-150">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="54b0f-151">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="54b0f-151">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="54b0f-152">*MipFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="54b0f-152">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54b0f-153">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54b0f-153">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54b0f-154">一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="54b0f-154">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="54b0f-155">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選方塊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="54b0f-155">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="54b0f-156">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="54b0f-156">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54b0f-157">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="54b0f-157">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="54b0f-158">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。</span><span class="sxs-lookup"><span data-stu-id="54b0f-158">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="54b0f-159">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="54b0f-159">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="54b0f-160">Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。</span><span class="sxs-lookup"><span data-stu-id="54b0f-160">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="54b0f-161">因此，若是不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="54b0f-161">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="54b0f-162">*pSrcInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="54b0f-162">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="54b0f-163">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="54b0f-163">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="54b0f-164">[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會以來源影像檔案中的資料描述來填滿，或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="54b0f-164">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="54b0f-165">*pPalette* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="54b0f-165">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54b0f-166">類型： **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="54b0f-166">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="54b0f-167">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，代表要填入的256色調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="54b0f-167">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="54b0f-168">*ppCubeTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="54b0f-168">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54b0f-169">類型： **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="54b0f-169">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="54b0f-170">[**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)介面指標的位址，表示已建立的 cube 紋理物件。</span><span class="sxs-lookup"><span data-stu-id="54b0f-170">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54b0f-171">傳回值</span><span class="sxs-lookup"><span data-stu-id="54b0f-171">Return value</span></span>

<span data-ttu-id="54b0f-172">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54b0f-172">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54b0f-173">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="54b0f-173">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="54b0f-174">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="54b0f-174">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="54b0f-175">備註</span><span class="sxs-lookup"><span data-stu-id="54b0f-175">Remarks</span></span>

<span data-ttu-id="54b0f-176">編譯器設定會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="54b0f-176">The compiler setting determines the function version.</span></span> <span data-ttu-id="54b0f-177">如果已定義 Unicode，函式呼叫會解析為 **D3DXCreateCubeTextureFromResourceExW**。</span><span class="sxs-lookup"><span data-stu-id="54b0f-177">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromResourceExW**.</span></span> <span data-ttu-id="54b0f-178">否則，函式呼叫會解析為 **D3DXCreateCubeTextureFromResourceExA** ，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="54b0f-178">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromResourceExA** because ANSI strings are being used.</span></span>

<span data-ttu-id="54b0f-179">此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="54b0f-179">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="54b0f-180">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="54b0f-180">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="54b0f-181">Cube 紋理不同于其他表面，因為它們是表面的集合。</span><span class="sxs-lookup"><span data-stu-id="54b0f-181">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="54b0f-182">若要使用 cube 材質來呼叫 [**SetRenderTarget**](/windows/desktop/api) ，您必須使用 [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) 選取個別臉部，並將產生的介面傳遞至 **SetRenderTarget**。</span><span class="sxs-lookup"><span data-stu-id="54b0f-182">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

<span data-ttu-id="54b0f-183">**D3DXCreateCubeTextureFromResourceEx** 會使用 DirectDraw 介面 (DDS) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="54b0f-183">**D3DXCreateCubeTextureFromResourceEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="54b0f-184">[DirectX 材質編輯器] (Dxtex.exe) 可讓您從其他檔案格式產生 cube 對應，並以 DDS 檔案格式儲存。</span><span class="sxs-lookup"><span data-stu-id="54b0f-184">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="54b0f-185">您可以從 DirectX SDK 取得 Dxtex.exe 並瞭解它的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="54b0f-185">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="54b0f-186">如需有關 DirectX SDK 的資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)。</span><span class="sxs-lookup"><span data-stu-id="54b0f-186">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54b0f-187">規格需求</span><span class="sxs-lookup"><span data-stu-id="54b0f-187">Requirements</span></span>



| <span data-ttu-id="54b0f-188">需求</span><span class="sxs-lookup"><span data-stu-id="54b0f-188">Requirement</span></span> | <span data-ttu-id="54b0f-189">值</span><span class="sxs-lookup"><span data-stu-id="54b0f-189">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54b0f-190">標頭</span><span class="sxs-lookup"><span data-stu-id="54b0f-190">Header</span></span><br/>  | <dl> <span data-ttu-id="54b0f-191"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="54b0f-191"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="54b0f-192">程式庫</span><span class="sxs-lookup"><span data-stu-id="54b0f-192">Library</span></span><br/> | <dl> <span data-ttu-id="54b0f-193"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="54b0f-193"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="54b0f-194">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54b0f-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54b0f-195">**D3DXCreateCubeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="54b0f-195">**D3DXCreateCubeTextureFromResource**</span></span>](d3dxcreatecubetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="54b0f-196">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="54b0f-196">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
