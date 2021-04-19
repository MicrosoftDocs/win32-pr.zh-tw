---
description: 取得網格中的頂點數目。
ms.assetid: fea8a3b5-ca10-4066-b2ca-6579829d31b6
title: 'ID3DX10Mesh：： GetVertexCount 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 189be6ff6872cfb85c2f336c29dedef2e435382e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988609"
---
# <a name="id3dx10meshgetvertexcount-method"></a><span data-ttu-id="66bd2-103">ID3DX10Mesh：： GetVertexCount 方法</span><span class="sxs-lookup"><span data-stu-id="66bd2-103">ID3DX10Mesh::GetVertexCount method</span></span>

<span data-ttu-id="66bd2-104">取得網格中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="66bd2-104">Get the number of vertices in the mesh.</span></span> <span data-ttu-id="66bd2-105">網格可能包含多個頂點緩衝區 (也就是一個頂點緩衝區可能包含所有位置資料、另一個可能包含所有紋理座標資料等 ) ，不過每個頂點緩衝區都包含相同數目的元素。</span><span class="sxs-lookup"><span data-stu-id="66bd2-105">A mesh may contain multiple vertex buffers (i.e. one vertex buffer may contain all position data, another may contains all texture coordinate data, etc.), however each vertex buffer will contain the same number of elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="66bd2-106">語法</span><span class="sxs-lookup"><span data-stu-id="66bd2-106">Syntax</span></span>


```C++
UINT GetVertexCount();
```



## <a name="parameters"></a><span data-ttu-id="66bd2-107">參數</span><span class="sxs-lookup"><span data-stu-id="66bd2-107">Parameters</span></span>

<span data-ttu-id="66bd2-108">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="66bd2-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="66bd2-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="66bd2-109">Return value</span></span>

<span data-ttu-id="66bd2-110">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66bd2-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66bd2-111">網格中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="66bd2-111">The number of vertices in the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="66bd2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="66bd2-112">Requirements</span></span>



| <span data-ttu-id="66bd2-113">需求</span><span class="sxs-lookup"><span data-stu-id="66bd2-113">Requirement</span></span> | <span data-ttu-id="66bd2-114">值</span><span class="sxs-lookup"><span data-stu-id="66bd2-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66bd2-115">標頭</span><span class="sxs-lookup"><span data-stu-id="66bd2-115">Header</span></span><br/>  | <dl> <span data-ttu-id="66bd2-116"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="66bd2-116"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="66bd2-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="66bd2-117">Library</span></span><br/> | <dl> <span data-ttu-id="66bd2-118"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="66bd2-118"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66bd2-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66bd2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66bd2-120">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="66bd2-120">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="66bd2-121">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="66bd2-121">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
