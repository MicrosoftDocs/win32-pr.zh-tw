---
description: 描述矩形高序位修補程式。
ms.assetid: 5f195009-d047-4dc0-a386-e1a434914e34
title: 'D3DRECTPATCH_INFO 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECTPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a2b7fedbaac2cc9c204d4691828d31794cea1f47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975682"
---
# <a name="d3drectpatch_info-structure"></a><span data-ttu-id="d4394-103">D3DRECTPATCH \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="d4394-103">D3DRECTPATCH\_INFO structure</span></span>

<span data-ttu-id="d4394-104">描述矩形高序位修補程式。</span><span class="sxs-lookup"><span data-stu-id="d4394-104">Describes a rectangular high-order patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4394-105">語法</span><span class="sxs-lookup"><span data-stu-id="d4394-105">Syntax</span></span>


```C++
typedef struct D3DRECTPATCH_INFO {
  UINT          StartVertexOffsetWidth;
  UINT          StartVertexOffsetHeight;
  UINT          Width;
  UINT          Height;
  UINT          Stride;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DRECTPATCH_INFO, *LPD3DRECTPATCH_INFO;
```



## <a name="members"></a><span data-ttu-id="d4394-106">成員</span><span class="sxs-lookup"><span data-stu-id="d4394-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d4394-107">**StartVertexOffsetWidth**</span><span class="sxs-lookup"><span data-stu-id="d4394-107">**StartVertexOffsetWidth**</span></span>
</dt> <dd>

<span data-ttu-id="d4394-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4394-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4394-109">開始頂點位移寬度（以頂點數目為限）。</span><span class="sxs-lookup"><span data-stu-id="d4394-109">Starting vertex offset width, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d4394-110">**StartVertexOffsetHeight**</span><span class="sxs-lookup"><span data-stu-id="d4394-110">**StartVertexOffsetHeight**</span></span>
</dt> <dd>

<span data-ttu-id="d4394-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4394-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4394-112">開始頂點位移高度（以頂點數目為限）。</span><span class="sxs-lookup"><span data-stu-id="d4394-112">Starting vertex offset height, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d4394-113">**寬度**</span><span class="sxs-lookup"><span data-stu-id="d4394-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="d4394-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4394-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4394-115">每個頂點的寬度（以頂點的數目為限）。</span><span class="sxs-lookup"><span data-stu-id="d4394-115">Width of each vertex, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d4394-116">**高度**</span><span class="sxs-lookup"><span data-stu-id="d4394-116">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="d4394-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4394-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4394-118">每個頂點的高度（以頂點數目為限）。</span><span class="sxs-lookup"><span data-stu-id="d4394-118">Height of each vertex, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d4394-119">**分散**</span><span class="sxs-lookup"><span data-stu-id="d4394-119">**Stride**</span></span>
</dt> <dd>

<span data-ttu-id="d4394-120">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4394-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4394-121">虛數二維頂點陣列的寬度，其佔用的空間與頂點緩衝區相同。</span><span class="sxs-lookup"><span data-stu-id="d4394-121">Width of the imaginary two-dimensional vertex array, which occupies the same space as the vertex buffer.</span></span> <span data-ttu-id="d4394-122">如需範例，請參閱下圖。</span><span class="sxs-lookup"><span data-stu-id="d4394-122">For an example, see the diagram below.</span></span>

</dd> <dt>

<span data-ttu-id="d4394-123">**Basis**</span><span class="sxs-lookup"><span data-stu-id="d4394-123">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="d4394-124">類型： **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="d4394-124">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4394-125">[**D3DBASISTYPE**](./d3dbasistype.md)列舉型別的成員，定義矩形高序位修補程式的基礎型別。</span><span class="sxs-lookup"><span data-stu-id="d4394-125">Member of the [**D3DBASISTYPE**](./d3dbasistype.md) enumerated type, defining the basis type for the rectangular high-order patch.</span></span>



| <span data-ttu-id="d4394-126">值</span><span class="sxs-lookup"><span data-stu-id="d4394-126">Value</span></span>                 | <span data-ttu-id="d4394-127">支援的訂單</span><span class="sxs-lookup"><span data-stu-id="d4394-127">Order supported</span></span>            | <span data-ttu-id="d4394-128">寬度和高度</span><span class="sxs-lookup"><span data-stu-id="d4394-128">Width and height</span></span>                  |
|-----------------------|----------------------------|-----------------------------------|
| <span data-ttu-id="d4394-129">D3DBASIS \_ 貝塞爾</span><span class="sxs-lookup"><span data-stu-id="d4394-129">D3DBASIS\_BEZIER</span></span>      | <span data-ttu-id="d4394-130">線性、三個和 quintic</span><span class="sxs-lookup"><span data-stu-id="d4394-130">Linear, cubic, and quintic</span></span> | <span data-ttu-id="d4394-131">Width = height = (DWORD) order + 1</span><span class="sxs-lookup"><span data-stu-id="d4394-131">Width = height = (DWORD)order + 1</span></span> |
| <span data-ttu-id="d4394-132">D3DBASIS \_ BSPLINE</span><span class="sxs-lookup"><span data-stu-id="d4394-132">D3DBASIS\_BSPLINE</span></span>     | <span data-ttu-id="d4394-133">線性、三個和 quintic</span><span class="sxs-lookup"><span data-stu-id="d4394-133">Linear, cubic, and quintic</span></span> | <span data-ttu-id="d4394-134">Width = height > (DWORD) 順序</span><span class="sxs-lookup"><span data-stu-id="d4394-134">Width = height > (DWORD)order</span></span>  |
| <span data-ttu-id="d4394-135">D3DBASIS \_ 插補</span><span class="sxs-lookup"><span data-stu-id="d4394-135">D3DBASIS\_INTERPOLATE</span></span> | <span data-ttu-id="d4394-136">立方</span><span class="sxs-lookup"><span data-stu-id="d4394-136">Cubic</span></span>                      | <span data-ttu-id="d4394-137">Width = height > (DWORD) 順序</span><span class="sxs-lookup"><span data-stu-id="d4394-137">Width = height > (DWORD)order</span></span>  |



 

</dd> <dt>

<span data-ttu-id="d4394-138">**角度**</span><span class="sxs-lookup"><span data-stu-id="d4394-138">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="d4394-139">類型： **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="d4394-139">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4394-140">[**D3DDEGREETYPE**](./d3ddegreetype.md)列舉型別的成員，定義矩形修補程式的程度。</span><span class="sxs-lookup"><span data-stu-id="d4394-140">Member of the [**D3DDEGREETYPE**](./d3ddegreetype.md) enumerated type, defining the degree for the rectangular patch.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4394-141">備註</span><span class="sxs-lookup"><span data-stu-id="d4394-141">Remarks</span></span>

<span data-ttu-id="d4394-142">下圖識別指定矩形修補程式的參數。</span><span class="sxs-lookup"><span data-stu-id="d4394-142">The following diagram identifies the parameters that specify a rectangle patch.</span></span>

![矩形高序位修補程式的圖表，以及指定它的參數](images/hop-rectpatch.png)

<span data-ttu-id="d4394-144">頂點緩衝區中的每個頂點都會顯示為黑色點。</span><span class="sxs-lookup"><span data-stu-id="d4394-144">Each of the vertices in the vertex buffer is shown as a black dot.</span></span> <span data-ttu-id="d4394-145">在此情況下，頂點緩衝區中有20個頂點，矩形 patch 中有16個。</span><span class="sxs-lookup"><span data-stu-id="d4394-145">In this case, the vertex buffer has 20 vertices in it, 16 of which are in the rectangle patch.</span></span> <span data-ttu-id="d4394-146">Stride 是頂點緩衝區寬度的頂點數目，在此案例中為五。</span><span class="sxs-lookup"><span data-stu-id="d4394-146">The stride is the number of vertices in the width of the vertex buffer, in this case five.</span></span> <span data-ttu-id="d4394-147">第一個頂點的 x 位移稱為 StartIndexVertexWidth，在此案例中為1。</span><span class="sxs-lookup"><span data-stu-id="d4394-147">The x offset to the first vertex is called the StartIndexVertexWidth and is in this case 1.</span></span> <span data-ttu-id="d4394-148">第一個 patch 頂點的 y 位移稱為 StartIndexVertexHeight，在此案例中為0。</span><span class="sxs-lookup"><span data-stu-id="d4394-148">The y offset to the first patch vertex is called the StartIndexVertexHeight and is in this case 0.</span></span>

<span data-ttu-id="d4394-149">若要將個別矩形修補程式的資料流程轉譯 (非馬賽克) ，您應該將幾何轉譯為 long 窄 (1 x N) 矩形修補程式。</span><span class="sxs-lookup"><span data-stu-id="d4394-149">To render a stream of individual rectangular patches (non-mosaic), you should interpret your geometry as a long narrow (1 x N) rectangular patch.</span></span> <span data-ttu-id="d4394-150">這類區域 (三次方貝塞爾) 的 **D3DRECTPATCH \_ 資訊** 結構會以下列方式設定。</span><span class="sxs-lookup"><span data-stu-id="d4394-150">The **D3DRECTPATCH\_INFO** structure for such a strip (cubic Bézier) would be set up in the following manner.</span></span>


```
    
D3DRECTPATCH_INFO RectInfo;

RectInfo.Width = 4;
RectInfo.Height = 4;
RectInfo.Stride = 4;
RectInfo.Basis = D3DBASIS_BEZIER;
RectInfo.Order = D3DORDER_CUBIC;
RectInfo.StartVertexOffsetWidth = 0;
RectInfo.StartVertexOffsetHeight = 4*i;  // The variable i is the index of the 
//   patch you want to render.
```



## <a name="requirements"></a><span data-ttu-id="d4394-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4394-151">Requirements</span></span>



| <span data-ttu-id="d4394-152">需求</span><span class="sxs-lookup"><span data-stu-id="d4394-152">Requirement</span></span> | <span data-ttu-id="d4394-153">值</span><span class="sxs-lookup"><span data-stu-id="d4394-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4394-154">標頭</span><span class="sxs-lookup"><span data-stu-id="d4394-154">Header</span></span><br/> | <dl> <span data-ttu-id="d4394-155"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4394-155"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4394-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4394-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4394-157">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="d4394-157">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="d4394-158">**DrawRectPatch**</span><span class="sxs-lookup"><span data-stu-id="d4394-158">**DrawRectPatch**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)
</dt> <dt>

[<span data-ttu-id="d4394-159">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="d4394-159">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
