---
description: 一般地圖產生常數。
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4263237cedf92a5e322f2fe139e9afe2297f6b9b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342853"
---
# <a name="d3dx_normalmap"></a><span data-ttu-id="29f6b-103">D3DX \_ NORMALMAP</span><span class="sxs-lookup"><span data-stu-id="29f6b-103">D3DX\_NORMALMAP</span></span>

<span data-ttu-id="29f6b-104">一般地圖產生常數。</span><span class="sxs-lookup"><span data-stu-id="29f6b-104">Normal maps generation constants.</span></span>



| <span data-ttu-id="29f6b-105">\#定義</span><span class="sxs-lookup"><span data-stu-id="29f6b-105">\#define</span></span>                            | <span data-ttu-id="29f6b-106">Description</span><span class="sxs-lookup"><span data-stu-id="29f6b-106">Description</span></span>                                                                                                                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29f6b-107">D3DX \_ NORMALMAP \_ 鏡像 \_ U</span><span class="sxs-lookup"><span data-stu-id="29f6b-107">D3DX\_NORMALMAP\_MIRROR\_U</span></span>          | <span data-ttu-id="29f6b-108">表示 u 軸上材質邊緣的圖元應進行鏡像，而不會換行。</span><span class="sxs-lookup"><span data-stu-id="29f6b-108">Indicates that pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="29f6b-109">D3DX \_ NORMALMAP \_ 鏡像 \_ V</span><span class="sxs-lookup"><span data-stu-id="29f6b-109">D3DX\_NORMALMAP\_MIRROR\_V</span></span>          | <span data-ttu-id="29f6b-110">指出 v 軸上材質邊緣的圖元應進行鏡像，而不會換行。</span><span class="sxs-lookup"><span data-stu-id="29f6b-110">Indicates that pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="29f6b-111">D3DX \_ NORMALMAP \_ 鏡像</span><span class="sxs-lookup"><span data-stu-id="29f6b-111">D3DX\_NORMALMAP\_MIRROR</span></span>             | <span data-ttu-id="29f6b-112">與指定 D3DX \_ NORMALMAP \_ 鏡像 \_ U \| D3DX \_ NORMALMAP \_ 鏡像 V 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="29f6b-112">Same as specifying D3DX\_NORMALMAP\_MIRROR\_U \| D3DX\_NORMALMAP\_MIRROR\_V.</span></span>                                                                                                                       |
| <span data-ttu-id="29f6b-113">D3DX \_ NORMALMAP \_ INVERTSIGN</span><span class="sxs-lookup"><span data-stu-id="29f6b-113">D3DX\_NORMALMAP\_INVERTSIGN</span></span>         | <span data-ttu-id="29f6b-114">反轉每個標準的方向。</span><span class="sxs-lookup"><span data-stu-id="29f6b-114">Inverts the direction of each normal.</span></span>                                                                                                                                                              |
| <span data-ttu-id="29f6b-115">D3DX \_ NORMALMAP \_ COMPUTE \_ 遮蔽</span><span class="sxs-lookup"><span data-stu-id="29f6b-115">D3DX\_NORMALMAP\_COMPUTE\_OCCLUSION</span></span> | <span data-ttu-id="29f6b-116">計算每個圖元的遮蔽詞彙，然後將其編碼成 Alpha。</span><span class="sxs-lookup"><span data-stu-id="29f6b-116">Computes the per-pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="29f6b-117">Alpha 為1表示圖元不會以任何方式隱藏，而 Alpha 為0表示圖元完全隱藏。</span><span class="sxs-lookup"><span data-stu-id="29f6b-117">An alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 means that the pixel is completely obscured.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="29f6b-118">常數資訊</span><span class="sxs-lookup"><span data-stu-id="29f6b-118">Constant Information</span></span>



| <span data-ttu-id="29f6b-119">需求</span><span class="sxs-lookup"><span data-stu-id="29f6b-119">Requirement</span></span>                         | <span data-ttu-id="29f6b-120">值</span><span class="sxs-lookup"><span data-stu-id="29f6b-120">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="29f6b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="29f6b-121">Header</span></span>                   | <span data-ttu-id="29f6b-122">d3dx9tex。h</span><span class="sxs-lookup"><span data-stu-id="29f6b-122">d3dx9tex.h</span></span> |
| <span data-ttu-id="29f6b-123">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="29f6b-123">Minimum operating system</span></span> | <span data-ttu-id="29f6b-124">Windows 98</span><span class="sxs-lookup"><span data-stu-id="29f6b-124">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="29f6b-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="29f6b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29f6b-126">D3DX 常數</span><span class="sxs-lookup"><span data-stu-id="29f6b-126">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[<span data-ttu-id="29f6b-127">**D3DXComputeNormalMap**</span><span class="sxs-lookup"><span data-stu-id="29f6b-127">**D3DXComputeNormalMap**</span></span>](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



