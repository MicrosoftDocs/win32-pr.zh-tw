---
description: 將材質儲存至檔案。
ms.assetid: c1718903-039a-4132-b128-82e03078ef62
title: 'D3DX10SaveTextureToFile 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c760876160d8ce1cbc0423639a59218c79716481
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985728"
---
# <a name="d3dx10savetexturetofile-function"></a><span data-ttu-id="00426-103">D3DX10SaveTextureToFile 函式</span><span class="sxs-lookup"><span data-stu-id="00426-103">D3DX10SaveTextureToFile function</span></span>

<span data-ttu-id="00426-104">將材質儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="00426-104">Save a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="00426-105">語法</span><span class="sxs-lookup"><span data-stu-id="00426-105">Syntax</span></span>


```C++
HRESULT D3DX10SaveTextureToFile(
  _In_ ID3D10Resource           *pSrcTexture,
  _In_ D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a><span data-ttu-id="00426-106">參數</span><span class="sxs-lookup"><span data-stu-id="00426-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00426-107">*pSrcTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00426-107">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00426-108">類型： **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="00426-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="00426-109">要儲存的材質指標。</span><span class="sxs-lookup"><span data-stu-id="00426-109">Pointer to the texture to be saved.</span></span> <span data-ttu-id="00426-110">請參閱 [**ID3D10Resource 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)。</span><span class="sxs-lookup"><span data-stu-id="00426-110">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="00426-111">*DestFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00426-111">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00426-112">類型： **[ **D3DX10 \_ 圖像 \_ 檔案 \_ 格式**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="00426-112">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

<span data-ttu-id="00426-113">材質儲存格式的格式 (參閱 [**D3DX10 \_ 圖像 \_ 檔案 \_ 格式**](d3dx10-image-file-format.md)) 。</span><span class="sxs-lookup"><span data-stu-id="00426-113">The format the texture will be saved as (see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)).</span></span> <span data-ttu-id="00426-114">D3DX10 \_ 如果 \_ DDS 是慣用的格式，因為它是唯一支援 [**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)格式的選項。</span><span class="sxs-lookup"><span data-stu-id="00426-114">D3DX10\_IFF\_DDS is the preferred format since it is the only option that supports all the formats in [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="00426-115">*pDestFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00426-115">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00426-116">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00426-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00426-117">將儲存材質的目的地輸出檔名稱。</span><span class="sxs-lookup"><span data-stu-id="00426-117">Name of the destination output file where the texture will be saved.</span></span> <span data-ttu-id="00426-118">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="00426-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="00426-119">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="00426-119">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00426-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="00426-120">Return value</span></span>

<span data-ttu-id="00426-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="00426-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="00426-122">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值;使用傳回值來查看是否支援 *DestFormat* 。</span><span class="sxs-lookup"><span data-stu-id="00426-122">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md); use the return value to see if the *DestFormat* is supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="00426-123">備註</span><span class="sxs-lookup"><span data-stu-id="00426-123">Remarks</span></span>

<span data-ttu-id="00426-124">**D3DX10SaveTextureToFile** 只會在必要時為輸入材質寫出額外的 [**DDS \_ 標頭 \_ DXT10**](../direct3ddds/dds-header-dxt10.md) 結構 (例如，因為輸入材質是在標準 RGB (sRGB) 格式) 。</span><span class="sxs-lookup"><span data-stu-id="00426-124">**D3DX10SaveTextureToFile** writes out the extra [**DDS\_HEADER\_DXT10**](../direct3ddds/dds-header-dxt10.md) structure for the input texture only if necessary (for example, because the input texture is in standard RGB (sRGB) format).</span></span> <span data-ttu-id="00426-125">如果 **D3DX10SaveTextureToFile** 寫出 **dds \_ 標頭 \_ DXT10** 結構，則會將材質 [**\_ PIXELFORMAT**](../direct3ddds/dds-pixelformat.md)結構的 **DwFourCC** 成員設定為 [ **DX10** ]，以指出 **DDS \_ 標頭 \_ prescense** 延伸標頭的 DXT10。</span><span class="sxs-lookup"><span data-stu-id="00426-125">If **D3DX10SaveTextureToFile** writes out the **DDS\_HEADER\_DXT10** structure, it sets the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](../direct3ddds/dds-pixelformat.md) structure for the texture to **DX10** to indicate the prescense of the **DDS\_HEADER\_DXT10** extended header.</span></span>

## <a name="requirements"></a><span data-ttu-id="00426-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="00426-126">Requirements</span></span>



| <span data-ttu-id="00426-127">需求</span><span class="sxs-lookup"><span data-stu-id="00426-127">Requirement</span></span> | <span data-ttu-id="00426-128">值</span><span class="sxs-lookup"><span data-stu-id="00426-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00426-129">標頭</span><span class="sxs-lookup"><span data-stu-id="00426-129">Header</span></span><br/>  | <dl> <span data-ttu-id="00426-130"><dt>D3DX10Tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="00426-130"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="00426-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="00426-131">Library</span></span><br/> | <dl> <span data-ttu-id="00426-132"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="00426-132"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="00426-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00426-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00426-134">D3DX 10 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="00426-134">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="00426-135">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="00426-135">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
