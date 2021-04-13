---
title: 'D3DX11_TEXTURE_LOAD_INFO 結構 (D3DX11tex .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 描述用來從另一個材質載入紋理的參數。
ms.assetid: 2fe24752-d1bc-4666-bf0f-cc397394da56
keywords:
- D3DX11_TEXTURE_LOAD_INFO 結構 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TEXTURE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca893908f854b6b127d783af25cc2fb9bc5df6a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992311"
---
# <a name="d3dx11_texture_load_info-structure"></a><span data-ttu-id="55651-105">D3DX11 \_ 材質 \_ 載入 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="55651-105">D3DX11\_TEXTURE\_LOAD\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="55651-106">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="55651-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="55651-107">描述用來從另一個材質載入紋理的參數。</span><span class="sxs-lookup"><span data-stu-id="55651-107">Describes parameters used to load a texture from another texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="55651-108">語法</span><span class="sxs-lookup"><span data-stu-id="55651-108">Syntax</span></span>


```C++
typedef struct _D3DX11_TEXTURE_LOAD_INFO {
  D3D11_BOX *pSrcBox;
  D3D11_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX11_TEXTURE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="55651-109">成員</span><span class="sxs-lookup"><span data-stu-id="55651-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="55651-110">**pSrcBox**</span><span class="sxs-lookup"><span data-stu-id="55651-110">**pSrcBox**</span></span>
</dt> <dd>

<span data-ttu-id="55651-111">Type： **[ **D3D11 \_ BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span><span class="sxs-lookup"><span data-stu-id="55651-111">Type: **[**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="55651-112">來源材質方塊 (查看 [**D3D11 \_ box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)) 。</span><span class="sxs-lookup"><span data-stu-id="55651-112">Source texture box (see [**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span></span>

</dd> <dt>

<span data-ttu-id="55651-113">**pDstBox**</span><span class="sxs-lookup"><span data-stu-id="55651-113">**pDstBox**</span></span>
</dt> <dd>

<span data-ttu-id="55651-114">Type： **[ **D3D11 \_ BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span><span class="sxs-lookup"><span data-stu-id="55651-114">Type: **[**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="55651-115">目的地材質方塊 (查看 [**D3D11 \_ box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)) 。</span><span class="sxs-lookup"><span data-stu-id="55651-115">Destination texture box (see [**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span></span>

</dd> <dt>

<span data-ttu-id="55651-116">**SrcFirstMip**</span><span class="sxs-lookup"><span data-stu-id="55651-116">**SrcFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="55651-117">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="55651-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="55651-118">來源紋理 mipmap 層級，如需詳細資料，請參閱 [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) 。</span><span class="sxs-lookup"><span data-stu-id="55651-118">Source texture mipmap level, see [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="55651-119">**DstFirstMip**</span><span class="sxs-lookup"><span data-stu-id="55651-119">**DstFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="55651-120">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="55651-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="55651-121">目的地紋理 mipmap 層級，如需詳細資料，請參閱 [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) 。</span><span class="sxs-lookup"><span data-stu-id="55651-121">Destination texture mipmap level, see [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="55651-122">**NumMips**</span><span class="sxs-lookup"><span data-stu-id="55651-122">**NumMips**</span></span>
</dt> <dd>

<span data-ttu-id="55651-123">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="55651-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="55651-124">來源材質中的 mipmap 層級數目。</span><span class="sxs-lookup"><span data-stu-id="55651-124">Number of mipmap levels in the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="55651-125">**SrcFirstElement**</span><span class="sxs-lookup"><span data-stu-id="55651-125">**SrcFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="55651-126">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="55651-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="55651-127">來源材質的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="55651-127">First element of the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="55651-128">**DstFirstElement**</span><span class="sxs-lookup"><span data-stu-id="55651-128">**DstFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="55651-129">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="55651-129">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="55651-130">目的地材質的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="55651-130">First element of the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="55651-131">**NumElements**</span><span class="sxs-lookup"><span data-stu-id="55651-131">**NumElements**</span></span>
</dt> <dd>

<span data-ttu-id="55651-132">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="55651-132">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="55651-133">要載入的元素數目。</span><span class="sxs-lookup"><span data-stu-id="55651-133">Number of elements to load.</span></span>

</dd> <dt>

<span data-ttu-id="55651-134">**Filter**</span><span class="sxs-lookup"><span data-stu-id="55651-134">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="55651-135">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="55651-135">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="55651-136">重新取樣期間的篩選選項 (參閱 [**D3DX11 \_ 篩選 \_ 旗**](d3dx11-filter-flag.md) 標) 。</span><span class="sxs-lookup"><span data-stu-id="55651-136">Filtering options during resampling (see [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md)).</span></span>

</dd> <dt>

<span data-ttu-id="55651-137">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="55651-137">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="55651-138">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="55651-138">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="55651-139">產生 mip 層級時的篩選選項 (參閱 [**D3DX11 \_ 篩選 \_ 旗**](d3dx11-filter-flag.md) 標) 。</span><span class="sxs-lookup"><span data-stu-id="55651-139">Filtering options when generating mip levels (see [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55651-140">備註</span><span class="sxs-lookup"><span data-stu-id="55651-140">Remarks</span></span>

<span data-ttu-id="55651-141">呼叫 [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md)時，會使用此結構。</span><span class="sxs-lookup"><span data-stu-id="55651-141">This structure is used in a call to [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).</span></span>

<span data-ttu-id="55651-142">預設值是：</span><span class="sxs-lookup"><span data-stu-id="55651-142">The default values are:</span></span>


```
    pSrcBox = NULL;
    pDstBox = NULL;
    SrcFirstMip = 0;
    DstFirstMip = 0;
    NumMips = D3DX11_DEFAULT;
    SrcFirstElement = 0;
    DstFirstElement = 0;
    NumElements = D3DX11_DEFAULT;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
```



## <a name="requirements"></a><span data-ttu-id="55651-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="55651-143">Requirements</span></span>



| <span data-ttu-id="55651-144">需求</span><span class="sxs-lookup"><span data-stu-id="55651-144">Requirement</span></span> | <span data-ttu-id="55651-145">值</span><span class="sxs-lookup"><span data-stu-id="55651-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55651-146">標頭</span><span class="sxs-lookup"><span data-stu-id="55651-146">Header</span></span><br/> | <dl> <span data-ttu-id="55651-147"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="55651-147"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55651-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55651-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55651-149">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="55651-149">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

