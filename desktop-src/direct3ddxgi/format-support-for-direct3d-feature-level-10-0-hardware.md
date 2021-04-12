---
description: 本節指定 Direct3D 功能等級10.0 硬體支援的格式 ([ **DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)值) 。
ms.assetid: 3C1CCA7D-9F2F-4B1B-8424-BA9C6DED4974
title: Direct3D 功能層級 10.0 硬體的格式支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f298460330feb2143b20da37ae82c3a6d63790
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187425"
---
# <a name="format-support-for-direct3d-feature-level-100-hardware"></a><span data-ttu-id="ba9fe-103">Direct3D 功能層級 10.0 硬體的格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-103">Format support for Direct3D Feature Level 10.0 hardware</span></span>

<span data-ttu-id="ba9fe-104">此區段會指定 Direct3D 功能等級10.0 硬體支援的格式 ([ _\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)值) 。</span><span class="sxs-lookup"><span data-stu-id="ba9fe-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 10.0 hardware.</span></span>

<span data-ttu-id="ba9fe-105">下表摘要說明使用下列索引鍵的功能支援。</span><span class="sxs-lookup"><span data-stu-id="ba9fe-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="ba9fe-106">符號</span><span class="sxs-lookup"><span data-stu-id="ba9fe-106">Symbol</span></span>                            | <span data-ttu-id="ba9fe-107">描述</span><span class="sxs-lookup"><span data-stu-id="ba9fe-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="ba9fe-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="ba9fe-108">_ *-*\*</span></span>                             | <span data-ttu-id="ba9fe-109">不允許或無法使用。</span><span class="sxs-lookup"><span data-stu-id="ba9fe-109">Disallowed or not available.</span></span>                                                  |
| ![必要](images/letter-r.jpg)  | <span data-ttu-id="ba9fe-111">需要硬體支援。</span><span class="sxs-lookup"><span data-stu-id="ba9fe-111">Hardware support is required.</span></span>                                                 |
| ![選用](images/letter-o.jpg)  | <span data-ttu-id="ba9fe-113">硬體支援是選擇性的，格式可能或可能不會有硬體加速。</span><span class="sxs-lookup"><span data-stu-id="ba9fe-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![依賴](images/letter-d.jpg) | <span data-ttu-id="ba9fe-115">如果支援相關的選擇性功能，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="ba9fe-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="ba9fe-116">本主題包含每一種格式的區段。</span><span class="sxs-lookup"><span data-stu-id="ba9fe-116">This topic contains a section per format.</span></span> <span data-ttu-id="ba9fe-117">格式 *目標* (資料表每個目標各包含一個資料列) 可以是資源類型、HLSL 內建函式，或是相依于特定格式的特定功能。</span><span class="sxs-lookup"><span data-stu-id="ba9fe-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="ba9fe-118">若要以程式設計方式驗證 D3D11 和 D3D12 中的格式支援，請參閱 [檢查硬體功能支援](checking-hardware-feature-support.md)。</span><span class="sxs-lookup"><span data-stu-id="ba9fe-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="ba9fe-119">這些格式的數目大多是（但不是全部），以遞增的數值順序來 &mdash; 看，有些會超出數值順序，並與其他相關的格式一起列出。</span><span class="sxs-lookup"><span data-stu-id="ba9fe-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="ba9fe-120">另請注意 *，格式名稱的無* 型別可以表示 *部分* 具型別，而不是嚴格的無型別 (請參閱主題結尾的 [格式附注](#format-notes) 章節) 。</span><span class="sxs-lookup"><span data-stu-id="ba9fe-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>
 
## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="ba9fe-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="ba9fe-122">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-122">Target</span></span> | <span data-ttu-id="ba9fe-123">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-123">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-124">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-125">0</span><span class="sxs-lookup"><span data-stu-id="ba9fe-125">0</span></span> |
| <span data-ttu-id="ba9fe-126">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-126">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-128">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-128">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-130">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-131">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-132">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-133">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-134">Texture2D</span></span> | \- |
| <span data-ttu-id="ba9fe-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-135">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-136">TextureCube</span></span> | \- |
| <span data-ttu-id="ba9fe-137">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-137">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-138">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-139">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-139">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-140">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-140">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-141">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-142">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-142">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-143">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-143">Mipmap</span></span> | \- |
| <span data-ttu-id="ba9fe-144">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-146">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-147">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-148">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-149">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-150">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-151">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-151">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-152">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-153">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-154">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-155">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-156">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-157">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-158">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-159">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-160">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-160">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-162">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-163">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-164">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-165">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-166">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-166">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-167">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-168">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-168">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-169">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-170">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-171">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-172">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-172">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-173">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="ba9fe-174">DXGI_FORMAT_R32G32B32A32 無的 \_ <sup>電腦</sup> (1) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-174">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="ba9fe-175">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-175">Target</span></span> | <span data-ttu-id="ba9fe-176">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-176">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-177">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-178">128</span><span class="sxs-lookup"><span data-stu-id="ba9fe-178">128</span></span> |
| <span data-ttu-id="ba9fe-179">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-179">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-181">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-181">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-182">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-182">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-183">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-183">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-184">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-184">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-185">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-185">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-187">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-189">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-189">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-191">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-191">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-193">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-193">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-194">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-194">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-195">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-195">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-196">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-196">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-197">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-197">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-198">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-198">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-199">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-199">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-201">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-201">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-202">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-202">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-203">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-203">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-204">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-204">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-205">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-206">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-207">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-208">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-208">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-209">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-209">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-210">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-210">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-211">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-211">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-212">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-212">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-213">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-213">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-214">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-214">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-215">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-215">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-216">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-216">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-217">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-217">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-219">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-219">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-220">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-220">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-221">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-221">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-222">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-222">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-223">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-223">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-224">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-224">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-225">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-225">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-227">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-227">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-228">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-228">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-229">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-229">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-230">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-230">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-232">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-232">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="ba9fe-233">DXGI_FORMAT_R32G32B32A32 \_ FLOAT<sup>FCS</sup> (2) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-233">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="ba9fe-234">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-234">Target</span></span> | <span data-ttu-id="ba9fe-235">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-235">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-236">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-236">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-237">128</span><span class="sxs-lookup"><span data-stu-id="ba9fe-237">128</span></span> |
| <span data-ttu-id="ba9fe-238">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-238">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-240">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-240">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-242">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-242">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-244">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-244">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-245">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-245">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-247">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-249">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-249">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-251">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-253">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-253">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-255">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-255">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-257">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-257">Shader sample (any filter)</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-259">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-260">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-261">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-261">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-262">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-263">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-263">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-265">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-265">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-267">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-267">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-269">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-269">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-271">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-272">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-273">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-274">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-275">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-275">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-276">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-276">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-277">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-277">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-278">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-278">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-279">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-279">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-280">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-280">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-281">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-281">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-282">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-282">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-283">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-283">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-284">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-284">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-286">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-286">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-288">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-288">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-290">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-290">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-292">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-292">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-294">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-294">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-296">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-296">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-297">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-297">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-299">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-299">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-300">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-300">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-301">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-301">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-302">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-302">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-304">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-304">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="ba9fe-305">DXGI_FORMAT_R32G32B32A32 \_ UINT<sup>FCS</sup> (3) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-305">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="ba9fe-306">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-306">Target</span></span> | <span data-ttu-id="ba9fe-307">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-307">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-308">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-308">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-309">128</span><span class="sxs-lookup"><span data-stu-id="ba9fe-309">128</span></span> |
| <span data-ttu-id="ba9fe-310">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-310">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-312">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-312">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-314">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-314">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-316">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-316">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-317">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-317">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-319">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-319">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-321">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-321">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-323">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-323">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-325">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-325">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-327">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-327">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-329">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-329">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-330">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-330">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-331">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-331">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-332">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-332">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-333">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-333">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-334">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-334">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-336">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-336">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-337">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-337">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-339">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-339">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-340">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-340">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-342">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-342">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-343">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-343">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-344">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-344">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-345">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-345">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-346">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-346">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-347">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-347">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-348">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-348">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-349">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-349">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-350">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-350">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-351">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-351">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-352">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-352">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-353">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-353">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-354">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-354">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-356">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-356">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-358">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-358">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-360">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-360">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-362">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-362">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-363">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-363">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-365">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-365">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-366">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-366">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-368">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-369">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-370">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-371">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-371">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-373">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-373">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="ba9fe-374">DXGI_FORMAT_R32G32B32A32 \_ 聖的<sup>FCS</sup> (4) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-374">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="ba9fe-375">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-375">Target</span></span> | <span data-ttu-id="ba9fe-376">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-376">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-377">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-377">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-378">128</span><span class="sxs-lookup"><span data-stu-id="ba9fe-378">128</span></span> |
| <span data-ttu-id="ba9fe-379">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-379">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-381">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-381">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-383">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-383">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-385">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-385">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-386">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-386">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-388">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-388">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-390">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-390">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-392">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-392">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-394">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-396">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-396">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-398">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-399">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-400">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-401">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-401">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-402">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-403">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-403">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-405">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-406">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-408">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-409">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-410">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-411">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-412">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-413">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-414">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-415">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-416">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-417">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-418">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-419">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-420">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-421">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-422">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-422">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-424">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-424">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-426">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-426">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-428">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-428">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-430">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-430">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-431">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-431">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-433">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-434">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-434">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-436">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-437">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-438">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-439">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-439">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-441">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="ba9fe-442">DXGI_FORMAT_R32G32B32 無的 \_ <sup>電腦</sup> (5) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-442">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="ba9fe-443">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-443">Target</span></span> | <span data-ttu-id="ba9fe-444">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-444">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-445">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-446">96</span><span class="sxs-lookup"><span data-stu-id="ba9fe-446">96</span></span> |
| <span data-ttu-id="ba9fe-447">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-447">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-449">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-449">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-450">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-451">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-452">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-453">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-455">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-455">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-457">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-459">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-459">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-461">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-461">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-462">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-462">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-463">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-463">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-464">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-464">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-465">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-465">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-466">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-466">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-467">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-467">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-469">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-470">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-471">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-472">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-473">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-474">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-475">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-476">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-476">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-477">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-478">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-479">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-480">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-481">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-481">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-482">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-483">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-484">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-485">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-485">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-487">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-487">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-488">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-488">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-489">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-489">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-490">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-490">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-491">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-491">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-492">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-492">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-493">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-493">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-495">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-496">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-497">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-498">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-498">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-499">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="ba9fe-500">DXGI_FORMAT_R32G32B32 \_ FLOAT<sup>FCS</sup> (6) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-500">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="ba9fe-501">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-501">Target</span></span> | <span data-ttu-id="ba9fe-502">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-502">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-503">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-504">96</span><span class="sxs-lookup"><span data-stu-id="ba9fe-504">96</span></span> |
| <span data-ttu-id="ba9fe-505">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-505">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-507">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-507">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-509">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-509">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-511">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-511">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-512">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-512">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-514">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-514">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-516">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-518">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-520">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-522">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-522">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-524">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-524">Shader sample (any filter)</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-526">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-526">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-527">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-527">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-528">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-528">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-529">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-529">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-530">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-530">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-532">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-532">Mipmap Auto-Generation</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-534">RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-536">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-536">Blendable RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="ba9fe-538">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-538">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-539">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-539">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-540">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-540">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-541">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-541">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-542">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-542">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-543">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-543">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-544">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-544">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-545">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-545">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-546">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-546">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-547">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-547">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-548">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-548">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-549">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-549">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-550">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-550">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-551">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-551">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-553">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-553">4x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="ba9fe-555">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-555">8x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="ba9fe-557">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-557">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-559">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-559">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-561">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-561">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-563">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-563">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-564">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-564">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-566">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-566">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-567">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-567">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-568">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-568">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-569">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-569">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-570">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-570">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="ba9fe-571">DXGI_FORMAT_R32G32B32 \_ UINT<sup>FCS</sup> (7) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-571">DXGI_FORMAT_R32G32B32\_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="ba9fe-572">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-572">Target</span></span> | <span data-ttu-id="ba9fe-573">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-573">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-574">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-574">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-575">96</span><span class="sxs-lookup"><span data-stu-id="ba9fe-575">96</span></span> |
| <span data-ttu-id="ba9fe-576">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-576">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-578">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-578">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-580">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-580">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-582">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-583">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-583">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-585">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-587">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-589">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-591">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-591">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-593">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-593">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-595">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-595">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-596">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-596">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-597">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-597">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-598">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-598">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-599">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-600">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-600">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-602">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-602">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-603">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-603">RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-605">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-606">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-606">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-608">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-608">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-609">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-609">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-610">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-610">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-611">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-611">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-612">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-612">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-613">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-613">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-614">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-614">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-615">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-615">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-616">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-616">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-617">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-617">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-618">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-618">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-619">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-619">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-620">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-620">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-622">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-622">4x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="ba9fe-624">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-624">8x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="ba9fe-626">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-626">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-628">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-628">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-629">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-629">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-631">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-631">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-632">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-632">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-634">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-634">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-635">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-635">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-636">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-636">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-637">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-637">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-638">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-638">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="ba9fe-639">DXGI_FORMAT_R32G32B32 \_ 聖的<sup>FCS</sup> (8) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-639">DXGI_FORMAT_R32G32B32\_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="ba9fe-640">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-640">Target</span></span> | <span data-ttu-id="ba9fe-641">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-641">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-642">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-642">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-643">96</span><span class="sxs-lookup"><span data-stu-id="ba9fe-643">96</span></span> |
| <span data-ttu-id="ba9fe-644">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-644">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-646">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-646">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-648">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-648">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-650">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-650">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-651">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-651">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-653">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-655">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-657">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-659">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-661">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-661">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-663">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-664">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-665">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-666">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-666">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-667">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-668">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-668">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-670">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-670">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-671">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-671">RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-673">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-673">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-674">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-675">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-676">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-677">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-678">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-678">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-679">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-680">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-681">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-682">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-683">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-683">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-684">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-685">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-686">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-687">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-687">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-689">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-689">4x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="ba9fe-691">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-691">8x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="ba9fe-693">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-693">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-695">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-696">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-696">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-698">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-698">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-699">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-699">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-701">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-701">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-702">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-702">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-703">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-703">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-704">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-704">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-705">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-705">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="ba9fe-706">DXGI_FORMAT_R16G16B16A16 無別 \_ <sup>電腦</sup> (9) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-706">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="ba9fe-707">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-707">Target</span></span> | <span data-ttu-id="ba9fe-708">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-708">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-709">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-709">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-710">64</span><span class="sxs-lookup"><span data-stu-id="ba9fe-710">64</span></span> |
| <span data-ttu-id="ba9fe-711">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-711">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-713">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-713">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-714">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-714">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-715">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-715">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-716">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-716">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-717">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-717">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-719">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-719">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-721">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-721">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-723">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-723">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-725">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-725">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-726">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-726">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-727">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-727">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-728">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-728">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-729">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-729">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-730">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-730">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-731">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-731">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-733">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-733">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-734">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-734">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-735">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-735">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-736">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-736">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-737">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-738">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-739">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-740">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-740">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-741">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-741">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-742">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-742">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-743">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-743">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-744">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-744">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-745">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-745">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-746">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-746">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-747">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-747">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-748">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-748">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-749">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-749">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-751">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-751">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-752">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-752">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-753">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-753">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-754">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-754">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-755">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-755">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-756">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-756">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-757">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-757">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-759">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-759">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-760">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-760">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-761">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-761">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-762">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-762">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-764">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-764">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="ba9fe-765">DXGI_FORMAT_R16G16B16A16 \_ FLOAT<sup>FCS</sup> (10) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-765">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="ba9fe-766">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-766">Target</span></span> | <span data-ttu-id="ba9fe-767">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-767">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-768">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-768">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-769">64</span><span class="sxs-lookup"><span data-stu-id="ba9fe-769">64</span></span> |
| <span data-ttu-id="ba9fe-770">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-770">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-772">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-772">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-774">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-774">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-776">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-776">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-777">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-777">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-778">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-778">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-780">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-780">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-782">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-782">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-784">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-786">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-786">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-788">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-788">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-790">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-790">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-791">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-791">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-792">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-792">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-793">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-793">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-794">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-794">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-796">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-796">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-798">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-798">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-800">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-800">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-802">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-802">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-803">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-803">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-804">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-804">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-805">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-805">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-806">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-806">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-807">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-807">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-808">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-808">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-809">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-809">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-810">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-810">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-811">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-811">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-812">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-812">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-813">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-813">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-814">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-814">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-815">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-815">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-817">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-817">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-819">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-819">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-821">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-821">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-823">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-823">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-825">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-825">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-827">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-827">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-829">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-829">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-831">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-831">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-832">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-832">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-834">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-834">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-836">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-836">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-838">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-838">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="ba9fe-839">DXGI_FORMAT_R16G16B16A16 \_ UNORM 的<sup>FCS</sup> (11) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-839">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="ba9fe-840">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-840">Target</span></span> | <span data-ttu-id="ba9fe-841">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-841">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-842">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-842">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-843">64</span><span class="sxs-lookup"><span data-stu-id="ba9fe-843">64</span></span> |
| <span data-ttu-id="ba9fe-844">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-844">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-846">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-846">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-848">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-848">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-850">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-850">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-851">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-851">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-852">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-852">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-854">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-854">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-856">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-856">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-858">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-860">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-860">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-862">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-862">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-864">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-864">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-865">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-865">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-866">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-866">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-867">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-867">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-868">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-868">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-870">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-870">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-872">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-872">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-874">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-874">Blendable RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-876">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-877">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-878">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-879">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-880">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-880">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-881">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-882">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-883">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-884">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-885">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-885">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-886">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-887">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-888">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-889">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-889">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-891">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-891">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-893">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-893">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-895">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-895">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-897">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-897">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-899">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-899">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-901">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-901">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-902">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-902">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-904">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-905">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-906">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-907">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-907">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-909">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-909">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="ba9fe-910">DXGI_FORMAT_R16G16B16A16 \_ UINT<sup>FCS</sup> (12) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-910">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="ba9fe-911">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-911">Target</span></span> | <span data-ttu-id="ba9fe-912">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-912">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-913">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-913">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-914">64</span><span class="sxs-lookup"><span data-stu-id="ba9fe-914">64</span></span> |
| <span data-ttu-id="ba9fe-915">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-915">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-917">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-917">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-919">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-919">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-921">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-921">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-922">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-922">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-923">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-923">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-925">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-927">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-929">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-929">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-931">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-931">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-933">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-934">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-935">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-936">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-936">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-937">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-938">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-938">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-940">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-940">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-941">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-941">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-943">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-943">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-944">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-944">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-946">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-946">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-947">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-947">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-948">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-948">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-949">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-949">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-950">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-950">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-951">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-951">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-952">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-952">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-953">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-953">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-954">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-954">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-955">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-955">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-956">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-956">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-957">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-957">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-958">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-958">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-960">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-960">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-962">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-962">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-964">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-964">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-966">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-966">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-967">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-967">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-969">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-969">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-970">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-970">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-972">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-972">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-973">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-973">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-974">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-974">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-975">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-975">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-977">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-977">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="ba9fe-978">DXGI_FORMAT_R16G16B16A16 \_ SNORM 的<sup>FCS</sup> (13) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-978">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="ba9fe-979">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-979">Target</span></span> | <span data-ttu-id="ba9fe-980">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-980">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-981">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-981">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-982">64</span><span class="sxs-lookup"><span data-stu-id="ba9fe-982">64</span></span> |
| <span data-ttu-id="ba9fe-983">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-983">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-985">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-985">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-987">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-987">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-989">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-990">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-991">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-993">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-993">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-995">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-995">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-997">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-997">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-999">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-999">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1001">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1001">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1003">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1003">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1004">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1004">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1005">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1005">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-1006">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1006">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-1007">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1007">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1009">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1009">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1011">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1013">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1013">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1014">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1014">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-1015">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1015">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-1016">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1016">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1017">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1017">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1018">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1018">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-1019">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1019">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-1020">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1020">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1021">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1021">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-1022">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1022">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-1023">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1023">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-1024">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1024">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-1025">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1025">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1026">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1026">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1027">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1027">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1029">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1029">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1031">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1031">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1033">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1033">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1035">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1035">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1037">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1037">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1039">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1039">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-1040">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1040">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1042">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1042">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-1043">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1043">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-1044">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1044">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-1045">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1045">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1047">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1047">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="ba9fe-1048">DXGI_FORMAT_R16G16B16A16 \_ 聖的<sup>FCS</sup> (14) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1048">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="ba9fe-1049">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1049">Target</span></span> | <span data-ttu-id="ba9fe-1050">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1050">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-1051">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1051">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-1052">64</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1052">64</span></span> |
| <span data-ttu-id="ba9fe-1053">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1053">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1055">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1055">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1057">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1057">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1059">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1059">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1060">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1060">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1061">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1061">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1063">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1063">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1065">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1065">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1067">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1067">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1069">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1069">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1071">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1071">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1072">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1072">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1073">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1073">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1074">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1074">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-1075">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1075">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-1076">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1076">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1078">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1078">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-1079">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1079">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1081">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1081">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1082">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1082">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-1083">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1083">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-1084">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1084">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1085">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1085">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1086">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1086">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-1087">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1087">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-1088">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1088">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1089">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1089">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-1090">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1090">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-1091">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1091">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-1092">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1092">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-1093">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1093">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1094">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1094">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1095">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1095">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1097">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1097">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1099">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1099">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1101">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1101">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1103">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1103">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-1104">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1104">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1106">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1106">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-1107">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1107">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1109">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1109">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-1110">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1110">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-1111">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1111">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-1112">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1112">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1114">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1114">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="ba9fe-1115">DXGI_FORMAT_R32G32 無別 \_ <sup>電腦</sup> (15) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1115">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="ba9fe-1116">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1116">Target</span></span> | <span data-ttu-id="ba9fe-1117">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1117">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-1118">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1118">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-1119">64</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1119">64</span></span> |
| <span data-ttu-id="ba9fe-1120">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1120">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1122">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1122">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1123">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1123">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1124">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1124">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1125">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1125">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1126">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1128">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1130">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1132">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1132">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1134">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1134">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-1135">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1135">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1136">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1136">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1137">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1137">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1138">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1138">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-1139">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1139">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-1140">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1140">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1142">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-1143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1143">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1144">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1145">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-1146">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-1147">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1148">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1149">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1149">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-1150">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-1151">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1152">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-1153">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-1154">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1154">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-1155">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-1156">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1157">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1158">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1158">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1160">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1160">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1161">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1161">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1162">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1162">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-1163">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1163">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-1164">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1164">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1165">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1165">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-1166">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1166">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1168">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1168">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-1169">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1169">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-1170">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1170">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-1171">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1171">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-1172">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1172">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="ba9fe-1173">DXGI_FORMAT_R32G32 \_ FLOAT<sup>FCS</sup> (16) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1173">DXGI_FORMAT_R32G32\_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="ba9fe-1174">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1174">Target</span></span> | <span data-ttu-id="ba9fe-1175">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1175">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-1176">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1176">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-1177">64</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1177">64</span></span> |
| <span data-ttu-id="ba9fe-1178">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1178">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1180">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1180">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1182">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1182">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1184">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1184">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1185">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1185">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1187">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1187">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1189">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1189">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1191">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1191">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1193">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1193">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1195">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1195">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1197">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1197">Shader sample (any filter)</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1199">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1199">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1200">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1200">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1201">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1201">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-1202">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1202">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-1203">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1203">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1205">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1205">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1207">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1207">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1209">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1209">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1211">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1211">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-1212">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1212">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-1213">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1213">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1214">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1214">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1215">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1215">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-1216">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1216">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-1217">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1217">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1218">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1218">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-1219">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1219">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-1220">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1220">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-1221">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1221">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-1222">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1222">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1223">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1223">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1224">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1224">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1226">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1226">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1228">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1228">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1230">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1230">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1232">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1232">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1234">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1234">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1236">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1236">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-1237">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1237">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1239">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1239">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-1240">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1240">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-1241">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1241">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-1242">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1242">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-1243">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1243">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="ba9fe-1244">DXGI_FORMAT_R32G32 \_ UINT<sup>FCS</sup> (17) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1244">DXGI_FORMAT_R32G32\_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="ba9fe-1245">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1245">Target</span></span> | <span data-ttu-id="ba9fe-1246">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1246">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-1247">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1247">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-1248">64</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1248">64</span></span> |
| <span data-ttu-id="ba9fe-1249">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1249">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1251">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1251">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1253">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1253">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1255">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1255">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1256">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1256">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1258">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1258">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1260">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1260">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1262">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1262">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1264">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1264">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1266">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1266">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1268">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1268">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1269">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1269">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1270">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1270">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1271">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1271">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-1272">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1272">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-1273">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1273">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1275">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1275">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-1276">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1276">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1278">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1278">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1279">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1279">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1281">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1281">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-1282">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1282">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1283">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1283">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1284">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1284">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-1285">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1285">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-1286">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1286">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1287">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1287">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-1288">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1288">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-1289">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1289">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-1290">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1290">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-1291">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1291">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1292">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1292">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1293">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1293">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1295">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1295">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1297">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1297">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1299">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1299">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1301">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1301">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-1302">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1302">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1304">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1304">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-1305">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1305">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1307">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1307">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-1308">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1308">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-1309">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1309">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-1310">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1310">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-1311">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1311">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="ba9fe-1312">DXGI_FORMAT_R32G32 \_ 聖的<sup>FCS</sup> (18) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1312">DXGI_FORMAT_R32G32\_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="ba9fe-1313">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1313">Target</span></span> | <span data-ttu-id="ba9fe-1314">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1314">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-1315">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1315">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-1316">64</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1316">64</span></span> |
| <span data-ttu-id="ba9fe-1317">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1317">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1319">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1319">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1321">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1321">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1323">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1323">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1324">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1324">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1326">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1326">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1328">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1328">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1330">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1330">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1332">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1332">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1334">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1334">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1336">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1336">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1337">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1337">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1338">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1338">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1339">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1339">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-1340">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1340">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-1341">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1341">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1343">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1343">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-1344">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1344">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1346">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1346">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1347">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1347">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-1348">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1348">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-1349">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1349">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1350">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1350">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1351">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1351">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-1352">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1352">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-1353">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1353">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1354">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1354">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-1355">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1355">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-1356">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1356">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-1357">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1357">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-1358">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1358">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1359">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1359">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1360">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1360">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1362">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1362">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1364">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1364">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1366">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1366">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1368">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1368">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-1369">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1369">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1371">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1371">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-1372">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1372">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1374">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-1375">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-1376">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-1377">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1377">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-1378">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="ba9fe-1379">DXGI_FORMAT_R32G8X24 無別 \_ <sup>電腦</sup> (19) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1379">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="ba9fe-1380">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1380">Target</span></span> | <span data-ttu-id="ba9fe-1381">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1381">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-1382">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-1383">64</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1383">64</span></span> |
| <span data-ttu-id="ba9fe-1384">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1384">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1386">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1386">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1387">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1387">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1388">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1388">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1389">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1389">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1390">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1390">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1392">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1394">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1394">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-1395">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1395">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1397">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1397">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-1398">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1399">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1400">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1401">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1401">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-1402">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-1403">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1403">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1405">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-1406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1406">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1407">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1407">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1408">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1408">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-1409">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1409">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-1410">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1410">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1411">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1411">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1412">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1412">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-1413">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1413">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-1414">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1414">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1415">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1415">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-1416">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1416">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-1417">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1417">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-1418">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1418">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-1419">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1419">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1420">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1420">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1421">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1421">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1423">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1423">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1424">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1424">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1425">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1425">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-1426">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1426">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-1427">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1427">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1428">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1428">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-1429">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1429">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1431">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1431">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-1432">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1432">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-1433">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1433">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-1434">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1434">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-1435">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1435">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a><span data-ttu-id="ba9fe-1436">DXGI_FORMAT_D32 \_ FLOAT \_ S8X24 \_ UINT<sup>FCS</sup> (20) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1436">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FCS</sup> (20)</span></span>
| <span data-ttu-id="ba9fe-1437">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1437">Target</span></span> | <span data-ttu-id="ba9fe-1438">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1438">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-1439">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1439">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-1440">64</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1440">64</span></span> |
| <span data-ttu-id="ba9fe-1441">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1441">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1443">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1443">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1444">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1444">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1445">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1446">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1447">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1449">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1449">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1451">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1451">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-1452">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1452">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1454">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1454">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-1455">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1455">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1456">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1456">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1457">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1457">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1458">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1458">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-1459">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1459">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-1460">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1460">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1462">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1462">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-1463">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1463">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1464">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1464">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1465">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1465">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-1466">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1466">Depth/Stencil Target</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1468">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1468">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1469">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1469">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1470">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1470">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-1471">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1471">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-1472">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1472">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1473">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1473">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-1474">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1474">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-1475">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1475">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-1476">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1476">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-1477">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1477">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1478">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1478">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1479">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1479">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1481">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1481">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1483">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1483">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1485">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1485">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1487">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1487">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-1488">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1488">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1489">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1489">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-1490">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1490">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1492">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1492">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-1493">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1493">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-1494">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1494">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-1495">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1495">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-1496">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1496">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a><span data-ttu-id="ba9fe-1497">DXGI_FORMAT_R32 \_ FLOAT X8X24 無型別 \_ \_ <sup>FCS</sup> (21) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1497">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FCS</sup> (21)</span></span>
| <span data-ttu-id="ba9fe-1498">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1498">Target</span></span> | <span data-ttu-id="ba9fe-1499">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1499">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-1500">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1500">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-1501">64</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1501">64</span></span> |
| <span data-ttu-id="ba9fe-1502">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1502">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1504">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1504">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1505">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1505">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1506">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1506">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1507">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1507">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1508">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1508">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1510">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1510">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1512">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-1513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1513">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1515">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1515">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1517">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1517">Shader sample (any filter)</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1519">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1519">Shader sample\_c (comparison filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1521">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1521">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1522">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1522">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-1523">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1523">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-1524">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1524">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1526">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1526">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-1527">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1527">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1528">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1528">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1529">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1529">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-1530">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1530">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-1531">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1531">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1532">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1532">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1533">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1533">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-1534">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1534">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-1535">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1535">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1536">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1536">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-1537">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1537">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-1538">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1538">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-1539">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1539">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-1540">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1540">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1541">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1541">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1542">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1542">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1544">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1544">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1545">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1545">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1546">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1546">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-1547">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1547">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-1548">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1548">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1549">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1549">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-1550">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1550">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1552">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1552">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-1553">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1553">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-1554">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1554">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-1555">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1555">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-1556">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1556">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a><span data-ttu-id="ba9fe-1557">DXGI_FORMAT_X32 無別 \_ \_ G8X24 \_ UINT<sup>FCS</sup> (22) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1557">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FCS</sup> (22)</span></span>
| <span data-ttu-id="ba9fe-1558">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1558">Target</span></span> | <span data-ttu-id="ba9fe-1559">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1559">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-1560">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1560">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-1561">64</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1561">64</span></span> |
| <span data-ttu-id="ba9fe-1562">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1562">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1564">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1564">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1565">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1565">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1566">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1566">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1567">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1567">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1568">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1568">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1570">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1570">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1572">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1572">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-1573">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1573">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1575">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1575">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1577">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1577">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1578">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1578">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1579">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1579">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1580">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1580">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-1581">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1581">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-1582">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1582">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1584">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1584">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-1585">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1585">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1586">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1586">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1587">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1587">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-1588">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1588">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-1589">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1589">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1590">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1590">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1591">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1591">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-1592">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1592">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-1593">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1593">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1594">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1594">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-1595">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1595">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-1596">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1596">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-1597">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1597">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-1598">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1598">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1599">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1599">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1600">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1600">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1602">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1602">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1603">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1603">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1604">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1604">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-1605">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1605">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-1606">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1606">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1607">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1607">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-1608">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1608">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1610">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1610">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-1611">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1611">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-1612">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1612">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-1613">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1613">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-1614">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1614">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="ba9fe-1615">DXGI_FORMAT_R10G10B10A2 無別 \_ <sup>電腦</sup> (23) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1615">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="ba9fe-1616">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1616">Target</span></span> | <span data-ttu-id="ba9fe-1617">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1617">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-1618">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1618">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-1619">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1619">32</span></span> |
| <span data-ttu-id="ba9fe-1620">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1620">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1622">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1622">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1623">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1623">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1624">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1624">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1625">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1625">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1626">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1626">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1628">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1628">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1630">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1630">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1632">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1632">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1634">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1634">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-1635">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1635">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1636">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1636">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1637">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1637">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1638">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1638">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-1639">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1639">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-1640">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1640">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1642">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1642">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-1643">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1643">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1644">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1644">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1645">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1645">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-1646">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1646">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-1647">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1647">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1648">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1648">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1649">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1649">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-1650">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1650">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-1651">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1651">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1652">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1652">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-1653">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1653">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-1654">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1654">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-1655">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1655">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-1656">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1656">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1657">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1657">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1658">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1658">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1660">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1660">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1661">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1661">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1662">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1662">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-1663">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1663">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-1664">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1664">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1665">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1665">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-1666">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1666">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1668">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1668">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-1669">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1669">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-1670">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1670">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-1671">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1671">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1673">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1673">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="ba9fe-1674">DXGI_FORMAT_R10G10B10A2 \_ UNORM 的<sup>FCS</sup> (24) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1674">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="ba9fe-1675">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1675">Target</span></span> | <span data-ttu-id="ba9fe-1676">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1676">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-1677">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1677">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-1678">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1678">32</span></span> |
| <span data-ttu-id="ba9fe-1679">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1679">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1681">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1681">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1683">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1683">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1685">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1685">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1686">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1686">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1687">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1687">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1689">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1689">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1691">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1691">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1693">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1693">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1695">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1695">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1697">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1697">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1699">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1699">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1700">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1700">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1701">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1701">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-1702">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1702">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-1703">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1703">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1705">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1705">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1707">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1707">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1709">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1709">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1711">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1711">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-1712">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1712">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-1713">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1713">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1714">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1714">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1715">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1715">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-1716">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1716">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-1717">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1717">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1718">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1718">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-1719">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1719">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-1720">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1720">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-1721">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1721">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-1722">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1722">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1723">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1723">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1724">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1724">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1726">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1726">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1728">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1728">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1730">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1730">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1732">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1732">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1734">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1734">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1736">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1736">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1738">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1738">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1740">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1740">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-1741">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1741">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1743">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1743">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1745">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1745">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1747">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1747">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="ba9fe-1748">DXGI_FORMAT_R10G10B10A2 \_ UINT<sup>FCS</sup> (25) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1748">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="ba9fe-1749">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1749">Target</span></span> | <span data-ttu-id="ba9fe-1750">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1750">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-1751">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1751">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-1752">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1752">32</span></span> |
| <span data-ttu-id="ba9fe-1753">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1753">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1755">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1755">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1757">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1757">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1759">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1760">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1761">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1763">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1763">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1765">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1765">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1767">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1767">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1769">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1769">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1771">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1771">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1772">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1772">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1773">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1773">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1774">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1774">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-1775">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1775">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-1776">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1776">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1778">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1778">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-1779">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1779">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1781">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1781">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1782">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1782">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1784">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1784">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-1785">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1785">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1786">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1786">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1787">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1787">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-1788">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1788">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-1789">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1789">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1790">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1790">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-1791">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1791">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-1792">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1792">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-1793">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1793">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-1794">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1794">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1795">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1795">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1796">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1796">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1798">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1798">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1800">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1800">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1802">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1802">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1804">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1804">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-1805">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1805">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1807">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1807">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-1808">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1808">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1810">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1810">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-1811">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1811">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-1812">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1812">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-1813">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1813">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1815">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1815">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="ba9fe-1816">DXGI_FORMAT_R10G10B10 \_ XR \_ 偏差 \_ A2 \_ UNORM<sup>FCS</sup> (89) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1816">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="ba9fe-1817">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1817">Target</span></span> | <span data-ttu-id="ba9fe-1818">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1818">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-1819">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1819">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-1820">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1820">32</span></span> |
| <span data-ttu-id="ba9fe-1821">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1821">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1823">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1823">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1824">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1824">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1825">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1825">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1826">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1826">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1827">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1827">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-1828">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1828">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1830">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1830">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-1831">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1831">TextureCube</span></span> | \- |
| <span data-ttu-id="ba9fe-1832">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1832">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-1833">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1833">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1834">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1834">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1835">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1835">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1836">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1836">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-1837">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1837">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-1838">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1838">Mipmap</span></span> | \- |
| <span data-ttu-id="ba9fe-1839">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1839">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-1840">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1840">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1841">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1841">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1842">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1842">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-1843">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1843">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-1844">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1844">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1845">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1845">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1846">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1846">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-1847">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1847">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-1848">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1848">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1849">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1849">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-1850">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1850">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-1851">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1851">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-1852">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1852">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-1853">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1853">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1854">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1854">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1855">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1855">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1857">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1857">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1858">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1858">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1859">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1859">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-1860">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1860">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-1861">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1861">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1862">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1862">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1864">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1864">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1866">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1866">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-1867">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1867">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1869">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1869">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1871">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1871">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1873">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1873">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="ba9fe-1874">DXGI_FORMAT_R11G11B10 \_ FLOAT<sup>FNS</sup> (26) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1874">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="ba9fe-1875">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1875">Target</span></span> | <span data-ttu-id="ba9fe-1876">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1876">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-1877">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1877">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-1878">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1878">32</span></span> |
| <span data-ttu-id="ba9fe-1879">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1879">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1881">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1881">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1883">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1883">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1885">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1885">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1886">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1886">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1887">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1887">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1889">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1889">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1891">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1891">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1893">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1893">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1895">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1895">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1897">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1897">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1899">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1899">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1900">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1900">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1901">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1901">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-1902">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1902">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-1903">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1903">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1905">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1905">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1907">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1907">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1909">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1909">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1911">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-1912">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-1913">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1914">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1915">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1915">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-1916">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1916">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-1917">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1917">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1918">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1918">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-1919">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1919">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-1920">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1920">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-1921">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1921">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-1922">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1922">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1923">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1923">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1924">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1924">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1926">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1926">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1928">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1928">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1930">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1930">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1932">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1932">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1934">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1934">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-1936">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1936">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-1937">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1937">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-1938">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1938">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-1939">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1939">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-1940">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1940">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-1941">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1941">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-1942">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1942">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="ba9fe-1943">DXGI_FORMAT_R8G8B8A8 無別 \_ <sup>電腦</sup> (27) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1943">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="ba9fe-1944">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1944">Target</span></span> | <span data-ttu-id="ba9fe-1945">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1945">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-1946">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1946">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-1947">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1947">32</span></span> |
| <span data-ttu-id="ba9fe-1948">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1948">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1950">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1950">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1951">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1951">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1952">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1952">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1953">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1953">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-1954">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1954">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1956">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1956">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1958">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1958">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1960">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1960">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1962">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1962">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-1963">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1963">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1964">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1964">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1965">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-1965">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-1966">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1966">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-1967">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1967">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-1968">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1968">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1970">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1970">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-1971">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1971">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1972">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1972">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1973">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1973">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-1974">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1974">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-1975">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1975">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1976">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1976">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-1977">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1977">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-1978">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1978">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-1979">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1979">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1980">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1980">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-1981">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1981">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-1982">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1982">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-1983">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1983">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-1984">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1984">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1985">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1985">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-1986">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1986">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1988">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1988">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1989">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1989">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-1990">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1990">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-1991">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1991">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-1992">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1992">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-1993">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1993">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-1994">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1994">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-1996">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1996">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-1997">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1997">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-1998">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1998">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-1999">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-1999">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2001">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2001">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="ba9fe-2002">DXGI_FORMAT_R8G8B8A8 \_ UNORM 的<sup>FCS</sup> (28) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2002">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="ba9fe-2003">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2003">Target</span></span> | <span data-ttu-id="ba9fe-2004">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2004">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-2005">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2005">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-2006">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2006">32</span></span> |
| <span data-ttu-id="ba9fe-2007">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2007">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2009">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2009">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2011">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2011">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2013">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2013">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2014">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2014">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2015">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2015">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2017">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2017">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2019">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2019">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2021">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2021">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2023">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2023">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2025">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2025">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2027">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2027">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2028">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2028">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2029">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2029">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-2030">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2030">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-2031">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2031">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2033">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2033">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2035">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2035">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2037">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2037">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2039">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2039">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-2040">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2040">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-2041">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2041">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2042">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2042">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2043">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2043">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-2044">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2044">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-2045">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2045">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2046">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2046">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-2047">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2047">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-2048">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2048">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-2049">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2049">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-2050">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2050">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2051">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2051">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2052">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2052">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2054">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2054">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2056">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2056">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2058">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2058">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2060">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2060">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2062">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2062">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2064">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2064">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2066">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2066">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2068">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2068">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-2069">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2069">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2071">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2071">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2073">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2073">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2075">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2075">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="ba9fe-2076">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ SRGB<sup>FCS</sup> (29) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2076">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="ba9fe-2077">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2077">Target</span></span> | <span data-ttu-id="ba9fe-2078">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2078">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-2079">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2079">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-2080">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2080">32</span></span> |
| <span data-ttu-id="ba9fe-2081">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2081">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2083">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2083">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2084">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2085">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2086">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2087">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2089">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2089">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2091">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2091">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2093">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2093">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2095">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2095">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2097">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2097">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2099">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2099">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2100">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2100">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2101">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2101">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-2102">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2102">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-2103">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2103">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2105">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2105">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2107">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2107">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2109">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2109">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2111">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2111">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-2112">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2112">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-2113">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2113">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2114">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2114">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2115">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2115">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-2116">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2116">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-2117">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2117">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2118">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2118">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-2119">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2119">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-2120">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2120">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-2121">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2121">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-2122">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2122">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2123">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2123">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2124">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2124">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2126">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2126">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2128">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2128">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2130">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2130">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2132">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2132">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2134">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2134">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2136">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2136">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2138">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2138">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2140">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2140">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-2141">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2141">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2143">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2143">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2145">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2145">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2147">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="ba9fe-2148">DXGI_FORMAT_R8G8B8A8 \_ UINT<sup>FCS</sup> (30) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2148">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="ba9fe-2149">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2149">Target</span></span> | <span data-ttu-id="ba9fe-2150">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2150">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-2151">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-2152">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2152">32</span></span> |
| <span data-ttu-id="ba9fe-2153">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2153">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2155">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2155">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2157">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2157">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2159">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2159">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2160">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2160">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2161">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2161">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2163">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2163">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2165">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2165">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2167">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2167">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2169">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2169">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2171">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2171">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2172">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2172">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2173">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2173">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2174">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2174">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-2175">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2175">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-2176">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2176">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2178">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2178">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-2179">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2179">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2181">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2181">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-2182">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2182">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2184">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2184">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-2185">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2185">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2186">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2186">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2187">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2187">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-2188">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2188">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-2189">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2189">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2190">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2190">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-2191">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2191">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-2192">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2192">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-2193">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2193">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-2194">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2194">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2195">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2195">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2196">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2196">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2198">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2198">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2200">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2200">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2202">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2202">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2204">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2204">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-2205">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2205">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2207">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2207">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-2208">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2208">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2210">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2210">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-2211">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2211">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-2212">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2212">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-2213">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2213">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2215">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2215">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="ba9fe-2216">DXGI_FORMAT_R8G8B8A8 \_ SNORM 的<sup>FCS</sup> (31) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2216">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="ba9fe-2217">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2217">Target</span></span> | <span data-ttu-id="ba9fe-2218">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2218">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-2219">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2219">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-2220">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2220">32</span></span> |
| <span data-ttu-id="ba9fe-2221">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2221">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2223">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2223">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2225">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2225">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2227">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2227">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2228">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2228">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2229">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2229">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2231">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2231">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2233">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2233">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2235">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2235">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2237">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2237">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2239">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2239">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2241">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2241">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2242">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2242">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2243">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2243">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-2244">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2244">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-2245">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2245">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2247">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2247">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2249">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2249">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2251">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2251">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-2252">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2252">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-2253">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2253">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-2254">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2254">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2255">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2255">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2256">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2256">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-2257">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2257">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-2258">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2258">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2259">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2259">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-2260">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2260">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-2261">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2261">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-2262">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2262">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-2263">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2263">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2264">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2264">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2265">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2265">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2267">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2267">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2269">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2269">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2271">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2271">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2273">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2273">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2275">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2275">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2277">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2277">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-2278">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2278">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2280">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2280">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-2281">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2281">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-2282">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2282">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-2283">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2283">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2285">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2285">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="ba9fe-2286">DXGI_FORMAT_R8G8B8A8 \_ 聖的<sup>FCS</sup> (32) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2286">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="ba9fe-2287">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2287">Target</span></span> | <span data-ttu-id="ba9fe-2288">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2288">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-2289">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2289">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-2290">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2290">32</span></span> |
| <span data-ttu-id="ba9fe-2291">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2291">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2293">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2293">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2295">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2295">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2297">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2297">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2298">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2298">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2299">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2299">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2301">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2301">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2303">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2303">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2305">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2305">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2307">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2307">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2309">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2309">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2310">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2310">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2311">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2311">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2312">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2312">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-2313">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2313">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-2314">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2314">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2316">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2316">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-2317">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2317">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2319">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2319">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-2320">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2320">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-2321">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2321">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-2322">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2322">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2323">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2323">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2324">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2324">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-2325">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2325">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-2326">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2326">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2327">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2327">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-2328">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2328">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-2329">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2329">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-2330">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2330">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-2331">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2331">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2332">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2332">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2333">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2333">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2335">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2335">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2337">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2337">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2339">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2339">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2341">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2341">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-2342">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2342">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2344">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2344">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-2345">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2345">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2347">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2347">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-2348">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2348">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-2349">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2349">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-2350">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2350">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2352">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2352">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="ba9fe-2353">DXGI_FORMAT_R16G16 無的 \_ <sup>電腦</sup> (33) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2353">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="ba9fe-2354">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2354">Target</span></span> | <span data-ttu-id="ba9fe-2355">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2355">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-2356">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2356">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-2357">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2357">32</span></span> |
| <span data-ttu-id="ba9fe-2358">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2358">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2360">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2360">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2361">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2361">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2362">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2362">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2363">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2363">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2364">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2364">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2366">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2366">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2368">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2368">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2370">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2370">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2372">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2372">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-2373">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2373">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2374">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2374">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2375">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2375">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2376">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2376">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-2377">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2377">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-2378">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2378">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2380">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2380">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-2381">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2381">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-2382">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2382">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-2383">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2383">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-2384">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2384">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-2385">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2385">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2386">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2386">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2387">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2387">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-2388">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2388">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-2389">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2389">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2390">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2390">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-2391">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2391">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-2392">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2392">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-2393">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2393">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-2394">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2394">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2395">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2395">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2396">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2396">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2398">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2398">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-2399">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2399">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-2400">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2400">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-2401">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2401">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-2402">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2402">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2403">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2403">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-2404">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2404">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2406">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2406">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-2407">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2407">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-2408">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2408">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-2409">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2409">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-2410">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2410">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="ba9fe-2411">DXGI_FORMAT_R16G16 \_ FLOAT<sup>FCS</sup> (34) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2411">DXGI_FORMAT_R16G16\_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="ba9fe-2412">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2412">Target</span></span> | <span data-ttu-id="ba9fe-2413">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2413">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-2414">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2414">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-2415">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2415">32</span></span> |
| <span data-ttu-id="ba9fe-2416">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2416">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2418">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2418">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2420">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2420">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2422">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2422">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2423">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2423">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2424">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2424">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2426">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2426">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2428">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2428">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2430">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2430">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2432">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2432">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2434">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2434">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2436">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2436">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2437">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2437">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2438">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2438">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-2439">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2439">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-2440">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2440">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2442">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2442">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2444">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2444">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2446">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2446">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2448">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2448">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-2449">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2449">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-2450">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2450">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2451">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2451">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2452">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2452">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-2453">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2453">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-2454">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2454">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2455">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2455">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-2456">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2456">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-2457">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2457">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-2458">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2458">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-2459">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2459">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2460">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2460">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2461">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2461">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2463">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2463">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2465">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2465">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2467">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2467">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2469">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2469">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2471">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2471">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2473">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2473">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-2474">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2474">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2476">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2476">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-2477">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2477">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-2478">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2478">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-2479">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2479">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-2480">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2480">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="ba9fe-2481">DXGI_FORMAT_R16G16 \_ UNORM 的<sup>FCS</sup> (35) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2481">DXGI_FORMAT_R16G16\_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="ba9fe-2482">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2482">Target</span></span> | <span data-ttu-id="ba9fe-2483">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2483">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-2484">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2484">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-2485">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2485">32</span></span> |
| <span data-ttu-id="ba9fe-2486">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2486">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2488">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2488">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2490">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2490">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2492">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2492">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2493">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2493">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2494">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2494">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2496">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2496">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2498">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2498">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2500">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2500">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2502">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2502">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2504">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2504">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2506">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2507">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2508">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2508">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-2509">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-2510">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2510">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2512">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2512">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2514">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2516">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2516">Blendable RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2518">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2518">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-2519">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2519">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-2520">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2520">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2521">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2521">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2522">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2522">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-2523">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2523">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-2524">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2524">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2525">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2525">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-2526">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2526">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-2527">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2527">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-2528">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2528">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-2529">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2529">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2530">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2530">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2531">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2531">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2533">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2533">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2535">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2535">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2537">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2537">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2539">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2539">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2541">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2541">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2543">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2543">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-2544">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2544">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2546">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2546">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-2547">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2547">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-2548">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2548">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-2549">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2549">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-2550">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2550">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="ba9fe-2551">DXGI_FORMAT_R16G16 \_ UINT<sup>FCS</sup> (36) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2551">DXGI_FORMAT_R16G16\_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="ba9fe-2552">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2552">Target</span></span> | <span data-ttu-id="ba9fe-2553">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2553">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-2554">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2554">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-2555">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2555">32</span></span> |
| <span data-ttu-id="ba9fe-2556">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2556">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2558">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2558">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2560">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2560">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2562">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2562">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2563">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2563">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2564">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2564">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2566">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2566">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2568">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2568">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2570">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2570">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2572">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2572">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2574">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2574">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2575">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2575">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2576">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2576">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2577">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2577">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-2578">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2578">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-2579">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2579">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2581">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2581">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-2582">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2582">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2584">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2584">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-2585">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2585">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2587">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2587">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-2588">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2588">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2589">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2589">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2590">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2590">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-2591">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2591">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-2592">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2592">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2593">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2593">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-2594">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2594">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-2595">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2595">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-2596">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2596">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-2597">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2597">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2598">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2598">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2599">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2599">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2601">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2601">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2603">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2603">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2605">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2605">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2607">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2607">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-2608">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2608">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2610">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2610">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-2611">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2611">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2613">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2613">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-2614">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2614">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-2615">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2615">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-2616">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2616">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-2617">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2617">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="ba9fe-2618">DXGI_FORMAT_R16G16 \_ SNORM 的<sup>FCS</sup> (37) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2618">DXGI_FORMAT_R16G16\_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="ba9fe-2619">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2619">Target</span></span> | <span data-ttu-id="ba9fe-2620">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2620">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-2621">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2621">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-2622">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2622">32</span></span> |
| <span data-ttu-id="ba9fe-2623">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2623">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2625">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2625">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2627">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2627">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2629">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2629">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2630">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2630">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2631">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2631">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2633">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2633">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2635">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2635">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2637">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2637">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2639">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2639">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2641">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2641">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2643">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2643">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2644">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2644">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2645">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2645">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-2646">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2646">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-2647">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2647">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2649">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2649">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2651">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2651">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2653">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2653">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-2654">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2654">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-2655">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2655">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-2656">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2656">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2657">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2657">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2658">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2658">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-2659">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2659">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-2660">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2660">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2661">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2661">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-2662">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2662">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-2663">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2663">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-2664">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2664">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-2665">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2665">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2666">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2666">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2667">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2667">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2669">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2669">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2671">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2671">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2673">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2673">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2675">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2675">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2677">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2677">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2679">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2679">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-2680">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2680">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2682">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2682">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-2683">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2683">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-2684">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2684">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-2685">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2685">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-2686">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2686">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="ba9fe-2687">DXGI_FORMAT_R16G16 \_ 聖的<sup>FCS</sup> (38) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2687">DXGI_FORMAT_R16G16\_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="ba9fe-2688">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2688">Target</span></span> | <span data-ttu-id="ba9fe-2689">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2689">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-2690">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2690">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-2691">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2691">32</span></span> |
| <span data-ttu-id="ba9fe-2692">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2692">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2694">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2694">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2696">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2696">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2698">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2698">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2699">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2699">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2700">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2700">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2702">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2702">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2704">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2704">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2706">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2706">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2708">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2708">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2710">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2710">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2711">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2711">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2712">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2712">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2713">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2713">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-2714">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2714">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-2715">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2715">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2717">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2717">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-2718">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2718">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2720">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2720">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-2721">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2721">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-2722">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2722">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-2723">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2723">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2724">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2724">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2725">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2725">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-2726">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2726">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-2727">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2727">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2728">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2728">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-2729">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2729">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-2730">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2730">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-2731">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2731">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-2732">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2732">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2733">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2733">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2734">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2734">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2736">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2736">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2738">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2738">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2740">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2740">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2742">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-2743">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2743">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2745">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2745">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-2746">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2746">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2748">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2748">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-2749">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2749">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-2750">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2750">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-2751">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2751">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-2752">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2752">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="ba9fe-2753">DXGI_FORMAT_R32 無的 \_ <sup>電腦</sup> (39) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2753">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="ba9fe-2754">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2754">Target</span></span> | <span data-ttu-id="ba9fe-2755">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2755">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-2756">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2756">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-2757">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2757">32</span></span> |
| <span data-ttu-id="ba9fe-2758">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2758">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2760">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2760">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2761">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2761">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2762">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2762">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2763">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2763">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2764">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2764">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2766">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2766">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2768">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2768">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2770">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2770">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2772">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2772">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-2773">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2773">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2774">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2774">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2775">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2775">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2776">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2776">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-2777">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2777">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-2778">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2778">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2780">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2780">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-2781">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2781">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-2782">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2782">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-2783">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2783">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-2784">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2784">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-2785">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2785">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2786">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2786">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2787">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2787">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-2788">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2788">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-2789">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2789">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2790">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2790">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-2791">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2791">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-2792">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2792">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-2793">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2793">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-2794">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2794">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2795">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2795">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2796">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2796">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2798">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2798">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-2799">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2799">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-2800">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2800">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-2801">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2801">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-2802">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2802">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2803">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2803">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-2804">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2804">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2806">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2806">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-2807">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2807">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-2808">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2808">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-2809">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2809">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2811">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="ba9fe-2812">DXGI_FORMAT_D32 \_ FLOAT<sup>FCS</sup> (40) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2812">DXGI_FORMAT_D32\_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="ba9fe-2813">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2813">Target</span></span> | <span data-ttu-id="ba9fe-2814">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2814">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-2815">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-2816">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2816">32</span></span> |
| <span data-ttu-id="ba9fe-2817">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2817">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2819">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2819">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2820">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2821">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2822">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2823">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2825">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2825">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2827">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2827">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-2828">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2828">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2830">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2830">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-2831">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2831">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2832">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2832">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2833">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2833">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2834">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2834">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-2835">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2835">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-2836">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2836">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2838">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2838">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-2839">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2839">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-2840">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-2841">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-2842">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2842">Depth/Stencil Target</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2844">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2844">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2845">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2845">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2846">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2846">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-2847">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2847">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-2848">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2848">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2849">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2849">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-2850">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2850">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-2851">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2851">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-2852">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2852">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-2853">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2853">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2854">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2854">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2855">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2855">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2857">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2857">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2859">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2859">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2861">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2861">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2863">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2863">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-2864">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2864">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2865">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2865">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-2866">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2866">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2868">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2868">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-2869">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2869">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-2870">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2870">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-2871">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2871">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2873">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2873">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="ba9fe-2874">DXGI_FORMAT_R32 \_ FLOAT<sup>FCS</sup> (41) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2874">DXGI_FORMAT_R32\_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="ba9fe-2875">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2875">Target</span></span> | <span data-ttu-id="ba9fe-2876">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2876">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-2877">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2877">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-2878">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2878">32</span></span> |
| <span data-ttu-id="ba9fe-2879">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2879">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2881">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2881">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2883">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2883">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2885">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2885">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-2886">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2886">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2888">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2888">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2890">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2890">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2892">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2892">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2894">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2894">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2896">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2896">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2898">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2898">Shader sample (any filter)</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2900">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2900">Shader sample\_c (comparison filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2902">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2902">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2903">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2903">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-2904">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2904">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-2905">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2905">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2907">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2907">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2909">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2909">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2911">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2911">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2913">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2913">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-2914">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2914">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-2915">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2915">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2916">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2916">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2917">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2917">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-2918">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2918">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-2919">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2919">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2920">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2920">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-2921">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2921">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-2922">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2922">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-2923">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2923">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-2924">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2924">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2925">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2925">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2926">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2926">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2928">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2928">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2930">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2930">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2932">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2932">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2934">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2934">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2936">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2936">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2938">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2938">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-2939">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2939">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2941">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2941">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-2942">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2942">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-2943">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2943">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-2944">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2944">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2946">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="ba9fe-2947">DXGI_FORMAT_R32 \_ UINT<sup>FCS</sup> (42) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2947">DXGI_FORMAT_R32\_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="ba9fe-2948">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2948">Target</span></span> | <span data-ttu-id="ba9fe-2949">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2949">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-2950">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-2951">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2951">32</span></span> |
| <span data-ttu-id="ba9fe-2952">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2952">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2954">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2954">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2956">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2956">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2958">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2958">Input Assembler Index Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2960">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2960">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2962">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2962">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2964">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2964">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2966">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2966">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2968">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2968">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2970">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2970">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2972">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2972">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2973">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2973">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2974">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-2974">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-2975">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2975">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-2976">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2976">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-2977">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2977">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2979">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2979">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-2980">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2980">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2982">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2982">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-2983">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2983">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-2985">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2985">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-2986">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2986">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2987">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2987">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-2988">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2988">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-2989">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2989">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-2990">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2990">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-2991">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2991">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-2992">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2992">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-2993">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2993">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-2994">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2994">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-2995">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2995">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2996">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2996">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-2997">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2997">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-2999">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-2999">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3001">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3001">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3003">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3003">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3005">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3005">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-3006">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3006">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3008">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3008">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-3009">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3009">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3011">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3011">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-3012">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3012">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-3013">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3013">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-3014">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3014">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3016">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3016">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="ba9fe-3017">DXGI_FORMAT_R32 \_ 聖的<sup>FCS</sup> (43) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3017">DXGI_FORMAT_R32\_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="ba9fe-3018">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3018">Target</span></span> | <span data-ttu-id="ba9fe-3019">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3019">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-3020">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3020">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-3021">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3021">32</span></span> |
| <span data-ttu-id="ba9fe-3022">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3022">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3024">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3024">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3026">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3026">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3028">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3028">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3029">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3029">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3031">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3031">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3033">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3033">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3035">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3035">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3037">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3037">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3039">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3039">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3041">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3041">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3042">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3042">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3043">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3043">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3044">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3044">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-3045">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3045">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-3046">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3046">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3048">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3048">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-3049">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3049">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3051">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3051">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3052">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3052">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-3053">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3053">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-3054">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3054">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3055">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3055">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3056">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3056">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-3057">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3057">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-3058">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3058">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3059">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3059">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-3060">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3060">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-3061">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3061">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-3062">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3062">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-3063">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3063">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3064">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3064">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3065">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3065">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3067">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3067">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3069">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3069">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3071">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3071">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3073">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3073">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-3074">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3074">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3076">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3076">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-3077">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3077">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3079">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3079">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-3080">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3080">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-3081">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3081">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-3082">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3082">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3084">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3084">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="ba9fe-3085">DXGI_FORMAT_R24G8 無的 \_ <sup>電腦</sup> (44) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3085">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="ba9fe-3086">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3086">Target</span></span> | <span data-ttu-id="ba9fe-3087">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3087">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-3088">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3088">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-3089">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3089">32</span></span> |
| <span data-ttu-id="ba9fe-3090">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3090">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3092">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3092">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3093">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3093">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3094">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3094">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3095">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3095">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3096">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3096">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3098">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3098">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3100">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3100">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-3101">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3101">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3103">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3103">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-3104">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3104">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3105">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3105">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3106">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3106">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3107">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3107">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-3108">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3108">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-3109">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3109">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3111">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3111">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-3112">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3112">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3113">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3113">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3114">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3114">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-3115">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3115">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-3116">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3116">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3117">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3117">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3118">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3118">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-3119">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3119">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-3120">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3120">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3121">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3121">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-3122">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3122">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-3123">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3123">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-3124">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3124">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-3125">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3125">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3126">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3126">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3127">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3127">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3129">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3129">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3130">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3130">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3131">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3131">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-3132">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3132">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-3133">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3133">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3134">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3134">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-3135">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3135">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3137">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3137">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-3138">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3138">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-3139">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3139">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-3140">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3140">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-3141">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3141">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a><span data-ttu-id="ba9fe-3142">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FCS</sup> (45) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3142">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FCS</sup> (45)</span></span>
| <span data-ttu-id="ba9fe-3143">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3143">Target</span></span> | <span data-ttu-id="ba9fe-3144">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3144">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-3145">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3145">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-3146">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3146">32</span></span> |
| <span data-ttu-id="ba9fe-3147">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3147">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3149">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3149">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3150">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3150">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3151">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3151">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3152">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3152">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3153">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3153">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3155">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3155">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3157">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3157">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-3158">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3158">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3160">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3160">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-3161">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3161">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3162">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3162">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3163">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3163">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3164">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3164">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-3165">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3165">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-3166">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3166">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3168">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3168">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-3169">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3169">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3170">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3170">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3171">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3171">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-3172">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3172">Depth/Stencil Target</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3174">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3174">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3175">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3175">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3176">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3176">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-3177">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3177">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-3178">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3178">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3179">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3179">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-3180">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3180">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-3181">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3181">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-3182">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3182">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-3183">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3183">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3184">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3184">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3185">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3185">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3187">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3187">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3189">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3189">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3191">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3191">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3193">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3193">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-3194">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3194">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3195">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3195">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-3196">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3196">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3198">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3198">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-3199">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3199">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-3200">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3200">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-3201">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3201">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-3202">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3202">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a><span data-ttu-id="ba9fe-3203">DXGI_FORMAT_R24 \_ UNORM \_ X8 \_ 無<sup></sup> (的 46) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3203">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FCS</sup> (46)</span></span>
| <span data-ttu-id="ba9fe-3204">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3204">Target</span></span> | <span data-ttu-id="ba9fe-3205">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3205">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-3206">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3206">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-3207">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3207">32</span></span> |
| <span data-ttu-id="ba9fe-3208">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3208">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3210">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3210">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3211">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3211">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3212">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3212">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3213">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3213">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3214">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3214">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3216">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3216">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3218">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3218">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-3219">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3219">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3221">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3221">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3223">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3223">Shader sample (any filter)</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3225">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3225">Shader sample\_c (comparison filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3227">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3227">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3228">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3228">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-3229">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3229">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-3230">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3230">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3232">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3232">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-3233">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3233">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3234">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3234">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3235">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3235">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-3236">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3236">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-3237">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3237">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3238">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3238">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3239">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3239">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-3240">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3240">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-3241">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3241">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3242">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3242">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-3243">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3243">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-3244">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3244">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-3245">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3245">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-3246">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3246">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3247">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3247">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3248">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3248">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3250">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3250">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3251">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3251">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3252">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3252">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-3253">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3253">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-3254">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3254">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3255">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3255">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-3256">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3256">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3258">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3258">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-3259">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3259">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-3260">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3260">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-3261">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3261">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-3262">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3262">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a><span data-ttu-id="ba9fe-3263">DXGI_FORMAT_X24 無別 \_ \_ G8 \_ UINT<sup>FCS</sup> (47) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3263">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FCS</sup> (47)</span></span>
| <span data-ttu-id="ba9fe-3264">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3264">Target</span></span> | <span data-ttu-id="ba9fe-3265">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3265">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-3266">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3266">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-3267">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3267">32</span></span> |
| <span data-ttu-id="ba9fe-3268">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3268">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3270">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3270">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3271">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3271">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3272">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3272">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3273">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3273">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3274">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3274">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3276">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3276">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3278">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3278">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-3279">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3279">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3281">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3281">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3283">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3283">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3284">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3284">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3285">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3285">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3286">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3286">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-3287">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3287">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-3288">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3288">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3290">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3290">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-3291">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3291">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3292">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3292">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3293">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3293">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-3294">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3294">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-3295">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3295">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3296">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3296">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3297">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3297">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-3298">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3298">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-3299">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3299">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3300">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3300">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-3301">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3301">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-3302">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3302">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-3303">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3303">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-3304">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3304">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3305">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3305">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3306">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3306">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3308">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3308">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3309">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3309">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3310">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3310">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-3311">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3311">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-3312">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3312">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3313">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3313">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-3314">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3314">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3316">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3316">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-3317">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3317">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-3318">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3318">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-3319">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3319">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-3320">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3320">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="ba9fe-3321">DXGI_FORMAT_R8G8 無的 \_ <sup>電腦</sup> (48) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3321">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="ba9fe-3322">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3322">Target</span></span> | <span data-ttu-id="ba9fe-3323">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3323">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-3324">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3324">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-3325">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3325">16</span></span> |
| <span data-ttu-id="ba9fe-3326">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3326">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3328">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3328">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3329">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3329">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3330">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3330">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3331">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3331">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3332">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3332">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3334">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3336">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3336">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3338">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3338">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3340">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3340">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-3341">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3341">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3342">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3342">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3343">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3343">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3344">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3344">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-3345">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3345">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-3346">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3346">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3348">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3348">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-3349">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3349">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3350">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3350">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3351">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3351">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-3352">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3352">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-3353">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3353">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3354">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3354">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3355">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3355">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-3356">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3356">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-3357">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3357">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3358">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3358">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-3359">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3359">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-3360">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3360">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-3361">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3361">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-3362">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3362">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3363">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3363">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3364">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3364">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3366">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3366">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3367">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3367">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3368">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3368">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-3369">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-3370">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3370">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3371">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3371">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-3372">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3372">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3374">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-3375">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-3376">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-3377">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3377">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-3378">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="ba9fe-3379">DXGI_FORMAT_R8G8 \_ UNORM 的<sup>FCS</sup> (49) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3379">DXGI_FORMAT_R8G8\_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="ba9fe-3380">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3380">Target</span></span> | <span data-ttu-id="ba9fe-3381">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3381">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-3382">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-3383">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3383">16</span></span> |
| <span data-ttu-id="ba9fe-3384">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3384">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3386">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3386">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3388">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3388">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3390">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3390">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3391">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3391">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3392">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3392">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3394">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3394">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3396">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3396">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3398">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3398">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3400">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3400">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3402">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3402">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3404">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3404">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3405">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3405">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3406">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3406">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-3407">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3407">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-3408">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3408">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3410">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3410">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3412">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3412">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3414">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3414">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3416">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3416">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-3417">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3417">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-3418">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3418">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3419">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3419">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3420">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3420">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-3421">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3421">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-3422">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3422">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3423">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3423">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-3424">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3424">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-3425">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3425">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-3426">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3426">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-3427">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3427">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3428">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3428">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3429">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3429">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3431">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3431">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3433">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3433">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3435">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3435">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3437">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3437">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3439">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3439">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3441">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-3442">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3442">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3444">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3444">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-3445">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3445">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-3446">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3446">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-3447">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3447">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3449">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3449">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="ba9fe-3450">DXGI_FORMAT_R8G8 \_ UINT<sup>FCS</sup> (50) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3450">DXGI_FORMAT_R8G8\_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="ba9fe-3451">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3451">Target</span></span> | <span data-ttu-id="ba9fe-3452">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3452">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-3453">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3453">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-3454">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3454">16</span></span> |
| <span data-ttu-id="ba9fe-3455">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3455">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3457">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3457">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3459">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3459">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3461">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3461">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3462">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3462">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3463">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3463">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3465">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3465">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3467">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3467">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3469">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3469">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3471">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3471">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3473">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3473">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3474">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3474">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3475">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3475">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3476">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3476">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-3477">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3477">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-3478">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3478">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3480">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3480">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-3481">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3481">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3483">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3483">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3484">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3484">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3486">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3486">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-3487">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3487">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3488">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3488">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3489">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3489">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-3490">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3490">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-3491">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3491">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3492">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3492">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-3493">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3493">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-3494">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3494">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-3495">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3495">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-3496">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3496">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3497">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3497">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3498">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3498">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3500">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3500">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3502">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3502">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3504">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3504">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3506">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3506">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-3507">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3507">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3509">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3509">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-3510">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3510">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3512">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3512">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-3513">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3513">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-3514">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3514">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-3515">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3515">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-3516">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3516">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="ba9fe-3517">DXGI_FORMAT_R8G8 \_ SNORM 的<sup>FCS</sup> (51) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3517">DXGI_FORMAT_R8G8\_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="ba9fe-3518">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3518">Target</span></span> | <span data-ttu-id="ba9fe-3519">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3519">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-3520">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3520">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-3521">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3521">16</span></span> |
| <span data-ttu-id="ba9fe-3522">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3522">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3524">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3524">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3526">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3526">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3528">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3528">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3529">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3529">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3530">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3530">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3532">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3532">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3534">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3534">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3536">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3536">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3538">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3538">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3540">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3540">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3542">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3542">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3543">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3543">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3544">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3544">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-3545">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3545">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-3546">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3546">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3548">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3548">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3550">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3550">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3552">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3552">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3553">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3553">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-3554">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3554">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-3555">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3555">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3556">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3556">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3557">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3557">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-3558">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3558">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-3559">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3559">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3560">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3560">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-3561">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3561">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-3562">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3562">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-3563">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3563">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-3564">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3564">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3565">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3565">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3566">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3566">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3568">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3568">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3570">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3570">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3572">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3572">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3574">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3574">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3576">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3576">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3578">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3578">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-3579">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3579">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3581">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3581">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-3582">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3582">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-3583">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3583">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-3584">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3584">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-3585">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3585">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="ba9fe-3586">DXGI_FORMAT_R8G8 \_ 聖的<sup>FCS</sup> (52) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3586">DXGI_FORMAT_R8G8\_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="ba9fe-3587">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3587">Target</span></span> | <span data-ttu-id="ba9fe-3588">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3588">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-3589">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3589">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-3590">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3590">16</span></span> |
| <span data-ttu-id="ba9fe-3591">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3591">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3593">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3593">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3595">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3595">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3597">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3597">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3598">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3598">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3599">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3599">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3601">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3601">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3603">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3603">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3605">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3607">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3607">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3609">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3609">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3610">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3610">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3611">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3611">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3612">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3612">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-3613">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3613">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-3614">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3614">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3616">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3616">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-3617">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3617">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3619">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3619">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3620">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3620">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-3621">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3621">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-3622">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3622">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3623">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3623">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3624">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3624">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-3625">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3625">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-3626">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3626">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3627">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3627">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-3628">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3628">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-3629">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3629">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-3630">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3630">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-3631">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3631">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3632">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3632">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3633">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3633">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3635">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3635">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3637">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3637">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3639">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3639">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3641">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3641">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-3642">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3642">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3644">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3644">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-3645">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3645">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3647">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3647">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-3648">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3648">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-3649">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3649">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-3650">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3650">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-3651">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3651">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="ba9fe-3652">DXGI_FORMAT_R16 無的 \_ <sup>電腦</sup> (53) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3652">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="ba9fe-3653">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3653">Target</span></span> | <span data-ttu-id="ba9fe-3654">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3654">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-3655">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3655">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-3656">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3656">16</span></span> |
| <span data-ttu-id="ba9fe-3657">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3657">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3659">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3659">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3660">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3660">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3661">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3661">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3662">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3662">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3663">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3663">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3665">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3665">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3667">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3667">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3669">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3669">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3671">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3671">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-3672">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3672">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3673">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3673">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3674">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3674">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3675">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3675">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-3676">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3676">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-3677">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3677">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3679">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3679">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-3680">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3680">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3681">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3681">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3682">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3682">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-3683">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3683">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-3684">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3684">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3685">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3685">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3686">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3686">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-3687">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3687">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-3688">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3688">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3689">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3689">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-3690">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3690">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-3691">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3691">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-3692">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3692">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-3693">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3693">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3694">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3694">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3695">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3695">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3697">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3697">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3698">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3698">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3699">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3699">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-3700">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3700">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-3701">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3701">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3702">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3702">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-3703">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3703">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3705">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3705">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-3706">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3706">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-3707">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3707">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-3708">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3708">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3710">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3710">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="ba9fe-3711">DXGI_FORMAT_R16 \_ FLOAT<sup>FCS</sup> (54) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3711">DXGI_FORMAT_R16\_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="ba9fe-3712">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3712">Target</span></span> | <span data-ttu-id="ba9fe-3713">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3713">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-3714">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3714">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-3715">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3715">16</span></span> |
| <span data-ttu-id="ba9fe-3716">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3716">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3718">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3718">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3720">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3720">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3722">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3722">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3723">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3723">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3724">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3724">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3726">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3728">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3730">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3730">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3732">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3732">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3734">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3734">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3736">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3736">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3737">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3737">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3738">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3738">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-3739">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3739">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-3740">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3740">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3742">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3742">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3744">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3744">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3746">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3746">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3748">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3748">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-3749">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3749">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-3750">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3750">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3751">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3751">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3752">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3752">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-3753">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3753">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-3754">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3754">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3755">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3755">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-3756">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3756">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-3757">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3757">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-3758">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3758">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-3759">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3759">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3760">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3760">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3761">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3761">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3763">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3763">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3765">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3765">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3767">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3767">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3769">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3769">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3771">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3771">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3773">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3773">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-3774">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3774">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3776">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3776">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-3777">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3777">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-3778">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3778">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-3779">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3779">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3781">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3781">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="ba9fe-3782">DXGI_FORMAT_D16 \_ UNORM 的<sup>FCS</sup> (55) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3782">DXGI_FORMAT_D16\_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="ba9fe-3783">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3783">Target</span></span> | <span data-ttu-id="ba9fe-3784">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3784">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-3785">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3785">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-3786">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3786">16</span></span> |
| <span data-ttu-id="ba9fe-3787">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3787">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3789">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3789">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3790">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3790">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3791">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3791">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3792">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3792">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3793">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3793">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3795">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3795">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3797">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-3798">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3798">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3800">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3800">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-3801">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3801">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3802">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3802">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3803">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3803">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3804">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3804">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-3805">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3805">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-3806">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3806">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3808">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3808">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-3809">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3809">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3810">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3810">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3811">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-3812">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3812">Depth/Stencil Target</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3814">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3814">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3815">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3815">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3816">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3816">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-3817">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3817">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-3818">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3818">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3819">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3819">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-3820">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3820">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-3821">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3821">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-3822">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3822">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-3823">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3823">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3824">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3824">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3825">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3825">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3827">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3827">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3829">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3829">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3831">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3831">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3833">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3833">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-3834">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3834">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3835">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3835">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-3836">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3836">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3838">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3838">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-3839">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3839">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-3840">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3840">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-3841">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3841">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3843">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3843">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="ba9fe-3844">DXGI_FORMAT_R16 \_ UNORM 的<sup>FCS</sup> (56) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3844">DXGI_FORMAT_R16\_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="ba9fe-3845">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3845">Target</span></span> | <span data-ttu-id="ba9fe-3846">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3846">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-3847">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3847">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-3848">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3848">16</span></span> |
| <span data-ttu-id="ba9fe-3849">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3849">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3851">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3851">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3853">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3853">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3855">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3855">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3856">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3856">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3857">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3857">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3859">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3859">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3861">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3861">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3863">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3863">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3865">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3865">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3867">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3867">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3869">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3869">Shader sample\_c (comparison filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3871">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3871">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3872">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3872">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-3873">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3873">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-3874">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3874">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3876">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3876">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3878">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3878">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3880">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3880">Blendable RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3882">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3882">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-3883">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3883">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-3884">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3884">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3885">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3885">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3886">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3886">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-3887">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3887">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-3888">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3888">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3889">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3889">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-3890">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3890">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-3891">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3891">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-3892">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3892">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-3893">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3893">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3894">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3894">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3895">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3895">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3897">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3897">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3899">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3899">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3901">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3901">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3903">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3903">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3905">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3905">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3907">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3907">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-3908">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3908">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3910">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3910">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-3911">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3911">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-3912">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3912">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-3913">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3913">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3915">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3915">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="ba9fe-3916">DXGI_FORMAT_R16 \_ UINT<sup>FCS</sup> (57) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3916">DXGI_FORMAT_R16\_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="ba9fe-3917">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3917">Target</span></span> | <span data-ttu-id="ba9fe-3918">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3918">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-3919">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3919">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-3920">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3920">16</span></span> |
| <span data-ttu-id="ba9fe-3921">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3921">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3923">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3923">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3925">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3925">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3927">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3927">Input Assembler Index Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3929">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3929">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3930">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3930">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3932">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3932">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3934">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3934">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3936">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3936">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3938">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3938">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3940">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3940">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3941">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3941">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3942">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3942">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-3943">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3943">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-3944">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3944">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-3945">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3945">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3947">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3947">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-3948">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3948">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3950">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3950">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-3951">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3951">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3953">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3953">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-3954">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3954">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3955">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3955">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-3956">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3956">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-3957">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3957">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-3958">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3958">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-3959">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3959">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-3960">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3960">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-3961">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3961">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-3962">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3962">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-3963">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3963">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3964">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3964">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-3965">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3965">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3967">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3967">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3969">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3969">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3971">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3971">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3973">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3973">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-3974">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3974">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-3976">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3976">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-3977">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3977">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3979">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3979">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-3980">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3980">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-3981">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3981">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-3982">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3982">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3984">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3984">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="ba9fe-3985">DXGI_FORMAT_R16 \_ SNORM 的<sup>FCS</sup> (58) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3985">DXGI_FORMAT_R16\_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="ba9fe-3986">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3986">Target</span></span> | <span data-ttu-id="ba9fe-3987">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3987">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-3988">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-3988">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-3989">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3989">16</span></span> |
| <span data-ttu-id="ba9fe-3990">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3990">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3992">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3992">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3994">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3994">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-3996">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3996">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3997">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3997">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-3998">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-3998">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4000">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4000">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4002">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4002">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4004">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4004">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4006">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4006">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4008">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4008">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4010">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4010">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4011">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4011">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4012">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4012">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-4013">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4013">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-4014">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4014">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4016">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4016">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4018">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4018">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4020">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4020">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4021">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4021">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-4022">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4022">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-4023">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4023">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4024">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4024">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4025">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4025">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-4026">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4026">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-4027">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4027">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4028">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4028">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-4029">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4029">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-4030">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4030">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-4031">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4031">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-4032">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4032">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4033">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4033">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4034">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4034">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4036">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4036">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4038">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4038">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4040">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4040">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4042">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4042">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4044">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4044">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4046">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4046">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-4047">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4047">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4049">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4049">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-4050">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4050">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-4051">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4051">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-4052">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4052">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4054">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4054">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="ba9fe-4055">DXGI_FORMAT_R16 \_ 聖的<sup>FCS</sup> (59) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4055">DXGI_FORMAT_R16\_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="ba9fe-4056">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4056">Target</span></span> | <span data-ttu-id="ba9fe-4057">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4057">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-4058">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4058">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-4059">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4059">16</span></span> |
| <span data-ttu-id="ba9fe-4060">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4060">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4062">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4062">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4064">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4064">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4066">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4066">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4067">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4067">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4068">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4068">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4070">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4070">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4072">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4072">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4074">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4074">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4076">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4076">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4078">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4078">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4079">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4079">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4080">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4080">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4081">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4081">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-4082">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4082">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-4083">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4083">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4085">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4085">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-4086">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4086">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4088">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4088">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4089">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4089">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-4090">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4090">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-4091">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4091">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4092">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4092">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4093">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4093">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-4094">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4094">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-4095">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4095">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4096">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4096">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-4097">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4097">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-4098">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4098">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-4099">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4099">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-4100">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4100">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4101">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4101">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4102">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4102">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4104">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4104">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4106">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4106">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4108">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4108">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4110">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4110">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-4111">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4111">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4113">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4113">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-4114">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4114">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4116">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4116">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-4117">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4117">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-4118">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4118">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-4119">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4119">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4121">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4121">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="ba9fe-4122">DXGI_FORMAT_R8 無的 \_ <sup>電腦</sup> (60) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4122">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="ba9fe-4123">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4123">Target</span></span> | <span data-ttu-id="ba9fe-4124">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4124">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-4125">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4125">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-4126">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4126">8</span></span> |
| <span data-ttu-id="ba9fe-4127">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4127">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4129">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4129">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4130">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4131">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4132">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4133">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4135">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4135">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4137">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4137">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4139">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4139">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4141">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4141">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-4142">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4142">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4143">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4143">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4144">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4144">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4145">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4145">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-4146">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4146">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-4147">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4147">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4149">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4149">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-4150">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4150">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4151">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4151">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4152">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4152">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-4153">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4153">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-4154">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4154">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4155">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4155">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4156">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4156">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-4157">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4157">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-4158">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4158">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4159">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4159">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-4160">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4160">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-4161">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4161">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-4162">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4162">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-4163">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4163">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4164">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4164">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4165">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4165">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4167">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4167">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4168">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4168">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4169">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4169">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-4170">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4170">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-4171">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4171">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4172">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4172">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-4173">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4173">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4175">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4175">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-4176">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4176">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-4177">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4177">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-4178">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4178">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4180">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4180">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="ba9fe-4181">DXGI_FORMAT_R8 \_ UNORM 的<sup>FCS</sup> (61) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4181">DXGI_FORMAT_R8\_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="ba9fe-4182">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4182">Target</span></span> | <span data-ttu-id="ba9fe-4183">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4183">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-4184">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4184">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-4185">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4185">8</span></span> |
| <span data-ttu-id="ba9fe-4186">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4186">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4188">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4188">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4190">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4190">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4192">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4192">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4193">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4193">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4194">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4194">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4196">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4196">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4198">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4198">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4200">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4200">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4202">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4202">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4204">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4204">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4206">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4206">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4207">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4207">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4208">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4208">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-4209">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4209">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-4210">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4210">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4212">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4212">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4214">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4214">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4216">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4216">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4218">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4218">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-4219">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4219">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-4220">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4220">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4221">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4221">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4222">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4222">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-4223">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4223">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-4224">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4224">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4225">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4225">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-4226">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4226">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-4227">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4227">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-4228">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4228">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-4229">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4229">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4230">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4230">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4231">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4231">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4233">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4233">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4235">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4235">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4237">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4237">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4239">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4239">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4241">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4241">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4243">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4243">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-4244">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4244">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4246">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4246">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-4247">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4247">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-4248">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4248">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-4249">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4249">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4251">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4251">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="ba9fe-4252">DXGI_FORMAT_R8 \_ UINT<sup>FCS</sup> (62) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4252">DXGI_FORMAT_R8\_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="ba9fe-4253">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4253">Target</span></span> | <span data-ttu-id="ba9fe-4254">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4254">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-4255">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4255">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-4256">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4256">8</span></span> |
| <span data-ttu-id="ba9fe-4257">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4257">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4259">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4259">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4261">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4261">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4263">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4263">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4264">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4264">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4265">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4265">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4267">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4269">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4271">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4271">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4273">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4273">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4275">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4275">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4276">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4276">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4277">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4277">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4278">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4278">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-4279">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4279">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-4280">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4280">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4282">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4282">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-4283">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4283">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4285">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4285">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4286">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4286">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4288">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4288">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-4289">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4289">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4290">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4290">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4291">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4291">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-4292">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4292">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-4293">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4293">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4294">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4294">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-4295">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4295">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-4296">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4296">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-4297">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4297">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-4298">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4298">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4299">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4299">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4300">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4300">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4302">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4302">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4304">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4304">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4306">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4306">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4308">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4308">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-4309">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4309">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4311">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4311">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-4312">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4312">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4314">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4314">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-4315">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4315">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-4316">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4316">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-4317">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4317">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4319">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4319">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="ba9fe-4320">DXGI_FORMAT_R8 \_ SNORM 的<sup>FCS</sup> (63) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4320">DXGI_FORMAT_R8\_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="ba9fe-4321">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4321">Target</span></span> | <span data-ttu-id="ba9fe-4322">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4322">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-4323">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4323">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-4324">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4324">8</span></span> |
| <span data-ttu-id="ba9fe-4325">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4325">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4327">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4327">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4329">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4329">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4331">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4331">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4332">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4332">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4333">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4333">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4335">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4335">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4337">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4337">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4339">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4339">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4341">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4341">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4343">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4343">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4345">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4345">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4346">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4346">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4347">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4347">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-4348">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4348">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-4349">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4349">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4351">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4351">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4353">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4353">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4355">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4355">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4356">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4356">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-4357">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4357">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-4358">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4358">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4359">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4359">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4360">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4360">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-4361">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4361">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-4362">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4362">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4363">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4363">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-4364">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4364">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-4365">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4365">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-4366">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4366">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-4367">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4367">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4368">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4368">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4369">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4369">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4371">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4371">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4373">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4373">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4375">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4375">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4377">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4377">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4379">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4379">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4381">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4381">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-4382">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4382">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4384">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-4385">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-4386">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-4387">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4387">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4389">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4389">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="ba9fe-4390">DXGI_FORMAT_R8 \_ 聖的<sup>FCS</sup> (64) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4390">DXGI_FORMAT_R8\_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="ba9fe-4391">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4391">Target</span></span> | <span data-ttu-id="ba9fe-4392">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4392">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-4393">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-4394">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4394">8</span></span> |
| <span data-ttu-id="ba9fe-4395">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4395">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4397">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4397">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4399">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4399">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4401">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4402">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4402">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4403">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4403">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4405">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4405">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4407">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4407">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4409">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4409">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4411">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4411">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4413">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4413">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4414">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4415">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4416">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4416">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-4417">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-4418">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4418">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4420">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4420">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-4421">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4421">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4423">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4423">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4424">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4424">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-4425">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4425">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-4426">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4426">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4427">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4427">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4428">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4428">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-4429">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4429">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-4430">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4430">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4431">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4431">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-4432">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4432">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-4433">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4433">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-4434">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4434">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-4435">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4435">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4436">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4436">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4437">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4437">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4439">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4439">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4441">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4441">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4443">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4443">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4445">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4445">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-4446">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4446">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4448">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4448">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-4449">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4449">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4451">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4451">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-4452">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4452">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-4453">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4453">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-4454">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4454">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4456">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4456">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="ba9fe-4457">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4457">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="ba9fe-4458">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4458">Target</span></span> | <span data-ttu-id="ba9fe-4459">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4459">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-4460">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4460">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-4461">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4461">8</span></span> |
| <span data-ttu-id="ba9fe-4462">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4462">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4464">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4464">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4465">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4465">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4466">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4466">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4467">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4467">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4468">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4468">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4470">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4470">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4472">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4472">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4474">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4474">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4476">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4476">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4478">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4478">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4480">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4480">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4481">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4481">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4482">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4482">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-4483">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4483">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-4484">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4484">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4486">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4486">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4488">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4488">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4490">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4490">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4492">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4492">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-4493">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4493">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-4494">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4494">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4495">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4495">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4496">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4496">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-4497">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4497">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-4498">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4498">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4499">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4499">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-4500">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4500">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-4501">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4501">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-4502">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4502">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-4503">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4503">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4504">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4504">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4505">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4505">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4507">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4507">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4509">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4509">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4511">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4511">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4513">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4513">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4515">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4515">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-4517">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4517">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-4518">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4518">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-4519">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4519">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-4520">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4520">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-4521">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4521">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-4522">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4522">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4524">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4524">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="ba9fe-4525">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4525">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="ba9fe-4526">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4526">Target</span></span> | <span data-ttu-id="ba9fe-4527">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4527">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-4528">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4528">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-4529">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4529">32</span></span> |
| <span data-ttu-id="ba9fe-4530">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4530">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4532">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4532">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4533">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4533">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4534">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4534">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4535">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4535">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4536">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4536">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4538">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4538">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4540">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4540">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4542">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4542">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4544">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4544">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4546">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4546">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4548">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4548">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4549">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4549">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4550">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4550">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-4551">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4551">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-4552">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4552">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4554">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4554">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-4555">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4555">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4556">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4556">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4557">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4557">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-4558">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4558">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-4559">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4559">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4560">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4560">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4561">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4561">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-4562">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4562">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-4563">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4563">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4564">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4564">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-4565">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4565">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-4566">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4566">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-4567">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4567">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-4568">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4568">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4569">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4569">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4570">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4570">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4572">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4572">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4573">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4573">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4574">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4574">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-4575">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4575">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-4576">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4576">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4577">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4577">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-4578">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4578">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-4579">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4579">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-4580">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4580">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-4581">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4581">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-4582">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4582">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-4583">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4583">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="ba9fe-4584">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4584">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="ba9fe-4585">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4585">Target</span></span> | <span data-ttu-id="ba9fe-4586">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4586">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-4587">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4587">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-4588">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4588">16</span></span> |
| <span data-ttu-id="ba9fe-4589">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4589">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4591">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4591">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4592">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4592">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4593">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4593">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4594">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4594">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4595">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4595">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4597">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4597">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4599">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4599">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4601">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4601">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4603">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4603">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4605">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4605">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4607">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4607">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4608">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4608">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4609">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4609">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-4610">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4610">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-4611">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4611">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4613">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-4614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4614">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4615">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4616">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-4617">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-4618">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4619">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4620">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4620">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-4621">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-4622">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4623">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-4624">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-4625">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4625">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-4626">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-4627">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4628">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4629">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4629">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4631">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4631">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4632">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4632">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4633">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4633">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-4634">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4634">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-4635">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4635">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4636">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4636">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-4637">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4637">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-4638">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4638">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-4639">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4639">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-4640">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4640">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-4641">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4641">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-4642">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4642">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="ba9fe-4643">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4643">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="ba9fe-4644">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4644">Target</span></span> | <span data-ttu-id="ba9fe-4645">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4645">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-4646">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4646">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-4647">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4647">16</span></span> |
| <span data-ttu-id="ba9fe-4648">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4648">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4650">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4650">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4651">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4651">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4652">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4652">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4653">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4653">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4654">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4654">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4656">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4656">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4658">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4658">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4660">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4660">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4662">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4662">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4664">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4664">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4666">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4666">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4667">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4667">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4668">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4668">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-4669">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4669">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-4670">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4670">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4672">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4672">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-4673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4673">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4674">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4674">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4675">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4675">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-4676">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4676">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-4677">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4677">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4678">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4678">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4679">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4679">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-4680">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4680">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-4681">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4681">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4682">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4682">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-4683">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4683">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-4684">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4684">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-4685">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4685">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-4686">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4686">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4687">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4687">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4688">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4688">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4690">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4690">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4691">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4691">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4692">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4692">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-4693">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4693">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-4694">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4694">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4695">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4695">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-4696">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4696">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-4697">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4697">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-4698">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4698">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-4699">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4699">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-4700">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4700">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-4701">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="ba9fe-4702">DXGI_FORMAT_BC1 無別 \_ <sup>PCC</sup> (70) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4702">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="ba9fe-4703">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4703">Target</span></span> | <span data-ttu-id="ba9fe-4704">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4704">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-4705">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-4706">4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4706">4</span></span> |
| <span data-ttu-id="ba9fe-4707">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4707">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4709">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4709">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4710">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4710">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4711">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4711">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4712">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4712">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4713">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4713">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-4714">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4714">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4716">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4716">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4718">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4718">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4720">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4720">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-4721">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4721">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4722">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4722">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4723">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4723">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4724">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4724">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-4725">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4725">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-4726">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4726">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4728">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4728">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-4729">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4729">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4730">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4730">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4731">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4731">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-4732">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4732">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-4733">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4733">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4734">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4734">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4735">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4735">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-4736">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4736">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-4737">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4737">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4738">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4738">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-4739">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4739">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-4740">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4740">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-4741">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4741">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-4742">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4742">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4743">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4743">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4744">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4744">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4746">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4746">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4747">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4747">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4748">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4748">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-4749">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4749">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-4750">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4750">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4751">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-4752">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4752">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4754">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4754">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-4755">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4755">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-4756">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-4757">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4757">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4759">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4759">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfccsup-71"></a><span data-ttu-id="ba9fe-4760">DXGI_FORMAT_BC1 \_ UNORM<sup>FCC</sup> (71) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4760">DXGI_FORMAT_BC1\_UNORM<sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="ba9fe-4761">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4761">Target</span></span> | <span data-ttu-id="ba9fe-4762">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4762">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-4763">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4763">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-4764">4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4764">4</span></span> |
| <span data-ttu-id="ba9fe-4765">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4765">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4767">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4767">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4768">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4768">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4769">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4769">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4770">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4770">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4771">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4771">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-4772">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4772">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4774">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4776">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4776">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4778">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4778">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4780">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4780">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4782">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4782">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4783">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4783">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4784">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4784">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-4785">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4785">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-4786">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4786">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4788">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4788">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-4789">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4789">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4790">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4790">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4791">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4791">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-4792">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4792">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-4793">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4793">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4794">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4794">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4795">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4795">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-4796">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4796">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-4797">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4797">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4798">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4798">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-4799">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4799">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-4800">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4800">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-4801">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4801">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-4802">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4802">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4803">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4803">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4804">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4804">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4806">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4806">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4807">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4807">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4808">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4808">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-4809">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4809">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-4810">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4810">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4811">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4811">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-4812">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4812">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4814">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4814">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-4815">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4815">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-4816">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4816">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-4817">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4817">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4819">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4819">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfccsup-72"></a><span data-ttu-id="ba9fe-4820">DXGI_FORMAT_BC1 \_ UNORM \_ SRGB<sup>FCC</sup> (72) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4820">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="ba9fe-4821">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4821">Target</span></span> | <span data-ttu-id="ba9fe-4822">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4822">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-4823">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4823">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-4824">4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4824">4</span></span> |
| <span data-ttu-id="ba9fe-4825">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4825">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4827">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4827">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4828">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4828">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4829">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4829">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4830">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4830">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4831">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4831">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-4832">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4832">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4834">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4834">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4836">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4836">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4838">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4838">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4840">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4840">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4842">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4842">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4843">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4843">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4844">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4844">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-4845">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4845">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-4846">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4846">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4848">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4848">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-4849">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4849">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4850">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4850">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4851">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4851">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-4852">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4852">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-4853">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4853">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4854">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4854">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4855">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4855">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-4856">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4856">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-4857">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4857">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4858">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4858">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-4859">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4859">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-4860">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4860">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-4861">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4861">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-4862">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4862">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4863">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4863">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4864">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4864">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4866">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4866">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4867">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4867">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4868">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4868">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-4869">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4869">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-4870">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4870">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4871">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4871">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-4872">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4872">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4874">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4874">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-4875">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4875">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-4876">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4876">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-4877">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4877">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4879">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4879">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="ba9fe-4880">DXGI_FORMAT_BC2 無別 \_ <sup>PCC</sup> (73) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4880">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="ba9fe-4881">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4881">Target</span></span> | <span data-ttu-id="ba9fe-4882">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4882">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-4883">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4883">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-4884">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4884">8</span></span> |
| <span data-ttu-id="ba9fe-4885">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4885">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4887">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4887">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4888">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4888">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4889">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4889">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4890">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4890">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4891">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4891">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-4892">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4892">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4894">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4894">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4896">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4896">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4898">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4898">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-4899">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4899">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4900">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4900">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4901">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4901">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4902">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4902">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-4903">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4903">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-4904">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4904">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4906">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4906">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-4907">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4907">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4908">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4908">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4909">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4909">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-4910">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4910">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-4911">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4911">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4912">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4912">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4913">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4913">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-4914">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4914">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-4915">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4915">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4916">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4916">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-4917">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4917">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-4918">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4918">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-4919">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4919">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-4920">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4920">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4921">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4921">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4922">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4922">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4924">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4924">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4925">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4925">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4926">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4926">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-4927">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4927">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-4928">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4928">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4929">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4929">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-4930">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4930">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4932">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4932">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-4933">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4933">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-4934">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4934">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-4935">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4935">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4937">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4937">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfccsup-74"></a><span data-ttu-id="ba9fe-4938">DXGI_FORMAT_BC2 \_ UNORM<sup>FCC</sup> (74) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4938">DXGI_FORMAT_BC2\_UNORM<sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="ba9fe-4939">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4939">Target</span></span> | <span data-ttu-id="ba9fe-4940">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4940">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-4941">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4941">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-4942">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4942">8</span></span> |
| <span data-ttu-id="ba9fe-4943">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4943">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4945">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4945">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4946">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4946">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4947">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4947">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4948">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4948">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-4949">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4949">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-4950">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4950">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4952">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4952">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4954">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4954">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4956">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4956">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4958">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4958">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4960">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4960">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4961">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4961">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-4962">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4962">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-4963">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4963">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-4964">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4964">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4966">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4966">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-4967">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4967">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4968">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4968">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4969">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4969">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-4970">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4970">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-4971">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4971">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4972">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4972">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-4973">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4973">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-4974">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4974">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-4975">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4975">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4976">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4976">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-4977">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4977">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-4978">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4978">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-4979">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4979">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-4980">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4980">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4981">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4981">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-4982">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4982">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4984">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4984">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4985">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4985">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-4986">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4986">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-4987">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4987">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-4988">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4988">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-4989">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4989">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-4990">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4990">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4992">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4992">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-4993">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4993">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-4994">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4994">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-4995">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4995">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-4997">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4997">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfccsup-75"></a><span data-ttu-id="ba9fe-4998">DXGI_FORMAT_BC2 \_ UNORM \_ SRGB<sup>FCC</sup> (75) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-4998">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="ba9fe-4999">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-4999">Target</span></span> | <span data-ttu-id="ba9fe-5000">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5000">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-5001">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5001">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-5002">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5002">8</span></span> |
| <span data-ttu-id="ba9fe-5003">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5003">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5005">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5005">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5006">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5006">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5007">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5007">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5008">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5008">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5009">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5009">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-5010">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5010">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5012">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5012">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5014">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5014">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5016">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5016">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5018">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5018">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5020">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5020">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5021">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5021">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5022">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5022">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-5023">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5023">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-5024">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5024">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5026">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5026">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-5027">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5027">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5028">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5028">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5029">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5029">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-5030">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5030">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-5031">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5031">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5032">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5032">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5033">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5033">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-5034">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5034">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-5035">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5035">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5036">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5036">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-5037">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5037">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-5038">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5038">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-5039">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5039">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-5040">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5040">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5041">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5041">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5042">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5042">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5044">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5044">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5045">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5045">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5046">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5046">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-5047">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5047">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-5048">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5048">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5049">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5049">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-5050">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5050">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5052">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5052">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-5053">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5053">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-5054">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5054">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-5055">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5055">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5057">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5057">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="ba9fe-5058">DXGI_FORMAT_BC3 無別 \_ <sup>PCC</sup> (76) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5058">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="ba9fe-5059">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5059">Target</span></span> | <span data-ttu-id="ba9fe-5060">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5060">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-5061">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5061">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-5062">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5062">8</span></span> |
| <span data-ttu-id="ba9fe-5063">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5063">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5065">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5065">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5066">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5066">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5067">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5067">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5068">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5068">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5069">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5069">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-5070">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5070">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5072">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5072">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5074">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5074">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5076">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5076">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-5077">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5077">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5078">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5078">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5079">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5079">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5080">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5080">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-5081">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5081">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-5082">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5082">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5084">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5084">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-5085">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5085">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5086">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5086">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5087">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-5088">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-5089">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5090">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5091">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5091">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-5092">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5092">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-5093">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5093">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5094">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5094">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-5095">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5095">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-5096">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5096">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-5097">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5097">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-5098">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5098">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5099">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5099">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5100">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5100">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5102">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5102">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5103">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5103">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5104">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5104">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-5105">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5105">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-5106">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5106">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5107">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5107">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-5108">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5108">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5110">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-5111">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-5112">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-5113">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5113">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5115">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5115">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfccsup-77"></a><span data-ttu-id="ba9fe-5116">DXGI_FORMAT_BC3 \_ UNORM<sup>FCC</sup> (77) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5116">DXGI_FORMAT_BC3\_UNORM<sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="ba9fe-5117">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5117">Target</span></span> | <span data-ttu-id="ba9fe-5118">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5118">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-5119">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5119">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-5120">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5120">8</span></span> |
| <span data-ttu-id="ba9fe-5121">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5121">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5123">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5123">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5124">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5124">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5125">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5125">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5126">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5126">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5127">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5127">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-5128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5128">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5130">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5132">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5132">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5134">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5134">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5136">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5136">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5138">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5138">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5139">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5139">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5140">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5140">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-5141">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5141">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-5142">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5142">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5144">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-5145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5145">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5146">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5147">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-5148">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-5149">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5150">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5151">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5151">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-5152">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-5153">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5154">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-5155">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-5156">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-5157">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-5158">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5159">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5160">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5160">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5162">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5163">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5164">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-5165">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-5166">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5166">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5167">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-5168">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5168">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5170">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5170">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-5171">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5171">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-5172">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5172">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-5173">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5173">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5175">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5175">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfccsup-78"></a><span data-ttu-id="ba9fe-5176">DXGI_FORMAT_BC3 \_ UNORM \_ SRGB<sup>FCC</sup> (78) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5176">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="ba9fe-5177">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5177">Target</span></span> | <span data-ttu-id="ba9fe-5178">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5178">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-5179">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5179">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-5180">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5180">8</span></span> |
| <span data-ttu-id="ba9fe-5181">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5181">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5183">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5183">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5184">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5184">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5185">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5185">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5186">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5186">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5187">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5187">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-5188">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5188">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5190">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5190">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5192">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5192">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5194">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5194">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5196">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5196">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5198">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5198">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5199">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5199">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5200">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5200">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-5201">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5201">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-5202">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5202">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5204">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5204">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-5205">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5205">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5206">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5206">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5207">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5207">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-5208">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5208">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-5209">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5209">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5210">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5210">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5211">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5211">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-5212">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5212">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-5213">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5213">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5214">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5214">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-5215">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5215">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-5216">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5216">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-5217">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5217">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-5218">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5218">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5219">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5219">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5220">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5220">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5222">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5223">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5224">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-5225">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-5226">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5226">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5227">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-5228">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5228">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5230">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5230">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-5231">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5231">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-5232">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5232">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-5233">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5233">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5235">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5235">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="ba9fe-5236">DXGI_FORMAT_BC4 無別 \_ <sup>PCC</sup> (79) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5236">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="ba9fe-5237">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5237">Target</span></span> | <span data-ttu-id="ba9fe-5238">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5238">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-5239">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5239">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-5240">4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5240">4</span></span> |
| <span data-ttu-id="ba9fe-5241">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5241">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5243">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5243">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5244">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5244">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5245">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5245">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5246">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5246">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5247">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-5248">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5248">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5250">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5250">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5252">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5254">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5254">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-5255">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5255">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5256">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5256">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5257">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5257">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5258">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5258">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-5259">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5259">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-5260">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5260">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5262">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5262">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-5263">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5263">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5264">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5264">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5265">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5265">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-5266">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5266">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-5267">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5267">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5268">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5268">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5269">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5269">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-5270">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5270">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-5271">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5271">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5272">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5272">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-5273">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5273">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-5274">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5274">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-5275">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5275">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-5276">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5276">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5277">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5277">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5278">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5278">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5280">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5280">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5281">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5281">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5282">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5282">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-5283">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5283">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-5284">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5284">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5285">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5285">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-5286">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5286">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5288">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5288">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-5289">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5289">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-5290">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5290">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-5291">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5291">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-5292">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5292">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfccsup-80"></a><span data-ttu-id="ba9fe-5293">DXGI_FORMAT_BC4 \_ UNORM<sup>FCC</sup> (80) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5293">DXGI_FORMAT_BC4\_UNORM<sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="ba9fe-5294">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5294">Target</span></span> | <span data-ttu-id="ba9fe-5295">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5295">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-5296">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5296">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-5297">4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5297">4</span></span> |
| <span data-ttu-id="ba9fe-5298">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5298">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5300">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5300">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5301">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5301">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5302">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5302">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5303">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5303">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5304">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5304">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-5305">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5305">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5307">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5307">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5309">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5309">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5311">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5311">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5313">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5313">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5315">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5315">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5316">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5316">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5317">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5317">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-5318">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5318">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-5319">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5319">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5321">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5321">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-5322">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5322">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5323">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5323">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5324">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5324">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-5325">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5325">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-5326">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5326">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5327">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5327">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5328">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5328">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-5329">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5329">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-5330">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5330">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5331">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5331">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-5332">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5332">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-5333">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5333">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-5334">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5334">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-5335">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5335">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5336">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5336">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5337">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5337">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5339">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5339">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5340">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5340">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5341">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5341">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-5342">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5342">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-5343">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5343">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5344">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5344">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-5345">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5345">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5347">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5347">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-5348">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5348">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-5349">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5349">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-5350">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5350">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-5351">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5351">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfccsup-81"></a><span data-ttu-id="ba9fe-5352">DXGI_FORMAT_BC4 \_ SNORM<sup>FCC</sup> (81) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5352">DXGI_FORMAT_BC4\_SNORM<sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="ba9fe-5353">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5353">Target</span></span> | <span data-ttu-id="ba9fe-5354">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5354">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-5355">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5355">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-5356">4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5356">4</span></span> |
| <span data-ttu-id="ba9fe-5357">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5357">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5359">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5359">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5360">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5360">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5361">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5361">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5362">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5362">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5363">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5363">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-5364">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5364">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5366">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5366">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5368">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5368">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5370">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5370">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5372">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5372">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5374">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5374">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5375">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5375">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5376">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5376">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-5377">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5377">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-5378">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5378">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5380">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5380">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-5381">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5381">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5382">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5382">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5383">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5383">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-5384">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5384">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-5385">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5385">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5386">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5386">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5387">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5387">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-5388">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5388">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-5389">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5389">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5390">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5390">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-5391">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5391">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-5392">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5392">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-5393">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5393">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-5394">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5394">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5395">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5395">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5396">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5396">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5398">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5398">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5399">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5399">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5400">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5400">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-5401">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5401">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-5402">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5402">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5403">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5403">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-5404">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5404">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5406">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5406">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-5407">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5407">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-5408">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5408">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-5409">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5409">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-5410">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5410">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="ba9fe-5411">DXGI_FORMAT_BC5 無別 \_ <sup>PCC</sup> (82) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5411">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="ba9fe-5412">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5412">Target</span></span> | <span data-ttu-id="ba9fe-5413">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5413">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-5414">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5414">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-5415">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5415">8</span></span> |
| <span data-ttu-id="ba9fe-5416">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5416">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5418">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5418">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5419">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5419">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5420">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5420">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5421">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5421">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5422">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5422">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-5423">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5423">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5425">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5425">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5427">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5427">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5429">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5429">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-5430">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5430">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5431">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5431">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5432">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5432">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5433">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5433">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-5434">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5434">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-5435">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5435">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5437">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5437">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-5438">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5438">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5439">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5439">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5440">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5440">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-5441">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5441">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-5442">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5442">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5443">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5443">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5444">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5444">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-5445">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5445">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-5446">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5446">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5447">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5447">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-5448">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5448">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-5449">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5449">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-5450">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5450">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-5451">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5451">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5452">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5452">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5453">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5453">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5455">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5455">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5456">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5456">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5457">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5457">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-5458">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5458">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-5459">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5459">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5460">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5460">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-5461">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5461">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5463">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5463">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-5464">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5464">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-5465">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5465">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-5466">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5466">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-5467">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5467">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfccsup-83"></a><span data-ttu-id="ba9fe-5468">DXGI_FORMAT_BC5 \_ UNORM<sup>FCC</sup> (83) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5468">DXGI_FORMAT_BC5\_UNORM<sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="ba9fe-5469">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5469">Target</span></span> | <span data-ttu-id="ba9fe-5470">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5470">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-5471">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5471">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-5472">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5472">8</span></span> |
| <span data-ttu-id="ba9fe-5473">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5473">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5475">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5475">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5476">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5476">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5477">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5477">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5478">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5478">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5479">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5479">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-5480">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5480">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5482">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5482">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5484">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5484">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5486">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5486">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5488">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5488">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5490">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5490">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5491">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5491">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5492">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5492">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-5493">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5493">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-5494">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5494">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5496">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5496">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-5497">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5497">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5498">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5498">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5499">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5499">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-5500">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5500">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-5501">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5501">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5502">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5502">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5503">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5503">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-5504">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5504">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-5505">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5505">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5506">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5506">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-5507">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5507">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-5508">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5508">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-5509">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5509">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-5510">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5510">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5511">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5511">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5512">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5512">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5514">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5514">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5515">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5515">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5516">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5516">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-5517">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5517">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-5518">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5518">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5519">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5519">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-5520">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5520">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5522">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5522">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-5523">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5523">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-5524">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5524">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-5525">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5525">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-5526">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5526">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfccsup-84"></a><span data-ttu-id="ba9fe-5527">DXGI_FORMAT_BC5 \_ SNORM<sup>FCC</sup> (84) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5527">DXGI_FORMAT_BC5\_SNORM<sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="ba9fe-5528">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5528">Target</span></span> | <span data-ttu-id="ba9fe-5529">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5529">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-5530">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5530">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-5531">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5531">8</span></span> |
| <span data-ttu-id="ba9fe-5532">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5532">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5534">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5534">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5535">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5535">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5536">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5536">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5537">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5537">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5538">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5538">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-5539">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5539">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5541">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5541">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5543">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5543">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5545">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5545">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5547">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5547">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5549">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5549">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5550">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5550">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5551">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5551">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-5552">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5552">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-5553">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5553">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5555">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5555">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-5556">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5556">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5557">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5557">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5558">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5558">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-5559">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5559">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-5560">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5560">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5561">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5561">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5562">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5562">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-5563">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5563">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-5564">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5564">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5565">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5565">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-5566">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5566">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-5567">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5567">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-5568">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5568">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-5569">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5569">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5570">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5570">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5571">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5571">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5573">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5573">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5574">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5574">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5575">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5575">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-5576">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5576">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-5577">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5577">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5578">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5578">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-5579">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5579">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5581">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5581">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-5582">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5582">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-5583">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5583">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-5584">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5584">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-5585">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5585">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="ba9fe-5586">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5586">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="ba9fe-5587">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5587">Target</span></span> | <span data-ttu-id="ba9fe-5588">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5588">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-5589">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5589">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-5590">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5590">16</span></span> |
| <span data-ttu-id="ba9fe-5591">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5591">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5593">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5593">Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5595">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5595">Input Assembler Vertex Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5597">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5597">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5598">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5598">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5599">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5599">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5601">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5601">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5603">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5603">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5605">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5607">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5607">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5609">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5609">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5611">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5611">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5612">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5612">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5613">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5613">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-5614">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5614">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-5615">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5615">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5617">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5617">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5619">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5621">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5621">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5623">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5623">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-5624">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5624">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-5625">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5625">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5626">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5626">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5627">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5627">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-5628">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5628">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-5629">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5629">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5630">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5630">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-5631">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5631">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-5632">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5632">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-5633">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5633">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-5634">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5634">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5635">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5635">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5636">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5636">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5638">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5638">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5640">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5640">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5642">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5642">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5644">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5644">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5646">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5646">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5648">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5648">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-5649">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5649">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-5650">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5650">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-5651">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5651">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-5652">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5652">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-5653">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5653">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-5654">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5654">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="ba9fe-5655">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5655">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="ba9fe-5656">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5656">Target</span></span> | <span data-ttu-id="ba9fe-5657">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5657">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-5658">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5658">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-5659">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5659">16</span></span> |
| <span data-ttu-id="ba9fe-5660">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5660">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5662">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5662">Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5664">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5664">Input Assembler Vertex Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5666">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5666">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5667">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5667">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5668">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5668">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5670">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5670">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5672">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5672">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5674">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5674">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5676">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5676">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5678">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5678">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5680">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5680">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5681">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5681">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5682">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5682">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-5683">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5683">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-5684">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5684">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5686">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5686">Mipmap Auto-Generation</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5688">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5688">RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5690">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5690">Blendable RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5692">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5692">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-5693">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5693">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-5694">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5694">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5695">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5695">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5696">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5696">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-5697">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5697">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-5698">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5698">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5699">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5699">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-5700">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5700">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-5701">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5701">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-5702">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5702">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-5703">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5703">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5704">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5704">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5705">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5705">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5707">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5707">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5709">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5709">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5711">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5711">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5713">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5713">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5715">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5715">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5717">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5717">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-5718">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5718">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-5719">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5719">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-5720">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5720">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-5721">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5721">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-5722">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5722">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-5723">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5723">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="ba9fe-5724">DXGI_FORMAT_B8G8R8A8 無的 \_ <sup>電腦</sup> (90) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5724">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="ba9fe-5725">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5725">Target</span></span> | <span data-ttu-id="ba9fe-5726">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5726">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-5727">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5727">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-5728">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5728">32</span></span> |
| <span data-ttu-id="ba9fe-5729">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5729">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5731">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5731">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5732">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5732">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5733">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5733">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5734">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5734">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5735">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5735">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5737">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5737">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5739">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5739">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5741">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5741">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5743">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5743">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-5744">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5744">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5745">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5745">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5746">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5746">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5747">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5747">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-5748">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5748">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-5749">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5749">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5751">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5751">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-5752">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5752">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5753">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5753">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5754">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5754">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-5755">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5755">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-5756">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5756">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5757">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5757">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5758">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5758">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-5759">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5759">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-5760">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5760">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5761">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5761">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-5762">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5762">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-5763">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5763">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-5764">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5764">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-5765">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5765">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5766">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5766">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5767">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5767">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5769">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5769">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5770">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5770">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5771">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5771">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-5772">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5772">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-5773">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5773">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5774">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5774">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-5775">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5775">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5777">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5777">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-5778">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5778">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-5779">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5779">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-5780">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5780">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5782">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="ba9fe-5783">DXGI_FORMAT_B8G8R8A8 \_ UNORM 的<sup>FCS</sup> (87) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5783">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="ba9fe-5784">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5784">Target</span></span> | <span data-ttu-id="ba9fe-5785">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5785">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-5786">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-5787">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5787">32</span></span> |
| <span data-ttu-id="ba9fe-5788">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5788">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5790">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5790">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5792">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5792">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5794">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5794">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5795">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5795">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5796">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5796">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5798">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5798">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5800">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5800">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5802">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5802">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5804">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5804">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5806">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5806">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5808">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5808">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5809">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5809">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5810">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5810">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-5811">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5811">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-5812">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5812">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5814">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5814">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5816">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5816">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5818">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5818">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5820">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5820">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-5821">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5821">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-5822">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5822">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5823">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5823">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5824">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5824">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-5825">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5825">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-5826">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5826">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5827">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5827">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-5828">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5828">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-5829">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5829">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-5830">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5830">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-5831">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5831">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5832">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5832">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5833">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5833">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5835">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5835">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5837">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5837">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5839">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5839">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5841">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5841">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5843">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5843">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5845">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5845">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5847">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5847">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5849">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5849">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-5850">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5850">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5852">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5852">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5854">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5854">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5856">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5856">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="ba9fe-5857">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ SRGB<sup>FCS</sup> (91) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5857">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="ba9fe-5858">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5858">Target</span></span> | <span data-ttu-id="ba9fe-5859">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5859">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-5860">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5860">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-5861">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5861">32</span></span> |
| <span data-ttu-id="ba9fe-5862">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5862">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5864">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5864">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5865">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5865">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5866">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5866">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5867">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5867">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5868">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5868">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5870">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5870">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5872">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5872">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5874">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5874">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5876">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5876">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5878">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5878">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5880">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5880">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5881">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5881">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5882">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5882">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-5883">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5883">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-5884">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5884">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5886">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5886">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5888">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5888">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5890">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5890">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5892">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-5893">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-5894">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5895">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5896">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5896">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-5897">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-5898">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5899">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-5900">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-5901">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5901">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-5902">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-5903">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5904">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5905">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5905">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5907">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5907">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5909">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5909">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5911">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5911">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5913">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5913">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5915">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5915">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5917">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5917">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5919">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5919">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5921">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5921">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-5922">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5922">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5924">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5924">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-5926">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5926">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5928">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="ba9fe-5929">DXGI_FORMAT_B8G8R8X8 無的 \_ <sup>電腦</sup> (92) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5929">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="ba9fe-5930">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5930">Target</span></span> | <span data-ttu-id="ba9fe-5931">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5931">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-5932">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-5933">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5933">32</span></span> |
| <span data-ttu-id="ba9fe-5934">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5934">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5936">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5936">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5937">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5937">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5938">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5938">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5939">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5939">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-5940">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5940">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5942">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5942">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5944">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5944">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5946">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5946">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5948">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5948">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-5949">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5949">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5950">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5950">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5951">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5951">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-5952">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5952">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-5953">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5953">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-5954">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5954">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5956">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5956">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-5957">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5957">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5958">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5958">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5959">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5959">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-5960">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5960">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-5961">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5961">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5962">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5962">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-5963">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5963">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-5964">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5964">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-5965">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5965">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5966">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5966">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-5967">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5967">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-5968">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5968">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-5969">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5969">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-5970">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5970">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5971">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5971">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-5972">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5972">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5974">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5974">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5975">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5975">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-5976">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5976">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-5977">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5977">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-5978">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5978">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-5979">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5979">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-5980">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5980">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5982">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5982">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-5983">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5983">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-5984">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5984">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-5985">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5985">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5987">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5987">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="ba9fe-5988">DXGI_FORMAT_B8G8R8X8 \_ UNORM 的<sup>FCS</sup> (88) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5988">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="ba9fe-5989">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5989">Target</span></span> | <span data-ttu-id="ba9fe-5990">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5990">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-5991">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-5991">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-5992">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5992">32</span></span> |
| <span data-ttu-id="ba9fe-5993">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5993">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5995">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5995">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5997">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5997">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-5999">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-5999">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6000">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6000">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6001">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6001">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6003">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6003">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6005">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6005">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6007">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6007">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6009">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6009">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6011">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6011">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6013">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6013">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6014">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6014">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6015">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6015">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-6016">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6016">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-6017">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6017">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6019">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6019">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6021">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6021">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6023">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6023">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6025">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6025">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-6026">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6026">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-6027">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6027">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6028">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6028">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6029">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6029">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-6030">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6030">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-6031">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6031">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6032">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6032">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-6033">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6033">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-6034">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6034">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-6035">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6035">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-6036">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6036">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6037">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6037">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6038">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6038">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6040">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6040">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6042">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6042">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6044">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6044">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6046">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6046">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6048">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6048">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6050">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6050">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-6051">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6051">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6053">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6053">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-6054">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6054">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6056">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6056">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6058">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6058">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6060">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6060">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="ba9fe-6061">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ SRGB<sup>FCS</sup> (93) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6061">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="ba9fe-6062">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6062">Target</span></span> | <span data-ttu-id="ba9fe-6063">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6063">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-6064">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6064">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-6065">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6065">32</span></span> |
| <span data-ttu-id="ba9fe-6066">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6066">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6068">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6068">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6069">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6069">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6070">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6070">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6071">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6071">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6072">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6072">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6074">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6074">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6076">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6076">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6078">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6078">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6080">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6080">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6082">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6082">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6084">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6084">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6085">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6085">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6086">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6086">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-6087">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6087">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-6088">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6088">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6090">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6090">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6092">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6092">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6094">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6094">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6096">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6096">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-6097">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6097">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-6098">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6098">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6099">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6099">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6100">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6100">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-6101">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6101">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-6102">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6102">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6103">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6103">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-6104">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6104">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-6105">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6105">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-6106">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6106">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-6107">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6107">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6108">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6108">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6109">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6109">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6111">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6111">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6113">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6113">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6115">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6115">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6117">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6117">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6119">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6119">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6121">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6121">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-6122">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6122">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6124">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6124">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-6125">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6125">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-6126">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6126">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-6127">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6127">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6129">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6129">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="ba9fe-6130">DXGI_FORMAT_AYUV<sup>V</sup> (100) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6130">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="ba9fe-6131">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6131">Target</span></span> | <span data-ttu-id="ba9fe-6132">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6132">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-6133">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6133">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-6134">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6134">32</span></span> |
| <span data-ttu-id="ba9fe-6135">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6135">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6137">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6137">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6138">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6138">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6139">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6139">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6140">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6140">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6141">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6141">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-6142">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6142">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6144">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6144">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-6145">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6145">TextureCube</span></span> | \- |
| <span data-ttu-id="ba9fe-6146">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6146">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6148">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6148">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6150">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6150">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6151">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6151">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6152">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6152">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-6153">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6153">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-6154">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6154">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6156">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6156">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6158">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6158">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6160">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6160">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6162">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6162">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-6163">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6163">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-6164">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6164">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6165">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6165">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6166">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6166">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-6167">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6167">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-6168">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6168">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6169">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6169">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-6170">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6170">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-6171">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6171">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-6172">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6172">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-6173">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6173">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6174">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6174">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6175">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6175">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6177">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6177">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6178">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6178">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6179">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6179">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-6180">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6180">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-6181">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6181">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6182">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6182">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-6183">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6183">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-6184">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6184">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6186">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6186">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6188">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6188">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6190">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6190">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6192">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6192">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="ba9fe-6193">DXGI_FORMAT_Y410<sup>V</sup> (101) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6193">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="ba9fe-6194">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6194">Target</span></span> | <span data-ttu-id="ba9fe-6195">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6195">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-6196">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6196">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-6197">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6197">32</span></span> |
| <span data-ttu-id="ba9fe-6198">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6198">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6200">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6200">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6201">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6201">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6202">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6202">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6203">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6203">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6204">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6204">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-6205">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6205">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6207">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6207">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-6208">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6208">TextureCube</span></span> | \- |
| <span data-ttu-id="ba9fe-6209">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6209">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6211">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6211">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6213">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6213">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6214">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6214">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6215">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6215">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-6216">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6216">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-6217">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6217">Mipmap</span></span> | \- |
| <span data-ttu-id="ba9fe-6218">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6218">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-6219">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6219">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6220">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6220">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6221">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6221">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-6222">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6222">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-6223">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6223">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6224">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6224">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6225">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6225">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-6226">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6226">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-6227">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6227">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6228">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6228">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-6229">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6229">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-6230">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6230">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-6231">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6231">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-6232">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6232">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6233">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6233">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6234">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6234">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6236">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6236">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6237">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6237">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6238">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6238">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-6239">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6239">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-6240">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6240">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6241">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6241">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-6242">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6242">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-6243">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6243">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6245">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6245">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6247">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6247">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6249">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6249">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6251">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6251">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="ba9fe-6252">DXGI_FORMAT_Y416<sup>V</sup> (102) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6252">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="ba9fe-6253">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6253">Target</span></span> | <span data-ttu-id="ba9fe-6254">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6254">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-6255">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6255">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-6256">64</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6256">64</span></span> |
| <span data-ttu-id="ba9fe-6257">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6257">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6259">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6259">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6260">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6260">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6261">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6261">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6262">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6262">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6263">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6263">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-6264">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6264">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6266">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6266">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-6267">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6267">TextureCube</span></span> | \- |
| <span data-ttu-id="ba9fe-6268">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6268">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6270">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6270">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6272">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6272">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6273">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6273">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6274">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6274">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-6275">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6275">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-6276">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6276">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6278">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6278">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-6279">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6279">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6280">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6280">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6281">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6281">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-6282">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-6283">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6284">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6285">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6285">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-6286">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-6287">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6288">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-6289">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-6290">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6290">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-6291">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-6292">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6293">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6294">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6294">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6296">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6296">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6297">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6297">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6298">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6298">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-6299">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6299">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-6300">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6300">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6301">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6301">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-6302">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6302">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-6303">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6303">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6305">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6305">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6307">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6307">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6309">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6309">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6311">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6311">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="ba9fe-6312">DXGI_FORMAT_NV12<sup>V</sup> (103) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6312">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="ba9fe-6313">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6313">Target</span></span> | <span data-ttu-id="ba9fe-6314">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6314">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-6315">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6315">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-6316">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6316">8</span></span> |
| <span data-ttu-id="ba9fe-6317">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6317">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6319">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6319">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6320">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6320">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6321">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6321">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6322">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6322">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6323">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6323">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-6324">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6324">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6326">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6326">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-6327">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6327">TextureCube</span></span> | \- |
| <span data-ttu-id="ba9fe-6328">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6328">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6330">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6330">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6332">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6332">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6333">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6333">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6334">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6334">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-6335">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6335">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-6336">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6336">Mipmap</span></span> | \- |
| <span data-ttu-id="ba9fe-6337">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6337">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-6338">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6338">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6340">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6340">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6342">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-6343">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-6344">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6345">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6346">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6346">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-6347">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-6348">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6349">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-6350">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-6351">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6351">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-6352">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-6353">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6354">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6355">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6355">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6357">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6358">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6359">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-6360">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-6361">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6361">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6362">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-6363">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6363">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-6364">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6364">Video Decoder Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6366">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6366">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6368">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6368">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6370">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6370">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6372">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6372">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="ba9fe-6373">DXGI_FORMAT_P010<sup>V</sup> (104) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6373">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="ba9fe-6374">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6374">Target</span></span> | <span data-ttu-id="ba9fe-6375">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6375">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-6376">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6376">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-6377">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6377">16</span></span> |
| <span data-ttu-id="ba9fe-6378">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6378">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6380">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6380">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6381">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6381">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6382">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6382">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6383">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6383">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6384">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6384">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-6385">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6385">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6387">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6387">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-6388">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6388">TextureCube</span></span> | \- |
| <span data-ttu-id="ba9fe-6389">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6389">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6391">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6391">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6393">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6393">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6394">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6394">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6395">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6395">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-6396">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6396">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-6397">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6397">Mipmap</span></span> | \- |
| <span data-ttu-id="ba9fe-6398">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6398">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-6399">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6399">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6401">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6401">Blendable RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6403">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6403">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-6404">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6404">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-6405">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6405">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6406">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6406">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6407">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6407">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-6408">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6408">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-6409">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6409">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6410">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6410">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-6411">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6411">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-6412">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6412">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-6413">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6413">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-6414">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6414">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6415">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6415">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6416">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6416">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6418">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6418">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6419">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6419">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6420">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6420">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-6421">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6421">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-6422">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6422">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6423">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6423">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-6424">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6424">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-6425">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6425">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6427">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6427">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6429">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6429">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6431">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6431">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6433">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6433">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="ba9fe-6434">DXGI_FORMAT_P016<sup>V</sup> (105) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6434">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="ba9fe-6435">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6435">Target</span></span> | <span data-ttu-id="ba9fe-6436">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6436">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-6437">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6437">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-6438">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6438">16</span></span> |
| <span data-ttu-id="ba9fe-6439">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6439">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6441">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6441">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6442">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6442">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6443">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6443">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6444">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6444">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6445">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6445">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-6446">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6446">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6448">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6448">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-6449">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6449">TextureCube</span></span> | \- |
| <span data-ttu-id="ba9fe-6450">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6450">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6452">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6452">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6454">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6454">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6455">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6455">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6456">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6456">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-6457">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6457">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-6458">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6458">Mipmap</span></span> | \- |
| <span data-ttu-id="ba9fe-6459">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6459">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-6460">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6460">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6462">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6462">Blendable RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6464">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-6465">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-6466">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6467">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6468">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6468">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-6469">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-6470">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6471">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-6472">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-6473">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6473">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-6474">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-6475">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6476">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6477">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6477">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6479">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6479">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6480">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6480">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6481">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6481">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-6482">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6482">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-6483">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6483">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6484">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6484">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-6485">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6485">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-6486">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6486">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6488">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6488">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6490">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6490">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6492">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6492">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6494">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6494">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="ba9fe-6495">DXGI_FORMAT_420 不 \_ 透明的<sup>V</sup> (106) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6495">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="ba9fe-6496">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6496">Target</span></span> | <span data-ttu-id="ba9fe-6497">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6497">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-6498">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6498">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-6499">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6499">8</span></span> |
| <span data-ttu-id="ba9fe-6500">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6500">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6502">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6502">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6503">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6503">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6504">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6504">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6505">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6505">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6506">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6506">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-6507">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6507">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6509">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6509">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-6510">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6510">TextureCube</span></span> | \- |
| <span data-ttu-id="ba9fe-6511">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6511">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-6512">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6512">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6513">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6513">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6514">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6514">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6515">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6515">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-6516">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6516">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-6517">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6517">Mipmap</span></span> | \- |
| <span data-ttu-id="ba9fe-6518">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6518">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-6519">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6519">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6520">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6520">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6521">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6521">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-6522">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6522">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-6523">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6523">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6524">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6524">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6525">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6525">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-6526">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6526">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-6527">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6527">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6528">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6528">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-6529">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6529">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-6530">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6530">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-6531">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6531">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-6532">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6532">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6533">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6533">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6534">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6534">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ba9fe-6535">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6535">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6536">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6536">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6537">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6537">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-6538">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6538">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-6539">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6539">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6540">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6540">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-6541">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6541">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-6542">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6542">Video Decoder Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6544">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6544">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6546">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6546">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6548">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6548">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6550">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6550">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="ba9fe-6551">DXGI_FORMAT_YUY2<sup>V</sup> (107) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6551">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="ba9fe-6552">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6552">Target</span></span> | <span data-ttu-id="ba9fe-6553">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6553">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-6554">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6554">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-6555">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6555">16</span></span> |
| <span data-ttu-id="ba9fe-6556">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6556">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6558">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6558">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6559">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6559">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6560">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6560">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6561">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6561">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6562">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6562">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-6563">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6563">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6565">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6565">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-6566">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6566">TextureCube</span></span> | \- |
| <span data-ttu-id="ba9fe-6567">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6567">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6569">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6569">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6571">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6571">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6572">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6572">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6573">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6573">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-6574">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6574">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-6575">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6575">Mipmap</span></span> | \- |
| <span data-ttu-id="ba9fe-6576">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6576">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-6577">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6577">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6578">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6578">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6579">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6579">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-6580">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6580">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-6581">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6581">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6582">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6582">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6583">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6583">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-6584">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6584">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-6585">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6585">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6586">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6586">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-6587">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6587">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-6588">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6588">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-6589">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6589">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-6590">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6590">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6591">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6591">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6592">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6592">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6594">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6594">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6595">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6595">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6596">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6596">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-6597">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6597">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-6598">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6598">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6599">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6599">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-6600">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6600">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-6601">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6601">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6603">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6603">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6605">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6605">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6607">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6607">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6609">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6609">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="ba9fe-6610">DXGI_FORMAT_Y210<sup>V</sup> (108) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6610">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="ba9fe-6611">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6611">Target</span></span> | <span data-ttu-id="ba9fe-6612">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6612">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-6613">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6613">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-6614">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6614">32</span></span> |
| <span data-ttu-id="ba9fe-6615">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6615">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6617">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6617">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6618">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6618">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6619">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6619">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6620">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6620">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6621">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6621">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-6622">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6622">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6624">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6624">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-6625">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6625">TextureCube</span></span> | \- |
| <span data-ttu-id="ba9fe-6626">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6626">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6628">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6628">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6630">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6630">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6631">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6631">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6632">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6632">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-6633">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6633">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-6634">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6634">Mipmap</span></span> | \- |
| <span data-ttu-id="ba9fe-6635">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6635">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-6636">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6636">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6637">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6637">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6638">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6638">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-6639">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6639">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-6640">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6640">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6641">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6641">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6642">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6642">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-6643">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6643">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-6644">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6644">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6645">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6645">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-6646">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6646">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-6647">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6647">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-6648">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6648">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-6649">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6649">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6650">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6650">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6651">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6651">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6653">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6653">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6654">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6654">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6655">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6655">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-6656">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6656">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-6657">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6657">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6658">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6658">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-6659">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6659">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-6660">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6660">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6662">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6662">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6664">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6664">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6666">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6666">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6668">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6668">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="ba9fe-6669">DXGI_FORMAT_Y216<sup>V</sup> (109) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6669">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="ba9fe-6670">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6670">Target</span></span> | <span data-ttu-id="ba9fe-6671">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6671">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-6672">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6672">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-6673">32</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6673">32</span></span> |
| <span data-ttu-id="ba9fe-6674">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6674">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6676">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6676">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6677">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6677">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6678">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6678">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6679">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6679">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6680">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6680">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-6681">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6681">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6683">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6683">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-6684">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6684">TextureCube</span></span> | \- |
| <span data-ttu-id="ba9fe-6685">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6685">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6687">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6687">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6689">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6689">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6690">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6690">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6691">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6691">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-6692">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6692">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-6693">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6693">Mipmap</span></span> | \- |
| <span data-ttu-id="ba9fe-6694">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6694">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-6695">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6695">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6696">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6696">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6697">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6697">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-6698">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6698">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-6699">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6699">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6700">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6700">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6701">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6701">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-6702">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6702">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-6703">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6703">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6704">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6704">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-6705">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6705">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-6706">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6706">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-6707">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6707">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-6708">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6708">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6709">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6709">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6710">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6710">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6712">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6712">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6713">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6713">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6714">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6714">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-6715">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6715">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-6716">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6716">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6717">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6717">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-6718">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6718">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-6719">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6719">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6721">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6721">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6723">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6723">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6725">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6725">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6727">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6727">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="ba9fe-6728">DXGI_FORMAT_NV11<sup>V</sup> (110) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6728">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="ba9fe-6729">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6729">Target</span></span> | <span data-ttu-id="ba9fe-6730">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6730">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-6731">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6731">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-6732">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6732">8</span></span> |
| <span data-ttu-id="ba9fe-6733">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6733">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6735">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6735">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6736">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6736">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6737">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6737">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6738">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6738">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6739">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6739">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-6740">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6740">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6742">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6742">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-6743">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6743">TextureCube</span></span> | \- |
| <span data-ttu-id="ba9fe-6744">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6744">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6746">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6746">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6748">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6748">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6749">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6749">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6750">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6750">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-6751">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6751">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-6752">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6752">Mipmap</span></span> | \- |
| <span data-ttu-id="ba9fe-6753">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6753">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-6754">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6754">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6756">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6756">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6758">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6758">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-6759">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6759">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-6760">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6760">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6761">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6761">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6762">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6762">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-6763">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6763">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-6764">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6764">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6765">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6765">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-6766">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6766">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-6767">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6767">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-6768">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6768">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-6769">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6769">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6770">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6770">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6771">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6771">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6773">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6773">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6774">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6774">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6775">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6775">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-6776">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6776">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-6777">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6777">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6778">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6778">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-6779">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6779">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-6780">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6780">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6782">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6782">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6784">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6784">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6786">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6786">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6788">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6788">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="ba9fe-6789">DXGI_FORMAT_AI44<sup>V</sup> (111) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6789">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="ba9fe-6790">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6790">Target</span></span> | <span data-ttu-id="ba9fe-6791">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6791">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-6792">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6792">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-6793">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6793">8</span></span> |
| <span data-ttu-id="ba9fe-6794">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6794">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6796">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6796">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6797">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6797">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6798">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6798">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6799">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6799">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6800">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6800">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-6801">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6801">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6803">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6803">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-6804">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6804">TextureCube</span></span> | \- |
| <span data-ttu-id="ba9fe-6805">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6805">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-6806">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6806">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6807">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6807">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6808">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6808">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6809">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6809">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-6810">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6810">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-6811">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6811">Mipmap</span></span> | \- |
| <span data-ttu-id="ba9fe-6812">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6812">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-6813">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6813">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6814">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6814">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6815">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6815">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-6816">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6816">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-6817">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6817">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6818">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6818">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6819">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6819">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-6820">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6820">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-6821">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6821">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6822">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6822">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-6823">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6823">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-6824">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6824">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-6825">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6825">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-6826">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6826">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6827">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6827">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6828">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6828">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6830">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6830">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6831">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6831">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6832">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6832">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-6833">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6833">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-6834">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6834">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6835">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6835">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-6836">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6836">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-6837">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6837">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-6838">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6838">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6840">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6840">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-6841">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6841">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-6842">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6842">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="ba9fe-6843">DXGI_FORMAT_IA44<sup>V</sup> (112) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6843">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="ba9fe-6844">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6844">Target</span></span> | <span data-ttu-id="ba9fe-6845">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6845">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-6846">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6846">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-6847">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6847">8</span></span> |
| <span data-ttu-id="ba9fe-6848">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6848">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6850">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6850">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6851">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6851">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6852">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6852">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6853">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6853">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6854">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6854">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-6855">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6855">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6857">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6857">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-6858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6858">TextureCube</span></span> | \- |
| <span data-ttu-id="ba9fe-6859">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6859">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-6860">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6860">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6861">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6861">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6862">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6862">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6863">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6863">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-6864">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6864">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-6865">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6865">Mipmap</span></span> | \- |
| <span data-ttu-id="ba9fe-6866">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6866">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-6867">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6867">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6868">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6868">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6869">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6869">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-6870">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6870">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-6871">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6871">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6872">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6872">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6873">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6873">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-6874">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6874">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-6875">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6875">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6876">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6876">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-6877">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6877">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-6878">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6878">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-6879">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6879">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-6880">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6880">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6881">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6881">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6882">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6882">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6884">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6884">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6885">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6885">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6886">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6886">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-6887">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6887">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-6888">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6888">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6889">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6889">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-6890">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6890">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-6891">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6891">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-6892">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6892">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6894">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6894">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-6895">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6895">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-6896">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6896">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="ba9fe-6897">DXGI_FORMAT_P8<sup>V</sup> (113) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6897">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="ba9fe-6898">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6898">Target</span></span> | <span data-ttu-id="ba9fe-6899">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6899">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-6900">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6900">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-6901">8</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6901">8</span></span> |
| <span data-ttu-id="ba9fe-6902">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6902">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6904">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6904">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6905">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6905">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6906">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6906">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6907">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6907">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6908">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6908">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-6909">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6909">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6911">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6911">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-6912">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6912">TextureCube</span></span> | \- |
| <span data-ttu-id="ba9fe-6913">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6913">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-6914">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6914">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6915">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6915">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6916">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6916">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6917">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6917">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-6918">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6918">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-6919">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6919">Mipmap</span></span> | \- |
| <span data-ttu-id="ba9fe-6920">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6920">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-6921">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6921">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6922">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6922">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6923">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6923">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-6924">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6924">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-6925">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6925">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6926">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6926">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6927">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6927">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-6928">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6928">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-6929">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6929">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6930">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6930">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-6931">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6931">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-6932">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6932">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-6933">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6933">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-6934">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6934">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6935">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6935">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6936">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6936">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6938">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6938">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6939">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6939">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6940">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6940">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-6941">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6941">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-6942">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6942">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6943">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6943">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-6944">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6944">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-6945">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6945">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-6946">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6946">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6948">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6948">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-6949">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6949">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-6950">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6950">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="ba9fe-6951">DXGI_FORMAT_A8P8<sup>V</sup> (114) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6951">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="ba9fe-6952">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6952">Target</span></span> | <span data-ttu-id="ba9fe-6953">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6953">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-6954">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6954">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-6955">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6955">16</span></span> |
| <span data-ttu-id="ba9fe-6956">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6956">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-6958">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6958">Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6959">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6959">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6960">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6960">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6961">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6961">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-6962">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6962">Texture1D</span></span> | \- |
| <span data-ttu-id="ba9fe-6963">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6963">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6965">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6965">Texture3D</span></span> | \- |
| <span data-ttu-id="ba9fe-6966">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6966">TextureCube</span></span> | \- |
| <span data-ttu-id="ba9fe-6967">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6967">Shader ld</span></span> | \- |
| <span data-ttu-id="ba9fe-6968">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6968">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6969">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6969">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6970">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-6970">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-6971">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6971">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-6972">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6972">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-6973">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6973">Mipmap</span></span> | \- |
| <span data-ttu-id="ba9fe-6974">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ba9fe-6975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6975">RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6976">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6977">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-6978">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-6979">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6980">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-6981">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6981">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-6982">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-6983">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6984">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-6985">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-6986">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-6987">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-6988">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6989">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-6990">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6990">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-6992">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6993">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ba9fe-6994">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ba9fe-6995">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ba9fe-6996">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6996">Multisample Load</span></span> | \- |
| <span data-ttu-id="ba9fe-6997">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-6998">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6998">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-6999">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-6999">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-7000">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7000">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-7002">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-7003">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7003">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-7004">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7004">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="ba9fe-7005">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-7005">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="ba9fe-7006">目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7006">Target</span></span> | <span data-ttu-id="ba9fe-7007">支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7007">Support</span></span> |
| - | - |
| <span data-ttu-id="ba9fe-7008">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-7008">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ba9fe-7009">16</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7009">16</span></span> |
| <span data-ttu-id="ba9fe-7010">格式支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7010">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-7012">Buffer</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7012">Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-7014">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7014">Input Assembler Vertex Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-7016">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7016">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-7017">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7017">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ba9fe-7018">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7018">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-7020">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7020">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-7022">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7022">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-7024">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7024">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-7026">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7026">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-7028">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-7028">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-7030">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-7030">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-7031">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ba9fe-7031">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ba9fe-7032">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7032">Shader gather4</span></span> | \- |
| <span data-ttu-id="ba9fe-7033">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7033">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ba9fe-7034">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7034">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-7036">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7036">Mipmap Auto-Generation</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-7038">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7038">RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-7040">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7040">Blendable RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-7042">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7042">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ba9fe-7043">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7043">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ba9fe-7044">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7044">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-7045">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7045">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ba9fe-7046">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7046">Typed UAV</span></span> | \- |
| <span data-ttu-id="ba9fe-7047">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7047">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ba9fe-7048">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7048">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ba9fe-7049">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7049">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ba9fe-7050">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7050">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ba9fe-7051">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7051">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ba9fe-7052">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7052">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ba9fe-7053">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7053">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-7054">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7054">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ba9fe-7055">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7055">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-7057">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7057">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-7059">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7059">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-7061">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7061">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-7063">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7063">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ba9fe-7065">多級載入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7065">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ba9fe-7067">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ba9fe-7068">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ba9fe-7069">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ba9fe-7070">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7070">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ba9fe-7071">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7071">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ba9fe-7072">共用資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7072">Shared Resource</span></span> | \- |
| <span data-ttu-id="ba9fe-7073">磚資源</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7073">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="ba9fe-7074">格式化附注</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7074">Format notes</span></span>

<span data-ttu-id="ba9fe-7075">格式的用途可從一個硬體功能層級變更為下一個硬體功能層級。</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7075">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="ba9fe-7076"><sup>L</sup> ：無格式的格式</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7076"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="ba9fe-7077"><sup>電腦</sup> ：部分類型、可轉換和簡單版面配置</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7077"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="ba9fe-7078"><sup>FCS</sup> ：完整型別、可轉換和 simple 版面配置</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7078"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="ba9fe-7079"><sup>FNS</sup> ：完全具類型、非可轉換和簡單版面配置</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7079"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="ba9fe-7080"><sup>PCC</sup> ：部分類型、可轉換和複雜版面配置</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7080"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="ba9fe-7081"><sup>FCC</sup> ：完整型別、可轉換和複雜的版面配置</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7081"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="ba9fe-7082"><sup>FNC</sup> ：完整型別、非可轉換和複雜的版面配置</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7082"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="ba9fe-7083"><sup>V</sup> ：影片格式</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7083"><sup>V</sup> : video format</span></span>
</dt> </dl>

<span data-ttu-id="ba9fe-7084">使用 [**DXGI \_ 格式 \_ R16G16B16A16 \_ FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式的背景緩衝區和掃描輸出包含線性值 gamma 資料。</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7084">Back buffers and scan outs with the [**DXGI\_FORMAT\_R16G16B16A16\_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format contain linear-valued gamma data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba9fe-7085">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7085">Related topics</span></span>

[<span data-ttu-id="ba9fe-7086">D3D12 硬體功能等級</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7086">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="ba9fe-7087">**ID3D10Device::CheckFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7087">**ID3D10Device::CheckFormatSupport**</span></span>](/windows/win32/api/d3d10/nf-d3d10-id3d10device-checkformatsupport)

[<span data-ttu-id="ba9fe-7088">DXGI 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="ba9fe-7088">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
