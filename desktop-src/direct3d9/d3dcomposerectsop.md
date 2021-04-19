---
description: 指定如何在呼叫 ComposeRects 時，結合來源和目的介面中的字元資料。
ms.assetid: 4b0e6e48-48e0-4955-bb20-f953fdce785c
title: 'D3DCOMPOSERECTSOP 列舉 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTSOP
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cd47cb14ab129bf27a4b59ba07e0be12d144fb8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999000"
---
# <a name="d3dcomposerectsop-enumeration"></a><span data-ttu-id="e1729-103">D3DCOMPOSERECTSOP 列舉</span><span class="sxs-lookup"><span data-stu-id="e1729-103">D3DCOMPOSERECTSOP enumeration</span></span>

<span data-ttu-id="e1729-104">指定如何在呼叫 [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects)時，結合來源和目的介面中的字元資料。</span><span class="sxs-lookup"><span data-stu-id="e1729-104">Specifies how to combine the glyph data from the source and destination surfaces in a call to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects).</span></span>

## <a name="syntax"></a><span data-ttu-id="e1729-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1729-105">Syntax</span></span>


```C++
typedef enum _D3DCOMPOSERECTSOP { 
  D3DCOMPOSERECTS_COPY         = 1,
  D3DCOMPOSERECTS_OR           = 2,
  D3DCOMPOSERECTS_AND          = 3,
  D3DCOMPOSERECTS_NEG          = 4,
  D3DCOMPOSERECTS_FORCE_DWORD  = 0x7fffffff
} D3DCOMPOSERECTSOP;
```



## <a name="constants"></a><span data-ttu-id="e1729-106">常數</span><span class="sxs-lookup"><span data-stu-id="e1729-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e1729-107"><span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**D3DCOMPOSERECTS \_ 複製**</span><span class="sxs-lookup"><span data-stu-id="e1729-107"><span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**D3DCOMPOSERECTS\_COPY**</span></span>
</dt> <dd>

<span data-ttu-id="e1729-108">將來源複製到目的地。</span><span class="sxs-lookup"><span data-stu-id="e1729-108">Copy the source to the destination.</span></span>

</dd> <dt>

<span data-ttu-id="e1729-109"><span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS \_ 或**</span><span class="sxs-lookup"><span data-stu-id="e1729-109"><span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS\_OR**</span></span>
</dt> <dd>

<span data-ttu-id="e1729-110">位或來源和目的地。</span><span class="sxs-lookup"><span data-stu-id="e1729-110">Bitwise OR the source and the destination.</span></span>

</dd> <dt>

<span data-ttu-id="e1729-111"><span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS \_ 和**</span><span class="sxs-lookup"><span data-stu-id="e1729-111"><span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS\_AND**</span></span>
</dt> <dd>

<span data-ttu-id="e1729-112">位和來源和目的地。</span><span class="sxs-lookup"><span data-stu-id="e1729-112">Bitwise AND the source and the destination.</span></span>

</dd> <dt>

<span data-ttu-id="e1729-113"><span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS \_ >neg**</span><span class="sxs-lookup"><span data-stu-id="e1729-113"><span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS\_NEG**</span></span>
</dt> <dd>

<span data-ttu-id="e1729-114">將否定來源複製到目的地 (Dst & ~ Src) 。</span><span class="sxs-lookup"><span data-stu-id="e1729-114">Copy the negated source to the destination (Dst & ~Src).</span></span>

</dd> <dt>

<span data-ttu-id="e1729-115"><span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e1729-115"><span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="e1729-116">保留的。</span><span class="sxs-lookup"><span data-stu-id="e1729-116">Reserved.</span></span> <span data-ttu-id="e1729-117">用來強制列舉的大小為 32-位。</span><span class="sxs-lookup"><span data-stu-id="e1729-117">Used to force enumeration to 32-bits in size.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1729-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1729-118">Requirements</span></span>



| <span data-ttu-id="e1729-119">需求</span><span class="sxs-lookup"><span data-stu-id="e1729-119">Requirement</span></span> | <span data-ttu-id="e1729-120">值</span><span class="sxs-lookup"><span data-stu-id="e1729-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1729-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e1729-121">Header</span></span><br/> | <dl> <span data-ttu-id="e1729-122"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="e1729-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1729-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1729-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1729-124">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="e1729-124">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




