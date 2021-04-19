---
description: 存取網格的相鄰緩衝區。
ms.assetid: 42b13f14-4edf-4b56-9198-60a548855542
title: 'ID3DX10Mesh：： GetAdjacencyBuffer 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAdjacencyBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 80dd5c6e6d9b12cb1c648c42a4758d215d3810c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997408"
---
# <a name="id3dx10meshgetadjacencybuffer-method"></a><span data-ttu-id="2d9d4-103">ID3DX10Mesh：： GetAdjacencyBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="2d9d4-103">ID3DX10Mesh::GetAdjacencyBuffer method</span></span>

<span data-ttu-id="2d9d4-104">存取網格的相鄰緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2d9d4-104">Access the mesh's adjacency buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d9d4-105">語法</span><span class="sxs-lookup"><span data-stu-id="2d9d4-105">Syntax</span></span>


```C++
HRESULT GetAdjacencyBuffer(
  [out] ID3DX10MeshBuffer **ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="2d9d4-106">參數</span><span class="sxs-lookup"><span data-stu-id="2d9d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d9d4-107">*ppAdjacency* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2d9d4-107">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d9d4-108">類型： **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="2d9d4-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="2d9d4-109">鄰接緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2d9d4-109">The adjacency buffer.</span></span> <span data-ttu-id="2d9d4-110">請參閱 [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="2d9d4-110">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d9d4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d9d4-111">Return value</span></span>

<span data-ttu-id="2d9d4-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2d9d4-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2d9d4-113">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2d9d4-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d9d4-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d9d4-114">Requirements</span></span>



| <span data-ttu-id="2d9d4-115">需求</span><span class="sxs-lookup"><span data-stu-id="2d9d4-115">Requirement</span></span> | <span data-ttu-id="2d9d4-116">值</span><span class="sxs-lookup"><span data-stu-id="2d9d4-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d9d4-117">標頭</span><span class="sxs-lookup"><span data-stu-id="2d9d4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2d9d4-118"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="2d9d4-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d9d4-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="2d9d4-119">Library</span></span><br/> | <dl> <span data-ttu-id="2d9d4-120"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d9d4-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d9d4-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d9d4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d9d4-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="2d9d4-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="2d9d4-123">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="2d9d4-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




