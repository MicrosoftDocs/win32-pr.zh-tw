---
description: 球形調和 (SH) 壓縮設定。
ms.assetid: 214d6efb-419d-4eea-8360-322885c26bc3
title: 'D3DXSHCOMPRESSQUALITYTYPE 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHCOMPRESSQUALITYTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d61c70317505442ca4911a13dac8566f9bd7c6fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196239"
---
# <a name="d3dxshcompressqualitytype-enumeration"></a><span data-ttu-id="97f55-103">D3DXSHCOMPRESSQUALITYTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="97f55-103">D3DXSHCOMPRESSQUALITYTYPE enumeration</span></span>

<span data-ttu-id="97f55-104">球形調和 (SH) 壓縮設定。</span><span class="sxs-lookup"><span data-stu-id="97f55-104">Spherical harmonic (SH) compression setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="97f55-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="97f55-105">Syntax</span></span>


```C++
typedef enum D3DXSHCOMPRESSQUALITYTYPE { 
  D3DXSHCQUAL_FASTLOWQUALITY   = 1,
  D3DXSHCQUAL_SLOWHIGHQUALITY  = 2,
  D3DXSHCQUAL_FORCE_DWORD      = 0x7fffffff
} D3DXSHCOMPRESSQUALITYTYPE, *LPD3DXSHCOMPRESSQUALITYTYPE;
```



## <a name="constants"></a><span data-ttu-id="97f55-106">常數</span><span class="sxs-lookup"><span data-stu-id="97f55-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="97f55-107"><span id="D3DXSHCQUAL_FASTLOWQUALITY"></span><span id="d3dxshcqual_fastlowquality"></span>**D3DXSHCQUAL \_ FASTLOWQUALITY**</span><span class="sxs-lookup"><span data-stu-id="97f55-107"><span id="D3DXSHCQUAL_FASTLOWQUALITY"></span><span id="d3dxshcqual_fastlowquality"></span>**D3DXSHCQUAL\_FASTLOWQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="97f55-108">資料壓縮很低，但可快速壓縮。</span><span class="sxs-lookup"><span data-stu-id="97f55-108">The data compression is low quality, but is fast to compress.</span></span>

</dd> <dt>

<span data-ttu-id="97f55-109"><span id="D3DXSHCQUAL_SLOWHIGHQUALITY"></span><span id="d3dxshcqual_slowhighquality"></span>**D3DXSHCQUAL \_ SLOWHIGHQUALITY**</span><span class="sxs-lookup"><span data-stu-id="97f55-109"><span id="D3DXSHCQUAL_SLOWHIGHQUALITY"></span><span id="d3dxshcqual_slowhighquality"></span>**D3DXSHCQUAL\_SLOWHIGHQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="97f55-110">資料壓縮具有高品質，但是壓縮速度較慢。</span><span class="sxs-lookup"><span data-stu-id="97f55-110">The data compression is high quality, but is slow to compress.</span></span>

</dd> <dt>

<span data-ttu-id="97f55-111"><span id="D3DXSHCQUAL_FORCE_DWORD"></span><span id="d3dxshcqual_force_dword"></span>**D3DXSHCQUAL \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="97f55-111"><span id="D3DXSHCQUAL_FORCE_DWORD"></span><span id="d3dxshcqual_force_dword"></span>**D3DXSHCQUAL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="97f55-112">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="97f55-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="97f55-113">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="97f55-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="97f55-114">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="97f55-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97f55-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="97f55-115">Requirements</span></span>



| <span data-ttu-id="97f55-116">需求</span><span class="sxs-lookup"><span data-stu-id="97f55-116">Requirement</span></span> | <span data-ttu-id="97f55-117">值</span><span class="sxs-lookup"><span data-stu-id="97f55-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97f55-118">標頭</span><span class="sxs-lookup"><span data-stu-id="97f55-118">Header</span></span><br/> | <dl> <span data-ttu-id="97f55-119"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="97f55-119"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97f55-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97f55-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97f55-121">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="97f55-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




