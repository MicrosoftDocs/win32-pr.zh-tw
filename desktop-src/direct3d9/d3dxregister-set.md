---
description: 註冊的資料類型。
ms.assetid: b54530d3-4267-4b41-9a16-59d400ef3e18
title: 'D3DXREGISTER_SET 列舉 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXREGISTER_SET
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 683b13d0b386fcdbc162293455e2beb11bc1ee85
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986085"
---
# <a name="d3dxregister_set-enumeration"></a><span data-ttu-id="4aef8-103">D3DXREGISTER \_ 集合列舉</span><span class="sxs-lookup"><span data-stu-id="4aef8-103">D3DXREGISTER\_SET enumeration</span></span>

<span data-ttu-id="4aef8-104">註冊的資料類型。</span><span class="sxs-lookup"><span data-stu-id="4aef8-104">Data type of the register.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aef8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4aef8-105">Syntax</span></span>


```C++
typedef enum _D3DXREGISTER_SET { 
  D3DXRS_BOOL,
  D3DXRS_INT4,
  D3DXRS_FLOAT4,
  D3DXRS_SAMPLER,
  D3DXRS_FORCE_DWORD  = 0x7fffffff
} D3DXREGISTER_SET, *LPD3DXREGISTER_SET;
```



## <a name="constants"></a><span data-ttu-id="4aef8-106">常數</span><span class="sxs-lookup"><span data-stu-id="4aef8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4aef8-107"><span id="D3DXRS_BOOL"></span><span id="d3dxrs_bool"></span>**D3DXRS \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="4aef8-107"><span id="D3DXRS_BOOL"></span><span id="d3dxrs_bool"></span>**D3DXRS\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="4aef8-108">布林值。</span><span class="sxs-lookup"><span data-stu-id="4aef8-108">Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="4aef8-109"><span id="D3DXRS_INT4"></span><span id="d3dxrs_int4"></span>**D3DXRS \_ INT4**</span><span class="sxs-lookup"><span data-stu-id="4aef8-109"><span id="D3DXRS_INT4"></span><span id="d3dxrs_int4"></span>**D3DXRS\_INT4**</span></span>
</dt> <dd>

<span data-ttu-id="4aef8-110">4D 整數數位。</span><span class="sxs-lookup"><span data-stu-id="4aef8-110">4D integer number.</span></span>

</dd> <dt>

<span data-ttu-id="4aef8-111"><span id="D3DXRS_FLOAT4"></span><span id="d3dxrs_float4"></span>**D3DXRS \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="4aef8-111"><span id="D3DXRS_FLOAT4"></span><span id="d3dxrs_float4"></span>**D3DXRS\_FLOAT4**</span></span>
</dt> <dd>

<span data-ttu-id="4aef8-112">4D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="4aef8-112">4D floating-point number.</span></span>

</dd> <dt>

<span data-ttu-id="4aef8-113"><span id="D3DXRS_SAMPLER"></span><span id="d3dxrs_sampler"></span>**D3DXRS \_ 取樣器**</span><span class="sxs-lookup"><span data-stu-id="4aef8-113"><span id="D3DXRS_SAMPLER"></span><span id="d3dxrs_sampler"></span>**D3DXRS\_SAMPLER**</span></span>
</dt> <dd>

<span data-ttu-id="4aef8-114">此註冊包含4D 取樣器資料。</span><span class="sxs-lookup"><span data-stu-id="4aef8-114">The register contains 4D sampler data.</span></span>

</dd> <dt>

<span data-ttu-id="4aef8-115"><span id="D3DXRS_FORCE_DWORD"></span><span id="d3dxrs_force_dword"></span>**D3DXRS \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4aef8-115"><span id="D3DXRS_FORCE_DWORD"></span><span id="d3dxrs_force_dword"></span>**D3DXRS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="4aef8-116">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="4aef8-116">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="4aef8-117">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="4aef8-117">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="4aef8-118">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="4aef8-118">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4aef8-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4aef8-119">Requirements</span></span>



| <span data-ttu-id="4aef8-120">需求</span><span class="sxs-lookup"><span data-stu-id="4aef8-120">Requirement</span></span> | <span data-ttu-id="4aef8-121">值</span><span class="sxs-lookup"><span data-stu-id="4aef8-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aef8-122">標頭</span><span class="sxs-lookup"><span data-stu-id="4aef8-122">Header</span></span><br/> | <dl> <span data-ttu-id="4aef8-123"><dt>D3dx9shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="4aef8-123"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aef8-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4aef8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aef8-125">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="4aef8-125">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="4aef8-126">**D3DXSHADER \_ CONSTANTINFO**</span><span class="sxs-lookup"><span data-stu-id="4aef8-126">**D3DXSHADER\_CONSTANTINFO**</span></span>](d3dxshader-constantinfo.md)
</dt> <dt>

[<span data-ttu-id="4aef8-127">**D3DXCONSTANT \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="4aef8-127">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




