---
description: 指定在單色介面上用來括住字元的矩形。
ms.assetid: ce5d492f-38d1-4e7b-a9c2-68c791c84d0c
title: 'D3DCOMPOSERECTDESC 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cf9ad5f1c075f4dc52d68b894b37c7d0f0a7b310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386434"
---
# <a name="d3dcomposerectdesc-structure"></a><span data-ttu-id="4d7a8-103">D3DCOMPOSERECTDESC 結構</span><span class="sxs-lookup"><span data-stu-id="4d7a8-103">D3DCOMPOSERECTDESC structure</span></span>

<span data-ttu-id="4d7a8-104">指定在單色介面上用來括住字元的矩形。</span><span class="sxs-lookup"><span data-stu-id="4d7a8-104">Specifies the rectangle used to enclose glyphs on a monochrome surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d7a8-105">語法</span><span class="sxs-lookup"><span data-stu-id="4d7a8-105">Syntax</span></span>


```C++
typedef struct _D3DCOMPOSERECTDESC {
  USHORT X;
  USHORT Y;
  USHORT Width;
  USHORT Height;
} D3DCOMPOSERECTDESC;
```



## <a name="members"></a><span data-ttu-id="4d7a8-106">成員</span><span class="sxs-lookup"><span data-stu-id="4d7a8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4d7a8-107">**X**</span><span class="sxs-lookup"><span data-stu-id="4d7a8-107">**X**</span></span>
</dt> <dd>

<span data-ttu-id="4d7a8-108">類型： **[ **USHORT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d7a8-108">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4d7a8-109">開始複製的左座標。</span><span class="sxs-lookup"><span data-stu-id="4d7a8-109">Left coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="4d7a8-110">**Y**</span><span class="sxs-lookup"><span data-stu-id="4d7a8-110">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="4d7a8-111">類型： **[ **USHORT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d7a8-111">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4d7a8-112">開始複製的上座標。</span><span class="sxs-lookup"><span data-stu-id="4d7a8-112">Top coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="4d7a8-113">**寬度**</span><span class="sxs-lookup"><span data-stu-id="4d7a8-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="4d7a8-114">類型： **[ **USHORT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d7a8-114">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4d7a8-115">從左座標的材質數目。</span><span class="sxs-lookup"><span data-stu-id="4d7a8-115">Number of texels from left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="4d7a8-116">**高度**</span><span class="sxs-lookup"><span data-stu-id="4d7a8-116">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="4d7a8-117">類型： **[ **USHORT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d7a8-117">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4d7a8-118">從上座標開始的材質數目。</span><span class="sxs-lookup"><span data-stu-id="4d7a8-118">Number of texels from the top coordinate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d7a8-119">備註</span><span class="sxs-lookup"><span data-stu-id="4d7a8-119">Remarks</span></span>

<span data-ttu-id="4d7a8-120">此結構是用來呼叫 [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) ，以括住來源介面上的字元。</span><span class="sxs-lookup"><span data-stu-id="4d7a8-120">This structure is used in calls to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) to enclose glyphs on the source surface.</span></span> <span data-ttu-id="4d7a8-121">頂點緩衝區 (看到以這些結構填入的 [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) 會建立成包含字元位置。</span><span class="sxs-lookup"><span data-stu-id="4d7a8-121">A vertex buffer (see [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) filled with these structures are created to contain the glyph locations.</span></span> <span data-ttu-id="4d7a8-122">USHORT 成員是用來盡可能減少記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="4d7a8-122">USHORT members are used to reduce the memory footprint as much as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d7a8-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d7a8-123">Requirements</span></span>



| <span data-ttu-id="4d7a8-124">需求</span><span class="sxs-lookup"><span data-stu-id="4d7a8-124">Requirement</span></span> | <span data-ttu-id="4d7a8-125">值</span><span class="sxs-lookup"><span data-stu-id="4d7a8-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d7a8-126">標頭</span><span class="sxs-lookup"><span data-stu-id="4d7a8-126">Header</span></span><br/> | <dl> <span data-ttu-id="4d7a8-127"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="4d7a8-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d7a8-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d7a8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d7a8-129">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="4d7a8-129">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
