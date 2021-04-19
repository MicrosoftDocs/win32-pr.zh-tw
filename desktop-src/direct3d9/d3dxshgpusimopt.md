---
description: 描述將用於預先計算 Radiance 傳輸 (PRT) GPU 上的直接光源模擬之陰影 z 緩衝區的解析度。
ms.assetid: 05354328-9b6f-45f5-a913-47ede170b03f
title: 'D3DXSHGPUSIMOPT 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHGPUSIMOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a94845faf4c34657f486cfa371c5d41a12dc4336
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999980"
---
# <a name="d3dxshgpusimopt-enumeration"></a><span data-ttu-id="21836-103">D3DXSHGPUSIMOPT 列舉</span><span class="sxs-lookup"><span data-stu-id="21836-103">D3DXSHGPUSIMOPT enumeration</span></span>

<span data-ttu-id="21836-104">描述將用於預先計算 Radiance 傳輸 (PRT) GPU 上的直接光源模擬之陰影 z 緩衝區的解析度。</span><span class="sxs-lookup"><span data-stu-id="21836-104">Describes the resolution of the shadow z-buffer that will be used in Precomputed Radiance Transfer (PRT) direct lighting simulation on the GPU.</span></span> <span data-ttu-id="21836-105">您也可以指定較高品質的 z 緩衝區來減少直接光源模擬結果中的雜訊，雖然模擬會變慢。</span><span class="sxs-lookup"><span data-stu-id="21836-105">A higher quality z-buffer can also be specified to reduce noise in the results of the direct lighting simulation, although the simulation will be slower.</span></span>

## <a name="syntax"></a><span data-ttu-id="21836-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="21836-106">Syntax</span></span>


```C++
typedef enum D3DXSHGPUSIMOPT { 
  D3DXSHGPUSIMOPT_SHADOWRES256   = 1,
  D3DXSHGPUSIMOPT_SHADOWRES512   = 0,
  D3DXSHGPUSIMOPT_SHADOWRES1024  = 2,
  D3DXSHGPUSIMOPT_SHADOWRES2048  = 3,
  D3DXSHGPUSIMOPT_HIGHQUALITY    = 4,
  D3DXSHGPUSIMOPT_FORCE_DWORD    = 0x7fffffff
} D3DXSHGPUSIMOPT, *LPD3DXSHGPUSIMOPT;
```



## <a name="constants"></a><span data-ttu-id="21836-107">常數</span><span class="sxs-lookup"><span data-stu-id="21836-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="21836-108"><span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES256**</span><span class="sxs-lookup"><span data-stu-id="21836-108"><span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT\_SHADOWRES256**</span></span>
</dt> <dd>

<span data-ttu-id="21836-109">低解析度模擬。</span><span class="sxs-lookup"><span data-stu-id="21836-109">Low resolution simulation.</span></span> <span data-ttu-id="21836-110">在模擬中使用 256 x 256 圖元材質來編碼陰影 z 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="21836-110">A 256 x 256 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="21836-111"><span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES512**</span><span class="sxs-lookup"><span data-stu-id="21836-111"><span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT\_SHADOWRES512**</span></span>
</dt> <dd>

<span data-ttu-id="21836-112">中解析度模擬。</span><span class="sxs-lookup"><span data-stu-id="21836-112">Medium resolution simulation.</span></span> <span data-ttu-id="21836-113">在模擬中使用 512 x 512 圖元材質來編碼陰影 z 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="21836-113">A 512 x 512 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span> <span data-ttu-id="21836-114">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="21836-114">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="21836-115"><span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES1024**</span><span class="sxs-lookup"><span data-stu-id="21836-115"><span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT\_SHADOWRES1024**</span></span>
</dt> <dd>

<span data-ttu-id="21836-116">高解析度模擬。</span><span class="sxs-lookup"><span data-stu-id="21836-116">High resolution simulation.</span></span> <span data-ttu-id="21836-117">在模擬中使用 1024 x 1024 圖元材質來編碼陰影 z 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="21836-117">A 1024 x 1024 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="21836-118"><span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES2048**</span><span class="sxs-lookup"><span data-stu-id="21836-118"><span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT\_SHADOWRES2048**</span></span>
</dt> <dd>

<span data-ttu-id="21836-119">最高解析度的模擬。</span><span class="sxs-lookup"><span data-stu-id="21836-119">Highest resolution simulation.</span></span> <span data-ttu-id="21836-120">在模擬中使用 2048 x 2048 圖元材質來編碼陰影 z 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="21836-120">A 2048 x 2048 pixel texture is used in the simulation to encode the shadow z-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="21836-121"><span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT \_ HIGHQUALITY**</span><span class="sxs-lookup"><span data-stu-id="21836-121"><span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT\_HIGHQUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="21836-122">無論選取的解析度為何，模擬都是高精確度。</span><span class="sxs-lookup"><span data-stu-id="21836-122">The simulation is of high precision, regardless of the selected resolution.</span></span> <span data-ttu-id="21836-123">設定此值會減少直接光源模擬結果中的雜訊，但模擬的速度會較慢。</span><span class="sxs-lookup"><span data-stu-id="21836-123">Setting this value will reduce noise in the results of the direct lighting simulation, although the simulation will be slower.</span></span> <span data-ttu-id="21836-124">可以與其中一個解析度值結合。</span><span class="sxs-lookup"><span data-stu-id="21836-124">May be combined with one of the resolution values.</span></span>

</dd> <dt>

<span data-ttu-id="21836-125"><span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="21836-125"><span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="21836-126">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="21836-126">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="21836-127">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="21836-127">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="21836-128">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="21836-128">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21836-129">備註</span><span class="sxs-lookup"><span data-stu-id="21836-129">Remarks</span></span>

<span data-ttu-id="21836-130">您只能指定一個解決值，而且可以與高品質的值結合。</span><span class="sxs-lookup"><span data-stu-id="21836-130">Only one of the resolution values may be specified, and may be combined with the high-quality value.</span></span>

## <a name="requirements"></a><span data-ttu-id="21836-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="21836-131">Requirements</span></span>



| <span data-ttu-id="21836-132">需求</span><span class="sxs-lookup"><span data-stu-id="21836-132">Requirement</span></span> | <span data-ttu-id="21836-133">值</span><span class="sxs-lookup"><span data-stu-id="21836-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21836-134">標頭</span><span class="sxs-lookup"><span data-stu-id="21836-134">Header</span></span><br/> | <dl> <span data-ttu-id="21836-135"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="21836-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21836-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21836-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21836-137">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="21836-137">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




