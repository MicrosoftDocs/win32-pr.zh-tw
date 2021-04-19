---
description: 使用宣告子建立網格物件。
ms.assetid: 50e09378-2935-4b18-8fc9-5e58eaadae44
title: 'D3DX10CreateMesh 函式 (D3DX10Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateMesh
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2b00addb152fe18db448364fcc784c2044b10d23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992736"
---
# <a name="d3dx10createmesh-function"></a><span data-ttu-id="18140-103">D3DX10CreateMesh 函式</span><span class="sxs-lookup"><span data-stu-id="18140-103">D3DX10CreateMesh function</span></span>

<span data-ttu-id="18140-104">使用宣告子建立網格物件。</span><span class="sxs-lookup"><span data-stu-id="18140-104">Creates a mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="18140-105">語法</span><span class="sxs-lookup"><span data-stu-id="18140-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateMesh(
  _In_        ID3D10Device             *pDevice,
  _In_  const D3D10_INPUT_ELEMENT_DESC *pDeclaration,
  _In_        UINT                     DeclCount,
  _In_        LPCSTR                   pPositionSemantic,
  _In_        UINT                     VertexCount,
  _In_        UINT                     FaceCount,
  _In_        UINT                     Options,
  _Out_       ID3DX10Mesh              **ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="18140-106">參數</span><span class="sxs-lookup"><span data-stu-id="18140-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18140-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18140-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18140-108">類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="18140-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="18140-109">[**ID3D10Device 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)的指標，也就是要與網格相關聯的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="18140-109">Pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="18140-110">*pDeclaration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18140-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18140-111">Type： **Const [**D3D10 \_ INPUT \_ ELEMENT \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***</span><span class="sxs-lookup"><span data-stu-id="18140-111">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\***</span></span>

<span data-ttu-id="18140-112">[**D3D10 \_ 輸入 \_ 元素 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)元素的陣列，描述傳回之網格的頂點格式。</span><span class="sxs-lookup"><span data-stu-id="18140-112">Array of [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) elements, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="18140-113">此參數必須直接對應至彈性頂點格式， (FVF) 。</span><span class="sxs-lookup"><span data-stu-id="18140-113">This parameter must map directly to a flexible vertex format (FVF).</span></span>

</dd> <dt>

<span data-ttu-id="18140-114">*DeclCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18140-114">*DeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18140-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18140-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18140-116">PDeclaration 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="18140-116">The number of elements in pDeclaration.</span></span>

</dd> <dt>

<span data-ttu-id="18140-117">*pPositionSemantic* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18140-117">*pPositionSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18140-118">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18140-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18140-119">識別頂點宣告中哪個部分包含位置資訊的語法。</span><span class="sxs-lookup"><span data-stu-id="18140-119">Semantic that identifies which part of the vertex declaration contains position information.</span></span>

</dd> <dt>

<span data-ttu-id="18140-120">*VertexCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18140-120">*VertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18140-121">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18140-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18140-122">網格的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="18140-122">Number of vertices for the mesh.</span></span> <span data-ttu-id="18140-123">此參數必須大於0。</span><span class="sxs-lookup"><span data-stu-id="18140-123">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="18140-124">*FaceCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18140-124">*FaceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18140-125">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18140-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18140-126">網格的臉部數目。</span><span class="sxs-lookup"><span data-stu-id="18140-126">Number of faces for the mesh.</span></span> <span data-ttu-id="18140-127">此數位的有效範圍大於0，而一個小於最大 DWORD (通常是 65534) ，因為會保留最後一個索引。</span><span class="sxs-lookup"><span data-stu-id="18140-127">The valid range for this number is greater than 0, and one less than the maximum DWORD (typically 65534), because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="18140-128">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18140-128">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18140-129">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18140-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18140-130">[**D3DX10 \_ 網格**](d3dx10-mesh.md)中一或多個旗標的組合，指定網格的選項。</span><span class="sxs-lookup"><span data-stu-id="18140-130">Combination of one or more flags from the [**D3DX10\_MESH**](d3dx10-mesh.md), specifying options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="18140-131">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="18140-131">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18140-132">類型： **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="18140-132">Type: **[**ID3DX10Mesh**](id3dx10mesh.md)\*\***</span></span>

<span data-ttu-id="18140-133">[**ID3DX10Mesh 介面**](id3dx10mesh.md)指標的位址，表示所建立的網格物件。</span><span class="sxs-lookup"><span data-stu-id="18140-133">Address of a pointer to an [**ID3DX10Mesh Interface**](id3dx10mesh.md), representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18140-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="18140-134">Return value</span></span>

<span data-ttu-id="18140-135">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="18140-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="18140-136">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="18140-136">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="18140-137">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="18140-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="18140-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="18140-138">Requirements</span></span>



| <span data-ttu-id="18140-139">需求</span><span class="sxs-lookup"><span data-stu-id="18140-139">Requirement</span></span> | <span data-ttu-id="18140-140">值</span><span class="sxs-lookup"><span data-stu-id="18140-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18140-141">標頭</span><span class="sxs-lookup"><span data-stu-id="18140-141">Header</span></span><br/>  | <dl> <span data-ttu-id="18140-142"><dt>D3DX10Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="18140-142"><dt>D3DX10Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="18140-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="18140-143">Library</span></span><br/> | <dl> <span data-ttu-id="18140-144"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="18140-144"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="18140-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18140-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18140-146">網格函數</span><span class="sxs-lookup"><span data-stu-id="18140-146">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="18140-147">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="18140-147">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
