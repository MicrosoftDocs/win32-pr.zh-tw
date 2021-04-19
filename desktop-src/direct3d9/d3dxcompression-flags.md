---
description: 定義用來儲存壓縮動畫集資料的壓縮模式。
ms.assetid: 41592b71-52ba-4727-a885-fb10fc23c5f8
title: 'D3DXCOMPRESSION_FLAGS 列舉 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOMPRESSION_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 6f912c44659d418d543194ba82a9d82f31e7ef08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991476"
---
# <a name="d3dxcompression_flags-enumeration"></a><span data-ttu-id="f96bc-103">D3DXCOMPRESSION \_ 旗標列舉</span><span class="sxs-lookup"><span data-stu-id="f96bc-103">D3DXCOMPRESSION\_FLAGS enumeration</span></span>

<span data-ttu-id="f96bc-104">定義用來儲存壓縮動畫集資料的壓縮模式。</span><span class="sxs-lookup"><span data-stu-id="f96bc-104">Defines the compression mode used for storing compressed animation set data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f96bc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f96bc-105">Syntax</span></span>


```C++
typedef enum D3DXCOMPRESSION_FLAGS { 
  D3DXCOMPRESS_DEFAULT      = 0,
  D3DXCOMPRESS_STRONG       = 1,
  D3DXCOMPRESS_FORCE_DWORD  = 0x7fffffff
} D3DXCOMPRESSION_FLAGS, *LPD3DXCOMPRESSION_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="f96bc-106">常數</span><span class="sxs-lookup"><span data-stu-id="f96bc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f96bc-107"><span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**D3DXCOMPRESS \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="f96bc-107"><span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**D3DXCOMPRESS\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="f96bc-108">實行快速壓縮。</span><span class="sxs-lookup"><span data-stu-id="f96bc-108">Implements fast compression.</span></span>

</dd> <dt>

<span data-ttu-id="f96bc-109"><span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS \_ 強式**</span><span class="sxs-lookup"><span data-stu-id="f96bc-109"><span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS\_STRONG**</span></span>
</dt> <dd>

<span data-ttu-id="f96bc-110">執行緩慢壓縮。</span><span class="sxs-lookup"><span data-stu-id="f96bc-110">Implements slow compression.</span></span> <span data-ttu-id="f96bc-111">通常會產生比使用 D3DXCOMPRESS 預設值更高的高品質壓縮動畫 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f96bc-111">Typically results in a better quality compressed animation set than if D3DXCOMPRESS\_DEFAULT is used.</span></span>

</dd> <dt>

<span data-ttu-id="f96bc-112"><span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f96bc-112"><span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="f96bc-113">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="f96bc-113">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="f96bc-114">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="f96bc-114">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="f96bc-115">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="f96bc-115">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f96bc-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f96bc-116">Requirements</span></span>



| <span data-ttu-id="f96bc-117">需求</span><span class="sxs-lookup"><span data-stu-id="f96bc-117">Requirement</span></span> | <span data-ttu-id="f96bc-118">值</span><span class="sxs-lookup"><span data-stu-id="f96bc-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f96bc-119">標頭</span><span class="sxs-lookup"><span data-stu-id="f96bc-119">Header</span></span><br/> | <dl> <span data-ttu-id="f96bc-120"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="f96bc-120"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f96bc-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f96bc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f96bc-122">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="f96bc-122">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




