---
description: 此介面會封裝修補程式網格功能。
ms.assetid: c70c0fe0-b695-4ad9-b0c6-7854cf8f7593
title: 'ID3DXPatchMesh 介面 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1f13e6abe3a164e8027ddcb6bb33e9f0ca618fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323060"
---
# <a name="id3dxpatchmesh-interface"></a><span data-ttu-id="84a08-103">ID3DXPatchMesh 介面</span><span class="sxs-lookup"><span data-stu-id="84a08-103">ID3DXPatchMesh interface</span></span>

<span data-ttu-id="84a08-104">此介面會封裝修補程式網格功能。</span><span class="sxs-lookup"><span data-stu-id="84a08-104">This interface encapsulates patch mesh functionality.</span></span>

## <a name="members"></a><span data-ttu-id="84a08-105">成員</span><span class="sxs-lookup"><span data-stu-id="84a08-105">Members</span></span>

<span data-ttu-id="84a08-106">**ID3DXPatchMesh** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="84a08-106">The **ID3DXPatchMesh** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="84a08-107">**ID3DXPatchMesh** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="84a08-107">**ID3DXPatchMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="84a08-108">方法</span><span class="sxs-lookup"><span data-stu-id="84a08-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="84a08-109">方法</span><span class="sxs-lookup"><span data-stu-id="84a08-109">Methods</span></span>

<span data-ttu-id="84a08-110">**ID3DXPatchMesh** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="84a08-110">The **ID3DXPatchMesh** interface has these methods.</span></span>



| <span data-ttu-id="84a08-111">方法</span><span class="sxs-lookup"><span data-stu-id="84a08-111">Method</span></span>                                                                           | <span data-ttu-id="84a08-112">描述</span><span class="sxs-lookup"><span data-stu-id="84a08-112">Description</span></span>                                                                                     |
|:---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84a08-113">**CloneMesh**</span><span class="sxs-lookup"><span data-stu-id="84a08-113">**CloneMesh**</span></span>](id3dxpatchmesh--clonemesh.md)                                   | <span data-ttu-id="84a08-114">使用指定的頂點宣告來建立新的 patch 網狀。</span><span class="sxs-lookup"><span data-stu-id="84a08-114">Creates a new patch mesh with the specified vertex declaration.</span></span><br/>                      |
| [<span data-ttu-id="84a08-115">**GenerateAdjacency**</span><span class="sxs-lookup"><span data-stu-id="84a08-115">**GenerateAdjacency**</span></span>](id3dxpatchmesh--generateadjacency.md)                   | <span data-ttu-id="84a08-116">產生網格邊緣清單以及共用每個邊緣的修補程式。</span><span class="sxs-lookup"><span data-stu-id="84a08-116">Generate a list of mesh edges and the patches that share each edge.</span></span><br/>                  |
| [<span data-ttu-id="84a08-117">**GetControlVerticesPerPatch**</span><span class="sxs-lookup"><span data-stu-id="84a08-117">**GetControlVerticesPerPatch**</span></span>](id3dxpatchmesh--getcontrolverticesperpatch.md) | <span data-ttu-id="84a08-118">取得每個修補程式的控制頂點數目。</span><span class="sxs-lookup"><span data-stu-id="84a08-118">Gets the number of control vertices per patch.</span></span><br/>                                       |
| [<span data-ttu-id="84a08-119">**GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="84a08-119">**GetDeclaration**</span></span>](id3dxpatchmesh--getdeclaration.md)                         | <span data-ttu-id="84a08-120">取得頂點宣告。</span><span class="sxs-lookup"><span data-stu-id="84a08-120">Gets the vertex declaration.</span></span><br/>                                                         |
| [<span data-ttu-id="84a08-121">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="84a08-121">**GetDevice**</span></span>](id3dxpatchmesh--getdevice.md)                                   | <span data-ttu-id="84a08-122">取得建立網格的裝置。</span><span class="sxs-lookup"><span data-stu-id="84a08-122">Gets the device that created the mesh.</span></span><br/>                                               |
| [<span data-ttu-id="84a08-123">**GetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="84a08-123">**GetDisplaceParam**</span></span>](id3dxpatchmesh--getdisplaceparam.md)                     | <span data-ttu-id="84a08-124">取得網狀幾何置換參數。</span><span class="sxs-lookup"><span data-stu-id="84a08-124">Gets mesh geometry displacement parameters.</span></span><br/>                                          |
| [<span data-ttu-id="84a08-125">**GetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="84a08-125">**GetIndexBuffer**</span></span>](id3dxpatchmesh--getindexbuffer.md)                         | <span data-ttu-id="84a08-126">取得網狀索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="84a08-126">Gets the mesh index buffer.</span></span><br/>                                                          |
| [<span data-ttu-id="84a08-127">**GetNumPatches**</span><span class="sxs-lookup"><span data-stu-id="84a08-127">**GetNumPatches**</span></span>](id3dxpatchmesh--getnumpatches.md)                           | <span data-ttu-id="84a08-128">取得網格中的修補程式數目。</span><span class="sxs-lookup"><span data-stu-id="84a08-128">Gets the number of patches in the mesh.</span></span><br/>                                              |
| [<span data-ttu-id="84a08-129">**GetNumVertices**</span><span class="sxs-lookup"><span data-stu-id="84a08-129">**GetNumVertices**</span></span>](id3dxpatchmesh--getnumvertices.md)                         | <span data-ttu-id="84a08-130">取得網格中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="84a08-130">Gets the number of vertices in the mesh.</span></span><br/>                                             |
| [<span data-ttu-id="84a08-131">**GetOptions**</span><span class="sxs-lookup"><span data-stu-id="84a08-131">**GetOptions**</span></span>](id3dxpatchmesh--getoptions.md)                                 | <span data-ttu-id="84a08-132">取得修補程式的類型。</span><span class="sxs-lookup"><span data-stu-id="84a08-132">Gets the type of patch.</span></span><br/>                                                              |
| [<span data-ttu-id="84a08-133">**GetPatchInfo**</span><span class="sxs-lookup"><span data-stu-id="84a08-133">**GetPatchInfo**</span></span>](id3dxpatchmesh--getpatchinfo.md)                             | <span data-ttu-id="84a08-134">取得修補程式的屬性。</span><span class="sxs-lookup"><span data-stu-id="84a08-134">Gets the attributes of the patch.</span></span><br/>                                                    |
| [<span data-ttu-id="84a08-135">**GetTessSize**</span><span class="sxs-lookup"><span data-stu-id="84a08-135">**GetTessSize**</span></span>](id3dxpatchmesh--gettesssize.md)                               | <span data-ttu-id="84a08-136">取得鑲嵌層級的鑲嵌網格大小。</span><span class="sxs-lookup"><span data-stu-id="84a08-136">Gets the size of the tessellated mesh, given a tessellation level.</span></span><br/>                   |
| [<span data-ttu-id="84a08-137">**GetVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="84a08-137">**GetVertexBuffer**</span></span>](id3dxpatchmesh--getvertexbuffer.md)                       | <span data-ttu-id="84a08-138">取得網格頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="84a08-138">Gets the mesh vertex buffer.</span></span><br/>                                                         |
| [<span data-ttu-id="84a08-139">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="84a08-139">**LockAttributeBuffer**</span></span>](id3dxpatchmesh--lockattributebuffer.md)               | <span data-ttu-id="84a08-140">鎖定屬性緩衝區。</span><span class="sxs-lookup"><span data-stu-id="84a08-140">Locks the attribute buffer.</span></span><br/>                                                          |
| [<span data-ttu-id="84a08-141">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="84a08-141">**LockIndexBuffer**</span></span>](id3dxpatchmesh--lockindexbuffer.md)                       | <span data-ttu-id="84a08-142">鎖定索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="84a08-142">Lock the index buffer.</span></span><br/>                                                               |
| [<span data-ttu-id="84a08-143">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="84a08-143">**LockVertexBuffer**</span></span>](id3dxpatchmesh--lockvertexbuffer.md)                     | <span data-ttu-id="84a08-144">鎖定頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="84a08-144">Lock the vertex buffer.</span></span><br/>                                                              |
| [<span data-ttu-id="84a08-145">**優化**</span><span class="sxs-lookup"><span data-stu-id="84a08-145">**Optimize**</span></span>](id3dxpatchmesh--optimize.md)                                     | <span data-ttu-id="84a08-146">將修補程式網格優化以進行有效率的鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="84a08-146">Optimizes the patch mesh for efficient tessellation.</span></span><br/>                                 |
| [<span data-ttu-id="84a08-147">**SetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="84a08-147">**SetDisplaceParam**</span></span>](id3dxpatchmesh--setdisplaceparam.md)                     | <span data-ttu-id="84a08-148">設定網狀幾何置換參數。</span><span class="sxs-lookup"><span data-stu-id="84a08-148">Sets mesh geometry displacement parameters.</span></span><br/>                                          |
| [<span data-ttu-id="84a08-149">**Tessellate**</span><span class="sxs-lookup"><span data-stu-id="84a08-149">**Tessellate**</span></span>](id3dxpatchmesh--tessellate.md)                                 | <span data-ttu-id="84a08-150">根據鑲嵌式層級執行統一鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="84a08-150">Performs uniform tessellation based on the tessellation level.</span></span><br/>                       |
| [<span data-ttu-id="84a08-151">**TessellateAdaptive**</span><span class="sxs-lookup"><span data-stu-id="84a08-151">**TessellateAdaptive**</span></span>](id3dxpatchmesh--tessellateadaptive.md)                 | <span data-ttu-id="84a08-152">根據以 z 為基礎的調適型鑲嵌準則，執行適應性鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="84a08-152">Performs adaptive tessellation based on the z-based adaptive tessellation criterion.</span></span><br/> |
| [<span data-ttu-id="84a08-153">**UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="84a08-153">**UnlockAttributeBuffer**</span></span>](id3dxpatchmesh--unlockattributebuffer.md)           | <span data-ttu-id="84a08-154">解除鎖定屬性緩衝區。</span><span class="sxs-lookup"><span data-stu-id="84a08-154">Unlock the attribute buffer.</span></span><br/>                                                         |
| [<span data-ttu-id="84a08-155">**UnlockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="84a08-155">**UnlockIndexBuffer**</span></span>](id3dxpatchmesh--unlockindexbuffer.md)                   | <span data-ttu-id="84a08-156">解除鎖定索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="84a08-156">Unlock the index buffer.</span></span><br/>                                                             |
| [<span data-ttu-id="84a08-157">**UnlockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="84a08-157">**UnlockVertexBuffer**</span></span>](id3dxpatchmesh--unlockvertexbuffer.md)                 | <span data-ttu-id="84a08-158">解除鎖定頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="84a08-158">Unlock the vertex buffer.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="84a08-159">備註</span><span class="sxs-lookup"><span data-stu-id="84a08-159">Remarks</span></span>

<span data-ttu-id="84a08-160">Patch 網格是由一連串修補程式所組成的網格。</span><span class="sxs-lookup"><span data-stu-id="84a08-160">A patch mesh is a mesh that consists of a series of patches.</span></span>

<span data-ttu-id="84a08-161">若要取得 **ID3DXPatchMesh** 介面，請呼叫 [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="84a08-161">To obtain the **ID3DXPatchMesh** interface, call the [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) function.</span></span>

<span data-ttu-id="84a08-162">LPD3DXPATCHMESH 型別定義為 **ID3DXPatchMesh** 介面的指標，如下所示：</span><span class="sxs-lookup"><span data-stu-id="84a08-162">The LPD3DXPATCHMESH type is defined as a pointer to the **ID3DXPatchMesh** interface, as follows:</span></span>


```
typedef struct ID3DXPatchMesh *LPD3DXPATCHMESH;
```



## <a name="requirements"></a><span data-ttu-id="84a08-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="84a08-163">Requirements</span></span>



| <span data-ttu-id="84a08-164">需求</span><span class="sxs-lookup"><span data-stu-id="84a08-164">Requirement</span></span> | <span data-ttu-id="84a08-165">值</span><span class="sxs-lookup"><span data-stu-id="84a08-165">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84a08-166">標頭</span><span class="sxs-lookup"><span data-stu-id="84a08-166">Header</span></span><br/>  | <dl> <span data-ttu-id="84a08-167"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="84a08-167"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="84a08-168">程式庫</span><span class="sxs-lookup"><span data-stu-id="84a08-168">Library</span></span><br/> | <dl> <span data-ttu-id="84a08-169"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="84a08-169"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="84a08-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84a08-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84a08-171">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="84a08-171">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="84a08-172">網格函數</span><span class="sxs-lookup"><span data-stu-id="84a08-172">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
