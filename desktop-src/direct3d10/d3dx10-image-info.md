---
description: D3DX10_IMAGE_INFO 結構-傳回影像檔案原始內容的描述。
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: 'D3DX10_IMAGE_INFO 結構 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 228ddf777217e9e61369b0a7fc3b3eb1ca012b1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105476"
---
# <a name="d3dx10_image_info-structure"></a><span data-ttu-id="31db4-103">D3DX10 \_ 影像 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="31db4-103">D3DX10\_IMAGE\_INFO structure</span></span>

<span data-ttu-id="31db4-104">傳回影像檔案原始內容的描述。</span><span class="sxs-lookup"><span data-stu-id="31db4-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="31db4-105">語法</span><span class="sxs-lookup"><span data-stu-id="31db4-105">Syntax</span></span>


```C++
typedef struct D3DX10_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D10_RESOURCE_DIMENSION ResourceDimension;
  D3DX10_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX10_IMAGE_INFO, *LPD3DX10_IMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="31db4-106">成員</span><span class="sxs-lookup"><span data-stu-id="31db4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="31db4-107">**寬度**</span><span class="sxs-lookup"><span data-stu-id="31db4-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="31db4-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31db4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="31db4-109">原始影像的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="31db4-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="31db4-110">**高度**</span><span class="sxs-lookup"><span data-stu-id="31db4-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="31db4-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31db4-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="31db4-112">原始影像的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="31db4-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="31db4-113">**深度**</span><span class="sxs-lookup"><span data-stu-id="31db4-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="31db4-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31db4-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="31db4-115">原始影像的深度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="31db4-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="31db4-116">[陣列大小]</span><span class="sxs-lookup"><span data-stu-id="31db4-116">**ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="31db4-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31db4-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="31db4-118">材質陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="31db4-118">Size of the texture array.</span></span> <span data-ttu-id="31db4-119">單一映射的 *ArraySize* 會是1。</span><span class="sxs-lookup"><span data-stu-id="31db4-119">*ArraySize* will be 1 for a single image.</span></span>

</dd> <dt>

<span data-ttu-id="31db4-120">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="31db4-120">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="31db4-121">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31db4-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="31db4-122">原始影像中的 mipmap 層級數目。</span><span class="sxs-lookup"><span data-stu-id="31db4-122">Number of mipmap levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="31db4-123">**MiscFlags**</span><span class="sxs-lookup"><span data-stu-id="31db4-123">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="31db4-124">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31db4-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="31db4-125">其他資源屬性 (參閱 [**D3D10 \_ 資源 \_ 其他 \_ 旗**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag) 標) 。</span><span class="sxs-lookup"><span data-stu-id="31db4-125">Miscellaneous resource properties (see [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="31db4-126">**格式**</span><span class="sxs-lookup"><span data-stu-id="31db4-126">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="31db4-127">類型： **[ **DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="31db4-127">Type: **[**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="31db4-128">從 [**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 列舉類型到最接近原始影像中資料的值。</span><span class="sxs-lookup"><span data-stu-id="31db4-128">A value from the [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="31db4-129">**ResourceDimension**</span><span class="sxs-lookup"><span data-stu-id="31db4-129">**ResourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="31db4-130">類型： **[ **D3D10 \_ 資源 \_ 維度**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="31db4-130">Type: **[**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="31db4-131">表示儲存在檔案中的材質類型。</span><span class="sxs-lookup"><span data-stu-id="31db4-131">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="31db4-132">請參閱 [**D3D10 \_ 資源 \_ 維度**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)。</span><span class="sxs-lookup"><span data-stu-id="31db4-132">See [**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).</span></span>

</dd> <dt>

<span data-ttu-id="31db4-133">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="31db4-133">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="31db4-134">類型： **[ **D3DX10 \_ 圖像 \_ 檔案 \_ 格式**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="31db4-134">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

</dd> <dd>

<span data-ttu-id="31db4-135">代表影像檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="31db4-135">Represents the format of the image file.</span></span> <span data-ttu-id="31db4-136">請參閱 [**D3DX10 \_ 影像檔案 \_ \_ 格式**](d3dx10-image-file-format.md)。</span><span class="sxs-lookup"><span data-stu-id="31db4-136">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31db4-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="31db4-137">Requirements</span></span>



| <span data-ttu-id="31db4-138">需求</span><span class="sxs-lookup"><span data-stu-id="31db4-138">Requirement</span></span> | <span data-ttu-id="31db4-139">值</span><span class="sxs-lookup"><span data-stu-id="31db4-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="31db4-140">標頭</span><span class="sxs-lookup"><span data-stu-id="31db4-140">Header</span></span><br/> | <dl> <span data-ttu-id="31db4-141"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="31db4-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31db4-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31db4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31db4-143">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="31db4-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
