---
description: 從字串所指定的資源建立磁片區材質。 這是比 D3DXCreateVolumeTextureFromResource 更先進的函式。
ms.assetid: 02f2cb9e-4750-4854-aa74-202426427af5
title: 'D3DXCreateVolumeTextureFromResourceEx 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44d842df2da1d5c3db374e838e0ffd2492683961
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946102"
---
# <a name="d3dxcreatevolumetexturefromresourceex-function"></a><span data-ttu-id="2f4ca-104">D3DXCreateVolumeTextureFromResourceEx 函式</span><span class="sxs-lookup"><span data-stu-id="2f4ca-104">D3DXCreateVolumeTextureFromResourceEx function</span></span>

<span data-ttu-id="2f4ca-105">從字串所指定的資源建立磁片區材質。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-105">Creates a volume texture from a resource specified by a string.</span></span> <span data-ttu-id="2f4ca-106">這是比 [**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md)更先進的函式。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-106">This is a more advanced function than [**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f4ca-107">語法</span><span class="sxs-lookup"><span data-stu-id="2f4ca-107">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    HMODULE                  hSrcModule,
  _In_    LPCTSTR                  pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="2f4ca-108">參數</span><span class="sxs-lookup"><span data-stu-id="2f4ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f4ca-109">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f4ca-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ca-110">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2f4ca-111">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="2f4ca-112">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f4ca-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ca-113">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f4ca-114">資源所在之模組的控制碼，或與作業系統用來建立目前進程的映射相關聯的模組的 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-114">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="2f4ca-115">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f4ca-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ca-116">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f4ca-117">指定資源名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="2f4ca-118">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="2f4ca-119">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="2f4ca-120">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2f4ca-121">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f4ca-121">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ca-122">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f4ca-123">寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-123">Width in pixels.</span></span> <span data-ttu-id="2f4ca-124">如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="2f4ca-125">驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-125">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="2f4ca-126">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f4ca-126">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ca-127">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f4ca-128">高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-128">Height, in pixels.</span></span> <span data-ttu-id="2f4ca-129">如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-129">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="2f4ca-130">驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-130">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="2f4ca-131">*深度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f4ca-131">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ca-132">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f4ca-133">深度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-133">Depth, in pixels.</span></span> <span data-ttu-id="2f4ca-134">如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-134">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="2f4ca-135">驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-135">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="2f4ca-136">*MipLevels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f4ca-136">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ca-137">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-137">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f4ca-138">要求的 mip 層級數目。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-138">Number of mip levels requested.</span></span> <span data-ttu-id="2f4ca-139">如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-139">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="2f4ca-140">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="2f4ca-140">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ca-141">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-141">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f4ca-142">0、D3DUSAGE \_ RENDERTARGET 或 D3DUSAGE \_ DYNAMIC。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-142">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="2f4ca-143">將此旗標設定為 D3DUSAGE \_ RENDERTARGET 表示介面要當做轉譯目標使用。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-143">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="2f4ca-144">然後，您可以將資源傳遞給 [**SetRenderTarget**](/windows/desktop/api)方法的 *pNewRenderTarget* 參數。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-144">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="2f4ca-145">如果 \_ 指定了 D3DUSAGE RENDERTARGET 或 D3DUSAGE \_ DYNAMIC，則必須將集區設定為 D3DPOOL \_ 預設值，而應用程式應藉由呼叫 [**CheckDeviceFormat**](/windows/desktop/api)來檢查裝置是否支援這項操作。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-145">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="2f4ca-146">D3DUSAGE \_ DYNAMIC 表示介面應該以動態方式處理。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-146">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="2f4ca-147">如需使用動態紋理的詳細資訊，請參閱 [使用動態紋理](performance-optimizations.md)。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-147">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f4ca-148">*格式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f4ca-148">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ca-149">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-149">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="2f4ca-150">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述紋理所要求的像素格式。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-150">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="2f4ca-151">傳回的材質可能與以 *格式* 指定的格式不同。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-151">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="2f4ca-152">應用程式應該檢查傳回的材質格式。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-152">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="2f4ca-153">如果 [D3DFMT \_ 未知](other-d3dx-constants.md)，就會從檔案中取得格式。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-153">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="2f4ca-154">如果從檔案 D3DFMT \_ \_ ，格式會與檔案中的格式完全相同，而且如果這違反裝置功能，呼叫就會失敗。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-154">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="2f4ca-155">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="2f4ca-155">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ca-156">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-156">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="2f4ca-157">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置紋理的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-157">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="2f4ca-158">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f4ca-158">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ca-159">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-159">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f4ca-160">一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-160">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="2f4ca-161">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-161">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="2f4ca-162">*MipFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f4ca-162">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ca-163">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-163">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f4ca-164">一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合，可控制影像的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-164">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="2f4ca-165">指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選方塊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-165">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="2f4ca-166">*>colorkey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f4ca-166">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ca-167">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-167">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="2f4ca-168">要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-168">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="2f4ca-169">這一律是32位的 ARGB 色彩，與來源影像格式無關。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-169">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="2f4ca-170">Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-170">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="2f4ca-171">因此，若是不透明的黑色，此值會等於0xFF000000。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-171">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="2f4ca-172">*pSrcInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2f4ca-172">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ca-173">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f4ca-173">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="2f4ca-174">要填入的 [**D3DXIMAGE \_ 資訊**](d3dximage-info.md) 結構的指標，其中包含來源影像檔案中的資料描述或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-174">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2f4ca-175">*pPalette* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2f4ca-175">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ca-176">類型： **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="2f4ca-176">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="2f4ca-177">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，代表要填入的256色調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-177">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2f4ca-178">*ppVolumeTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2f4ca-178">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ca-179">類型： **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="2f4ca-179">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="2f4ca-180">[**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)介面指標的位址，表示所建立的材質物件。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-180">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f4ca-181">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f4ca-181">Return value</span></span>

<span data-ttu-id="2f4ca-182">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-182">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2f4ca-183">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-183">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2f4ca-184">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-184">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f4ca-185">備註</span><span class="sxs-lookup"><span data-stu-id="2f4ca-185">Remarks</span></span>

<span data-ttu-id="2f4ca-186">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-186">The compiler setting also determines the function version.</span></span> <span data-ttu-id="2f4ca-187">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateVolumeTextureFromResourceExW。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-187">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromResourceExW.</span></span> <span data-ttu-id="2f4ca-188">否則，函式呼叫會解析為 D3DXCreateVolumeTextureFromResourceExA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-188">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromResourceExA because ANSI strings are being used.</span></span>

<span data-ttu-id="2f4ca-189">要載入的資源必須是應用程式定義的資源 (RT \_ RCDATA) 。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-189">The resource being loaded must be an application-defined resource (RT\_RCDATA).</span></span>

<span data-ttu-id="2f4ca-190">此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-190">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="2f4ca-191">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-191">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f4ca-192">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f4ca-192">Requirements</span></span>



| <span data-ttu-id="2f4ca-193">需求</span><span class="sxs-lookup"><span data-stu-id="2f4ca-193">Requirement</span></span> | <span data-ttu-id="2f4ca-194">值</span><span class="sxs-lookup"><span data-stu-id="2f4ca-194">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f4ca-195">標頭</span><span class="sxs-lookup"><span data-stu-id="2f4ca-195">Header</span></span><br/>  | <dl> <span data-ttu-id="2f4ca-196"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f4ca-196"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2f4ca-197">程式庫</span><span class="sxs-lookup"><span data-stu-id="2f4ca-197">Library</span></span><br/> | <dl> <span data-ttu-id="2f4ca-198"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f4ca-198"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2f4ca-199">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f4ca-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f4ca-200">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-200">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="2f4ca-201">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-201">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="2f4ca-202">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-202">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="2f4ca-203">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-203">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="2f4ca-204">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="2f4ca-204">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="2f4ca-205">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="2f4ca-205">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
