---
description: 將點代表資料轉換為網格相鄰資訊。
ms.assetid: 6ae40486-74be-45a8-9971-f20517c8dcf0
title: 'ID3DXBaseMesh：： ConvertPointRepsToAdjacency 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertPointRepsToAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b1c38d7790d575bdf6794e0e21f1c4043e80257c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974853"
---
# <a name="id3dxbasemeshconvertpointrepstoadjacency-method"></a><span data-ttu-id="96c34-103">ID3DXBaseMesh：： ConvertPointRepsToAdjacency 方法</span><span class="sxs-lookup"><span data-stu-id="96c34-103">ID3DXBaseMesh::ConvertPointRepsToAdjacency method</span></span>

<span data-ttu-id="96c34-104">將點代表資料轉換為網格相鄰資訊。</span><span class="sxs-lookup"><span data-stu-id="96c34-104">Converts point representative data to mesh adjacency information.</span></span>

## <a name="syntax"></a><span data-ttu-id="96c34-105">語法</span><span class="sxs-lookup"><span data-stu-id="96c34-105">Syntax</span></span>


```C++
HRESULT ConvertPointRepsToAdjacency(
  [in]      const DWORD *pPRep,
  [in, out]       DWORD *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="96c34-106">參數</span><span class="sxs-lookup"><span data-stu-id="96c34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96c34-107">*pPRep* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96c34-107">*pPRep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96c34-108">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="96c34-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="96c34-109">包含點代表資料之網格的每個頂點的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="96c34-109">Pointer to an array of one DWORD per vertex of the mesh that contains point representative data.</span></span> <span data-ttu-id="96c34-110">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="96c34-110">This parameter is optional.</span></span> <span data-ttu-id="96c34-111">提供 **Null** 值將會使此參數解讀為 "identity" 陣列。</span><span class="sxs-lookup"><span data-stu-id="96c34-111">Supplying a **NULL** value will cause this parameter to be interpreted as an "identity" array.</span></span>

</dd> <dt>

<span data-ttu-id="96c34-112">*pAdjacency* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="96c34-112">*pAdjacency* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="96c34-113">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="96c34-113">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="96c34-114">指標，指向每個臉部的三個 Dword 陣列，為網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="96c34-114">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="96c34-115">此陣列中的位元組數目必須至少為 3 \* [**ID3DXBaseMesh：： GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD) 。</span><span class="sxs-lookup"><span data-stu-id="96c34-115">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96c34-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="96c34-116">Return value</span></span>

<span data-ttu-id="96c34-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="96c34-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="96c34-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="96c34-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="96c34-119">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="96c34-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="96c34-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="96c34-120">Requirements</span></span>



| <span data-ttu-id="96c34-121">需求</span><span class="sxs-lookup"><span data-stu-id="96c34-121">Requirement</span></span> | <span data-ttu-id="96c34-122">值</span><span class="sxs-lookup"><span data-stu-id="96c34-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96c34-123">標頭</span><span class="sxs-lookup"><span data-stu-id="96c34-123">Header</span></span><br/>  | <dl> <span data-ttu-id="96c34-124"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="96c34-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="96c34-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="96c34-125">Library</span></span><br/> | <dl> <span data-ttu-id="96c34-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="96c34-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="96c34-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96c34-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c34-128">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="96c34-128">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
