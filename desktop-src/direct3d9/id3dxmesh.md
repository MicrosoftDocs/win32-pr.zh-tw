---
description: 應用程式會使用 ID3DXMesh 介面的方法來操作網格物件。
ms.assetid: f571fe0b-3f0c-43c9-809c-d1e14f85b720
title: 'ID3DXMesh 介面 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c2a677edba4bad5e908b6dd69aa21a467b2a245
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323263"
---
# <a name="id3dxmesh-interface"></a><span data-ttu-id="a1a22-103">ID3DXMesh 介面</span><span class="sxs-lookup"><span data-stu-id="a1a22-103">ID3DXMesh interface</span></span>

<span data-ttu-id="a1a22-104">應用程式會使用 ID3DXMesh 介面的方法來操作網格物件。</span><span class="sxs-lookup"><span data-stu-id="a1a22-104">Applications use the methods of the ID3DXMesh interface to manipulate mesh objects.</span></span>

## <a name="members"></a><span data-ttu-id="a1a22-105">成員</span><span class="sxs-lookup"><span data-stu-id="a1a22-105">Members</span></span>

<span data-ttu-id="a1a22-106">**ID3DXMesh** 介面繼承自 [**ID3DXBaseMesh**](id3dxbasemesh.md)。</span><span class="sxs-lookup"><span data-stu-id="a1a22-106">The **ID3DXMesh** interface inherits from [**ID3DXBaseMesh**](id3dxbasemesh.md).</span></span> <span data-ttu-id="a1a22-107">**ID3DXMesh** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a1a22-107">**ID3DXMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="a1a22-108">方法</span><span class="sxs-lookup"><span data-stu-id="a1a22-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a1a22-109">方法</span><span class="sxs-lookup"><span data-stu-id="a1a22-109">Methods</span></span>

<span data-ttu-id="a1a22-110">**ID3DXMesh** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a1a22-110">The **ID3DXMesh** interface has these methods.</span></span>



| <span data-ttu-id="a1a22-111">方法</span><span class="sxs-lookup"><span data-stu-id="a1a22-111">Method</span></span>                                                            | <span data-ttu-id="a1a22-112">描述</span><span class="sxs-lookup"><span data-stu-id="a1a22-112">Description</span></span>                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1a22-113">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="a1a22-113">**LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)     | <span data-ttu-id="a1a22-114">鎖定包含網格屬性資料的網狀緩衝區，並傳回其指標。</span><span class="sxs-lookup"><span data-stu-id="a1a22-114">Locks the mesh buffer that contains the mesh attribute data, and returns a pointer to it.</span></span><br/>                                   |
| [<span data-ttu-id="a1a22-115">**優化**</span><span class="sxs-lookup"><span data-stu-id="a1a22-115">**Optimize**</span></span>](id3dxmesh--optimize.md)                           | <span data-ttu-id="a1a22-116">產生具有重新排序臉部和頂點的新網格，以將繪製效能優化。</span><span class="sxs-lookup"><span data-stu-id="a1a22-116">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span><br/>                                     |
| [<span data-ttu-id="a1a22-117">**OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="a1a22-117">**OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)             | <span data-ttu-id="a1a22-118">產生具有重新排序臉部和頂點的網格，以將繪製效能優化。</span><span class="sxs-lookup"><span data-stu-id="a1a22-118">Generates a mesh with reordered faces and vertices to optimize drawing performance.</span></span> <span data-ttu-id="a1a22-119">這個方法會重新排序現有的網格。</span><span class="sxs-lookup"><span data-stu-id="a1a22-119">This method reorders the existing mesh.</span></span><br/> |
| [<span data-ttu-id="a1a22-120">**SetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="a1a22-120">**SetAttributeTable**</span></span>](id3dxmesh--setattributetable.md)         | <span data-ttu-id="a1a22-121">設定網格的屬性工作表和儲存在資料表中的專案數目。</span><span class="sxs-lookup"><span data-stu-id="a1a22-121">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span><br/>                                          |
| [<span data-ttu-id="a1a22-122">**UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="a1a22-122">**UnlockAttributeBuffer**</span></span>](id3dxmesh--unlockattributebuffer.md) | <span data-ttu-id="a1a22-123">解除鎖定屬性緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a1a22-123">Unlocks an attribute buffer.</span></span><br/>                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="a1a22-124">備註</span><span class="sxs-lookup"><span data-stu-id="a1a22-124">Remarks</span></span>

<span data-ttu-id="a1a22-125">若要取得 **ID3DXMesh** 介面，請呼叫 [**D3DXCreateMesh**](d3dxcreatemesh.md) 或 [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="a1a22-125">To obtain the **ID3DXMesh** interface, call either the [**D3DXCreateMesh**](d3dxcreatemesh.md) or [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) function.</span></span>

<span data-ttu-id="a1a22-126">這個介面會從 [**ID3DXBaseMesh**](id3dxbasemesh.md) 介面繼承其他功能。</span><span class="sxs-lookup"><span data-stu-id="a1a22-126">This interface inherits additional functionality from the [**ID3DXBaseMesh**](id3dxbasemesh.md) interface.</span></span>

<span data-ttu-id="a1a22-127">LPD3DXMESH 型別定義為 **ID3DXMesh** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="a1a22-127">The LPD3DXMESH type is defined as a pointer to the **ID3DXMesh** interface.</span></span>


```
typedef struct ID3DXMesh *LPD3DXMESH;
```



## <a name="requirements"></a><span data-ttu-id="a1a22-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1a22-128">Requirements</span></span>



| <span data-ttu-id="a1a22-129">需求</span><span class="sxs-lookup"><span data-stu-id="a1a22-129">Requirement</span></span> | <span data-ttu-id="a1a22-130">值</span><span class="sxs-lookup"><span data-stu-id="a1a22-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1a22-131">標頭</span><span class="sxs-lookup"><span data-stu-id="a1a22-131">Header</span></span><br/>  | <dl> <span data-ttu-id="a1a22-132"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1a22-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a1a22-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="a1a22-133">Library</span></span><br/> | <dl> <span data-ttu-id="a1a22-134"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1a22-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a1a22-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1a22-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1a22-136">**ID3DXBaseMesh**</span><span class="sxs-lookup"><span data-stu-id="a1a22-136">**ID3DXBaseMesh**</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="a1a22-137">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="a1a22-137">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a1a22-138">網格函數</span><span class="sxs-lookup"><span data-stu-id="a1a22-138">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




