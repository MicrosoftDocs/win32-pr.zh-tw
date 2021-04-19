---
description: 描述三角形高序位修補程式。
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: 'D3DTRIPATCH_INFO 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRIPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b910d38025c44d6157a76aa3e3425ba46d628787
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976728"
---
# <a name="d3dtripatch_info-structure"></a><span data-ttu-id="297e0-103">D3DTRIPATCH \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="297e0-103">D3DTRIPATCH\_INFO structure</span></span>

<span data-ttu-id="297e0-104">描述三角形高序位修補程式。</span><span class="sxs-lookup"><span data-stu-id="297e0-104">Describes a triangular high-order patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="297e0-105">語法</span><span class="sxs-lookup"><span data-stu-id="297e0-105">Syntax</span></span>


```C++
typedef struct D3DTRIPATCH_INFO {
  UINT          StartVertexOffset;
  UINT          NumVertices;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DTRIPATCH_INFO, *LPD3DTRIPATCH_INFO;
```



## <a name="members"></a><span data-ttu-id="297e0-106">成員</span><span class="sxs-lookup"><span data-stu-id="297e0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="297e0-107">**StartVertexOffset**</span><span class="sxs-lookup"><span data-stu-id="297e0-107">**StartVertexOffset**</span></span>
</dt> <dd>

<span data-ttu-id="297e0-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="297e0-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="297e0-109">以頂點數目起始頂點位移。</span><span class="sxs-lookup"><span data-stu-id="297e0-109">Starting vertex offset, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="297e0-110">**NumVertices**</span><span class="sxs-lookup"><span data-stu-id="297e0-110">**NumVertices**</span></span>
</dt> <dd>

<span data-ttu-id="297e0-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="297e0-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="297e0-112">頂點數目。</span><span class="sxs-lookup"><span data-stu-id="297e0-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="297e0-113">**Basis**</span><span class="sxs-lookup"><span data-stu-id="297e0-113">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="297e0-114">類型： **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="297e0-114">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="297e0-115">[**D3DBASISTYPE**](./d3dbasistype.md)列舉型別的成員，它會定義三角形高序位修補程式的基礎型別。</span><span class="sxs-lookup"><span data-stu-id="297e0-115">Member of the [**D3DBASISTYPE**](./d3dbasistype.md) enumerated type, which defines the basis type for the triangular high-order patch.</span></span> <span data-ttu-id="297e0-116">此成員唯一有效的值為 D3DBASIS \_ 貝塞爾。</span><span class="sxs-lookup"><span data-stu-id="297e0-116">The only valid value for this member is D3DBASIS\_BEZIER.</span></span>

</dd> <dt>

<span data-ttu-id="297e0-117">**角度**</span><span class="sxs-lookup"><span data-stu-id="297e0-117">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="297e0-118">類型： **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="297e0-118">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="297e0-119">[**D3DDEGREETYPE**](./d3ddegreetype.md)列舉型別的成員，定義三角形高序位修補程式的程度型別。</span><span class="sxs-lookup"><span data-stu-id="297e0-119">Member of the [**D3DDEGREETYPE**](./d3ddegreetype.md) enumerated type, defining the degree type for the triangular high-order patch.</span></span>



| <span data-ttu-id="297e0-120">值</span><span class="sxs-lookup"><span data-stu-id="297e0-120">Value</span></span>                | <span data-ttu-id="297e0-121">頂點數目</span><span class="sxs-lookup"><span data-stu-id="297e0-121">Number of vertices</span></span> |
|----------------------|--------------------|
| <span data-ttu-id="297e0-122">D3DDEGREE \_ 立方</span><span class="sxs-lookup"><span data-stu-id="297e0-122">D3DDEGREE\_CUBIC</span></span>     | <span data-ttu-id="297e0-123">10</span><span class="sxs-lookup"><span data-stu-id="297e0-123">10</span></span>                 |
| <span data-ttu-id="297e0-124">D3DDEGREE \_ 線性</span><span class="sxs-lookup"><span data-stu-id="297e0-124">D3DDEGREE\_LINEAR</span></span>    | <span data-ttu-id="297e0-125">3</span><span class="sxs-lookup"><span data-stu-id="297e0-125">3</span></span>                  |
| <span data-ttu-id="297e0-126">D3DDEGREE \_ 二次</span><span class="sxs-lookup"><span data-stu-id="297e0-126">D3DDEGREE\_QUADRATIC</span></span> | <span data-ttu-id="297e0-127">N/A</span><span class="sxs-lookup"><span data-stu-id="297e0-127">N/A</span></span>                |
| <span data-ttu-id="297e0-128">D3DDEGREE \_ QUINTIC</span><span class="sxs-lookup"><span data-stu-id="297e0-128">D3DDEGREE\_QUINTIC</span></span>   | <span data-ttu-id="297e0-129">21</span><span class="sxs-lookup"><span data-stu-id="297e0-129">21</span></span>                 |



 

<span data-ttu-id="297e0-130">N/A-無法使用。</span><span class="sxs-lookup"><span data-stu-id="297e0-130">N/A - Not available.</span></span> <span data-ttu-id="297e0-131">不支援。</span><span class="sxs-lookup"><span data-stu-id="297e0-131">Not supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="297e0-132">備註</span><span class="sxs-lookup"><span data-stu-id="297e0-132">Remarks</span></span>

<span data-ttu-id="297e0-133">例如，下圖識別三次方貝塞爾三角形修補程式的頂點順序和區段編號。</span><span class="sxs-lookup"><span data-stu-id="297e0-133">For example, the following diagram identifies the vertex order and segment numbers for a cubic Bézier triangle patch.</span></span> <span data-ttu-id="297e0-134">頂點順序可決定 [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)所使用的區段編號。</span><span class="sxs-lookup"><span data-stu-id="297e0-134">The vertex order determines the segment numbers used by [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch).</span></span> <span data-ttu-id="297e0-135">位移是頂點緩衝區中第一個三角形 patch 頂點的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="297e0-135">The offset is the number of bytes to the first triangle patch vertex in the vertex buffer.</span></span>

![具有九個頂點的三角形高序位修補程式圖](images/hop-tripatch-info.png)

## <a name="requirements"></a><span data-ttu-id="297e0-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="297e0-137">Requirements</span></span>



| <span data-ttu-id="297e0-138">需求</span><span class="sxs-lookup"><span data-stu-id="297e0-138">Requirement</span></span> | <span data-ttu-id="297e0-139">值</span><span class="sxs-lookup"><span data-stu-id="297e0-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="297e0-140">標頭</span><span class="sxs-lookup"><span data-stu-id="297e0-140">Header</span></span><br/> | <dl> <span data-ttu-id="297e0-141"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="297e0-141"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="297e0-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="297e0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="297e0-143">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="297e0-143">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="297e0-144">**DrawTriPatch**</span><span class="sxs-lookup"><span data-stu-id="297e0-144">**DrawTriPatch**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[<span data-ttu-id="297e0-145">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="297e0-145">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
