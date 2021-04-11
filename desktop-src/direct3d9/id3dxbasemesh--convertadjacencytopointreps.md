---
description: 將網格相鄰資訊轉換成點代表的陣列。
ms.assetid: b8914f9c-8550-498d-813d-bb1afe0fb5b2
title: 'ID3DXBaseMesh：： ConvertAdjacencyToPointReps 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertAdjacencyToPointReps
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3a4827473cce115f742a85b99732d09a2c5efa4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196233"
---
# <a name="id3dxbasemeshconvertadjacencytopointreps-method"></a><span data-ttu-id="efe10-103">ID3DXBaseMesh：： ConvertAdjacencyToPointReps 方法</span><span class="sxs-lookup"><span data-stu-id="efe10-103">ID3DXBaseMesh::ConvertAdjacencyToPointReps method</span></span>

<span data-ttu-id="efe10-104">將網格相鄰資訊轉換成點代表的陣列。</span><span class="sxs-lookup"><span data-stu-id="efe10-104">Converts mesh adjacency information to an array of point representatives.</span></span>

## <a name="syntax"></a><span data-ttu-id="efe10-105">語法</span><span class="sxs-lookup"><span data-stu-id="efe10-105">Syntax</span></span>


```C++
HRESULT ConvertAdjacencyToPointReps(
  [in]      const DWORD *pAdjacency,
  [in, out]       DWORD *pPRep
);
```



## <a name="parameters"></a><span data-ttu-id="efe10-106">參數</span><span class="sxs-lookup"><span data-stu-id="efe10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efe10-107">*pAdjacency* \[在\]</span><span class="sxs-lookup"><span data-stu-id="efe10-107">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efe10-108">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="efe10-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="efe10-109">指標，指向每個臉部的三個 Dword 陣列，為網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="efe10-109">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="efe10-110">此陣列中的位元組數目必須至少為 3 \* [**ID3DXBaseMesh：： GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD) 。</span><span class="sxs-lookup"><span data-stu-id="efe10-110">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> <dt>

<span data-ttu-id="efe10-111">*pPRep* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="efe10-111">*pPRep* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="efe10-112">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="efe10-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="efe10-113">網格的指標，該陣列將以點代表資料填滿網格的每個頂點的一個 DWORD。</span><span class="sxs-lookup"><span data-stu-id="efe10-113">Pointer to an array of one DWORD per vertex of the mesh that will be filled with point representative data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efe10-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="efe10-114">Return value</span></span>

<span data-ttu-id="efe10-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="efe10-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="efe10-116">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="efe10-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="efe10-117">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="efe10-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="efe10-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="efe10-118">Requirements</span></span>



| <span data-ttu-id="efe10-119">需求</span><span class="sxs-lookup"><span data-stu-id="efe10-119">Requirement</span></span> | <span data-ttu-id="efe10-120">值</span><span class="sxs-lookup"><span data-stu-id="efe10-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="efe10-121">標頭</span><span class="sxs-lookup"><span data-stu-id="efe10-121">Header</span></span><br/>  | <dl> <span data-ttu-id="efe10-122"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="efe10-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="efe10-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="efe10-123">Library</span></span><br/> | <dl> <span data-ttu-id="efe10-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="efe10-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="efe10-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="efe10-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe10-126">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="efe10-126">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
