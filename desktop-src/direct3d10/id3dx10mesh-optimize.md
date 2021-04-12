---
description: 產生具有重新排序臉部和頂點的新網格，以將繪製效能優化。
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: 'ID3DX10Mesh：： Optimize 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Optimize
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e3c416b28cefe1a3f7fb487567afac4c99057478
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323087"
---
# <a name="id3dx10meshoptimize-method"></a><span data-ttu-id="9556f-103">ID3DX10Mesh：： Optimize 方法</span><span class="sxs-lookup"><span data-stu-id="9556f-103">ID3DX10Mesh::Optimize method</span></span>

<span data-ttu-id="9556f-104">產生具有重新排序臉部和頂點的新網格，以將繪製效能優化。</span><span class="sxs-lookup"><span data-stu-id="9556f-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="9556f-105">語法</span><span class="sxs-lookup"><span data-stu-id="9556f-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="9556f-106">參數</span><span class="sxs-lookup"><span data-stu-id="9556f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9556f-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="9556f-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9556f-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9556f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9556f-109">指定要執行的優化類型。</span><span class="sxs-lookup"><span data-stu-id="9556f-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="9556f-110">這個參數可以設定為 D3DXMESHOPT 和 D3DXMESH (的一或多個旗標的組合，除了 D3DXMESH \_ 32 位、D3DXMESH \_ IB \_ WRITEONLY 和 D3DXMESH \_ WRITEONLY) 之外。</span><span class="sxs-lookup"><span data-stu-id="9556f-110">This parameter can be set to a combination of one or more flags from D3DXMESHOPT and D3DXMESH (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="9556f-111">*pFaceRemap* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9556f-111">*pFaceRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9556f-112">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9556f-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9556f-113">UINTs 的陣列，每個臉部各一個，用來識別對應至優化網格中各臉部的原始網格臉部。</span><span class="sxs-lookup"><span data-stu-id="9556f-113">An array of UINTs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="9556f-114">如果提供給此引數的值為 **Null**，則不會傳回臉部重新對應資料。</span><span class="sxs-lookup"><span data-stu-id="9556f-114">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="9556f-115">*ppVertexRemap* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9556f-115">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9556f-116">類型： **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="9556f-116">Type: **[**LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="9556f-117">[**ID3D10Blob 介面**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)指標的位址，其中包含每個頂點的 DWORD，以指定新頂點如何對應至舊頂點。</span><span class="sxs-lookup"><span data-stu-id="9556f-117">Address of a pointer to an [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="9556f-118">如果您需要根據新的頂點對應來改變外部資料，這個重新對應會很有用。</span><span class="sxs-lookup"><span data-stu-id="9556f-118">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9556f-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="9556f-119">Return value</span></span>

<span data-ttu-id="9556f-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9556f-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9556f-121">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9556f-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9556f-122">備註</span><span class="sxs-lookup"><span data-stu-id="9556f-122">Remarks</span></span>

<span data-ttu-id="9556f-123">這個方法會產生新的網格。</span><span class="sxs-lookup"><span data-stu-id="9556f-123">This method generates a new mesh.</span></span> <span data-ttu-id="9556f-124">執行 Optimize 之前，應用程式必須藉由呼叫 [**ID3DX10Mesh：： GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md)來產生連續的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9556f-124">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DX10Mesh::GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md).</span></span> <span data-ttu-id="9556f-125">鄰接緩衝區包含連續的資料，例如邊緣清單和彼此連續的臉部。</span><span class="sxs-lookup"><span data-stu-id="9556f-125">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="9556f-126">這個方法與 [**ID3DX10Mesh：： CloneMesh**](id3dx10mesh-clonemesh.md) 方法非常類似，不同之處在于它可以在產生新的網格複製時執行優化。</span><span class="sxs-lookup"><span data-stu-id="9556f-126">This method is very similar to the [**ID3DX10Mesh::CloneMesh**](id3dx10mesh-clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="9556f-127">輸出網格會繼承輸入網格的所有建立參數。</span><span class="sxs-lookup"><span data-stu-id="9556f-127">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="9556f-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="9556f-128">Requirements</span></span>



| <span data-ttu-id="9556f-129">需求</span><span class="sxs-lookup"><span data-stu-id="9556f-129">Requirement</span></span> | <span data-ttu-id="9556f-130">值</span><span class="sxs-lookup"><span data-stu-id="9556f-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9556f-131">標頭</span><span class="sxs-lookup"><span data-stu-id="9556f-131">Header</span></span><br/>  | <dl> <span data-ttu-id="9556f-132"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="9556f-132"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="9556f-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="9556f-133">Library</span></span><br/> | <dl> <span data-ttu-id="9556f-134"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9556f-134"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9556f-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9556f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9556f-136">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="9556f-136">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="9556f-137">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="9556f-137">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
