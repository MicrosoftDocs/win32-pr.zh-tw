---
title: DDS 磁片區材質範例
description: 若為磁片區材質，請使用 DDSCAPS \_ COMPLEX、DDSCAPS2 \_ VOLUME、DDSD \_ DEPTH、flags 及 set 和 dwDepth。 磁片區材質是 Direct3D 9 標準材質的延伸;您可以使用或不使用 mipmap 來定義磁片區材質。
ms.assetid: c1675a6d-129a-4e95-993f-e1be905781cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d82faa8041f2b5c99ef57ee2386ff5de84d787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968639"
---
# <a name="dds-volume-texture-example"></a><span data-ttu-id="73158-104">DDS 磁片區材質範例</span><span class="sxs-lookup"><span data-stu-id="73158-104">DDS Volume Texture Example</span></span>

<span data-ttu-id="73158-105">若為磁片區材質，請使用 DDSCAPS \_ COMPLEX、DDSCAPS2 \_ VOLUME、DDSD \_ DEPTH、flags 及 set 和 dwDepth。</span><span class="sxs-lookup"><span data-stu-id="73158-105">For a volume texture, use the DDSCAPS\_COMPLEX, DDSCAPS2\_VOLUME, DDSD\_DEPTH, flags and set and dwDepth.</span></span> <span data-ttu-id="73158-106">磁片區材質是 Direct3D 9 標準材質的延伸;您可以使用或不使用 mipmap 來定義磁片區材質。</span><span class="sxs-lookup"><span data-stu-id="73158-106">A volume texture is an extension of a standard texture for Direct3D 9; a volume texture is can be defined with or without mipmaps.</span></span>

<span data-ttu-id="73158-107">針對沒有 mipmap 的磁片區，每個深度配量都會依序寫入至檔案。</span><span class="sxs-lookup"><span data-stu-id="73158-107">For volumes without mipmaps, each depth slice is written to the file in order.</span></span> <span data-ttu-id="73158-108">如果包含 mipmap，則會將指定 mipmap 層級的所有深度配量一起寫入，其中每個層級都包含與上一個層級一半相同的配量，最少為1。</span><span class="sxs-lookup"><span data-stu-id="73158-108">If mipmaps are included, all depth slices for a given mipmap level are written together, with each level containing half as many slices as the previous level with a minimum of 1.</span></span>

<span data-ttu-id="73158-109">例如，使用 R8G8B8 像素格式的64到64的磁片區對應 (3 個位元組的每圖元) ，而且所有 mipmap 層級都會包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="73158-109">For example, a 64-by-64-by-4 volume map using a pixel format of R8G8B8 (3 bytes per pixel) with all mipmap levels would contain the following:</span></span>



| <span data-ttu-id="73158-110">DDS 元件</span><span class="sxs-lookup"><span data-stu-id="73158-110">DDS Components</span></span>                      | <span data-ttu-id="73158-111">\# 位元組</span><span class="sxs-lookup"><span data-stu-id="73158-111">\# Bytes</span></span>    |
|-------------------------------------|-------------|
| <span data-ttu-id="73158-112">header</span><span class="sxs-lookup"><span data-stu-id="73158-112">header</span></span>                              | <span data-ttu-id="73158-113">128位元組</span><span class="sxs-lookup"><span data-stu-id="73158-113">128 bytes</span></span>   |
| <span data-ttu-id="73158-114">四個主要影像的 64-64 配量1。</span><span class="sxs-lookup"><span data-stu-id="73158-114">64-by-64 slice 1 of 4 main image.</span></span>   | <span data-ttu-id="73158-115">12288位元組</span><span class="sxs-lookup"><span data-stu-id="73158-115">12288 bytes</span></span> |
| <span data-ttu-id="73158-116">四個主要影像的 64-64 配量2。</span><span class="sxs-lookup"><span data-stu-id="73158-116">64-by-64 slice 2 of 4 main image.</span></span>   | <span data-ttu-id="73158-117">12288位元組</span><span class="sxs-lookup"><span data-stu-id="73158-117">12288 bytes</span></span> |
| <span data-ttu-id="73158-118">四個主要影像的 64-64 配量3。</span><span class="sxs-lookup"><span data-stu-id="73158-118">64-by-64 slice 3 of 4 main image.</span></span>   | <span data-ttu-id="73158-119">12288位元組</span><span class="sxs-lookup"><span data-stu-id="73158-119">12288 bytes</span></span> |
| <span data-ttu-id="73158-120">四個主要映射的 64-64 配量4。</span><span class="sxs-lookup"><span data-stu-id="73158-120">64-by-64 slice 4 of 4 main image.</span></span>   | <span data-ttu-id="73158-121">12288位元組</span><span class="sxs-lookup"><span data-stu-id="73158-121">12288 bytes</span></span> |
| <span data-ttu-id="73158-122">32-32 mipmap 影像中的配量第1個磁區。</span><span class="sxs-lookup"><span data-stu-id="73158-122">32-by-32 slice 1 of 2 mipmap image.</span></span> | <span data-ttu-id="73158-123">3072位元組</span><span class="sxs-lookup"><span data-stu-id="73158-123">3072 bytes</span></span>  |
| <span data-ttu-id="73158-124">32-32 mipmap 影像中的配量2。</span><span class="sxs-lookup"><span data-stu-id="73158-124">32-by-32 slice 2 of 2 mipmap image.</span></span> | <span data-ttu-id="73158-125">3072位元組</span><span class="sxs-lookup"><span data-stu-id="73158-125">3072 bytes</span></span>  |
| <span data-ttu-id="73158-126">1個 mipmap 影像的 16 x 16 磁區1。</span><span class="sxs-lookup"><span data-stu-id="73158-126">16-by-16 slice 1 of 1 mipmap image.</span></span> | <span data-ttu-id="73158-127">768位元組</span><span class="sxs-lookup"><span data-stu-id="73158-127">768 bytes</span></span>   |
| <span data-ttu-id="73158-128">1個 mipmap 影像的8到8個配量1。</span><span class="sxs-lookup"><span data-stu-id="73158-128">8-by-8 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="73158-129">192位元組</span><span class="sxs-lookup"><span data-stu-id="73158-129">192 bytes</span></span>   |
| <span data-ttu-id="73158-130">1 mipmap 映射的4到4配量1。</span><span class="sxs-lookup"><span data-stu-id="73158-130">4-by-4 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="73158-131">48位元組</span><span class="sxs-lookup"><span data-stu-id="73158-131">48 bytes</span></span>    |
| <span data-ttu-id="73158-132">1個 mipmap 影像的2到2個配量1。</span><span class="sxs-lookup"><span data-stu-id="73158-132">2-by-2 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="73158-133">12個位元組</span><span class="sxs-lookup"><span data-stu-id="73158-133">12 bytes</span></span>    |
| <span data-ttu-id="73158-134">1 mipmap 影像的1到1配量1。</span><span class="sxs-lookup"><span data-stu-id="73158-134">1-by-1 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="73158-135">3個位元組</span><span class="sxs-lookup"><span data-stu-id="73158-135">3 bytes</span></span>     |



 

<span data-ttu-id="73158-136">請注意，最小的 mipmap 層級只有3個位元組，因為 bitcount 是24，而且此層級沒有額外的壓縮。</span><span class="sxs-lookup"><span data-stu-id="73158-136">Note that the smallest mipmap level is only 3 bytes because the bitcount is 24 and there is no added compression at this level.</span></span>

<span data-ttu-id="73158-137">已在 DirectX 8 中新增對磁片區紋理的支援。</span><span class="sxs-lookup"><span data-stu-id="73158-137">Support for volume textures was added in DirectX 8.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73158-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="73158-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73158-139">DDS 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="73158-139">Programming Guide for DDS</span></span>](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




