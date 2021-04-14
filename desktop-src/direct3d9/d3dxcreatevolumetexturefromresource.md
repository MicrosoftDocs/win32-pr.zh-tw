---
description: 從資源建立磁片區材質。
ms.assetid: 82a0b7aa-69fa-450d-b0d2-769f05fd75ea
title: 'D3DXCreateVolumeTextureFromResource 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5f0a0faf97f773c3174ced22ec7259091d6e07e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514597"
---
# <a name="d3dxcreatevolumetexturefromresource-function"></a><span data-ttu-id="4dd12-103">D3DXCreateVolumeTextureFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="4dd12-103">D3DXCreateVolumeTextureFromResource function</span></span>

<span data-ttu-id="4dd12-104">從資源建立磁片區材質。</span><span class="sxs-lookup"><span data-stu-id="4dd12-104">Creates a volume texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd12-105">語法</span><span class="sxs-lookup"><span data-stu-id="4dd12-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromResource(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="4dd12-106">參數</span><span class="sxs-lookup"><span data-stu-id="4dd12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dd12-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4dd12-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd12-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="4dd12-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="4dd12-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與磁片區材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="4dd12-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="4dd12-110">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4dd12-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd12-111">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4dd12-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4dd12-112">資源所在模組的控制碼，或與作業系統用來建立目前進程的映射相關聯的模組之 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="4dd12-112">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="4dd12-113">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4dd12-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd12-114">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4dd12-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4dd12-115">指定資源名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="4dd12-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="4dd12-116">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="4dd12-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="4dd12-117">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="4dd12-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="4dd12-118">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="4dd12-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4dd12-119">*ppVolumeTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4dd12-119">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd12-120">類型： **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="4dd12-120">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="4dd12-121">[**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)介面指標的位址，表示所建立的材質物件。</span><span class="sxs-lookup"><span data-stu-id="4dd12-121">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dd12-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="4dd12-122">Return value</span></span>

<span data-ttu-id="4dd12-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4dd12-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4dd12-124">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="4dd12-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4dd12-125">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="4dd12-125">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dd12-126">備註</span><span class="sxs-lookup"><span data-stu-id="4dd12-126">Remarks</span></span>

<span data-ttu-id="4dd12-127">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="4dd12-127">The compiler setting also determines the function version.</span></span> <span data-ttu-id="4dd12-128">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateVolumeTextureFromResourceW。</span><span class="sxs-lookup"><span data-stu-id="4dd12-128">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromResourceW.</span></span> <span data-ttu-id="4dd12-129">否則，函式呼叫會解析為 D3DXCreateVolumeTextureFromResourceA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="4dd12-129">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="4dd12-130">函數相當於 D3DXCreateVolumeTextureFromResourceEx (pDevice、hSrcModule、pSrcResource、D3DX \_ default、D3DX \_ DEFAULT、D3DX \_ default、D3DX \_ DEFAULT、0、D3DFMT \_ UNKNOWN、D3DPOOL \_ MANAGED、D3DX \_ Default、D3DX \_ default、0、 **null**、 **null**、ppVolumeTexture) 。</span><span class="sxs-lookup"><span data-stu-id="4dd12-130">The function is equivalent to D3DXCreateVolumeTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="4dd12-131">要載入的資源必須是應用程式定義的資源 (RT \_ RCDATA) 。</span><span class="sxs-lookup"><span data-stu-id="4dd12-131">The resource being loaded must be an application-defined resource (RT\_RCDATA).</span></span>

<span data-ttu-id="4dd12-132">此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="4dd12-132">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="4dd12-133">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="4dd12-133">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="4dd12-134">請注意，從 IDirect3DDevice9 物件呼叫時，使用這個函式所建立的資源將會放置在 D3DPOOL MANAGED 所表示的記憶體類別中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4dd12-134">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="4dd12-135">從 IDirect3DDevice9Ex 物件呼叫這個方法時，資源會放在 D3DPOOL 預設值所表示的 memory 類別中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4dd12-135">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="4dd12-136">篩選會自動套用至使用這個方法所建立的材質。</span><span class="sxs-lookup"><span data-stu-id="4dd12-136">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="4dd12-137">篩選相當於 \_ \_ \| \_ \_ 在 [D3DX \_ 篩選](d3dx-filter.md)中 D3DX 篩選三角形 D3DX 篩選遞色。</span><span class="sxs-lookup"><span data-stu-id="4dd12-137">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4dd12-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="4dd12-138">Requirements</span></span>



| <span data-ttu-id="4dd12-139">需求</span><span class="sxs-lookup"><span data-stu-id="4dd12-139">Requirement</span></span> | <span data-ttu-id="4dd12-140">值</span><span class="sxs-lookup"><span data-stu-id="4dd12-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4dd12-141">標頭</span><span class="sxs-lookup"><span data-stu-id="4dd12-141">Header</span></span><br/>  | <dl> <span data-ttu-id="4dd12-142"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="4dd12-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="4dd12-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="4dd12-143">Library</span></span><br/> | <dl> <span data-ttu-id="4dd12-144"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4dd12-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4dd12-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4dd12-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dd12-146">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="4dd12-146">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="4dd12-147">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="4dd12-147">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="4dd12-148">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="4dd12-148">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="4dd12-149">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="4dd12-149">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="4dd12-150">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="4dd12-150">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="4dd12-151">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="4dd12-151">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
