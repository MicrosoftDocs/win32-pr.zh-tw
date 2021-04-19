---
description: 將介面儲存至影像檔。
ms.assetid: 6320e5ed-e43d-43bf-a746-5478df42941d
title: 'D3DXSaveSurfaceToFileInMemory 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8e8bbdd447b7154e150b3469a4b12180252ed516
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975671"
---
# <a name="d3dxsavesurfacetofileinmemory-function"></a><span data-ttu-id="19d8e-103">D3DXSaveSurfaceToFileInMemory 函式</span><span class="sxs-lookup"><span data-stu-id="19d8e-103">D3DXSaveSurfaceToFileInMemory function</span></span>

<span data-ttu-id="19d8e-104">將介面儲存至影像檔。</span><span class="sxs-lookup"><span data-stu-id="19d8e-104">Saves a surface to an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="19d8e-105">語法</span><span class="sxs-lookup"><span data-stu-id="19d8e-105">Syntax</span></span>


```C++
HRESULT D3DXSaveSurfaceToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DSURFACE9   pSrcSurface,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const RECT                 *pSrcRect
);
```



## <a name="parameters"></a><span data-ttu-id="19d8e-106">參數</span><span class="sxs-lookup"><span data-stu-id="19d8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19d8e-107">*ppDestBuf* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="19d8e-107">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19d8e-108">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="19d8e-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="19d8e-109">將儲存影像之 [**ID3DXBuffer**](id3dxbuffer.md) 的指標位址。</span><span class="sxs-lookup"><span data-stu-id="19d8e-109">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="19d8e-110">*DestFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19d8e-110">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19d8e-111">類型： **[ **D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="19d8e-111">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="19d8e-112">[**D3DXIMAGE \_>FILEFORMAT**](./d3dximage-fileformat.md) 指定儲存時要使用的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="19d8e-112">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="19d8e-113">此函數支援儲存至所有 **D3DXIMAGE \_ >fileformat** 格式，但便攜 Pixmap ( Ppm) 和 Targa/Truevision 圖形介面卡 (. tga) 。</span><span class="sxs-lookup"><span data-stu-id="19d8e-113">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="19d8e-114">*pSrcSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19d8e-114">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19d8e-115">類型： **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="19d8e-115">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="19d8e-116">[**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)介面的指標，其中包含要儲存的影像。</span><span class="sxs-lookup"><span data-stu-id="19d8e-116">Pointer to [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="19d8e-117">*pSrcPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19d8e-117">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19d8e-118">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="19d8e-118">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="19d8e-119">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，其中包含256色彩的調色板。</span><span class="sxs-lookup"><span data-stu-id="19d8e-119">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="19d8e-120">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="19d8e-120">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19d8e-121">*pSrcRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19d8e-121">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19d8e-122">Type： **Const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="19d8e-122">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="19d8e-123">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標。</span><span class="sxs-lookup"><span data-stu-id="19d8e-123">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="19d8e-124">指定來源矩形。</span><span class="sxs-lookup"><span data-stu-id="19d8e-124">Specifies the source rectangle.</span></span> <span data-ttu-id="19d8e-125">將此參數設定為 **Null** ，以指定整個映射。</span><span class="sxs-lookup"><span data-stu-id="19d8e-125">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19d8e-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="19d8e-126">Return value</span></span>

<span data-ttu-id="19d8e-127">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19d8e-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19d8e-128">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="19d8e-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="19d8e-129">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="19d8e-129">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="19d8e-130">備註</span><span class="sxs-lookup"><span data-stu-id="19d8e-130">Remarks</span></span>

<span data-ttu-id="19d8e-131">此函式會處理壓縮材質格式的轉換。</span><span class="sxs-lookup"><span data-stu-id="19d8e-131">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="19d8e-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="19d8e-132">Requirements</span></span>



| <span data-ttu-id="19d8e-133">需求</span><span class="sxs-lookup"><span data-stu-id="19d8e-133">Requirement</span></span> | <span data-ttu-id="19d8e-134">值</span><span class="sxs-lookup"><span data-stu-id="19d8e-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19d8e-135">標頭</span><span class="sxs-lookup"><span data-stu-id="19d8e-135">Header</span></span><br/>  | <dl> <span data-ttu-id="19d8e-136"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="19d8e-136"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="19d8e-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="19d8e-137">Library</span></span><br/> | <dl> <span data-ttu-id="19d8e-138"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="19d8e-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="19d8e-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19d8e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19d8e-140">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="19d8e-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="19d8e-141">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="19d8e-141">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
