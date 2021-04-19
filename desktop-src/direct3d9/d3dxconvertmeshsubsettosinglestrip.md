---
description: 將指定的網格子集轉換成單一三角形帶狀。
ms.assetid: 618c7bee-dd09-4379-bb8b-30505e809df9
title: 'D3DXConvertMeshSubsetToSingleStrip 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToSingleStrip
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c76aa52b08a21faf9bc2a6ef35745513063cc3b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992305"
---
# <a name="d3dxconvertmeshsubsettosinglestrip-function"></a><span data-ttu-id="07883-103">D3DXConvertMeshSubsetToSingleStrip 函式</span><span class="sxs-lookup"><span data-stu-id="07883-103">D3DXConvertMeshSubsetToSingleStrip function</span></span>

<span data-ttu-id="07883-104">將指定的網格子集轉換成單一三角形帶狀。</span><span class="sxs-lookup"><span data-stu-id="07883-104">Converts the specified mesh subset into a single triangle strip.</span></span>

## <a name="syntax"></a><span data-ttu-id="07883-105">語法</span><span class="sxs-lookup"><span data-stu-id="07883-105">Syntax</span></span>


```C++
HRESULT D3DXConvertMeshSubsetToSingleStrip(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices
);
```



## <a name="parameters"></a><span data-ttu-id="07883-106">參數</span><span class="sxs-lookup"><span data-stu-id="07883-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07883-107">*MeshIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07883-107">*MeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07883-108">類型： **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="07883-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="07883-109">[**ID3DXBaseMesh**](id3dxbasemesh.md)介面的指標，代表要轉換成條紋的網格。</span><span class="sxs-lookup"><span data-stu-id="07883-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to convert to a strip.</span></span>

</dd> <dt>

<span data-ttu-id="07883-110">*AttribId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07883-110">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07883-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07883-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07883-112">要轉換成條紋之網格子集的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="07883-112">Attribute ID of the mesh subset to convert to strips.</span></span>

</dd> <dt>

<span data-ttu-id="07883-113">*IBOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07883-113">*IBOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07883-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07883-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07883-115">結合 [**D3DXMESH**](./d3dxmesh.md) 列舉中的一或多個旗標，指定建立索引緩衝區的選項。</span><span class="sxs-lookup"><span data-stu-id="07883-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for creating the index buffer.</span></span> <span data-ttu-id="07883-116">不可為 D3DXMESH \_ 32 位。</span><span class="sxs-lookup"><span data-stu-id="07883-116">Cannot be D3DXMESH\_32BIT.</span></span> <span data-ttu-id="07883-117">根據 *MeshIn* 參數所指定之網格的索引緩衝區格式，將會使用32位或16位索引來建立索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="07883-117">The index buffer will be created with 32-bit or 16-bit indices, depending on the format of the index buffer of the mesh specified by the *MeshIn* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="07883-118">*ppIndexBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="07883-118">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07883-119">類型： **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="07883-119">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="07883-120">[**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)介面的指標，代表包含該帶的索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="07883-120">Pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer containing the strip.</span></span>

</dd> <dt>

<span data-ttu-id="07883-121">*pNumIndices* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="07883-121">*pNumIndices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07883-122">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="07883-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="07883-123">在 *ppIndexBuffer* 參數中傳回之緩衝區中的索引數目。</span><span class="sxs-lookup"><span data-stu-id="07883-123">Number of indices in the buffer returned in the *ppIndexBuffer* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07883-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="07883-124">Return value</span></span>

<span data-ttu-id="07883-125">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="07883-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="07883-126">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="07883-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="07883-127">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="07883-127">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="07883-128">備註</span><span class="sxs-lookup"><span data-stu-id="07883-128">Remarks</span></span>

<span data-ttu-id="07883-129">在執行此函式之前，請呼叫 [**Optimize**](id3dxmesh--optimize.md) 或 [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)，並 \_ 設定 D3DXMESHOPT ATTRSORT 旗標。</span><span class="sxs-lookup"><span data-stu-id="07883-129">Before running this function, call [**Optimize**](id3dxmesh--optimize.md) or [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), with the D3DXMESHOPT\_ATTRSORT flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="07883-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="07883-130">Requirements</span></span>



| <span data-ttu-id="07883-131">需求</span><span class="sxs-lookup"><span data-stu-id="07883-131">Requirement</span></span> | <span data-ttu-id="07883-132">值</span><span class="sxs-lookup"><span data-stu-id="07883-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07883-133">標頭</span><span class="sxs-lookup"><span data-stu-id="07883-133">Header</span></span><br/>  | <dl> <span data-ttu-id="07883-134"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="07883-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="07883-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="07883-135">Library</span></span><br/> | <dl> <span data-ttu-id="07883-136"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="07883-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="07883-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07883-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07883-138">網格函數</span><span class="sxs-lookup"><span data-stu-id="07883-138">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
