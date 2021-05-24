---
description: 繪製相同網格子集的數個實例。
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: 'ID3DX10Mesh：:D rawSubsetInstanced 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubsetInstanced
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2e28d7a7d2c1d743090832d68793ec3743662308
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335632"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a><span data-ttu-id="4d51e-103">ID3DX10Mesh：:D rawSubsetInstanced 方法</span><span class="sxs-lookup"><span data-stu-id="4d51e-103">ID3DX10Mesh::DrawSubsetInstanced method</span></span>

<span data-ttu-id="4d51e-104">繪製相同網格子集的數個實例。</span><span class="sxs-lookup"><span data-stu-id="4d51e-104">Draw several instances of the same subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d51e-105">語法</span><span class="sxs-lookup"><span data-stu-id="4d51e-105">Syntax</span></span>


```C++
HRESULT DrawSubsetInstanced(
  [in] UINT AttribId,
  [in] UINT InstanceCount,
  [in] UINT StartInstanceLocation
);
```



## <a name="parameters"></a><span data-ttu-id="4d51e-106">參數</span><span class="sxs-lookup"><span data-stu-id="4d51e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d51e-107">*AttribId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d51e-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d51e-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d51e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4d51e-109">指定要繪製的網格子集。</span><span class="sxs-lookup"><span data-stu-id="4d51e-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="4d51e-110">此值可用來區分網格中的臉部，以屬於一或多個屬性群組。</span><span class="sxs-lookup"><span data-stu-id="4d51e-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span> <span data-ttu-id="4d51e-111">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="4d51e-111">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4d51e-112">*InstanceCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d51e-112">*InstanceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d51e-113">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d51e-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4d51e-114">要呈現的實例數目。</span><span class="sxs-lookup"><span data-stu-id="4d51e-114">Number of instances to render.</span></span>

</dd> <dt>

<span data-ttu-id="4d51e-115">*StartInstanceLocation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d51e-115">*StartInstanceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d51e-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d51e-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4d51e-117">要在每個標記為實例資料的緩衝區中開始提取的實例。</span><span class="sxs-lookup"><span data-stu-id="4d51e-117">Which instance to start fetching from in each buffer marked as instance data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d51e-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d51e-118">Return value</span></span>

<span data-ttu-id="4d51e-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4d51e-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4d51e-120">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4d51e-120">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4d51e-121">備註</span><span class="sxs-lookup"><span data-stu-id="4d51e-121">Remarks</span></span>

<span data-ttu-id="4d51e-122">網格包含屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="4d51e-122">A mesh contains an attribute table.</span></span> <span data-ttu-id="4d51e-123">屬性資料表可將網格分割成子集，其中每個子集都以屬性識別碼來識別。</span><span class="sxs-lookup"><span data-stu-id="4d51e-123">The attribute table can divide a mesh into subsets, where each subset is identified with an attribute ID.</span></span> <span data-ttu-id="4d51e-124">例如，具有200臉部的網格（分成三個子集）可能會有如下所示的屬性工作表：</span><span class="sxs-lookup"><span data-stu-id="4d51e-124">For example, a mesh with 200 faces, divided into three subsets, might have an attribute table that looks like this:</span></span>



| <span data-ttu-id="4d51e-125">Subset</span><span class="sxs-lookup"><span data-stu-id="4d51e-125">Subset</span></span>     | <span data-ttu-id="4d51e-126">笑臉</span><span class="sxs-lookup"><span data-stu-id="4d51e-126">Faces</span></span>           |
|------------|-----------------|
| <span data-ttu-id="4d51e-127">AttribID 0</span><span class="sxs-lookup"><span data-stu-id="4d51e-127">AttribID 0</span></span> | <span data-ttu-id="4d51e-128">臉部 0 ~ 50</span><span class="sxs-lookup"><span data-stu-id="4d51e-128">Faces 0 ~ 50</span></span>    |
| <span data-ttu-id="4d51e-129">AttribID 1</span><span class="sxs-lookup"><span data-stu-id="4d51e-129">AttribID 1</span></span> | <span data-ttu-id="4d51e-130">臉部 51 ~ 125</span><span class="sxs-lookup"><span data-stu-id="4d51e-130">Faces 51 ~ 125</span></span>  |
| <span data-ttu-id="4d51e-131">AttribID 2</span><span class="sxs-lookup"><span data-stu-id="4d51e-131">AttribID 2</span></span> | <span data-ttu-id="4d51e-132">臉部 126 ~ 200</span><span class="sxs-lookup"><span data-stu-id="4d51e-132">Faces 126 ~ 200</span></span> |



 

<span data-ttu-id="4d51e-133">實例可能會藉由重複使用相同幾何來在場景中繪製多個物件，來擴充效能。</span><span class="sxs-lookup"><span data-stu-id="4d51e-133">Instancing may extend performance by reusing the same geometry to draw multiple objects in a scene.</span></span> <span data-ttu-id="4d51e-134">實例的其中一個範例，就是使用不同的位置和色彩繪製相同的物件。</span><span class="sxs-lookup"><span data-stu-id="4d51e-134">One example of instancing could be to draw the same object with different positions and colors.</span></span> <span data-ttu-id="4d51e-135">索引編制需要多個頂點緩衝區：每個頂點的資料至少有一個，以及針對每個實例資料使用第二個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4d51e-135">Indexing requires multiple vertex buffers: at least one for per-vertex data and a second buffer for per-instance data.</span></span>

<span data-ttu-id="4d51e-136">使用 DrawSubsetInstanced 的繪圖實例非常類似于 [實例範例](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)中所述的 [**ID3D10Device：:D rawindexedinstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced)所使用的進程。</span><span class="sxs-lookup"><span data-stu-id="4d51e-136">Drawing instances with DrawSubsetInstanced is very similar to the process used with [**ID3D10Device::DrawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) that is outlined in [Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx).</span></span> <span data-ttu-id="4d51e-137">使用 DrawSubsetInstanced 時的主要差異在於，您必須先從 [**ID3DX10Mesh 介面**](id3dx10mesh.md) 物件解壓縮頂點和索引緩衝區，然後才能合併實例資料。</span><span class="sxs-lookup"><span data-stu-id="4d51e-137">The key difference when using DrawSubsetInstanced is that vertex and index buffers must be extracted from the [**ID3DX10Mesh Interface**](id3dx10mesh.md) object before the instancing data can be combined.</span></span>

<span data-ttu-id="4d51e-138">下列程式碼說明如何從網格物件中解壓縮頂點和索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4d51e-138">The following code illustrates extracting the vertex and index buffers from the mesh object.</span></span>


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



## <a name="requirements"></a><span data-ttu-id="4d51e-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d51e-139">Requirements</span></span>



| <span data-ttu-id="4d51e-140">需求</span><span class="sxs-lookup"><span data-stu-id="4d51e-140">Requirement</span></span> | <span data-ttu-id="4d51e-141">值</span><span class="sxs-lookup"><span data-stu-id="4d51e-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d51e-142">標頭</span><span class="sxs-lookup"><span data-stu-id="4d51e-142">Header</span></span><br/>  | <dl> <span data-ttu-id="4d51e-143"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="4d51e-143"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4d51e-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="4d51e-144">Library</span></span><br/> | <dl> <span data-ttu-id="4d51e-145"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d51e-145"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d51e-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d51e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d51e-147">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="4d51e-147">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="4d51e-148">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="4d51e-148">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
