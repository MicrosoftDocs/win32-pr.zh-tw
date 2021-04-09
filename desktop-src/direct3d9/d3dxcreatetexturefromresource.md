---
description: 從資源建立紋理。
ms.assetid: 7c841f21-5565-4923-a2fe-bbd618616f87
title: 'D3DXCreateTextureFromResource 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ce9101caed2a60dc3be7fe0039a1e391423f1fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103853987"
---
# <a name="d3dxcreatetexturefromresource-function"></a><span data-ttu-id="43cf7-103">D3DXCreateTextureFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="43cf7-103">D3DXCreateTextureFromResource function</span></span>

<span data-ttu-id="43cf7-104">從資源建立紋理。</span><span class="sxs-lookup"><span data-stu-id="43cf7-104">Creates a texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="43cf7-105">語法</span><span class="sxs-lookup"><span data-stu-id="43cf7-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromResource(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  HMODULE            hSrcModule,
  _In_  LPCTSTR            pSrcResource,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="43cf7-106">參數</span><span class="sxs-lookup"><span data-stu-id="43cf7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43cf7-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="43cf7-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cf7-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="43cf7-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="43cf7-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="43cf7-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="43cf7-110">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="43cf7-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cf7-111">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43cf7-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43cf7-112">資源所在之模組的控制碼，或與作業系統用來建立目前進程的映射相關聯的模組的 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="43cf7-112">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="43cf7-113">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="43cf7-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cf7-114">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43cf7-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43cf7-115">指定資源名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="43cf7-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="43cf7-116">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="43cf7-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="43cf7-117">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="43cf7-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="43cf7-118">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="43cf7-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="43cf7-119">*ppTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="43cf7-119">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43cf7-120">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="43cf7-120">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="43cf7-121">[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面指標的位址，表示所建立的材質物件。</span><span class="sxs-lookup"><span data-stu-id="43cf7-121">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43cf7-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="43cf7-122">Return value</span></span>

<span data-ttu-id="43cf7-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43cf7-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43cf7-124">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="43cf7-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="43cf7-125">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="43cf7-125">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="43cf7-126">備註</span><span class="sxs-lookup"><span data-stu-id="43cf7-126">Remarks</span></span>

<span data-ttu-id="43cf7-127">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="43cf7-127">The compiler setting also determines the function version.</span></span> <span data-ttu-id="43cf7-128">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateTextureFromResourceW。</span><span class="sxs-lookup"><span data-stu-id="43cf7-128">If Unicode is defined, the function call resolves to D3DXCreateTextureFromResourceW.</span></span> <span data-ttu-id="43cf7-129">否則，函式呼叫會解析為 D3DXCreateTextureFromResourceA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="43cf7-129">Otherwise, the function call resolves to D3DXCreateTextureFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="43cf7-130">函數相當於 D3DXCreateTextureFromResourceEx (pDevice、hSrcModule、pSrcResource、D3DX \_ default、D3DX \_ DEFAULT、D3DX \_ default、0、D3DFMT \_ UNKNOWN、D3DPOOL \_ MANAGED、D3DX \_ default、D3DX \_ default、0、 **null**、 **null**、ppTexture) 。</span><span class="sxs-lookup"><span data-stu-id="43cf7-130">The function is equivalent to D3DXCreateTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="43cf7-131">要載入的資源必須是 RT \_ 點陣圖或 rt RCDATA 類型 \_ 。</span><span class="sxs-lookup"><span data-stu-id="43cf7-131">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="43cf7-132">資源類型 RT \_ RCDATA 可用來載入點陣圖以外的格式 (例如 tga、.jpg 和 dds) 。</span><span class="sxs-lookup"><span data-stu-id="43cf7-132">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="43cf7-133">此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="43cf7-133">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="43cf7-134">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="43cf7-134">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="43cf7-135">請注意，從 IDirect3DDevice9 物件呼叫時，使用這個函式所建立的資源將會放置在 D3DPOOL MANAGED 所表示的記憶體類別中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="43cf7-135">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="43cf7-136">從 IDirect3DDevice9Ex 物件呼叫這個方法時，資源會放在 D3DPOOL 預設值所表示的 memory 類別中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="43cf7-136">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="43cf7-137">篩選會自動套用至使用這個方法所建立的材質。</span><span class="sxs-lookup"><span data-stu-id="43cf7-137">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="43cf7-138">篩選相當於 \_ \_ \| \_ \_ 在 [D3DX \_ 篩選](d3dx-filter.md)中 D3DX 篩選三角形 D3DX 篩選遞色。</span><span class="sxs-lookup"><span data-stu-id="43cf7-138">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43cf7-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="43cf7-139">Requirements</span></span>



| <span data-ttu-id="43cf7-140">需求</span><span class="sxs-lookup"><span data-stu-id="43cf7-140">Requirement</span></span> | <span data-ttu-id="43cf7-141">值</span><span class="sxs-lookup"><span data-stu-id="43cf7-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43cf7-142">標頭</span><span class="sxs-lookup"><span data-stu-id="43cf7-142">Header</span></span><br/>  | <dl> <span data-ttu-id="43cf7-143"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="43cf7-143"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="43cf7-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="43cf7-144">Library</span></span><br/> | <dl> <span data-ttu-id="43cf7-145"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="43cf7-145"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="43cf7-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43cf7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43cf7-147">**D3DXCreateTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="43cf7-147">**D3DXCreateTextureFromResourceEx**</span></span>](d3dxcreatetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="43cf7-148">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="43cf7-148">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
