---
description: 描述用來從另一個材質載入紋理的參數。
ms.assetid: dee693ce-afa7-479b-a76a-00816e30d5cf
title: 'D3DX10_TEXTURE_LOAD_INFO 結構 (D3DX10Tex .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_TEXTURE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: d3a689bb2104ee4cb419eb1483619d1fcf71d7e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986105"
---
# <a name="d3dx10_texture_load_info-structure"></a><span data-ttu-id="69da4-103">D3DX10 \_ 材質 \_ 載入 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="69da4-103">D3DX10\_TEXTURE\_LOAD\_INFO structure</span></span>

<span data-ttu-id="69da4-104">描述用來從另一個材質載入紋理的參數。</span><span class="sxs-lookup"><span data-stu-id="69da4-104">Describes parameters used to load a texture from another texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="69da4-105">語法</span><span class="sxs-lookup"><span data-stu-id="69da4-105">Syntax</span></span>


```C++
typedef struct _D3DX10_TEXTURE_LOAD_INFO {
  D3D10_BOX *pSrcBox;
  D3D10_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX10_TEXTURE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="69da4-106">成員</span><span class="sxs-lookup"><span data-stu-id="69da4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="69da4-107">**pSrcBox**</span><span class="sxs-lookup"><span data-stu-id="69da4-107">**pSrcBox**</span></span>
</dt> <dd>

<span data-ttu-id="69da4-108">Type： **[ **D3D10 \_ BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span><span class="sxs-lookup"><span data-stu-id="69da4-108">Type: **[**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="69da4-109">來源材質方塊 (查看 [**D3D10 \_ box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)) 。</span><span class="sxs-lookup"><span data-stu-id="69da4-109">Source texture box (see [**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span></span>

</dd> <dt>

<span data-ttu-id="69da4-110">**pDstBox**</span><span class="sxs-lookup"><span data-stu-id="69da4-110">**pDstBox**</span></span>
</dt> <dd>

<span data-ttu-id="69da4-111">Type： **[ **D3D10 \_ BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span><span class="sxs-lookup"><span data-stu-id="69da4-111">Type: **[**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="69da4-112">目的地材質方塊 (查看 [**D3D10 \_ box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)) 。</span><span class="sxs-lookup"><span data-stu-id="69da4-112">Destination texture box (see [**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span></span>

</dd> <dt>

<span data-ttu-id="69da4-113">**SrcFirstMip**</span><span class="sxs-lookup"><span data-stu-id="69da4-113">**SrcFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="69da4-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69da4-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="69da4-115">來源紋理 mipmap 層級，如需詳細資料，請參閱 [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) 。</span><span class="sxs-lookup"><span data-stu-id="69da4-115">Source texture mipmap level, see [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="69da4-116">**DstFirstMip**</span><span class="sxs-lookup"><span data-stu-id="69da4-116">**DstFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="69da4-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69da4-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="69da4-118">目的地紋理 mipmap 層級，如需詳細資料，請參閱 [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) 。</span><span class="sxs-lookup"><span data-stu-id="69da4-118">Destination texture mipmap level, see [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="69da4-119">**NumMips**</span><span class="sxs-lookup"><span data-stu-id="69da4-119">**NumMips**</span></span>
</dt> <dd>

<span data-ttu-id="69da4-120">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69da4-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="69da4-121">來源材質中的 mipmap 層級數目。</span><span class="sxs-lookup"><span data-stu-id="69da4-121">Number of mipmap levels in the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="69da4-122">**SrcFirstElement**</span><span class="sxs-lookup"><span data-stu-id="69da4-122">**SrcFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="69da4-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69da4-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="69da4-124">來源材質的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="69da4-124">First element of the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="69da4-125">**DstFirstElement**</span><span class="sxs-lookup"><span data-stu-id="69da4-125">**DstFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="69da4-126">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69da4-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="69da4-127">目的地材質的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="69da4-127">First element of the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="69da4-128">**NumElements**</span><span class="sxs-lookup"><span data-stu-id="69da4-128">**NumElements**</span></span>
</dt> <dd>

<span data-ttu-id="69da4-129">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69da4-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="69da4-130">要載入的元素數目。</span><span class="sxs-lookup"><span data-stu-id="69da4-130">Number of elements to load.</span></span>

</dd> <dt>

<span data-ttu-id="69da4-131">**Filter**</span><span class="sxs-lookup"><span data-stu-id="69da4-131">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="69da4-132">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69da4-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="69da4-133">重新取樣期間的篩選選項 (參閱 [**D3DX10 \_ 篩選 \_ 旗**](d3dx10-filter-flag.md) 標) 。</span><span class="sxs-lookup"><span data-stu-id="69da4-133">Filtering options during resampling (see [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md)).</span></span>

</dd> <dt>

<span data-ttu-id="69da4-134">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="69da4-134">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="69da4-135">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69da4-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="69da4-136">產生 mip 層級時的篩選選項 (參閱 [**D3DX10 \_ 篩選 \_ 旗**](d3dx10-filter-flag.md) 標) 。</span><span class="sxs-lookup"><span data-stu-id="69da4-136">Filtering options when generating mip levels (see [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69da4-137">備註</span><span class="sxs-lookup"><span data-stu-id="69da4-137">Remarks</span></span>

<span data-ttu-id="69da4-138">呼叫 [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md)時，會使用此結構。</span><span class="sxs-lookup"><span data-stu-id="69da4-138">This structure is used in a call to [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69da4-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="69da4-139">Requirements</span></span>



| <span data-ttu-id="69da4-140">需求</span><span class="sxs-lookup"><span data-stu-id="69da4-140">Requirement</span></span> | <span data-ttu-id="69da4-141">值</span><span class="sxs-lookup"><span data-stu-id="69da4-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69da4-142">標頭</span><span class="sxs-lookup"><span data-stu-id="69da4-142">Header</span></span><br/> | <dl> <span data-ttu-id="69da4-143"><dt>D3DX10Tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="69da4-143"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69da4-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69da4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69da4-145">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="69da4-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
