---
description: 從檔案建立紋理。
ms.assetid: 247b0ee2-ee31-4090-b94c-41951b46675f
title: 'D3DXCreateTextureFromFile 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 19453986405ee4d46a3e72145c2117bb113663bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386459"
---
# <a name="d3dxcreatetexturefromfile-function"></a><span data-ttu-id="16ab3-103">D3DXCreateTextureFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="16ab3-103">D3DXCreateTextureFromFile function</span></span>

<span data-ttu-id="16ab3-104">從檔案建立紋理。</span><span class="sxs-lookup"><span data-stu-id="16ab3-104">Creates a texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="16ab3-105">語法</span><span class="sxs-lookup"><span data-stu-id="16ab3-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFile(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCTSTR            pSrcFile,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="16ab3-106">參數</span><span class="sxs-lookup"><span data-stu-id="16ab3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16ab3-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16ab3-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16ab3-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="16ab3-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="16ab3-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="16ab3-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="16ab3-110">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16ab3-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16ab3-111">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16ab3-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16ab3-112">指定檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="16ab3-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="16ab3-113">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="16ab3-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="16ab3-114">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="16ab3-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="16ab3-115">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="16ab3-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="16ab3-116">*ppTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="16ab3-116">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16ab3-117">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="16ab3-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="16ab3-118">[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面指標的位址，表示所建立的材質物件。</span><span class="sxs-lookup"><span data-stu-id="16ab3-118">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16ab3-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="16ab3-119">Return value</span></span>

<span data-ttu-id="16ab3-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="16ab3-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="16ab3-121">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="16ab3-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="16ab3-122">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="16ab3-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="16ab3-123">備註</span><span class="sxs-lookup"><span data-stu-id="16ab3-123">Remarks</span></span>

<span data-ttu-id="16ab3-124">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="16ab3-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="16ab3-125">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateTextureFromFileW。</span><span class="sxs-lookup"><span data-stu-id="16ab3-125">If Unicode is defined, the function call resolves to D3DXCreateTextureFromFileW.</span></span> <span data-ttu-id="16ab3-126">否則，函式呼叫會解析為 D3DXCreateTextureFromFileA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="16ab3-126">Otherwise, the function call resolves to D3DXCreateTextureFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="16ab3-127">此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="16ab3-127">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="16ab3-128">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="16ab3-128">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="16ab3-129">函數相當於 D3DXCreateTextureFromFileEx (pDevice、pSrcFile、D3DX \_ DEFAULT、D3DX \_ DEFAULT、D3DX \_ default、0、D3DFMT \_ UNKNOWN、D3DPOOL \_ MANAGED、D3DX \_ default、D3DX \_ default、0、 **null**、 **null**、ppTexture) 。</span><span class="sxs-lookup"><span data-stu-id="16ab3-129">The function is equivalent to D3DXCreateTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="16ab3-130">Mipmapped 紋理會自動以載入的材質填滿每個層級。</span><span class="sxs-lookup"><span data-stu-id="16ab3-130">Mipmapped textures automatically have each level filled with the loaded texture.</span></span>

<span data-ttu-id="16ab3-131">將影像載入 mipmapped 材質時，某些裝置無法進入1x1 影像，而且此函式將會失敗。</span><span class="sxs-lookup"><span data-stu-id="16ab3-131">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="16ab3-132">如果發生這種情況，則必須以手動方式載入映射。</span><span class="sxs-lookup"><span data-stu-id="16ab3-132">If this happens, the images need to be loaded manually.</span></span>

<span data-ttu-id="16ab3-133">請注意，使用此函式建立的資源會放在 D3DPOOL MANAGED 所表示的記憶體類別中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="16ab3-133">Note that a resource created with this function will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span>

<span data-ttu-id="16ab3-134">篩選會自動套用至使用這個方法所建立的材質。</span><span class="sxs-lookup"><span data-stu-id="16ab3-134">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="16ab3-135">篩選相當於 \_ \_ \| \_ \_ 在 [D3DX \_ 篩選](d3dx-filter.md)中 D3DX 篩選三角形 D3DX 篩選遞色。</span><span class="sxs-lookup"><span data-stu-id="16ab3-135">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="16ab3-136">若要在使用 **D3DXCreateTextureFromFile** 時獲得最佳效能：</span><span class="sxs-lookup"><span data-stu-id="16ab3-136">For the best performance when using **D3DXCreateTextureFromFile**:</span></span>

1.  <span data-ttu-id="16ab3-137">在載入時間進行映射調整和格式轉換可能會很慢。</span><span class="sxs-lookup"><span data-stu-id="16ab3-137">Doing image scaling and format conversion at load time can be slow.</span></span> <span data-ttu-id="16ab3-138">以將使用的格式和解析度儲存影像。</span><span class="sxs-lookup"><span data-stu-id="16ab3-138">Store images in the format and resolution they will be used.</span></span> <span data-ttu-id="16ab3-139">如果目標硬體需要兩個維度的強大功能，請使用兩個維度的強大功能來建立和儲存影像。</span><span class="sxs-lookup"><span data-stu-id="16ab3-139">If the target hardware requires power of two dimensions, create and store images using power of two dimensions.</span></span>
2.  <span data-ttu-id="16ab3-140">請考慮使用 DirectDraw 介面 (DDS) 檔。</span><span class="sxs-lookup"><span data-stu-id="16ab3-140">Consider using DirectDraw surface (DDS) files.</span></span> <span data-ttu-id="16ab3-141">因為 DDS 檔案可以用來代表任何 Direct3D 9 材質格式，所以很容易 D3DX 閱讀。</span><span class="sxs-lookup"><span data-stu-id="16ab3-141">Because DDS files can be used to represent any Direct3D 9 texture format, they are very easy for D3DX to read.</span></span> <span data-ttu-id="16ab3-142">此外，他們也可以儲存 mipmap，讓任何 mipmap 產生的演算法都能用來撰寫映射。</span><span class="sxs-lookup"><span data-stu-id="16ab3-142">Also, they can store mipmaps, so any mipmap-generation algorithms can be used to author the images.</span></span>

## <a name="requirements"></a><span data-ttu-id="16ab3-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="16ab3-143">Requirements</span></span>



| <span data-ttu-id="16ab3-144">需求</span><span class="sxs-lookup"><span data-stu-id="16ab3-144">Requirement</span></span> | <span data-ttu-id="16ab3-145">值</span><span class="sxs-lookup"><span data-stu-id="16ab3-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16ab3-146">標頭</span><span class="sxs-lookup"><span data-stu-id="16ab3-146">Header</span></span><br/>  | <dl> <span data-ttu-id="16ab3-147"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="16ab3-147"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="16ab3-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="16ab3-148">Library</span></span><br/> | <dl> <span data-ttu-id="16ab3-149"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="16ab3-149"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="16ab3-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16ab3-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16ab3-151">**D3DXCreateTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="16ab3-151">**D3DXCreateTextureFromFileEx**</span></span>](d3dxcreatetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="16ab3-152">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="16ab3-152">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
