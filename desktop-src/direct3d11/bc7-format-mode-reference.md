---
title: BC7 格式模式參考
description: 本檔包含 BC7 材質壓縮格式區塊的8區塊模式和位配置清單。
ms.assetid: B1CEB729-6694-49BF-ACB9-FD1EFAB0B0D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719a223e6ac057b949d5e1222582058f637ec526
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/22/2020
ms.locfileid: "104374158"
---
# <a name="bc7-format-mode-reference"></a><span data-ttu-id="4dfd4-103">BC7 格式模式參考</span><span class="sxs-lookup"><span data-stu-id="4dfd4-103">BC7 Format Mode Reference</span></span>

<span data-ttu-id="4dfd4-104">本檔包含 BC7 材質壓縮格式區塊的8區塊模式和位配置清單。</span><span class="sxs-lookup"><span data-stu-id="4dfd4-104">This documentation contains a list of the 8 block modes and bit allocations for BC7 texture compression format blocks.</span></span>

<span data-ttu-id="4dfd4-105">區塊中每個子集的色彩會以兩個明確端點色彩以及其之間插入的色彩組呈現。</span><span class="sxs-lookup"><span data-stu-id="4dfd4-105">The colors for each subset within a block are represented by two explicit endpoint colors and a set of interpolated colors between them.</span></span> <span data-ttu-id="4dfd4-106">依區塊索引精確度而定，每個子集能具備 4 個、8 或 16 個可用的色彩。</span><span class="sxs-lookup"><span data-stu-id="4dfd4-106">Depending on the block's index precision, each subset can have 4, 8 or 16 possible colors.</span></span>

-   [<span data-ttu-id="4dfd4-107">模式0</span><span class="sxs-lookup"><span data-stu-id="4dfd4-107">Mode 0</span></span>](#mode-0)
-   [<span data-ttu-id="4dfd4-108">模式1</span><span class="sxs-lookup"><span data-stu-id="4dfd4-108">Mode 1</span></span>](#mode-1)
-   [<span data-ttu-id="4dfd4-109">模式2</span><span class="sxs-lookup"><span data-stu-id="4dfd4-109">Mode 2</span></span>](#mode-2)
-   [<span data-ttu-id="4dfd4-110">模式3</span><span class="sxs-lookup"><span data-stu-id="4dfd4-110">Mode 3</span></span>](#mode-3)
-   [<span data-ttu-id="4dfd4-111">模式4</span><span class="sxs-lookup"><span data-stu-id="4dfd4-111">Mode 4</span></span>](#mode-4)
-   [<span data-ttu-id="4dfd4-112">模式5</span><span class="sxs-lookup"><span data-stu-id="4dfd4-112">Mode 5</span></span>](#mode-5)
-   [<span data-ttu-id="4dfd4-113">模式6</span><span class="sxs-lookup"><span data-stu-id="4dfd4-113">Mode 6</span></span>](#mode-6)
-   [<span data-ttu-id="4dfd4-114">模式7</span><span class="sxs-lookup"><span data-stu-id="4dfd4-114">Mode 7</span></span>](#mode-7)
-   [<span data-ttu-id="4dfd4-115">備註</span><span class="sxs-lookup"><span data-stu-id="4dfd4-115">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="4dfd4-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="4dfd4-116">Related topics</span></span>](#related-topics)

## <a name="mode-0"></a><span data-ttu-id="4dfd4-117">模式 0</span><span class="sxs-lookup"><span data-stu-id="4dfd4-117">Mode 0</span></span>

<span data-ttu-id="4dfd4-118">BC7 模式 0 的特性如下︰</span><span class="sxs-lookup"><span data-stu-id="4dfd4-118">BC7 Mode 0 has the following characteristics:</span></span>

-   <span data-ttu-id="4dfd4-119">僅限色彩元件 (無 Alpha)</span><span class="sxs-lookup"><span data-stu-id="4dfd4-119">Color components only (no alpha)</span></span>
-   <span data-ttu-id="4dfd4-120">每個區塊 3 個子集</span><span class="sxs-lookup"><span data-stu-id="4dfd4-120">3 subsets per block</span></span>
-   <span data-ttu-id="4dfd4-121">每個端點都有一個唯一 P 位元的 RGBP 4.4.4.1 端點</span><span class="sxs-lookup"><span data-stu-id="4dfd4-121">RGBP 4.4.4.1 endpoints with a unique P-bit per endpoint</span></span>
-   <span data-ttu-id="4dfd4-122">3 位元索引</span><span class="sxs-lookup"><span data-stu-id="4dfd4-122">3-bit indices</span></span>
-   <span data-ttu-id="4dfd4-123">16 個分割</span><span class="sxs-lookup"><span data-stu-id="4dfd4-123">16 partitions</span></span>

![模式 0 位元配置](images/bc7-mode0.png)

## <a name="mode-1"></a><span data-ttu-id="4dfd4-125">模式 1</span><span class="sxs-lookup"><span data-stu-id="4dfd4-125">Mode 1</span></span>

<span data-ttu-id="4dfd4-126">BC7 模式 1 的特性如下︰</span><span class="sxs-lookup"><span data-stu-id="4dfd4-126">BC7 Mode 1 has the following characteristics:</span></span>

-   <span data-ttu-id="4dfd4-127">僅限色彩元件 (無 Alpha)</span><span class="sxs-lookup"><span data-stu-id="4dfd4-127">Color components only (no alpha)</span></span>
-   <span data-ttu-id="4dfd4-128">每個區塊 2 個子集</span><span class="sxs-lookup"><span data-stu-id="4dfd4-128">2 subsets per block</span></span>
-   <span data-ttu-id="4dfd4-129">每個子集具有共用 P 位元的 RGBP 6.6.6.1 端點)</span><span class="sxs-lookup"><span data-stu-id="4dfd4-129">RGBP 6.6.6.1 endpoints with a shared P-bit per subset)</span></span>
-   <span data-ttu-id="4dfd4-130">3 位元索引</span><span class="sxs-lookup"><span data-stu-id="4dfd4-130">3-bit indices</span></span>
-   <span data-ttu-id="4dfd4-131">64 個分割</span><span class="sxs-lookup"><span data-stu-id="4dfd4-131">64 partitions</span></span>

![模式 1 位元配置](images/bc7-mode1.png)

## <a name="mode-2"></a><span data-ttu-id="4dfd4-133">模式 2</span><span class="sxs-lookup"><span data-stu-id="4dfd4-133">Mode 2</span></span>

<span data-ttu-id="4dfd4-134">BC7 模式 2 的特性如下︰</span><span class="sxs-lookup"><span data-stu-id="4dfd4-134">BC7 Mode 2 has the following characteristics:</span></span>

-   <span data-ttu-id="4dfd4-135">僅限色彩元件 (無 Alpha)</span><span class="sxs-lookup"><span data-stu-id="4dfd4-135">Color components only (no alpha)</span></span>
-   <span data-ttu-id="4dfd4-136">每個區塊 3 個子集</span><span class="sxs-lookup"><span data-stu-id="4dfd4-136">3 subsets per block</span></span>
-   <span data-ttu-id="4dfd4-137">RGB 5.5.5 端點</span><span class="sxs-lookup"><span data-stu-id="4dfd4-137">RGB 5.5.5 endpoints</span></span>
-   <span data-ttu-id="4dfd4-138">2 位元索引</span><span class="sxs-lookup"><span data-stu-id="4dfd4-138">2-bit indices</span></span>
-   <span data-ttu-id="4dfd4-139">64 個分割</span><span class="sxs-lookup"><span data-stu-id="4dfd4-139">64 partitions</span></span>

![模式 2 位元配置](images/bc7-mode2.png)

## <a name="mode-3"></a><span data-ttu-id="4dfd4-141">模式 3</span><span class="sxs-lookup"><span data-stu-id="4dfd4-141">Mode 3</span></span>

<span data-ttu-id="4dfd4-142">BC7 模式 3 的特性如下︰</span><span class="sxs-lookup"><span data-stu-id="4dfd4-142">BC7 Mode 3 has the following characteristics:</span></span>

-   <span data-ttu-id="4dfd4-143">僅限色彩元件 (無 Alpha)</span><span class="sxs-lookup"><span data-stu-id="4dfd4-143">Color components only (no alpha)</span></span>
-   <span data-ttu-id="4dfd4-144">每個區塊 2 個子集</span><span class="sxs-lookup"><span data-stu-id="4dfd4-144">2 subsets per block</span></span>
-   <span data-ttu-id="4dfd4-145">每個子集具有唯一 P 位元的 RGBP 7.7.7.1 端點)</span><span class="sxs-lookup"><span data-stu-id="4dfd4-145">RGBP 7.7.7.1 endpoints with a unique P-bit per subset)</span></span>
-   <span data-ttu-id="4dfd4-146">2 位元索引</span><span class="sxs-lookup"><span data-stu-id="4dfd4-146">2-bit indices</span></span>
-   <span data-ttu-id="4dfd4-147">64 個分割</span><span class="sxs-lookup"><span data-stu-id="4dfd4-147">64 partitions</span></span>

![模式 3 位元配置](images/bc7-mode3.png)

## <a name="mode-4"></a><span data-ttu-id="4dfd4-149">模式 4</span><span class="sxs-lookup"><span data-stu-id="4dfd4-149">Mode 4</span></span>

<span data-ttu-id="4dfd4-150">BC7 模式 4 的特性如下︰</span><span class="sxs-lookup"><span data-stu-id="4dfd4-150">BC7 Mode 4 has the following characteristics:</span></span>

-   <span data-ttu-id="4dfd4-151">具有獨立 Alpha 元件的色彩元件</span><span class="sxs-lookup"><span data-stu-id="4dfd4-151">Color components with separate alpha component</span></span>
-   <span data-ttu-id="4dfd4-152">每個區塊 1 個子集</span><span class="sxs-lookup"><span data-stu-id="4dfd4-152">1 subset per block</span></span>
-   <span data-ttu-id="4dfd4-153">RGB 5.5.5 色彩端點</span><span class="sxs-lookup"><span data-stu-id="4dfd4-153">RGB 5.5.5 color endpoints</span></span>
-   <span data-ttu-id="4dfd4-154">6 位元 Alpha 端點</span><span class="sxs-lookup"><span data-stu-id="4dfd4-154">6-bit alpha endpoints</span></span>
-   <span data-ttu-id="4dfd4-155">16 x 2 位元索引</span><span class="sxs-lookup"><span data-stu-id="4dfd4-155">16 x 2-bit indices</span></span>
-   <span data-ttu-id="4dfd4-156">16 x 3 位元索引</span><span class="sxs-lookup"><span data-stu-id="4dfd4-156">16 x 3-bit indices</span></span>
-   <span data-ttu-id="4dfd4-157">2 位元元件旋轉</span><span class="sxs-lookup"><span data-stu-id="4dfd4-157">2-bit component rotation</span></span>
-   <span data-ttu-id="4dfd4-158">1 位元索引選取器 (不論是否使用 2 或 3 位元索引)</span><span class="sxs-lookup"><span data-stu-id="4dfd4-158">1-bit index selector (whether the 2- or 3-bit indices are used)</span></span>

![模式 4 位元配置](images/bc7-mode4.png)

## <a name="mode-5"></a><span data-ttu-id="4dfd4-160">模式 5</span><span class="sxs-lookup"><span data-stu-id="4dfd4-160">Mode 5</span></span>

<span data-ttu-id="4dfd4-161">BC7 模式 5 的特性如下︰</span><span class="sxs-lookup"><span data-stu-id="4dfd4-161">BC7 Mode 5 has the following characteristics:</span></span>

-   <span data-ttu-id="4dfd4-162">具有獨立 Alpha 元件的色彩元件</span><span class="sxs-lookup"><span data-stu-id="4dfd4-162">Color components with separate alpha component</span></span>
-   <span data-ttu-id="4dfd4-163">每個區塊 1 個子集</span><span class="sxs-lookup"><span data-stu-id="4dfd4-163">1 subset per block</span></span>
-   <span data-ttu-id="4dfd4-164">RGB 7.7.7 色彩端點</span><span class="sxs-lookup"><span data-stu-id="4dfd4-164">RGB 7.7.7 color endpoints</span></span>
-   <span data-ttu-id="4dfd4-165">8位 Alpha 端點</span><span class="sxs-lookup"><span data-stu-id="4dfd4-165">8-bit alpha endpoints</span></span>
-   <span data-ttu-id="4dfd4-166">16 x 2 位元色彩索引</span><span class="sxs-lookup"><span data-stu-id="4dfd4-166">16 x 2-bit color indices</span></span>
-   <span data-ttu-id="4dfd4-167">16 x 2 位元 Alpha 索引</span><span class="sxs-lookup"><span data-stu-id="4dfd4-167">16 x 2-bit alpha indices</span></span>
-   <span data-ttu-id="4dfd4-168">2 位元元件旋轉</span><span class="sxs-lookup"><span data-stu-id="4dfd4-168">2-bit component rotation</span></span>

![模式 5 位元配置](images/bc7-mode5.png)

## <a name="mode-6"></a><span data-ttu-id="4dfd4-170">模式 6</span><span class="sxs-lookup"><span data-stu-id="4dfd4-170">Mode 6</span></span>

<span data-ttu-id="4dfd4-171">BC7 模式 6 的特性如下︰</span><span class="sxs-lookup"><span data-stu-id="4dfd4-171">BC7 Mode 6 has the following characteristics:</span></span>

-   <span data-ttu-id="4dfd4-172">合併的色彩和 Alpha 元件</span><span class="sxs-lookup"><span data-stu-id="4dfd4-172">Combined color and alpha components</span></span>
-   <span data-ttu-id="4dfd4-173">每個區塊一個子集</span><span class="sxs-lookup"><span data-stu-id="4dfd4-173">One subset per block</span></span>
-   <span data-ttu-id="4dfd4-174">RGBAP 7.7.7.7.1 色彩 (和 Alpha) 端點 (每個端點都有唯一 P 位元)</span><span class="sxs-lookup"><span data-stu-id="4dfd4-174">RGBAP 7.7.7.7.1 color (and alpha) endpoints (unique P-bit per endpoint)</span></span>
-   <span data-ttu-id="4dfd4-175">16 x 4 位元索引</span><span class="sxs-lookup"><span data-stu-id="4dfd4-175">16 x 4-bit indices</span></span>

![模式 6 位元配置](images/bc7-mode6.png)

## <a name="mode-7"></a><span data-ttu-id="4dfd4-177">模式 7</span><span class="sxs-lookup"><span data-stu-id="4dfd4-177">Mode 7</span></span>

<span data-ttu-id="4dfd4-178">BC7 模式 7 的特性如下︰</span><span class="sxs-lookup"><span data-stu-id="4dfd4-178">BC7 Mode 7 has the following characteristics:</span></span>

-   <span data-ttu-id="4dfd4-179">合併的色彩和 Alpha 元件</span><span class="sxs-lookup"><span data-stu-id="4dfd4-179">Combined color and alpha components</span></span>
-   <span data-ttu-id="4dfd4-180">每個區塊 2 個子集</span><span class="sxs-lookup"><span data-stu-id="4dfd4-180">2 subsets per block</span></span>
-   <span data-ttu-id="4dfd4-181">RGBAP 5.5.5.5.1 色彩 (和 Alpha) 端點 (每個端點都有唯一 P 位元)</span><span class="sxs-lookup"><span data-stu-id="4dfd4-181">RGBAP 5.5.5.5.1 color (and alpha) endpoints (unique P-bit per endpoint)</span></span>
-   <span data-ttu-id="4dfd4-182">2 位元索引</span><span class="sxs-lookup"><span data-stu-id="4dfd4-182">2-bit indices</span></span>
-   <span data-ttu-id="4dfd4-183">64 個分割</span><span class="sxs-lookup"><span data-stu-id="4dfd4-183">64 partitions</span></span>

![模式 7 位元配置](images/bc7-mode7.png)

## <a name="remarks"></a><span data-ttu-id="4dfd4-185">備註</span><span class="sxs-lookup"><span data-stu-id="4dfd4-185">Remarks</span></span>

<span data-ttu-id="4dfd4-186">模式 8 (最小顯著性位元組設定為 0x00) 已保留。</span><span class="sxs-lookup"><span data-stu-id="4dfd4-186">Mode 8 (the least significant byte is set to 0x00) is reserved.</span></span> <span data-ttu-id="4dfd4-187">請勿在您的編碼器中使用它。</span><span class="sxs-lookup"><span data-stu-id="4dfd4-187">Don't use it in your encoder.</span></span> <span data-ttu-id="4dfd4-188">如果您將此模式傳遞至硬體，就會傳回初始化至所有零的區塊。</span><span class="sxs-lookup"><span data-stu-id="4dfd4-188">If you pass this mode to the hardware, a block initialized to all zeroes is returned.</span></span>

<span data-ttu-id="4dfd4-189">在 BC7 中，您能以下列其中一種方式編碼 Alpha 元件：</span><span class="sxs-lookup"><span data-stu-id="4dfd4-189">In BC7, you can encode the alpha component in one of the following ways:</span></span>

-   <span data-ttu-id="4dfd4-190">不具備明確 Alpha 元件編碼的區塊類型。</span><span class="sxs-lookup"><span data-stu-id="4dfd4-190">Block types without explicit alpha component encoding.</span></span> <span data-ttu-id="4dfd4-191">在這些區塊中，色彩端點有一個僅限 RGB 的編碼，還有對所有材質解碼至 1.0 的 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="4dfd4-191">In these blocks, the color endpoints have an RGB-only encoding, with the alpha component decoded to 1.0 for all texels.</span></span>
-   <span data-ttu-id="4dfd4-192">具有合併色彩與 Alpha 元件的區塊類型。</span><span class="sxs-lookup"><span data-stu-id="4dfd4-192">Block types with combined color and alpha components.</span></span> <span data-ttu-id="4dfd4-193">在這些區塊中，端點色彩值會以 RGBA 格式指定，而且會插入 Alpha 元件值和色彩值。</span><span class="sxs-lookup"><span data-stu-id="4dfd4-193">In these blocks, the endpoint color values are specified in the RGBA format, and the alpha component values are interpolated along with the color values.</span></span>
-   <span data-ttu-id="4dfd4-194">具有獨立色彩與 Alpha 元件的區塊類型。</span><span class="sxs-lookup"><span data-stu-id="4dfd4-194">Block types with separated color and alpha components.</span></span> <span data-ttu-id="4dfd4-195">在這些區塊中，色彩和 Alpha 值是個別指定的，兩方都有獨立的索引集。</span><span class="sxs-lookup"><span data-stu-id="4dfd4-195">In these blocks the color and alpha values are specified separately, each with their own set of indices.</span></span> <span data-ttu-id="4dfd4-196">如此一來，它們就會分別編碼有效的向量和純量通道，其中向量通常會指定色板 \[ R、G、B，而純量會 \] 指定 Alpha 色板 \[ a \] 。</span><span class="sxs-lookup"><span data-stu-id="4dfd4-196">As a result, they have an effective vector and a scalar channel separately encoded, where the vector commonly specifies the color channels \[R, G, B\] and the scalar specifies the alpha channel \[A\].</span></span> <span data-ttu-id="4dfd4-197">為了支援這種方式，編碼中提供了一個獨立的 2 位元欄位，允許將不同的通道編碼指定為純量值。</span><span class="sxs-lookup"><span data-stu-id="4dfd4-197">To support this approach, a separate 2-bit field is provided in the encoding, which permits the specification of the separate channel encoding as a scalar value.</span></span> <span data-ttu-id="4dfd4-198">如此一來，區塊就可以具有此 Alpha 編碼 (同 2 元欄位所指示) 下列四個不同表示法中的其中一項︰</span><span class="sxs-lookup"><span data-stu-id="4dfd4-198">As a result, the block can have one of the following four different representations of this alpha encoding (as indicated by the 2-bit field):</span></span>
    -   <span data-ttu-id="4dfd4-199">RGB \| A： Alpha 通道分隔</span><span class="sxs-lookup"><span data-stu-id="4dfd4-199">RGB\|A: alpha channel separate</span></span>
    -   <span data-ttu-id="4dfd4-200">AGB \| R：個別的紅色色板</span><span class="sxs-lookup"><span data-stu-id="4dfd4-200">AGB\|R: "red" color channel separate</span></span>
    -   <span data-ttu-id="4dfd4-201">RAB \| G：「綠色」色頻分開</span><span class="sxs-lookup"><span data-stu-id="4dfd4-201">RAB\|G: "green" color channel separate</span></span>
    -   <span data-ttu-id="4dfd4-202">RGA \| B： "blue" 色頻道分隔</span><span class="sxs-lookup"><span data-stu-id="4dfd4-202">RGA\|B: "blue" color channel separate</span></span>

    <span data-ttu-id="4dfd4-203">解碼器在解碼之後會將通道順序重新排列回 RGBA，因此開發人員看不到內部區塊格式。</span><span class="sxs-lookup"><span data-stu-id="4dfd4-203">The decoder reorders the channel order back to RGBA after decoding, so the internal block format is invisible to the developer.</span></span> <span data-ttu-id="4dfd4-204">具有獨立色彩和 Alpha 元件的黑色也有兩組索引資料︰一個用於通道的向量集，一個用於純量通道。</span><span class="sxs-lookup"><span data-stu-id="4dfd4-204">Blacks with separate color and alpha components also have two sets of index data: one for the vectored set of channels, and one for the scalar channel.</span></span> <span data-ttu-id="4dfd4-205">在模式4的情況下 (，這些索引的寬度為 \[ 2 或3位 \] 。</span><span class="sxs-lookup"><span data-stu-id="4dfd4-205">(In the case of Mode 4, these indices are of differing widths \[2 or 3 bits\].</span></span> <span data-ttu-id="4dfd4-206">模式 4 也包含 1 位元選取器，可指定向量或純量通道是否使用 3 位元索引。)</span><span class="sxs-lookup"><span data-stu-id="4dfd4-206">Mode 4 also contains a 1-bit selector that specifies whether the vector or the scalar channel uses the 3-bit indices.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dfd4-207">相關主題</span><span class="sxs-lookup"><span data-stu-id="4dfd4-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dfd4-208">BC7 格式</span><span class="sxs-lookup"><span data-stu-id="4dfd4-208">BC7 Format</span></span>](bc7-format.md)
</dt> </dl>

 

 




