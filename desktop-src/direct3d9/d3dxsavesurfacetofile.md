---
description: 將介面儲存至檔案。
ms.assetid: 28bbf728-afde-4d25-8562-9d6a957aab2d
title: 'D3DXSaveSurfaceToFile 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd19e0a8f7b9557b6bcbe6c71afcdca7c9037b70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989194"
---
# <a name="d3dxsavesurfacetofile-function"></a><span data-ttu-id="b1a23-103">D3DXSaveSurfaceToFile 函式</span><span class="sxs-lookup"><span data-stu-id="b1a23-103">D3DXSaveSurfaceToFile function</span></span>

<span data-ttu-id="b1a23-104">將介面儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="b1a23-104">Saves a surface to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1a23-105">語法</span><span class="sxs-lookup"><span data-stu-id="b1a23-105">Syntax</span></span>


```C++
HRESULT D3DXSaveSurfaceToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DSURFACE9   pSrcSurface,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const RECT                 *pSrcRect
);
```



## <a name="parameters"></a><span data-ttu-id="b1a23-106">參數</span><span class="sxs-lookup"><span data-stu-id="b1a23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1a23-107">*pDestFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b1a23-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a23-108">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1a23-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1a23-109">字串的指標，指定目的地影像的檔案名。</span><span class="sxs-lookup"><span data-stu-id="b1a23-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="b1a23-110">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="b1a23-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="b1a23-111">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="b1a23-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="b1a23-112">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="b1a23-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b1a23-113">*DestFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b1a23-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a23-114">類型： **[ **D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="b1a23-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="b1a23-115">[**D3DXIMAGE \_>FILEFORMAT**](./d3dximage-fileformat.md) 指定儲存時要使用的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="b1a23-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="b1a23-116">此函數支援儲存至所有 **D3DXIMAGE \_ >fileformat** 格式，但便攜 Pixmap ( Ppm) 和 Targa/Truevision 圖形介面卡 (. tga) 。</span><span class="sxs-lookup"><span data-stu-id="b1a23-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="b1a23-117">*pSrcSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b1a23-117">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a23-118">類型： **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="b1a23-118">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="b1a23-119">[**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)介面的指標，其中包含要儲存的影像。</span><span class="sxs-lookup"><span data-stu-id="b1a23-119">Pointer to [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="b1a23-120">*pSrcPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b1a23-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a23-121">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="b1a23-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="b1a23-122">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，其中包含256色彩的調色板。</span><span class="sxs-lookup"><span data-stu-id="b1a23-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="b1a23-123">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b1a23-123">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b1a23-124">*pSrcRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b1a23-124">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a23-125">Type： **Const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="b1a23-125">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="b1a23-126">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b1a23-126">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="b1a23-127">指定來源矩形。</span><span class="sxs-lookup"><span data-stu-id="b1a23-127">Specifies the source rectangle.</span></span> <span data-ttu-id="b1a23-128">將此參數設定為 **Null** ，以指定整個映射。</span><span class="sxs-lookup"><span data-stu-id="b1a23-128">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1a23-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1a23-129">Return value</span></span>

<span data-ttu-id="b1a23-130">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1a23-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1a23-131">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="b1a23-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b1a23-132">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="b1a23-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="b1a23-133">備註</span><span class="sxs-lookup"><span data-stu-id="b1a23-133">Remarks</span></span>

<span data-ttu-id="b1a23-134">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="b1a23-134">The compiler setting also determines the function version.</span></span> <span data-ttu-id="b1a23-135">如果已定義 Unicode，函式呼叫會解析為 D3DXSaveSurfaceToFileW。</span><span class="sxs-lookup"><span data-stu-id="b1a23-135">If Unicode is defined, the function call resolves to D3DXSaveSurfaceToFileW.</span></span> <span data-ttu-id="b1a23-136">否則，函式呼叫會解析為 D3DXSaveSurfaceToFileA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="b1a23-136">Otherwise, the function call resolves to D3DXSaveSurfaceToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="b1a23-137">此函式會處理壓縮材質格式的轉換。</span><span class="sxs-lookup"><span data-stu-id="b1a23-137">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1a23-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1a23-138">Requirements</span></span>



| <span data-ttu-id="b1a23-139">需求</span><span class="sxs-lookup"><span data-stu-id="b1a23-139">Requirement</span></span> | <span data-ttu-id="b1a23-140">值</span><span class="sxs-lookup"><span data-stu-id="b1a23-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a23-141">標頭</span><span class="sxs-lookup"><span data-stu-id="b1a23-141">Header</span></span><br/>  | <dl> <span data-ttu-id="b1a23-142"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1a23-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b1a23-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="b1a23-143">Library</span></span><br/> | <dl> <span data-ttu-id="b1a23-144"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1a23-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b1a23-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1a23-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1a23-146">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="b1a23-146">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="b1a23-147">**D3DXSaveTextureToFile**</span><span class="sxs-lookup"><span data-stu-id="b1a23-147">**D3DXSaveTextureToFile**</span></span>](d3dxsavetexturetofile.md)
</dt> <dt>

[<span data-ttu-id="b1a23-148">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="b1a23-148">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
