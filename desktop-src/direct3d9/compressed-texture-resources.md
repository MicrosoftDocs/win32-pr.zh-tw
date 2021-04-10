---
description: 紋理貼圖為繪製在三維圖形上的數位化影像，用來增加更多視覺上的細節。
ms.assetid: 0ea5cb07-a21a-4e2c-93e2-54966153bb8a
title: " (Direct3D 9) 的壓縮材質資源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9b7ef048c0e1780f92246a407863a4fa48a94a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191000"
---
# <a name="compressed-texture-resources-direct3d-9"></a><span data-ttu-id="78e1b-103"> (Direct3D 9) 的壓縮材質資源</span><span class="sxs-lookup"><span data-stu-id="78e1b-103">Compressed Texture Resources (Direct3D 9)</span></span>

<span data-ttu-id="78e1b-104">紋理貼圖為繪製在三維圖形上的數位化影像，用來增加更多視覺上的細節。</span><span class="sxs-lookup"><span data-stu-id="78e1b-104">Texture maps are digitized images drawn on three-dimensional shapes to add visual detail.</span></span> <span data-ttu-id="78e1b-105">他們在點陣化的過程中對應至這些圖形之上，並且整個過程可能會取用大量的系統匯流排及記憶體。</span><span class="sxs-lookup"><span data-stu-id="78e1b-105">They are mapped into these shapes during rasterization, and the process can consume large amounts of both the system bus and memory.</span></span> <span data-ttu-id="78e1b-106">若要減少紋理所使用的記憶體，Direct3D 支援壓縮紋理表面。</span><span class="sxs-lookup"><span data-stu-id="78e1b-106">To reduce the amount of memory consumed by textures, Direct3D supports the compression of texture surfaces.</span></span> <span data-ttu-id="78e1b-107">某些 Direct3D 裝置原生支援壓縮紋理表面。</span><span class="sxs-lookup"><span data-stu-id="78e1b-107">Some Direct3D devices support compressed texture surfaces natively.</span></span> <span data-ttu-id="78e1b-108">在這類裝置上，當您建立了一個壓縮表面並且將資料載入其中，該表面即可像任何其他的紋理表面一樣用於 Direct3D 之中。</span><span class="sxs-lookup"><span data-stu-id="78e1b-108">On such devices, when you have created a compressed surface and loaded the data into it, the surface can be used in Direct3D like any other texture surface.</span></span> <span data-ttu-id="78e1b-109">Direct3D 將會在該紋理對應至 3D 物件之上時，對其進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="78e1b-109">Direct3D handles decompression when the texture is mapped to a 3D object.</span></span>

## <a name="storage-efficiency-and-texture-compression"></a><span data-ttu-id="78e1b-110">儲存效率和材質壓縮</span><span class="sxs-lookup"><span data-stu-id="78e1b-110">Storage Efficiency and Texture Compression</span></span>

<span data-ttu-id="78e1b-111">所有紋理壓縮格式都是二的乘冪。</span><span class="sxs-lookup"><span data-stu-id="78e1b-111">All texture compression formats are powers of two.</span></span> <span data-ttu-id="78e1b-112">雖然這並不表示紋理一定是矩形，但實際上紋理的 x 值和 y 值的確都是二的乘冪。</span><span class="sxs-lookup"><span data-stu-id="78e1b-112">While this does not mean that a texture is necessarily square, it does mean that both x and y are powers of two.</span></span> <span data-ttu-id="78e1b-113">例如：一個原本是 512 x 128 位元組的紋理，在下一個 Mipmapping 將會縮小至 256 x 64，並且在每個層級以 2 的乘冪遞減。</span><span class="sxs-lookup"><span data-stu-id="78e1b-113">For example, if a texture is originally 512 by 128 bytes, the next mipmapping would be 256 by 64 and so on, with each level decreasing by a power of two.</span></span> <span data-ttu-id="78e1b-114">當紋理在較低的層級被篩選至 16 x 2 或 8 x 1 時，將會有未充分利用的位元存在，因為壓縮區塊一律都是 4 x 4 的材質區塊。</span><span class="sxs-lookup"><span data-stu-id="78e1b-114">At lower levels, where the texture is filtered to 16 by 2 and 8 by 1, there will be wasted bits because the compression block is always a 4 by 4 block of texels.</span></span> <span data-ttu-id="78e1b-115">未使用的區塊部分將會獲得填補。</span><span class="sxs-lookup"><span data-stu-id="78e1b-115">Unused portions of the block are padded.</span></span> <span data-ttu-id="78e1b-116">雖然在最低的層級時會有未充分利用的位元，整體增益仍然相當可觀。</span><span class="sxs-lookup"><span data-stu-id="78e1b-116">Although there are wasted bits at the lowest levels, the overall gain is still significant.</span></span> <span data-ttu-id="78e1b-117">理論上，最差的情況便是 2K x 1 的紋理 (2⁰ 乘冪)。</span><span class="sxs-lookup"><span data-stu-id="78e1b-117">The worst case is, in theory, a 2K by 1 texture (2⁰ power).</span></span> <span data-ttu-id="78e1b-118">在這種情況下，每一區塊只有一列像素獲得編碼，區塊的其餘部分都將不會被使用到。</span><span class="sxs-lookup"><span data-stu-id="78e1b-118">Here, only a single row of pixels is encoded per block, while the rest of the block is unused.</span></span>

## <a name="mixing-formats-within-a-single-texture"></a><span data-ttu-id="78e1b-119">在單一材質內混用格式</span><span class="sxs-lookup"><span data-stu-id="78e1b-119">Mixing Formats Within a Single Texture</span></span>

<span data-ttu-id="78e1b-120">請務必注意任何單一紋理都必須指定由 16 個材質組成的每個群組，資料將會以 64 位元或是 128 位元的方式儲存。</span><span class="sxs-lookup"><span data-stu-id="78e1b-120">It is important to note that any single texture must specify that its data is stored as 64 or 128 bits per group of 16 texels.</span></span> <span data-ttu-id="78e1b-121">如果有64位區塊（也就是 DXT1 格式）用於紋理，就可以在相同材質內的每個區塊上混用不透明和1位的 Alpha 格式。</span><span class="sxs-lookup"><span data-stu-id="78e1b-121">If 64-bit blocks - that is, format DXT1 - are used for the texture, it is possible to mix the opaque and 1-bit alpha formats on a per-block basis within the same texture.</span></span> <span data-ttu-id="78e1b-122">換句話說，色彩0和色彩1的不帶正負號整數量詞的比較， \_ \_ 是針對每個16材質的區塊來唯一執行。</span><span class="sxs-lookup"><span data-stu-id="78e1b-122">In other words, the comparison of the unsigned integer magnitude of color\_0 and color\_1 is performed uniquely for each block of 16 texels.</span></span>

<span data-ttu-id="78e1b-123">使用128位區塊之後，必須以明確的 (格式 DXT2 和 DXT3) 或插入模式來指定 Alpha 色板， (格式 DXT4 和 DXT5) 適用于整個材質。</span><span class="sxs-lookup"><span data-stu-id="78e1b-123">Once the 128-bit blocks are used, the alpha channel must be specified in either explicit (format DXT2 and DXT3) or interpolated mode (format DXT4 and DXT5) for the entire texture.</span></span> <span data-ttu-id="78e1b-124">同樣地，如果選取了插補模式 (format DXT4 和 DXT5) ，則可以使用八個插入 Alpha 或六個插補 Alpha 模式來逐一封鎖。</span><span class="sxs-lookup"><span data-stu-id="78e1b-124">As with color, when interpolated mode (format DXT4 and DXT5) is selected, then either eight interpolated alphas or six interpolated alphas mode can be used on a block-by-block basis.</span></span> <span data-ttu-id="78e1b-125">同樣地，Alpha \_ 0 和 Alpha 1 的量 \_ 值比較是依區塊逐一完成。</span><span class="sxs-lookup"><span data-stu-id="78e1b-125">Again the magnitude comparison of alpha\_0 and alpha\_1 is done uniquely on a block-by-block basis.</span></span>

<span data-ttu-id="78e1b-126">Direct3D 針對用於 3D 模型貼圖的表面，提供了壓縮的服務。</span><span class="sxs-lookup"><span data-stu-id="78e1b-126">Direct3D provides services to compress surfaces that are used for texturing 3D models.</span></span> <span data-ttu-id="78e1b-127">本章節提供了建立和管理壓縮紋理表面中資料的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="78e1b-127">This section provides information about creating and manipulating the data in a compressed texture surface.</span></span>

<span data-ttu-id="78e1b-128">下列主題包含資訊。</span><span class="sxs-lookup"><span data-stu-id="78e1b-128">Information is contained in the following topics.</span></span>

-   [<span data-ttu-id="78e1b-129"> (Direct3D 9) 的不透明和1位 Alpha 紋理 </span><span class="sxs-lookup"><span data-stu-id="78e1b-129">Opaque and 1-Bit Alpha Textures (Direct3D 9)</span></span>](opaque-and-1-bit-alpha-textures.md)
-   [<span data-ttu-id="78e1b-130">具有 Alpha 通道的材質 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="78e1b-130">Textures with Alpha Channels (Direct3D 9)</span></span>](textures-with-alpha-channels.md)
-   [<span data-ttu-id="78e1b-131"> (Direct3D 9) 的壓縮材質格式 </span><span class="sxs-lookup"><span data-stu-id="78e1b-131">Compressed Texture Formats (Direct3D 9)</span></span>](compressed-texture-formats.md)
-   [<span data-ttu-id="78e1b-132">使用 (Direct3D 9) 的壓縮紋理 </span><span class="sxs-lookup"><span data-stu-id="78e1b-132">Using Compressed Textures (Direct3D 9)</span></span>](using-compressed-textures.md)

## <a name="related-topics"></a><span data-ttu-id="78e1b-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="78e1b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78e1b-134">Direct3D 紋理</span><span class="sxs-lookup"><span data-stu-id="78e1b-134">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 



