---
description: 將磁片區儲存到緩衝區。 方法會建立 ID3DXBuffer 緩衝區來儲存資料，並傳回該物件。
ms.assetid: 4887ff1f-7904-4764-b284-b2c8e037f806
title: 'D3DXSaveVolumeToFileInMemory 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7daaa41e0cc87ea03a0aedc5fc2f7ca96653329f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196241"
---
# <a name="d3dxsavevolumetofileinmemory-function"></a><span data-ttu-id="097d5-104">D3DXSaveVolumeToFileInMemory 函式</span><span class="sxs-lookup"><span data-stu-id="097d5-104">D3DXSaveVolumeToFileInMemory function</span></span>

<span data-ttu-id="097d5-105">將磁片區儲存到緩衝區。</span><span class="sxs-lookup"><span data-stu-id="097d5-105">Saves a volume to a buffer.</span></span> <span data-ttu-id="097d5-106">方法會建立 [**ID3DXBuffer**](id3dxbuffer.md) 緩衝區來儲存資料，並傳回該物件。</span><span class="sxs-lookup"><span data-stu-id="097d5-106">The method creates an [**ID3DXBuffer**](id3dxbuffer.md) buffer to store the data, and returns that object.</span></span>

## <a name="syntax"></a><span data-ttu-id="097d5-107">語法</span><span class="sxs-lookup"><span data-stu-id="097d5-107">Syntax</span></span>


```C++
HRESULT D3DXSaveVolumeToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DVOLUME9    pSrcVolume,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a><span data-ttu-id="097d5-108">參數</span><span class="sxs-lookup"><span data-stu-id="097d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="097d5-109">*ppDestBuf* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="097d5-109">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="097d5-110">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="097d5-110">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="097d5-111">將儲存映射之 [**ID3DXBuffer**](id3dxbuffer.md) 緩衝區指標的位址。</span><span class="sxs-lookup"><span data-stu-id="097d5-111">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) buffer that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="097d5-112">*DestFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="097d5-112">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="097d5-113">類型： **[ **D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="097d5-113">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="097d5-114">[**D3DXIMAGE \_>FILEFORMAT**](./d3dximage-fileformat.md) 指定儲存時要使用的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="097d5-114">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="097d5-115">此函數支援儲存至所有 **D3DXIMAGE \_ >fileformat** 格式，但便攜 Pixmap ( Ppm) 和 Targa/Truevision 圖形介面卡 (. tga) 。</span><span class="sxs-lookup"><span data-stu-id="097d5-115">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="097d5-116">*pSrcVolume* \[在\]</span><span class="sxs-lookup"><span data-stu-id="097d5-116">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="097d5-117">類型： **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="097d5-117">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="097d5-118">[**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)介面的指標，其中包含要儲存的影像。</span><span class="sxs-lookup"><span data-stu-id="097d5-118">Pointer to [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="097d5-119">*pSrcPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="097d5-119">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="097d5-120">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="097d5-120">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="097d5-121">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，其中包含256色彩的調色板。</span><span class="sxs-lookup"><span data-stu-id="097d5-121">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="097d5-122">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="097d5-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="097d5-123">*pSrcBox* \[在\]</span><span class="sxs-lookup"><span data-stu-id="097d5-123">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="097d5-124">Type： **Const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="097d5-124">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="097d5-125">[**D3DBOX**](d3dbox.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="097d5-125">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="097d5-126">指定 [來源] 方塊。</span><span class="sxs-lookup"><span data-stu-id="097d5-126">Specifies the source box.</span></span> <span data-ttu-id="097d5-127">將此參數設定為 **Null** ，以指定整個磁片區。</span><span class="sxs-lookup"><span data-stu-id="097d5-127">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="097d5-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="097d5-128">Return value</span></span>

<span data-ttu-id="097d5-129">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="097d5-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="097d5-130">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="097d5-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="097d5-131">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="097d5-131">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="097d5-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="097d5-132">Requirements</span></span>



| <span data-ttu-id="097d5-133">需求</span><span class="sxs-lookup"><span data-stu-id="097d5-133">Requirement</span></span> | <span data-ttu-id="097d5-134">值</span><span class="sxs-lookup"><span data-stu-id="097d5-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="097d5-135">標頭</span><span class="sxs-lookup"><span data-stu-id="097d5-135">Header</span></span><br/>  | <dl> <span data-ttu-id="097d5-136"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="097d5-136"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="097d5-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="097d5-137">Library</span></span><br/> | <dl> <span data-ttu-id="097d5-138"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="097d5-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="097d5-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="097d5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="097d5-140">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="097d5-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="097d5-141">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="097d5-141">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
