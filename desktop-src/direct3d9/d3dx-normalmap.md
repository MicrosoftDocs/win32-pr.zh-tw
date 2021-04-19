---
description: 一般地圖產生常數。
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37985456e81b20af9b3e4396d10045d5e58c9b7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "107000037"
---
# <a name="d3dx_normalmap"></a><span data-ttu-id="19cc2-103">D3DX \_ NORMALMAP</span><span class="sxs-lookup"><span data-stu-id="19cc2-103">D3DX\_NORMALMAP</span></span>

<span data-ttu-id="19cc2-104">一般地圖產生常數。</span><span class="sxs-lookup"><span data-stu-id="19cc2-104">Normal maps generation constants.</span></span>



|                                     |                                                                                                                                                                                                    |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19cc2-105">\#定義</span><span class="sxs-lookup"><span data-stu-id="19cc2-105">\#define</span></span>                            | <span data-ttu-id="19cc2-106">Description</span><span class="sxs-lookup"><span data-stu-id="19cc2-106">Description</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="19cc2-107">D3DX \_ NORMALMAP \_ 鏡像 \_ U</span><span class="sxs-lookup"><span data-stu-id="19cc2-107">D3DX\_NORMALMAP\_MIRROR\_U</span></span>          | <span data-ttu-id="19cc2-108">表示 u 軸上材質邊緣的圖元應進行鏡像，而不會換行。</span><span class="sxs-lookup"><span data-stu-id="19cc2-108">Indicates that pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="19cc2-109">D3DX \_ NORMALMAP \_ 鏡像 \_ V</span><span class="sxs-lookup"><span data-stu-id="19cc2-109">D3DX\_NORMALMAP\_MIRROR\_V</span></span>          | <span data-ttu-id="19cc2-110">指出 v 軸上材質邊緣的圖元應進行鏡像，而不會換行。</span><span class="sxs-lookup"><span data-stu-id="19cc2-110">Indicates that pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="19cc2-111">D3DX \_ NORMALMAP \_ 鏡像</span><span class="sxs-lookup"><span data-stu-id="19cc2-111">D3DX\_NORMALMAP\_MIRROR</span></span>             | <span data-ttu-id="19cc2-112">與指定 D3DX \_ NORMALMAP \_ 鏡像 \_ U \| D3DX \_ NORMALMAP \_ 鏡像 V 相同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="19cc2-112">Same as specifying D3DX\_NORMALMAP\_MIRROR\_U \| D3DX\_NORMALMAP\_MIRROR\_V.</span></span>                                                                                                                       |
| <span data-ttu-id="19cc2-113">D3DX \_ NORMALMAP \_ INVERTSIGN</span><span class="sxs-lookup"><span data-stu-id="19cc2-113">D3DX\_NORMALMAP\_INVERTSIGN</span></span>         | <span data-ttu-id="19cc2-114">反轉每個標準的方向。</span><span class="sxs-lookup"><span data-stu-id="19cc2-114">Inverts the direction of each normal.</span></span>                                                                                                                                                              |
| <span data-ttu-id="19cc2-115">D3DX \_ NORMALMAP \_ COMPUTE \_ 遮蔽</span><span class="sxs-lookup"><span data-stu-id="19cc2-115">D3DX\_NORMALMAP\_COMPUTE\_OCCLUSION</span></span> | <span data-ttu-id="19cc2-116">計算每個圖元的遮蔽詞彙，然後將其編碼成 Alpha。</span><span class="sxs-lookup"><span data-stu-id="19cc2-116">Computes the per-pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="19cc2-117">Alpha 為1表示圖元不會以任何方式隱藏，而 Alpha 為0表示圖元完全隱藏。</span><span class="sxs-lookup"><span data-stu-id="19cc2-117">An alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 means that the pixel is completely obscured.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="19cc2-118">常數資訊</span><span class="sxs-lookup"><span data-stu-id="19cc2-118">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="19cc2-119">標頭</span><span class="sxs-lookup"><span data-stu-id="19cc2-119">Header</span></span>                   | <span data-ttu-id="19cc2-120">d3dx9tex。h</span><span class="sxs-lookup"><span data-stu-id="19cc2-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="19cc2-121">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="19cc2-121">Minimum operating system</span></span> | <span data-ttu-id="19cc2-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="19cc2-122">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="19cc2-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="19cc2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19cc2-124">D3DX 常數</span><span class="sxs-lookup"><span data-stu-id="19cc2-124">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[<span data-ttu-id="19cc2-125">**D3DXComputeNormalMap**</span><span class="sxs-lookup"><span data-stu-id="19cc2-125">**D3DXComputeNormalMap**</span></span>](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



