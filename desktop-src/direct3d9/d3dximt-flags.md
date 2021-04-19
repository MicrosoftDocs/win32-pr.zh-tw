---
description: IMT 計算 Api 的材質換行選項。
ms.assetid: ec364418-67c6-42c7-9c5d-b97aa7e17c24
title: 'D3DXIMT 旗標列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 97731d4720e67fce899bf96f457e55f6adbc05a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992314"
---
# <a name="d3dximt-flags-enumeration"></a><span data-ttu-id="74b85-103">D3DXIMT 旗標列舉</span><span class="sxs-lookup"><span data-stu-id="74b85-103">D3DXIMT FLAGS enumeration</span></span>

<span data-ttu-id="74b85-104">IMT 計算 Api 的材質換行選項。</span><span class="sxs-lookup"><span data-stu-id="74b85-104">Texture wrapping options for IMT computation APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="74b85-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="74b85-105">Syntax</span></span>


```C++
typedef enum D3DXIMT_FLAGS { 
  D3DXIMT_WRAP_U   = 1,
  D3DXIMT_WRAP_V   = 2,
  D3DXIMT_WRAP_UV  = 3
} D3DXIMT FLAGS, *LPD3DXIMT FLAGS;
```



## <a name="constants"></a><span data-ttu-id="74b85-106">常數</span><span class="sxs-lookup"><span data-stu-id="74b85-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="74b85-107"><span id="D3DXIMT_WRAP_U"></span><span id="d3dximt_wrap_u"></span>**D3DXIMT \_ WRAP \_ U**</span><span class="sxs-lookup"><span data-stu-id="74b85-107"><span id="D3DXIMT_WRAP_U"></span><span id="d3dximt_wrap_u"></span>**D3DXIMT\_WRAP\_U**</span></span>
</dt> <dd>

<span data-ttu-id="74b85-108">紋理會以 U 方向換行。</span><span class="sxs-lookup"><span data-stu-id="74b85-108">The texture wraps in the U direction.</span></span>

</dd> <dt>

<span data-ttu-id="74b85-109"><span id="D3DXIMT_WRAP_V"></span><span id="d3dximt_wrap_v"></span>**D3DXIMT \_ WRAP \_ V**</span><span class="sxs-lookup"><span data-stu-id="74b85-109"><span id="D3DXIMT_WRAP_V"></span><span id="d3dximt_wrap_v"></span>**D3DXIMT\_WRAP\_V**</span></span>
</dt> <dd>

<span data-ttu-id="74b85-110">材質會以 V 方向換行。</span><span class="sxs-lookup"><span data-stu-id="74b85-110">The texture wraps in the V direction.</span></span>

</dd> <dt>

<span data-ttu-id="74b85-111"><span id="D3DXIMT_WRAP_UV"></span><span id="d3dximt_wrap_uv"></span>**D3DXIMT \_ WRAP \_ UV**</span><span class="sxs-lookup"><span data-stu-id="74b85-111"><span id="D3DXIMT_WRAP_UV"></span><span id="d3dximt_wrap_uv"></span>**D3DXIMT\_WRAP\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="74b85-112">紋理會以您和 V 方向換行。</span><span class="sxs-lookup"><span data-stu-id="74b85-112">The texture wraps in both the U and V direction.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74b85-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="74b85-113">Requirements</span></span>



| <span data-ttu-id="74b85-114">需求</span><span class="sxs-lookup"><span data-stu-id="74b85-114">Requirement</span></span> | <span data-ttu-id="74b85-115">值</span><span class="sxs-lookup"><span data-stu-id="74b85-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74b85-116">標頭</span><span class="sxs-lookup"><span data-stu-id="74b85-116">Header</span></span><br/> | <dl> <span data-ttu-id="74b85-117"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="74b85-117"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74b85-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74b85-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74b85-119">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="74b85-119">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="74b85-120">**D3DXComputeIMTFromSignal**</span><span class="sxs-lookup"><span data-stu-id="74b85-120">**D3DXComputeIMTFromSignal**</span></span>](d3dxcomputeimtfromsignal.md)
</dt> <dt>

[<span data-ttu-id="74b85-121">**D3DXComputeIMTFromTexture**</span><span class="sxs-lookup"><span data-stu-id="74b85-121">**D3DXComputeIMTFromTexture**</span></span>](d3dxcomputeimtfromtexture.md)
</dt> <dt>

[<span data-ttu-id="74b85-122">**D3DXComputeIMTFromPerTexelSignal**</span><span class="sxs-lookup"><span data-stu-id="74b85-122">**D3DXComputeIMTFromPerTexelSignal**</span></span>](d3dxcomputeimtfrompertexelsignal.md)
</dt> <dt>

[<span data-ttu-id="74b85-123">**D3DXComputeIMTFromPerVertexSignal**</span><span class="sxs-lookup"><span data-stu-id="74b85-123">**D3DXComputeIMTFromPerVertexSignal**</span></span>](d3dxcomputeimtfrompervertexsignal.md)
</dt> </dl>

 

 




