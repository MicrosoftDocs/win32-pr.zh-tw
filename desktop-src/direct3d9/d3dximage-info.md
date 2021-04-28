---
description: D3DXIMAGE_INFO 結構-傳回影像檔案原始內容的描述。
ms.assetid: d6cbd5b7-642e-43ce-a2ed-11a400c5bdc1
title: 'D3DXIMAGE_INFO 結構 (D3dx9tex .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_INFO
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: be70cc88645e0aac6734907c6a97f2d4bb104c99
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090536"
---
# <a name="d3dximage_info-structure"></a><span data-ttu-id="57bbb-103">D3DXIMAGE \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="57bbb-103">D3DXIMAGE\_INFO structure</span></span>

<span data-ttu-id="57bbb-104">傳回影像檔案原始內容的描述。</span><span class="sxs-lookup"><span data-stu-id="57bbb-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="57bbb-105">語法</span><span class="sxs-lookup"><span data-stu-id="57bbb-105">Syntax</span></span>


```C++
typedef struct D3DXIMAGE_INFO {
  UINT                 Width;
  UINT                 Height;
  UINT                 Depth;
  UINT                 MipLevels;
  D3DFORMAT            Format;
  D3DRESOURCETYPE      ResourceType;
  D3DXIMAGE_FILEFORMAT ImageFileFormat;
} D3DXIMAGE_INFO, *LPD3DXIMAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="57bbb-106">成員</span><span class="sxs-lookup"><span data-stu-id="57bbb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="57bbb-107">**寬度**</span><span class="sxs-lookup"><span data-stu-id="57bbb-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="57bbb-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57bbb-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="57bbb-109">原始影像的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="57bbb-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="57bbb-110">**高度**</span><span class="sxs-lookup"><span data-stu-id="57bbb-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="57bbb-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57bbb-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="57bbb-112">原始影像的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="57bbb-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="57bbb-113">**深度**</span><span class="sxs-lookup"><span data-stu-id="57bbb-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="57bbb-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57bbb-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="57bbb-115">原始影像的深度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="57bbb-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="57bbb-116">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="57bbb-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="57bbb-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57bbb-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="57bbb-118">原始影像中的 mip 層級數目。</span><span class="sxs-lookup"><span data-stu-id="57bbb-118">Number of mip levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="57bbb-119">**格式**</span><span class="sxs-lookup"><span data-stu-id="57bbb-119">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="57bbb-120">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="57bbb-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="57bbb-121">[D3DFORMAT](d3dformat.md)列舉型別中最能描述原始影像中資料的值。</span><span class="sxs-lookup"><span data-stu-id="57bbb-121">A value from the [D3DFORMAT](d3dformat.md) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="57bbb-122">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="57bbb-122">**ResourceType**</span></span>
</dt> <dd>

<span data-ttu-id="57bbb-123">類型： **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="57bbb-123">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="57bbb-124">表示儲存在檔案中的材質類型。</span><span class="sxs-lookup"><span data-stu-id="57bbb-124">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="57bbb-125">它可以是 D3DRTYPE \_ 材質、D3DRTYPE \_ VOLUMETEXTURE 或 D3DRTYPE \_ CubeTexture。</span><span class="sxs-lookup"><span data-stu-id="57bbb-125">It is either D3DRTYPE\_TEXTURE, D3DRTYPE\_VOLUMETEXTURE, or D3DRTYPE\_CubeTexture.</span></span>

</dd> <dt>

<span data-ttu-id="57bbb-126">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="57bbb-126">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="57bbb-127">類型： **[ **D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="57bbb-127">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="57bbb-128">代表影像檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="57bbb-128">Represents the format of the image file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="57bbb-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="57bbb-129">Requirements</span></span>



| <span data-ttu-id="57bbb-130">需求</span><span class="sxs-lookup"><span data-stu-id="57bbb-130">Requirement</span></span> | <span data-ttu-id="57bbb-131">值</span><span class="sxs-lookup"><span data-stu-id="57bbb-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57bbb-132">標頭</span><span class="sxs-lookup"><span data-stu-id="57bbb-132">Header</span></span><br/> | <dl> <span data-ttu-id="57bbb-133"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="57bbb-133"><dt>D3dx9tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57bbb-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57bbb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57bbb-135">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="57bbb-135">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
