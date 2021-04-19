---
description: 用來指定網格之建立選項的旗標。
ms.assetid: 1a5a6b3f-34f4-4338-9ffe-8f95f6f0c385
title: 'D3DX10_MESH 列舉 (D3DX10Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: c2387024512a42c0a9e06ac1818b0282121cd0eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982225"
---
# <a name="d3dx10_mesh-enumeration"></a><span data-ttu-id="3859e-103">D3DX10 \_ 網格列舉</span><span class="sxs-lookup"><span data-stu-id="3859e-103">D3DX10\_MESH enumeration</span></span>

<span data-ttu-id="3859e-104">用來指定網格之建立選項的旗標。</span><span class="sxs-lookup"><span data-stu-id="3859e-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="3859e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3859e-105">Syntax</span></span>


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a><span data-ttu-id="3859e-106">常數</span><span class="sxs-lookup"><span data-stu-id="3859e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3859e-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 \_ 網格 \_ 32 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="3859e-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10\_MESH\_32\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="3859e-108">網格有32位的索引，而不是16位的索引。</span><span class="sxs-lookup"><span data-stu-id="3859e-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="3859e-109">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="3859e-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3859e-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10 \_ 網格 \_ GS \_ 相鄰**</span><span class="sxs-lookup"><span data-stu-id="3859e-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10\_MESH\_GS\_ADJACENCY**</span></span>
</dt> <dd>

<span data-ttu-id="3859e-111">指示網格包含幾何著色器的相鄰資料。</span><span class="sxs-lookup"><span data-stu-id="3859e-111">Signals that the mesh contains geometry shader adjacency data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3859e-112">備註</span><span class="sxs-lookup"><span data-stu-id="3859e-112">Remarks</span></span>

<span data-ttu-id="3859e-113">32位網格 (D3DXMESH 32 位 \_) 理論上可支援 (2 ³²) -1 臉部和頂點。</span><span class="sxs-lookup"><span data-stu-id="3859e-113">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2³²)-1 faces and vertices.</span></span> <span data-ttu-id="3859e-114">不過，為在32位作業系統上大的網狀架構配置記憶體並不實用。</span><span class="sxs-lookup"><span data-stu-id="3859e-114">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="3859e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="3859e-115">Requirements</span></span>



| <span data-ttu-id="3859e-116">需求</span><span class="sxs-lookup"><span data-stu-id="3859e-116">Requirement</span></span> | <span data-ttu-id="3859e-117">值</span><span class="sxs-lookup"><span data-stu-id="3859e-117">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3859e-118">標頭</span><span class="sxs-lookup"><span data-stu-id="3859e-118">Header</span></span><br/> | <dl> <span data-ttu-id="3859e-119"><dt>D3DX10Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="3859e-119"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3859e-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3859e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3859e-121">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="3859e-121">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




