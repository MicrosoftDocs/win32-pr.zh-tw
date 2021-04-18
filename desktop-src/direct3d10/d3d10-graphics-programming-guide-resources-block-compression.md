---
description: 區塊壓縮是一種用於降低紋理大小的紋理壓縮技術。
ms.assetid: add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5
title: " (Direct3D 10) 封鎖壓縮"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fcfb4bc91256415ab23686b7333df7d21df335d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551857"
---
# <a name="block-compression-direct3d-10"></a><span data-ttu-id="6933c-103"> (Direct3D 10) 封鎖壓縮</span><span class="sxs-lookup"><span data-stu-id="6933c-103">Block Compression (Direct3D 10)</span></span>

<span data-ttu-id="6933c-104">區塊壓縮是一種用於降低紋理大小的紋理壓縮技術。</span><span class="sxs-lookup"><span data-stu-id="6933c-104">Block compression is a texture compression technique for reducing texture size.</span></span> <span data-ttu-id="6933c-105">與每個色彩 32 位元的材質相比，區塊壓縮的紋理可省下高達 75% 的空間。</span><span class="sxs-lookup"><span data-stu-id="6933c-105">When compared to a texture with 32-bits per color, a block-compressed texture can be up to 75 percent smaller.</span></span> <span data-ttu-id="6933c-106">當使用區塊壓縮時，應用程式的效能通常會增加，這是因為磁碟使用量較少。</span><span class="sxs-lookup"><span data-stu-id="6933c-106">Applications usually see a performance increase when using block compression because of the smaller memory footprint.</span></span>

<span data-ttu-id="6933c-107">雖然區塊壓縮會造成失真，但在經過管線轉換並篩選的所有紋理上運作良好，而且建議在這些紋理上使用。</span><span class="sxs-lookup"><span data-stu-id="6933c-107">While lossy, block compression works well and is recommended for all textures that get transformed and filtered by the pipeline.</span></span> <span data-ttu-id="6933c-108">直接對應至螢幕的紋理 (例如圖示和文字等 UI 元素) 不是進行壓縮的好選擇，因為成品會更為醒目。</span><span class="sxs-lookup"><span data-stu-id="6933c-108">Textures that are directly mapped to the screen (UI elements like icons and text) are not good choices for compression because artifacts are more noticeable.</span></span>

<span data-ttu-id="6933c-109">建立經區塊壓縮的紋理時，所有維度都必須是 4 的倍數，且無法用作管線的輸出。</span><span class="sxs-lookup"><span data-stu-id="6933c-109">A block-compressed texture must be created as a multiple of size 4 in all dimensions and cannot be used as an output of the pipeline.</span></span>

-   [<span data-ttu-id="6933c-110">Block 壓縮的運作方式為何？</span><span class="sxs-lookup"><span data-stu-id="6933c-110">How Does Block Compression Work?</span></span>](#how-does-block-compression-work)
    -   [<span data-ttu-id="6933c-111">儲存未壓縮的資料</span><span class="sxs-lookup"><span data-stu-id="6933c-111">Storing Uncompressed Data</span></span>](#storing-uncompressed-data)
    -   [<span data-ttu-id="6933c-112">儲存壓縮的資料</span><span class="sxs-lookup"><span data-stu-id="6933c-112">Storing Compressed Data</span></span>](#storing-compressed-data)
-   [<span data-ttu-id="6933c-113">使用區塊壓縮</span><span class="sxs-lookup"><span data-stu-id="6933c-113">Using Block Compression</span></span>](#using-block-compression)
    -   [<span data-ttu-id="6933c-114">虛擬大小與實體大小</span><span class="sxs-lookup"><span data-stu-id="6933c-114">Virtual Size versus Physical Size</span></span>](#virtual-size-versus-physical-size)
-   [<span data-ttu-id="6933c-115">壓縮演算法</span><span class="sxs-lookup"><span data-stu-id="6933c-115">Compression Algorithms</span></span>](#compression-algorithms)
    -   [<span data-ttu-id="6933c-116">BC1</span><span class="sxs-lookup"><span data-stu-id="6933c-116">BC1</span></span>](#bc1)
    -   [<span data-ttu-id="6933c-117">BC2</span><span class="sxs-lookup"><span data-stu-id="6933c-117">BC2</span></span>](#bc2)
    -   [<span data-ttu-id="6933c-118">BC3</span><span class="sxs-lookup"><span data-stu-id="6933c-118">BC3</span></span>](#bc3)
    -   [<span data-ttu-id="6933c-119">BC4</span><span class="sxs-lookup"><span data-stu-id="6933c-119">BC4</span></span>](#bc4)
    -   [<span data-ttu-id="6933c-120">BC5</span><span class="sxs-lookup"><span data-stu-id="6933c-120">BC5</span></span>](#bc5)
-   [<span data-ttu-id="6933c-121">使用 Direct3D 10.1 的格式轉換</span><span class="sxs-lookup"><span data-stu-id="6933c-121">Format Conversion Using Direct3D 10.1</span></span>](#format-conversion-using-direct3d-101)
-   [<span data-ttu-id="6933c-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="6933c-122">Related topics</span></span>](#related-topics)

## <a name="how-does-block-compression-work"></a><span data-ttu-id="6933c-123">Block 壓縮的運作方式為何？</span><span class="sxs-lookup"><span data-stu-id="6933c-123">How Does Block Compression Work?</span></span>

<span data-ttu-id="6933c-124">區塊壓縮是一種用以減少儲存色彩資料所需記憶體的技術。</span><span class="sxs-lookup"><span data-stu-id="6933c-124">Block compression is a technique for reducing the amount of memory required to store color data.</span></span> <span data-ttu-id="6933c-125">藉由將某些色彩儲存為其原始大小，並在其他色彩上使用編碼配置，您可以大幅減少儲存圖片所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6933c-125">By storing some colors in their original size, and other colors using an encoding scheme, you can dramatically reduce the amount of memory required to store the image.</span></span> <span data-ttu-id="6933c-126">因為硬體會自動解碼壓縮過的資料，所以就不會有使用壓縮紋理而造成效能降低的情形。</span><span class="sxs-lookup"><span data-stu-id="6933c-126">Since the hardware automatically decodes compressed data, there is no performance penalty for using compressed textures.</span></span>

<span data-ttu-id="6933c-127">若要查看壓縮的運作方式，請查看下列兩個範例。</span><span class="sxs-lookup"><span data-stu-id="6933c-127">To see how compression works, look at the following two examples.</span></span> <span data-ttu-id="6933c-128">第一個範例描述儲存未壓縮的資料時使用的記憶體量；第二個範例描述儲存壓縮資料時使用的記憶體量。</span><span class="sxs-lookup"><span data-stu-id="6933c-128">The first example describes the amount of memory used when storing uncompressed data; the second example describes the amount of memory used when storing compressed data.</span></span>

### <a name="storing-uncompressed-data"></a><span data-ttu-id="6933c-129">儲存未壓縮的資料</span><span class="sxs-lookup"><span data-stu-id="6933c-129">Storing Uncompressed Data</span></span>

<span data-ttu-id="6933c-130">下圖為一個未壓縮的 4 × 4 紋理。</span><span class="sxs-lookup"><span data-stu-id="6933c-130">The following illustration represents an uncompressed 4×4 texture.</span></span> <span data-ttu-id="6933c-131">假設每個色彩都包含單一色彩元件 (例如紅色)，並儲存在記憶體的一個位元組內。</span><span class="sxs-lookup"><span data-stu-id="6933c-131">Assume that each color contains a single color component (red for instance) and is stored in one byte of memory.</span></span>

![未壓縮的4x4 材質圖例](images/d3d10-block-compress-1.png)

<span data-ttu-id="6933c-133">未壓縮的資料會在記憶體中循序配置，且需要 16 位元組的記憶體，如下所示。</span><span class="sxs-lookup"><span data-stu-id="6933c-133">The uncompressed data is laid out in memory sequentially and requires 16 bytes, as shown in the following illustration.</span></span>

![連續記憶體中未壓縮資料的圖例](images/d3d10-block-compress-2.png)

### <a name="storing-compressed-data"></a><span data-ttu-id="6933c-135">儲存壓縮的資料</span><span class="sxs-lookup"><span data-stu-id="6933c-135">Storing Compressed Data</span></span>

<span data-ttu-id="6933c-136">既然您已經看過未壓縮圖片會使用多少記憶體，現在就來看看壓縮圖片會節省多少記憶體。</span><span class="sxs-lookup"><span data-stu-id="6933c-136">Now that you've seen how much memory an uncompressed image uses, take a look at how much memory a compressed image saves.</span></span> <span data-ttu-id="6933c-137">[BC1](#bc1) 壓縮格式儲存 2 種色彩 (每種 1 位元組) 和 16 個 3 位元索引 (48 位元或 6 位元組)，用來插入材質內的原始色彩，如下列圖例所示。</span><span class="sxs-lookup"><span data-stu-id="6933c-137">The [BC1](#bc1) compression format stores 2 colors (1 byte each) and 16 3-bit indices (48 bits, or 6 bytes) that are used to interpolate the original colors in the texture, as shown in the following illustration.</span></span>

![bc1 壓縮格式的圖例](images/d3d10-block-compress-3.png)

<span data-ttu-id="6933c-139">儲存壓縮資料所需的總空間為 8 位元組，和未壓縮的範例相比省下 50% 的記憶體空間。</span><span class="sxs-lookup"><span data-stu-id="6933c-139">The total space required to store the compressed data is 8 bytes which is a 50-percent memory savings over the uncompressed example.</span></span> <span data-ttu-id="6933c-140">使用多個色彩元件時，會省下更大的空間。</span><span class="sxs-lookup"><span data-stu-id="6933c-140">The savings are even larger when more than one color component is used.</span></span>

<span data-ttu-id="6933c-141">區塊壓縮省下的大量記憶體，可促使效能增加。</span><span class="sxs-lookup"><span data-stu-id="6933c-141">The substantial memory savings provided by block compression can lead to an increase in performance.</span></span> <span data-ttu-id="6933c-142">此效能增長是降低圖片品質而得 (基於色彩內插補點)。不過，品質的下降通常不明顯。</span><span class="sxs-lookup"><span data-stu-id="6933c-142">This performance comes at the cost of image quality (due to color interpolation); however, the lower quality is often not noticeable.</span></span>

<span data-ttu-id="6933c-143">下一節會說明 Direct3D 10 如何讓您輕鬆地在應用程式中使用區塊壓縮。</span><span class="sxs-lookup"><span data-stu-id="6933c-143">The next section shows you how Direct3D 10 makes it easy for you to use block compression in your application.</span></span>

## <a name="using-block-compression"></a><span data-ttu-id="6933c-144">使用區塊壓縮</span><span class="sxs-lookup"><span data-stu-id="6933c-144">Using Block Compression</span></span>

<span data-ttu-id="6933c-145">建立區塊壓縮紋理，就像未壓縮的材質一樣 (請參閱 [從檔案建立材質](d3d10-graphics-programming-guide-resources-creating-textures.md)) 但您指定了區塊壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="6933c-145">Create a block-compressed texture just like an uncompressed texture (see [Create a Texture from a File](d3d10-graphics-programming-guide-resources-creating-textures.md)) except that you specify a block-compressed format.</span></span>


```
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;
D3DX10CreateTextureFromFile(...);
```



<span data-ttu-id="6933c-146">接著，建立將材質系結至管線的 view。</span><span class="sxs-lookup"><span data-stu-id="6933c-146">Next, create a view to bind the texture to the pipeline.</span></span> <span data-ttu-id="6933c-147">由於區塊壓縮的材質只能用來做為著色器階段的輸入，因此您想要藉由呼叫 [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview)來建立著色器資源檢視。</span><span class="sxs-lookup"><span data-stu-id="6933c-147">Since a block-compressed texture can be used only as an input to a shader-stage, you want to create a shader-resource view by calling [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span></span>

<span data-ttu-id="6933c-148">依您使用未壓縮紋理的相同方式來使用區塊壓縮紋理。</span><span class="sxs-lookup"><span data-stu-id="6933c-148">Use a block compressed texture the same way you would use an uncompressed texture.</span></span> <span data-ttu-id="6933c-149">如果您的應用程式會取得記憶體指標來顯示區塊壓縮資料，你需要處理造成宣告大小和實際大小不同的 Mipmap 內記憶體填補。</span><span class="sxs-lookup"><span data-stu-id="6933c-149">If your application will get a memory pointer to block-compressed data, you need to account for the memory padding in a mipmap that causes the declared size to differ from the actual size.</span></span>

### <a name="virtual-size-versus-physical-size"></a><span data-ttu-id="6933c-150">虛擬大小與實體大小</span><span class="sxs-lookup"><span data-stu-id="6933c-150">Virtual Size versus Physical Size</span></span>

<span data-ttu-id="6933c-151">如果您應用程式中的程式碼，使用記憶體指標來引導區塊壓縮紋理記憶體的話，有一個重要考量要注意，這可能會需要修改您應用程式中的程式碼。</span><span class="sxs-lookup"><span data-stu-id="6933c-151">If you have application code that uses a memory pointer to walk the memory of a block compressed texture, there is one important consideration that may require a modification in your application code.</span></span> <span data-ttu-id="6933c-152">區塊壓縮紋理必須在所有維度中都是 4 的倍數，因為區塊壓縮演算法是在 4x4 的材質區塊上執行。</span><span class="sxs-lookup"><span data-stu-id="6933c-152">A block-compressed texture must be a multiple of 4 in all dimensions because the block-compression algorithms operate on 4x4 texel blocks.</span></span> <span data-ttu-id="6933c-153">這對原始維度能被 4 整除，但分出的子層級卻不能的 Mipmap 會出現問題。</span><span class="sxs-lookup"><span data-stu-id="6933c-153">This will be a problem for a mipmap whose initial dimensions are divisible by 4, but subdivided levels are not.</span></span> <span data-ttu-id="6933c-154">下列圖表顯示每個 Mipmap 層級的虛擬 (宣告) 大小和實體 (實際) 大小差異。</span><span class="sxs-lookup"><span data-stu-id="6933c-154">The following diagram shows the difference in area between the virtual (declared) size and the physical (actual) size of each mipmap level.</span></span>

![未壓縮和壓縮的 mipmap 層級圖表](images/d3d10-block-compress-pad.png)

<span data-ttu-id="6933c-156">圖表左側顯示專為未壓縮 60 × 40 紋理而產生的 Mipmap 層級大小。</span><span class="sxs-lookup"><span data-stu-id="6933c-156">The left side of the diagram shows the mipmap level sizes that are generated for an uncompressed 60×40 texture.</span></span> <span data-ttu-id="6933c-157">最上層大小是從產生該紋理的 API 呼叫而來；每個後續層級的大小為先前層級的一半。</span><span class="sxs-lookup"><span data-stu-id="6933c-157">The top level size is taken from the API call that generates the texture; each subsequent level is half the size of the previous level.</span></span> <span data-ttu-id="6933c-158">對未壓縮紋理而言，虛擬 (宣告) 大小和實體 (實際) 大小之間並無不同。</span><span class="sxs-lookup"><span data-stu-id="6933c-158">For an uncompressed texture, there is no difference between the virtual (declared) size and the physical (actual) size.</span></span>

<span data-ttu-id="6933c-159">圖表右側顯示專為使用壓縮之相同 60 × 40 紋理而產生的 Mipmap 層級大小。</span><span class="sxs-lookup"><span data-stu-id="6933c-159">The right side of the diagram shows the mipmap level sizes that are generated for the same 60×40 texture with compression.</span></span> <span data-ttu-id="6933c-160">請注意第二個和第三個層級都有記憶體填補，讓每個層級的大小都為 4 的因數。</span><span class="sxs-lookup"><span data-stu-id="6933c-160">Notice that both the second and third levels have memory padding to make the sizes factors of 4 on every level.</span></span> <span data-ttu-id="6933c-161">這是必要的，好讓演算法可以在 4×4 材質區塊上執行。</span><span class="sxs-lookup"><span data-stu-id="6933c-161">This is necessary so that the algorithms can operate on 4×4 texel blocks.</span></span> <span data-ttu-id="6933c-162">如果您考慮讓 Mipmap 層級小於 4×4，這會特別明顯。在配置紋理記憶體時，這些非常小的 Mipmap 層級大小將會進位成最接近之 4 的因數。</span><span class="sxs-lookup"><span data-stu-id="6933c-162">This is expecially evident if you consider mipmap levels that are smaller than 4×4; the size of these very small mipmap levels will be rounded up to the nearest factor of 4 when texture memory is allocated.</span></span>

<span data-ttu-id="6933c-163">取樣硬體使用虛擬大小。在取樣紋理時，會忽略記憶體填補。</span><span class="sxs-lookup"><span data-stu-id="6933c-163">Sampling hardware uses the virtual size; when the texture is sampled, the memory padding is ignored.</span></span> <span data-ttu-id="6933c-164">對小於 4x4 的 Mipmap 層級，僅前四個材質會用於 2×2 貼圖，且只有第一個材質會由一個 1×1 區塊使用。</span><span class="sxs-lookup"><span data-stu-id="6933c-164">For mipmap levels that are smaller than 4×4, only the first four texels will be used for a 2×2 map, and only the first texel will be used by a 1×1 block.</span></span> <span data-ttu-id="6933c-165">不過，沒有 API 結構會公開實體大小 (包括記憶體填補)。</span><span class="sxs-lookup"><span data-stu-id="6933c-165">However, there is no API structure that exposes the physical size (including the memory padding).</span></span>

<span data-ttu-id="6933c-166">總結來說，複製包含區塊壓縮資料的區域時，請注意使用對齊的記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="6933c-166">In summary, be careful to use aligned memory blocks when copying regions that contain block-compressed data.</span></span> <span data-ttu-id="6933c-167">若要在可取得記憶體指標的應用程式中執行此動作，請確定指標使用表面字幅來處理實體記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="6933c-167">To do this in an application that gets a memory pointer, make sure that the pointer uses the surface pitch to account for the physical memory size.</span></span>

## <a name="compression-algorithms"></a><span data-ttu-id="6933c-168">壓縮演算法</span><span class="sxs-lookup"><span data-stu-id="6933c-168">Compression Algorithms</span></span>

<span data-ttu-id="6933c-169">在 Direct3D 內的區塊壓縮技術，會將未壓縮紋理資料切割為 4×4 的區塊、壓縮每個區塊，並儲存該資料。</span><span class="sxs-lookup"><span data-stu-id="6933c-169">Block compression techniques in Direct3D break up uncompressed texture data into 4×4 blocks, compress each block, and then store the data.</span></span> <span data-ttu-id="6933c-170">基於這個原因，需要壓縮之材質的紋理維度必須要為 4 的倍數。</span><span class="sxs-lookup"><span data-stu-id="6933c-170">For this reason, textures are expected to be compressed must have texture dimensions that are multiples of 4.</span></span>

![區塊壓縮的圖表](images/d3d10-compression-1.png)

<span data-ttu-id="6933c-172">上述圖表顯示出一個分割成材質區塊的紋理。</span><span class="sxs-lookup"><span data-stu-id="6933c-172">The preceding diagram shows a texture partitioned into texel blocks.</span></span> <span data-ttu-id="6933c-173">第一個區塊會顯示標記為 a 至 p 的 16 種材質配置，但每個區塊都具有相同的資料組織。</span><span class="sxs-lookup"><span data-stu-id="6933c-173">The first block shows the layout of the 16 texels labeled a-p, but every block has the same organization of data.</span></span>

<span data-ttu-id="6933c-174">Direct3D 實作多種壓縮配置，其個別實作以下三種不同折衷之處的其中一項：元件的儲存數、每個元件的位元，以及使用的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="6933c-174">Direct3D implements several compression schemes, each implements a different tradeoff between number of components stored, the number of bits per component, and the amount of memory consumed.</span></span> <span data-ttu-id="6933c-175">使用此表格，以協助您選擇最適合所用資料類型的格式，以及最符合您應用程式的資料解析度。</span><span class="sxs-lookup"><span data-stu-id="6933c-175">Use this table to help choose the format that works best with the type of data and the data resolution that best fits your application.</span></span>



| <span data-ttu-id="6933c-176">來源資料</span><span class="sxs-lookup"><span data-stu-id="6933c-176">Source Data</span></span>                     | <span data-ttu-id="6933c-177">資料壓縮解析度 (依位元計算)</span><span class="sxs-lookup"><span data-stu-id="6933c-177">Data Compression Resolution (in bits)</span></span> | <span data-ttu-id="6933c-178">選擇此壓縮格式</span><span class="sxs-lookup"><span data-stu-id="6933c-178">Choose this compression format</span></span> |
|---------------------------------|---------------------------------------|--------------------------------|
| <span data-ttu-id="6933c-179">三元件色彩和 Alpha</span><span class="sxs-lookup"><span data-stu-id="6933c-179">Three-component color and alpha</span></span> | <span data-ttu-id="6933c-180">色彩 (5:6:5)、Alpha (1) 或沒有 Alpha</span><span class="sxs-lookup"><span data-stu-id="6933c-180">Color (5:6:5), Alpha (1) or no alpha</span></span>  | <span data-ttu-id="6933c-181">BC1</span><span class="sxs-lookup"><span data-stu-id="6933c-181">BC1</span></span>                            |
| <span data-ttu-id="6933c-182">三元件色彩和 Alpha</span><span class="sxs-lookup"><span data-stu-id="6933c-182">Three-component color and alpha</span></span> | <span data-ttu-id="6933c-183">色彩 (5:6:5)、Alpha (4)</span><span class="sxs-lookup"><span data-stu-id="6933c-183">Color (5:6:5), Alpha (4)</span></span>              | [<span data-ttu-id="6933c-184">BC2</span><span class="sxs-lookup"><span data-stu-id="6933c-184">BC2</span></span>](#bc2)                    |
| <span data-ttu-id="6933c-185">三元件色彩和 Alpha</span><span class="sxs-lookup"><span data-stu-id="6933c-185">Three-component color and alpha</span></span> | <span data-ttu-id="6933c-186">色彩 (5:6:5)、Alpha (8)</span><span class="sxs-lookup"><span data-stu-id="6933c-186">Color (5:6:5), Alpha (8)</span></span>              | [<span data-ttu-id="6933c-187">BC3</span><span class="sxs-lookup"><span data-stu-id="6933c-187">BC3</span></span>](#bc3)                    |
| <span data-ttu-id="6933c-188">單元件色彩</span><span class="sxs-lookup"><span data-stu-id="6933c-188">One-component color</span></span>             | <span data-ttu-id="6933c-189">單元件 (8)</span><span class="sxs-lookup"><span data-stu-id="6933c-189">One component (8)</span></span>                     | [<span data-ttu-id="6933c-190">BC4</span><span class="sxs-lookup"><span data-stu-id="6933c-190">BC4</span></span>](#bc4)                    |
| <span data-ttu-id="6933c-191">雙元件色彩</span><span class="sxs-lookup"><span data-stu-id="6933c-191">Two-component color</span></span>             | <span data-ttu-id="6933c-192">雙元件 (8:8)</span><span class="sxs-lookup"><span data-stu-id="6933c-192">Two components (8:8)</span></span>                  | [<span data-ttu-id="6933c-193">BC5</span><span class="sxs-lookup"><span data-stu-id="6933c-193">BC5</span></span>](#bc5)                    |



 

### <a name="bc1"></a><span data-ttu-id="6933c-194">BC1</span><span class="sxs-lookup"><span data-stu-id="6933c-194">BC1</span></span>

<span data-ttu-id="6933c-195">您可以使用第一個區塊壓縮格式 (BC1)  (DXGI 格式 BC1 無型別 \_ \_ \_ 、dxgi \_ FORMAT \_ BC1 \_ UNORM 或 dxgi \_ BC1 \_ UNORM \_ SRGB) 使用5:6:5 色 (5 位紅色、6位綠色、5位藍色) 來儲存三個元件的色彩資料。</span><span class="sxs-lookup"><span data-stu-id="6933c-195">Use the first block compression format (BC1) (either DXGI\_FORMAT\_BC1\_TYPELESS, DXGI\_FORMAT\_BC1\_UNORM, or DXGI\_BC1\_UNORM\_SRGB) to store three-component color data using a 5:6:5 color (5 bits red, 6 bits green, 5 bits blue).</span></span> <span data-ttu-id="6933c-196">即使您的資料也包含 1 位元 Alpha 也是如此。</span><span class="sxs-lookup"><span data-stu-id="6933c-196">This is true even if the data also contains 1-bit alpha.</span></span> <span data-ttu-id="6933c-197">假設 4×4 紋理使用所能使用的最大資料格式，BC1 格式會將所需的記憶體從 48 位元組 (16 色 × 3 元件/色彩 × 1 位元組/元件) 降低至 8 位元組的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6933c-197">Assuming a 4×4 texture using the largest data format possible, the BC1 format reduces the memory required from 48 bytes (16 colors × 3 components/color × 1 byte/component) to 8 bytes of memory.</span></span>

<span data-ttu-id="6933c-198">此演算法適用於 4×4 材質區塊上。</span><span class="sxs-lookup"><span data-stu-id="6933c-198">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="6933c-199">演算法不會儲存16個色彩，而是會將2個參考色彩儲存 (色 \_ 0 和色彩 \_ 1) 和 16 2 位色彩索引 (區塊 a – p) ，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="6933c-199">Instead of storing 16 colors, the algorithm saves 2 reference colors (color\_0 and color\_1) and 16 2-bit color indices (blocks a–p), as shown in the following diagram.</span></span>

![bc1 壓縮的版面配置圖表](images/d3d10-compression-bc1.png)

<span data-ttu-id="6933c-201">色彩索引 (a 至 p) 是用來從色彩表查看原始的色彩。</span><span class="sxs-lookup"><span data-stu-id="6933c-201">The color indices (a–p) are used to look up the original colors from a color table.</span></span> <span data-ttu-id="6933c-202">色彩表包含 4 個色彩。</span><span class="sxs-lookup"><span data-stu-id="6933c-202">The color table contains 4 colors.</span></span> <span data-ttu-id="6933c-203">前兩個色彩（色彩 \_ 0 和色彩 \_ 1）是最小和最大的色彩。</span><span class="sxs-lookup"><span data-stu-id="6933c-203">The first two colors—color\_0 and color\_1—are the minimum and maximum colors.</span></span> <span data-ttu-id="6933c-204">其他兩種色彩（色彩 \_ 2 和色彩 \_ 3）是以線性插補計算的中間色彩。</span><span class="sxs-lookup"><span data-stu-id="6933c-204">The other two colors, color\_2 and color\_3, are intermediate colors calculated with linear interpolation.</span></span>


```
color_2 = 2/3*color_0 + 1/3*color_1
color_3 = 1/3*color_0 + 2/3*color_1
```



<span data-ttu-id="6933c-205">四個色彩都被指派了 2 位元索引值，這些值將會儲存在 a 至 p 區塊。</span><span class="sxs-lookup"><span data-stu-id="6933c-205">The four colors are assigned 2-bit index values that will be saved in blocks a–p.</span></span>


```
color_0 = 00
color_1 = 01
color_2 = 10
color_3 = 11
```



<span data-ttu-id="6933c-206">最後，每個 a 至 p 區塊中的色彩會與四種在色彩表內的色彩對比，而最接近色彩的索引會儲存在 2 位元區塊中。</span><span class="sxs-lookup"><span data-stu-id="6933c-206">Finally, each of the colors in blocks a–p are compared with the four colors in the color table, and the index for the closest color is stored in the 2-bit blocks.</span></span>

<span data-ttu-id="6933c-207">此演算法也適用於包含 1 位元 Alpha 的資料。</span><span class="sxs-lookup"><span data-stu-id="6933c-207">This algorithm lends itself to data that contains 1-bit alpha also.</span></span> <span data-ttu-id="6933c-208">唯一的差別在於色彩 \_ 3 會設定為 0 (代表透明色彩) 而色彩 \_ 2 則是色彩 \_ 0 和色彩1的線性 blend \_ 。</span><span class="sxs-lookup"><span data-stu-id="6933c-208">The only difference is that color\_3 is set to 0 (which represents a transparent color) and color\_2 is a linear blend of color\_0 and color\_1.</span></span>


```
color_2 = 1/2*color_0 + 1/2*color_1;
color_3 = 0;
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6933c-209">Direct3D 9 與 Direct3D 10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="6933c-209">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="6933c-210">這種格式同時存在於 Direct3D 9 和10。</span><span class="sxs-lookup"><span data-stu-id="6933c-210">This format exists in both Direct3D 9 and 10.</span></span><br/>
<ul>
<li><span data-ttu-id="6933c-211">在 Direct3D 9 中，BC1 格式稱為 D3DFMT_DXT1。</span><span class="sxs-lookup"><span data-stu-id="6933c-211">In Direct3D 9, the BC1 format is called D3DFMT_DXT1.</span></span></li>
<li><span data-ttu-id="6933c-212">在 Direct3D 10 中，BC1 格式是以 DXGI_FORMAT_BC1_UNORM 或 DXGI_FORMAT_BC1_UNORM_SRGB 表示。</span><span class="sxs-lookup"><span data-stu-id="6933c-212">In Direct3D 10, the BC1 format is represented by DXGI_FORMAT_BC1_UNORM or DXGI_FORMAT_BC1_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc2"></a><span data-ttu-id="6933c-213">BC2</span><span class="sxs-lookup"><span data-stu-id="6933c-213">BC2</span></span>

<span data-ttu-id="6933c-214">使用 BC2 格式 (DXGI 格式 BC2 無型別 \_ \_ \_ 、dxgi \_ FORMAT \_ BC2 \_ UNORM 或 dxgi \_ BC2 \_ UNORM \_ SRGB) 儲存包含色彩和 Alpha 資料（具有低一致性）的資料 (使用 [BC3](#bc3) 來進行高度一致的 Alpha 資料) 。</span><span class="sxs-lookup"><span data-stu-id="6933c-214">Use the BC2 format (either DXGI\_FORMAT\_BC2\_TYPELESS, DXGI\_FORMAT\_BC2\_UNORM, or DXGI\_BC2\_UNORM\_SRGB) to store data that contains color and alpha data with low coherency (use [BC3](#bc3) for highly-coherent alpha data).</span></span> <span data-ttu-id="6933c-215">BC2 格式將 RGB 資料儲存為 5:6:5 色彩 (5 位元紅色、6 位元綠色、5 位元藍色)，並將 Alpha 儲存為不同的 4 位元值。</span><span class="sxs-lookup"><span data-stu-id="6933c-215">The BC2 format stores RGB data as a 5:6:5 color (5 bits red, 6 bits green, 5 bits blue) and alpha as a separate 4-bit value.</span></span> <span data-ttu-id="6933c-216">假設 4×4 紋理使用所能使用的最大資料格式，此壓縮技術會將所需的記憶體從 64 位元組 (16 色 × 4 元件/色彩 × 1 位元組/元件) 降低至 16 位元組的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6933c-216">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 64 bytes (16 colors × 4 components/color × 1 byte/component) to 16 bytes of memory.</span></span>

<span data-ttu-id="6933c-217">BC2 格式儲存的色彩與 [BC1](#bc1) 格式的位元數量和資料配置相同。不過，BC2 需要額外 64 位元的記憶體來儲存 Alpha 資料，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="6933c-217">The BC2 format stores colors with the same number of bits and data layout as the [BC1](#bc1) format; however, BC2 requires an additional 64-bits of memory to store the alpha data, as shown in the following diagram.</span></span>

![bc2 壓縮的版面配置圖表](images/d3d10-compression-bc2.png)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6933c-219">Direct3D 9 與 Direct3D 10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="6933c-219">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="6933c-220">這種格式同時存在於 Direct3D 9 和10。</span><span class="sxs-lookup"><span data-stu-id="6933c-220">This format exists in both Direct3D 9 and 10.</span></span><br/>
<ul>
<li><span data-ttu-id="6933c-221">在 Direct3D 9 中，BC2 格式稱為 D3DFMT_DXT2 和 D3DFMT_DXT3。</span><span class="sxs-lookup"><span data-stu-id="6933c-221">In Direct3D 9, the BC2 format is called D3DFMT_DXT2 and D3DFMT_DXT3.</span></span></li>
<li><span data-ttu-id="6933c-222">在 Direct3D 10 中，BC2 格式是以 DXGI_FORMAT_BC2_UNORM 或 DXGI_FORMAT_BC2_UNORM_SRGB 表示。</span><span class="sxs-lookup"><span data-stu-id="6933c-222">In Direct3D 10, the BC2 format is represented by DXGI_FORMAT_BC2_UNORM or DXGI_FORMAT_BC2_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc3"></a><span data-ttu-id="6933c-223">BC3</span><span class="sxs-lookup"><span data-stu-id="6933c-223">BC3</span></span>

<span data-ttu-id="6933c-224">您可以使用 BC3 格式 (DXGI \_ 格式 BC3 無別別 \_ \_ 、dxgi \_ FORMAT \_ BC3 \_ UNORM 或 dxgi \_ BC3 \_ UNORM \_ SRGB) 來儲存高度一致的色彩資料 (使用的 [BC2](#bc2) 與較不一致的 Alpha 資料) 。</span><span class="sxs-lookup"><span data-stu-id="6933c-224">Use the BC3 format (either DXGI\_FORMAT\_BC3\_TYPELESS, DXGI\_FORMAT\_BC3\_UNORM, or DXGI\_BC3\_UNORM\_SRGB) to store highly coherent color data (use [BC2](#bc2) with less coherent alpha data).</span></span> <span data-ttu-id="6933c-225">BC3 格式使用 5:6:5 色彩 (5 位元紅色、6 位元綠色、5 位元藍色) 儲存色彩資料，並使用 1 個位元組儲存 Alpha 資料。</span><span class="sxs-lookup"><span data-stu-id="6933c-225">The BC3 format stores color data using 5:6:5 color (5 bits red, 6 bits green, 5 bits blue) and alpha data using one byte.</span></span> <span data-ttu-id="6933c-226">假設 4×4 紋理使用所能使用的最大資料格式，此壓縮技術會將所需的記憶體從 64 位元組 (16 色 × 4 元件/色彩 × 1 位元組/元件) 降低至 16 位元組的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6933c-226">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 64 bytes (16 colors × 4 components/color × 1 byte/component) to 16 bytes of memory.</span></span>

<span data-ttu-id="6933c-227">BC3 格式儲存的色彩與 [BC1](#bc1) 格式的位元數量和資料配置相同。不過，BC3 需要額外 64 位元的記憶體來儲存 Alpha 資料。</span><span class="sxs-lookup"><span data-stu-id="6933c-227">The BC3 format stores colors with the same number of bits and data layout as the [BC1](#bc1) format; however, BC3 requires an additional 64-bits of memory to store the alpha data.</span></span> <span data-ttu-id="6933c-228">BC3 格式藉由儲存兩個參考值並在它們之間內插補點來處理 Alpha (和 BC1 儲存 RGB 色彩的方式相同)。</span><span class="sxs-lookup"><span data-stu-id="6933c-228">The BC3 format handles alpha by storing two reference values and interpolating between them (similarly to how BC1 stores RGB color).</span></span>

<span data-ttu-id="6933c-229">此演算法適用於 4×4 材質區塊上。</span><span class="sxs-lookup"><span data-stu-id="6933c-229">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="6933c-230">演算法不會儲存16個 Alpha 值，而是會儲存2個參考 Alpha (Alpha \_ 0 和 Alpha \_ 1) 和 16 3 位色彩索引 (Alpha a 到 p) ，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="6933c-230">Instead of storing 16 alpha values, the algorithm stores 2 reference alphas (alpha\_0 and alpha\_1) and 16 3-bit color indices (alpha a through p), as shown in the following diagram.</span></span>

![bc3 壓縮的版面配置圖表](images/d3d10-compression-bc3.png)

<span data-ttu-id="6933c-232">BC3 格式使用 Alpha 索引 (a 至 p)，從包含 8 個值的查閱資料表查詢原始的色彩。</span><span class="sxs-lookup"><span data-stu-id="6933c-232">The BC3 format uses the alpha indices (a–p) to look up the original colors from a lookup table that contains 8 values.</span></span> <span data-ttu-id="6933c-233">前兩個值（Alpha \_ 0 和 Alpha \_ 1）是最小值和最大值，其他六個中間值則是使用線性插補來計算。</span><span class="sxs-lookup"><span data-stu-id="6933c-233">The first two values—alpha\_0 and alpha\_1—are the minimum and maximum values; the other six intermediate values are calculated using linear interpolation.</span></span>

<span data-ttu-id="6933c-234">此演算法藉由檢查兩個 Alpha 參考值來判斷插入的 Alpha 值數目。</span><span class="sxs-lookup"><span data-stu-id="6933c-234">The algorithm determines the number of interpolated alpha values by examining the two reference alpha values.</span></span> <span data-ttu-id="6933c-235">如果 Alpha \_ 0 大於 Alpha \_ 1，則 BC3 會將6個 Alpha 值插補，否則會插入4。</span><span class="sxs-lookup"><span data-stu-id="6933c-235">If alpha\_0 is greater than alpha\_1, then BC3 interpolates 6 alpha values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="6933c-236">當 BC3 僅插入 4 個 Alpha 值時，它就會設定兩個額外 Alpha 值 (0 為完全透明，而 255 為完全不透明)。</span><span class="sxs-lookup"><span data-stu-id="6933c-236">When BC3 interpolates only 4 alpha values, it sets two additional alpha values (0 for fully transparent and 255 for fully opaque).</span></span> <span data-ttu-id="6933c-237">BC3 藉由儲存對應插補 Alpha 值的位元程式碼，以壓縮 4×4 材質區域中的 Alpha 值，插補進的 Alpha 值最符合特定材質的原始 Alpha。</span><span class="sxs-lookup"><span data-stu-id="6933c-237">BC3 compresses the alpha values in the 4×4 texel area by storing the bit code corresponding to the interpolated alpha values which most closely matches the original alpha for a given texel.</span></span>


```
if( alpha_0 > alpha_1 )
{
  // 6 interpolated alpha values.
  alpha_2 = 6/7*alpha_0 + 1/7*alpha_1; // bit code 010
  alpha_3 = 5/7*alpha_0 + 2/7*alpha_1; // bit code 011
  alpha_4 = 4/7*alpha_0 + 3/7*alpha_1; // bit code 100
  alpha_5 = 3/7*alpha_0 + 4/7*alpha_1; // bit code 101
  alpha_6 = 2/7*alpha_0 + 5/7*alpha_1; // bit code 110
  alpha_7 = 1/7*alpha_0 + 6/7*alpha_1; // bit code 111
}
else
{
  // 4 interpolated alpha values.
  alpha_2 = 4/5*alpha_0 + 1/5*alpha_1; // bit code 010
  alpha_3 = 3/5*alpha_0 + 2/5*alpha_1; // bit code 011
  alpha_4 = 2/5*alpha_0 + 3/5*alpha_1; // bit code 100
  alpha_5 = 1/5*alpha_0 + 4/5*alpha_1; // bit code 101
  alpha_6 = 0;                         // bit code 110
  alpha_7 = 255;                       // bit code 111
}
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6933c-238">Direct3D 9 與 Direct3D 10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="6933c-238">Differences between Direct3D 9 and Direct3D 10:</span></span><br/>
<ul>
<li><span data-ttu-id="6933c-239">在 Direct3D 9 中，BC3 格式稱為 D3DFMT_DXT4 和 D3DFMT_DXT5。</span><span class="sxs-lookup"><span data-stu-id="6933c-239">In Direct3D 9, the BC3 format is called D3DFMT_DXT4 and D3DFMT_DXT5.</span></span></li>
<li><span data-ttu-id="6933c-240">在 Direct3D 10 中，BC3 格式是以 DXGI_FORMAT_BC3_UNORM 或 DXGI_FORMAT_BC3_UNORM_SRGB 表示。</span><span class="sxs-lookup"><span data-stu-id="6933c-240">In Direct3D 10, the BC3 format is represented by DXGI_FORMAT_BC3_UNORM or DXGI_FORMAT_BC3_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc4"></a><span data-ttu-id="6933c-241">BC4</span><span class="sxs-lookup"><span data-stu-id="6933c-241">BC4</span></span>

<span data-ttu-id="6933c-242">使用 BC4 格式儲存每個色彩都使用 8 位元的單一元件色彩資料。</span><span class="sxs-lookup"><span data-stu-id="6933c-242">Use the BC4 format to store one-component color data using 8 bits for each color.</span></span> <span data-ttu-id="6933c-243">相較于 [BC1](#bc1)) ，精確度 (的結果，BC4 適合用 dxgi 格式 BC4 UNORM 格式，將浮點數資料儲存在 \[ 0 到1的範圍內， \] \_ \_ \_ 而 \[ \] 使用 dxgi \_ 格式 \_ BC4 \_ SNORM 格式的-1 到 + 1。</span><span class="sxs-lookup"><span data-stu-id="6933c-243">As a result of the increased accuracy (compared to [BC1](#bc1)), BC4 is ideal for storing floating-point data in the range of \[0 to 1\] using the DXGI\_FORMAT\_BC4\_UNORM format and \[-1 to +1\] using the DXGI\_FORMAT\_BC4\_SNORM format.</span></span> <span data-ttu-id="6933c-244">假設 4×4 紋理使用所能使用的最大資料格式，此壓縮技術會將所需的記憶體從 16 位元組 (16 色 × 1 元件/色彩 × 1 位元組/元件) 降低至 8 位元組。</span><span class="sxs-lookup"><span data-stu-id="6933c-244">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 16 bytes (16 colors × 1 components/color × 1 byte/component) to 8 bytes.</span></span>

<span data-ttu-id="6933c-245">此演算法適用於 4×4 材質區塊上。</span><span class="sxs-lookup"><span data-stu-id="6933c-245">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="6933c-246">演算法不會儲存16種色彩，而是會儲存2個參考色彩 (紅色 \_ 0 和紅色 \_ 1) 和 16 3 位色彩索引 (紅色 a 到紅色 p) ，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="6933c-246">Instead of storing 16 colors, the algorithm stores 2 reference colors (red\_0 and red\_1) and 16 3-bit color indices (red a through red p), as shown in the following diagram.</span></span>

![bc4 壓縮的版面配置圖表](images/d3d10-compression-bc4.png)

<span data-ttu-id="6933c-248">此演算法使用 3 位元索引，從一個包含 8 種顏色的顏色表內查詢顏色。</span><span class="sxs-lookup"><span data-stu-id="6933c-248">The algorithm uses the 3-bit indices to look up colors from a color table that contains 8 colors.</span></span> <span data-ttu-id="6933c-249">前兩個色彩（紅色 \_ 0 和紅色 \_ 1）是最小和最大的色彩。</span><span class="sxs-lookup"><span data-stu-id="6933c-249">The first two colors—red\_0 and red\_1—are the minimum and maximum colors.</span></span> <span data-ttu-id="6933c-250">此演算法使用線性插補來計算出剩餘的色彩。</span><span class="sxs-lookup"><span data-stu-id="6933c-250">The algorithm calculates the remaining colors using linear interpolation.</span></span>

<span data-ttu-id="6933c-251">此演算法藉由檢查兩個參考值來判斷插入的色彩值數目。</span><span class="sxs-lookup"><span data-stu-id="6933c-251">The algorithm determines the number of interpolated color values by examining the two reference values.</span></span> <span data-ttu-id="6933c-252">如果紅色 \_ 0 大於紅色 \_ 1，則 BC4 會將6個色彩值插補，否則會插入4。</span><span class="sxs-lookup"><span data-stu-id="6933c-252">If red\_0 is greater than red\_1, then BC4 interpolates 6 color values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="6933c-253">當 BC4 僅插入 4 個色彩值時，它會設定兩個額外的色彩值 (0.0f 為完全透明，而 1.0f 為完全不透明)。</span><span class="sxs-lookup"><span data-stu-id="6933c-253">When BC4 interpolates only 4 color values, it sets two additional color values (0.0f for fully transparent and 1.0f for fully opaque).</span></span> <span data-ttu-id="6933c-254">BC4 藉由儲存對應插補 Alpha 值的位元程式碼，以壓縮 4×4 材質區域中的 Alpha 值，插補進的 Alpha 值最符合特定材質的原始 Alpha。</span><span class="sxs-lookup"><span data-stu-id="6933c-254">BC4 compresses the alpha values in the 4×4 texel area by storing the bit code corresponding to the interpolated alpha values that most closely matches the original alpha for a given texel.</span></span>

-   [<span data-ttu-id="6933c-255">BC4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="6933c-255">BC4\_UNORM</span></span>](/windows)
-   [<span data-ttu-id="6933c-256">BC4 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="6933c-256">BC4\_SNORM</span></span>](/windows)

### <a name="bc4_unorm"></a><span data-ttu-id="6933c-257">BC4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="6933c-257">BC4\_UNORM</span></span>

<span data-ttu-id="6933c-258">單一元件資料的內插補點方式如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="6933c-258">The interpolation of the single-component data is done as in the following code sample.</span></span>


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



<span data-ttu-id="6933c-259">參考色彩會被指派 3 位元索引 (因為有 8 個值，所以是 000-111)，此索引會於壓縮期間儲存在紅色 a 到紅色 p 區塊內。</span><span class="sxs-lookup"><span data-stu-id="6933c-259">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc4_snorm"></a><span data-ttu-id="6933c-260">BC4 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="6933c-260">BC4\_SNORM</span></span>

<span data-ttu-id="6933c-261">DXGI \_ 格式 \_ BC4 \_ SNORM 完全相同，不同之處在于資料是以 SNORM 範圍編碼，以及在插入4個色彩值時。</span><span class="sxs-lookup"><span data-stu-id="6933c-261">The DXGI\_FORMAT\_BC4\_SNORM is exactly the same, except that the data is encoded in SNORM range and when 4 color values are interpolated.</span></span> <span data-ttu-id="6933c-262">單一元件資料的內插補點方式如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="6933c-262">The interpolation of the single-component data is done as in the following code sample.</span></span>


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                     // bit code 110
  red_7 =  1.0f;                     // bit code 111
}
```



<span data-ttu-id="6933c-263">參考色彩會被指派 3 位元索引 (因為有 8 個值，所以是 000-111)，此索引會於壓縮期間儲存在紅色 a 到紅色 p 區塊內。</span><span class="sxs-lookup"><span data-stu-id="6933c-263">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc5"></a><span data-ttu-id="6933c-264">BC5</span><span class="sxs-lookup"><span data-stu-id="6933c-264">BC5</span></span>

<span data-ttu-id="6933c-265">以 BC5 格式儲存每個色彩都使用 8 位元的雙元件色彩資料。</span><span class="sxs-lookup"><span data-stu-id="6933c-265">Use the BC5 format to store two-component color data using 8 bits for each color.</span></span> <span data-ttu-id="6933c-266">相較于 [BC1](#bc1)) ，精確度 (的結果，BC5 適合用 dxgi 格式 BC5 UNORM 格式，將浮點數資料儲存在 \[ 0 到1的範圍內， \] \_ \_ \_ 而 \[ \] 使用 dxgi \_ 格式 \_ BC5 \_ SNORM 格式的-1 到 + 1。</span><span class="sxs-lookup"><span data-stu-id="6933c-266">As a result of the increased accuracy (compared to [BC1](#bc1)), BC5 is ideal for storing floating-point data in the range of \[0 to 1\] using the DXGI\_FORMAT\_BC5\_UNORM format and \[-1 to +1\] using the DXGI\_FORMAT\_BC5\_SNORM format.</span></span> <span data-ttu-id="6933c-267">假設 4×4 紋理使用所能使用的最大資料格式，此壓縮技術會將所需的記憶體從 32 位元組 (16 色 × 2 元件/色彩 × 1 位元組/元件) 降低至 16 位元組。</span><span class="sxs-lookup"><span data-stu-id="6933c-267">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 32 bytes (16 colors × 2 components/color × 1 byte/component) to 16 bytes.</span></span>

<span data-ttu-id="6933c-268">此演算法適用於 4×4 材質區塊上。</span><span class="sxs-lookup"><span data-stu-id="6933c-268">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="6933c-269">演算法不會針對這兩個元件儲存16個色彩，而是會為每個元件儲存2個參考色彩 (紅色 \_ 0、紅色 \_ 1、綠色 \_ 0 和綠色 \_ 1) 和每個元件的 16 3 位色彩索引， (紅色 a 到紅色 p，綠色 a 到綠色 p) ，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="6933c-269">Instead of storing 16 colors for both components, the algorithm stores 2 reference colors for each component (red\_0, red\_1, green\_0, and green\_1) and 16 3-bit color indices for each component (red a through red p and green a through green p), as shown in the following diagram.</span></span>

![bc5 壓縮的版面配置圖表](images/d3d10-compression-bc5.png)

<span data-ttu-id="6933c-271">此演算法使用 3 位元索引，從一個包含 8 種顏色的顏色表內查詢顏色。</span><span class="sxs-lookup"><span data-stu-id="6933c-271">The algorithm uses the 3-bit indices to look up colors from a color table that contains 8 colors.</span></span> <span data-ttu-id="6933c-272">前兩個色彩（紅色 \_ 0 和紅色 \_ 1 (或綠色 \_ 0 和綠色 \_ 1) ）是最小和最大的色彩。</span><span class="sxs-lookup"><span data-stu-id="6933c-272">The first two colors—red\_0 and red\_1 (or green\_0 and green\_1)—are the minimum and maximum colors.</span></span> <span data-ttu-id="6933c-273">此演算法使用線性插補來計算出剩餘的色彩。</span><span class="sxs-lookup"><span data-stu-id="6933c-273">The algorithm calculates the remaining colors using linear interpolation.</span></span>

<span data-ttu-id="6933c-274">此演算法藉由檢查兩個參考值來判斷插入的色彩值數目。</span><span class="sxs-lookup"><span data-stu-id="6933c-274">The algorithm determines the number of interpolated color values by examining the two reference values.</span></span> <span data-ttu-id="6933c-275">如果紅色 \_ 0 大於紅色 \_ 1，則 BC5 會將6個色彩值插補，否則會插入4。</span><span class="sxs-lookup"><span data-stu-id="6933c-275">If red\_0 is greater than red\_1, then BC5 interpolates 6 color values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="6933c-276">當 BC5 僅插入 4 個色彩值時，它會將剩下的兩個色彩值設定為 0.0f 和 1.0f。</span><span class="sxs-lookup"><span data-stu-id="6933c-276">When BC5 interpolates only 4 color values, it sets the remaining two color values at 0.0f and 1.0f.</span></span>

-   [<span data-ttu-id="6933c-277">BC5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="6933c-277">BC5\_UNORM</span></span>](/windows)
-   [<span data-ttu-id="6933c-278">BC5 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="6933c-278">BC5\_SNORM</span></span>](/windows)

### <a name="bc5_unorm"></a><span data-ttu-id="6933c-279">BC5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="6933c-279">BC5\_UNORM</span></span>

<span data-ttu-id="6933c-280">單一元件資料的內插補點方式如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="6933c-280">The interpolation of the single-component data is done as in the following code sample.</span></span> <span data-ttu-id="6933c-281">綠色元件的計算方法都很相似。</span><span class="sxs-lookup"><span data-stu-id="6933c-281">The calculations for the green components are similar.</span></span>


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



<span data-ttu-id="6933c-282">參考色彩會被指派 3 位元索引 (因為有 8 個值，所以是 000-111)，此索引會於壓縮期間儲存在紅色 a 到紅色 p 區塊內。</span><span class="sxs-lookup"><span data-stu-id="6933c-282">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc5_snorm"></a><span data-ttu-id="6933c-283">BC5 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="6933c-283">BC5\_SNORM</span></span>

<span data-ttu-id="6933c-284">DXGI \_ 格式 \_ BC5 \_ SNORM 完全相同，不同之處在于資料是以 SNORM 範圍編碼，而且當插入4個數據值時，另外兩個值為-1.0 f 和 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="6933c-284">The DXGI\_FORMAT\_BC5\_SNORM is exactly the same, except that the data is encoded in SNORM range and when 4 data values are interpolated, the two additional values are -1.0f and 1.0f.</span></span> <span data-ttu-id="6933c-285">單一元件資料的內插補點方式如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="6933c-285">The interpolation of the single-component data is done as in the following code sample.</span></span> <span data-ttu-id="6933c-286">綠色元件的計算方法都很相似。</span><span class="sxs-lookup"><span data-stu-id="6933c-286">The calculations for the green components are similar.</span></span>


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                    // bit code 110
  red_7 =  1.0f;                    // bit code 111
}
```



<span data-ttu-id="6933c-287">參考色彩會被指派 3 位元索引 (因為有 8 個值，所以是 000-111)，此索引會於壓縮期間儲存在紅色 a 到紅色 p 區塊內。</span><span class="sxs-lookup"><span data-stu-id="6933c-287">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

## <a name="format-conversion-using-direct3d-101"></a><span data-ttu-id="6933c-288">使用 Direct3D 10.1 的格式轉換</span><span class="sxs-lookup"><span data-stu-id="6933c-288">Format Conversion Using Direct3D 10.1</span></span>

<span data-ttu-id="6933c-289">Direct3D 10.1 可讓 prestructured 型別紋理與相同位寬度的區塊壓縮紋理之間進行複製。</span><span class="sxs-lookup"><span data-stu-id="6933c-289">Direct3D 10.1 enables copies between prestructured-typed textures and block-compressed textures of the same bit widths.</span></span> <span data-ttu-id="6933c-290">可以完成此工作的函式為 [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) 和 [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)。</span><span class="sxs-lookup"><span data-stu-id="6933c-290">The functions that can accomplish this are [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) and [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion).</span></span>

<span data-ttu-id="6933c-291">從 Direct3D 10.1 開始，您可以使用 [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) 和 [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) ，在幾種格式類型之間複製。</span><span class="sxs-lookup"><span data-stu-id="6933c-291">Beginning with Direct3D 10.1, you can use [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) and [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) to copy between a few format types.</span></span> <span data-ttu-id="6933c-292">此類型的複製作業會執行一種格式轉換，將資源資料重新解譯為不同的格式類型。</span><span class="sxs-lookup"><span data-stu-id="6933c-292">This type of copy operation performs a type of format conversion that reinterprets resource data as a different format type.</span></span> <span data-ttu-id="6933c-293">請將此範例納入考慮，它用更典型的轉換行為方式來顯示重新解譯資料之間的不同︰</span><span class="sxs-lookup"><span data-stu-id="6933c-293">Consider this example that shows the difference between reinterpreting data with the way a more typical type of conversion behaves:</span></span>


```
    FLOAT32 f = 1.0f;
    UINT32 u;
```



<span data-ttu-id="6933c-294">若要將 ' f ' 重新解譯為 ' u ' 的類型，請使用 [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy)：</span><span class="sxs-lookup"><span data-stu-id="6933c-294">To reinterpret ‘f’ as the type of ‘u’, use [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy):</span></span>


```
    memcpy( &u, &f, sizeof( f ) ); // ‘u’ becomes equal to 0x3F800000.
```



<span data-ttu-id="6933c-295">在上述重新解譯中，資料的基礎值不會變更。[memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) 會將浮點數重新解譯為不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="6933c-295">In the preceding reinterpretation, the underlying value of the data doesn’t change; [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) reinterprets the float as an unsigned integer.</span></span>

<span data-ttu-id="6933c-296">若要執行更常見的轉換類型，請使用下列設定︰</span><span class="sxs-lookup"><span data-stu-id="6933c-296">To perform the more typical type of conversion, use assignment:</span></span>


```
    u = f; // ‘u’ becomes 1.
```



<span data-ttu-id="6933c-297">在上述轉換中，資料的基礎值有所變更。</span><span class="sxs-lookup"><span data-stu-id="6933c-297">In the preceding conversion, the underlying value of the data changes.</span></span>

<span data-ttu-id="6933c-298">下表列出允許的來源和目的地格式，您可以在此格式轉換的重新解譯類型內使用。</span><span class="sxs-lookup"><span data-stu-id="6933c-298">The following table lists the allowable source and destination formats that you can use in this reinterpretation type of format conversion.</span></span> <span data-ttu-id="6933c-299">您必須正確地為值進行編碼，才能讓重新解譯正常運作。</span><span class="sxs-lookup"><span data-stu-id="6933c-299">You must encode the values properly for the reinterpretation to work as expected.</span></span>



| <span data-ttu-id="6933c-300">位元寬度</span><span class="sxs-lookup"><span data-stu-id="6933c-300">Bit Width</span></span> | <span data-ttu-id="6933c-301">未壓縮資源</span><span class="sxs-lookup"><span data-stu-id="6933c-301">Uncompressed Resource</span></span>                                                                                                                                               | <span data-ttu-id="6933c-302">區塊壓縮資源</span><span class="sxs-lookup"><span data-stu-id="6933c-302">Block-Compressed Resource</span></span>                                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6933c-303">32</span><span class="sxs-lookup"><span data-stu-id="6933c-303">32</span></span>        | <span data-ttu-id="6933c-304">DXGI \_ 格式 \_ R32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="6933c-304">DXGI\_FORMAT\_R32\_UINT</span></span><br/> <span data-ttu-id="6933c-305">DXGI \_ 格式 \_ R32 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="6933c-305">DXGI\_FORMAT\_R32\_SINT</span></span><br/>                                                                                               | <span data-ttu-id="6933c-306">DXGI \_ 格式 \_ R9G9B9E5 \_ SHAREDEXP</span><span class="sxs-lookup"><span data-stu-id="6933c-306">DXGI\_FORMAT\_R9G9B9E5\_SHAREDEXP</span></span>                                                                                                                                   |
| <span data-ttu-id="6933c-307">64</span><span class="sxs-lookup"><span data-stu-id="6933c-307">64</span></span>        | <span data-ttu-id="6933c-308">DXGI \_ 格式 \_ R16G16B16A16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="6933c-308">DXGI\_FORMAT\_R16G16B16A16\_UINT</span></span><br/> <span data-ttu-id="6933c-309">DXGI \_ 格式 \_ R16G16B16A16 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="6933c-309">DXGI\_FORMAT\_R16G16B16A16\_SINT</span></span><br/> <span data-ttu-id="6933c-310">DXGI \_ 格式 \_ R32G32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="6933c-310">DXGI\_FORMAT\_R32G32\_UINT</span></span><br/> <span data-ttu-id="6933c-311">DXGI \_ 格式 \_ R32G32 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="6933c-311">DXGI\_FORMAT\_R32G32\_SINT</span></span><br/> | <span data-ttu-id="6933c-312">DXGI \_ 格式 \_ BC1 \_ UNORM \[ \_ SRGB\]</span><span class="sxs-lookup"><span data-stu-id="6933c-312">DXGI\_FORMAT\_BC1\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="6933c-313">DXGI \_ 格式 \_ BC4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="6933c-313">DXGI\_FORMAT\_BC4\_UNORM</span></span><br/> <span data-ttu-id="6933c-314">DXGI \_ 格式 \_ BC4 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="6933c-314">DXGI\_FORMAT\_BC4\_SNORM</span></span><br/>                                               |
| <span data-ttu-id="6933c-315">128</span><span class="sxs-lookup"><span data-stu-id="6933c-315">128</span></span>       | <span data-ttu-id="6933c-316">DXGI \_ 格式 \_ R32G32B32A32 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="6933c-316">DXGI\_FORMAT\_R32G32B32A32\_UINT</span></span><br/> <span data-ttu-id="6933c-317">DXGI \_ 格式 \_ R32G32B32A32 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="6933c-317">DXGI\_FORMAT\_R32G32B32A32\_SINT</span></span><br/>                                                                             | <span data-ttu-id="6933c-318">DXGI \_ 格式 \_ BC2 \_ UNORM \[ \_ SRGB\]</span><span class="sxs-lookup"><span data-stu-id="6933c-318">DXGI\_FORMAT\_BC2\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="6933c-319">DXGI \_ 格式 \_ BC3 \_ UNORM \[ \_ SRGB\]</span><span class="sxs-lookup"><span data-stu-id="6933c-319">DXGI\_FORMAT\_BC3\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="6933c-320">DXGI \_ 格式 \_ BC5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="6933c-320">DXGI\_FORMAT\_BC5\_UNORM</span></span><br/> <span data-ttu-id="6933c-321">DXGI \_ 格式 \_ BC5 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="6933c-321">DXGI\_FORMAT\_BC5\_SNORM</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="6933c-322">相關主題</span><span class="sxs-lookup"><span data-stu-id="6933c-322">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6933c-323"> (Direct3D 10) 的資源 </span><span class="sxs-lookup"><span data-stu-id="6933c-323">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
