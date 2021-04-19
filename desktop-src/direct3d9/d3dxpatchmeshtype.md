---
description: 網狀修補類型。
ms.assetid: 229d01b2-781c-48a8-93f2-9dd9dbd67f3e
title: 'D3DXPATCHMESHTYPE 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHMESHTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d6a663e983b339d79ec89bf1b4ddfe7b4eaa9f1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993855"
---
# <a name="d3dxpatchmeshtype-enumeration"></a><span data-ttu-id="1c33b-103">D3DXPATCHMESHTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="1c33b-103">D3DXPATCHMESHTYPE enumeration</span></span>

<span data-ttu-id="1c33b-104">網狀修補類型。</span><span class="sxs-lookup"><span data-stu-id="1c33b-104">Mesh patch types.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c33b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c33b-105">Syntax</span></span>


```C++
typedef enum D3DXPATCHMESHTYPE { 
  D3DXPATCHMESH_RECT         = 0x001,
  D3DXPATCHMESH_TRI          = 0x002,
  D3DXPATCHMESH_NPATCH       = 0x003,
  D3DXPATCHMESH_FORCE_DWORD  = 0x7fffffff
} D3DXPATCHMESHTYPE, *LPD3DXPATCHMESHTYPE;
```



## <a name="constants"></a><span data-ttu-id="1c33b-106">常數</span><span class="sxs-lookup"><span data-stu-id="1c33b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1c33b-107"><span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH \_ RECT**</span><span class="sxs-lookup"><span data-stu-id="1c33b-107"><span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH\_RECT**</span></span>
</dt> <dd>

<span data-ttu-id="1c33b-108">矩形修補程式網格類型。</span><span class="sxs-lookup"><span data-stu-id="1c33b-108">Rectangle patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="1c33b-109"><span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH \_ 三**</span><span class="sxs-lookup"><span data-stu-id="1c33b-109"><span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH\_TRI**</span></span>
</dt> <dd>

<span data-ttu-id="1c33b-110">三角形 patch 網狀型別。</span><span class="sxs-lookup"><span data-stu-id="1c33b-110">Triangle patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="1c33b-111"><span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**D3DXPATCHMESH \_ NPATCH**</span><span class="sxs-lookup"><span data-stu-id="1c33b-111"><span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**D3DXPATCHMESH\_NPATCH**</span></span>
</dt> <dd>

<span data-ttu-id="1c33b-112">N-修補程式網格類型。</span><span class="sxs-lookup"><span data-stu-id="1c33b-112">N-patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="1c33b-113"><span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="1c33b-113"><span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="1c33b-114">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="1c33b-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="1c33b-115">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="1c33b-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="1c33b-116">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="1c33b-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c33b-117">備註</span><span class="sxs-lookup"><span data-stu-id="1c33b-117">Remarks</span></span>

<span data-ttu-id="1c33b-118">三角形修補程式有三個邊，在 [**D3DTRIPATCH \_ 資訊**](d3dtripatch-info.md)中有說明。</span><span class="sxs-lookup"><span data-stu-id="1c33b-118">Triangle patches have three sides and are described in [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span> <span data-ttu-id="1c33b-119">矩形修補程式為四側，在 [**D3DRECTPATCH \_ 資訊**](d3drectpatch-info.md)中有說明。</span><span class="sxs-lookup"><span data-stu-id="1c33b-119">Rectangle patches are four-sided and are described in [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c33b-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c33b-120">Requirements</span></span>



| <span data-ttu-id="1c33b-121">需求</span><span class="sxs-lookup"><span data-stu-id="1c33b-121">Requirement</span></span> | <span data-ttu-id="1c33b-122">值</span><span class="sxs-lookup"><span data-stu-id="1c33b-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c33b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="1c33b-123">Header</span></span><br/> | <dl> <span data-ttu-id="1c33b-124"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="1c33b-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c33b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c33b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c33b-126">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="1c33b-126">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="1c33b-127">使用 Higher-Order 基本 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="1c33b-127">Using Higher-Order Primitives (Direct3D 9)</span></span>](using-higher-order-primitives.md)
</dt> </dl>

 

 




