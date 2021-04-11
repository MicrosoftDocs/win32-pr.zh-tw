---
description: 將相鄰資料新增至網格的索引緩衝區。 當網格要傳送至採用相鄰資料的幾何著色器時，網格的索引緩衝區必須包含相鄰資料。
ms.assetid: 8e587620-a4b6-4415-8fe7-9ec22f253b16
title: 'ID3DX10Mesh：： GenerateGSAdjacency 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateGSAdjacency
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d47747acfa97fbe843dabf527c8f94742db78d6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035386"
---
# <a name="id3dx10meshgenerategsadjacency-method"></a><span data-ttu-id="a2b42-104">ID3DX10Mesh：： GenerateGSAdjacency 方法</span><span class="sxs-lookup"><span data-stu-id="a2b42-104">ID3DX10Mesh::GenerateGSAdjacency method</span></span>

<span data-ttu-id="a2b42-105">將相鄰資料新增至網格的索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a2b42-105">Adds adjacency data to the mesh's index buffer.</span></span> <span data-ttu-id="a2b42-106">當網格要傳送至採用相鄰資料的幾何著色器時，網格的索引緩衝區必須包含相鄰資料。</span><span class="sxs-lookup"><span data-stu-id="a2b42-106">When the mesh is to be sent to a geometry shader that takes adjacency data, it is neccessary for the mesh's index buffer to contain adjacency data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2b42-107">語法</span><span class="sxs-lookup"><span data-stu-id="a2b42-107">Syntax</span></span>


```C++
HRESULT GenerateGSAdjacency();
```



## <a name="parameters"></a><span data-ttu-id="a2b42-108">參數</span><span class="sxs-lookup"><span data-stu-id="a2b42-108">Parameters</span></span>

<span data-ttu-id="a2b42-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a2b42-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2b42-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2b42-110">Return value</span></span>

<span data-ttu-id="a2b42-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a2b42-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a2b42-112">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a2b42-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2b42-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2b42-113">Requirements</span></span>



| <span data-ttu-id="a2b42-114">需求</span><span class="sxs-lookup"><span data-stu-id="a2b42-114">Requirement</span></span> | <span data-ttu-id="a2b42-115">值</span><span class="sxs-lookup"><span data-stu-id="a2b42-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2b42-116">標頭</span><span class="sxs-lookup"><span data-stu-id="a2b42-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a2b42-117"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="a2b42-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2b42-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="a2b42-118">Library</span></span><br/> | <dl> <span data-ttu-id="a2b42-119"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2b42-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2b42-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2b42-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2b42-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="a2b42-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="a2b42-122">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="a2b42-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




