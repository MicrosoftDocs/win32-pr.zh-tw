---
description: 網狀緩衝區是包含網格相關資料的緩衝區。
ms.assetid: a9fdfa22-531d-4da0-89f0-8766c2635e20
title: 'ID3DX10MeshBuffer 介面 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 42076393c3be5443688ec4db954131935b62f696
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991464"
---
# <a name="id3dx10meshbuffer-interface"></a><span data-ttu-id="cf3ab-103">ID3DX10MeshBuffer 介面</span><span class="sxs-lookup"><span data-stu-id="cf3ab-103">ID3DX10MeshBuffer interface</span></span>

<span data-ttu-id="cf3ab-104">網狀緩衝區是包含網格相關資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cf3ab-104">A mesh buffer is a buffer that contains data about a mesh.</span></span> <span data-ttu-id="cf3ab-105">它可以包含五種不同類型的資料之一：頂點資料、索引資料、相鄰資料、屬性資料或點代表資料。</span><span class="sxs-lookup"><span data-stu-id="cf3ab-105">It can contain one of five different types of data: vertex data, index data, adjacency data, attribute data, or point rep data.</span></span> <span data-ttu-id="cf3ab-106">結構是用來透過下列五個 Api 來存取這五個數據片段： [**ID3DX10Mesh：： GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md)、 [**ID3DX10Mesh：： GetIndexBuffer**](id3dx10mesh-getindexbuffer.md)、 [**ID3DX10Mesh：： GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md)、 [**ID3DX10Mesh：： GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)或 [**ID3DX10Mesh：： GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="cf3ab-106">The structure is used to access these five pieces of data through the following five APIs: [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh::GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh::GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md), or [**ID3DX10Mesh::GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md).</span></span>

## <a name="members"></a><span data-ttu-id="cf3ab-107">成員</span><span class="sxs-lookup"><span data-stu-id="cf3ab-107">Members</span></span>

<span data-ttu-id="cf3ab-108">**ID3DX10MeshBuffer** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="cf3ab-108">The **ID3DX10MeshBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cf3ab-109">**ID3DX10MeshBuffer** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cf3ab-109">**ID3DX10MeshBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="cf3ab-110">方法</span><span class="sxs-lookup"><span data-stu-id="cf3ab-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cf3ab-111">方法</span><span class="sxs-lookup"><span data-stu-id="cf3ab-111">Methods</span></span>

<span data-ttu-id="cf3ab-112">**ID3DX10MeshBuffer** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="cf3ab-112">The **ID3DX10MeshBuffer** interface has these methods.</span></span>



| <span data-ttu-id="cf3ab-113">方法</span><span class="sxs-lookup"><span data-stu-id="cf3ab-113">Method</span></span>                                       | <span data-ttu-id="cf3ab-114">描述</span><span class="sxs-lookup"><span data-stu-id="cf3ab-114">Description</span></span>                                                                |
|:---------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="cf3ab-115">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="cf3ab-115">**GetSize**</span></span>](id3dx10meshbuffer-getsize.md) | <span data-ttu-id="cf3ab-116">取得網狀緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cf3ab-116">Get the size of the mesh buffer, in bytes.</span></span><br/>                      |
| [<span data-ttu-id="cf3ab-117">**對應**</span><span class="sxs-lookup"><span data-stu-id="cf3ab-117">**Map**</span></span>](id3dx10meshbuffer-map.md)         | <span data-ttu-id="cf3ab-118">取得網狀緩衝區記憶體的指標，以修改其內容。</span><span class="sxs-lookup"><span data-stu-id="cf3ab-118">Get a pointer to the mesh buffer memory to modify its contents.</span></span><br/> |
| [<span data-ttu-id="cf3ab-119">**Unmap**</span><span class="sxs-lookup"><span data-stu-id="cf3ab-119">**Unmap**</span></span>](id3dx10meshbuffer-unmap.md)     | <span data-ttu-id="cf3ab-120">取消對應緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cf3ab-120">Unmap a buffer.</span></span><br/>                                                 |



 

## <a name="requirements"></a><span data-ttu-id="cf3ab-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf3ab-121">Requirements</span></span>



| <span data-ttu-id="cf3ab-122">需求</span><span class="sxs-lookup"><span data-stu-id="cf3ab-122">Requirement</span></span> | <span data-ttu-id="cf3ab-123">值</span><span class="sxs-lookup"><span data-stu-id="cf3ab-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf3ab-124">標頭</span><span class="sxs-lookup"><span data-stu-id="cf3ab-124">Header</span></span><br/>  | <dl> <span data-ttu-id="cf3ab-125"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="cf3ab-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf3ab-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="cf3ab-126">Library</span></span><br/> | <dl> <span data-ttu-id="cf3ab-127"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf3ab-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf3ab-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf3ab-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf3ab-129">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="cf3ab-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
