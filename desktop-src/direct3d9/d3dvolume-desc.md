---
description: 描述磁片區。
ms.assetid: c0224f4e-3d32-4bdd-b56c-4e8aa291bb27
title: 'D3DVOLUME_DESC 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVOLUME_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b736333cefcfc8a3307ff7a0cecd53cd96bc0af2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323052"
---
# <a name="d3dvolume_desc-structure"></a><span data-ttu-id="7d89e-103">D3DVOLUME \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="7d89e-103">D3DVOLUME\_DESC structure</span></span>

<span data-ttu-id="7d89e-104">描述磁片區。</span><span class="sxs-lookup"><span data-stu-id="7d89e-104">Describes a volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d89e-105">語法</span><span class="sxs-lookup"><span data-stu-id="7d89e-105">Syntax</span></span>


```C++
typedef struct D3DVOLUME_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Width;
  UINT            Height;
  UINT            Depth;
} D3DVOLUME_DESC, *LPD3DVOLUME_DESC;
```



## <a name="members"></a><span data-ttu-id="7d89e-106">成員</span><span class="sxs-lookup"><span data-stu-id="7d89e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7d89e-107">**格式**</span><span class="sxs-lookup"><span data-stu-id="7d89e-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="7d89e-108">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="7d89e-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7d89e-109">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述磁片區的介面格式。</span><span class="sxs-lookup"><span data-stu-id="7d89e-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the volume.</span></span>

</dd> <dt>

<span data-ttu-id="7d89e-110">**型別**</span><span class="sxs-lookup"><span data-stu-id="7d89e-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="7d89e-111">類型： **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="7d89e-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7d89e-112">[**D3DRESOURCETYPE**](./d3dresourcetype.md)列舉型別的成員，將此資源識別為磁片區。</span><span class="sxs-lookup"><span data-stu-id="7d89e-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a volume.</span></span>

</dd> <dt>

<span data-ttu-id="7d89e-113">**使用量**</span><span class="sxs-lookup"><span data-stu-id="7d89e-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="7d89e-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d89e-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7d89e-115">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="7d89e-115">Currently not used.</span></span> <span data-ttu-id="7d89e-116">一律傳回為0。</span><span class="sxs-lookup"><span data-stu-id="7d89e-116">Always returned as 0.</span></span>

</dd> <dt>

<span data-ttu-id="7d89e-117">**集區**</span><span class="sxs-lookup"><span data-stu-id="7d89e-117">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="7d89e-118">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="7d89e-118">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7d89e-119">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，指定配置給這個磁片區的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="7d89e-119">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this volume.</span></span>

</dd> <dt>

<span data-ttu-id="7d89e-120">**寬度**</span><span class="sxs-lookup"><span data-stu-id="7d89e-120">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="7d89e-121">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d89e-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7d89e-122">磁片區的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="7d89e-122">Width of the volume, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="7d89e-123">**高度**</span><span class="sxs-lookup"><span data-stu-id="7d89e-123">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="7d89e-124">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d89e-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7d89e-125">磁片區的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="7d89e-125">Height of the volume, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="7d89e-126">**深度**</span><span class="sxs-lookup"><span data-stu-id="7d89e-126">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="7d89e-127">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d89e-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7d89e-128">磁片區的深度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="7d89e-128">Depth of the volume, in pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d89e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d89e-129">Requirements</span></span>



| <span data-ttu-id="7d89e-130">需求</span><span class="sxs-lookup"><span data-stu-id="7d89e-130">Requirement</span></span> | <span data-ttu-id="7d89e-131">值</span><span class="sxs-lookup"><span data-stu-id="7d89e-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d89e-132">標頭</span><span class="sxs-lookup"><span data-stu-id="7d89e-132">Header</span></span><br/> | <dl> <span data-ttu-id="7d89e-133"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d89e-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d89e-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d89e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d89e-135">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="7d89e-135">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="7d89e-136">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="7d89e-136">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getdesc)
</dt> <dt>

[<span data-ttu-id="7d89e-137">**GetLevelDesc**</span><span class="sxs-lookup"><span data-stu-id="7d89e-137">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-getleveldesc)
</dt> </dl>

 

 
