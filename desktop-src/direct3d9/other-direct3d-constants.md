---
description: 其他 Direct3D 常數
ms.assetid: 3e314f73-2653-481a-ac7d-1ce7db0591e2
title: 其他 Direct3D 常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990dc0a2ef06850fb9fc0839fd7a0be361832d65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106986242"
---
# <a name="other-direct3d-constants"></a><span data-ttu-id="0b7a2-103">其他 Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="0b7a2-103">Other Direct3D Constants</span></span>

## <a name="sdk-version"></a><span data-ttu-id="0b7a2-104">SDK 版本</span><span class="sxs-lookup"><span data-stu-id="0b7a2-104">SDK Version</span></span>



|                     |
|---------------------|
| <span data-ttu-id="0b7a2-105">\#定義</span><span class="sxs-lookup"><span data-stu-id="0b7a2-105">\#define</span></span>            |
| <span data-ttu-id="0b7a2-106">D3D \_ SDK \_ 版本</span><span class="sxs-lookup"><span data-stu-id="0b7a2-106">D3D\_SDK\_VERSION</span></span>   |
| <span data-ttu-id="0b7a2-107">D3D9b \_ SDK \_ 版本</span><span class="sxs-lookup"><span data-stu-id="0b7a2-107">D3D9b\_SDK\_VERSION</span></span> |



 

<span data-ttu-id="0b7a2-108">這些 \# 定義是在 d3d9 中宣告。</span><span class="sxs-lookup"><span data-stu-id="0b7a2-108">These \#defines are declared in d3d9.h.</span></span>

## <a name="other-constants"></a><span data-ttu-id="0b7a2-109">其他常數</span><span class="sxs-lookup"><span data-stu-id="0b7a2-109">Other Constants</span></span>

<span data-ttu-id="0b7a2-110">下表列出內部使用的常數：</span><span class="sxs-lookup"><span data-stu-id="0b7a2-110">The following table lists constants that are used internally:</span></span>



|                                       |                                                   |                                                                    |
|---------------------------------------|---------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="0b7a2-111">\#定義</span><span class="sxs-lookup"><span data-stu-id="0b7a2-111">\#define</span></span>                              | <span data-ttu-id="0b7a2-112">值</span><span class="sxs-lookup"><span data-stu-id="0b7a2-112">Value</span></span>                                             | <span data-ttu-id="0b7a2-113">描述</span><span class="sxs-lookup"><span data-stu-id="0b7a2-113">Description</span></span>                                                        |
| <span data-ttu-id="0b7a2-114">D3D \_ 最大 \_ 同時 \_ RENDERTARGETS</span><span class="sxs-lookup"><span data-stu-id="0b7a2-114">D3D\_MAX\_SIMULTANEOUS\_RENDERTARGETS</span></span> | <span data-ttu-id="0b7a2-115">4</span><span class="sxs-lookup"><span data-stu-id="0b7a2-115">4</span></span>                                                 | <span data-ttu-id="0b7a2-116">Rendertargets 數目上限。</span><span class="sxs-lookup"><span data-stu-id="0b7a2-116">The maximum number of rendertargets.</span></span>                               |
| <span data-ttu-id="0b7a2-117">D3DDMAPSAMPLER</span><span class="sxs-lookup"><span data-stu-id="0b7a2-117">D3DDMAPSAMPLER</span></span>                        | <span data-ttu-id="0b7a2-118">256</span><span class="sxs-lookup"><span data-stu-id="0b7a2-118">256</span></span>                                               | <span data-ttu-id="0b7a2-119">置換地圖樣本的最大數目。</span><span class="sxs-lookup"><span data-stu-id="0b7a2-119">The maximum number of displacement map samples.</span></span>                    |
| <span data-ttu-id="0b7a2-120">D3DDP \_ MAXTEXCOORD</span><span class="sxs-lookup"><span data-stu-id="0b7a2-120">D3DDP\_MAXTEXCOORD</span></span>                    | <span data-ttu-id="0b7a2-121">8</span><span class="sxs-lookup"><span data-stu-id="0b7a2-121">8</span></span>                                                 | <span data-ttu-id="0b7a2-122">材質座標的最大數目。</span><span class="sxs-lookup"><span data-stu-id="0b7a2-122">The maximum number of texture coordinates.</span></span>                         |
| <span data-ttu-id="0b7a2-123">MAXD3DDECLLENGTH</span><span class="sxs-lookup"><span data-stu-id="0b7a2-123">MAXD3DDECLLENGTH</span></span>                      | <span data-ttu-id="0b7a2-124">64 (不包含 "end" 標記頂點元素) </span><span class="sxs-lookup"><span data-stu-id="0b7a2-124">64 (does not include "end" marker vertex element)</span></span> | <span data-ttu-id="0b7a2-125">頂點宣告中的元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="0b7a2-125">Maximum number of elements in a vertex declaration.</span></span>                |
| <span data-ttu-id="0b7a2-126">MAXD3DDECLUSAGEINDEX</span><span class="sxs-lookup"><span data-stu-id="0b7a2-126">MAXD3DDECLUSAGEINDEX</span></span>                  | <span data-ttu-id="0b7a2-127">15</span><span class="sxs-lookup"><span data-stu-id="0b7a2-127">15</span></span>                                                | <span data-ttu-id="0b7a2-128">可以在頂點宣告中使用的最大索引 (0-15) 。</span><span class="sxs-lookup"><span data-stu-id="0b7a2-128">The maximum index (0-15) that can be used in a vertex declaration.</span></span> |



 

<span data-ttu-id="0b7a2-129">這些 \# 定義是在 d3d9types 中宣告。</span><span class="sxs-lookup"><span data-stu-id="0b7a2-129">These \#defines are declared in d3d9types.h.</span></span>

## <a name="constant-information"></a><span data-ttu-id="0b7a2-130">常數資訊</span><span class="sxs-lookup"><span data-stu-id="0b7a2-130">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="0b7a2-131">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="0b7a2-131">Minimum operating system</span></span> | <span data-ttu-id="0b7a2-132">Windows 98</span><span class="sxs-lookup"><span data-stu-id="0b7a2-132">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0b7a2-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b7a2-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b7a2-134">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="0b7a2-134">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



