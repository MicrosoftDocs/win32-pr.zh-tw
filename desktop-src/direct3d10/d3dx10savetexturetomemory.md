---
description: 將材質儲存至記憶體。
ms.assetid: be541b99-6d07-480e-8f28-b7fc44566e7d
title: 'D3DX10SaveTextureToMemory 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f20278f9fc590e72f93051d5fdd4cfbd918098df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107001789"
---
# <a name="d3dx10savetexturetomemory-function"></a><span data-ttu-id="b5ada-103">D3DX10SaveTextureToMemory 函式</span><span class="sxs-lookup"><span data-stu-id="b5ada-103">D3DX10SaveTextureToMemory function</span></span>

<span data-ttu-id="b5ada-104">將材質儲存至記憶體。</span><span class="sxs-lookup"><span data-stu-id="b5ada-104">Save a texture to memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ada-105">語法</span><span class="sxs-lookup"><span data-stu-id="b5ada-105">Syntax</span></span>


```C++
HRESULT D3DX10SaveTextureToMemory(
  _In_  ID3D10Resource           *pSrcTexture,
  _In_  D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="b5ada-106">參數</span><span class="sxs-lookup"><span data-stu-id="b5ada-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5ada-107">*pSrcTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b5ada-107">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ada-108">類型： **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="b5ada-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="b5ada-109">要儲存的材質指標。</span><span class="sxs-lookup"><span data-stu-id="b5ada-109">Pointer to the texture to be saved.</span></span> <span data-ttu-id="b5ada-110">請參閱 [**ID3D10Resource 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)。</span><span class="sxs-lookup"><span data-stu-id="b5ada-110">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="b5ada-111">*DestFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b5ada-111">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ada-112">類型： **[ **D3DX10 \_ 圖像 \_ 檔案 \_ 格式**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="b5ada-112">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

<span data-ttu-id="b5ada-113">材質將儲存成的格式。</span><span class="sxs-lookup"><span data-stu-id="b5ada-113">The format the texture will be saved as.</span></span> <span data-ttu-id="b5ada-114">請參閱 [**D3DX10 \_ 影像檔案 \_ \_ 格式**](d3dx10-image-file-format.md)。</span><span class="sxs-lookup"><span data-stu-id="b5ada-114">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5ada-115">*ppDestBuf* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b5ada-115">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ada-116">類型： **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="b5ada-116">Type: **[**LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="b5ada-117">包含已儲存材質之記憶體的指標位址。</span><span class="sxs-lookup"><span data-stu-id="b5ada-117">Address of a pointer to the memory containing the saved texture.</span></span> <span data-ttu-id="b5ada-118">請參閱 [**ID3D10Blob 介面**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)。</span><span class="sxs-lookup"><span data-stu-id="b5ada-118">See [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob).</span></span>

</dd> <dt>

<span data-ttu-id="b5ada-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b5ada-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ada-120">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b5ada-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b5ada-121">選擇性。</span><span class="sxs-lookup"><span data-stu-id="b5ada-121">Optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5ada-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="b5ada-122">Return value</span></span>

<span data-ttu-id="b5ada-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5ada-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5ada-124">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b5ada-124">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ada-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5ada-125">Requirements</span></span>



| <span data-ttu-id="b5ada-126">需求</span><span class="sxs-lookup"><span data-stu-id="b5ada-126">Requirement</span></span> | <span data-ttu-id="b5ada-127">值</span><span class="sxs-lookup"><span data-stu-id="b5ada-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ada-128">標頭</span><span class="sxs-lookup"><span data-stu-id="b5ada-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b5ada-129"><dt>D3DX10Tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="b5ada-129"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b5ada-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="b5ada-130">Library</span></span><br/> | <dl> <span data-ttu-id="b5ada-131"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5ada-131"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b5ada-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5ada-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5ada-133">D3DX 10 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="b5ada-133">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="b5ada-134">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="b5ada-134">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
