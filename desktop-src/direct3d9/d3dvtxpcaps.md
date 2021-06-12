---
description: 瞭解一或多個旗標的組合，以控制裝置在 D3DVTXPCAPS 常數中的建立行為。
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b544f3e4a69de23607366832aca110e42c61d6d
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011081"
---
# <a name="d3dvtxpcaps"></a><span data-ttu-id="b5a1b-103">D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="b5a1b-103">D3DVTXPCAPS</span></span>

<span data-ttu-id="b5a1b-104">一或多個旗標的組合，可控制裝置的建立行為。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-104">A combination of one or more flags that control the device create behavior.</span></span>



| <span data-ttu-id="b5a1b-105">\#定義</span><span class="sxs-lookup"><span data-stu-id="b5a1b-105">\#define</span></span>                                | <span data-ttu-id="b5a1b-106">Description</span><span class="sxs-lookup"><span data-stu-id="b5a1b-106">Description</span></span>                                                                                                                                                                                        |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a1b-107">D3DVTXPCAPS \_ DIRECTIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="b5a1b-107">D3DVTXPCAPS\_DIRECTIONALLIGHTS</span></span>          | <span data-ttu-id="b5a1b-108">裝置可以進行方向燈。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-108">Device can do directional lights.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="b5a1b-109">D3DVTXPCAPS \_ LOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="b5a1b-109">D3DVTXPCAPS\_LOCALVIEWER</span></span>                | <span data-ttu-id="b5a1b-110">裝置可以進行本機檢視器。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-110">Device can do local viewer.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="b5a1b-111">D3DVTXPCAPS \_ MATERIALSOURCE7</span><span class="sxs-lookup"><span data-stu-id="b5a1b-111">D3DVTXPCAPS\_MATERIALSOURCE7</span></span>            | <span data-ttu-id="b5a1b-112">設定此上限時，裝置會支援色彩材質狀態： D3DRS \_ AMBIENTMATERIALSOURCE、D3DRS \_ DIFFUSEMATERIALSOURCE、D3DRS \_ EMISSIVEMATERIALSOURCE 和 D3DRS \_ SPECULARMATERIALSOURCE。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-112">When this cap is set, the device supports the color material states: D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="b5a1b-113">D3DVTXPCAPS \_ NO \_ TEXGEN \_ NONLOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="b5a1b-113">D3DVTXPCAPS\_NO\_TEXGEN\_NONLOCALVIEWER</span></span> | <span data-ttu-id="b5a1b-114">裝置不支援在非本機檢視器模式中產生紋理。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-114">Device does not support texture generation in non-local viewer mode.</span></span>                                                                                                                               |
| <span data-ttu-id="b5a1b-115">D3DVTXPCAPS \_ POSITIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="b5a1b-115">D3DVTXPCAPS\_POSITIONALLIGHTS</span></span>           | <span data-ttu-id="b5a1b-116">裝置可以進行位置燈光 (包括點和點) 。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-116">Device can do positional lights (includes point and spot).</span></span>                                                                                                                                         |
| <span data-ttu-id="b5a1b-117">D3DVTXPCAPS \_ TEXGEN</span><span class="sxs-lookup"><span data-stu-id="b5a1b-117">D3DVTXPCAPS\_TEXGEN</span></span>                     | <span data-ttu-id="b5a1b-118">裝置可以進行 texgen。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-118">Device can do texgen.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="b5a1b-119">D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="b5a1b-119">D3DVTXPCAPS\_TEXGEN\_SPHEREMAP</span></span>          | <span data-ttu-id="b5a1b-120">裝置支援 D3DTSS \_ TCI \_ SPHEREMAP。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-120">Device supports D3DTSS\_TCI\_SPHEREMAP.</span></span>                                                                                                                                                            |
| <span data-ttu-id="b5a1b-121">D3DVTXPCAPS \_ 補間</span><span class="sxs-lookup"><span data-stu-id="b5a1b-121">D3DVTXPCAPS\_TWEENING</span></span>                   | <span data-ttu-id="b5a1b-122">裝置可以進行頂點補間。</span><span class="sxs-lookup"><span data-stu-id="b5a1b-122">Device can do vertex tweening.</span></span>                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="b5a1b-123">常數資訊</span><span class="sxs-lookup"><span data-stu-id="b5a1b-123">Constant Information</span></span>



| <span data-ttu-id="b5a1b-124">需求</span><span class="sxs-lookup"><span data-stu-id="b5a1b-124">Requirement</span></span>                         | <span data-ttu-id="b5a1b-125">值</span><span class="sxs-lookup"><span data-stu-id="b5a1b-125">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="b5a1b-126">標頭</span><span class="sxs-lookup"><span data-stu-id="b5a1b-126">Header</span></span>                   | <span data-ttu-id="b5a1b-127">d3d9caps。h</span><span class="sxs-lookup"><span data-stu-id="b5a1b-127">d3d9caps.h</span></span> |
| <span data-ttu-id="b5a1b-128">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="b5a1b-128">Minimum operating system</span></span> | <span data-ttu-id="b5a1b-129">Windows 98</span><span class="sxs-lookup"><span data-stu-id="b5a1b-129">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b5a1b-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="b5a1b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5a1b-131">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="b5a1b-131">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



