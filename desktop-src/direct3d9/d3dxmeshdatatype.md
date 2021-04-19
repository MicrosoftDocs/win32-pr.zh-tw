---
description: 定義存在於 D3DXMESHDATA 中的網格資料類型。
ms.assetid: e5324f85-17cc-46a7-886a-c8f3464baade
title: 'D3DXMESHDATATYPE 列舉 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATATYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 9dea67984992e4bb26cd9e2613013169b1ff097d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985884"
---
# <a name="d3dxmeshdatatype-enumeration"></a><span data-ttu-id="9536b-103">D3DXMESHDATATYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="9536b-103">D3DXMESHDATATYPE enumeration</span></span>

<span data-ttu-id="9536b-104">定義存在於 [**D3DXMESHDATA**](d3dxmeshdata.md)中的網格資料類型。</span><span class="sxs-lookup"><span data-stu-id="9536b-104">Defines the type of mesh data present in [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9536b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9536b-105">Syntax</span></span>


```C++
typedef enum D3DXMESHDATATYPE { 
  D3DXMESHTYPE_MESH         = 0x001,
  D3DXMESHTYPE_PATCHMESH    = 0x003,
  D3DXMESHTYPE_FORCE_DWORD  = 0x7fffffff
} D3DXMESHDATATYPE, *LPD3DXMESHDATATYPE;
```



## <a name="constants"></a><span data-ttu-id="9536b-106">常數</span><span class="sxs-lookup"><span data-stu-id="9536b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9536b-107"><span id="D3DXMESHTYPE_MESH"></span><span id="d3dxmeshtype_mesh"></span>**D3DXMESHTYPE \_ 網格**</span><span class="sxs-lookup"><span data-stu-id="9536b-107"><span id="D3DXMESHTYPE_MESH"></span><span id="d3dxmeshtype_mesh"></span>**D3DXMESHTYPE\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="9536b-108">資料類型是網格。</span><span class="sxs-lookup"><span data-stu-id="9536b-108">The data type is a mesh.</span></span> <span data-ttu-id="9536b-109">請參閱 [**ID3DXMesh**](id3dxmesh.md)。</span><span class="sxs-lookup"><span data-stu-id="9536b-109">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="9536b-110"><span id="D3DXMESHTYPE_PATCHMESH"></span><span id="d3dxmeshtype_patchmesh"></span>**D3DXMESHTYPE \_ PATCHMESH**</span><span class="sxs-lookup"><span data-stu-id="9536b-110"><span id="D3DXMESHTYPE_PATCHMESH"></span><span id="d3dxmeshtype_patchmesh"></span>**D3DXMESHTYPE\_PATCHMESH**</span></span>
</dt> <dd>

<span data-ttu-id="9536b-111">資料類型是修補程式網格。</span><span class="sxs-lookup"><span data-stu-id="9536b-111">The data type is a patch mesh.</span></span> <span data-ttu-id="9536b-112">請參閱 [**ID3DXPatchMesh**](id3dxpatchmesh.md)。</span><span class="sxs-lookup"><span data-stu-id="9536b-112">See [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="9536b-113"><span id="D3DXMESHTYPE_FORCE_DWORD"></span><span id="d3dxmeshtype_force_dword"></span>**D3DXMESHTYPE \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="9536b-113"><span id="D3DXMESHTYPE_FORCE_DWORD"></span><span id="d3dxmeshtype_force_dword"></span>**D3DXMESHTYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="9536b-114">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="9536b-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="9536b-115">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="9536b-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="9536b-116">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="9536b-116">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9536b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9536b-117">Requirements</span></span>



| <span data-ttu-id="9536b-118">需求</span><span class="sxs-lookup"><span data-stu-id="9536b-118">Requirement</span></span> | <span data-ttu-id="9536b-119">值</span><span class="sxs-lookup"><span data-stu-id="9536b-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9536b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9536b-120">Header</span></span><br/> | <dl> <span data-ttu-id="9536b-121"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="9536b-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9536b-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9536b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9536b-123">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="9536b-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="9536b-124">**D3DXMESHDATA**</span><span class="sxs-lookup"><span data-stu-id="9536b-124">**D3DXMESHDATA**</span></span>](d3dxmeshdata.md)
</dt> </dl>

 

 




