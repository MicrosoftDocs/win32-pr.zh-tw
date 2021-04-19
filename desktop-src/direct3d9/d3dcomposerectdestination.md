---
description: 指定要在單色介面中複製字元的來源字元和位置。
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: 'D3DCOMPOSERECTDESTINATION 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESTINATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 56843bc78943a4c76fe4fe0f5e18242728a979c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982199"
---
# <a name="d3dcomposerectdestination-structure"></a><span data-ttu-id="e1eea-103">D3DCOMPOSERECTDESTINATION 結構</span><span class="sxs-lookup"><span data-stu-id="e1eea-103">D3DCOMPOSERECTDESTINATION structure</span></span>

<span data-ttu-id="e1eea-104">指定要在單色介面中複製字元的來源字元和位置。</span><span class="sxs-lookup"><span data-stu-id="e1eea-104">Specifies the source glyph and location in a monochrome surface to copy glyphs into.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1eea-105">語法</span><span class="sxs-lookup"><span data-stu-id="e1eea-105">Syntax</span></span>


```C++
typedef struct _D3DCOMPOSERECTDESTINATION {
  USHORT SrcRectIndex;
  USHORT Reserved;
  USHORT X;
  USHORT Y;
} D3DCOMPOSERECTDESTINATION;
```



## <a name="members"></a><span data-ttu-id="e1eea-106">成員</span><span class="sxs-lookup"><span data-stu-id="e1eea-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e1eea-107">**SrcRectIndex**</span><span class="sxs-lookup"><span data-stu-id="e1eea-107">**SrcRectIndex**</span></span>
</dt> <dd>

<span data-ttu-id="e1eea-108">類型： **[ **USHORT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1eea-108">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e1eea-109">從包含 [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) 結構的頂點緩衝區索引特定圖像。</span><span class="sxs-lookup"><span data-stu-id="e1eea-109">Index particular glyph from vertex buffer containing [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="e1eea-110">**已保留**</span><span class="sxs-lookup"><span data-stu-id="e1eea-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="e1eea-111">類型： **[ **USHORT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1eea-111">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e1eea-112">保留以供對齊之用。</span><span class="sxs-lookup"><span data-stu-id="e1eea-112">Reserved for alignment purposes.</span></span>

</dd> <dt>

<span data-ttu-id="e1eea-113">**X**</span><span class="sxs-lookup"><span data-stu-id="e1eea-113">**X**</span></span>
</dt> <dd>

<span data-ttu-id="e1eea-114">類型： **[ **USHORT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1eea-114">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e1eea-115">開始複製的左座標。</span><span class="sxs-lookup"><span data-stu-id="e1eea-115">Left coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="e1eea-116">**Y**</span><span class="sxs-lookup"><span data-stu-id="e1eea-116">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="e1eea-117">類型： **[ **USHORT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1eea-117">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e1eea-118">開始複製的上座標。</span><span class="sxs-lookup"><span data-stu-id="e1eea-118">Top coordinate to begin copy at.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1eea-119">備註</span><span class="sxs-lookup"><span data-stu-id="e1eea-119">Remarks</span></span>

<span data-ttu-id="e1eea-120">此結構是用來呼叫 [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) ，以指出應該將位置圖像複製到的位置，以及應該複製的特定圖像。</span><span class="sxs-lookup"><span data-stu-id="e1eea-120">This structure is used in calls to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) to indicate the location glyphs should be copied to and which particular glyph should be copied.</span></span> <span data-ttu-id="e1eea-121">頂點緩衝區 (看到以這些結構填入的 [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) 會建立成包含字元位置。</span><span class="sxs-lookup"><span data-stu-id="e1eea-121">A vertex buffer (see [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) filled with these structures are created to contain the glyph locations.</span></span> <span data-ttu-id="e1eea-122">USHORT 成員是用來盡可能減少記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="e1eea-122">USHORT members are used to reduce the memory footprint as much as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1eea-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1eea-123">Requirements</span></span>



| <span data-ttu-id="e1eea-124">需求</span><span class="sxs-lookup"><span data-stu-id="e1eea-124">Requirement</span></span> | <span data-ttu-id="e1eea-125">值</span><span class="sxs-lookup"><span data-stu-id="e1eea-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1eea-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e1eea-126">Header</span></span><br/> | <dl> <span data-ttu-id="e1eea-127"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="e1eea-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1eea-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1eea-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1eea-129">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="e1eea-129">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
