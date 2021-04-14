---
description: 描述頂點緩衝區。
ms.assetid: 0ae8f976-d0ca-4d55-b6db-5be85fa3c799
title: 'D3DVERTEXBUFFER_DESC 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b2c0838743f8190eeb0e5c825e7125d2e48c0b6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514649"
---
# <a name="d3dvertexbuffer_desc-structure"></a><span data-ttu-id="a39af-103">D3DVERTEXBUFFER \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="a39af-103">D3DVERTEXBUFFER\_DESC structure</span></span>

<span data-ttu-id="a39af-104">描述頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a39af-104">Describes a vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a39af-105">語法</span><span class="sxs-lookup"><span data-stu-id="a39af-105">Syntax</span></span>


```C++
typedef struct D3DVERTEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
  DWORD           FVF;
} D3DVERTEXBUFFER_DESC, *LPD3DVERTEXBUFFER_DESC;
```



## <a name="members"></a><span data-ttu-id="a39af-106">成員</span><span class="sxs-lookup"><span data-stu-id="a39af-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a39af-107">**格式**</span><span class="sxs-lookup"><span data-stu-id="a39af-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="a39af-108">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="a39af-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a39af-109">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述頂點緩衝區資料的表面格式。</span><span class="sxs-lookup"><span data-stu-id="a39af-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the vertex buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="a39af-110">**型別**</span><span class="sxs-lookup"><span data-stu-id="a39af-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="a39af-111">類型： **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="a39af-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a39af-112">[**D3DRESOURCETYPE**](./d3dresourcetype.md)列舉型別的成員，將此資源識別為頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a39af-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a39af-113">**使用量**</span><span class="sxs-lookup"><span data-stu-id="a39af-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="a39af-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a39af-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a39af-115">一或多個 [**D3DUSAGE**](d3dusage.md) 旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="a39af-115">Combination of one or more [**D3DUSAGE**](d3dusage.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="a39af-116">**集區**</span><span class="sxs-lookup"><span data-stu-id="a39af-116">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="a39af-117">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="a39af-117">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a39af-118">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，指定配置給這個頂點緩衝區的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="a39af-118">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a39af-119">**大小**</span><span class="sxs-lookup"><span data-stu-id="a39af-119">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="a39af-120">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a39af-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a39af-121">頂點緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a39af-121">Size of the vertex buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a39af-122">**FVF**</span><span class="sxs-lookup"><span data-stu-id="a39af-122">**FVF**</span></span>
</dt> <dd>

<span data-ttu-id="a39af-123">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a39af-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a39af-124">描述此緩衝區中頂點頂點格式的 [D3DFVF](d3dfvf.md) 組合。</span><span class="sxs-lookup"><span data-stu-id="a39af-124">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format of the vertices in this buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a39af-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="a39af-125">Requirements</span></span>



| <span data-ttu-id="a39af-126">需求</span><span class="sxs-lookup"><span data-stu-id="a39af-126">Requirement</span></span> | <span data-ttu-id="a39af-127">值</span><span class="sxs-lookup"><span data-stu-id="a39af-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a39af-128">標頭</span><span class="sxs-lookup"><span data-stu-id="a39af-128">Header</span></span><br/> | <dl> <span data-ttu-id="a39af-129"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="a39af-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a39af-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a39af-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a39af-131">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="a39af-131">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="a39af-132">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="a39af-132">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-getdesc)
</dt> <dt>

[<span data-ttu-id="a39af-133"> (Direct3D 9) 的頂點緩衝區 </span><span class="sxs-lookup"><span data-stu-id="a39af-133">Vertex Buffers (Direct3D 9)</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
