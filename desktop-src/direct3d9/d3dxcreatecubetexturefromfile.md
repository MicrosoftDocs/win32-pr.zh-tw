---
description: 從檔案建立 cube 紋理。
ms.assetid: 7ff3b051-568c-4c77-b8a6-b626ba156eb1
title: 'D3DXCreateCubeTextureFromFile 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2071a1d1e16e769d1a0623138e24c2e0fbab85e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981837"
---
# <a name="d3dxcreatecubetexturefromfile-function"></a><span data-ttu-id="37443-103">D3DXCreateCubeTextureFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="37443-103">D3DXCreateCubeTextureFromFile function</span></span>

<span data-ttu-id="37443-104">從檔案建立 cube 紋理。</span><span class="sxs-lookup"><span data-stu-id="37443-104">Creates a cube texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="37443-105">語法</span><span class="sxs-lookup"><span data-stu-id="37443-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="37443-106">參數</span><span class="sxs-lookup"><span data-stu-id="37443-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37443-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37443-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37443-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="37443-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="37443-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與 cube 材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="37443-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="37443-110">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37443-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37443-111">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37443-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37443-112">指定檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="37443-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="37443-113">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="37443-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="37443-114">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="37443-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="37443-115">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="37443-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="37443-116">*ppCubeTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="37443-116">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37443-117">類型： **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="37443-117">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="37443-118">[**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)介面指標的位址，表示已建立的 cube 紋理物件。</span><span class="sxs-lookup"><span data-stu-id="37443-118">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37443-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="37443-119">Return value</span></span>

<span data-ttu-id="37443-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="37443-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="37443-121">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="37443-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="37443-122">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL、D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="37443-122">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="37443-123">備註</span><span class="sxs-lookup"><span data-stu-id="37443-123">Remarks</span></span>

<span data-ttu-id="37443-124">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="37443-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="37443-125">如果已定義 Unicode，函式呼叫會解析為 **D3DXCreateCubeTextureFromFileW**。</span><span class="sxs-lookup"><span data-stu-id="37443-125">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromFileW**.</span></span> <span data-ttu-id="37443-126">否則，函式呼叫會解析為 **D3DXCreateCubeTextureFromFileA** ，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="37443-126">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromFileA** because ANSI strings are being used.</span></span>

<span data-ttu-id="37443-127">函數相當於 D3DXCreateCubeTextureFromFileEx (pDevice、pSrcFile、D3DX \_ DEFAULT、D3DX \_ DEFAULT、0、D3DFMT \_ UNKNOWN、D3DPOOL \_ MANAGED、D3DX \_ default、D3DX \_ default、0、 **null**、 **null**、ppCubeTexture) 。</span><span class="sxs-lookup"><span data-stu-id="37443-127">The function is equivalent to D3DXCreateCubeTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="37443-128">此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="37443-128">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="37443-129">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="37443-129">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="37443-130">請注意，從 IDirect3DDevice9 物件呼叫時，使用這個函式所建立的資源將會放置在 D3DPOOL MANAGED 所表示的記憶體類別中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="37443-130">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="37443-131">從 IDirect3DDevice9Ex 物件呼叫這個方法時，資源會放在 D3DPOOL 預設值所表示的 memory 類別中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="37443-131">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="37443-132">篩選會自動套用至使用這個方法所建立的材質。</span><span class="sxs-lookup"><span data-stu-id="37443-132">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="37443-133">篩選相當於 \_ \_ \| \_ \_ 在 [D3DX \_ 篩選](d3dx-filter.md)中 D3DX 篩選三角形 D3DX 篩選遞色。</span><span class="sxs-lookup"><span data-stu-id="37443-133">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="37443-134">**D3DXCreateCubeTextureFromFile** 會使用 DirectDraw 介面 (DDS) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="37443-134">**D3DXCreateCubeTextureFromFile** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="37443-135">[DirectX 材質編輯器] (Dxtex.exe) 可讓您從其他檔案格式產生 cube 對應，並以 DDS 檔案格式儲存。</span><span class="sxs-lookup"><span data-stu-id="37443-135">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="37443-136">您可以從 DirectX SDK 取得 Dxtex.exe 並瞭解它的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="37443-136">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="37443-137">如需有關 DirectX SDK 的資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)。</span><span class="sxs-lookup"><span data-stu-id="37443-137">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="37443-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="37443-138">Requirements</span></span>



| <span data-ttu-id="37443-139">需求</span><span class="sxs-lookup"><span data-stu-id="37443-139">Requirement</span></span> | <span data-ttu-id="37443-140">值</span><span class="sxs-lookup"><span data-stu-id="37443-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37443-141">標頭</span><span class="sxs-lookup"><span data-stu-id="37443-141">Header</span></span><br/>  | <dl> <span data-ttu-id="37443-142"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="37443-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="37443-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="37443-143">Library</span></span><br/> | <dl> <span data-ttu-id="37443-144"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="37443-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="37443-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37443-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37443-146">**D3DXCreateCubeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="37443-146">**D3DXCreateCubeTextureFromFileEx**</span></span>](d3dxcreatecubetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="37443-147">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="37443-147">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
