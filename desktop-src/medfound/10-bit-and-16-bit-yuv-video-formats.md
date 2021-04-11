---
description: 本主題說明在 Microsoft Windows 作業系統中，建議用來捕捉、處理及顯示影片的10和16位 YUV 格式。
ms.assetid: fcaaaa6f-f886-4f6e-9c3c-e513ccc90d37
title: 10位和16位 YUV 影片格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbc357653848cd51ce6f56ebd8a1da3e5f60403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113444"
---
# <a name="10-bit-and-16-bit-yuv-video-formats"></a><span data-ttu-id="b8c2e-103">10位和16位 YUV 影片格式</span><span class="sxs-lookup"><span data-stu-id="b8c2e-103">10-bit and 16-bit YUV Video Formats</span></span>

<span data-ttu-id="b8c2e-104">本主題說明在 Microsoft Windows 作業系統中，建議用來捕捉、處理及顯示影片的10和16位 YUV 格式。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-104">This topic describes the 10- and 16-bit YUV formats that are recommended for capturing, processing, and displaying video in the Microsoft Windows operating system.</span></span>

<span data-ttu-id="b8c2e-105">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="b8c2e-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b8c2e-106">概觀</span><span class="sxs-lookup"><span data-stu-id="b8c2e-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="b8c2e-107">10位和16位 YUV 的 FOURCC 碼</span><span class="sxs-lookup"><span data-stu-id="b8c2e-107">FOURCC Codes For 10-Bit and 16-Bit YUV</span></span>](#fourcc-codes-for-10-bit-and-16-bit-yuv)
-   [<span data-ttu-id="b8c2e-108">介面定義</span><span class="sxs-lookup"><span data-stu-id="b8c2e-108">Surface Definitions</span></span>](#surface-definitions)
    -   [<span data-ttu-id="b8c2e-109">4:2:0 格式</span><span class="sxs-lookup"><span data-stu-id="b8c2e-109">4:2:0 Formats</span></span>](#420-formats)
    -   [<span data-ttu-id="b8c2e-110">4:2:2 格式</span><span class="sxs-lookup"><span data-stu-id="b8c2e-110">4:2:2 Formats</span></span>](#422-formats)
    -   [<span data-ttu-id="b8c2e-111">4:4:4 格式</span><span class="sxs-lookup"><span data-stu-id="b8c2e-111">4:4:4 Formats</span></span>](#444-formats)
-   [<span data-ttu-id="b8c2e-112">慣用的 YUV 格式</span><span class="sxs-lookup"><span data-stu-id="b8c2e-112">Preferred YUV Formats</span></span>](#preferred-yuv-formats)
-   [<span data-ttu-id="b8c2e-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8c2e-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="b8c2e-114">概觀</span><span class="sxs-lookup"><span data-stu-id="b8c2e-114">Overview</span></span>

<span data-ttu-id="b8c2e-115">這些格式會針對 luma 通道和色度 (C'b 和 C'r) 通道使用固定點標記法。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-115">These formats use a fixed-point representation for both the luma channel and the chroma (C'b and C'r) channels.</span></span> <span data-ttu-id="b8c2e-116">範例值是使用 2 ^ (n − 8) 的縮放比例來調整，其中 n 為10或16，每個區段為 7.7-7.8 和 7.11-7.12 的 SMPTE 274M。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-116">Sample values are scaled 8-bit values, using a scaling factor of 2^(n − 8), where n is either 10 or 16, as per sections 7.7-7.8 and 7.11-7.12 of SMPTE 274M.</span></span> <span data-ttu-id="b8c2e-117">精確度轉換可以使用簡單的位移位來執行。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-117">Precision conversions can be performed using simple bit shifts.</span></span> <span data-ttu-id="b8c2e-118">例如，如果8位格式的白色點是235，對應的10位格式會有一個位於 940 (235 × 4) 的點。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-118">For example, if the white point of an 8-bit format is 235, the corresponding 10-bit format has a white point at 940 (235 × 4).</span></span>

<span data-ttu-id="b8c2e-119">此處所述的16位標記法會針對每個通道使用位元組由小到小的 **文字** 值。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-119">The 16-bit representations described here use little-endian **WORD** values for each channel.</span></span> <span data-ttu-id="b8c2e-120">10位格式也會針對每個通道使用16個位，最低6位設定為零，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-120">The 10-bit formats also use 16 bits for each channel, with the lowest 6 bits set to zero, as shown in the following diagram.</span></span>

![顯示10位標記法的圖表](images/ee3aae23-4f0a-47d0-a46c-f3d7d94205e6.gif)

<span data-ttu-id="b8c2e-122">由於相同 YUV 格式的10位和16位標記法具有相同的記憶體配置，因此可以將10位表示轉換成16標記法，而不會遺失有效位數。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-122">Because the 10-bit and 16-bit representations of the same YUV format have the same memory layout, it is possible to cast a 10-bit representation to a 16-representation with no loss of precision.</span></span> <span data-ttu-id="b8c2e-123">您也可以將16位標記法轉換為10位標記法。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-123">It is also possible to cast a 16-bit representation down to a 10-bit representation.</span></span> <span data-ttu-id="b8c2e-124">不過， (Y416 和 Y410 格式是此一般規則的例外狀況，因為它們不會共用相同的記憶體配置。 ) </span><span class="sxs-lookup"><span data-stu-id="b8c2e-124">(The Y416 and Y410 formats are an exception to this general rule, however, because they do not share the same memory layout.)</span></span>

<span data-ttu-id="b8c2e-125">當圖形硬體讀取包含10位標記法的介面時，應該忽略每個通道的低序位6位。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-125">When the graphics hardware reads a surface that contains a 10-bit representation, it should ignore the low-order 6 bits of each channel.</span></span> <span data-ttu-id="b8c2e-126">但是，如果某個介面包含有效的16位資料，則應該將它識別為16位介面。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-126">If a surface contains valid 16-bit data, however, it should be identified as a 16-bit surface.</span></span>

<span data-ttu-id="b8c2e-127">在包含 Alpha 的格式中，完全透明圖元的 Alpha 值為零，而完全不透明的圖元具有 Alpha 值 (2 ^ n) –1，其中 n 是 Alpha 位的數目。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-127">In the formats that contain alpha, a completely transparent pixel has an alpha value of zero, and a completely opaque pixel has an alpha value of (2^n) – 1, where n is the number of alpha bits.</span></span> <span data-ttu-id="b8c2e-128">在元件轉換成正規化的線性形式之後，會假設 Alpha 是套用到每個元件的線性值。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-128">Alpha is assumed to be a linear value that is applied to each component after the component has been converted into its normalized linear form.</span></span>

<span data-ttu-id="b8c2e-129">針對視訊記憶體中的影像，圖形驅動程式會選取介面的記憶體對齊。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-129">For images in video memory, the graphics driver selects the memory alignment of the surface.</span></span> <span data-ttu-id="b8c2e-130">介面必須對齊 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-130">The surface must be **DWORD** aligned.</span></span> <span data-ttu-id="b8c2e-131">也就是說，介面內的個別線條保證會從32位界限開始，雖然對齊可以大於32位。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-131">That is, individual lines within a surface are guaranteed to start at a 32-bit boundary, although the alignment can be larger than 32 bits.</span></span> <span data-ttu-id="b8c2e-132">原點 (0，0) 一律是表面的左上角。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-132">The origin (0,0) is always the upper-left corner of the surface.</span></span>

<span data-ttu-id="b8c2e-133">基於本檔的目的， *U* 這一詞相當於 *Cb*，而詞彙 *V* 則相當於 *Cr*。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-133">For the purposes of this documentation, the term *U* is equivalent to *Cb*, and the term *V* is equivalent to *Cr*.</span></span>

## <a name="fourcc-codes-for-10-bit-and-16-bit-yuv"></a><span data-ttu-id="b8c2e-134">10位和16位 YUV 的 FOURCC 碼</span><span class="sxs-lookup"><span data-stu-id="b8c2e-134">FOURCC Codes For 10-Bit and 16-Bit YUV</span></span>

<span data-ttu-id="b8c2e-135">此處所述格式的 FOURCC 碼使用下列慣例：</span><span class="sxs-lookup"><span data-stu-id="b8c2e-135">The FOURCC codes for the formats described here use the following convention:</span></span>

-   <span data-ttu-id="b8c2e-136">如果格式為平面，則 FOURCC 程式碼中的第一個字元是 ' P '。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-136">If the format is planar, the first character in the FOURCC code is 'P'.</span></span> <span data-ttu-id="b8c2e-137">如果壓縮格式，則第一個字元是 ' Y '。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-137">If the format is packed, the first character is 'Y'.</span></span>
-   <span data-ttu-id="b8c2e-138">FOURCC 程式碼中的第二個字元是由色度取樣所決定，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-138">The second character in the FOURCC code is determined by the chroma sampling, as shown in the following table.</span></span>

    

    | <span data-ttu-id="b8c2e-139">色度取樣</span><span class="sxs-lookup"><span data-stu-id="b8c2e-139">Chroma sampling</span></span> | <span data-ttu-id="b8c2e-140">FOURCC 碼字母</span><span class="sxs-lookup"><span data-stu-id="b8c2e-140">FOURCC code letter</span></span> |
    |-----------------|--------------------|
    | <span data-ttu-id="b8c2e-141">4:4:4</span><span class="sxs-lookup"><span data-stu-id="b8c2e-141">4:4:4</span></span>           | <span data-ttu-id="b8c2e-142">億</span><span class="sxs-lookup"><span data-stu-id="b8c2e-142">'4'</span></span>                |
    | <span data-ttu-id="b8c2e-143">4:2:2</span><span class="sxs-lookup"><span data-stu-id="b8c2e-143">4:2:2</span></span>           | <span data-ttu-id="b8c2e-144">二級</span><span class="sxs-lookup"><span data-stu-id="b8c2e-144">'2'</span></span>                |
    | <span data-ttu-id="b8c2e-145">4:2:1</span><span class="sxs-lookup"><span data-stu-id="b8c2e-145">4:2:1</span></span>           | <span data-ttu-id="b8c2e-146">'1'</span><span class="sxs-lookup"><span data-stu-id="b8c2e-146">'1'</span></span>                |
    | <span data-ttu-id="b8c2e-147">4:2:0</span><span class="sxs-lookup"><span data-stu-id="b8c2e-147">4:2:0</span></span>           | <span data-ttu-id="b8c2e-148">'0'</span><span class="sxs-lookup"><span data-stu-id="b8c2e-148">'0'</span></span>                |

    

     

-   <span data-ttu-id="b8c2e-149">FOURCC 中的最後兩個字元代表每個通道的位數，' 16 ' 代表16位或 ' 10 ' （代表10個位）。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-149">The final two characters in the FOURCC indicate the number of bits per channel, either '16' for 16 bits or '10' for 10 bits.</span></span>

<span data-ttu-id="b8c2e-150">使用此配置時，已定義下列 FOURCC 碼。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-150">Using this scheme, the following FOURCC codes have been defined.</span></span> <span data-ttu-id="b8c2e-151">目前尚未定義10位或16位 YUV 的4:2:1 格式。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-151">No 4:2:1 formats for 10-bit or 16-bit YUV have been defined at this time.</span></span>



| <span data-ttu-id="b8c2e-152">FOURCC</span><span class="sxs-lookup"><span data-stu-id="b8c2e-152">FOURCC</span></span> | <span data-ttu-id="b8c2e-153">Description</span><span class="sxs-lookup"><span data-stu-id="b8c2e-153">Description</span></span>            |
|--------|------------------------|
| <span data-ttu-id="b8c2e-154">P016</span><span class="sxs-lookup"><span data-stu-id="b8c2e-154">P016</span></span>   | <span data-ttu-id="b8c2e-155">平面、4:2:0、16位。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-155">Planar, 4:2:0, 16-bit.</span></span> |
| <span data-ttu-id="b8c2e-156">P010</span><span class="sxs-lookup"><span data-stu-id="b8c2e-156">P010</span></span>   | <span data-ttu-id="b8c2e-157">平面、4:2:0、10位。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-157">Planar, 4:2:0, 10-bit.</span></span> |
| <span data-ttu-id="b8c2e-158">P216</span><span class="sxs-lookup"><span data-stu-id="b8c2e-158">P216</span></span>   | <span data-ttu-id="b8c2e-159">平面、4:2:2、16位。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-159">Planar, 4:2:2, 16-bit.</span></span> |
| <span data-ttu-id="b8c2e-160">P210</span><span class="sxs-lookup"><span data-stu-id="b8c2e-160">P210</span></span>   | <span data-ttu-id="b8c2e-161">平面、4:2:2、10位。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-161">Planar, 4:2:2, 10-bit.</span></span> |
| <span data-ttu-id="b8c2e-162">Y216</span><span class="sxs-lookup"><span data-stu-id="b8c2e-162">Y216</span></span>   | <span data-ttu-id="b8c2e-163">已封裝，4:2:2，16位。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-163">Packed, 4:2:2, 16-bit.</span></span> |
| <span data-ttu-id="b8c2e-164">Y210</span><span class="sxs-lookup"><span data-stu-id="b8c2e-164">Y210</span></span>   | <span data-ttu-id="b8c2e-165">封裝、4:2:2、10位。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-165">Packed, 4:2:2, 10-bit.</span></span> |
| <span data-ttu-id="b8c2e-166">Y416</span><span class="sxs-lookup"><span data-stu-id="b8c2e-166">Y416</span></span>   | <span data-ttu-id="b8c2e-167">已封裝，4:4:4，16位</span><span class="sxs-lookup"><span data-stu-id="b8c2e-167">Packed, 4:4:4, 16-bit</span></span>  |
| <span data-ttu-id="b8c2e-168">Y410</span><span class="sxs-lookup"><span data-stu-id="b8c2e-168">Y410</span></span>   | <span data-ttu-id="b8c2e-169">封裝、4:4:4、10位。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-169">Packed, 4:4:4, 10-bit.</span></span> |



 

<span data-ttu-id="b8c2e-170">子類型 Guid 也已經從這些 FOURCCs 中定義;請參閱 [影片子類型 guid](video-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-170">Subtype GUIDs have also been defined from these FOURCCs; see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="surface-definitions"></a><span data-ttu-id="b8c2e-171">介面定義</span><span class="sxs-lookup"><span data-stu-id="b8c2e-171">Surface Definitions</span></span>

<span data-ttu-id="b8c2e-172">本節說明每個格式的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-172">This section describes the memory layout of each format.</span></span> <span data-ttu-id="b8c2e-173">在接下來的描述中， **單字** 詞彙指的是位元組由大到小的16位值，而 **DWORD** 一詞指的是位元組由大到小的32位值。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-173">In the descriptions that follow, the term **WORD** refers to a little-endian 16-bit value, and the term **DWORD** refers to a little-endian 32-bit value.</span></span>

### <a name="420-formats"></a><span data-ttu-id="b8c2e-174">4:2:0 格式</span><span class="sxs-lookup"><span data-stu-id="b8c2e-174">4:2:0 Formats</span></span>

<span data-ttu-id="b8c2e-175">定義兩種4:2:0 格式，FOURCC 碼為 P016 和 P010。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-175">Two 4:2:0 formats are defined, with the FOURCC codes P016 and P010.</span></span> <span data-ttu-id="b8c2e-176">它們共用相同的記憶體配置，但 P016 使用每個通道16個位，而 P010 則會使用每個通道10個位。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-176">They share the same memory layout, but P016 uses 16 bits per channel and P010 uses 10 bits per channel.</span></span>

### <a name="p016-and-p010"></a><span data-ttu-id="b8c2e-177">P016 和 P010</span><span class="sxs-lookup"><span data-stu-id="b8c2e-177">P016 and P010</span></span>

<span data-ttu-id="b8c2e-178">在這兩種格式中，所有的 Y 範例都會先出現在記憶體中，做為 **單字** 的陣列，並具有偶數的行數。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-178">In these two formats, all Y samples appear first in memory as an array of **WORD** s with an even number of lines.</span></span> <span data-ttu-id="b8c2e-179">介面 stride 可以大於 Y 平面的寬度。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-179">The surface stride can be larger than the width of the Y plane.</span></span> <span data-ttu-id="b8c2e-180">這個陣列後面緊接著包含交錯您和 V 範例的 **單字** 陣列，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-180">This array is followed immediately by an array of **WORD** s that contains interleaved U and V samples, as shown in the following diagram.</span></span>

![顯示 p016 和 p010 圖元版面配置的圖表](images/1e1c4d66-6172-4d3a-bd25-4b5caa67edcd.gif)

<span data-ttu-id="b8c2e-182">如果結合的 U-V 陣列是以 **DWORD** s 的陣列定址，則最不重要的單字 (LSW) 包含 U 值，而最重要的單字 (MSW) 包含 V 值。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-182">If the combined U-V array is addressed as an array of **DWORD** s, the least significant word (LSW) contains the U value and the most significant word (MSW) contains the V value.</span></span> <span data-ttu-id="b8c2e-183">結合的 U V 平面的 stride 等於 Y 平面的 stride。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-183">The stride of the combined U-V plane is equal to the stride of the Y plane.</span></span> <span data-ttu-id="b8c2e-184">U V 平面有一半與 Y 平面一樣多的行數。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-184">The U-V plane has half as many lines as the Y plane.</span></span>

<span data-ttu-id="b8c2e-185">這兩種格式是慣用的4:2:0 平面像素格式，適用于較高的精確度 YUV 表示。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-185">These two formats are the preferred 4:2:0 planar pixel formats for higher precision YUV representations.</span></span> <span data-ttu-id="b8c2e-186">它們應該是支援10位或16位4:2:0 影片的 DirectX Video 加速 (DXVA) 加速器的中繼詞彙需求。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-186">They are expected to be an intermediate-term requirement for DirectX Video Acceleration (DXVA) accelerators that support 10-bit or 16-bit 4:2:0 video.</span></span>

### <a name="422-formats"></a><span data-ttu-id="b8c2e-187">4:2:2 格式</span><span class="sxs-lookup"><span data-stu-id="b8c2e-187">4:2:2 Formats</span></span>

<span data-ttu-id="b8c2e-188">定義了四種4:2:2 格式：兩個平面和兩個都是封裝的。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-188">Four 4:2:2 formats are defined, two planar and two packed.</span></span> <span data-ttu-id="b8c2e-189">它們具有下列 FOURCC 碼：</span><span class="sxs-lookup"><span data-stu-id="b8c2e-189">They have the following FOURCC codes:</span></span>

-   <span data-ttu-id="b8c2e-190">P216</span><span class="sxs-lookup"><span data-stu-id="b8c2e-190">P216</span></span>
-   <span data-ttu-id="b8c2e-191">P210</span><span class="sxs-lookup"><span data-stu-id="b8c2e-191">P210</span></span>
-   <span data-ttu-id="b8c2e-192">Y216</span><span class="sxs-lookup"><span data-stu-id="b8c2e-192">Y216</span></span>
-   <span data-ttu-id="b8c2e-193">Y210</span><span class="sxs-lookup"><span data-stu-id="b8c2e-193">Y210</span></span>

### <a name="p216-and-p210"></a><span data-ttu-id="b8c2e-194">P216 和 P210</span><span class="sxs-lookup"><span data-stu-id="b8c2e-194">P216 and P210</span></span>

<span data-ttu-id="b8c2e-195">在這兩種平面格式中，所有的 Y 範例都會先出現在記憶體中，做為 **單字** 的陣列，包含偶數的行數。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-195">In these two planar formats, all Y samples appear first in memory as an array of **WORD** s with an even number of lines.</span></span> <span data-ttu-id="b8c2e-196">介面 stride 可以大於 Y 平面的寬度。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-196">The surface stride can be larger than the width of the Y plane.</span></span> <span data-ttu-id="b8c2e-197">這個陣列後面緊接著包含交錯您和 V 範例的 **單字** 陣列，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-197">This array is followed immediately by an array of **WORD** s that contains interleaved U and V samples, as shown in the following diagram.</span></span>

![顯示 p216 和 p210 圖元版面配置的圖表](images/ff672fef-218f-4722-b806-d06c77fe8cfa.gif)

<span data-ttu-id="b8c2e-199">如果結合的 U-V 陣列是定址為 **DWORD** s 的陣列，LSW 就會包含 U 值，而且 MSW 會包含 V 值。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-199">If the combined U-V array is addressed as an array of **DWORD** s, the LSW contains the U value and the MSW contains the V value.</span></span> <span data-ttu-id="b8c2e-200">結合的 U V 平面的 stride 等於 Y 平面的 stride。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-200">The stride of the combined U-V plane is equal to the stride of the Y plane.</span></span> <span data-ttu-id="b8c2e-201">U V 平面與 Y 平面的行數相同。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-201">The U-V plane has the same number of lines as the Y plane.</span></span>

<span data-ttu-id="b8c2e-202">這兩種格式是慣用的4:2:2 平面像素格式，適用于較高的精確度 YUV 表示。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-202">These two formats are the preferred 4:2:2 planar pixel formats for higher precision YUV representations.</span></span> <span data-ttu-id="b8c2e-203">它們應該是支援10位或16位4:2:2 影片的 DirectX Video 加速 (DXVA) 加速器的中繼詞彙需求。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-203">They are expected to be an intermediate-term requirement for DirectX Video Acceleration (DXVA) accelerators that support 10-bit or 16-bit 4:2:2 video.</span></span>

### <a name="y216-and-y210"></a><span data-ttu-id="b8c2e-204">Y216 和 Y210</span><span class="sxs-lookup"><span data-stu-id="b8c2e-204">Y216 and Y210</span></span>

<span data-ttu-id="b8c2e-205">在這兩個壓縮格式中，每對圖元都會儲存為四個 **單字** 的陣列，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-205">In these two packed formats, each pair of pixels is stored as an array of four **WORD** s, as shown in the following illustration.</span></span>

![顯示 y216 和 y210 圖元配置的圖表。](images/6f68aeeb-18ca-48ee-82c4-5b79d5510e9f.gif)

<span data-ttu-id="b8c2e-207">陣列中的第一個 **單字** 包含配對中的第一個 Y 樣本、第二 **個單字** 包含 U 範例、第三個 **字** 組包含第二個 y 樣本，而 **第四個單字包含** V 範例。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-207">The first **WORD** in the array contains the first Y sample in the pair, the second **WORD** contains the U sample, the third **WORD** contains the second Y sample, and the fourth **WORD** contains the V sample.</span></span>

<span data-ttu-id="b8c2e-208">Y210 與 Y216 完全相同，不同之處在于每個範例只包含10個位的重要資料。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-208">Y210 is identical to Y216 except that each sample contains only 10 bits of significant data.</span></span> <span data-ttu-id="b8c2e-209">最不重要的6個位會設定為零，如先前所述。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-209">The least significant 6 bits are set to zero, as described previously.</span></span>

### <a name="444-formats"></a><span data-ttu-id="b8c2e-210">4:4:4 格式</span><span class="sxs-lookup"><span data-stu-id="b8c2e-210">4:4:4 Formats</span></span>

<span data-ttu-id="b8c2e-211">定義兩種4:4:4 格式，FOURCC 碼為 Y410 和 Y416。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-211">Two 4:4:4 formats are defined, with the FOURCC codes Y410 and Y416.</span></span> <span data-ttu-id="b8c2e-212">兩者都是封裝格式。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-212">Both are packed formats.</span></span>

### <a name="y410"></a><span data-ttu-id="b8c2e-213">Y410</span><span class="sxs-lookup"><span data-stu-id="b8c2e-213">Y410</span></span>

<span data-ttu-id="b8c2e-214">這種格式是包含2位 Alpha 的壓縮10位標記法。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-214">This format is a packed 10-bit representation that includes 2 bits of alpha.</span></span> <span data-ttu-id="b8c2e-215">每個圖元都會編碼為單一 **DWORD** ，其中的記憶體配置如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-215">Each pixel is encoded as a single **DWORD** with the memory layout shown in the following diagram.</span></span>

![顯示 y410 圖元配置的圖表。](images/f8a71437-e3f1-4331-be30-f766c028d648.gif)

<span data-ttu-id="b8c2e-217">Bits 0-9 包含 U 範例、bits 10-19 包含 Y 樣本、bits 20-29 包含 V 範例，而 bits 30-31 則包含 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-217">Bits 0-9 contain the U sample, bits 10-19 contain the Y sample, bits 20-29 contain the V sample, and bits 30-31 contain the alpha value.</span></span> <span data-ttu-id="b8c2e-218">若要指出圖元完全不透明，應用程式必須將兩個 Alpha 位設定為等於0x03。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-218">To indicate that a pixel is fully opaque, an application must set the two alpha bits equal to 0x03.</span></span>

### <a name="y416"></a><span data-ttu-id="b8c2e-219">Y416</span><span class="sxs-lookup"><span data-stu-id="b8c2e-219">Y416</span></span>

<span data-ttu-id="b8c2e-220">此格式是包含16位 Alpha 的封裝16位標記法。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-220">This format is a packed 16-bit representation that includes 16 bits of alpha.</span></span> <span data-ttu-id="b8c2e-221">每個圖元都會編碼為一對 **DWORD**，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-221">Each pixel is encoded as a pair of **DWORD** s, as shown in the following illustration.</span></span>

![顯示 y416 圖元配置的圖表。](images/c928523a-25d3-4712-9aec-5b492b51435f.gif)

<span data-ttu-id="b8c2e-223">Bits 0-15 包含 U 範例、bits 16-31 包含 Y 樣本、bits 32-47 包含 V 範例，而 bits 48-63 則包含 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-223">Bits 0-15 contain the U sample, bits 16-31 contain the Y sample, bits 32-47 contain the V sample, and bits 48-63 contain the alpha value.</span></span>

<span data-ttu-id="b8c2e-224">若要指出圖元是完全不透明的，應用程式必須將兩個 Alpha 位設定為0xFFFF。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-224">To indicate that a pixel is fully opaque, an application must set the two alpha bits equal to 0xFFFF.</span></span> <span data-ttu-id="b8c2e-225">此格式主要是在影像處理期間作為中繼格式，以避免發生錯誤的累積。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-225">This format is intended primarily as an intermediate format during image processing to avoid the accumulation of errors.</span></span>

## <a name="preferred-yuv-formats"></a><span data-ttu-id="b8c2e-226">慣用的 YUV 格式</span><span class="sxs-lookup"><span data-stu-id="b8c2e-226">Preferred YUV Formats</span></span>

<span data-ttu-id="b8c2e-227">下表列出慣用的 YUV 格式，包括8位格式。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-227">The following table lists the preferred YUV formats, including 8-bit formats.</span></span>



| <span data-ttu-id="b8c2e-228">格式</span><span class="sxs-lookup"><span data-stu-id="b8c2e-228">Format</span></span> | <span data-ttu-id="b8c2e-229">色度取樣</span><span class="sxs-lookup"><span data-stu-id="b8c2e-229">Chroma sampling</span></span> | <span data-ttu-id="b8c2e-230">已封裝或平面</span><span class="sxs-lookup"><span data-stu-id="b8c2e-230">Packed or planar</span></span> | <span data-ttu-id="b8c2e-231">每個通道的位數</span><span class="sxs-lookup"><span data-stu-id="b8c2e-231">Bits per channel</span></span> |
|--------|-----------------|------------------|------------------|
| <span data-ttu-id="b8c2e-232">AYUV</span><span class="sxs-lookup"><span data-stu-id="b8c2e-232">AYUV</span></span>   | <span data-ttu-id="b8c2e-233">4:4:4</span><span class="sxs-lookup"><span data-stu-id="b8c2e-233">4:4:4</span></span>           | <span data-ttu-id="b8c2e-234">包裝</span><span class="sxs-lookup"><span data-stu-id="b8c2e-234">Packed</span></span>           | <span data-ttu-id="b8c2e-235">8</span><span class="sxs-lookup"><span data-stu-id="b8c2e-235">8</span></span>                |
| <span data-ttu-id="b8c2e-236">Y410</span><span class="sxs-lookup"><span data-stu-id="b8c2e-236">Y410</span></span>   | <span data-ttu-id="b8c2e-237">4:4:4</span><span class="sxs-lookup"><span data-stu-id="b8c2e-237">4:4:4</span></span>           | <span data-ttu-id="b8c2e-238">包裝</span><span class="sxs-lookup"><span data-stu-id="b8c2e-238">Packed</span></span>           | <span data-ttu-id="b8c2e-239">10</span><span class="sxs-lookup"><span data-stu-id="b8c2e-239">10</span></span>               |
| <span data-ttu-id="b8c2e-240">Y416</span><span class="sxs-lookup"><span data-stu-id="b8c2e-240">Y416</span></span>   | <span data-ttu-id="b8c2e-241">4:4:4</span><span class="sxs-lookup"><span data-stu-id="b8c2e-241">4:4:4</span></span>           | <span data-ttu-id="b8c2e-242">包裝</span><span class="sxs-lookup"><span data-stu-id="b8c2e-242">Packed</span></span>           | <span data-ttu-id="b8c2e-243">16</span><span class="sxs-lookup"><span data-stu-id="b8c2e-243">16</span></span>               |
| <span data-ttu-id="b8c2e-244">AI44</span><span class="sxs-lookup"><span data-stu-id="b8c2e-244">AI44</span></span>   | <span data-ttu-id="b8c2e-245">4:4:4</span><span class="sxs-lookup"><span data-stu-id="b8c2e-245">4:4:4</span></span>           | <span data-ttu-id="b8c2e-246">包裝</span><span class="sxs-lookup"><span data-stu-id="b8c2e-246">Packed</span></span>           | <span data-ttu-id="b8c2e-247">調色盤</span><span class="sxs-lookup"><span data-stu-id="b8c2e-247">Palettized</span></span>       |
| <span data-ttu-id="b8c2e-248">YUY2</span><span class="sxs-lookup"><span data-stu-id="b8c2e-248">YUY2</span></span>   | <span data-ttu-id="b8c2e-249">4:2:2</span><span class="sxs-lookup"><span data-stu-id="b8c2e-249">4:2:2</span></span>           | <span data-ttu-id="b8c2e-250">包裝</span><span class="sxs-lookup"><span data-stu-id="b8c2e-250">Packed</span></span>           | <span data-ttu-id="b8c2e-251">8</span><span class="sxs-lookup"><span data-stu-id="b8c2e-251">8</span></span>                |
| <span data-ttu-id="b8c2e-252">Y210</span><span class="sxs-lookup"><span data-stu-id="b8c2e-252">Y210</span></span>   | <span data-ttu-id="b8c2e-253">4:2:2</span><span class="sxs-lookup"><span data-stu-id="b8c2e-253">4:2:2</span></span>           | <span data-ttu-id="b8c2e-254">包裝</span><span class="sxs-lookup"><span data-stu-id="b8c2e-254">Packed</span></span>           | <span data-ttu-id="b8c2e-255">10</span><span class="sxs-lookup"><span data-stu-id="b8c2e-255">10</span></span>               |
| <span data-ttu-id="b8c2e-256">Y216</span><span class="sxs-lookup"><span data-stu-id="b8c2e-256">Y216</span></span>   | <span data-ttu-id="b8c2e-257">4:2:2</span><span class="sxs-lookup"><span data-stu-id="b8c2e-257">4:2:2</span></span>           | <span data-ttu-id="b8c2e-258">包裝</span><span class="sxs-lookup"><span data-stu-id="b8c2e-258">Packed</span></span>           | <span data-ttu-id="b8c2e-259">16</span><span class="sxs-lookup"><span data-stu-id="b8c2e-259">16</span></span>               |
| <span data-ttu-id="b8c2e-260">P210</span><span class="sxs-lookup"><span data-stu-id="b8c2e-260">P210</span></span>   | <span data-ttu-id="b8c2e-261">4:2:2</span><span class="sxs-lookup"><span data-stu-id="b8c2e-261">4:2:2</span></span>           | <span data-ttu-id="b8c2e-262">平面</span><span class="sxs-lookup"><span data-stu-id="b8c2e-262">Planar</span></span>           | <span data-ttu-id="b8c2e-263">10</span><span class="sxs-lookup"><span data-stu-id="b8c2e-263">10</span></span>               |
| <span data-ttu-id="b8c2e-264">P216</span><span class="sxs-lookup"><span data-stu-id="b8c2e-264">P216</span></span>   | <span data-ttu-id="b8c2e-265">4:2:2</span><span class="sxs-lookup"><span data-stu-id="b8c2e-265">4:2:2</span></span>           | <span data-ttu-id="b8c2e-266">平面</span><span class="sxs-lookup"><span data-stu-id="b8c2e-266">Planar</span></span>           | <span data-ttu-id="b8c2e-267">16</span><span class="sxs-lookup"><span data-stu-id="b8c2e-267">16</span></span>               |
| <span data-ttu-id="b8c2e-268">NV12</span><span class="sxs-lookup"><span data-stu-id="b8c2e-268">NV12</span></span>   | <span data-ttu-id="b8c2e-269">4:2:0</span><span class="sxs-lookup"><span data-stu-id="b8c2e-269">4:2:0</span></span>           | <span data-ttu-id="b8c2e-270">平面</span><span class="sxs-lookup"><span data-stu-id="b8c2e-270">Planar</span></span>           | <span data-ttu-id="b8c2e-271">8</span><span class="sxs-lookup"><span data-stu-id="b8c2e-271">8</span></span>                |
| <span data-ttu-id="b8c2e-272">P010</span><span class="sxs-lookup"><span data-stu-id="b8c2e-272">P010</span></span>   | <span data-ttu-id="b8c2e-273">4:2:0</span><span class="sxs-lookup"><span data-stu-id="b8c2e-273">4:2:0</span></span>           | <span data-ttu-id="b8c2e-274">平面</span><span class="sxs-lookup"><span data-stu-id="b8c2e-274">Planar</span></span>           | <span data-ttu-id="b8c2e-275">10</span><span class="sxs-lookup"><span data-stu-id="b8c2e-275">10</span></span>               |
| <span data-ttu-id="b8c2e-276">P016</span><span class="sxs-lookup"><span data-stu-id="b8c2e-276">P016</span></span>   | <span data-ttu-id="b8c2e-277">4:2:0</span><span class="sxs-lookup"><span data-stu-id="b8c2e-277">4:2:0</span></span>           | <span data-ttu-id="b8c2e-278">平面</span><span class="sxs-lookup"><span data-stu-id="b8c2e-278">Planar</span></span>           | <span data-ttu-id="b8c2e-279">16</span><span class="sxs-lookup"><span data-stu-id="b8c2e-279">16</span></span>               |
| <span data-ttu-id="b8c2e-280">NV11</span><span class="sxs-lookup"><span data-stu-id="b8c2e-280">NV11</span></span>   | <span data-ttu-id="b8c2e-281">4:1:1</span><span class="sxs-lookup"><span data-stu-id="b8c2e-281">4:1:1</span></span>           | <span data-ttu-id="b8c2e-282">平面</span><span class="sxs-lookup"><span data-stu-id="b8c2e-282">Planar</span></span>           | <span data-ttu-id="b8c2e-283">8</span><span class="sxs-lookup"><span data-stu-id="b8c2e-283">8</span></span>                |



 

<span data-ttu-id="b8c2e-284">建議您如果物件支援指定的位深度和色度取樣配置，則應該支援下表所列的對應 YUV 格式。</span><span class="sxs-lookup"><span data-stu-id="b8c2e-284">It is recommended that if an object supports a given bit depth and chroma sampling scheme, it should support the corresponding YUV formats listed in this table.</span></span> <span data-ttu-id="b8c2e-285"> (物件可能會支援此處未列出的其他格式。 ) </span><span class="sxs-lookup"><span data-stu-id="b8c2e-285">(Objects might support additional formats not listed here.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8c2e-286">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8c2e-286">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8c2e-287">適用于影片轉譯的建議8位 YUV 格式</span><span class="sxs-lookup"><span data-stu-id="b8c2e-287">Recommended 8-Bit YUV Formats for Video Rendering</span></span>](recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[<span data-ttu-id="b8c2e-288">影片子類型 Guid</span><span class="sxs-lookup"><span data-stu-id="b8c2e-288">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> <dt>

[<span data-ttu-id="b8c2e-289">影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="b8c2e-289">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 



