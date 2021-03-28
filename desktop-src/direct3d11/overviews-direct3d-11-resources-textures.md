---
title: 紋理
description: 本節說明 Direct3D 11 中所使用的材質，以及一般案例的工作架構檔連結。
ms.assetid: ec833431-a7b4-4aea-91c8-e99b718de2c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc3909f354b0709e82ffd2bdffafe6cdb35516
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183821"
---
# <a name="textures"></a><span data-ttu-id="01cc6-103">紋理</span><span class="sxs-lookup"><span data-stu-id="01cc6-103">Textures</span></span>

<span data-ttu-id="01cc6-104">材質會儲存材質資訊。</span><span class="sxs-lookup"><span data-stu-id="01cc6-104">A texture stores texel information.</span></span> <span data-ttu-id="01cc6-105">本節說明 Direct3D 11 中所使用的材質，以及一般案例的工作架構檔連結。</span><span class="sxs-lookup"><span data-stu-id="01cc6-105">This section describes textures that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="01cc6-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="01cc6-106">In this section</span></span>



| <span data-ttu-id="01cc6-107">主題</span><span class="sxs-lookup"><span data-stu-id="01cc6-107">Topic</span></span>                                                                                                    | <span data-ttu-id="01cc6-108">描述</span><span class="sxs-lookup"><span data-stu-id="01cc6-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01cc6-109">Direct3D 11 中的材質簡介</span><span class="sxs-lookup"><span data-stu-id="01cc6-109">Introduction To Textures in Direct3D 11</span></span>](overviews-direct3d-11-resources-textures-intro.md)<br/> | <span data-ttu-id="01cc6-110">紋理資源是設計來儲存紋素的結構化資料集合。</span><span class="sxs-lookup"><span data-stu-id="01cc6-110">A texture resource is a structured collection of data designed to store texels.</span></span> <span data-ttu-id="01cc6-111">紋素代表管線可讀取或寫入的最小紋理單位。</span><span class="sxs-lookup"><span data-stu-id="01cc6-111">A texel represents the smallest unit of a texture that can be read or written to by the pipeline.</span></span> <span data-ttu-id="01cc6-112">和緩衝區不同的是，紋理可依紋理樣本篩選，由著色器單位讀取。</span><span class="sxs-lookup"><span data-stu-id="01cc6-112">Unlike buffers, textures can be filtered by texture samplers as they are read by shader units.</span></span> <span data-ttu-id="01cc6-113">紋理類型會影響篩選紋理的方式。</span><span class="sxs-lookup"><span data-stu-id="01cc6-113">The type of texture impacts how the texture is filtered.</span></span> <span data-ttu-id="01cc6-114">每個材質都包含1至4個元件，以 DXGI 格式列舉所定義的其中一個 DXGI 格式來排列 \_ 。</span><span class="sxs-lookup"><span data-stu-id="01cc6-114">Each texel contains 1 to 4 components, arranged in one of the DXGI formats defined by the DXGI\_FORMAT enumeration.</span></span><br/> |
| [<span data-ttu-id="01cc6-115">Direct3D 11 中的材質區塊壓縮</span><span class="sxs-lookup"><span data-stu-id="01cc6-115">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)<br/>      | <span data-ttu-id="01cc6-116">紋理的區塊壓縮 (BC) 支援在 Direct3D 11 中已進行擴充，內含 BC6H 和 BC7 演算法。</span><span class="sxs-lookup"><span data-stu-id="01cc6-116">Block Compression (BC) support for textures has been extended in Direct3D 11 to include the BC6H and BC7 algorithms.</span></span> <span data-ttu-id="01cc6-117">BC6H 支援高動態範圍色彩來源資料，而 BC7 使用較少的標準 RGB 來源資料成品，提供高於平均品質的壓縮。</span><span class="sxs-lookup"><span data-stu-id="01cc6-117">BC6H supports high-dynamic range color source data, and BC7 provides better-than-average quality compression with less artifacts for standard RGB source data.</span></span><br/>                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="01cc6-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="01cc6-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01cc6-119">如何：建立材質</span><span class="sxs-lookup"><span data-stu-id="01cc6-119">How to: Create a Texture</span></span>](overviews-direct3d-11-resources-textures-create.md)
</dt> <dt>

[<span data-ttu-id="01cc6-120">如何：以程式設計方式初始化材質</span><span class="sxs-lookup"><span data-stu-id="01cc6-120">How to: Initialize a Texture Programmatically</span></span>](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
</dt> <dt>

[<span data-ttu-id="01cc6-121">如何：從檔案初始化材質</span><span class="sxs-lookup"><span data-stu-id="01cc6-121">How to: Initialize a Texture From a File</span></span>](overviews-direct3d-11-resources-textures-how-to.md)
</dt> <dt>

[<span data-ttu-id="01cc6-122">資源</span><span class="sxs-lookup"><span data-stu-id="01cc6-122">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





