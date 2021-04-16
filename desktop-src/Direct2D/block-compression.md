---
title: 區塊壓縮
description: 描述區塊壓縮的運作方式，以及如何在 WIC 和 Direct2D 中使用它。
ms.assetid: 52AF86A5-16E8-4AC8-BB67-CC2F1A3635B5
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: aeb6ba9427a04f7a251a1d59062be508e4249b41
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2021
ms.locfileid: "104514268"
---
# <a name="block-compression"></a><span data-ttu-id="b7b93-103">區塊壓縮</span><span class="sxs-lookup"><span data-stu-id="b7b93-103">Block compression</span></span>

<span data-ttu-id="b7b93-104">從 Windows 8.1 開始，Direct2D 支援數個區塊壓縮的像素格式。</span><span class="sxs-lookup"><span data-stu-id="b7b93-104">Starting with Windows 8.1, Direct2D supports several block compressed pixel formats.</span></span> <span data-ttu-id="b7b93-105">此外，Windows 8.1 包含新的 Windows 影像處理元件 (WIC) DDS 編解碼器，以啟用以 DDS 檔案格式載入和儲存區塊壓縮的影像。</span><span class="sxs-lookup"><span data-stu-id="b7b93-105">In addition, Windows 8.1 contains a new Windows Imaging Component (WIC) DDS codec to enable loading and storing block compressed images in the DDS file format.</span></span> <span data-ttu-id="b7b93-106">「封鎖壓縮」是一種技術，可減少點陣圖內容所耗用的圖形記憶體量。</span><span class="sxs-lookup"><span data-stu-id="b7b93-106">Block compression is a technique for reducing the amount of graphics memory that is consumed by bitmap content.</span></span> <span data-ttu-id="b7b93-107">使用區塊壓縮時，您的應用程式可以減少相同解析度影像的記憶體耗用量和載入時間。</span><span class="sxs-lookup"><span data-stu-id="b7b93-107">By using block compression, your app can reduce memory consumption and load times for the same resolution images.</span></span> <span data-ttu-id="b7b93-108">或者，您的應用程式可以使用更多或更高的解析度影像，同時仍然耗用相同的 GPU 記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="b7b93-108">Or, your app can use more or higher resolution images while still consuming the same GPU memory footprint.</span></span>

<span data-ttu-id="b7b93-109">由於 Direct3D 應用程式已有一段很長的時間可以使用區塊壓縮，而 Windows 8.1 也提供給主流和 Direct2D 的應用程式開發人員使用。</span><span class="sxs-lookup"><span data-stu-id="b7b93-109">Block compression has been used by Direct3D applications for a long time, and with Windows 8.1 is available to mainstream and Direct2D application developers as well.</span></span>

<span data-ttu-id="b7b93-110">本主題說明 block 壓縮的運作方式，以及如何在 WIC 和 Direct2D 中使用它。</span><span class="sxs-lookup"><span data-stu-id="b7b93-110">This topic describes how block compression works and how to use it in WIC and Direct2D.</span></span>

## <a name="about-block-compression"></a><span data-ttu-id="b7b93-111">關於區塊壓縮</span><span class="sxs-lookup"><span data-stu-id="b7b93-111">About Block Compression</span></span>

<span data-ttu-id="b7b93-112">[區塊壓縮](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression) (BC) 指的是減少材質大小的一種壓縮技術。</span><span class="sxs-lookup"><span data-stu-id="b7b93-112">[Block Compression](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression) (BC) refers to a class of compression techniques for reducing texture sizes.</span></span> <span data-ttu-id="b7b93-113">根據功能等級，Direct3D 11 最多可支援7種不同的 BC 格式。</span><span class="sxs-lookup"><span data-stu-id="b7b93-113">Direct3D 11 supports up to 7 different BC formats depending on feature level.</span></span> <span data-ttu-id="b7b93-114">在 Windows 8.1 Direct2D 引進 BC1、BC2 和 BC3 格式的支援，這些格式可在所有功能層級中使用。</span><span class="sxs-lookup"><span data-stu-id="b7b93-114">In Windows 8.1 Direct2D introduces support for the BC1, BC2 and BC3 formats which are available across all feature levels.</span></span>

### <a name="how-block-compression-works"></a><span data-ttu-id="b7b93-115">區塊壓縮的運作方式</span><span class="sxs-lookup"><span data-stu-id="b7b93-115">How Block Compression works</span></span>

<span data-ttu-id="b7b93-116">區塊壓縮格式全都使用相同的基本技術來減少色彩資料所耗用的空間。</span><span class="sxs-lookup"><span data-stu-id="b7b93-116">The block compressed formats all use the same basic technique to reduce the space consumed by color data.</span></span> <span data-ttu-id="b7b93-117">本節摘要說明最簡單的演算法 BC1。</span><span class="sxs-lookup"><span data-stu-id="b7b93-117">This section summarizes the simplest algorithm, BC1.</span></span> <span data-ttu-id="b7b93-118">如需更詳細的說明，請參閱 [區塊壓縮](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11)。</span><span class="sxs-lookup"><span data-stu-id="b7b93-118">For a more detailed explanation, see [Block Compression](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11).</span></span>

<span data-ttu-id="b7b93-119">首先，映射會分成4個圖元的區塊。</span><span class="sxs-lookup"><span data-stu-id="b7b93-119">First, the image is divided into blocks of 4 by 4 pixels.</span></span> <span data-ttu-id="b7b93-120">每個區塊會分開壓縮。</span><span class="sxs-lookup"><span data-stu-id="b7b93-120">Each block is compressed separately.</span></span>

> [!Note]  
> <span data-ttu-id="b7b93-121">這表示影像的寬度和高度必須是4圖元的倍數，以封鎖壓縮。</span><span class="sxs-lookup"><span data-stu-id="b7b93-121">This means an image’s width and height must each be a multiple of 4 pixel for it to be block compressed.</span></span>

 

<span data-ttu-id="b7b93-122">此範例影像顯示影像內的4x4 圖元區塊。</span><span class="sxs-lookup"><span data-stu-id="b7b93-122">This example image shows a 4x4 pixel block within an image.</span></span>

![範例影像顯示影像內的4x4 圖元區塊。](images/dds1.png)

<span data-ttu-id="b7b93-124">接下來，在 4 x 4 區塊中，選取兩個「參考」色彩，並將其編碼為 2 16 位值 (5 位紅色、6位綠色、5位藍色) 。</span><span class="sxs-lookup"><span data-stu-id="b7b93-124">Next, within a 4 by 4 block, two “reference” colors are selected and are encoded as two 16 bit values (5 bits red, 6 bits green, 5 bits blue).</span></span> <span data-ttu-id="b7b93-125">這些色彩的選擇會大幅影響影像品質，而且重要。</span><span class="sxs-lookup"><span data-stu-id="b7b93-125">The choice of these colors significantly affects image quality and is nontrivial.</span></span> <span data-ttu-id="b7b93-126">兩個中繼色彩的計算方式是在 RGB 色彩空間中兩個參考色彩之間的線性插即用。</span><span class="sxs-lookup"><span data-stu-id="b7b93-126">Two intermediate colors are calculated by linearly interpolating between the two reference colors in the RGB color space.</span></span> <span data-ttu-id="b7b93-127">這總共會產生四個不同的可能色彩：每個色彩都會指派兩個位的索引值。</span><span class="sxs-lookup"><span data-stu-id="b7b93-127">This produces a total of 4 different possible colors; each color is assigned a two bit index value.</span></span> <span data-ttu-id="b7b93-128">不過，請注意，只有兩個端點色彩需要儲存，因為插補是固定的。</span><span class="sxs-lookup"><span data-stu-id="b7b93-128">However, note that only the two endpoint colors need to be stored as the interpolation is fixed.</span></span>

<span data-ttu-id="b7b93-129">在此圖中，會選取色彩0和3作為區塊的「參考」色彩，而色彩1和2則是使用線性插補來計算。</span><span class="sxs-lookup"><span data-stu-id="b7b93-129">In this figure, colors 0 and 3 are selected as “reference” colors for the block, while colors 1 and 2 are calculated using linear interpolation.</span></span>

![顯示代表區塊的4個色彩值計算的圖表。](images/dds2.png)

<span data-ttu-id="b7b93-131">最後，區塊中的每個圖元都會對應到其中四個先前計算的色彩之一，而且每個圖元都會使用兩個位索引值進行編碼。</span><span class="sxs-lookup"><span data-stu-id="b7b93-131">Finally, every pixel in the block is mapped to one of the four previously calculated colors, and each pixel is encoded using the two bit index value.</span></span>

<span data-ttu-id="b7b93-132">用來代表這些16圖元的資料總量如下：</span><span class="sxs-lookup"><span data-stu-id="b7b93-132">The total amount of data used to represent these 16 pixels is:</span></span>

`16 bits [to define a reference color] * 2 + 2 bits * 16 [number of pixels]  = 64 bits`

<span data-ttu-id="b7b93-133">這會產生每圖元4個位的平均密度。</span><span class="sxs-lookup"><span data-stu-id="b7b93-133">This results in an average density of 4 bits per pixel.</span></span> <span data-ttu-id="b7b93-134">相較之下，common DXGI \_ format \_ B8G8R8A8 \_ UNORM 像素格式耗用每圖元32位。</span><span class="sxs-lookup"><span data-stu-id="b7b93-134">For comparison, the common DXGI\_FORMAT\_B8G8R8A8\_UNORM pixel format consumes 32 bits per pixel.</span></span>

<span data-ttu-id="b7b93-135">下圖顯示每個圖元都會編碼為2位索引。</span><span class="sxs-lookup"><span data-stu-id="b7b93-135">This diagram shows that each pixel is encoded as a 2 bit index.</span></span> <span data-ttu-id="b7b93-136">整個區塊會以64位編碼。</span><span class="sxs-lookup"><span data-stu-id="b7b93-136">The entire block is encoded in 64 bits.</span></span>

![計算4個色彩值以表示區塊。](images/dds3.png)

<span data-ttu-id="b7b93-138">有各種不同的支援 Alpha 資料和不同的色彩通道數目。</span><span class="sxs-lookup"><span data-stu-id="b7b93-138">There are variations to support alpha data and varying numbers of color channels.</span></span> <span data-ttu-id="b7b93-139">BC6H 和 BC7 會使用明顯不同的演算法，以支援高動態範圍 (HDR) 內容，並分別增加影像品質。</span><span class="sxs-lookup"><span data-stu-id="b7b93-139">BC6H and BC7 use significantly different algorithms in order to support high dynamic range (HDR) content and increase image quality, respectively.</span></span>

### <a name="directdraw-surface-dds-file-format"></a><span data-ttu-id="b7b93-140">DirectDraw 介面 (DDS) 檔案格式</span><span class="sxs-lookup"><span data-stu-id="b7b93-140">DirectDraw Surface (DDS) file format</span></span>

<span data-ttu-id="b7b93-141">區塊壓縮資料通常儲存在 [DirectDraw 介面 (DDS) ](/windows/desktop/direct3ddds/dx-graphics-dds-reference) 檔。</span><span class="sxs-lookup"><span data-stu-id="b7b93-141">Block compressed data is typically stored in [DirectDraw Surface (DDS)](/windows/desktop/direct3ddds/dx-graphics-dds-reference) files.</span></span> <span data-ttu-id="b7b93-142">如果您是 Direct3D 開發人員，您可能很熟悉 DDS 檔。</span><span class="sxs-lookup"><span data-stu-id="b7b93-142">You may be familiar with DDS files if you are a Direct3D developer.</span></span> <span data-ttu-id="b7b93-143">請注意，Direct2D 只支援特定的 DDS 功能;如需詳細資訊，請參閱 [DDS 需求](#dds-requirements)。</span><span class="sxs-lookup"><span data-stu-id="b7b93-143">Note that Direct2D only supports certain DDS features; for more information see [DDS Requirements](#dds-requirements).</span></span>

### <a name="advantages-of-block-compression"></a><span data-ttu-id="b7b93-144">區塊壓縮的優點</span><span class="sxs-lookup"><span data-stu-id="b7b93-144">Advantages of block compression</span></span>

<span data-ttu-id="b7b93-145">封鎖壓縮格式與常見的產業影像壓縮格式不同，例如 JPEG，這類的 BC 格式會由新式 Gpu 原生支援。</span><span class="sxs-lookup"><span data-stu-id="b7b93-145">Block compressed formats differ from common industry image compression formats such as JPEG in that BC formats are natively supported by modern GPUs.</span></span> <span data-ttu-id="b7b93-146">這表示您可以直接將區塊壓縮的影像載入至 GPU，而不需要任何解碼或解壓縮。</span><span class="sxs-lookup"><span data-stu-id="b7b93-146">This means that you can directly load a block compressed image onto the GPU without any decoding or decompression.</span></span> <span data-ttu-id="b7b93-147">BC 格式平均耗用每圖元4到8位;相較于一般未壓縮的32位的每個圖元 BGRA 點陣圖，這會導致記憶體節省75% 到87.5%。</span><span class="sxs-lookup"><span data-stu-id="b7b93-147">BC formats consume from 4 to 8 bits per pixel on average; when compared to a typical uncompressed 32 bit per pixel BGRA bitmap, this results in memory savings of 75% to 87.5%.</span></span> <span data-ttu-id="b7b93-148">此外，由於沒有解碼步驟，相較于 JPEG 格式，載入 BC 映射的時間會大幅減少。</span><span class="sxs-lookup"><span data-stu-id="b7b93-148">Also, because there is no decode step, the time to load a BC image is significantly reduced compared to formats like JPEG.</span></span>

### <a name="when-to-use-block-compression"></a><span data-ttu-id="b7b93-149">使用區塊壓縮的時機</span><span class="sxs-lookup"><span data-stu-id="b7b93-149">When to use Block Compression</span></span>

<span data-ttu-id="b7b93-150">如果您想要減少點陣圖的記憶體耗用量，或想要減少解碼和載入時間，您應該考慮在應用程式中使用區塊壓縮影像，而不是其他格式，例如 JPEG。</span><span class="sxs-lookup"><span data-stu-id="b7b93-150">You should consider using block compressed images in your app instead of other formats such as JPEG if you want to reduce the memory consumption of bitmaps or want to reduce decode and load times.</span></span>

<span data-ttu-id="b7b93-151">不過，區塊壓縮並非適用于所有情況，而且需要一些取捨。</span><span class="sxs-lookup"><span data-stu-id="b7b93-151">However, block compression is not appropriate for all cases and requires some tradeoffs.</span></span> <span data-ttu-id="b7b93-152">首先，區塊壓縮演算法會有損量。</span><span class="sxs-lookup"><span data-stu-id="b7b93-152">First, the block compression algorithms are lossy.</span></span> <span data-ttu-id="b7b93-153">區塊壓縮適用于自然的影像內容，但可能會將不需要的視覺效果成品引入具有清晰、高對比界線的影像，例如電腦產生的螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="b7b93-153">Block compression works well with natural photographic content but can introduce unwanted visual artifacts into images with sharp, high contrast boundaries, such as computer-generated screenshots.</span></span> <span data-ttu-id="b7b93-154">您應該確定您的區塊壓縮影像資產在使用影像品質之前都具有可接受的影像品質。</span><span class="sxs-lookup"><span data-stu-id="b7b93-154">You should ensure that your block compressed image assets have acceptable image quality before using them.</span></span>

<span data-ttu-id="b7b93-155">其次，封鎖壓縮的 DDS 檔案通常會在磁片上耗用比可比較的 JPEG 影像更多的空間。</span><span class="sxs-lookup"><span data-stu-id="b7b93-155">Second, block compressed DDS files generally consume more space on disk than comparable JPEG images.</span></span> <span data-ttu-id="b7b93-156">這將會增加您應用程式的套件大小和網路頻寬需求。</span><span class="sxs-lookup"><span data-stu-id="b7b93-156">This in turn will increase your app’s package size and network bandwidth requirements.</span></span>

## <a name="using-block-compression"></a><span data-ttu-id="b7b93-157">使用區塊壓縮</span><span class="sxs-lookup"><span data-stu-id="b7b93-157">Using Block Compression</span></span>

<span data-ttu-id="b7b93-158">本節說明如何在 Direct2D 應用程式中產生和使用封鎖壓縮的資產。</span><span class="sxs-lookup"><span data-stu-id="b7b93-158">This section explains how to generate and use block compressed assets in a Direct2D app.</span></span>

### <a name="overview"></a><span data-ttu-id="b7b93-159">概觀</span><span class="sxs-lookup"><span data-stu-id="b7b93-159">Overview</span></span>

<span data-ttu-id="b7b93-160">區塊壓縮的 DDS 檔案是執行時間優化的格式，表示它們已特別針對應用程式執行時間的良好效能進行優化。</span><span class="sxs-lookup"><span data-stu-id="b7b93-160">Block compressed DDS files are a runtime-optimized format, meaning that they are specifically optimized for good performance at app runtime.</span></span> <span data-ttu-id="b7b93-161">建議您繼續使用現有的資產建立和編輯管線，並只在您將它們匯入至應用程式專案時或在組建階段時，轉換成區塊壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="b7b93-161">We recommend that you continue to use your existing asset creation and editing pipeline, and only convert to a block compressed format when you import them into your application project, or at build time.</span></span>

### <a name="dds-requirements"></a><span data-ttu-id="b7b93-162">DDS 需求</span><span class="sxs-lookup"><span data-stu-id="b7b93-162">DDS requirements</span></span>

<span data-ttu-id="b7b93-163">DDS 檔案格式的設計目的是要支援 Direct3D 中使用的各種功能。</span><span class="sxs-lookup"><span data-stu-id="b7b93-163">The DDS file format was designed to support a wide range of features used in Direct3D.</span></span> <span data-ttu-id="b7b93-164">Direct2D 只會使用這些功能的子集。</span><span class="sxs-lookup"><span data-stu-id="b7b93-164">Direct2D only uses a subset of these features.</span></span> <span data-ttu-id="b7b93-165">因此，當您建立要與 Direct2D 搭配使用的 DDS 映射時，必須記住下列限制：</span><span class="sxs-lookup"><span data-stu-id="b7b93-165">Therefore when you are creating DDS images for use with Direct2D, you must keep in mind the following restrictions:</span></span>

-   <span data-ttu-id="b7b93-166">只允許下列 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 值：</span><span class="sxs-lookup"><span data-stu-id="b7b93-166">Only the following [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) values are allowed:</span></span>
    -   <span data-ttu-id="b7b93-167">DXGI \_ 格式 \_ BC1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="b7b93-167">DXGI\_FORMAT\_BC1\_UNORM</span></span>
    -   <span data-ttu-id="b7b93-168">DXGI \_ 格式 \_ BC2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="b7b93-168">DXGI\_FORMAT\_BC2\_UNORM</span></span>
    -   <span data-ttu-id="b7b93-169">DXGI \_ 格式 \_ BC3 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="b7b93-169">DXGI\_FORMAT\_BC3\_UNORM</span></span>
-   <span data-ttu-id="b7b93-170">必須使用預乘的 Alpha 資料。</span><span class="sxs-lookup"><span data-stu-id="b7b93-170">Premultiplied alpha data must be used.</span></span> <span data-ttu-id="b7b93-171">這包括舊版的 DDS 檔，其使用的格式會明確定義預乘的 Alpha (DXT1、DXT2、DXT4) ，以及使用 dds \_ 標頭 \_ DX10 結構與 dds \_ Alpha \_ 模式不 \_ 透明和 dds \_ ALPHA \_ 模式預先設置值 \_ 的 dds 檔案。</span><span class="sxs-lookup"><span data-stu-id="b7b93-171">This includes legacy DDS files using formats that explicitly define premultiplied alpha (DXT1, DXT2, DXT4), as well as DDS files that use the DDS\_HEADER\_DX10 structure with the DDS\_ALPHA\_MODE\_OPAQUE and DDS\_ALPHA\_MODE\_PREMULTIPLIED values.</span></span>
-   <span data-ttu-id="b7b93-172">X 和 Y 維度必須是4圖元的倍數。</span><span class="sxs-lookup"><span data-stu-id="b7b93-172">The X and Y dimensions must be multiples of 4 pixels.</span></span>
-   <span data-ttu-id="b7b93-173">不允許使用磁片區紋理、cubemaps、mipmap 或紋理陣列。</span><span class="sxs-lookup"><span data-stu-id="b7b93-173">Volume textures, cubemaps, mipmaps, or texture arrays are not allowed.</span></span> <span data-ttu-id="b7b93-174">您應該只使用單一畫面格來源影像。</span><span class="sxs-lookup"><span data-stu-id="b7b93-174">You should only use single frame source images.</span></span>

### <a name="generating-block-compressed-assets"></a><span data-ttu-id="b7b93-175">產生區塊壓縮的資產</span><span class="sxs-lookup"><span data-stu-id="b7b93-175">Generating Block Compressed assets</span></span>

<span data-ttu-id="b7b93-176">有各種不同的 DDS 撰寫工具可用來建立或轉換區塊壓縮的 DDS 檔。</span><span class="sxs-lookup"><span data-stu-id="b7b93-176">There are a variety of DDS authoring tools available to create or convert block compressed DDS files.</span></span> <span data-ttu-id="b7b93-177">請注意，並非所有工具都支援搭配 Direct2D 使用 DDS 檔案的需求，如上一節中所述。</span><span class="sxs-lookup"><span data-stu-id="b7b93-177">Note not all tools support the requirements for using DDS files with Direct2D, as detailed in the previous section.</span></span>

<span data-ttu-id="b7b93-178">從 Visual Studio 2013 開始，您可以 Visual Studio 將 JPEG 和 PNG 等現有的視覺效果資產轉換成正確的 DDS 區塊壓縮格式，做為組建程式的自動部分。</span><span class="sxs-lookup"><span data-stu-id="b7b93-178">Beginning with Visual Studio 2013, you can have Visual Studio convert existing visual assets such as JPEG and PNG to the correct DDS block compressed format as an automatic part of your build process.</span></span> <span data-ttu-id="b7b93-179">這是使用「影像內容工作」自訂群組建步驟來完成的。</span><span class="sxs-lookup"><span data-stu-id="b7b93-179">This is accomplished using the Image Content Task custom build step.</span></span>

<span data-ttu-id="b7b93-180">如需如何為您的專案設定此專案的詳細資訊，請參閱： [如何：匯出材質以搭配 Direct2D 或 JAVAscipt Apps 使用](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120))。</span><span class="sxs-lookup"><span data-stu-id="b7b93-180">For information on how to set this up for your project, see: [How to: Export a Texture for Use with Direct2D or Javascipt Apps](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120)).</span></span>

### <a name="direct2d-apis"></a><span data-ttu-id="b7b93-181">Direct2D Api</span><span class="sxs-lookup"><span data-stu-id="b7b93-181">Direct2D APIs</span></span>

<span data-ttu-id="b7b93-182">Windows 8.1 中的 Direct2D 會更新為支援下列像素格式：</span><span class="sxs-lookup"><span data-stu-id="b7b93-182">Direct2D is updated in Windows 8.1 to support the following pixel formats:</span></span>

-   <span data-ttu-id="b7b93-183">DXGI \_ 格式 \_ BC1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="b7b93-183">DXGI\_FORMAT\_BC1\_UNORM</span></span>
-   <span data-ttu-id="b7b93-184">DXGI \_ 格式 \_ BC2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="b7b93-184">DXGI\_FORMAT\_BC2\_UNORM</span></span>
-   <span data-ttu-id="b7b93-185">DXGI \_ 格式 \_ BC3 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="b7b93-185">DXGI\_FORMAT\_BC3\_UNORM</span></span>

<span data-ttu-id="b7b93-186">針對上述格式，您必須使用預乘 Alpha。</span><span class="sxs-lookup"><span data-stu-id="b7b93-186">For the preceding formats, you must use premultiplied alpha.</span></span> <span data-ttu-id="b7b93-187">此外，這些格式只適用于作為來源，而不是目標。</span><span class="sxs-lookup"><span data-stu-id="b7b93-187">In addition, these formats are only valid for use as a source, not a target.</span></span> <span data-ttu-id="b7b93-188">例如，這表示您可以使用 BC1 （而不是裝置內容）來建立 Direct2D 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="b7b93-188">For example, this means that you can create a Direct2D bitmap using BC1, but not a device context.</span></span>

<span data-ttu-id="b7b93-189">Windows 8.1 中的下列方法會更新以支援 BC 格式：</span><span class="sxs-lookup"><span data-stu-id="b7b93-189">The following methods are updated in Windows 8.1 to support BC formats:</span></span>

-   [<span data-ttu-id="b7b93-190">**ID2D1DeviceCoNtext::IsDxgiFormatSupported**</span><span class="sxs-lookup"><span data-stu-id="b7b93-190">**ID2D1DeviceContext::IsDxgiFormatSupported**</span></span>](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported)
-   <span data-ttu-id="b7b93-191">[**ID2D1DeviceCoNtext::CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))</span><span class="sxs-lookup"><span data-stu-id="b7b93-191">[**ID2D1DeviceContext::CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))</span></span>
-   <span data-ttu-id="b7b93-192">[**ID2D1DeviceCoNtext::CreateBitmapFromDxgiSurface**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1))</span><span class="sxs-lookup"><span data-stu-id="b7b93-192">[**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1))</span></span>
-   [<span data-ttu-id="b7b93-193">**ID2D1RenderTarget::CreateSharedBitmap**</span><span class="sxs-lookup"><span data-stu-id="b7b93-193">**ID2D1RenderTarget::CreateSharedBitmap**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)
-   [<span data-ttu-id="b7b93-194">**ID2D1RenderTarget::CreateBitmapFromWicBitmap**</span><span class="sxs-lookup"><span data-stu-id="b7b93-194">**ID2D1RenderTarget::CreateBitmapFromWicBitmap**</span></span>](id2d1rendertarget-createbitmapfromwicbitmap.md)
-   [<span data-ttu-id="b7b93-195">**ID2D1Bitmap::CopyFromMemory**</span><span class="sxs-lookup"><span data-stu-id="b7b93-195">**ID2D1Bitmap::CopyFromMemory**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)
-   [<span data-ttu-id="b7b93-196">**ID2D1Bitmap::CopyFromBitmap**</span><span class="sxs-lookup"><span data-stu-id="b7b93-196">**ID2D1Bitmap::CopyFromBitmap**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [<span data-ttu-id="b7b93-197">**ID2D1Bitmap1::GetSurface**</span><span class="sxs-lookup"><span data-stu-id="b7b93-197">**ID2D1Bitmap1::GetSurface**</span></span>](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-getsurface)

<span data-ttu-id="b7b93-198">請注意， [**CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md) 會採用 [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) 作為介面;不過，在 Windows 8.1 WIC 不支援從 **IWICBitmapSource** 取得區塊壓縮資料，而且沒有對應至 DXGI \_ 格式 \_ BC1 UNORM 等的 WIC 像素格式 \_ 。相反地， **CreateBitmapFromWicBitmap** 會判斷 **IWICBitmapSource** 是否為有效的 DDS [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) ，並直接載入區塊壓縮的資料。</span><span class="sxs-lookup"><span data-stu-id="b7b93-198">Note that [**CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md) takes [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) as an interface; however in Windows 8.1 WIC does not support obtaining block compressed data from **IWICBitmapSource**, and there is no WIC pixel format corresponding to DXGI\_FORMAT\_BC1\_UNORM, etc. Instead, **CreateBitmapFromWicBitmap** determines if the **IWICBitmapSource** is a valid DDS [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) and directly loads the block compressed data.</span></span> <span data-ttu-id="b7b93-199">您可以在 [**D2D1 \_ 點陣圖 \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) 結構中明確指定像素格式，或允許 Direct2D 自動判斷正確的格式。</span><span class="sxs-lookup"><span data-stu-id="b7b93-199">You can either explicitly specify the pixel format in the [**D2D1\_BITMAP\_PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) struct, or allow Direct2D to automatically determine the correct format.</span></span>

### <a name="windows-imaging-component-apis"></a><span data-ttu-id="b7b93-200">Windows 影像處理元件 Api</span><span class="sxs-lookup"><span data-stu-id="b7b93-200">Windows Imaging Component APIs</span></span>

<span data-ttu-id="b7b93-201">Windows 影像處理元件 (WIC) 會在 Windows 8.1 中加入新的 DDS 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="b7b93-201">The Windows Imaging Component (WIC) adds a new DDS codec in Windows 8.1.</span></span> <span data-ttu-id="b7b93-202">此外，它還新增了支援存取 DDS 特定資料的新介面，包括區塊壓縮的圖元資料：</span><span class="sxs-lookup"><span data-stu-id="b7b93-202">In addition, it adds new interfaces that support accessing DDS-specific data, including block compressed pixel data:</span></span>

-   [<span data-ttu-id="b7b93-203">**IWICDdsDecoder**</span><span class="sxs-lookup"><span data-stu-id="b7b93-203">**IWICDdsDecoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicddsdecoder)
-   [<span data-ttu-id="b7b93-204">**IWICDdsEncoder**</span><span class="sxs-lookup"><span data-stu-id="b7b93-204">**IWICDdsEncoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicddsencoder)
-   [<span data-ttu-id="b7b93-205">**IWICDdsFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="b7b93-205">**IWICDdsFrameDecode**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="block-compressed-wic-pixel-formats"></a><span data-ttu-id="b7b93-206">封鎖壓縮的 WIC 像素格式</span><span class="sxs-lookup"><span data-stu-id="b7b93-206">Block Compressed WIC pixel formats</span></span>

<span data-ttu-id="b7b93-207">Windows 8.1 中沒有新的 WIC 區塊壓縮的像素格式。</span><span class="sxs-lookup"><span data-stu-id="b7b93-207">There are no new WIC block compressed pixel formats in Windows 8.1.</span></span> <span data-ttu-id="b7b93-208">相反地，如果您從 DDS 解碼器取得 [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) 並呼叫 [**CopyPixels**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels)，您將會收到標準的未壓縮圖元，例如 WICPixelFormat32bppPBGRA。</span><span class="sxs-lookup"><span data-stu-id="b7b93-208">Instead, if you obtain an [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) from the DDS decoder and call [**CopyPixels**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels), you will receive standard uncompressed pixels such as WICPixelFormat32bppPBGRA.</span></span> <span data-ttu-id="b7b93-209">您可以使用 [**IWICDdsFrameDecode：： CopyBlocks**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsframedecode-copyblocks) ，以來自 DDS 檔案的記憶體緩衝區形式取得原始區塊壓縮的資料。</span><span class="sxs-lookup"><span data-stu-id="b7b93-209">You can use [**IWICDdsFrameDecode::CopyBlocks**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsframedecode-copyblocks) to obtain the raw block compressed data in the form of a memory buffer from a DDS file.</span></span>

### <a name="multi-frame-dds-access"></a><span data-ttu-id="b7b93-210">多框架 DDS 存取</span><span class="sxs-lookup"><span data-stu-id="b7b93-210">Multi-frame DDS access</span></span>

<span data-ttu-id="b7b93-211">DDS 檔案格式允許將多個相關的影像儲存在單一檔案中。</span><span class="sxs-lookup"><span data-stu-id="b7b93-211">The DDS file format allows for multiple related images to be stored in a single file.</span></span> <span data-ttu-id="b7b93-212">例如，DDS 檔案可能包含立方體貼圖、磁片區材質或材質陣列，這些都可以 mipmapped。</span><span class="sxs-lookup"><span data-stu-id="b7b93-212">For example, a DDS file may contain a cubemap, volume texture, or texture array, all of which can be mipmapped.</span></span> <span data-ttu-id="b7b93-213">在 Direct3D 中，這些多個映射會公開為子資源。</span><span class="sxs-lookup"><span data-stu-id="b7b93-213">In Direct3D, these multiple images are exposed as subresources.</span></span> <span data-ttu-id="b7b93-214">在 WIC 中，會將多個映射公開為框架， ([**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) 和 [**IWICBitmapFrameEncode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode)) 。</span><span class="sxs-lookup"><span data-stu-id="b7b93-214">In WIC, multiple images are exposed as frames ([**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) and [**IWICBitmapFrameEncode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode)).</span></span>

<span data-ttu-id="b7b93-215">WIC 只支援一維框架陣列的概念，而 DDS 支援三個獨立的維度 (但只有兩個可用於任何一個檔案) 。</span><span class="sxs-lookup"><span data-stu-id="b7b93-215">WIC only supports the notion of a single dimensional array of frames, while DDS supports three independent dimensions (although only two may be used in any one file).</span></span> <span data-ttu-id="b7b93-216">WIC 提供便利的方法，協助您在 DDS subresource 和 WIC 框架之間進行對應。</span><span class="sxs-lookup"><span data-stu-id="b7b93-216">WIC provides convenience methods to assist with mapping between a DDS subresource and WIC frame.</span></span> <span data-ttu-id="b7b93-217">針對解碼， [**IWICDdsDecoder：： GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsdecoder-getframe) 可讓您指定 subresource 的陣列索引、mip 層級和配量索引，並傳回正確的 WIC 框架。</span><span class="sxs-lookup"><span data-stu-id="b7b93-217">For decoding, [**IWICDdsDecoder::GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsdecoder-getframe) lets you specify the array index, mip level and slice index of the subresource, and returns the correct WIC frame.</span></span>

<span data-ttu-id="b7b93-218">針對編碼， [**IWICDdsEncoder：： CreateNewFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-createnewframe) 會在您建立新的框架時，計算產生的陣列索引、mip 層級和配量索引。</span><span class="sxs-lookup"><span data-stu-id="b7b93-218">For encoding, [**IWICDdsEncoder::CreateNewFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-createnewframe) computes the resulting array index, mip level and slice index when you create a new frame.</span></span> <span data-ttu-id="b7b93-219">您必須先呼叫 [**IWICDdsEncoder：： SetParameters**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-setparameters) 來定義 DDS 特定的檔案參數。</span><span class="sxs-lookup"><span data-stu-id="b7b93-219">You must have first called [**IWICDdsEncoder::SetParameters**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-setparameters) to define the DDS-specific file parameters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7b93-220">相關主題</span><span class="sxs-lookup"><span data-stu-id="b7b93-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b7b93-221">[如何：匯出材質以搭配 Direct2D 或 Javascipt 應用程式使用](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="b7b93-221">[How to: Export a Texture for Use with Direct2D or Javascipt Apps](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120))</span></span>
</dt> <dt>

[<span data-ttu-id="b7b93-222">DDS 的參考</span><span class="sxs-lookup"><span data-stu-id="b7b93-222">Reference for DDS</span></span>](/windows/desktop/direct3ddds/dx-graphics-dds-reference)
</dt> <dt>

[<span data-ttu-id="b7b93-223">區塊壓縮</span><span class="sxs-lookup"><span data-stu-id="b7b93-223">Block Compression</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> </dl>

 

 