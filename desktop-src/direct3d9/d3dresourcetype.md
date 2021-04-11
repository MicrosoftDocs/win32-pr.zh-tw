---
description: 定義資源類型。
ms.assetid: 6b360fb1-4a5a-47a2-bef9-d8234770bf0c
title: 'D3DRESOURCETYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4d7fab861d85a2c0289ba1636dece0e76c7819e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946056"
---
# <a name="d3dresourcetype-enumeration"></a><span data-ttu-id="7d8b1-103">D3DRESOURCETYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="7d8b1-103">D3DRESOURCETYPE enumeration</span></span>

<span data-ttu-id="7d8b1-104">定義資源類型。</span><span class="sxs-lookup"><span data-stu-id="7d8b1-104">Defines resource types.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d8b1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d8b1-105">Syntax</span></span>


```C++
typedef enum D3DRESOURCETYPE { 
  D3DRTYPE_SURFACE        = 1,
  D3DRTYPE_VOLUME         = 2,
  D3DRTYPE_TEXTURE        = 3,
  D3DRTYPE_VOLUMETEXTURE  = 4,
  D3DRTYPE_CubeTexture    = 5,
  D3DRTYPE_VERTEXBUFFER   = 6,
  D3DRTYPE_INDEXBUFFER    = 7,
  D3DRTYPE_FORCE_DWORD    = 0x7fffffff
} D3DRESOURCETYPE, *LPD3DRESOURCETYPE;
```



## <a name="constants"></a><span data-ttu-id="7d8b1-106">常數</span><span class="sxs-lookup"><span data-stu-id="7d8b1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7d8b1-107"><span id="D3DRTYPE_SURFACE"></span><span id="d3drtype_surface"></span>**D3DRTYPE \_ 介面**</span><span class="sxs-lookup"><span data-stu-id="7d8b1-107"><span id="D3DRTYPE_SURFACE"></span><span id="d3drtype_surface"></span>**D3DRTYPE\_SURFACE**</span></span>
</dt> <dd>

<span data-ttu-id="7d8b1-108">Surface 資源。</span><span class="sxs-lookup"><span data-stu-id="7d8b1-108">Surface resource.</span></span>

</dd> <dt>

<span data-ttu-id="7d8b1-109"><span id="D3DRTYPE_VOLUME"></span><span id="d3drtype_volume"></span>**D3DRTYPE \_ 磁片區**</span><span class="sxs-lookup"><span data-stu-id="7d8b1-109"><span id="D3DRTYPE_VOLUME"></span><span id="d3drtype_volume"></span>**D3DRTYPE\_VOLUME**</span></span>
</dt> <dd>

<span data-ttu-id="7d8b1-110">磁片區資源。</span><span class="sxs-lookup"><span data-stu-id="7d8b1-110">Volume resource.</span></span>

</dd> <dt>

<span data-ttu-id="7d8b1-111"><span id="D3DRTYPE_TEXTURE"></span><span id="d3drtype_texture"></span>**D3DRTYPE \_ 材質**</span><span class="sxs-lookup"><span data-stu-id="7d8b1-111"><span id="D3DRTYPE_TEXTURE"></span><span id="d3drtype_texture"></span>**D3DRTYPE\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="7d8b1-112">材質資源。</span><span class="sxs-lookup"><span data-stu-id="7d8b1-112">Texture resource.</span></span>

</dd> <dt>

<span data-ttu-id="7d8b1-113"><span id="D3DRTYPE_VOLUMETEXTURE"></span><span id="d3drtype_volumetexture"></span>**D3DRTYPE \_ VOLUMETEXTURE**</span><span class="sxs-lookup"><span data-stu-id="7d8b1-113"><span id="D3DRTYPE_VOLUMETEXTURE"></span><span id="d3drtype_volumetexture"></span>**D3DRTYPE\_VOLUMETEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="7d8b1-114">音量材質資源。</span><span class="sxs-lookup"><span data-stu-id="7d8b1-114">Volume texture resource.</span></span>

</dd> <dt>

<span data-ttu-id="7d8b1-115"><span id="D3DRTYPE_CubeTexture"></span><span id="d3drtype_cubetexture"></span><span id="D3DRTYPE_CUBETEXTURE"></span>**D3DRTYPE \_ CubeTexture**</span><span class="sxs-lookup"><span data-stu-id="7d8b1-115"><span id="D3DRTYPE_CubeTexture"></span><span id="d3drtype_cubetexture"></span><span id="D3DRTYPE_CUBETEXTURE"></span>**D3DRTYPE\_CubeTexture**</span></span>
</dt> <dd>

<span data-ttu-id="7d8b1-116">Cube 材質資源。</span><span class="sxs-lookup"><span data-stu-id="7d8b1-116">Cube texture resource.</span></span>

</dd> <dt>

<span data-ttu-id="7d8b1-117"><span id="D3DRTYPE_VERTEXBUFFER"></span><span id="d3drtype_vertexbuffer"></span>**D3DRTYPE \_ VERTEXBUFFER**</span><span class="sxs-lookup"><span data-stu-id="7d8b1-117"><span id="D3DRTYPE_VERTEXBUFFER"></span><span id="d3drtype_vertexbuffer"></span>**D3DRTYPE\_VERTEXBUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="7d8b1-118">頂點緩衝區資源。</span><span class="sxs-lookup"><span data-stu-id="7d8b1-118">Vertex buffer resource.</span></span>

</dd> <dt>

<span data-ttu-id="7d8b1-119"><span id="D3DRTYPE_INDEXBUFFER"></span><span id="d3drtype_indexbuffer"></span>**D3DRTYPE \_ INDEXBUFFER**</span><span class="sxs-lookup"><span data-stu-id="7d8b1-119"><span id="D3DRTYPE_INDEXBUFFER"></span><span id="d3drtype_indexbuffer"></span>**D3DRTYPE\_INDEXBUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="7d8b1-120">索引緩衝區資源。</span><span class="sxs-lookup"><span data-stu-id="7d8b1-120">Index buffer resource.</span></span>

</dd> <dt>

<span data-ttu-id="7d8b1-121"><span id="D3DRTYPE_FORCE_DWORD"></span><span id="d3drtype_force_dword"></span>**D3DRTYPE \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="7d8b1-121"><span id="D3DRTYPE_FORCE_DWORD"></span><span id="d3drtype_force_dword"></span>**D3DRTYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="7d8b1-122">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="7d8b1-122">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="7d8b1-123">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="7d8b1-123">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="7d8b1-124">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="7d8b1-124">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d8b1-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d8b1-125">Requirements</span></span>



| <span data-ttu-id="7d8b1-126">需求</span><span class="sxs-lookup"><span data-stu-id="7d8b1-126">Requirement</span></span> | <span data-ttu-id="7d8b1-127">值</span><span class="sxs-lookup"><span data-stu-id="7d8b1-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d8b1-128">標頭</span><span class="sxs-lookup"><span data-stu-id="7d8b1-128">Header</span></span><br/> | <dl> <span data-ttu-id="7d8b1-129"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d8b1-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d8b1-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d8b1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d8b1-131">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="7d8b1-131">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="7d8b1-132">**IDirect3DResource9：： GetType**</span><span class="sxs-lookup"><span data-stu-id="7d8b1-132">**IDirect3DResource9::GetType**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-gettype)
</dt> </dl>

 

 
