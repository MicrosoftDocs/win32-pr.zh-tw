---
description: 從記憶體中的檔案建立紋理。
ms.assetid: 3ea811be-7db8-4436-b138-f0102389bb4d
title: 'D3DXCreateTextureFromFileInMemory 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 743a944da52bc6d2ae13b045f854d95b4751712d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696655"
---
# <a name="d3dxcreatetexturefromfileinmemory-function"></a><span data-ttu-id="25be7-103">D3DXCreateTextureFromFileInMemory 函式</span><span class="sxs-lookup"><span data-stu-id="25be7-103">D3DXCreateTextureFromFileInMemory function</span></span>

<span data-ttu-id="25be7-104">從記憶體中的檔案建立紋理。</span><span class="sxs-lookup"><span data-stu-id="25be7-104">Creates a texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="25be7-105">語法</span><span class="sxs-lookup"><span data-stu-id="25be7-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCVOID            pSrcData,
  _In_  UINT               SrcDataSize,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="25be7-106">參數</span><span class="sxs-lookup"><span data-stu-id="25be7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25be7-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25be7-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25be7-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="25be7-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="25be7-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="25be7-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="25be7-110">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25be7-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25be7-111">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25be7-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25be7-112">要從中建立材質之記憶體中的檔案指標。</span><span class="sxs-lookup"><span data-stu-id="25be7-112">Pointer to the file in memory from which to create the texture.</span></span>

</dd> <dt>

<span data-ttu-id="25be7-113">*SrcDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25be7-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25be7-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25be7-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25be7-115">記憶體中檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="25be7-115">Size in bytes of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="25be7-116">*ppTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="25be7-116">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25be7-117">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="25be7-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="25be7-118">[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面指標的位址，表示所建立的材質物件。</span><span class="sxs-lookup"><span data-stu-id="25be7-118">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25be7-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="25be7-119">Return value</span></span>

<span data-ttu-id="25be7-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="25be7-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="25be7-121">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="25be7-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="25be7-122">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="25be7-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="25be7-123">備註</span><span class="sxs-lookup"><span data-stu-id="25be7-123">Remarks</span></span>

<span data-ttu-id="25be7-124">函數相當於 D3DXCreateTextureFromFileInMemoryEx (pDevice、pSrcData、SrcDataSize、D3DX \_ default、D3DX \_ DEFAULT、D3DX \_ default、0、D3DFMT \_ UNKNOWN、D3DPOOL \_ MANAGED、D3DX \_ default、D3DX \_ default、0、 **null**、 **null**、ppTexture) 。</span><span class="sxs-lookup"><span data-stu-id="25be7-124">The function is equivalent to D3DXCreateTextureFromFileInMemoryEx(pDevice, pSrcData, SrcDataSize, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="25be7-125">此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。</span><span class="sxs-lookup"><span data-stu-id="25be7-125">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="25be7-126">請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。</span><span class="sxs-lookup"><span data-stu-id="25be7-126">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="25be7-127">請注意，從 IDirect3DDevice9 物件呼叫時，使用這個函式所建立的資源將會放置在 D3DPOOL MANAGED 所表示的記憶體類別中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="25be7-127">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="25be7-128">從 IDirect3DDevice9Ex 物件呼叫這個方法時，資源會放在 D3DPOOL 預設值所表示的 memory 類別中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="25be7-128">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="25be7-129">篩選會自動套用至使用這個方法所建立的材質。</span><span class="sxs-lookup"><span data-stu-id="25be7-129">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="25be7-130">篩選相當於 \_ \_ \| \_ \_ 在 [D3DX \_ 篩選](d3dx-filter.md)中 D3DX 篩選三角形 D3DX 篩選遞色。</span><span class="sxs-lookup"><span data-stu-id="25be7-130">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25be7-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="25be7-131">Requirements</span></span>



| <span data-ttu-id="25be7-132">需求</span><span class="sxs-lookup"><span data-stu-id="25be7-132">Requirement</span></span> | <span data-ttu-id="25be7-133">值</span><span class="sxs-lookup"><span data-stu-id="25be7-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25be7-134">標頭</span><span class="sxs-lookup"><span data-stu-id="25be7-134">Header</span></span><br/>  | <dl> <span data-ttu-id="25be7-135"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="25be7-135"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="25be7-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="25be7-136">Library</span></span><br/> | <dl> <span data-ttu-id="25be7-137"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="25be7-137"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="25be7-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25be7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25be7-139">**D3DXCreateTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="25be7-139">**D3DXCreateTextureFromFileInMemoryEx**</span></span>](d3dxcreatetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="25be7-140">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="25be7-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
