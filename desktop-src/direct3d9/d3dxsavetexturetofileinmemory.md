---
description: 將材質儲存至影像檔。
ms.assetid: 8dcfd58a-ae1e-43c3-8ff1-94e3fa398b0f
title: 'D3DXSaveTextureToFileInMemory 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c58da1663abc5295e8ce17c500bd46d6c365a2d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116213"
---
# <a name="d3dxsavetexturetofileinmemory-function"></a><span data-ttu-id="bb66a-103">D3DXSaveTextureToFileInMemory 函式</span><span class="sxs-lookup"><span data-stu-id="bb66a-103">D3DXSaveTextureToFileInMemory function</span></span>

<span data-ttu-id="bb66a-104">將材質儲存至影像檔。</span><span class="sxs-lookup"><span data-stu-id="bb66a-104">Saves a texture to an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb66a-105">語法</span><span class="sxs-lookup"><span data-stu-id="bb66a-105">Syntax</span></span>


```C++
HRESULT D3DXSaveTextureToFileInMemory(
  _Out_       LPD3DXBUFFER           *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_        LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a><span data-ttu-id="bb66a-106">參數</span><span class="sxs-lookup"><span data-stu-id="bb66a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb66a-107">*ppDestBuf* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bb66a-107">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb66a-108">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="bb66a-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="bb66a-109">將儲存影像之 [**ID3DXBuffer**](id3dxbuffer.md) 的指標位址。</span><span class="sxs-lookup"><span data-stu-id="bb66a-109">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="bb66a-110">*DestFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb66a-110">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb66a-111">類型： **[ **D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="bb66a-111">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="bb66a-112">[**D3DXIMAGE \_>FILEFORMAT**](./d3dximage-fileformat.md) 指定儲存時要使用的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="bb66a-112">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="bb66a-113">此函數支援儲存至所有 **D3DXIMAGE \_ >fileformat** 格式，但便攜 Pixmap ( Ppm) 和 Targa/Truevision 圖形介面卡 (. tga) 。</span><span class="sxs-lookup"><span data-stu-id="bb66a-113">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="bb66a-114">*pSrcTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb66a-114">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb66a-115">類型： **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="bb66a-115">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="bb66a-116">[**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)介面的指標，其中包含要儲存的影像。</span><span class="sxs-lookup"><span data-stu-id="bb66a-116">Pointer to [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="bb66a-117">*pSrcPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb66a-117">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb66a-118">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="bb66a-118">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="bb66a-119">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，其中包含256色彩的調色板。</span><span class="sxs-lookup"><span data-stu-id="bb66a-119">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="bb66a-120">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bb66a-120">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb66a-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb66a-121">Return value</span></span>

<span data-ttu-id="bb66a-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb66a-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb66a-123">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="bb66a-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bb66a-124">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="bb66a-124">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb66a-125">備註</span><span class="sxs-lookup"><span data-stu-id="bb66a-125">Remarks</span></span>

<span data-ttu-id="bb66a-126">此函式會處理壓縮材質格式的轉換。</span><span class="sxs-lookup"><span data-stu-id="bb66a-126">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb66a-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb66a-127">Requirements</span></span>



| <span data-ttu-id="bb66a-128">需求</span><span class="sxs-lookup"><span data-stu-id="bb66a-128">Requirement</span></span> | <span data-ttu-id="bb66a-129">值</span><span class="sxs-lookup"><span data-stu-id="bb66a-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb66a-130">標頭</span><span class="sxs-lookup"><span data-stu-id="bb66a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="bb66a-131"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb66a-131"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="bb66a-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="bb66a-132">Library</span></span><br/> | <dl> <span data-ttu-id="bb66a-133"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb66a-133"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="bb66a-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb66a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb66a-135">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="bb66a-135">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="bb66a-136">**D3DXSaveSurfaceToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="bb66a-136">**D3DXSaveSurfaceToFileInMemory**</span></span>](d3dxsavesurfacetofileinmemory.md)
</dt> <dt>

[<span data-ttu-id="bb66a-137">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="bb66a-137">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
