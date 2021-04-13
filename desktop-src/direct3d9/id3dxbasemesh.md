---
description: 應用程式會使用 ID3DXBaseMesh 介面的方法來操作和查詢網格和漸進式網格物件。
ms.assetid: ec4ccd77-e370-470c-9325-3d794a8f7f16
title: 'ID3DXBaseMesh 介面 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58029639852b30f5de357bb2643583615c45485c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322988"
---
# <a name="id3dxbasemesh-interface"></a><span data-ttu-id="e911f-103">ID3DXBaseMesh 介面</span><span class="sxs-lookup"><span data-stu-id="e911f-103">ID3DXBaseMesh interface</span></span>

<span data-ttu-id="e911f-104">應用程式會使用 **ID3DXBaseMesh** 介面的方法來操作和查詢網格和漸進式網格物件。</span><span class="sxs-lookup"><span data-stu-id="e911f-104">Applications use the methods of the **ID3DXBaseMesh** interface to manipulate and query mesh and progressive mesh objects.</span></span>

## <a name="members"></a><span data-ttu-id="e911f-105">成員</span><span class="sxs-lookup"><span data-stu-id="e911f-105">Members</span></span>

<span data-ttu-id="e911f-106">**ID3DXBaseMesh** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="e911f-106">The **ID3DXBaseMesh** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e911f-107">**ID3DXBaseMesh** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e911f-107">**ID3DXBaseMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="e911f-108">方法</span><span class="sxs-lookup"><span data-stu-id="e911f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e911f-109">方法</span><span class="sxs-lookup"><span data-stu-id="e911f-109">Methods</span></span>

<span data-ttu-id="e911f-110">**ID3DXBaseMesh** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e911f-110">The **ID3DXBaseMesh** interface has these methods.</span></span>



| <span data-ttu-id="e911f-111">方法</span><span class="sxs-lookup"><span data-stu-id="e911f-111">Method</span></span>                                                                            | <span data-ttu-id="e911f-112">描述</span><span class="sxs-lookup"><span data-stu-id="e911f-112">Description</span></span>                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e911f-113">**CloneMesh**</span><span class="sxs-lookup"><span data-stu-id="e911f-113">**CloneMesh**</span></span>](id3dxbasemesh--clonemesh.md)                                     | <span data-ttu-id="e911f-114">使用宣告子複製網格。</span><span class="sxs-lookup"><span data-stu-id="e911f-114">Clones a mesh using a declarator.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="e911f-115">**CloneMeshFVF**</span><span class="sxs-lookup"><span data-stu-id="e911f-115">**CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)                               | <span data-ttu-id="e911f-116">使用彈性頂點格式來複製網格 (FVF) 程式碼。</span><span class="sxs-lookup"><span data-stu-id="e911f-116">Clones a mesh using a flexible vertex format (FVF) code.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="e911f-117">**ConvertAdjacencyToPointReps**</span><span class="sxs-lookup"><span data-stu-id="e911f-117">**ConvertAdjacencyToPointReps**</span></span>](id3dxbasemesh--convertadjacencytopointreps.md) | <span data-ttu-id="e911f-118">將網格相鄰資訊轉換成點代表的陣列。</span><span class="sxs-lookup"><span data-stu-id="e911f-118">Converts mesh adjacency information to an array of point representatives.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="e911f-119">**ConvertPointRepsToAdjacency**</span><span class="sxs-lookup"><span data-stu-id="e911f-119">**ConvertPointRepsToAdjacency**</span></span>](id3dxbasemesh--convertpointrepstoadjacency.md) | <span data-ttu-id="e911f-120">將點代表資料轉換為網格相鄰資訊。</span><span class="sxs-lookup"><span data-stu-id="e911f-120">Converts point representative data to mesh adjacency information.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="e911f-121">**DrawSubset**</span><span class="sxs-lookup"><span data-stu-id="e911f-121">**DrawSubset**</span></span>](id3dxbasemesh--drawsubset.md)                                   | <span data-ttu-id="e911f-122">繪製網格的子集。</span><span class="sxs-lookup"><span data-stu-id="e911f-122">Draws a subset of a mesh.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="e911f-123">**GenerateAdjacency**</span><span class="sxs-lookup"><span data-stu-id="e911f-123">**GenerateAdjacency**</span></span>](id3dxbasemesh--generateadjacency.md)                     | <span data-ttu-id="e911f-124">產生網格邊緣清單以及共用每個邊緣的臉部清單。</span><span class="sxs-lookup"><span data-stu-id="e911f-124">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="e911f-125">**GetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="e911f-125">**GetAttributeTable**</span></span>](id3dxbasemesh--getattributetable.md)                     | <span data-ttu-id="e911f-126">抓取網格的屬性工作表，或網格的屬性資料表中儲存的專案數。</span><span class="sxs-lookup"><span data-stu-id="e911f-126">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span><br/>                                                                                          |
| [<span data-ttu-id="e911f-127">**GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="e911f-127">**GetDeclaration**</span></span>](id3dxbasemesh--getdeclaration.md)                           | <span data-ttu-id="e911f-128">捕獲描述網格中頂點的宣告。</span><span class="sxs-lookup"><span data-stu-id="e911f-128">Retrieves a declaration describing the vertices in the mesh.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="e911f-129">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="e911f-129">**GetDevice**</span></span>](id3dxbasemesh--getdevice.md)                                     | <span data-ttu-id="e911f-130">捕獲與網格相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="e911f-130">Retrieves the device associated with the mesh.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="e911f-131">**GetFVF**</span><span class="sxs-lookup"><span data-stu-id="e911f-131">**GetFVF**</span></span>](id3dxbasemesh--getfvf.md)                                           | <span data-ttu-id="e911f-132">取得固定的函式頂點值。</span><span class="sxs-lookup"><span data-stu-id="e911f-132">Gets the fixed function vertex value.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="e911f-133">**GetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="e911f-133">**GetIndexBuffer**</span></span>](id3dxbasemesh--getindexbuffer.md)                           | <span data-ttu-id="e911f-134">抓取索引緩衝區中的資料。</span><span class="sxs-lookup"><span data-stu-id="e911f-134">Retrieves the data in an index buffer.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="e911f-135">**GetNumBytesPerVertex**</span><span class="sxs-lookup"><span data-stu-id="e911f-135">**GetNumBytesPerVertex**</span></span>](id3dxbasemesh--getnumbytespervertex.md)               | <span data-ttu-id="e911f-136">取得每個頂點的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e911f-136">Gets the number of bytes per vertex.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="e911f-137">**GetNumFaces**</span><span class="sxs-lookup"><span data-stu-id="e911f-137">**GetNumFaces**</span></span>](id3dxbasemesh--getnumfaces.md)                                 | <span data-ttu-id="e911f-138">抓取網格中的臉部數目。</span><span class="sxs-lookup"><span data-stu-id="e911f-138">Retrieves the number of faces in the mesh.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="e911f-139">**GetNumVertices**</span><span class="sxs-lookup"><span data-stu-id="e911f-139">**GetNumVertices**</span></span>](id3dxbasemesh--getnumvertices.md)                           | <span data-ttu-id="e911f-140">抓取網格中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="e911f-140">Retrieves the number of vertices in the mesh.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="e911f-141">**GetOptions**</span><span class="sxs-lookup"><span data-stu-id="e911f-141">**GetOptions**</span></span>](id3dxbasemesh--getoptions.md)                                   | <span data-ttu-id="e911f-142">抓取在建立時為此網格啟用的網格選項。</span><span class="sxs-lookup"><span data-stu-id="e911f-142">Retrieves the mesh options enabled for this mesh at creation time.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="e911f-143">**GetVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="e911f-143">**GetVertexBuffer**</span></span>](id3dxbasemesh--getvertexbuffer.md)                         | <span data-ttu-id="e911f-144">抓取與網格相關聯的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e911f-144">Retrieves the vertex buffer associated with the mesh.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="e911f-145">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="e911f-145">**LockIndexBuffer**</span></span>](id3dxbasemesh--lockindexbuffer.md)                         | <span data-ttu-id="e911f-146">鎖定索引緩衝區，並取得索引緩衝區記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="e911f-146">Locks an index buffer and obtains a pointer to the index buffer memory.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="e911f-147">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="e911f-147">**LockVertexBuffer**</span></span>](id3dxbasemesh--lockvertexbuffer.md)                       | <span data-ttu-id="e911f-148">鎖定頂點緩衝區，並取得頂點緩衝區記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="e911f-148">Locks a vertex buffer and obtains a pointer to the vertex buffer memory.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="e911f-149">**UnlockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="e911f-149">**UnlockIndexBuffer**</span></span>](id3dxbasemesh--unlockindexbuffer.md)                     | <span data-ttu-id="e911f-150">解除鎖定索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e911f-150">Unlocks an index buffer.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="e911f-151">**UnlockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="e911f-151">**UnlockVertexBuffer**</span></span>](id3dxbasemesh--unlockvertexbuffer.md)                   | <span data-ttu-id="e911f-152">解除鎖定頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e911f-152">Unlocks a vertex buffer.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="e911f-153">**UpdateSemantics**</span><span class="sxs-lookup"><span data-stu-id="e911f-153">**UpdateSemantics**</span></span>](id3dxbasemesh--updatesemantics.md)                         | <span data-ttu-id="e911f-154">這種方法可讓使用者變更網格宣告，而不需要變更頂點緩衝區的資料版面配置。</span><span class="sxs-lookup"><span data-stu-id="e911f-154">This method allows the user to change the mesh declaration without changing the data layout of the vertex buffer.</span></span> <span data-ttu-id="e911f-155">只有當舊的和新的宣告格式具有相同的頂點大小時，呼叫才會有效。</span><span class="sxs-lookup"><span data-stu-id="e911f-155">The call is valid only if the old and new declaration formats have the same vertex size.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e911f-156">備註</span><span class="sxs-lookup"><span data-stu-id="e911f-156">Remarks</span></span>

<span data-ttu-id="e911f-157">網格是由一組多邊形臉部所組成的物件。</span><span class="sxs-lookup"><span data-stu-id="e911f-157">A mesh is an object made up of a set of polygonal faces.</span></span> <span data-ttu-id="e911f-158">網格會定義一組頂點和一組臉部 (臉部是根據網格) 的頂點和法線來定義。</span><span class="sxs-lookup"><span data-stu-id="e911f-158">A mesh defines a set of vertices and a set of faces (the faces are defined in terms of the vertices and normals of the mesh).</span></span>

<span data-ttu-id="e911f-159">LPD3DXBASEMESH 型別定義為 **ID3DXBaseMesh** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e911f-159">The LPD3DXBASEMESH type is defined as a pointer to the **ID3DXBaseMesh** interface.</span></span>


```
typedef struct ID3DXBaseMesh *LPD3DXBASEMESH;
```



## <a name="requirements"></a><span data-ttu-id="e911f-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="e911f-160">Requirements</span></span>



| <span data-ttu-id="e911f-161">需求</span><span class="sxs-lookup"><span data-stu-id="e911f-161">Requirement</span></span> | <span data-ttu-id="e911f-162">值</span><span class="sxs-lookup"><span data-stu-id="e911f-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e911f-163">標頭</span><span class="sxs-lookup"><span data-stu-id="e911f-163">Header</span></span><br/>  | <dl> <span data-ttu-id="e911f-164"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="e911f-164"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e911f-165">程式庫</span><span class="sxs-lookup"><span data-stu-id="e911f-165">Library</span></span><br/> | <dl> <span data-ttu-id="e911f-166"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e911f-166"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e911f-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e911f-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e911f-168">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="e911f-168">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
