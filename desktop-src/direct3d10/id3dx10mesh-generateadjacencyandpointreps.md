---
description: 產生網格邊緣清單以及共用每個邊緣的臉部清單。
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: 'ID3DX10Mesh：： GenerateAdjacencyAndPointReps 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateAdjacencyAndPointReps
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c46cf83931c95116132798ca971f9d4e61da2af8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514653"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a><span data-ttu-id="3782d-103">ID3DX10Mesh：： GenerateAdjacencyAndPointReps 方法</span><span class="sxs-lookup"><span data-stu-id="3782d-103">ID3DX10Mesh::GenerateAdjacencyAndPointReps method</span></span>

<span data-ttu-id="3782d-104">產生網格邊緣清單以及共用每個邊緣的臉部清單。</span><span class="sxs-lookup"><span data-stu-id="3782d-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="3782d-105">語法</span><span class="sxs-lookup"><span data-stu-id="3782d-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a><span data-ttu-id="3782d-106">參數</span><span class="sxs-lookup"><span data-stu-id="3782d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3782d-107">*Epsilon* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3782d-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3782d-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3782d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3782d-109">指定在位置中差異小於 epsilon 的頂點應視為重合。</span><span class="sxs-lookup"><span data-stu-id="3782d-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3782d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3782d-110">Return value</span></span>

<span data-ttu-id="3782d-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3782d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3782d-112">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3782d-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3782d-113">備註</span><span class="sxs-lookup"><span data-stu-id="3782d-113">Remarks</span></span>

<span data-ttu-id="3782d-114">在應用程式產生網格的相鄰資訊之後，可以將網格資料優化，以提升繪製效能。</span><span class="sxs-lookup"><span data-stu-id="3782d-114">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="3782d-115">相鄰緩衝區中的專案順序是由索引緩衝區中的頂點索引順序所決定。</span><span class="sxs-lookup"><span data-stu-id="3782d-115">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="3782d-116">連續的三角形0一律對應至角落0和1的索引之間的邊緣。</span><span class="sxs-lookup"><span data-stu-id="3782d-116">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="3782d-117">連續的三角形1一律對應至角落1和2的索引之間的邊緣，連續的三角形2則對應至角落2與0的索引之間的邊緣。</span><span class="sxs-lookup"><span data-stu-id="3782d-117">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="3782d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3782d-118">Requirements</span></span>



| <span data-ttu-id="3782d-119">需求</span><span class="sxs-lookup"><span data-stu-id="3782d-119">Requirement</span></span> | <span data-ttu-id="3782d-120">值</span><span class="sxs-lookup"><span data-stu-id="3782d-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3782d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="3782d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3782d-122"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="3782d-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3782d-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="3782d-123">Library</span></span><br/> | <dl> <span data-ttu-id="3782d-124"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3782d-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3782d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3782d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3782d-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="3782d-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="3782d-127">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="3782d-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
