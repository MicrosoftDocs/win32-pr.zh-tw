---
description: 指定要從裝置捨棄哪些網格資料片段。 搭配 ID3DX10Mesh 使用：:D iscard。
ms.assetid: 8b3c22ab-1337-4a66-ae32-17bd1b73f624
title: 'D3DX10_MESH_DISCARD_FLAGS 列舉 (D3DX10Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH_DISCARD_FLAGS
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 6640834cf81bfa5e4b6263d3b3cfbb1181bb16c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946206"
---
# <a name="d3dx10_mesh_discard_flags-enumeration"></a><span data-ttu-id="f464d-104">D3DX10 \_ 網格 \_ 捨棄 \_ 旗標列舉</span><span class="sxs-lookup"><span data-stu-id="f464d-104">D3DX10\_MESH\_DISCARD\_FLAGS enumeration</span></span>

<span data-ttu-id="f464d-105">指定要從裝置捨棄哪些網格資料片段。</span><span class="sxs-lookup"><span data-stu-id="f464d-105">Specifies which pieces of mesh data to discard from the device.</span></span> <span data-ttu-id="f464d-106">搭配 [**ID3DX10Mesh 使用：:D iscard**](id3dx10mesh-discard.md)。</span><span class="sxs-lookup"><span data-stu-id="f464d-106">Used with [**ID3DX10Mesh::Discard**](id3dx10mesh-discard.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f464d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f464d-107">Syntax</span></span>


```C++
typedef enum D3DX10_MESH_DISCARD_FLAGS { 
  D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER  = 0x01,
  D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE   = 0x02,
  D3DX10_MESH_DISCARD_POINTREPS         = 0x04,
  D3DX10_MESH_DISCARD_ADJACENCY         = 0x08,
  D3DX10_MESH_DISCARD_DEVICE_BUFFERS    = 0x10
} D3DX10_MESH_DISCARD_FLAGS, *LPD3DX10_MESH_DISCARD_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="f464d-108">常數</span><span class="sxs-lookup"><span data-stu-id="f464d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f464d-109"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**D3DX10 \_ 網格 \_ 捨棄 \_ 屬性 \_ 緩衝區**</span><span class="sxs-lookup"><span data-stu-id="f464d-109"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**D3DX10\_MESH\_DISCARD\_ATTRIBUTE\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="f464d-110">捨棄屬性緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f464d-110">Discard the attribute buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f464d-111"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**D3DX10 \_ 網格 \_ 捨棄 \_ 屬性 \_ 表**</span><span class="sxs-lookup"><span data-stu-id="f464d-111"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**D3DX10\_MESH\_DISCARD\_ATTRIBUTE\_TABLE**</span></span>
</dt> <dd>

<span data-ttu-id="f464d-112">捨棄屬性資料表。</span><span class="sxs-lookup"><span data-stu-id="f464d-112">Discard the attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="f464d-113"><span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10 \_ 網格 \_ 捨棄 \_ POINTREPS**</span><span class="sxs-lookup"><span data-stu-id="f464d-113"><span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10\_MESH\_DISCARD\_POINTREPS**</span></span>
</dt> <dd>

<span data-ttu-id="f464d-114">捨棄指標代表緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f464d-114">Discard the pointer reps buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f464d-115"><span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10 \_ 網格 \_ 捨棄 \_ 相鄰**</span><span class="sxs-lookup"><span data-stu-id="f464d-115"><span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10\_MESH\_DISCARD\_ADJACENCY**</span></span>
</dt> <dd>

<span data-ttu-id="f464d-116">捨棄相鄰緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f464d-116">Discard the adjacency buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f464d-117"><span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**D3DX10 \_ 網格 \_ 捨棄 \_ 裝置 \_ 緩衝區**</span><span class="sxs-lookup"><span data-stu-id="f464d-117"><span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**D3DX10\_MESH\_DISCARD\_DEVICE\_BUFFERS**</span></span>
</dt> <dd>

<span data-ttu-id="f464d-118">使用 [**ID3DX10Mesh：： CommitToDevice**](id3dx10mesh-committodevice.md)) 捨棄認可至裝置 (的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f464d-118">Discard the buffers committed to the device (with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f464d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f464d-119">Requirements</span></span>



| <span data-ttu-id="f464d-120">需求</span><span class="sxs-lookup"><span data-stu-id="f464d-120">Requirement</span></span> | <span data-ttu-id="f464d-121">值</span><span class="sxs-lookup"><span data-stu-id="f464d-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f464d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f464d-122">Header</span></span><br/> | <dl> <span data-ttu-id="f464d-123"><dt>D3DX10Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="f464d-123"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f464d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f464d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f464d-125">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="f464d-125">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




