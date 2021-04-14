---
description: 定義立方體貼圖的臉部。
ms.assetid: 6d18b410-6f22-4202-86ae-6b3ef85e6f69
title: 'D3DCUBEMAP_FACES 列舉 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCUBEMAP_FACES
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: eaf482f6f98d695f3aea3198948616c05ed01f72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322739"
---
# <a name="d3dcubemap_faces-enumeration"></a><span data-ttu-id="a2efc-103">D3DCUBEMAP \_ 臉部列舉</span><span class="sxs-lookup"><span data-stu-id="a2efc-103">D3DCUBEMAP\_FACES enumeration</span></span>

<span data-ttu-id="a2efc-104">定義立方體貼圖的臉部。</span><span class="sxs-lookup"><span data-stu-id="a2efc-104">Defines the faces of a cubemap.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2efc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2efc-105">Syntax</span></span>


```C++
typedef enum D3DCUBEMAP_FACES { 
  D3DCUBEMAP_FACE_POSITIVE_X   = 0,
  D3DCUBEMAP_FACE_NEGATIVE_X   = 1,
  D3DCUBEMAP_FACE_POSITIVE_Y   = 2,
  D3DCUBEMAP_FACE_NEGATIVE_Y   = 3,
  D3DCUBEMAP_FACE_POSITIVE_Z   = 4,
  D3DCUBEMAP_FACE_NEGATIVE_Z   = 5,
  D3DCUBEMAP_FACE_FORCE_DWORD  = 0xffffffff
} D3DCUBEMAP_FACES, *LPD3DCUBEMAP_FACES;
```



## <a name="constants"></a><span data-ttu-id="a2efc-106">常數</span><span class="sxs-lookup"><span data-stu-id="a2efc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a2efc-107"><span id="D3DCUBEMAP_FACE_POSITIVE_X"></span><span id="d3dcubemap_face_positive_x"></span>**D3DCUBEMAP \_ 臉部 \_ 正 \_ X**</span><span class="sxs-lookup"><span data-stu-id="a2efc-107"><span id="D3DCUBEMAP_FACE_POSITIVE_X"></span><span id="d3dcubemap_face_positive_x"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_X**</span></span>
</dt> <dd>

<span data-ttu-id="a2efc-108">正 x-立方體貼圖的臉部。</span><span class="sxs-lookup"><span data-stu-id="a2efc-108">Positive x-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="a2efc-109"><span id="D3DCUBEMAP_FACE_NEGATIVE_X"></span><span id="d3dcubemap_face_negative_x"></span>**D3DCUBEMAP \_ 臉部 \_ 負 \_ X**</span><span class="sxs-lookup"><span data-stu-id="a2efc-109"><span id="D3DCUBEMAP_FACE_NEGATIVE_X"></span><span id="d3dcubemap_face_negative_x"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_X**</span></span>
</dt> <dd>

<span data-ttu-id="a2efc-110">負 x-立方體貼圖的臉部。</span><span class="sxs-lookup"><span data-stu-id="a2efc-110">Negative x-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="a2efc-111"><span id="D3DCUBEMAP_FACE_POSITIVE_Y"></span><span id="d3dcubemap_face_positive_y"></span>**D3DCUBEMAP \_ 臉部 \_ 正面 \_ Y**</span><span class="sxs-lookup"><span data-stu-id="a2efc-111"><span id="D3DCUBEMAP_FACE_POSITIVE_Y"></span><span id="d3dcubemap_face_positive_y"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="a2efc-112">正面 y-立方體貼圖的臉部。</span><span class="sxs-lookup"><span data-stu-id="a2efc-112">Positive y-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="a2efc-113"><span id="D3DCUBEMAP_FACE_NEGATIVE_Y"></span><span id="d3dcubemap_face_negative_y"></span>**D3DCUBEMAP \_ 臉部 \_ 負 \_ Y**</span><span class="sxs-lookup"><span data-stu-id="a2efc-113"><span id="D3DCUBEMAP_FACE_NEGATIVE_Y"></span><span id="d3dcubemap_face_negative_y"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="a2efc-114">負 y-立方體貼圖的臉部。</span><span class="sxs-lookup"><span data-stu-id="a2efc-114">Negative y-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="a2efc-115"><span id="D3DCUBEMAP_FACE_POSITIVE_Z"></span><span id="d3dcubemap_face_positive_z"></span>**D3DCUBEMAP \_ 面 \_ 正 \_ Z**</span><span class="sxs-lookup"><span data-stu-id="a2efc-115"><span id="D3DCUBEMAP_FACE_POSITIVE_Z"></span><span id="d3dcubemap_face_positive_z"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="a2efc-116">正 z-立方體貼圖的臉部。</span><span class="sxs-lookup"><span data-stu-id="a2efc-116">Positive z-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="a2efc-117"><span id="D3DCUBEMAP_FACE_NEGATIVE_Z"></span><span id="d3dcubemap_face_negative_z"></span>**D3DCUBEMAP \_ 臉部 \_ 負 \_ Z**</span><span class="sxs-lookup"><span data-stu-id="a2efc-117"><span id="D3DCUBEMAP_FACE_NEGATIVE_Z"></span><span id="d3dcubemap_face_negative_z"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="a2efc-118">負 z-立方體貼圖的臉部。</span><span class="sxs-lookup"><span data-stu-id="a2efc-118">Negative z-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="a2efc-119"><span id="D3DCUBEMAP_FACE_FORCE_DWORD"></span><span id="d3dcubemap_face_force_dword"></span>**D3DCUBEMAP \_ 臉部 \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a2efc-119"><span id="D3DCUBEMAP_FACE_FORCE_DWORD"></span><span id="d3dcubemap_face_force_dword"></span>**D3DCUBEMAP\_FACE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a2efc-120">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="a2efc-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a2efc-121">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="a2efc-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a2efc-122">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="a2efc-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2efc-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2efc-123">Requirements</span></span>



| <span data-ttu-id="a2efc-124">需求</span><span class="sxs-lookup"><span data-stu-id="a2efc-124">Requirement</span></span> | <span data-ttu-id="a2efc-125">值</span><span class="sxs-lookup"><span data-stu-id="a2efc-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2efc-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a2efc-126">Header</span></span><br/> | <dl> <span data-ttu-id="a2efc-127"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="a2efc-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2efc-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2efc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2efc-129">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="a2efc-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="a2efc-130">**IDirect3DCubeTexture9::AddDirtyRect**</span><span class="sxs-lookup"><span data-stu-id="a2efc-130">**IDirect3DCubeTexture9::AddDirtyRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-adddirtyrect)
</dt> <dt>

[<span data-ttu-id="a2efc-131">**IDirect3DCubeTexture9::GetCubeMapSurface**</span><span class="sxs-lookup"><span data-stu-id="a2efc-131">**IDirect3DCubeTexture9::GetCubeMapSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
</dt> <dt>

[<span data-ttu-id="a2efc-132">**IDirect3DCubeTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="a2efc-132">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="a2efc-133">**IDirect3DCubeTexture9::UnlockRect**</span><span class="sxs-lookup"><span data-stu-id="a2efc-133">**IDirect3DCubeTexture9::UnlockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-unlockrect)
</dt> </dl>

 

 
