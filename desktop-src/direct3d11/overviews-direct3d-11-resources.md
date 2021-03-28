---
title: 資源
description: 本節說明 Direct3D 11 資源的各個層面。
ms.assetid: 5b8b1198-73ed-4058-9fc6-a1c43902d732
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9ed73d81d2521fe97b36e6bfc8d71e387f8c9c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104024352"
---
# <a name="resources"></a><span data-ttu-id="2783f-103">資源</span><span class="sxs-lookup"><span data-stu-id="2783f-103">Resources</span></span>

<span data-ttu-id="2783f-104">資源將資料提供給管線並定義您場景期間轉譯的項目。</span><span class="sxs-lookup"><span data-stu-id="2783f-104">Resources provide data to the pipeline and define what is rendered during your scene.</span></span> <span data-ttu-id="2783f-105">從您的遊戲媒體載入或在執行階段動態建立資源。</span><span class="sxs-lookup"><span data-stu-id="2783f-105">Resources can be loaded from your game media or created dynamically at run time.</span></span> <span data-ttu-id="2783f-106">通常，資源包括紋理資料、頂點資料和著色器資料。</span><span class="sxs-lookup"><span data-stu-id="2783f-106">Typically, resources include texture data, vertex data, and shader data.</span></span> <span data-ttu-id="2783f-107">大部分的 Direct3D 應用程式會在其存留期內廣泛地建立和終結資源。</span><span class="sxs-lookup"><span data-stu-id="2783f-107">Most Direct3D applications create and destroy resources extensively throughout their lifespan.</span></span> <span data-ttu-id="2783f-108">本節說明 Direct3D 11 資源的各個層面。</span><span class="sxs-lookup"><span data-stu-id="2783f-108">This section describes aspects of Direct3D 11 resources.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="2783f-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="2783f-109">In this section</span></span>



| <span data-ttu-id="2783f-110">主題</span><span class="sxs-lookup"><span data-stu-id="2783f-110">Topic</span></span>                                                                                             | <span data-ttu-id="2783f-111">描述</span><span class="sxs-lookup"><span data-stu-id="2783f-111">Description</span></span>                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2783f-112">Direct3D 11 中的資源簡介</span><span class="sxs-lookup"><span data-stu-id="2783f-112">Introduction to a Resource in Direct3D 11</span></span>](overviews-direct3d-11-resources-intro.md)<br/> | <span data-ttu-id="2783f-113">本主題介紹 Direct3D 資源，例如緩衝區和紋理。</span><span class="sxs-lookup"><span data-stu-id="2783f-113">This topic introduces Direct3D resources such as buffers and textures.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="2783f-114">資源類型</span><span class="sxs-lookup"><span data-stu-id="2783f-114">Types of Resources</span></span>](overviews-direct3d-11-resources-types.md)<br/>                        | <span data-ttu-id="2783f-115">本主題說明 Direct3D 10 中的資源類型，以及 Direct3D 11 中的新類型，包括結構化緩衝區和可寫入的材質和緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2783f-115">This topic describes the types of resources from Direct3D 10, as well as new types in Direct3D 11 including structured buffers and writable textures and buffers.</span></span><br/>                                                                       |
| [<span data-ttu-id="2783f-116">資源限制</span><span class="sxs-lookup"><span data-stu-id="2783f-116">Resource Limits</span></span>](overviews-direct3d-11-resources-limits.md)<br/>                          | <span data-ttu-id="2783f-117">本主題包含 Direct3D 11 支援的資源清單 (特別是 [功能等級](overviews-direct3d-11-devices-downlevel-intro.md) 11 或2.x 硬體) 。</span><span class="sxs-lookup"><span data-stu-id="2783f-117">This topic contains a list of resources that Direct3D 11 supports (specifically [feature level](overviews-direct3d-11-devices-downlevel-intro.md) 11 or 9.x hardware).</span></span><br/>                                 |
| [<span data-ttu-id="2783f-118">子資源</span><span class="sxs-lookup"><span data-stu-id="2783f-118">Subresources</span></span>](overviews-direct3d-11-resources-subresources.md)<br/>                       | <span data-ttu-id="2783f-119">本主題說明紋理子資源或資源的部分。</span><span class="sxs-lookup"><span data-stu-id="2783f-119">This topic describes texture subresources, or portions of a resource.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="2783f-120">緩衝區</span><span class="sxs-lookup"><span data-stu-id="2783f-120">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)<br/>                                 | <span data-ttu-id="2783f-121">緩衝區包含的資料用於描述幾何、編制幾何資訊的索引，以及著色器常數。</span><span class="sxs-lookup"><span data-stu-id="2783f-121">Buffers contain data that is used for describing geometry, indexing geometry information, and shader constants.</span></span> <span data-ttu-id="2783f-122">本節說明 Direct3D 11 中使用的緩衝區，以及一般案例的工作式檔連結。</span><span class="sxs-lookup"><span data-stu-id="2783f-122">This section describes buffers that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span><br/> |
| [<span data-ttu-id="2783f-123">紋理</span><span class="sxs-lookup"><span data-stu-id="2783f-123">Textures</span></span>](overviews-direct3d-11-resources-textures.md)<br/>                               | <span data-ttu-id="2783f-124">本節說明 Direct3D 11 中所使用的材質，以及一般案例的工作架構檔連結。</span><span class="sxs-lookup"><span data-stu-id="2783f-124">This section describes textures that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="2783f-125">浮點規則</span><span class="sxs-lookup"><span data-stu-id="2783f-125">Floating-point rules</span></span>](floating-point-rules.md)<br/>                                       | <span data-ttu-id="2783f-126">Direct3D 11 支援數個浮點數標記法。</span><span class="sxs-lookup"><span data-stu-id="2783f-126">Direct3D 11 supports several floating-point representations.</span></span> <span data-ttu-id="2783f-127">所有浮點數計算運作都在 IEEE 754 32 位元單精確度浮點數規則的定義子集下運作。</span><span class="sxs-lookup"><span data-stu-id="2783f-127">All floating-point computations operate under a defined subset of the IEEE 754 32-bit single precision floating-point rules.</span></span><br/>                                               |
| [<span data-ttu-id="2783f-128">磚資源</span><span class="sxs-lookup"><span data-stu-id="2783f-128">Tiled resources</span></span>](tiled-resources.md)<br/>                                                 | <span data-ttu-id="2783f-129">您可以將已平平的資源視為大型邏輯資源，其使用少量的實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="2783f-129">Tiled resources can be thought of as large logical resources that use small amounts of physical memory.</span></span><br/>                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="2783f-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="2783f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2783f-131">Direct3D 11 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="2783f-131">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

 





