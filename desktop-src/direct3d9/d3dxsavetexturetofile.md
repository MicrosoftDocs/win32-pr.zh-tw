---
description: 將材質儲存至檔案。
ms.assetid: b14dd893-e967-4be9-81e8-aeb52035d91c
title: 'D3DXSaveTextureToFile 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c11cc8b512527fb0610c288fdbaeba6c976604a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000587"
---
# <a name="d3dxsavetexturetofile-function"></a><span data-ttu-id="3e40e-103">D3DXSaveTextureToFile 函式</span><span class="sxs-lookup"><span data-stu-id="3e40e-103">D3DXSaveTextureToFile function</span></span>

<span data-ttu-id="3e40e-104">將材質儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="3e40e-104">Saves a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e40e-105">語法</span><span class="sxs-lookup"><span data-stu-id="3e40e-105">Syntax</span></span>


```C++
HRESULT D3DXSaveTextureToFile(
  _In_       LPCTSTR                pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_       LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_ const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a><span data-ttu-id="3e40e-106">參數</span><span class="sxs-lookup"><span data-stu-id="3e40e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e40e-107">*pDestFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3e40e-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e40e-108">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e40e-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e40e-109">字串的指標，指定目的地影像的檔案名。</span><span class="sxs-lookup"><span data-stu-id="3e40e-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="3e40e-110">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="3e40e-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="3e40e-111">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="3e40e-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="3e40e-112">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="3e40e-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3e40e-113">*DestFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3e40e-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e40e-114">類型： **[ **D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="3e40e-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="3e40e-115">[**D3DXIMAGE \_>FILEFORMAT**](./d3dximage-fileformat.md) 指定儲存時要使用的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="3e40e-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="3e40e-116">此函數支援儲存至所有 **D3DXIMAGE \_ >fileformat** 格式，但便攜 Pixmap ( Ppm) 和 Targa/Truevision 圖形介面卡 (. tga) 。</span><span class="sxs-lookup"><span data-stu-id="3e40e-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="3e40e-117">*pSrcTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3e40e-117">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e40e-118">類型： **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="3e40e-118">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="3e40e-119">[**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)介面的指標，其中包含要儲存的材質。</span><span class="sxs-lookup"><span data-stu-id="3e40e-119">Pointer to [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface, containing the texture to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="3e40e-120">*pSrcPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3e40e-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e40e-121">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="3e40e-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="3e40e-122">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，其中包含256色彩的調色板。</span><span class="sxs-lookup"><span data-stu-id="3e40e-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="3e40e-123">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3e40e-123">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e40e-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="3e40e-124">Return value</span></span>

<span data-ttu-id="3e40e-125">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3e40e-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3e40e-126">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="3e40e-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3e40e-127">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="3e40e-127">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="3e40e-128">備註</span><span class="sxs-lookup"><span data-stu-id="3e40e-128">Remarks</span></span>

<span data-ttu-id="3e40e-129">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="3e40e-129">The compiler setting also determines the function version.</span></span> <span data-ttu-id="3e40e-130">如果已定義 Unicode，函式呼叫會解析為 D3DXSaveTextureToFileW。</span><span class="sxs-lookup"><span data-stu-id="3e40e-130">If Unicode is defined, the function call resolves to D3DXSaveTextureToFileW.</span></span> <span data-ttu-id="3e40e-131">否則，函式呼叫會解析為 D3DXSaveTextureToFileA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="3e40e-131">Otherwise, the function call resolves to D3DXSaveTextureToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="3e40e-132">此函式會處理壓縮材質格式的轉換。</span><span class="sxs-lookup"><span data-stu-id="3e40e-132">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="3e40e-133">如果磁片區是 nondynamic (因為在建立) 將 usage 參數設定為0，並位於視訊記憶體 (記憶體集區設定為 D3DPOOL \_ 預設) 時， **D3DXSaveTextureToFile** 將會失敗，因為 D3DX 無法鎖定位於視訊記憶體中的 nondynamic 磁片區。</span><span class="sxs-lookup"><span data-stu-id="3e40e-133">If the volume is nondynamic (because of a usage parameter set to 0 at the creation) and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), **D3DXSaveTextureToFile** will fail because D3DX cannot lock nondynamic volumes located in video memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e40e-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e40e-134">Requirements</span></span>



| <span data-ttu-id="3e40e-135">需求</span><span class="sxs-lookup"><span data-stu-id="3e40e-135">Requirement</span></span> | <span data-ttu-id="3e40e-136">值</span><span class="sxs-lookup"><span data-stu-id="3e40e-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e40e-137">標頭</span><span class="sxs-lookup"><span data-stu-id="3e40e-137">Header</span></span><br/>  | <dl> <span data-ttu-id="3e40e-138"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="3e40e-138"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="3e40e-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="3e40e-139">Library</span></span><br/> | <dl> <span data-ttu-id="3e40e-140"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e40e-140"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3e40e-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e40e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e40e-142">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="3e40e-142">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="3e40e-143">**D3DXSaveSurfaceToFile**</span><span class="sxs-lookup"><span data-stu-id="3e40e-143">**D3DXSaveSurfaceToFile**</span></span>](d3dxsavesurfacetofile.md)
</dt> <dt>

[<span data-ttu-id="3e40e-144">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="3e40e-144">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
