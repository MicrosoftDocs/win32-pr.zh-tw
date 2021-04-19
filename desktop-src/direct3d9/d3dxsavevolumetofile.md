---
description: 將磁片區儲存到磁片上的檔案。
ms.assetid: 4d33fba5-e003-4385-b683-aff6723af2a5
title: 'D3DXSaveVolumeToFile 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 36550cda8d9ef664f96e236d2770a82c88412772
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986089"
---
# <a name="d3dxsavevolumetofile-function"></a><span data-ttu-id="01a48-103">D3DXSaveVolumeToFile 函式</span><span class="sxs-lookup"><span data-stu-id="01a48-103">D3DXSaveVolumeToFile function</span></span>

<span data-ttu-id="01a48-104">將磁片區儲存到磁片上的檔案。</span><span class="sxs-lookup"><span data-stu-id="01a48-104">Saves a volume to a file on disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="01a48-105">語法</span><span class="sxs-lookup"><span data-stu-id="01a48-105">Syntax</span></span>


```C++
HRESULT D3DXSaveVolumeToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DVOLUME9    pSrcVolume,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a><span data-ttu-id="01a48-106">參數</span><span class="sxs-lookup"><span data-stu-id="01a48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01a48-107">*pDestFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="01a48-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01a48-108">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="01a48-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="01a48-109">字串的指標，指定目的地影像的檔案名。</span><span class="sxs-lookup"><span data-stu-id="01a48-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="01a48-110">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="01a48-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="01a48-111">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="01a48-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="01a48-112">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="01a48-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="01a48-113">*DestFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="01a48-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01a48-114">類型： **[ **D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="01a48-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="01a48-115">[**D3DXIMAGE \_>FILEFORMAT**](./d3dximage-fileformat.md) 指定儲存時要使用的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="01a48-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="01a48-116">此函數支援儲存至所有 **D3DXIMAGE \_ >fileformat** 格式，但便攜 Pixmap ( Ppm) 和 Targa/Truevision 圖形介面卡 (. tga) 。</span><span class="sxs-lookup"><span data-stu-id="01a48-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="01a48-117">*pSrcVolume* \[在\]</span><span class="sxs-lookup"><span data-stu-id="01a48-117">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01a48-118">類型： **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="01a48-118">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="01a48-119">[**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)介面的指標，其中包含要儲存的影像。</span><span class="sxs-lookup"><span data-stu-id="01a48-119">Pointer to [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="01a48-120">*pSrcPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="01a48-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01a48-121">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="01a48-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="01a48-122">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，其中包含256色彩的調色板。</span><span class="sxs-lookup"><span data-stu-id="01a48-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="01a48-123">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="01a48-123">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="01a48-124">*pSrcBox* \[在\]</span><span class="sxs-lookup"><span data-stu-id="01a48-124">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01a48-125">Type： **Const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="01a48-125">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="01a48-126">[**D3DBOX**](d3dbox.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="01a48-126">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="01a48-127">指定 [來源] 方塊。</span><span class="sxs-lookup"><span data-stu-id="01a48-127">Specifies the source box.</span></span> <span data-ttu-id="01a48-128">將此參數設定為 **Null** ，以指定整個磁片區。</span><span class="sxs-lookup"><span data-stu-id="01a48-128">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01a48-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="01a48-129">Return value</span></span>

<span data-ttu-id="01a48-130">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="01a48-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="01a48-131">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="01a48-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="01a48-132">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="01a48-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="01a48-133">備註</span><span class="sxs-lookup"><span data-stu-id="01a48-133">Remarks</span></span>

<span data-ttu-id="01a48-134">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="01a48-134">The compiler setting also determines the function version.</span></span> <span data-ttu-id="01a48-135">如果已定義 Unicode，函式呼叫會解析為 D3DXSaveVolumeToFileW。</span><span class="sxs-lookup"><span data-stu-id="01a48-135">If Unicode is defined, the function call resolves to D3DXSaveVolumeToFileW.</span></span> <span data-ttu-id="01a48-136">否則，函式呼叫會解析為 >D3DXSaveVolumeToFileA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="01a48-136">Otherwise, the function call resolves to >D3DXSaveVolumeToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="01a48-137">此函式會處理壓縮材質格式的轉換。</span><span class="sxs-lookup"><span data-stu-id="01a48-137">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="01a48-138">如果磁片區是 nondynamic (因為在建立) 將 usage 參數設定為0，並位於視訊記憶體 (記憶體集區設定為 D3DPOOL \_ 預設) 時， [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) 將會失敗，因為 D3DX 無法鎖定位於視訊記憶體中的 nondynamic 磁片區。</span><span class="sxs-lookup"><span data-stu-id="01a48-138">If the volume is nondynamic (because of a usage parameter set to 0 at the creation) and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) will fail because D3DX cannot lock nondynamic volumes located in video memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="01a48-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="01a48-139">Requirements</span></span>



| <span data-ttu-id="01a48-140">需求</span><span class="sxs-lookup"><span data-stu-id="01a48-140">Requirement</span></span> | <span data-ttu-id="01a48-141">值</span><span class="sxs-lookup"><span data-stu-id="01a48-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01a48-142">標頭</span><span class="sxs-lookup"><span data-stu-id="01a48-142">Header</span></span><br/>  | <dl> <span data-ttu-id="01a48-143"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="01a48-143"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="01a48-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="01a48-144">Library</span></span><br/> | <dl> <span data-ttu-id="01a48-145"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="01a48-145"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="01a48-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01a48-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a48-147">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="01a48-147">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="01a48-148">**D3DXSaveSurfaceToFile**</span><span class="sxs-lookup"><span data-stu-id="01a48-148">**D3DXSaveSurfaceToFile**</span></span>](d3dxsavesurfacetofile.md)
</dt> <dt>

[<span data-ttu-id="01a48-149">**D3DXSaveTextureToFile**</span><span class="sxs-lookup"><span data-stu-id="01a48-149">**D3DXSaveTextureToFile**</span></span>](d3dxsavetexturetofile.md)
</dt> <dt>

[<span data-ttu-id="01a48-150">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="01a48-150">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
