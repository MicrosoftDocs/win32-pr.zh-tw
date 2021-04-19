---
description: 從記憶體中的檔案建立 cube 紋理。
ms.assetid: f7e99d5a-5479-4f0b-b040-bb07e7e37666
title: 'D3DXCreateCubeTextureFromFileInMemory 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f1d6de3fba0dcbda959a2811ec665ebc4a6541c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999015"
---
# <a name="d3dxcreatecubetexturefromfileinmemory-function"></a><span data-ttu-id="25482-103">D3DXCreateCubeTextureFromFileInMemory 函式</span><span class="sxs-lookup"><span data-stu-id="25482-103">D3DXCreateCubeTextureFromFileInMemory function</span></span>

<span data-ttu-id="25482-104">從記憶體中的檔案建立 cube 紋理。</span><span class="sxs-lookup"><span data-stu-id="25482-104">Creates a cube texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="25482-105">語法</span><span class="sxs-lookup"><span data-stu-id="25482-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  UINT                   SrcDataSize,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="25482-106">參數</span><span class="sxs-lookup"><span data-stu-id="25482-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25482-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25482-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25482-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="25482-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="25482-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與 cube 材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="25482-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="25482-110">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25482-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25482-111">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25482-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25482-112">要建立立方體貼圖之記憶體中的檔案指標。</span><span class="sxs-lookup"><span data-stu-id="25482-112">Pointer to the file in memory from which to create the cubemap.</span></span> <span data-ttu-id="25482-113">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="25482-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="25482-114">*SrcDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25482-114">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25482-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25482-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25482-116">檔案在記憶體中的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="25482-116">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="25482-117">*ppCubeTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="25482-117">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25482-118">類型： **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="25482-118">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="25482-119">[**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)介面指標的位址，表示已建立的 cube 紋理物件。</span><span class="sxs-lookup"><span data-stu-id="25482-119">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25482-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="25482-120">Return value</span></span>

<span data-ttu-id="25482-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="25482-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="25482-122">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="25482-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="25482-123">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="25482-123">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="25482-124">備註</span><span class="sxs-lookup"><span data-stu-id="25482-124">Remarks</span></span>

<span data-ttu-id="25482-125">此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="25482-125">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="25482-126">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="25482-126">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="25482-127">函數相當於 D3DXCreateCubeTextureFromFileInMemoryEx (pDevice、pSrcData、SrcDataSize、D3DX \_ default、D3DX \_ default、0、D3DFMT \_ UNKNOWN、D3DPOOL \_ MANAGED、D3DX \_ default、D3DX \_ default、0、 **null**、 **null**、ppCubeTexture) 。</span><span class="sxs-lookup"><span data-stu-id="25482-127">The function is equivalent to D3DXCreateCubeTextureFromFileInMemoryEx(pDevice, pSrcData, SrcDataSize, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="25482-128">請注意，從 IDirect3DDevice9 物件呼叫時，使用這個函式所建立的資源將會放置在 D3DPOOL MANAGED 所表示的記憶體類別中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="25482-128">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="25482-129">從 IDirect3DDevice9Ex 物件呼叫這個方法時，資源會放在 D3DPOOL 預設值所表示的 memory 類別中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="25482-129">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="25482-130">這個方法是設計用來載入儲存為 RT RCDATA 的影像檔 \_ ，這是應用程式定義的資源， (原始資料) 。</span><span class="sxs-lookup"><span data-stu-id="25482-130">This method is designed to be used for loading image files stored as RT\_RCDATA, which is an application-defined resource (raw data).</span></span> <span data-ttu-id="25482-131">否則，此方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="25482-131">Otherwise this method will fail.</span></span>

<span data-ttu-id="25482-132">篩選會自動套用至使用這個方法所建立的材質。</span><span class="sxs-lookup"><span data-stu-id="25482-132">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="25482-133">篩選相當於 \_ \_ \| \_ \_ 在 [D3DX \_ 篩選](d3dx-filter.md)中 D3DX 篩選三角形 D3DX 篩選遞色。</span><span class="sxs-lookup"><span data-stu-id="25482-133">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="25482-134">**D3DXCreateCubeTextureFromFileInMemory** 會使用 DirectDraw 介面 (DDS) 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="25482-134">**D3DXCreateCubeTextureFromFileInMemory** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="25482-135">[DirectX 材質編輯器] (Dxtex.exe) 可讓您從其他檔案格式產生 cube 對應，並以 DDS 檔案格式儲存。</span><span class="sxs-lookup"><span data-stu-id="25482-135">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="25482-136">您可以從 DirectX SDK 取得 Dxtex.exe 並瞭解它的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="25482-136">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="25482-137">如需有關 DirectX SDK 的資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)。</span><span class="sxs-lookup"><span data-stu-id="25482-137">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25482-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="25482-138">Requirements</span></span>



| <span data-ttu-id="25482-139">需求</span><span class="sxs-lookup"><span data-stu-id="25482-139">Requirement</span></span> | <span data-ttu-id="25482-140">值</span><span class="sxs-lookup"><span data-stu-id="25482-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25482-141">標頭</span><span class="sxs-lookup"><span data-stu-id="25482-141">Header</span></span><br/>  | <dl> <span data-ttu-id="25482-142"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="25482-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="25482-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="25482-143">Library</span></span><br/> | <dl> <span data-ttu-id="25482-144"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="25482-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="25482-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25482-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25482-146">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="25482-146">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
