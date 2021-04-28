---
description: D3DXCreateVolumeTextureFromFile 函式-從檔案建立磁片區材質。
ms.assetid: e68ac4bb-a89a-41a1-b2ba-40a1ac519e3d
title: 'D3DXCreateVolumeTextureFromFile 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c9355148c0b91a03aabe863fb20b3e312e30784
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094298"
---
# <a name="d3dxcreatevolumetexturefromfile-function"></a><span data-ttu-id="a5c7c-103">D3DXCreateVolumeTextureFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="a5c7c-103">D3DXCreateVolumeTextureFromFile function</span></span>

<span data-ttu-id="a5c7c-104">從檔案建立磁片區材質。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-104">Creates a volume texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5c7c-105">語法</span><span class="sxs-lookup"><span data-stu-id="a5c7c-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="a5c7c-106">參數</span><span class="sxs-lookup"><span data-stu-id="a5c7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5c7c-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a5c7c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5c7c-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a5c7c-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a5c7c-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與磁片區材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="a5c7c-110">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a5c7c-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5c7c-111">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5c7c-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5c7c-112">指定檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-112">Pointer to a string that specifies the file name.</span></span> <span data-ttu-id="a5c7c-113">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="a5c7c-114">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="a5c7c-115">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a5c7c-116">*ppVolumeTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a5c7c-116">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5c7c-117">類型： **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="a5c7c-117">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="a5c7c-118">[**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)介面指標的位址，表示所建立的材質物件。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-118">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5c7c-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5c7c-119">Return value</span></span>

<span data-ttu-id="a5c7c-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a5c7c-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a5c7c-121">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a5c7c-122">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5c7c-123">備註</span><span class="sxs-lookup"><span data-stu-id="a5c7c-123">Remarks</span></span>

<span data-ttu-id="a5c7c-124">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="a5c7c-125">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateVolumeTextureFromFileW。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-125">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromFileW.</span></span> <span data-ttu-id="a5c7c-126">否則，函式呼叫會解析為 D3DXCreateVolumeTextureFromFileA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-126">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="a5c7c-127">函數相當於 D3DXCreateVolumeTextureFromFileEx (pDevice、pSrcFile、D3DX \_ DEFAULT、D3DX \_ DEFAULT、D3DX \_ default、D3DX \_ DEFAULT、0、D3DFMT \_ UNKNOWN、D3DPOOL \_ MANAGED、D3DX \_ Default、D3DX \_ default、0、 **null**、 **null**、ppVolumeTexture) 。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-127">The function is equivalent to D3DXCreateVolumeTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="a5c7c-128">此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-128">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="a5c7c-129">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-129">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="a5c7c-130">Mipmapped 紋理會自動以載入的材質填滿每個層級。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-130">Mipmapped textures automatically have each level filled with the loaded texture.</span></span>

<span data-ttu-id="a5c7c-131">將影像載入 mipmapped 材質時，某些裝置無法進入1x1 影像，而且此函式將會失敗。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-131">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="a5c7c-132">如果發生這種情況，則必須以手動方式載入映射。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-132">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="a5c7c-133">請注意，從 IDirect3DDevice9 物件呼叫時，使用這個函式所建立的資源將會放置在 D3DPOOL MANAGED 所表示的記憶體類別中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-133">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="a5c7c-134">從 IDirect3DDevice9Ex 物件呼叫這個方法時，資源會放在 D3DPOOL 預設值所表示的 memory 類別中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-134">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="a5c7c-135">篩選會自動套用至使用這個方法所建立的材質。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-135">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="a5c7c-136">篩選相當於 \_ \_ \| \_ \_ 在 [D3DX \_ 篩選](d3dx-filter.md)中 D3DX 篩選三角形 D3DX 篩選遞色。</span><span class="sxs-lookup"><span data-stu-id="a5c7c-136">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5c7c-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5c7c-137">Requirements</span></span>



| <span data-ttu-id="a5c7c-138">需求</span><span class="sxs-lookup"><span data-stu-id="a5c7c-138">Requirement</span></span> | <span data-ttu-id="a5c7c-139">值</span><span class="sxs-lookup"><span data-stu-id="a5c7c-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c7c-140">標頭</span><span class="sxs-lookup"><span data-stu-id="a5c7c-140">Header</span></span><br/>  | <dl> <span data-ttu-id="a5c7c-141"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="a5c7c-141"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a5c7c-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="a5c7c-142">Library</span></span><br/> | <dl> <span data-ttu-id="a5c7c-143"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5c7c-143"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a5c7c-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5c7c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5c7c-145">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="a5c7c-145">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="a5c7c-146">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="a5c7c-146">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="a5c7c-147">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="a5c7c-147">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="a5c7c-148">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="a5c7c-148">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="a5c7c-149">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="a5c7c-149">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="a5c7c-150">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="a5c7c-150">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
