---
description: 傳回影像檔案原始內容的描述。
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
ms.openlocfilehash: 6ec152dc56dcea3a718cf5cd42fb351d4fddf852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696635"
---
# <a name="d3dximage_info-structure"></a><span data-ttu-id="022e4-103">D3DXIMAGE \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="022e4-103">D3DXIMAGE\_INFO structure</span></span>

<span data-ttu-id="022e4-104">傳回影像檔案原始內容的描述。</span><span class="sxs-lookup"><span data-stu-id="022e4-104">Returns a description of the original contents of an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="022e4-105">語法</span><span class="sxs-lookup"><span data-stu-id="022e4-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="022e4-106">成員</span><span class="sxs-lookup"><span data-stu-id="022e4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="022e4-107">**寬度**</span><span class="sxs-lookup"><span data-stu-id="022e4-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="022e4-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="022e4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="022e4-109">原始影像的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="022e4-109">Width of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="022e4-110">**高度**</span><span class="sxs-lookup"><span data-stu-id="022e4-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="022e4-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="022e4-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="022e4-112">原始影像的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="022e4-112">Height of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="022e4-113">**深度**</span><span class="sxs-lookup"><span data-stu-id="022e4-113">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="022e4-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="022e4-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="022e4-115">原始影像的深度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="022e4-115">Depth of original image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="022e4-116">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="022e4-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="022e4-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="022e4-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="022e4-118">原始影像中的 mip 層級數目。</span><span class="sxs-lookup"><span data-stu-id="022e4-118">Number of mip levels in original image.</span></span>

</dd> <dt>

<span data-ttu-id="022e4-119">**格式**</span><span class="sxs-lookup"><span data-stu-id="022e4-119">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="022e4-120">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="022e4-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="022e4-121">[D3DFORMAT](d3dformat.md)列舉型別中最能描述原始影像中資料的值。</span><span class="sxs-lookup"><span data-stu-id="022e4-121">A value from the [D3DFORMAT](d3dformat.md) enumerated type that most closely describes the data in the original image.</span></span>

</dd> <dt>

<span data-ttu-id="022e4-122">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="022e4-122">**ResourceType**</span></span>
</dt> <dd>

<span data-ttu-id="022e4-123">類型： **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="022e4-123">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="022e4-124">表示儲存在檔案中的材質類型。</span><span class="sxs-lookup"><span data-stu-id="022e4-124">Represents the type of the texture stored in the file.</span></span> <span data-ttu-id="022e4-125">它可以是 D3DRTYPE \_ 材質、D3DRTYPE \_ VOLUMETEXTURE 或 D3DRTYPE \_ CubeTexture。</span><span class="sxs-lookup"><span data-stu-id="022e4-125">It is either D3DRTYPE\_TEXTURE, D3DRTYPE\_VOLUMETEXTURE, or D3DRTYPE\_CubeTexture.</span></span>

</dd> <dt>

<span data-ttu-id="022e4-126">**ImageFileFormat**</span><span class="sxs-lookup"><span data-stu-id="022e4-126">**ImageFileFormat**</span></span>
</dt> <dd>

<span data-ttu-id="022e4-127">類型： **[ **D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="022e4-127">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="022e4-128">代表影像檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="022e4-128">Represents the format of the image file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="022e4-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="022e4-129">Requirements</span></span>



| <span data-ttu-id="022e4-130">需求</span><span class="sxs-lookup"><span data-stu-id="022e4-130">Requirement</span></span> | <span data-ttu-id="022e4-131">值</span><span class="sxs-lookup"><span data-stu-id="022e4-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="022e4-132">標頭</span><span class="sxs-lookup"><span data-stu-id="022e4-132">Header</span></span><br/> | <dl> <span data-ttu-id="022e4-133"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="022e4-133"><dt>D3dx9tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="022e4-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="022e4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="022e4-135">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="022e4-135">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
