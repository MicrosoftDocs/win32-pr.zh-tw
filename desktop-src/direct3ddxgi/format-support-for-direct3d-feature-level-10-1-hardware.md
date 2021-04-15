---
description: 本節指定 Direct3D 功能等級10.1 硬體支援的格式 ([ **DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)值) 。
ms.assetid: 2C7E16D7-EEF0-4EA7-A819-5274C9105F68
title: Direct3D 功能層級 10.1 硬體的格式支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edb5c81ef0a99bc14031a9a7a505736e91e13d8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467585"
---
# <a name="format-support-for-direct3d-feature-level-101-hardware"></a><span data-ttu-id="93a62-103">Direct3D 功能層級 10.1 硬體的格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-103">Format support for Direct3D Feature Level 10.1 hardware</span></span>

<span data-ttu-id="93a62-104">此區段會指定 Direct3D 功能等級10.1 硬體支援的格式 ([ _\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)值) 。</span><span class="sxs-lookup"><span data-stu-id="93a62-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 10.1 hardware.</span></span>

<span data-ttu-id="93a62-105">下表摘要說明使用下列索引鍵的功能支援。</span><span class="sxs-lookup"><span data-stu-id="93a62-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="93a62-106">符號</span><span class="sxs-lookup"><span data-stu-id="93a62-106">Symbol</span></span>                            | <span data-ttu-id="93a62-107">描述</span><span class="sxs-lookup"><span data-stu-id="93a62-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="93a62-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="93a62-108">_ *-*\*</span></span>                             | <span data-ttu-id="93a62-109">不允許或無法使用。</span><span class="sxs-lookup"><span data-stu-id="93a62-109">Disallowed or not available.</span></span>                                                  |
| ![必要](images/letter-r.jpg)  | <span data-ttu-id="93a62-111">需要硬體支援。</span><span class="sxs-lookup"><span data-stu-id="93a62-111">Hardware support is required.</span></span>                                                 |
| ![選用](images/letter-o.jpg)  | <span data-ttu-id="93a62-113">硬體支援是選擇性的，格式可能或可能不會有硬體加速。</span><span class="sxs-lookup"><span data-stu-id="93a62-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![依賴](images/letter-d.jpg) | <span data-ttu-id="93a62-115">如果支援相關的選擇性功能，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="93a62-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="93a62-116">本主題包含每一種格式的區段。</span><span class="sxs-lookup"><span data-stu-id="93a62-116">This topic contains a section per format.</span></span> <span data-ttu-id="93a62-117">格式 *目標* (資料表每個目標各包含一個資料列) 可以是資源類型、HLSL 內建函式，或是相依于特定格式的特定功能。</span><span class="sxs-lookup"><span data-stu-id="93a62-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="93a62-118">若要以程式設計方式驗證 D3D11 和 D3D12 中的格式支援，請參閱 [檢查硬體功能支援](checking-hardware-feature-support.md)。</span><span class="sxs-lookup"><span data-stu-id="93a62-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="93a62-119">這些格式的數目大多是（但不是全部），以遞增的數值順序來 &mdash; 看，有些會超出數值順序，並與其他相關的格式一起列出。</span><span class="sxs-lookup"><span data-stu-id="93a62-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="93a62-120">另請注意 *，格式名稱的無* 型別可以表示 *部分* 具型別，而不是嚴格的無型別 (請參閱主題結尾的 [格式附注](#format-notes) 章節) 。</span><span class="sxs-lookup"><span data-stu-id="93a62-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="93a62-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0) </span><span class="sxs-lookup"><span data-stu-id="93a62-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="93a62-122">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-122">Target</span></span> | <span data-ttu-id="93a62-123">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-123">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-124">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-125">0</span><span class="sxs-lookup"><span data-stu-id="93a62-125">0</span></span> |
| <span data-ttu-id="93a62-126">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-126">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-128">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-128">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-130">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-131">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-132">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-133">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-134">Texture2D</span></span> | \- |
| <span data-ttu-id="93a62-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-135">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-136">TextureCube</span></span> | \- |
| <span data-ttu-id="93a62-137">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-137">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-138">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-139">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-139">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-140">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-140">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-141">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-142">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-142">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-143">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-143">Mipmap</span></span> | \- |
| <span data-ttu-id="93a62-144">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-146">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-147">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-148">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-149">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-150">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-151">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-151">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-152">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-153">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-154">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-155">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-156">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-157">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-158">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-159">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-160">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-160">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-162">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-163">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-164">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-165">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-166">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-166">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-167">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-168">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-168">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-169">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-170">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-171">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-172">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-172">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-173">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="93a62-174">DXGI_FORMAT_R32G32B32A32 無的 \_ <sup>電腦</sup> (1) </span><span class="sxs-lookup"><span data-stu-id="93a62-174">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="93a62-175">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-175">Target</span></span> | <span data-ttu-id="93a62-176">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-176">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-177">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-178">128</span><span class="sxs-lookup"><span data-stu-id="93a62-178">128</span></span> |
| <span data-ttu-id="93a62-179">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-179">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-181">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-181">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-182">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-182">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-183">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-183">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-184">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-184">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-185">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-185">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-187">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-189">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-189">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-191">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-191">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-193">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-193">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-194">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-194">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-195">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-195">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-196">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-196">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-197">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-197">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-198">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-198">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-199">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-199">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-201">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-201">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-202">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-202">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-203">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-203">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-204">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-204">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-205">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-206">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-207">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-208">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-208">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-209">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-209">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-210">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-210">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-211">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-211">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-212">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-212">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-213">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-213">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-214">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-214">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-215">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-215">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-216">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-216">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-217">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-217">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-219">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-219">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-220">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-220">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-221">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-221">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-222">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-222">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-223">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-223">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-224">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-224">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-225">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-225">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-227">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-227">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-228">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-228">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-229">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-229">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-230">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-230">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-232">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-232">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="93a62-233">DXGI_FORMAT_R32G32B32A32 \_ FLOAT<sup>FCS</sup> (2) </span><span class="sxs-lookup"><span data-stu-id="93a62-233">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="93a62-234">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-234">Target</span></span> | <span data-ttu-id="93a62-235">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-235">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-236">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-236">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-237">128</span><span class="sxs-lookup"><span data-stu-id="93a62-237">128</span></span> |
| <span data-ttu-id="93a62-238">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-238">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-240">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-240">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-242">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-242">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-244">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-244">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-245">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-245">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-247">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-249">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-249">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-251">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-253">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-253">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-255">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-255">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-257">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-257">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-259">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-260">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-261">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-261">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-262">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-263">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-263">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-265">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-265">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-267">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-267">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-269">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-269">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-271">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-272">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-273">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-274">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-275">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-275">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-276">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-276">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-277">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-277">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-278">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-278">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-279">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-279">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-280">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-280">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-281">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-281">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-282">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-282">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-283">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-283">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-284">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-284">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-286">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-286">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-288">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-288">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-290">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-290">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-292">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-292">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-294">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-294">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-296">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-296">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-297">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-297">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-299">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-299">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-300">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-300">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-301">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-301">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-302">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-302">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-304">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-304">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="93a62-305">DXGI_FORMAT_R32G32B32A32 \_ UINT<sup>FCS</sup> (3) </span><span class="sxs-lookup"><span data-stu-id="93a62-305">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="93a62-306">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-306">Target</span></span> | <span data-ttu-id="93a62-307">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-307">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-308">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-308">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-309">128</span><span class="sxs-lookup"><span data-stu-id="93a62-309">128</span></span> |
| <span data-ttu-id="93a62-310">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-310">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-312">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-312">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-314">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-314">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-316">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-316">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-317">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-317">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-319">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-319">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-321">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-321">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-323">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-323">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-325">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-325">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-327">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-327">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-329">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-329">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-330">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-330">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-331">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-331">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-332">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-332">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-333">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-333">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-334">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-334">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-336">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-336">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-337">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-337">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-339">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-339">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-340">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-340">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-342">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-342">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-343">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-343">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-344">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-344">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-345">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-345">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-346">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-346">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-347">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-347">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-348">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-348">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-349">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-349">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-350">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-350">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-351">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-351">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-352">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-352">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-353">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-353">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-354">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-354">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-356">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-356">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-358">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-358">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-360">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-360">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-362">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-362">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-363">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-363">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-365">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-365">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-366">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-366">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-368">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-369">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-370">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-371">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-371">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-373">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-373">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="93a62-374">DXGI_FORMAT_R32G32B32A32 \_ 聖的<sup>FCS</sup> (4) </span><span class="sxs-lookup"><span data-stu-id="93a62-374">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="93a62-375">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-375">Target</span></span> | <span data-ttu-id="93a62-376">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-376">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-377">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-377">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-378">128</span><span class="sxs-lookup"><span data-stu-id="93a62-378">128</span></span> |
| <span data-ttu-id="93a62-379">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-379">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-381">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-381">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-383">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-383">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-385">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-385">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-386">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-386">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-388">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-388">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-390">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-390">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-392">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-392">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-394">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-396">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-396">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-398">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-399">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-400">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-401">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-401">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-402">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-403">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-403">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-405">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-406">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-408">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-409">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-410">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-411">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-412">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-413">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-414">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-415">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-416">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-417">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-418">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-419">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-420">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-421">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-422">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-422">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-424">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-424">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-426">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-426">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-428">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-428">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-430">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-430">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-431">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-431">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-433">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-434">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-434">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-436">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-437">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-438">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-439">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-439">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-441">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="93a62-442">DXGI_FORMAT_R32G32B32 無的 \_ <sup>電腦</sup> (5) </span><span class="sxs-lookup"><span data-stu-id="93a62-442">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="93a62-443">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-443">Target</span></span> | <span data-ttu-id="93a62-444">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-444">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-445">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-446">96</span><span class="sxs-lookup"><span data-stu-id="93a62-446">96</span></span> |
| <span data-ttu-id="93a62-447">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-447">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-449">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-449">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-450">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-451">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-452">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-453">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-455">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-455">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-457">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-459">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-459">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-461">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-461">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-462">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-462">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-463">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-463">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-464">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-464">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-465">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-465">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-466">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-466">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-467">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-467">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-469">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-470">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-471">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-472">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-473">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-474">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-475">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-476">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-476">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-477">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-478">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-479">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-480">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-481">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-481">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-482">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-483">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-484">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-485">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-485">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-487">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-487">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-488">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-488">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-489">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-489">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-490">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-490">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-491">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-491">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-492">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-492">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-493">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-493">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-495">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-496">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-497">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-498">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-498">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-499">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="93a62-500">DXGI_FORMAT_R32G32B32 \_ FLOAT<sup>FCS</sup> (6) </span><span class="sxs-lookup"><span data-stu-id="93a62-500">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="93a62-501">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-501">Target</span></span> | <span data-ttu-id="93a62-502">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-502">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-503">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-504">96</span><span class="sxs-lookup"><span data-stu-id="93a62-504">96</span></span> |
| <span data-ttu-id="93a62-505">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-505">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-507">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-507">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-509">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-509">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-511">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-511">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-512">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-512">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-514">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-514">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-516">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-518">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-520">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-522">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-522">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-524">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-524">Shader sample (any filter)</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-526">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-526">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-527">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-527">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-528">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-528">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-529">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-529">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-530">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-530">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-532">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-532">Mipmap Auto-Generation</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-534">RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-536">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-536">Blendable RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="93a62-538">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-538">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-539">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-539">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-540">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-540">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-541">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-541">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-542">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-542">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-543">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-543">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-544">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-544">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-545">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-545">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-546">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-546">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-547">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-547">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-548">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-548">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-549">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-549">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-550">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-550">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-551">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-551">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-553">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-553">4x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="93a62-555">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-555">8x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="93a62-557">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-557">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-559">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-559">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-561">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-561">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-563">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-563">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-564">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-564">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-566">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-566">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-567">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-567">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-568">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-568">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-569">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-569">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-570">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-570">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="93a62-571">DXGI_FORMAT_R32G32B32 \_ UINT<sup>FCS</sup> (7) </span><span class="sxs-lookup"><span data-stu-id="93a62-571">DXGI_FORMAT_R32G32B32\_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="93a62-572">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-572">Target</span></span> | <span data-ttu-id="93a62-573">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-573">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-574">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-574">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-575">96</span><span class="sxs-lookup"><span data-stu-id="93a62-575">96</span></span> |
| <span data-ttu-id="93a62-576">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-576">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-578">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-578">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-580">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-580">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-582">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-583">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-583">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-585">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-587">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-589">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-591">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-591">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-593">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-593">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-595">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-595">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-596">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-596">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-597">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-597">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-598">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-598">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-599">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-600">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-600">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-602">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-602">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-603">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-603">RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-605">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-606">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-606">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-608">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-608">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-609">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-609">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-610">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-610">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-611">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-611">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-612">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-612">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-613">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-613">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-614">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-614">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-615">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-615">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-616">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-616">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-617">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-617">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-618">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-618">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-619">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-619">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-620">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-620">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-622">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-622">4x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="93a62-624">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-624">8x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="93a62-626">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-626">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-628">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-628">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-629">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-629">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-631">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-631">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-632">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-632">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-634">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-634">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-635">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-635">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-636">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-636">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-637">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-637">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-638">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-638">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="93a62-639">DXGI_FORMAT_R32G32B32 \_ 聖的<sup>FCS</sup> (8) </span><span class="sxs-lookup"><span data-stu-id="93a62-639">DXGI_FORMAT_R32G32B32\_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="93a62-640">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-640">Target</span></span> | <span data-ttu-id="93a62-641">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-641">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-642">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-642">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-643">96</span><span class="sxs-lookup"><span data-stu-id="93a62-643">96</span></span> |
| <span data-ttu-id="93a62-644">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-644">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-646">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-646">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-648">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-648">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-650">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-650">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-651">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-651">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-653">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-655">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-657">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-659">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-661">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-661">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-663">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-664">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-665">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-666">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-666">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-667">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-668">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-668">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-670">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-670">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-671">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-671">RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-673">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-673">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-674">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-675">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-676">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-677">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-678">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-678">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-679">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-680">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-681">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-682">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-683">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-683">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-684">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-685">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-686">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-687">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-687">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-689">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-689">4x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="93a62-691">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-691">8x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="93a62-693">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-693">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-695">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-696">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-696">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-698">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-698">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-699">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-699">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-701">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-701">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-702">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-702">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-703">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-703">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-704">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-704">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-705">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-705">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="93a62-706">DXGI_FORMAT_R16G16B16A16 無別 \_ <sup>電腦</sup> (9) </span><span class="sxs-lookup"><span data-stu-id="93a62-706">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="93a62-707">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-707">Target</span></span> | <span data-ttu-id="93a62-708">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-708">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-709">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-709">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-710">64</span><span class="sxs-lookup"><span data-stu-id="93a62-710">64</span></span> |
| <span data-ttu-id="93a62-711">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-711">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-713">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-713">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-714">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-714">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-715">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-715">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-716">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-716">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-717">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-717">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-719">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-719">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-721">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-721">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-723">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-723">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-725">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-725">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-726">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-726">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-727">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-727">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-728">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-728">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-729">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-729">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-730">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-730">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-731">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-731">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-733">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-733">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-734">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-734">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-735">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-735">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-736">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-736">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-737">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-738">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-739">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-740">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-740">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-741">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-741">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-742">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-742">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-743">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-743">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-744">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-744">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-745">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-745">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-746">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-746">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-747">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-747">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-748">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-748">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-749">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-749">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-751">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-751">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-752">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-752">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-753">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-753">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-754">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-754">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-755">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-755">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-756">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-756">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-757">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-757">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-759">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-759">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-760">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-760">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-761">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-761">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-762">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-762">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-764">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-764">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="93a62-765">DXGI_FORMAT_R16G16B16A16 \_ FLOAT<sup>FCS</sup> (10) </span><span class="sxs-lookup"><span data-stu-id="93a62-765">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="93a62-766">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-766">Target</span></span> | <span data-ttu-id="93a62-767">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-767">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-768">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-768">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-769">64</span><span class="sxs-lookup"><span data-stu-id="93a62-769">64</span></span> |
| <span data-ttu-id="93a62-770">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-770">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-772">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-772">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-774">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-774">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-776">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-776">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-777">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-777">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-778">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-778">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-780">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-780">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-782">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-782">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-784">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-786">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-786">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-788">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-788">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-790">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-790">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-791">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-791">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-792">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-792">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-793">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-793">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-794">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-794">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-796">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-796">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-798">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-798">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-800">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-800">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-802">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-802">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-803">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-803">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-804">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-804">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-805">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-805">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-806">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-806">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-807">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-807">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-808">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-808">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-809">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-809">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-810">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-810">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-811">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-811">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-812">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-812">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-813">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-813">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-814">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-814">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-815">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-815">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-817">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-817">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-819">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-819">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-821">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-821">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-823">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-823">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-825">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-825">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-827">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-827">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-829">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-829">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-831">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-831">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-832">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-832">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-834">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-834">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-836">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-836">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-838">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-838">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="93a62-839">DXGI_FORMAT_R16G16B16A16 \_ UNORM 的<sup>FCS</sup> (11) </span><span class="sxs-lookup"><span data-stu-id="93a62-839">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="93a62-840">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-840">Target</span></span> | <span data-ttu-id="93a62-841">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-841">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-842">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-842">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-843">64</span><span class="sxs-lookup"><span data-stu-id="93a62-843">64</span></span> |
| <span data-ttu-id="93a62-844">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-844">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-846">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-846">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-848">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-848">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-850">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-850">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-851">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-851">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-852">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-852">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-854">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-854">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-856">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-856">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-858">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-860">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-860">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-862">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-862">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-864">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-864">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-865">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-865">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-866">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-866">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-867">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-867">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-868">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-868">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-870">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-870">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-872">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-872">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-874">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-874">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-876">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-877">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-878">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-879">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-880">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-880">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-881">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-882">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-883">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-884">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-885">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-885">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-886">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-887">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-888">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-889">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-889">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-891">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-891">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-893">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-893">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-895">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-895">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-897">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-897">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-899">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-899">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-901">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-901">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-902">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-902">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-904">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-905">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-906">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-907">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-907">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-909">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-909">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="93a62-910">DXGI_FORMAT_R16G16B16A16 \_ UINT<sup>FCS</sup> (12) </span><span class="sxs-lookup"><span data-stu-id="93a62-910">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="93a62-911">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-911">Target</span></span> | <span data-ttu-id="93a62-912">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-912">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-913">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-913">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-914">64</span><span class="sxs-lookup"><span data-stu-id="93a62-914">64</span></span> |
| <span data-ttu-id="93a62-915">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-915">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-917">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-917">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-919">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-919">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-921">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-921">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-922">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-922">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-923">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-923">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-925">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-927">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-929">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-929">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-931">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-931">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-933">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-934">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-935">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-936">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-936">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-937">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-938">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-938">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-940">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-940">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-941">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-941">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-943">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-943">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-944">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-944">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-946">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-946">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-947">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-947">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-948">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-948">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-949">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-949">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-950">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-950">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-951">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-951">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-952">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-952">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-953">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-953">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-954">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-954">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-955">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-955">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-956">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-956">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-957">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-957">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-958">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-958">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-960">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-960">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-962">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-962">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-964">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-964">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-966">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-966">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-967">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-967">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-969">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-969">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-970">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-970">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-972">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-972">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-973">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-973">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-974">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-974">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-975">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-975">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-977">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-977">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="93a62-978">DXGI_FORMAT_R16G16B16A16 \_ SNORM 的<sup>FCS</sup> (13) </span><span class="sxs-lookup"><span data-stu-id="93a62-978">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="93a62-979">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-979">Target</span></span> | <span data-ttu-id="93a62-980">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-980">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-981">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-981">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-982">64</span><span class="sxs-lookup"><span data-stu-id="93a62-982">64</span></span> |
| <span data-ttu-id="93a62-983">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-983">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-985">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-985">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-987">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-987">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-989">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-990">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-991">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-993">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-993">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-995">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-995">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-997">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-997">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-999">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-999">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1001">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1001">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1003">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1003">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-1004">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1004">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-1005">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-1005">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-1006">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-1006">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-1007">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-1007">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1009">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-1009">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1011">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1013">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1013">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1015">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-1015">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-1016">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1016">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-1017">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1017">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1018">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1018">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1019">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-1019">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-1020">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-1020">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-1021">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1021">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-1022">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-1022">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-1023">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-1023">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-1024">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-1024">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-1025">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-1025">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-1026">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1026">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1027">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1027">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1028">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-1028">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1030">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1030">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1032">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1032">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1034">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-1034">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1036">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-1036">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1038">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1038">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1040">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-1040">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-1041">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-1041">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1043">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1043">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-1044">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-1044">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-1045">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-1045">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-1046">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1046">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1048">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1048">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="93a62-1049">DXGI_FORMAT_R16G16B16A16 \_ 聖的<sup>FCS</sup> (14) </span><span class="sxs-lookup"><span data-stu-id="93a62-1049">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="93a62-1050">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1050">Target</span></span> | <span data-ttu-id="93a62-1051">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1051">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-1052">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-1052">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-1053">64</span><span class="sxs-lookup"><span data-stu-id="93a62-1053">64</span></span> |
| <span data-ttu-id="93a62-1054">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1054">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1056">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-1056">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1058">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1058">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1060">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1060">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1061">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1061">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1062">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-1062">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1064">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-1064">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1066">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-1066">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1068">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-1068">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1070">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-1070">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1072">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1072">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-1073">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1073">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-1074">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1074">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-1075">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-1075">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-1076">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-1076">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-1077">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-1077">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1079">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-1079">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-1080">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1080">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1082">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1082">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1083">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-1083">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-1084">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1084">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-1085">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1085">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1086">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1086">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1087">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-1087">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-1088">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-1088">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-1089">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1089">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-1090">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-1090">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-1091">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-1091">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-1092">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-1092">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-1093">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-1093">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-1094">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1094">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1095">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1095">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1096">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-1096">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1098">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1098">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1100">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1100">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1102">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-1102">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1104">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-1104">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-1105">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1105">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1107">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-1107">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-1108">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-1108">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1110">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-1111">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-1111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-1112">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-1112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-1113">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1113">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1115">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1115">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="93a62-1116">DXGI_FORMAT_R32G32 無別 \_ <sup>電腦</sup> (15) </span><span class="sxs-lookup"><span data-stu-id="93a62-1116">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="93a62-1117">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1117">Target</span></span> | <span data-ttu-id="93a62-1118">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1118">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-1119">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-1119">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-1120">64</span><span class="sxs-lookup"><span data-stu-id="93a62-1120">64</span></span> |
| <span data-ttu-id="93a62-1121">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1121">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1123">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-1123">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1124">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1124">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1125">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1125">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1126">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1126">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1127">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-1127">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1129">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-1129">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1131">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-1131">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1133">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-1133">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1135">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-1135">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-1136">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-1137">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-1138">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-1139">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-1139">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-1140">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-1140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-1141">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-1141">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1143">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-1143">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-1144">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1144">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1145">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1145">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1146">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-1146">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-1147">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1147">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-1148">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1148">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1149">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1149">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1150">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-1150">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-1151">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-1151">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-1152">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1152">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-1153">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-1153">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-1154">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-1154">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-1155">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-1155">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-1156">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-1156">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-1157">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1157">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1158">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1158">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1159">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-1159">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1161">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1161">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1162">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1162">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1163">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-1163">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-1164">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-1164">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-1165">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1165">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-1166">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-1166">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-1167">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-1167">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1169">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-1170">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-1170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-1171">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-1171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-1172">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1172">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-1173">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="93a62-1174">DXGI_FORMAT_R32G32 \_ FLOAT<sup>FCS</sup> (16) </span><span class="sxs-lookup"><span data-stu-id="93a62-1174">DXGI_FORMAT_R32G32\_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="93a62-1175">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1175">Target</span></span> | <span data-ttu-id="93a62-1176">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1176">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-1177">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-1177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-1178">64</span><span class="sxs-lookup"><span data-stu-id="93a62-1178">64</span></span> |
| <span data-ttu-id="93a62-1179">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1179">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1181">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-1181">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1183">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1183">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1185">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1185">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1186">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1186">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1188">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-1188">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1190">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-1190">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1192">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-1192">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1194">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-1194">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1196">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-1196">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1198">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1198">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1200">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1200">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-1201">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1201">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-1202">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-1202">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-1203">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-1203">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-1204">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-1204">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1206">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-1206">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1208">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1208">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1210">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1210">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1212">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-1212">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-1213">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1213">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-1214">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1214">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1215">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1215">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1216">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-1216">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-1217">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-1217">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-1218">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1218">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-1219">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-1219">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-1220">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-1220">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-1221">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-1221">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-1222">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-1222">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-1223">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1223">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1224">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1224">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1225">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-1225">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1227">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1227">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1229">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1229">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1231">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-1231">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1233">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-1233">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1235">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1235">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1237">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-1237">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-1238">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-1238">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1240">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1240">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-1241">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-1241">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-1242">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-1242">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-1243">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1243">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-1244">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1244">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="93a62-1245">DXGI_FORMAT_R32G32 \_ UINT<sup>FCS</sup> (17) </span><span class="sxs-lookup"><span data-stu-id="93a62-1245">DXGI_FORMAT_R32G32\_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="93a62-1246">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1246">Target</span></span> | <span data-ttu-id="93a62-1247">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1247">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-1248">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-1248">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-1249">64</span><span class="sxs-lookup"><span data-stu-id="93a62-1249">64</span></span> |
| <span data-ttu-id="93a62-1250">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1250">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1252">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-1252">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1254">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1254">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1256">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1256">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1257">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1257">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1259">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-1259">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1261">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-1261">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1263">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-1263">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1265">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-1265">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1267">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-1267">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1269">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1269">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-1270">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1270">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-1271">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1271">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-1272">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-1272">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-1273">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-1273">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-1274">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-1274">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1276">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-1276">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-1277">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1277">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1279">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1279">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1280">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-1280">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1282">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-1283">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1284">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1285">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-1285">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-1286">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-1286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-1287">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-1288">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-1288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-1289">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-1289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-1290">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-1290">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-1291">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-1291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-1292">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1293">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1294">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-1294">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1296">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1296">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1298">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1298">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1300">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-1300">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1302">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-1302">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-1303">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1303">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1305">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-1305">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-1306">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-1306">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1308">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1308">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-1309">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-1309">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-1310">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-1310">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-1311">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1311">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-1312">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1312">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="93a62-1313">DXGI_FORMAT_R32G32 \_ 聖的<sup>FCS</sup> (18) </span><span class="sxs-lookup"><span data-stu-id="93a62-1313">DXGI_FORMAT_R32G32\_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="93a62-1314">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1314">Target</span></span> | <span data-ttu-id="93a62-1315">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1315">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-1316">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-1316">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-1317">64</span><span class="sxs-lookup"><span data-stu-id="93a62-1317">64</span></span> |
| <span data-ttu-id="93a62-1318">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1318">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1320">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-1320">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1322">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1322">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1324">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1324">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1325">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1325">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1327">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-1327">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1329">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-1329">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1331">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-1331">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1333">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-1333">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1335">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-1335">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1337">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1337">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-1338">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1338">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-1339">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1339">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-1340">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-1340">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-1341">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-1341">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-1342">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-1342">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1344">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-1344">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-1345">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1345">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1347">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1347">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1348">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-1348">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-1349">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1349">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-1350">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1350">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1351">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1351">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1352">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-1352">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-1353">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-1353">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-1354">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1354">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-1355">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-1355">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-1356">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-1356">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-1357">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-1357">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-1358">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-1358">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-1359">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1359">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1360">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1360">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1361">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-1361">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1363">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1363">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1365">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1365">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1367">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-1367">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1369">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-1369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-1370">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1370">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1372">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-1372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-1373">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-1373">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1375">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1375">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-1376">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-1376">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-1377">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-1377">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-1378">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1378">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-1379">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1379">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="93a62-1380">DXGI_FORMAT_R32G8X24 無別 \_ <sup>電腦</sup> (19) </span><span class="sxs-lookup"><span data-stu-id="93a62-1380">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="93a62-1381">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1381">Target</span></span> | <span data-ttu-id="93a62-1382">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1382">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-1383">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-1383">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-1384">64</span><span class="sxs-lookup"><span data-stu-id="93a62-1384">64</span></span> |
| <span data-ttu-id="93a62-1385">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1385">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1387">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-1387">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1388">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1388">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1389">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1390">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-1391">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1393">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-1393">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1395">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-1395">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-1396">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-1396">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1398">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-1398">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-1399">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1399">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-1400">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1400">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-1401">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1401">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-1402">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-1402">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-1403">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-1403">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-1404">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-1404">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1406">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-1406">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-1407">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1407">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1408">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1409">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-1409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-1410">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-1411">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1412">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1413">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-1413">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-1414">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-1414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-1415">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-1416">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-1416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-1417">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-1417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-1418">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-1418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-1419">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-1419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-1420">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1421">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1422">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-1422">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1424">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1424">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1425">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1425">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1426">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-1426">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-1427">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-1427">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-1428">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1428">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-1429">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-1429">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-1430">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-1430">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1432">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1432">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-1433">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-1433">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-1434">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-1434">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-1435">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1435">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-1436">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1436">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a><span data-ttu-id="93a62-1437">DXGI_FORMAT_D32 \_ FLOAT \_ S8X24 \_ UINT<sup>FCS</sup> (20) </span><span class="sxs-lookup"><span data-stu-id="93a62-1437">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FCS</sup> (20)</span></span>
| <span data-ttu-id="93a62-1438">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1438">Target</span></span> | <span data-ttu-id="93a62-1439">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1439">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-1440">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-1440">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-1441">64</span><span class="sxs-lookup"><span data-stu-id="93a62-1441">64</span></span> |
| <span data-ttu-id="93a62-1442">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1442">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1444">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-1444">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1445">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1445">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1446">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1446">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1447">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1447">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1448">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-1448">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1450">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-1450">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1452">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-1452">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-1453">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-1453">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1455">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-1455">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-1456">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1456">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-1457">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1457">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-1458">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1458">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-1459">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-1459">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-1460">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-1460">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-1461">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-1461">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1463">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-1463">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-1464">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1464">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1465">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1465">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1466">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-1466">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-1467">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1467">Depth/Stencil Target</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1469">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1469">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1470">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1470">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1471">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-1471">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-1472">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-1472">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-1473">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1473">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-1474">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-1474">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-1475">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-1475">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-1476">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-1476">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-1477">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-1477">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-1478">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1478">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1479">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1479">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1480">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-1480">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1482">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1482">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1484">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1484">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1486">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-1486">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1488">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-1488">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-1489">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1489">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-1490">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-1490">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-1491">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-1491">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1493">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1493">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-1494">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-1494">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-1495">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-1495">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-1496">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1496">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-1497">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1497">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a><span data-ttu-id="93a62-1498">DXGI_FORMAT_R32 \_ FLOAT X8X24 無型別 \_ \_ <sup>FCS</sup> (21) </span><span class="sxs-lookup"><span data-stu-id="93a62-1498">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FCS</sup> (21)</span></span>
| <span data-ttu-id="93a62-1499">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1499">Target</span></span> | <span data-ttu-id="93a62-1500">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1500">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-1501">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-1501">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-1502">64</span><span class="sxs-lookup"><span data-stu-id="93a62-1502">64</span></span> |
| <span data-ttu-id="93a62-1503">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1503">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1505">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-1505">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1506">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1506">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1507">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1507">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1508">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1508">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1509">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-1509">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1511">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-1511">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1513">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-1513">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-1514">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-1514">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1516">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-1516">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1518">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1518">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1520">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1520">Shader sample\_c (comparison filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1522">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1522">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-1523">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-1523">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1525">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-1525">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-1526">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-1526">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1528">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-1528">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-1529">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1529">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1530">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1530">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1531">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-1531">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-1532">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1532">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-1533">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1533">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1534">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1534">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1535">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-1535">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-1536">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-1536">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-1537">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1537">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-1538">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-1538">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-1539">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-1539">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-1540">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-1540">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-1541">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-1541">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-1542">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1542">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1543">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1543">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1544">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-1544">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1546">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1546">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1547">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1547">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1548">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-1548">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-1549">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-1549">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-1550">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1550">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1552">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-1552">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-1553">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-1553">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1555">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1555">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-1556">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-1556">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-1557">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-1557">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-1558">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1558">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-1559">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1559">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a><span data-ttu-id="93a62-1560">DXGI_FORMAT_X32 無別 \_ \_ G8X24 \_ UINT<sup>FCS</sup> (22) </span><span class="sxs-lookup"><span data-stu-id="93a62-1560">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FCS</sup> (22)</span></span>
| <span data-ttu-id="93a62-1561">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1561">Target</span></span> | <span data-ttu-id="93a62-1562">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1562">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-1563">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-1563">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-1564">64</span><span class="sxs-lookup"><span data-stu-id="93a62-1564">64</span></span> |
| <span data-ttu-id="93a62-1565">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1565">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1567">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-1567">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1568">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1568">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1569">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1569">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1570">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1570">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1571">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-1571">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1573">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-1573">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1575">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-1575">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-1576">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-1576">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1578">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-1578">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1580">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1580">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-1581">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1581">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-1582">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1582">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-1583">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-1583">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-1584">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-1584">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-1585">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-1585">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1587">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-1587">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-1588">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1588">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1589">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1589">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1590">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-1590">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-1591">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1591">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-1592">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1592">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1593">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1593">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1594">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-1594">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-1595">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-1595">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-1596">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1596">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-1597">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-1597">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-1598">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-1598">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-1599">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-1599">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-1600">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-1600">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-1601">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1601">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1602">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1602">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1603">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-1603">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1605">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1605">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1606">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1606">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1607">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-1607">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-1608">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-1608">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-1609">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1609">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1611">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-1611">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-1612">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-1612">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1614">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1614">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-1615">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-1615">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-1616">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-1616">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-1617">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1617">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-1618">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1618">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="93a62-1619">DXGI_FORMAT_R10G10B10A2 無別 \_ <sup>電腦</sup> (23) </span><span class="sxs-lookup"><span data-stu-id="93a62-1619">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="93a62-1620">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1620">Target</span></span> | <span data-ttu-id="93a62-1621">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1621">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-1622">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-1622">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-1623">32</span><span class="sxs-lookup"><span data-stu-id="93a62-1623">32</span></span> |
| <span data-ttu-id="93a62-1624">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1624">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1626">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-1626">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1627">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1627">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1628">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1628">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1629">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1629">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1630">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-1630">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1632">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-1632">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1634">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-1634">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1636">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-1636">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1638">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-1638">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-1639">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1639">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-1640">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1640">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-1641">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1641">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-1642">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-1642">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-1643">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-1643">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-1644">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-1644">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1646">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-1646">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-1647">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1647">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1648">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1648">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1649">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-1649">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-1650">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1650">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-1651">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1651">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1652">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1652">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1653">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-1653">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-1654">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-1654">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-1655">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1655">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-1656">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-1656">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-1657">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-1657">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-1658">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-1658">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-1659">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-1659">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-1660">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1660">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1661">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1661">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1662">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-1662">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1664">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1664">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1665">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1665">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1666">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-1666">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-1667">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-1667">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-1668">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1668">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-1669">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-1669">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-1670">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-1670">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1672">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1672">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-1673">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-1673">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-1674">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-1674">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-1675">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1675">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1677">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1677">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="93a62-1678">DXGI_FORMAT_R10G10B10A2 \_ UNORM 的<sup>FCS</sup> (24) </span><span class="sxs-lookup"><span data-stu-id="93a62-1678">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="93a62-1679">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1679">Target</span></span> | <span data-ttu-id="93a62-1680">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1680">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-1681">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-1681">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-1682">32</span><span class="sxs-lookup"><span data-stu-id="93a62-1682">32</span></span> |
| <span data-ttu-id="93a62-1683">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1683">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1685">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-1685">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1687">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1687">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1689">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1689">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1690">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1690">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1691">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-1691">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1693">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-1693">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1695">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-1695">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1697">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-1697">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1699">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-1699">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1701">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1701">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1703">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1703">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-1704">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1704">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-1705">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-1705">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-1706">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-1706">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-1707">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-1707">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1709">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-1709">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1711">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1711">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1713">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1713">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1715">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-1715">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-1716">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1716">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-1717">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1717">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1718">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1718">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1719">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-1719">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-1720">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-1720">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-1721">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1721">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-1722">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-1722">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-1723">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-1723">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-1724">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-1724">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-1725">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-1725">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-1726">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1726">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1727">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1727">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1728">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-1728">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1730">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1730">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1732">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1732">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1734">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-1734">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1736">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-1736">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1738">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1738">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1740">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-1740">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1742">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-1742">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1744">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1744">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-1745">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-1745">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1747">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-1747">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1749">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1749">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1751">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1751">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="93a62-1752">DXGI_FORMAT_R10G10B10A2 \_ UINT<sup>FCS</sup> (25) </span><span class="sxs-lookup"><span data-stu-id="93a62-1752">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="93a62-1753">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1753">Target</span></span> | <span data-ttu-id="93a62-1754">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1754">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-1755">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-1755">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-1756">32</span><span class="sxs-lookup"><span data-stu-id="93a62-1756">32</span></span> |
| <span data-ttu-id="93a62-1757">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1757">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1759">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-1759">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1761">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1761">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1763">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1763">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1764">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1764">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1765">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-1765">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1767">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-1767">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1769">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-1769">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1771">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-1771">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1773">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-1773">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1775">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1775">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-1776">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1776">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-1777">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1777">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-1778">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-1778">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-1779">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-1779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-1780">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-1780">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1782">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-1782">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-1783">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1783">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1785">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1785">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1786">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-1786">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1788">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1788">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-1789">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1789">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1790">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1790">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1791">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-1791">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-1792">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-1792">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-1793">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1793">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-1794">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-1794">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-1795">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-1795">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-1796">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-1796">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-1797">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-1797">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-1798">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1798">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1799">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1799">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1800">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-1800">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1802">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1802">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1804">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1804">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1806">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-1806">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1808">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-1808">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-1809">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1809">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1811">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-1811">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-1812">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-1812">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1814">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1814">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-1815">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-1815">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-1816">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-1816">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-1817">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1817">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1819">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1819">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="93a62-1820">DXGI_FORMAT_R10G10B10 \_ XR \_ 偏差 \_ A2 \_ UNORM<sup>FCS</sup> (89) </span><span class="sxs-lookup"><span data-stu-id="93a62-1820">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="93a62-1821">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1821">Target</span></span> | <span data-ttu-id="93a62-1822">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1822">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-1823">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-1823">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-1824">32</span><span class="sxs-lookup"><span data-stu-id="93a62-1824">32</span></span> |
| <span data-ttu-id="93a62-1825">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1825">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1827">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-1827">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1828">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1828">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1829">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1829">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1830">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1830">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1831">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-1831">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-1832">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-1832">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1834">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-1834">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-1835">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-1835">TextureCube</span></span> | \- |
| <span data-ttu-id="93a62-1836">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-1836">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-1837">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1837">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-1838">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1838">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-1839">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1839">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-1840">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-1840">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-1841">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-1841">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-1842">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-1842">Mipmap</span></span> | \- |
| <span data-ttu-id="93a62-1843">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-1843">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-1844">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1844">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1845">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1845">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1846">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-1846">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-1847">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1847">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-1848">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1848">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1849">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1849">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1850">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-1850">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-1851">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-1851">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-1852">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1852">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-1853">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-1853">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-1854">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-1854">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-1855">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-1855">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-1856">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-1856">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-1857">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1857">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1858">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1858">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1859">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-1859">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1861">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1861">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1862">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1862">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1863">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-1863">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-1864">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-1864">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-1865">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1865">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-1866">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-1866">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1868">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-1868">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1870">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1870">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-1871">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-1871">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1873">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-1873">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1875">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1875">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1877">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1877">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="93a62-1878">DXGI_FORMAT_R11G11B10 \_ FLOAT<sup>FNS</sup> (26) </span><span class="sxs-lookup"><span data-stu-id="93a62-1878">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="93a62-1879">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1879">Target</span></span> | <span data-ttu-id="93a62-1880">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1880">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-1881">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-1881">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-1882">32</span><span class="sxs-lookup"><span data-stu-id="93a62-1882">32</span></span> |
| <span data-ttu-id="93a62-1883">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1883">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1885">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-1885">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1887">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1887">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1889">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1889">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1890">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1890">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1891">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-1891">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1893">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-1893">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1895">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-1895">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1897">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-1897">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1899">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-1899">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1901">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1901">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1903">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1903">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-1904">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1904">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-1905">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-1905">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-1906">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-1906">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-1907">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-1907">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1909">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-1909">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1911">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1911">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1913">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1913">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1915">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-1915">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-1916">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1916">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-1917">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1917">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1918">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1918">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1919">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-1919">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-1920">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-1920">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-1921">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1921">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-1922">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-1922">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-1923">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-1923">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-1924">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-1924">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-1925">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-1925">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-1926">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1926">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1927">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1927">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1928">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-1928">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1930">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1930">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1932">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1932">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1934">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-1934">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-1936">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-1936">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1938">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1938">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1940">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-1940">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-1941">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-1941">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-1942">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1942">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-1943">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-1943">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-1944">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-1944">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-1945">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1945">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-1946">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-1946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="93a62-1947">DXGI_FORMAT_R8G8B8A8 無別 \_ <sup>電腦</sup> (27) </span><span class="sxs-lookup"><span data-stu-id="93a62-1947">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="93a62-1948">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1948">Target</span></span> | <span data-ttu-id="93a62-1949">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1949">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-1950">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-1950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-1951">32</span><span class="sxs-lookup"><span data-stu-id="93a62-1951">32</span></span> |
| <span data-ttu-id="93a62-1952">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-1952">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1954">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-1954">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1955">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1955">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1956">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1956">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1957">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-1957">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-1958">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-1958">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1960">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-1960">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1962">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-1962">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1964">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-1964">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1966">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-1966">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-1967">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1967">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-1968">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1968">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-1969">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-1969">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-1970">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-1970">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-1971">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-1971">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-1972">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-1972">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1974">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-1974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-1975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1975">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1976">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1977">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-1977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-1978">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-1978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-1979">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1980">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-1980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-1981">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-1981">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-1982">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-1982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-1983">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-1984">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-1984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-1985">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-1985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-1986">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-1986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-1987">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-1987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-1988">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1989">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-1989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-1990">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-1990">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-1992">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1993">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-1993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-1994">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-1994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-1995">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-1995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-1996">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-1996">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-1997">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-1997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-1998">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-1998">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2000">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2000">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-2001">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-2001">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-2002">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-2002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-2003">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2003">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2005">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2005">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="93a62-2006">DXGI_FORMAT_R8G8B8A8 \_ UNORM 的<sup>FCS</sup> (28) </span><span class="sxs-lookup"><span data-stu-id="93a62-2006">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="93a62-2007">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2007">Target</span></span> | <span data-ttu-id="93a62-2008">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2008">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-2009">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-2009">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-2010">32</span><span class="sxs-lookup"><span data-stu-id="93a62-2010">32</span></span> |
| <span data-ttu-id="93a62-2011">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2011">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2013">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-2013">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2015">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2015">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2017">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2017">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2018">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2018">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2019">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-2019">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-2021">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-2023">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-2025">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2027">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-2027">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2029">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2029">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2031">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-2032">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-2033">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-2033">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-2034">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-2034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-2035">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-2035">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2037">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-2037">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2039">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2041">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2041">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2043">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-2043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-2044">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-2045">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2046">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2047">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-2047">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-2048">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-2048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-2049">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-2050">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-2050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-2051">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-2051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-2052">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-2052">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-2053">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-2053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-2054">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2055">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2056">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-2056">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2058">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2058">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2060">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2060">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2062">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-2062">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2064">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-2064">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2066">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2066">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2068">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-2068">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2070">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-2070">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2072">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2072">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-2073">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-2073">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2075">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-2075">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2077">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2077">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2079">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2079">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="93a62-2080">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ SRGB<sup>FCS</sup> (29) </span><span class="sxs-lookup"><span data-stu-id="93a62-2080">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="93a62-2081">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2081">Target</span></span> | <span data-ttu-id="93a62-2082">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2082">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-2083">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-2083">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-2084">32</span><span class="sxs-lookup"><span data-stu-id="93a62-2084">32</span></span> |
| <span data-ttu-id="93a62-2085">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2085">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2087">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-2087">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2088">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2088">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2089">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2089">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2090">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2090">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2091">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-2091">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2093">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-2093">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2095">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-2095">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2097">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-2097">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2099">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-2099">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2101">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2101">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2103">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2103">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-2104">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2104">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-2105">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-2105">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-2106">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-2106">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-2107">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-2107">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2109">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-2109">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2111">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2111">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2113">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2113">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2115">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-2115">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-2116">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2116">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-2117">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2117">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2118">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2118">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2119">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-2119">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-2120">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-2120">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-2121">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2121">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-2122">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-2122">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-2123">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-2123">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-2124">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-2124">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-2125">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-2125">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-2126">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2126">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2127">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2127">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2128">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-2128">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2130">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2130">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2132">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2132">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2134">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-2134">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2136">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-2136">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2138">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2138">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2140">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-2140">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2142">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-2142">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2144">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2144">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-2145">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-2145">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2147">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-2147">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2149">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2149">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2151">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2151">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="93a62-2152">DXGI_FORMAT_R8G8B8A8 \_ UINT<sup>FCS</sup> (30) </span><span class="sxs-lookup"><span data-stu-id="93a62-2152">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="93a62-2153">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2153">Target</span></span> | <span data-ttu-id="93a62-2154">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2154">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-2155">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-2155">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-2156">32</span><span class="sxs-lookup"><span data-stu-id="93a62-2156">32</span></span> |
| <span data-ttu-id="93a62-2157">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2157">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2159">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-2159">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2161">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2161">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2163">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2163">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2164">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2164">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2165">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-2165">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2167">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-2167">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2169">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-2169">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2171">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-2171">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2173">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-2173">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2175">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2175">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-2176">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2176">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-2177">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2177">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-2178">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-2178">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-2179">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-2179">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-2180">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-2180">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2182">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-2182">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-2183">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2183">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2185">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2185">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-2186">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-2186">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2188">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2188">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-2189">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2189">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2190">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2190">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2191">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-2191">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-2192">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-2192">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-2193">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2193">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-2194">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-2194">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-2195">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-2195">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-2196">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-2196">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-2197">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-2197">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-2198">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2198">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2199">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2199">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2200">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-2200">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2202">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2202">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2204">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2204">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2206">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-2206">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2208">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-2208">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-2209">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2209">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2211">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-2211">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-2212">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-2212">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2214">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2214">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-2215">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-2215">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-2216">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-2216">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-2217">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2217">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2219">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2219">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="93a62-2220">DXGI_FORMAT_R8G8B8A8 \_ SNORM 的<sup>FCS</sup> (31) </span><span class="sxs-lookup"><span data-stu-id="93a62-2220">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="93a62-2221">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2221">Target</span></span> | <span data-ttu-id="93a62-2222">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2222">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-2223">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-2223">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-2224">32</span><span class="sxs-lookup"><span data-stu-id="93a62-2224">32</span></span> |
| <span data-ttu-id="93a62-2225">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2225">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2227">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-2227">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2229">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2229">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2231">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2232">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-2233">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2235">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-2235">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2237">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-2237">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-2239">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2241">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-2241">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2243">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2243">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2245">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2245">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-2246">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2246">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-2247">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-2247">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-2248">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-2248">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-2249">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-2249">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2251">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-2251">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2253">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2253">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2255">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2255">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2257">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-2257">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-2258">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2258">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-2259">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2259">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2260">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2260">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2261">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-2261">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-2262">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-2262">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-2263">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2263">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-2264">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-2264">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-2265">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-2265">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-2266">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-2266">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-2267">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-2267">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-2268">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2268">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2269">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2269">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2270">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-2270">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2272">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2272">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2274">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2274">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2276">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-2276">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2278">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-2278">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2280">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2280">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2282">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-2282">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-2283">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-2283">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2285">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2285">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-2286">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-2286">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-2287">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-2287">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-2288">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2288">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2290">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2290">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="93a62-2291">DXGI_FORMAT_R8G8B8A8 \_ 聖的<sup>FCS</sup> (32) </span><span class="sxs-lookup"><span data-stu-id="93a62-2291">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="93a62-2292">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2292">Target</span></span> | <span data-ttu-id="93a62-2293">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2293">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-2294">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-2294">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-2295">32</span><span class="sxs-lookup"><span data-stu-id="93a62-2295">32</span></span> |
| <span data-ttu-id="93a62-2296">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2296">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2298">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-2298">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2300">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2300">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2302">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2302">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2303">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2303">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2304">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-2304">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2306">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-2306">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2308">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-2308">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2310">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-2310">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2312">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-2312">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2314">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2314">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-2315">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2315">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-2316">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2316">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-2317">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-2317">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-2318">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-2318">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-2319">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-2319">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2321">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-2321">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-2322">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2322">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2324">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2324">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-2325">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-2325">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-2326">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2326">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-2327">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2327">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2328">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2328">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2329">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-2329">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-2330">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-2330">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-2331">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2331">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-2332">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-2332">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-2333">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-2333">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-2334">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-2334">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-2335">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-2335">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-2336">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2336">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2337">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2337">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2338">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-2338">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2340">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2340">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2342">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2342">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2344">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-2344">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2346">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-2346">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-2347">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2347">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2349">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-2349">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-2350">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-2350">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2352">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2352">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-2353">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-2353">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-2354">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-2354">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-2355">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2355">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2357">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2357">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="93a62-2358">DXGI_FORMAT_R16G16 無的 \_ <sup>電腦</sup> (33) </span><span class="sxs-lookup"><span data-stu-id="93a62-2358">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="93a62-2359">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2359">Target</span></span> | <span data-ttu-id="93a62-2360">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2360">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-2361">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-2361">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-2362">32</span><span class="sxs-lookup"><span data-stu-id="93a62-2362">32</span></span> |
| <span data-ttu-id="93a62-2363">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2363">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2365">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-2365">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2366">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2366">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2367">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2367">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2368">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2368">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2369">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-2369">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2371">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-2371">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2373">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-2373">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2375">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-2375">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2377">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-2377">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-2378">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2378">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-2379">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2379">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-2380">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2380">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-2381">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-2381">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-2382">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-2382">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-2383">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-2383">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2385">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-2385">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-2386">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2386">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-2387">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2387">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-2388">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-2388">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-2389">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2389">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-2390">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2390">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2391">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2391">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2392">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-2392">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-2393">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-2393">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-2394">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2394">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-2395">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-2395">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-2396">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-2396">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-2397">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-2397">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-2398">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-2398">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-2399">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2399">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2400">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2400">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2401">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-2401">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2403">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2403">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-2404">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2404">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-2405">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-2405">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-2406">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-2406">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-2407">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2407">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-2408">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-2408">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-2409">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-2409">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2411">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2411">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-2412">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-2412">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-2413">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-2413">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-2414">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2414">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-2415">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2415">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="93a62-2416">DXGI_FORMAT_R16G16 \_ FLOAT<sup>FCS</sup> (34) </span><span class="sxs-lookup"><span data-stu-id="93a62-2416">DXGI_FORMAT_R16G16\_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="93a62-2417">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2417">Target</span></span> | <span data-ttu-id="93a62-2418">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2418">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-2419">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-2419">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-2420">32</span><span class="sxs-lookup"><span data-stu-id="93a62-2420">32</span></span> |
| <span data-ttu-id="93a62-2421">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2421">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2423">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-2423">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2425">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2425">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2427">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2427">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2428">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2428">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2429">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-2429">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2431">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-2431">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2433">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-2433">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2435">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-2435">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2437">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-2437">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2439">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2439">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2441">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-2442">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-2443">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-2443">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-2444">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-2444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-2445">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-2445">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2447">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-2447">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2449">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2449">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2451">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2451">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2453">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-2453">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-2454">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2454">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-2455">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2455">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2456">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2456">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2457">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-2457">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-2458">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-2458">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-2459">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2459">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-2460">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-2460">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-2461">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-2461">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-2462">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-2462">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-2463">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-2463">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-2464">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2464">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2465">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2465">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2466">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-2466">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2468">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2468">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2470">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2470">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2472">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-2472">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2474">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-2474">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2476">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2476">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2478">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-2478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-2479">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-2479">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2481">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-2482">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-2482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-2483">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-2483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-2484">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2484">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-2485">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2485">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="93a62-2486">DXGI_FORMAT_R16G16 \_ UNORM 的<sup>FCS</sup> (35) </span><span class="sxs-lookup"><span data-stu-id="93a62-2486">DXGI_FORMAT_R16G16\_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="93a62-2487">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2487">Target</span></span> | <span data-ttu-id="93a62-2488">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2488">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-2489">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-2489">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-2490">32</span><span class="sxs-lookup"><span data-stu-id="93a62-2490">32</span></span> |
| <span data-ttu-id="93a62-2491">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2491">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2493">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-2493">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2495">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2495">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2497">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2497">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2498">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2498">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2499">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-2499">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-2501">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2503">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-2503">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-2505">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2507">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-2507">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2509">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2509">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2511">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2511">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-2512">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2512">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-2513">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-2513">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-2514">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-2514">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-2515">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-2515">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2517">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-2517">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2519">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2519">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2521">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2521">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2523">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-2523">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-2524">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2524">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-2525">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2525">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2526">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2526">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2527">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-2527">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-2528">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-2528">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-2529">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2529">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-2530">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-2530">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-2531">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-2531">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-2532">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-2532">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-2533">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-2533">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-2534">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2534">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2535">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2535">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2536">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-2536">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2538">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2538">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2540">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2540">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2542">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-2542">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2544">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-2544">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2546">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2546">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2548">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-2548">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-2549">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-2549">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2551">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2551">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-2552">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-2552">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-2553">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-2553">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-2554">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2554">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-2555">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2555">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="93a62-2556">DXGI_FORMAT_R16G16 \_ UINT<sup>FCS</sup> (36) </span><span class="sxs-lookup"><span data-stu-id="93a62-2556">DXGI_FORMAT_R16G16\_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="93a62-2557">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2557">Target</span></span> | <span data-ttu-id="93a62-2558">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2558">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-2559">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-2559">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-2560">32</span><span class="sxs-lookup"><span data-stu-id="93a62-2560">32</span></span> |
| <span data-ttu-id="93a62-2561">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2561">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2563">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-2563">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2565">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2565">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2567">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2567">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2568">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2568">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2569">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-2569">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2571">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-2571">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2573">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-2573">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2575">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-2575">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2577">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-2577">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2579">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2579">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-2580">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2580">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-2581">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2581">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-2582">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-2582">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-2583">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-2583">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-2584">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-2584">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2586">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-2586">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-2587">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2587">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2589">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2589">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-2590">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-2590">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2592">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2592">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-2593">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2593">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2594">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2594">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2595">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-2595">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-2596">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-2596">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-2597">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2597">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-2598">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-2598">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-2599">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-2599">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-2600">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-2600">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-2601">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-2601">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-2602">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2602">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2603">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2603">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2604">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-2604">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2606">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2606">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2608">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2608">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2610">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-2610">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2612">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-2612">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-2613">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2613">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2615">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-2615">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-2616">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-2616">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2618">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2618">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-2619">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-2619">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-2620">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-2620">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-2621">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2621">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-2622">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2622">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="93a62-2623">DXGI_FORMAT_R16G16 \_ SNORM 的<sup>FCS</sup> (37) </span><span class="sxs-lookup"><span data-stu-id="93a62-2623">DXGI_FORMAT_R16G16\_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="93a62-2624">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2624">Target</span></span> | <span data-ttu-id="93a62-2625">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2625">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-2626">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-2626">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-2627">32</span><span class="sxs-lookup"><span data-stu-id="93a62-2627">32</span></span> |
| <span data-ttu-id="93a62-2628">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2628">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2630">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-2630">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2632">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2632">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2634">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2634">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2635">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2635">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2636">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-2636">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2638">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-2638">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2640">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-2640">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2642">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-2642">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2644">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-2644">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2646">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2646">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2648">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2648">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-2649">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2649">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-2650">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-2650">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-2651">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-2651">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-2652">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-2652">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2654">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-2654">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2656">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2656">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2658">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2658">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2660">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-2660">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-2661">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2661">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-2662">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2662">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2663">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2663">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2664">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-2664">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-2665">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-2665">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-2666">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2666">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-2667">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-2667">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-2668">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-2668">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-2669">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-2669">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-2670">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-2670">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-2671">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2671">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2672">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2672">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2673">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-2673">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2675">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2675">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2677">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2677">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2679">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-2679">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2681">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-2681">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2683">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2683">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2685">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-2685">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-2686">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-2686">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2688">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2688">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-2689">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-2689">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-2690">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-2690">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-2691">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2691">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-2692">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2692">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="93a62-2693">DXGI_FORMAT_R16G16 \_ 聖的<sup>FCS</sup> (38) </span><span class="sxs-lookup"><span data-stu-id="93a62-2693">DXGI_FORMAT_R16G16\_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="93a62-2694">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2694">Target</span></span> | <span data-ttu-id="93a62-2695">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2695">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-2696">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-2696">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-2697">32</span><span class="sxs-lookup"><span data-stu-id="93a62-2697">32</span></span> |
| <span data-ttu-id="93a62-2698">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2698">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2700">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-2700">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2702">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2702">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2704">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2704">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2705">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2705">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2706">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-2706">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2708">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-2708">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2710">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-2710">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2712">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-2712">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2714">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-2714">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2716">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2716">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-2717">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2717">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-2718">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2718">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-2719">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-2719">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-2720">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-2720">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-2721">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-2721">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2723">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-2723">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-2724">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2724">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2726">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2726">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-2727">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-2727">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-2728">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2728">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-2729">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2729">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2730">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2730">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2731">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-2731">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-2732">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-2732">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-2733">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2733">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-2734">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-2734">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-2735">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-2735">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-2736">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-2736">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-2737">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-2737">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-2738">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2738">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2739">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2739">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2740">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-2740">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2742">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2742">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2744">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2744">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2746">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-2746">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2748">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-2748">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-2749">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2749">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2751">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-2751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-2752">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-2752">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2754">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2754">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-2755">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-2755">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-2756">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-2756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-2757">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2757">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-2758">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2758">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="93a62-2759">DXGI_FORMAT_R32 無的 \_ <sup>電腦</sup> (39) </span><span class="sxs-lookup"><span data-stu-id="93a62-2759">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="93a62-2760">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2760">Target</span></span> | <span data-ttu-id="93a62-2761">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2761">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-2762">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-2762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-2763">32</span><span class="sxs-lookup"><span data-stu-id="93a62-2763">32</span></span> |
| <span data-ttu-id="93a62-2764">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2764">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2766">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-2766">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2767">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2767">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2768">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2768">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2769">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2769">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2770">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-2770">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2772">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-2772">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-2774">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2776">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-2776">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2778">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-2778">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-2779">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2779">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-2780">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2780">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-2781">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2781">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-2782">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-2782">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-2783">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-2783">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-2784">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-2784">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2786">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-2786">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-2787">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2787">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-2788">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2788">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-2789">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-2789">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-2790">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2790">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-2791">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2791">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2792">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2792">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2793">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-2793">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-2794">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-2794">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-2795">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2795">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-2796">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-2796">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-2797">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-2797">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-2798">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-2798">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-2799">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-2799">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-2800">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2800">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2801">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2801">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2802">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-2802">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2804">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2804">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-2805">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2805">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-2806">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-2806">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-2807">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-2807">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-2808">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2808">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-2809">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-2809">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-2810">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-2810">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2812">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2812">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-2813">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-2813">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-2814">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-2814">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-2815">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2815">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2817">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2817">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="93a62-2818">DXGI_FORMAT_D32 \_ FLOAT<sup>FCS</sup> (40) </span><span class="sxs-lookup"><span data-stu-id="93a62-2818">DXGI_FORMAT_D32\_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="93a62-2819">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2819">Target</span></span> | <span data-ttu-id="93a62-2820">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2820">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-2821">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-2821">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-2822">32</span><span class="sxs-lookup"><span data-stu-id="93a62-2822">32</span></span> |
| <span data-ttu-id="93a62-2823">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2823">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2825">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-2825">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2826">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2826">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2827">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2827">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2828">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2828">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2829">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-2829">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2831">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-2831">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2833">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-2833">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-2834">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-2834">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2836">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-2836">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-2837">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2837">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-2838">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2838">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-2839">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2839">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-2840">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-2840">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-2841">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-2841">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-2842">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-2842">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2844">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-2844">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-2845">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2845">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-2846">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2846">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-2847">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-2847">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-2848">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2848">Depth/Stencil Target</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2850">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2850">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2851">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2851">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2852">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-2852">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-2853">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-2853">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-2854">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2854">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-2855">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-2855">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-2856">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-2856">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-2857">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-2857">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-2858">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-2858">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-2859">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2859">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2860">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2860">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2861">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-2861">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2863">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2863">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2865">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2865">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2867">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-2867">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2869">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-2869">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-2870">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2870">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-2871">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-2871">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-2872">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-2872">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2874">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2874">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-2875">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-2875">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-2876">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-2876">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-2877">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2877">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2879">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2879">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="93a62-2880">DXGI_FORMAT_R32 \_ FLOAT<sup>FCS</sup> (41) </span><span class="sxs-lookup"><span data-stu-id="93a62-2880">DXGI_FORMAT_R32\_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="93a62-2881">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2881">Target</span></span> | <span data-ttu-id="93a62-2882">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2882">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-2883">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-2883">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-2884">32</span><span class="sxs-lookup"><span data-stu-id="93a62-2884">32</span></span> |
| <span data-ttu-id="93a62-2885">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2885">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2887">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-2887">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2889">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2889">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2891">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2891">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-2892">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2892">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2894">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-2894">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2896">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-2896">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2898">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-2898">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2900">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-2900">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2902">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-2902">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2904">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2904">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2906">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2906">Shader sample\_c (comparison filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2908">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2908">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-2909">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-2909">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2911">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-2911">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-2912">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-2912">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2914">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-2914">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2916">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2916">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2918">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2918">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2920">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-2920">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-2921">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2921">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-2922">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2922">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2923">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2923">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2924">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-2924">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-2925">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-2925">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-2926">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2926">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-2927">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-2927">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-2928">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-2928">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-2929">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-2929">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-2930">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-2930">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-2931">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2931">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2932">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-2932">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-2933">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-2933">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2935">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2935">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2937">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2937">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2939">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-2939">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2941">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-2941">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2943">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2943">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2945">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-2945">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-2946">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-2946">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2948">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2948">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-2949">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-2949">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-2950">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-2950">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-2951">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2951">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2953">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-2953">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="93a62-2954">DXGI_FORMAT_R32 \_ UINT<sup>FCS</sup> (42) </span><span class="sxs-lookup"><span data-stu-id="93a62-2954">DXGI_FORMAT_R32\_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="93a62-2955">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2955">Target</span></span> | <span data-ttu-id="93a62-2956">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2956">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-2957">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-2957">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-2958">32</span><span class="sxs-lookup"><span data-stu-id="93a62-2958">32</span></span> |
| <span data-ttu-id="93a62-2959">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-2959">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2961">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-2961">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2963">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2963">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2965">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2965">Input Assembler Index Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2967">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-2967">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2969">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-2969">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2971">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-2971">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2973">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-2973">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2975">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-2975">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2977">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-2977">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2979">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2979">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-2980">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2980">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-2981">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-2981">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-2982">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-2982">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-2983">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-2983">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-2984">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-2984">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2986">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-2986">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-2987">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2987">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-2989">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-2989">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-2990">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-2990">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-2992">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-2992">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-2993">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2993">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2994">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-2994">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-2995">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-2995">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-2996">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-2996">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-2997">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-2997">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-2998">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-2998">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-2999">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-2999">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-3000">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-3000">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-3001">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-3001">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-3002">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3002">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3003">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3003">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3004">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-3004">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3006">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3006">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3008">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3008">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3010">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-3010">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3012">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-3012">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-3013">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3013">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3015">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-3015">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-3016">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-3016">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3018">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3018">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-3019">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-3019">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-3020">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-3020">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-3021">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3021">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3023">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3023">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="93a62-3024">DXGI_FORMAT_R32 \_ 聖的<sup>FCS</sup> (43) </span><span class="sxs-lookup"><span data-stu-id="93a62-3024">DXGI_FORMAT_R32\_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="93a62-3025">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3025">Target</span></span> | <span data-ttu-id="93a62-3026">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3026">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-3027">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-3027">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-3028">32</span><span class="sxs-lookup"><span data-stu-id="93a62-3028">32</span></span> |
| <span data-ttu-id="93a62-3029">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3029">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3031">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-3031">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3033">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3033">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3035">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3035">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3036">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3036">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3038">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-3038">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3040">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-3040">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3042">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-3042">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3044">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-3044">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3046">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-3046">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3048">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3048">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-3049">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3049">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-3050">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3050">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-3051">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-3051">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-3052">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-3052">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-3053">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-3053">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3055">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-3055">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-3056">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3056">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3058">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3058">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3059">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-3059">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-3060">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3060">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-3061">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3061">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3062">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3062">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3063">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-3063">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-3064">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-3064">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-3065">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3065">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-3066">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-3066">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-3067">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-3067">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-3068">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-3068">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-3069">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-3069">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-3070">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3070">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3071">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3071">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3072">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-3072">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3074">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3074">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3076">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3076">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3078">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-3078">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3080">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-3080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-3081">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3081">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3083">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-3083">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-3084">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-3084">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3086">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3086">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-3087">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-3087">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-3088">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-3088">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-3089">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3089">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3091">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3091">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="93a62-3092">DXGI_FORMAT_R24G8 無的 \_ <sup>電腦</sup> (44) </span><span class="sxs-lookup"><span data-stu-id="93a62-3092">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="93a62-3093">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3093">Target</span></span> | <span data-ttu-id="93a62-3094">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3094">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-3095">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-3095">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-3096">32</span><span class="sxs-lookup"><span data-stu-id="93a62-3096">32</span></span> |
| <span data-ttu-id="93a62-3097">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3097">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3099">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-3099">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3100">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3100">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3101">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3101">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3102">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3102">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3103">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-3103">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3105">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-3105">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3107">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-3107">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-3108">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-3108">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3110">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-3110">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-3111">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3111">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-3112">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3112">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-3113">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3113">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-3114">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-3114">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-3115">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-3115">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-3116">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-3116">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3118">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-3118">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-3119">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3119">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3120">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3120">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3121">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-3121">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-3122">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3122">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-3123">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3123">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3124">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3124">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3125">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-3125">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-3126">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-3126">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-3127">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3127">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-3128">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-3128">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-3129">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-3129">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-3130">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-3130">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-3131">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-3131">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-3132">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3132">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3133">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3133">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3134">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-3134">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3136">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3136">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3137">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3137">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3138">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-3138">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-3139">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-3139">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-3140">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3140">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-3141">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-3141">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-3142">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-3142">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3144">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3144">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-3145">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-3145">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-3146">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-3146">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-3147">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3147">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-3148">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3148">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a><span data-ttu-id="93a62-3149">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FCS</sup> (45) </span><span class="sxs-lookup"><span data-stu-id="93a62-3149">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FCS</sup> (45)</span></span>
| <span data-ttu-id="93a62-3150">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3150">Target</span></span> | <span data-ttu-id="93a62-3151">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3151">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-3152">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-3152">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-3153">32</span><span class="sxs-lookup"><span data-stu-id="93a62-3153">32</span></span> |
| <span data-ttu-id="93a62-3154">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3154">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3156">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-3156">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3157">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3157">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3158">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3158">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3159">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3159">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3160">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-3160">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3162">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-3162">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3164">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-3164">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-3165">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-3165">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3167">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-3167">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-3168">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3168">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-3169">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3169">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-3170">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3170">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-3171">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-3171">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-3172">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-3172">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-3173">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-3173">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3175">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-3175">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-3176">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3176">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3177">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3177">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3178">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-3178">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-3179">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3179">Depth/Stencil Target</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3181">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3181">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3182">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3182">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3183">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-3183">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-3184">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-3184">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-3185">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3185">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-3186">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-3186">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-3187">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-3187">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-3188">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-3188">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-3189">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-3189">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-3190">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3190">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3191">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3191">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3192">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-3192">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3194">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3194">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3196">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3196">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3198">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-3198">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3200">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-3200">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-3201">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3201">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-3202">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-3202">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-3203">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-3203">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3205">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3205">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-3206">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-3206">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-3207">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-3207">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-3208">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3208">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-3209">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3209">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a><span data-ttu-id="93a62-3210">DXGI_FORMAT_R24 \_ UNORM \_ X8 \_ 無<sup></sup> (的 46) </span><span class="sxs-lookup"><span data-stu-id="93a62-3210">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FCS</sup> (46)</span></span>
| <span data-ttu-id="93a62-3211">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3211">Target</span></span> | <span data-ttu-id="93a62-3212">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3212">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-3213">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-3213">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-3214">32</span><span class="sxs-lookup"><span data-stu-id="93a62-3214">32</span></span> |
| <span data-ttu-id="93a62-3215">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3215">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3217">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-3217">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3218">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3218">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3219">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3219">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3220">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3220">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3221">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-3221">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3223">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-3223">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3225">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-3225">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-3226">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-3226">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3228">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-3228">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3230">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3230">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3232">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3232">Shader sample\_c (comparison filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3234">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3234">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-3235">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-3235">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3237">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-3237">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-3238">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-3238">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3240">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-3240">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-3241">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3241">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3242">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3242">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3243">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-3243">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-3244">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3244">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-3245">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3245">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3246">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3246">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3247">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-3247">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-3248">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-3248">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-3249">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3249">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-3250">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-3250">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-3251">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-3251">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-3252">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-3252">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-3253">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-3253">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-3254">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3254">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3255">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3255">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3256">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-3256">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3258">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3258">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3259">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3259">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3260">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-3260">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-3261">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-3261">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-3262">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3262">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3264">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-3264">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-3265">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-3265">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3267">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3267">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-3268">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-3268">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-3269">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-3269">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-3270">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3270">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-3271">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3271">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a><span data-ttu-id="93a62-3272">DXGI_FORMAT_X24 無別 \_ \_ G8 \_ UINT<sup>FCS</sup> (47) </span><span class="sxs-lookup"><span data-stu-id="93a62-3272">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FCS</sup> (47)</span></span>
| <span data-ttu-id="93a62-3273">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3273">Target</span></span> | <span data-ttu-id="93a62-3274">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3274">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-3275">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-3275">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-3276">32</span><span class="sxs-lookup"><span data-stu-id="93a62-3276">32</span></span> |
| <span data-ttu-id="93a62-3277">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3277">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3279">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-3279">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3280">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3281">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3282">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-3283">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3285">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-3285">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3287">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-3287">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-3288">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-3288">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3290">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-3290">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3292">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3292">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-3293">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3293">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-3294">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3294">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-3295">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-3295">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-3296">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-3296">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-3297">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-3297">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3299">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-3299">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-3300">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3300">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3301">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3302">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-3302">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-3303">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-3304">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3305">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3306">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-3306">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-3307">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-3307">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-3308">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3308">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-3309">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-3309">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-3310">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-3310">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-3311">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-3311">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-3312">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-3312">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-3313">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3313">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3314">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3314">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3315">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-3315">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3317">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3318">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3319">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-3319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-3320">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-3320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-3321">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3321">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3323">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-3323">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-3324">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-3324">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3326">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3326">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-3327">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-3327">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-3328">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-3328">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-3329">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3329">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-3330">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3330">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="93a62-3331">DXGI_FORMAT_R8G8 無的 \_ <sup>電腦</sup> (48) </span><span class="sxs-lookup"><span data-stu-id="93a62-3331">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="93a62-3332">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3332">Target</span></span> | <span data-ttu-id="93a62-3333">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3333">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-3334">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-3334">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-3335">16</span><span class="sxs-lookup"><span data-stu-id="93a62-3335">16</span></span> |
| <span data-ttu-id="93a62-3336">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3336">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3338">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-3338">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3339">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3339">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3340">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3340">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3341">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3341">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3342">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-3342">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3344">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-3344">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3346">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-3346">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-3348">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3350">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-3350">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-3351">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3351">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-3352">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3352">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-3353">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3353">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-3354">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-3354">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-3355">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-3355">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-3356">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-3356">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3358">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-3358">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-3359">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3359">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3360">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3360">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3361">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-3361">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-3362">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3362">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-3363">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3363">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3364">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3364">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3365">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-3365">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-3366">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-3366">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-3367">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3367">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-3368">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-3368">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-3369">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-3369">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-3370">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-3370">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-3371">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-3371">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-3372">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3372">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3373">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3373">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3374">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-3374">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3376">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3376">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3377">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3377">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3378">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-3378">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-3379">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-3379">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-3380">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3380">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-3381">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-3381">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-3382">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-3382">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3384">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-3385">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-3385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-3386">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-3386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-3387">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3387">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-3388">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3388">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="93a62-3389">DXGI_FORMAT_R8G8 \_ UNORM 的<sup>FCS</sup> (49) </span><span class="sxs-lookup"><span data-stu-id="93a62-3389">DXGI_FORMAT_R8G8\_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="93a62-3390">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3390">Target</span></span> | <span data-ttu-id="93a62-3391">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3391">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-3392">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-3392">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-3393">16</span><span class="sxs-lookup"><span data-stu-id="93a62-3393">16</span></span> |
| <span data-ttu-id="93a62-3394">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3394">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3396">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-3396">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3398">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3398">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3400">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3400">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3401">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3401">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3402">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-3402">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-3404">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3406">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-3406">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3408">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-3408">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3410">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-3410">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3412">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3412">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3414">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-3415">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-3416">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-3416">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-3417">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-3417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-3418">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-3418">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3420">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-3420">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3422">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3424">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3424">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3426">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-3426">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-3427">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3427">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-3428">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3428">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3429">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3429">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3430">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-3430">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-3431">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-3431">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-3432">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3432">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-3433">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-3433">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-3434">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-3434">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-3435">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-3435">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-3436">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-3436">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-3437">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3437">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3438">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3438">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3439">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-3439">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3441">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3441">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3443">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3443">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3445">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-3445">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3447">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-3447">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3449">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3449">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3451">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-3451">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-3452">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-3452">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3454">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3454">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-3455">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-3455">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-3456">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-3456">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-3457">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3457">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3459">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3459">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="93a62-3460">DXGI_FORMAT_R8G8 \_ UINT<sup>FCS</sup> (50) </span><span class="sxs-lookup"><span data-stu-id="93a62-3460">DXGI_FORMAT_R8G8\_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="93a62-3461">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3461">Target</span></span> | <span data-ttu-id="93a62-3462">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3462">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-3463">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-3463">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-3464">16</span><span class="sxs-lookup"><span data-stu-id="93a62-3464">16</span></span> |
| <span data-ttu-id="93a62-3465">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3465">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3467">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-3467">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3469">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3469">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3471">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3471">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3472">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3472">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3473">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-3473">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3475">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-3475">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3477">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-3477">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3479">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-3479">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3481">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-3481">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3483">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3483">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-3484">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3484">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-3485">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3485">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-3486">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-3486">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-3487">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-3487">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-3488">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-3488">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3490">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-3490">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-3491">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3491">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3493">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3493">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3494">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-3494">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3496">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3496">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-3497">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3497">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3498">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3498">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3499">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-3499">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-3500">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-3500">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-3501">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3501">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-3502">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-3502">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-3503">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-3503">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-3504">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-3504">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-3505">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-3505">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-3506">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3506">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3507">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3507">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3508">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-3508">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3510">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3510">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3512">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3512">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3514">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-3514">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3516">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-3516">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-3517">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3517">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3519">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-3519">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-3520">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-3520">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3522">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3522">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-3523">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-3523">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-3524">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-3524">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-3525">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3525">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-3526">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3526">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="93a62-3527">DXGI_FORMAT_R8G8 \_ SNORM 的<sup>FCS</sup> (51) </span><span class="sxs-lookup"><span data-stu-id="93a62-3527">DXGI_FORMAT_R8G8\_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="93a62-3528">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3528">Target</span></span> | <span data-ttu-id="93a62-3529">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3529">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-3530">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-3530">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-3531">16</span><span class="sxs-lookup"><span data-stu-id="93a62-3531">16</span></span> |
| <span data-ttu-id="93a62-3532">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3532">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3534">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-3534">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3536">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3536">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3538">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3538">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3539">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3539">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3540">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-3540">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3542">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-3542">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3544">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-3544">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3546">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-3546">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3548">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-3548">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3550">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3550">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3552">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3552">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-3553">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3553">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-3554">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-3554">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-3555">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-3555">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-3556">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-3556">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3558">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-3558">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3560">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3560">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3562">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3562">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3564">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-3564">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-3565">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-3566">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3567">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3568">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-3568">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-3569">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-3569">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-3570">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3570">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-3571">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-3571">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-3572">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-3572">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-3573">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-3573">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-3574">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-3574">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-3575">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3575">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3576">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3576">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3577">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-3577">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3579">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3579">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3581">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3581">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3583">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-3583">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3585">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-3585">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3587">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3587">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3589">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-3589">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-3590">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-3590">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3592">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3592">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-3593">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-3593">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-3594">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-3594">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-3595">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3595">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-3596">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3596">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="93a62-3597">DXGI_FORMAT_R8G8 \_ 聖的<sup>FCS</sup> (52) </span><span class="sxs-lookup"><span data-stu-id="93a62-3597">DXGI_FORMAT_R8G8\_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="93a62-3598">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3598">Target</span></span> | <span data-ttu-id="93a62-3599">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3599">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-3600">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-3600">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-3601">16</span><span class="sxs-lookup"><span data-stu-id="93a62-3601">16</span></span> |
| <span data-ttu-id="93a62-3602">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3602">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3604">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-3604">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3606">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3606">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3608">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3608">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3609">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3609">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3610">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-3610">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3612">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-3612">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3614">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-3614">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3616">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-3616">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3618">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-3618">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3620">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3620">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-3621">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3621">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-3622">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3622">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-3623">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-3623">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-3624">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-3624">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-3625">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-3625">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3627">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-3627">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-3628">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3628">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3630">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3630">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3631">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-3631">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-3632">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3632">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-3633">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3633">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3634">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3634">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3635">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-3635">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-3636">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-3636">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-3637">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3637">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-3638">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-3638">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-3639">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-3639">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-3640">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-3640">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-3641">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-3641">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-3642">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3642">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3643">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3643">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3644">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-3644">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3646">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3646">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3648">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3648">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3650">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-3650">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3652">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-3652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-3653">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3653">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3655">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-3655">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-3656">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-3656">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3658">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3658">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-3659">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-3659">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-3660">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-3660">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-3661">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3661">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-3662">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3662">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="93a62-3663">DXGI_FORMAT_R16 無的 \_ <sup>電腦</sup> (53) </span><span class="sxs-lookup"><span data-stu-id="93a62-3663">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="93a62-3664">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3664">Target</span></span> | <span data-ttu-id="93a62-3665">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3665">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-3666">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-3666">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-3667">16</span><span class="sxs-lookup"><span data-stu-id="93a62-3667">16</span></span> |
| <span data-ttu-id="93a62-3668">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3668">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3670">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-3670">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3671">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3671">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3672">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3672">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3673">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3673">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3674">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-3674">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3676">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-3676">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3678">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-3678">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3680">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-3680">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3682">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-3682">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-3683">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3683">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-3684">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3684">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-3685">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3685">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-3686">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-3686">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-3687">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-3687">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-3688">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-3688">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3690">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-3690">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-3691">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3691">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3692">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3692">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3693">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-3693">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-3694">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3694">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-3695">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3695">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3696">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3696">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3697">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-3697">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-3698">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-3698">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-3699">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3699">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-3700">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-3700">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-3701">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-3701">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-3702">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-3702">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-3703">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-3703">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-3704">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3704">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3705">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3705">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3706">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-3706">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3708">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3708">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3709">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3709">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3710">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-3710">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-3711">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-3711">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-3712">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3712">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-3713">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-3713">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-3714">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-3714">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3716">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3716">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-3717">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-3717">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-3718">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-3718">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-3719">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3719">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3721">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3721">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="93a62-3722">DXGI_FORMAT_R16 \_ FLOAT<sup>FCS</sup> (54) </span><span class="sxs-lookup"><span data-stu-id="93a62-3722">DXGI_FORMAT_R16\_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="93a62-3723">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3723">Target</span></span> | <span data-ttu-id="93a62-3724">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3724">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-3725">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-3725">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-3726">16</span><span class="sxs-lookup"><span data-stu-id="93a62-3726">16</span></span> |
| <span data-ttu-id="93a62-3727">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3727">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3729">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-3729">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3731">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3731">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3733">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3733">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3734">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3734">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3735">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-3735">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3737">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-3737">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3739">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-3739">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3741">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-3741">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3743">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-3743">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3745">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3745">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3747">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3747">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-3748">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3748">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-3749">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-3749">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3751">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-3751">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-3752">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-3752">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3754">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-3754">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3756">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3756">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3758">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3758">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3760">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-3760">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-3761">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3761">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-3762">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3762">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3763">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3763">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3764">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-3764">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-3765">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-3765">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-3766">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3766">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-3767">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-3767">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-3768">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-3768">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-3769">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-3769">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-3770">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-3770">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-3771">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3771">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3772">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3772">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3773">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-3773">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3775">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3775">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3777">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3777">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3779">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-3779">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3781">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-3781">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3783">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3783">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3785">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-3785">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-3786">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-3786">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3788">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3788">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-3789">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-3789">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-3790">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-3790">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-3791">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3791">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3793">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3793">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="93a62-3794">DXGI_FORMAT_D16 \_ UNORM 的<sup>FCS</sup> (55) </span><span class="sxs-lookup"><span data-stu-id="93a62-3794">DXGI_FORMAT_D16\_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="93a62-3795">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3795">Target</span></span> | <span data-ttu-id="93a62-3796">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3796">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-3797">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-3797">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-3798">16</span><span class="sxs-lookup"><span data-stu-id="93a62-3798">16</span></span> |
| <span data-ttu-id="93a62-3799">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3799">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3801">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-3801">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3802">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3802">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3803">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3803">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3804">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3804">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3805">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-3805">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3807">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-3807">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3809">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-3809">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-3810">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-3810">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3812">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-3812">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-3813">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3813">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-3814">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3814">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-3815">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3815">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-3816">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-3816">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-3817">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-3817">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-3818">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-3818">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3820">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-3820">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-3821">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3821">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3822">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3822">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3823">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-3823">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-3824">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3824">Depth/Stencil Target</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3826">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3826">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3827">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3827">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3828">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-3828">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-3829">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-3829">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-3830">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3830">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-3831">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-3831">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-3832">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-3832">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-3833">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-3833">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-3834">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-3834">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-3835">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3835">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3836">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3836">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3837">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-3837">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3839">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3839">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3841">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3841">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3843">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-3843">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3845">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-3845">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-3846">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3846">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-3847">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-3847">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-3848">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-3848">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3850">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3850">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-3851">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-3851">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-3852">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-3852">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-3853">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3853">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3855">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3855">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="93a62-3856">DXGI_FORMAT_R16 \_ UNORM 的<sup>FCS</sup> (56) </span><span class="sxs-lookup"><span data-stu-id="93a62-3856">DXGI_FORMAT_R16\_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="93a62-3857">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3857">Target</span></span> | <span data-ttu-id="93a62-3858">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3858">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-3859">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-3859">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-3860">16</span><span class="sxs-lookup"><span data-stu-id="93a62-3860">16</span></span> |
| <span data-ttu-id="93a62-3861">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3861">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3863">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-3863">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3865">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3865">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3867">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3867">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3868">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3868">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3869">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-3869">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3871">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-3871">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3873">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-3873">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3875">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-3875">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3877">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-3877">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3879">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3879">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3881">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3881">Shader sample\_c (comparison filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3883">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3883">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-3884">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-3884">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3886">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-3886">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-3887">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-3887">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3889">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-3889">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3891">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3891">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3893">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3893">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3895">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-3895">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-3896">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3896">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-3897">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3897">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3898">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3898">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3899">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-3899">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-3900">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-3900">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-3901">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3901">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-3902">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-3902">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-3903">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-3903">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-3904">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-3904">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-3905">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-3905">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-3906">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3906">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3907">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3907">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3908">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-3908">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3910">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3910">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3912">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3912">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3914">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-3914">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3916">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-3916">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3918">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3918">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3920">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-3920">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-3921">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-3921">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3923">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3923">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-3924">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-3924">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-3925">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-3925">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-3926">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3926">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3928">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="93a62-3929">DXGI_FORMAT_R16 \_ UINT<sup>FCS</sup> (57) </span><span class="sxs-lookup"><span data-stu-id="93a62-3929">DXGI_FORMAT_R16\_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="93a62-3930">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3930">Target</span></span> | <span data-ttu-id="93a62-3931">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3931">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-3932">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-3932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-3933">16</span><span class="sxs-lookup"><span data-stu-id="93a62-3933">16</span></span> |
| <span data-ttu-id="93a62-3934">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3934">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3936">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-3936">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3938">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3938">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3940">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3940">Input Assembler Index Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3942">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-3942">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-3943">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-3943">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3945">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-3945">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3947">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-3947">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3949">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-3949">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3951">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-3951">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3953">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3953">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-3954">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3954">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-3955">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-3955">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-3956">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-3956">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-3957">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-3957">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-3958">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-3958">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3960">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-3960">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-3961">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3961">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3963">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3963">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-3964">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-3964">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3966">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3966">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-3967">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3967">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3968">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-3968">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-3969">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-3969">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-3970">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-3970">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-3971">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3971">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-3972">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-3972">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-3973">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-3973">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-3974">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-3974">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-3975">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-3975">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-3976">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3976">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3977">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-3977">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-3978">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-3978">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3980">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3980">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3982">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-3982">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3984">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-3984">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-3986">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-3986">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-3987">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-3987">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3989">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-3989">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-3990">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-3990">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3992">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-3992">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-3993">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-3993">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-3994">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-3994">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-3995">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3995">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-3997">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-3997">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="93a62-3998">DXGI_FORMAT_R16 \_ SNORM 的<sup>FCS</sup> (58) </span><span class="sxs-lookup"><span data-stu-id="93a62-3998">DXGI_FORMAT_R16\_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="93a62-3999">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-3999">Target</span></span> | <span data-ttu-id="93a62-4000">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4000">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-4001">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-4001">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-4002">16</span><span class="sxs-lookup"><span data-stu-id="93a62-4002">16</span></span> |
| <span data-ttu-id="93a62-4003">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4003">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4005">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-4005">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4007">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4007">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4009">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4009">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4010">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4010">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4011">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-4011">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4013">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-4013">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4015">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-4015">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4017">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-4017">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4019">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-4019">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4021">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4021">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4023">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4023">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-4024">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4024">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-4025">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-4025">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4027">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-4027">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-4028">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-4028">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4030">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-4030">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4032">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4032">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4034">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4034">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4036">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-4036">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-4037">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4037">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-4038">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4038">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4039">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4039">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4040">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-4040">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-4041">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-4041">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-4042">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4042">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-4043">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-4043">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-4044">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-4044">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-4045">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-4045">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-4046">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-4046">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-4047">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4047">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4048">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4048">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4049">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-4049">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4051">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4051">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4053">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4053">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-4055">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-4055">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-4057">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-4057">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4059">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4059">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4061">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-4061">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-4062">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-4062">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4064">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4064">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-4065">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-4065">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-4066">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-4066">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-4067">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4067">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4069">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4069">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="93a62-4070">DXGI_FORMAT_R16 \_ 聖的<sup>FCS</sup> (59) </span><span class="sxs-lookup"><span data-stu-id="93a62-4070">DXGI_FORMAT_R16\_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="93a62-4071">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4071">Target</span></span> | <span data-ttu-id="93a62-4072">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4072">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-4073">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-4073">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-4074">16</span><span class="sxs-lookup"><span data-stu-id="93a62-4074">16</span></span> |
| <span data-ttu-id="93a62-4075">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4075">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4077">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-4077">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4079">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4079">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4081">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4081">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4082">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4082">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4083">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-4083">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4085">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-4085">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4087">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-4087">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4089">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-4089">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4091">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-4091">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4093">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4093">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-4094">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4094">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-4095">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4095">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-4096">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-4096">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-4097">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-4097">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-4098">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-4098">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4100">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-4100">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-4101">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4101">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4103">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4103">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4104">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-4104">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-4105">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4105">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-4106">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4106">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4107">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4107">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4108">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-4108">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-4109">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-4109">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-4110">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4110">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-4111">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-4111">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-4112">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-4112">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-4113">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-4113">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-4114">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-4114">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-4115">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4115">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4116">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4116">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4117">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-4117">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4119">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4119">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4121">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4121">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-4123">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-4123">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-4125">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-4125">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-4126">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4126">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4128">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-4128">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-4129">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-4129">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4131">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4131">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-4132">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-4132">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-4133">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-4133">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-4134">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4134">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4136">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4136">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="93a62-4137">DXGI_FORMAT_R8 無的 \_ <sup>電腦</sup> (60) </span><span class="sxs-lookup"><span data-stu-id="93a62-4137">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="93a62-4138">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4138">Target</span></span> | <span data-ttu-id="93a62-4139">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4139">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-4140">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-4140">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-4141">8</span><span class="sxs-lookup"><span data-stu-id="93a62-4141">8</span></span> |
| <span data-ttu-id="93a62-4142">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4142">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4144">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-4144">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4145">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4145">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4146">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4146">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4147">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4147">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4148">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-4148">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4150">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-4150">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4152">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-4152">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4154">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-4154">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4156">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-4156">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-4157">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4157">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-4158">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4158">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-4159">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4159">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-4160">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-4160">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-4161">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-4161">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-4162">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-4162">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4164">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-4164">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-4165">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4165">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4166">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4166">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4167">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-4167">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-4168">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4168">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-4169">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4169">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4170">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4170">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4171">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-4171">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-4172">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-4172">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-4173">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4173">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-4174">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-4174">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-4175">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-4175">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-4176">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-4176">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-4177">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-4177">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-4178">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4178">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4179">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4179">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4180">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-4180">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4182">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4182">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4183">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4183">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4184">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-4184">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-4185">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-4185">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-4186">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4186">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-4187">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-4187">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-4188">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-4188">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4190">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4190">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-4191">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-4191">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-4192">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-4192">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-4193">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4193">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4195">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4195">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="93a62-4196">DXGI_FORMAT_R8 \_ UNORM 的<sup>FCS</sup> (61) </span><span class="sxs-lookup"><span data-stu-id="93a62-4196">DXGI_FORMAT_R8\_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="93a62-4197">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4197">Target</span></span> | <span data-ttu-id="93a62-4198">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4198">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-4199">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-4199">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-4200">8</span><span class="sxs-lookup"><span data-stu-id="93a62-4200">8</span></span> |
| <span data-ttu-id="93a62-4201">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4201">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4203">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-4203">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4205">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4205">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4207">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4207">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4208">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4208">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4209">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-4209">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4211">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-4211">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4213">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-4213">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4215">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-4215">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4217">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-4217">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4219">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4219">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4221">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4221">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-4222">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4222">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-4223">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-4223">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4225">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-4225">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-4226">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-4226">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4228">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-4228">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4230">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4230">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4232">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4232">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4234">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-4234">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-4235">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4235">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-4236">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4236">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4237">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4237">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4238">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-4238">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-4239">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-4239">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-4240">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4240">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-4241">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-4241">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-4242">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-4242">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-4243">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-4243">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-4244">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-4244">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-4245">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4245">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4246">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4246">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4247">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-4247">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4249">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4249">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4251">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4251">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-4253">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-4253">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-4255">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-4255">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4257">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4257">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4259">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-4259">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-4260">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-4260">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4262">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4262">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-4263">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-4263">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-4264">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-4264">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-4265">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4265">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4267">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4267">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="93a62-4268">DXGI_FORMAT_R8 \_ UINT<sup>FCS</sup> (62) </span><span class="sxs-lookup"><span data-stu-id="93a62-4268">DXGI_FORMAT_R8\_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="93a62-4269">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4269">Target</span></span> | <span data-ttu-id="93a62-4270">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4270">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-4271">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-4271">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-4272">8</span><span class="sxs-lookup"><span data-stu-id="93a62-4272">8</span></span> |
| <span data-ttu-id="93a62-4273">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4273">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4275">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-4275">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4277">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4277">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4279">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4279">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4280">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4280">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4281">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-4281">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4283">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-4283">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4285">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-4285">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4287">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-4287">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4289">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-4289">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4291">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4291">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-4292">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-4293">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-4294">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-4294">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-4295">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-4295">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-4296">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-4296">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4298">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-4298">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-4299">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4299">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4301">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4302">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-4302">Output Merger Logic Op</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-4304">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4304">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-4305">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4305">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4306">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4306">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4307">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-4307">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-4308">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-4308">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-4309">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4309">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-4310">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-4310">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-4311">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-4311">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-4312">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-4312">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-4313">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-4313">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-4314">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4314">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4315">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4315">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4316">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-4316">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4318">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4318">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4320">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4320">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-4322">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-4322">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-4324">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-4324">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-4325">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4325">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4327">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-4327">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-4328">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-4328">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4330">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4330">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-4331">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-4331">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-4332">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-4332">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-4333">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4333">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4335">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4335">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="93a62-4336">DXGI_FORMAT_R8 \_ SNORM 的<sup>FCS</sup> (63) </span><span class="sxs-lookup"><span data-stu-id="93a62-4336">DXGI_FORMAT_R8\_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="93a62-4337">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4337">Target</span></span> | <span data-ttu-id="93a62-4338">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4338">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-4339">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-4339">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-4340">8</span><span class="sxs-lookup"><span data-stu-id="93a62-4340">8</span></span> |
| <span data-ttu-id="93a62-4341">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4341">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4343">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-4343">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4345">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4345">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4347">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4347">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4348">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4348">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4349">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-4349">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4351">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-4351">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4353">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-4353">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4355">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-4355">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4357">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-4357">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4359">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4359">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4361">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4361">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-4362">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4362">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-4363">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-4363">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4365">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-4365">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-4366">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-4366">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4368">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-4368">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4370">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4370">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4372">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4372">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4374">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-4374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-4375">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4375">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-4376">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4376">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4377">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4377">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4378">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-4378">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-4379">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-4379">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-4380">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4380">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-4381">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-4381">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-4382">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-4382">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-4383">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-4383">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-4384">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-4384">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-4385">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4385">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4386">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4386">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4387">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-4387">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4389">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4389">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4391">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4391">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-4393">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-4393">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-4395">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-4395">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4397">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4397">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4399">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-4399">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-4400">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-4400">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4402">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4402">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-4403">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-4403">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-4404">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-4404">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-4405">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4405">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4407">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4407">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="93a62-4408">DXGI_FORMAT_R8 \_ 聖的<sup>FCS</sup> (64) </span><span class="sxs-lookup"><span data-stu-id="93a62-4408">DXGI_FORMAT_R8\_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="93a62-4409">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4409">Target</span></span> | <span data-ttu-id="93a62-4410">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4410">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-4411">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-4411">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-4412">8</span><span class="sxs-lookup"><span data-stu-id="93a62-4412">8</span></span> |
| <span data-ttu-id="93a62-4413">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4413">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4415">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-4415">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4417">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4417">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4419">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4419">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4420">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4420">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4421">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-4421">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4423">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-4423">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4425">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-4425">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4427">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-4427">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4429">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-4429">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4431">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4431">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-4432">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4432">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-4433">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4433">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-4434">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-4434">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-4435">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-4435">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-4436">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-4436">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4438">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-4438">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-4439">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4439">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4441">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4441">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4442">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-4442">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-4443">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4443">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-4444">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4444">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4445">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4445">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4446">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-4446">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-4447">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-4447">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-4448">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4448">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-4449">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-4449">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-4450">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-4450">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-4451">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-4451">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-4452">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-4452">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-4453">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4453">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4454">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4454">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4455">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-4455">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4457">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4457">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4459">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4459">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-4461">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-4461">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-4463">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-4463">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-4464">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4464">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4466">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-4466">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-4467">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-4467">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4469">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4469">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-4470">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-4470">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-4471">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-4471">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-4472">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4472">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4474">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4474">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="93a62-4475">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65) </span><span class="sxs-lookup"><span data-stu-id="93a62-4475">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="93a62-4476">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4476">Target</span></span> | <span data-ttu-id="93a62-4477">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4477">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-4478">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-4478">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-4479">8</span><span class="sxs-lookup"><span data-stu-id="93a62-4479">8</span></span> |
| <span data-ttu-id="93a62-4480">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4480">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4482">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-4482">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4483">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4483">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4484">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4484">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4485">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4485">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4486">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-4486">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4488">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-4488">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4490">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-4490">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4492">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-4492">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4494">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-4494">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4496">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4496">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4498">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4498">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-4499">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4499">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-4500">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-4500">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-4501">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-4501">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-4502">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-4502">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4504">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-4504">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4506">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4506">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4508">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4508">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4510">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-4510">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-4511">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4511">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-4512">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4512">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4513">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4513">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4514">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-4514">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-4515">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-4515">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-4516">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4516">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-4517">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-4517">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-4518">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-4518">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-4519">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-4519">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-4520">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-4520">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-4521">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4521">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4522">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4522">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4523">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-4523">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4525">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4525">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4527">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4527">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-4529">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-4529">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-4531">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-4531">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4533">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4533">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4535">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-4535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-4536">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-4536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-4537">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-4538">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-4538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-4539">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-4539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-4540">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4540">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4542">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4542">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="93a62-4543">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67) </span><span class="sxs-lookup"><span data-stu-id="93a62-4543">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="93a62-4544">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4544">Target</span></span> | <span data-ttu-id="93a62-4545">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4545">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-4546">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-4546">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-4547">32</span><span class="sxs-lookup"><span data-stu-id="93a62-4547">32</span></span> |
| <span data-ttu-id="93a62-4548">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4548">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4550">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-4550">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4551">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4551">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4552">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4552">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4553">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4553">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4554">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-4554">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4556">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-4556">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4558">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-4558">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4560">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-4560">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4562">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-4562">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4564">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4564">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4566">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4566">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-4567">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4567">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-4568">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-4568">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-4569">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-4569">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-4570">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-4570">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4572">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-4572">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-4573">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4573">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4574">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4574">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4575">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-4575">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-4576">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4576">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-4577">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4577">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4578">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4578">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4579">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-4579">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-4580">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-4580">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-4581">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4581">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-4582">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-4582">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-4583">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-4583">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-4584">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-4584">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-4585">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-4585">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-4586">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4586">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4587">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4587">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4588">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-4588">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4590">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4590">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4591">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4591">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4592">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-4592">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-4593">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-4593">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-4594">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4594">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-4595">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-4595">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-4596">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-4596">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-4597">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4597">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-4598">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-4598">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-4599">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-4599">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-4600">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4600">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-4601">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4601">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="93a62-4602">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68) </span><span class="sxs-lookup"><span data-stu-id="93a62-4602">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="93a62-4603">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4603">Target</span></span> | <span data-ttu-id="93a62-4604">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4604">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-4605">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-4605">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-4606">16</span><span class="sxs-lookup"><span data-stu-id="93a62-4606">16</span></span> |
| <span data-ttu-id="93a62-4607">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4607">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4609">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-4609">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4610">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4610">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4611">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4611">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4612">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4612">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4613">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-4613">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4615">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-4615">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4617">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-4617">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4619">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-4619">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4621">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-4621">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4623">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4623">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4625">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4625">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-4626">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4626">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-4627">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-4627">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-4628">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-4628">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-4629">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-4629">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4631">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-4631">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-4632">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4632">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4633">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4633">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4634">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-4634">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-4635">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4635">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-4636">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4636">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4637">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4637">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4638">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-4638">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-4639">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-4639">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-4640">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4640">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-4641">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-4641">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-4642">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-4642">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-4643">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-4643">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-4644">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-4644">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-4645">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4645">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4646">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4646">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4647">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-4647">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4649">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4649">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4650">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4650">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4651">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-4651">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-4652">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-4652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-4653">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4653">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-4654">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-4654">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-4655">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-4655">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-4656">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4656">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-4657">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-4657">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-4658">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-4658">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-4659">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4659">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-4660">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4660">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="93a62-4661">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69) </span><span class="sxs-lookup"><span data-stu-id="93a62-4661">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="93a62-4662">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4662">Target</span></span> | <span data-ttu-id="93a62-4663">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4663">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-4664">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-4664">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-4665">16</span><span class="sxs-lookup"><span data-stu-id="93a62-4665">16</span></span> |
| <span data-ttu-id="93a62-4666">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4666">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4668">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-4668">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4669">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4669">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4670">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4670">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4671">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4671">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4672">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-4672">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4674">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-4674">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4676">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-4676">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4678">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-4678">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4680">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-4680">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4682">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4682">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4684">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4684">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-4685">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4685">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-4686">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-4686">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-4687">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-4687">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-4688">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-4688">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4690">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-4690">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-4691">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4691">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4692">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4692">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4693">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-4693">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-4694">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4694">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-4695">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4695">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4696">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4696">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4697">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-4697">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-4698">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-4698">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-4699">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4699">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-4700">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-4700">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-4701">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-4701">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-4702">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-4702">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-4703">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-4703">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-4704">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4704">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4705">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4705">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4706">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-4706">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4708">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4708">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4709">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4709">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4710">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-4710">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-4711">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-4711">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-4712">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4712">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-4713">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-4713">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-4714">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-4714">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-4715">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4715">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-4716">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-4716">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-4717">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-4717">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-4718">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4718">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-4719">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4719">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="93a62-4720">DXGI_FORMAT_BC1 無別 \_ <sup>PCC</sup> (70) </span><span class="sxs-lookup"><span data-stu-id="93a62-4720">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="93a62-4721">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4721">Target</span></span> | <span data-ttu-id="93a62-4722">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4722">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-4723">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-4723">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-4724">4</span><span class="sxs-lookup"><span data-stu-id="93a62-4724">4</span></span> |
| <span data-ttu-id="93a62-4725">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4725">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4727">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-4727">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4728">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4728">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4729">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4729">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4730">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4730">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4731">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-4731">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-4732">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-4732">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4734">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-4734">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4736">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-4736">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4738">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-4738">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-4739">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4739">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-4740">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4740">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-4741">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4741">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-4742">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-4742">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-4743">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-4743">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-4744">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-4744">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4746">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-4746">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-4747">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4747">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4748">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4748">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4749">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-4749">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-4750">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4750">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-4751">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4751">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4752">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4752">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4753">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-4753">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-4754">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-4754">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-4755">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4755">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-4756">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-4756">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-4757">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-4757">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-4758">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-4758">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-4759">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-4759">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-4760">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4760">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4761">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4761">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4762">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-4762">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4764">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4764">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4765">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4765">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4766">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-4766">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-4767">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-4767">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-4768">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4768">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-4769">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-4769">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-4770">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-4770">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4772">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4772">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-4773">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-4773">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-4774">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-4774">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-4775">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4775">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4777">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4777">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfccsup-71"></a><span data-ttu-id="93a62-4778">DXGI_FORMAT_BC1 \_ UNORM<sup>FCC</sup> (71) </span><span class="sxs-lookup"><span data-stu-id="93a62-4778">DXGI_FORMAT_BC1\_UNORM<sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="93a62-4779">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4779">Target</span></span> | <span data-ttu-id="93a62-4780">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4780">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-4781">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-4781">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-4782">4</span><span class="sxs-lookup"><span data-stu-id="93a62-4782">4</span></span> |
| <span data-ttu-id="93a62-4783">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4783">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4785">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-4785">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4786">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4786">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4787">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4787">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4788">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4788">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4789">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-4789">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-4790">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-4790">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4792">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-4792">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4794">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-4794">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4796">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-4796">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4798">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4798">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4800">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4800">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-4801">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4801">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-4802">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-4802">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-4803">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-4803">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-4804">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-4804">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4806">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-4806">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-4807">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4807">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4808">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4808">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4809">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-4809">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-4810">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4810">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-4811">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4811">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4812">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4812">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4813">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-4813">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-4814">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-4814">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-4815">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4815">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-4816">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-4816">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-4817">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-4817">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-4818">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-4818">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-4819">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-4819">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-4820">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4820">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4821">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4821">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4822">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-4822">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4824">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4824">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4825">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4825">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4826">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-4826">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-4827">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-4827">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-4828">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4828">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-4829">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-4829">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-4830">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-4830">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4832">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4832">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-4833">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-4833">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-4834">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-4834">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-4835">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4835">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4837">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4837">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfccsup-72"></a><span data-ttu-id="93a62-4838">DXGI_FORMAT_BC1 \_ UNORM \_ SRGB<sup>FCC</sup> (72) </span><span class="sxs-lookup"><span data-stu-id="93a62-4838">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="93a62-4839">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4839">Target</span></span> | <span data-ttu-id="93a62-4840">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4840">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-4841">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-4841">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-4842">4</span><span class="sxs-lookup"><span data-stu-id="93a62-4842">4</span></span> |
| <span data-ttu-id="93a62-4843">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4843">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4845">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-4845">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4846">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4846">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4847">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4847">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4848">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4848">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4849">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-4849">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-4850">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-4850">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4852">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-4852">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4854">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-4854">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4856">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-4856">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4858">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4858">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4860">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4860">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-4861">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4861">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-4862">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-4862">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-4863">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-4863">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-4864">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-4864">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4866">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-4866">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-4867">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4867">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4868">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4868">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4869">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-4869">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-4870">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4870">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-4871">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4871">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4872">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4872">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4873">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-4873">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-4874">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-4874">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-4875">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4875">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-4876">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-4876">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-4877">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-4877">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-4878">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-4878">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-4879">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-4879">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-4880">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4880">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4881">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4881">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4882">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-4882">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4884">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4884">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4885">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4885">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4886">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-4886">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-4887">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-4887">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-4888">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4888">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-4889">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-4889">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-4890">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-4890">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4892">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4892">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-4893">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-4893">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-4894">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-4894">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-4895">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4895">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4897">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4897">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="93a62-4898">DXGI_FORMAT_BC2 無別 \_ <sup>PCC</sup> (73) </span><span class="sxs-lookup"><span data-stu-id="93a62-4898">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="93a62-4899">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4899">Target</span></span> | <span data-ttu-id="93a62-4900">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4900">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-4901">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-4901">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-4902">8</span><span class="sxs-lookup"><span data-stu-id="93a62-4902">8</span></span> |
| <span data-ttu-id="93a62-4903">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4903">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4905">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-4905">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4906">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4906">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4907">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4907">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4908">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4908">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4909">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-4909">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-4910">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-4910">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4912">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-4912">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4914">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-4914">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4916">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-4916">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-4917">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4917">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-4918">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4918">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-4919">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4919">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-4920">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-4920">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-4921">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-4921">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-4922">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-4922">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4924">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-4924">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-4925">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4925">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4926">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4926">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4927">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-4927">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-4928">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4928">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-4929">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4929">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4930">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4930">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4931">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-4931">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-4932">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-4932">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-4933">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4933">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-4934">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-4934">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-4935">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-4935">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-4936">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-4936">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-4937">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-4937">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-4938">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4938">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4939">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4939">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4940">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-4940">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4942">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4942">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4943">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4943">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4944">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-4944">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-4945">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-4945">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-4946">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4946">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-4947">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-4947">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-4948">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-4948">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4950">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4950">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-4951">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-4951">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-4952">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-4952">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-4953">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4953">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4955">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-4955">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfccsup-74"></a><span data-ttu-id="93a62-4956">DXGI_FORMAT_BC2 \_ UNORM<sup>FCC</sup> (74) </span><span class="sxs-lookup"><span data-stu-id="93a62-4956">DXGI_FORMAT_BC2\_UNORM<sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="93a62-4957">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4957">Target</span></span> | <span data-ttu-id="93a62-4958">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4958">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-4959">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-4959">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-4960">8</span><span class="sxs-lookup"><span data-stu-id="93a62-4960">8</span></span> |
| <span data-ttu-id="93a62-4961">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-4961">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4963">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-4963">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4964">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4964">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4965">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4965">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4966">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-4966">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-4967">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-4967">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-4968">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-4968">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4970">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-4970">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4972">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-4972">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4974">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-4974">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4976">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4976">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4978">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4978">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-4979">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-4979">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-4980">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-4980">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-4981">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-4981">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-4982">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-4982">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-4984">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-4984">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-4985">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4985">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4986">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-4986">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-4987">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-4987">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-4988">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-4988">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-4989">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4989">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4990">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-4990">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-4991">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-4991">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-4992">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-4992">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-4993">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-4993">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-4994">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-4994">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-4995">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-4995">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-4996">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-4996">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-4997">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-4997">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-4998">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4998">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-4999">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-4999">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5000">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-5000">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5002">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5002">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5003">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5003">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5004">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-5004">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-5005">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-5005">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-5006">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5006">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-5007">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-5007">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-5008">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-5008">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5010">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5010">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-5011">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-5011">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-5012">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-5012">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-5013">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5013">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5015">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5015">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfccsup-75"></a><span data-ttu-id="93a62-5016">DXGI_FORMAT_BC2 \_ UNORM \_ SRGB<sup>FCC</sup> (75) </span><span class="sxs-lookup"><span data-stu-id="93a62-5016">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="93a62-5017">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5017">Target</span></span> | <span data-ttu-id="93a62-5018">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5018">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-5019">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-5019">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-5020">8</span><span class="sxs-lookup"><span data-stu-id="93a62-5020">8</span></span> |
| <span data-ttu-id="93a62-5021">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5021">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5023">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-5023">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5024">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5024">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5025">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5025">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5026">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5026">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5027">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-5027">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-5028">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-5028">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5030">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-5030">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5032">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-5032">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5034">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-5034">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5036">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5036">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5038">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5038">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-5039">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5039">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-5040">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-5040">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-5041">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-5041">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-5042">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-5042">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5044">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-5044">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-5045">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5045">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5046">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5046">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5047">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-5047">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-5048">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5048">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-5049">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5049">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5050">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5050">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5051">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-5051">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-5052">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-5052">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-5053">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5053">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-5054">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-5054">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-5055">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-5055">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-5056">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-5056">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-5057">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-5057">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-5058">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5058">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5059">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5059">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5060">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-5060">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5062">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5062">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5063">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5063">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5064">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-5064">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-5065">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-5065">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-5066">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5066">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-5067">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-5067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-5068">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-5068">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5070">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5070">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-5071">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-5071">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-5072">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-5072">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-5073">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5073">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5075">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5075">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="93a62-5076">DXGI_FORMAT_BC3 無別 \_ <sup>PCC</sup> (76) </span><span class="sxs-lookup"><span data-stu-id="93a62-5076">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="93a62-5077">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5077">Target</span></span> | <span data-ttu-id="93a62-5078">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5078">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-5079">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-5079">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-5080">8</span><span class="sxs-lookup"><span data-stu-id="93a62-5080">8</span></span> |
| <span data-ttu-id="93a62-5081">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5081">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5083">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-5083">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5084">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5085">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5086">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-5087">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-5088">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-5088">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5090">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-5090">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5092">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-5092">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5094">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-5094">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-5095">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5095">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-5096">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5096">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-5097">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5097">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-5098">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-5098">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-5099">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-5099">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-5100">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-5100">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5102">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-5102">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-5103">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5103">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5104">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5104">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5105">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-5105">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-5106">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5106">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-5107">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5107">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5108">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5108">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5109">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-5109">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-5110">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-5110">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-5111">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5111">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-5112">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-5112">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-5113">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-5113">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-5114">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-5114">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-5115">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-5115">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-5116">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5116">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5117">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5117">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5118">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-5118">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5120">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5120">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5121">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5121">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5122">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-5122">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-5123">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-5123">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-5124">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5124">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-5125">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-5125">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-5126">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-5126">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5128">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5128">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-5129">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-5129">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-5130">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-5130">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-5131">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5131">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5133">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5133">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfccsup-77"></a><span data-ttu-id="93a62-5134">DXGI_FORMAT_BC3 \_ UNORM<sup>FCC</sup> (77) </span><span class="sxs-lookup"><span data-stu-id="93a62-5134">DXGI_FORMAT_BC3\_UNORM<sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="93a62-5135">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5135">Target</span></span> | <span data-ttu-id="93a62-5136">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5136">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-5137">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-5137">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-5138">8</span><span class="sxs-lookup"><span data-stu-id="93a62-5138">8</span></span> |
| <span data-ttu-id="93a62-5139">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5139">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5141">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-5141">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5142">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5142">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5143">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5143">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5144">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5144">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5145">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-5145">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-5146">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-5146">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5148">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-5148">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5150">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-5150">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5152">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-5152">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5154">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5154">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5156">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5156">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-5157">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5157">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-5158">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-5158">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-5159">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-5159">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-5160">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-5160">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5162">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-5162">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-5163">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5163">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5164">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5164">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5165">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-5165">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-5166">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5166">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-5167">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5167">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5168">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5168">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5169">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-5169">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-5170">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-5170">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-5171">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-5172">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-5172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-5173">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-5173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-5174">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-5174">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-5175">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-5175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-5176">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5176">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5177">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5177">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5178">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-5178">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5180">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5180">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5181">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5181">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5182">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-5182">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-5183">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-5183">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-5184">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5184">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-5185">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-5185">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-5186">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-5186">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5188">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5188">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-5189">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-5189">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-5190">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-5190">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-5191">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5191">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5193">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5193">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfccsup-78"></a><span data-ttu-id="93a62-5194">DXGI_FORMAT_BC3 \_ UNORM \_ SRGB<sup>FCC</sup> (78) </span><span class="sxs-lookup"><span data-stu-id="93a62-5194">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="93a62-5195">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5195">Target</span></span> | <span data-ttu-id="93a62-5196">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5196">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-5197">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-5197">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-5198">8</span><span class="sxs-lookup"><span data-stu-id="93a62-5198">8</span></span> |
| <span data-ttu-id="93a62-5199">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5199">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5201">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-5201">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5202">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5202">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5203">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5203">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5204">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5204">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5205">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-5205">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-5206">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-5206">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5208">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-5208">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5210">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-5210">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5212">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-5212">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5214">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5214">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5216">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5216">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-5217">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5217">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-5218">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-5218">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-5219">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-5219">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-5220">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-5220">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5222">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-5222">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-5223">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5223">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5224">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5224">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5225">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-5225">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-5226">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5226">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-5227">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5227">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5228">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5228">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5229">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-5229">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-5230">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-5230">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-5231">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5231">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-5232">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-5232">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-5233">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-5233">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-5234">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-5234">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-5235">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-5235">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-5236">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5236">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5237">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5237">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5238">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-5238">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5240">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5240">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5241">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5241">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5242">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-5242">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-5243">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-5243">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-5244">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5244">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-5245">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-5245">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-5246">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-5246">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5248">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5248">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-5249">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-5249">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-5250">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-5250">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-5251">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5251">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5253">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5253">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="93a62-5254">DXGI_FORMAT_BC4 無別 \_ <sup>PCC</sup> (79) </span><span class="sxs-lookup"><span data-stu-id="93a62-5254">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="93a62-5255">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5255">Target</span></span> | <span data-ttu-id="93a62-5256">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5256">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-5257">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-5257">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-5258">4</span><span class="sxs-lookup"><span data-stu-id="93a62-5258">4</span></span> |
| <span data-ttu-id="93a62-5259">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5259">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5261">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-5261">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5262">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5262">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5263">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5263">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5264">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5264">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5265">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-5265">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-5266">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-5266">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5268">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-5268">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5270">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-5270">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5272">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-5272">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-5273">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5273">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-5274">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5274">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-5275">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5275">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-5276">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-5276">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-5277">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-5277">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-5278">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-5278">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5280">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-5280">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-5281">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5281">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5282">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5282">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5283">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-5283">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-5284">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5284">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-5285">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5285">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5286">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5286">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5287">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-5287">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-5288">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-5288">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-5289">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5289">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-5290">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-5290">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-5291">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-5291">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-5292">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-5292">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-5293">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-5293">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-5294">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5294">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5295">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5295">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5296">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-5296">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5298">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5298">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5299">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5299">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5300">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-5300">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-5301">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-5301">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-5302">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5302">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-5303">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-5303">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-5304">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-5304">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5306">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5306">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-5307">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-5307">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-5308">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-5308">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-5309">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5309">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-5310">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5310">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfccsup-80"></a><span data-ttu-id="93a62-5311">DXGI_FORMAT_BC4 \_ UNORM<sup>FCC</sup> (80) </span><span class="sxs-lookup"><span data-stu-id="93a62-5311">DXGI_FORMAT_BC4\_UNORM<sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="93a62-5312">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5312">Target</span></span> | <span data-ttu-id="93a62-5313">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5313">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-5314">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-5314">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-5315">4</span><span class="sxs-lookup"><span data-stu-id="93a62-5315">4</span></span> |
| <span data-ttu-id="93a62-5316">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5316">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5318">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-5318">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5319">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5319">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5320">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5321">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5321">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5322">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-5322">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-5323">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-5323">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5325">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-5325">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5327">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-5327">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5329">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-5329">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5331">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5331">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5333">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5333">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-5334">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5334">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-5335">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-5335">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-5336">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-5336">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-5337">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-5337">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5339">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-5339">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-5340">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5340">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5341">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5341">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5342">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-5342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-5343">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-5344">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5345">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5346">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-5346">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-5347">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-5347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-5348">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-5349">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-5349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-5350">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-5350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-5351">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-5351">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-5352">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-5352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-5353">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5354">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5355">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-5355">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5357">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5358">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5359">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-5359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-5360">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-5360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-5361">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5361">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-5362">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-5362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-5363">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-5363">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5365">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5365">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-5366">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-5366">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-5367">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-5367">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-5368">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5368">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-5369">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5369">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfccsup-81"></a><span data-ttu-id="93a62-5370">DXGI_FORMAT_BC4 \_ SNORM<sup>FCC</sup> (81) </span><span class="sxs-lookup"><span data-stu-id="93a62-5370">DXGI_FORMAT_BC4\_SNORM<sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="93a62-5371">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5371">Target</span></span> | <span data-ttu-id="93a62-5372">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5372">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-5373">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-5373">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-5374">4</span><span class="sxs-lookup"><span data-stu-id="93a62-5374">4</span></span> |
| <span data-ttu-id="93a62-5375">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5375">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5377">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-5377">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5378">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5378">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5379">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5379">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5380">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5380">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5381">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-5381">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-5382">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-5382">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5384">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-5384">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5386">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-5386">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5388">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-5388">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5390">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5390">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5392">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5392">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-5393">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5393">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-5394">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-5394">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-5395">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-5395">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-5396">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-5396">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5398">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-5398">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-5399">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5399">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5400">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5400">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5401">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-5401">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-5402">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5402">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-5403">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5403">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5404">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5404">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5405">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-5405">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-5406">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-5406">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-5407">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5407">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-5408">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-5408">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-5409">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-5409">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-5410">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-5410">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-5411">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-5411">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-5412">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5412">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5413">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5413">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5414">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-5414">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5416">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5416">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5417">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5417">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5418">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-5418">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-5419">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-5419">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-5420">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5420">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-5421">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-5421">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-5422">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-5422">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5424">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5424">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-5425">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-5425">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-5426">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-5426">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-5427">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5427">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-5428">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5428">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="93a62-5429">DXGI_FORMAT_BC5 無別 \_ <sup>PCC</sup> (82) </span><span class="sxs-lookup"><span data-stu-id="93a62-5429">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="93a62-5430">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5430">Target</span></span> | <span data-ttu-id="93a62-5431">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5431">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-5432">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-5432">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-5433">8</span><span class="sxs-lookup"><span data-stu-id="93a62-5433">8</span></span> |
| <span data-ttu-id="93a62-5434">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5434">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5436">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-5436">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5437">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5437">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5438">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5438">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5439">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5439">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5440">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-5440">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-5441">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-5441">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5443">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-5443">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5445">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-5445">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5447">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-5447">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-5448">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5448">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-5449">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5449">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-5450">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5450">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-5451">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-5451">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-5452">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-5452">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-5453">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-5453">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5455">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-5455">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-5456">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5456">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5457">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5457">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5458">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-5458">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-5459">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5459">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-5460">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5460">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5461">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5461">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5462">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-5462">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-5463">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-5463">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-5464">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5464">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-5465">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-5465">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-5466">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-5466">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-5467">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-5467">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-5468">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-5468">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-5469">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5469">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5470">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5470">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5471">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-5471">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5473">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5473">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5474">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5474">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5475">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-5475">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-5476">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-5476">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-5477">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5477">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-5478">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-5478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-5479">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-5479">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5481">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-5482">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-5482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-5483">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-5483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-5484">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5484">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-5485">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5485">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfccsup-83"></a><span data-ttu-id="93a62-5486">DXGI_FORMAT_BC5 \_ UNORM<sup>FCC</sup> (83) </span><span class="sxs-lookup"><span data-stu-id="93a62-5486">DXGI_FORMAT_BC5\_UNORM<sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="93a62-5487">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5487">Target</span></span> | <span data-ttu-id="93a62-5488">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5488">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-5489">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-5489">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-5490">8</span><span class="sxs-lookup"><span data-stu-id="93a62-5490">8</span></span> |
| <span data-ttu-id="93a62-5491">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5491">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5493">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-5493">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5494">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5494">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5495">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5495">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5496">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5496">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5497">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-5497">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-5498">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-5498">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5500">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-5500">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5502">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-5502">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5504">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-5504">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5506">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5506">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5508">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-5509">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-5510">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-5510">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-5511">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-5511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-5512">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-5512">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5514">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-5514">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-5515">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5515">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5516">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5516">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5517">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-5517">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-5518">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5518">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-5519">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5519">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5520">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5520">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5521">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-5521">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-5522">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-5522">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-5523">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5523">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-5524">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-5524">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-5525">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-5525">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-5526">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-5526">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-5527">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-5527">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-5528">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5528">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5529">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5529">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5530">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-5530">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5532">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5532">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5533">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5533">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5534">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-5534">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-5535">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-5535">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-5536">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5536">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-5537">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-5537">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-5538">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-5538">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5540">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5540">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-5541">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-5541">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-5542">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-5542">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-5543">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5543">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-5544">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5544">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfccsup-84"></a><span data-ttu-id="93a62-5545">DXGI_FORMAT_BC5 \_ SNORM<sup>FCC</sup> (84) </span><span class="sxs-lookup"><span data-stu-id="93a62-5545">DXGI_FORMAT_BC5\_SNORM<sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="93a62-5546">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5546">Target</span></span> | <span data-ttu-id="93a62-5547">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5547">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-5548">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-5548">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-5549">8</span><span class="sxs-lookup"><span data-stu-id="93a62-5549">8</span></span> |
| <span data-ttu-id="93a62-5550">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5550">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5552">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-5552">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5553">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5553">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5554">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5554">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5555">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5555">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5556">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-5556">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-5557">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-5557">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5559">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-5559">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5561">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-5561">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5563">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-5563">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5565">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5565">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5567">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5567">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-5568">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5568">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-5569">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-5569">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-5570">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-5570">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-5571">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-5571">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5573">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-5573">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-5574">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5574">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5575">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5575">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5576">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-5576">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-5577">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5577">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-5578">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5578">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5579">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5579">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5580">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-5580">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-5581">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-5581">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-5582">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5582">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-5583">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-5583">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-5584">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-5584">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-5585">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-5585">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-5586">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-5586">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-5587">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5587">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5588">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5588">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5589">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-5589">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5591">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5591">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5592">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5592">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5593">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-5593">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-5594">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-5594">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-5595">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5595">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-5596">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-5596">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-5597">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-5597">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5599">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5599">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-5600">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-5600">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-5601">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-5601">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-5602">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5602">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-5603">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5603">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="93a62-5604">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85) </span><span class="sxs-lookup"><span data-stu-id="93a62-5604">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="93a62-5605">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5605">Target</span></span> | <span data-ttu-id="93a62-5606">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5606">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-5607">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-5607">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-5608">16</span><span class="sxs-lookup"><span data-stu-id="93a62-5608">16</span></span> |
| <span data-ttu-id="93a62-5609">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5609">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5611">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-5611">Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5613">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5613">Input Assembler Vertex Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5615">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5615">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5616">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5616">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5617">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-5617">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5619">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-5619">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5621">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-5621">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5623">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-5623">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5625">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-5625">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5627">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5627">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5629">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5629">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-5630">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5630">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-5631">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-5631">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-5632">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-5632">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-5633">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-5633">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5635">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-5635">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5637">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5637">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5639">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5639">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5641">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-5641">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-5642">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5642">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-5643">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5643">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5644">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5644">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5645">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-5645">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-5646">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-5646">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-5647">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5647">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-5648">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-5648">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-5649">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-5649">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-5650">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-5650">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-5651">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-5651">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-5652">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5652">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5653">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5653">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5654">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-5654">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5656">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5656">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5658">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5658">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5660">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-5660">Other Multisample Count RT</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5662">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-5662">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5664">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5664">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5666">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-5666">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-5667">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-5667">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-5668">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5668">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-5669">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-5669">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-5670">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-5670">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-5671">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5671">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-5672">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5672">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="93a62-5673">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86) </span><span class="sxs-lookup"><span data-stu-id="93a62-5673">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="93a62-5674">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5674">Target</span></span> | <span data-ttu-id="93a62-5675">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5675">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-5676">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-5676">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-5677">16</span><span class="sxs-lookup"><span data-stu-id="93a62-5677">16</span></span> |
| <span data-ttu-id="93a62-5678">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5678">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5680">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-5680">Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5682">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5682">Input Assembler Vertex Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5684">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5684">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5685">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5685">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5686">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-5686">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5688">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-5688">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5690">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-5690">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5692">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-5692">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5694">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-5694">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5696">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5696">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5698">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5698">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-5699">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5699">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-5700">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-5700">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-5701">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-5701">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-5702">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-5702">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5704">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-5704">Mipmap Auto-Generation</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5706">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5706">RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5708">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5708">Blendable RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5710">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-5710">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-5711">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5711">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-5712">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5712">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5713">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5713">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5714">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-5714">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-5715">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-5715">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-5716">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5716">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-5717">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-5717">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-5718">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-5718">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-5719">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-5719">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-5720">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-5720">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-5721">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5721">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5722">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5722">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5723">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-5723">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5725">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5725">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5727">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5727">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5729">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-5729">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5731">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-5731">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5733">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5733">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5735">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-5735">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-5736">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-5736">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-5737">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5737">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-5738">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-5738">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-5739">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-5739">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-5740">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5740">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-5741">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5741">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="93a62-5742">DXGI_FORMAT_B8G8R8A8 無的 \_ <sup>電腦</sup> (90) </span><span class="sxs-lookup"><span data-stu-id="93a62-5742">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="93a62-5743">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5743">Target</span></span> | <span data-ttu-id="93a62-5744">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5744">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-5745">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-5745">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-5746">32</span><span class="sxs-lookup"><span data-stu-id="93a62-5746">32</span></span> |
| <span data-ttu-id="93a62-5747">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5747">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5749">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-5749">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5750">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5750">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5751">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5751">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5752">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5752">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5753">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-5753">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5755">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-5755">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-5757">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5759">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-5759">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5761">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-5761">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-5762">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5762">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-5763">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5763">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-5764">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5764">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-5765">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-5765">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-5766">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-5766">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-5767">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-5767">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5769">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-5769">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-5770">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5770">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5771">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5771">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5772">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-5772">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-5773">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5773">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-5774">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5774">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5775">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5775">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5776">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-5776">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-5777">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-5777">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-5778">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5778">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-5779">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-5779">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-5780">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-5780">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-5781">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-5781">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-5782">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-5782">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-5783">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5783">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5784">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5784">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5785">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-5785">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5787">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5787">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5788">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5788">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5789">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-5789">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-5790">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-5790">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-5791">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5791">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-5792">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-5792">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-5793">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-5793">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5795">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5795">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-5796">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-5796">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-5797">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-5797">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-5798">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5798">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5800">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5800">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="93a62-5801">DXGI_FORMAT_B8G8R8A8 \_ UNORM 的<sup>FCS</sup> (87) </span><span class="sxs-lookup"><span data-stu-id="93a62-5801">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="93a62-5802">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5802">Target</span></span> | <span data-ttu-id="93a62-5803">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5803">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-5804">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-5804">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-5805">32</span><span class="sxs-lookup"><span data-stu-id="93a62-5805">32</span></span> |
| <span data-ttu-id="93a62-5806">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5806">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5808">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-5808">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5810">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5810">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5812">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5812">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5813">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5813">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5814">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-5814">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5816">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-5816">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5818">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-5818">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5820">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-5820">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5822">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-5822">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5824">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5824">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5826">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5826">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-5827">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5827">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-5828">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-5828">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-5829">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-5829">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-5830">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-5830">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5832">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-5832">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5834">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5834">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5836">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5836">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5838">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-5838">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-5839">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5839">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-5840">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5840">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5841">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5841">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5842">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-5842">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-5843">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-5843">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-5844">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5844">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-5845">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-5845">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-5846">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-5846">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-5847">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-5847">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-5848">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-5848">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-5849">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5849">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5850">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5850">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5851">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-5851">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5853">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5853">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5855">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5855">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5857">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-5857">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5859">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-5859">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5861">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5861">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5863">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-5863">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5865">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-5865">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5867">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5867">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-5868">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-5868">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5870">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-5870">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5872">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5872">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5874">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5874">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="93a62-5875">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ SRGB<sup>FCS</sup> (91) </span><span class="sxs-lookup"><span data-stu-id="93a62-5875">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="93a62-5876">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5876">Target</span></span> | <span data-ttu-id="93a62-5877">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5877">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-5878">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-5878">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-5879">32</span><span class="sxs-lookup"><span data-stu-id="93a62-5879">32</span></span> |
| <span data-ttu-id="93a62-5880">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5880">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5882">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-5882">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5883">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5883">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5884">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5884">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5885">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5885">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5886">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-5886">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5888">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-5888">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5890">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-5890">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-5892">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5894">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-5894">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5896">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5896">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5898">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5898">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-5899">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5899">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-5900">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-5900">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-5901">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-5901">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-5902">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-5902">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5904">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-5904">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5906">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5906">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5908">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5908">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5910">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-5910">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-5911">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5911">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-5912">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5912">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5913">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5913">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5914">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-5914">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-5915">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-5915">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-5916">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5916">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-5917">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-5917">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-5918">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-5918">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-5919">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-5919">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-5920">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-5920">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-5921">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5921">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5922">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5922">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5923">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-5923">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5925">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5925">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5927">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5927">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5929">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-5929">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5931">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-5931">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5933">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5933">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5935">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-5935">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5937">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-5937">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5939">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5939">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-5940">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-5940">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5942">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-5942">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-5944">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5944">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5946">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-5946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="93a62-5947">DXGI_FORMAT_B8G8R8X8 無的 \_ <sup>電腦</sup> (92) </span><span class="sxs-lookup"><span data-stu-id="93a62-5947">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="93a62-5948">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5948">Target</span></span> | <span data-ttu-id="93a62-5949">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5949">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-5950">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-5950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-5951">32</span><span class="sxs-lookup"><span data-stu-id="93a62-5951">32</span></span> |
| <span data-ttu-id="93a62-5952">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-5952">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5954">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-5954">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5955">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5955">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5956">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5956">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5957">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-5957">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-5958">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-5958">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5960">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-5960">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5962">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-5962">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5964">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-5964">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5966">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-5966">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-5967">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5967">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-5968">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5968">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-5969">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-5969">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-5970">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-5970">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-5971">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-5971">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-5972">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-5972">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5974">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-5974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-5975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5975">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5976">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5977">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-5977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-5978">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-5978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-5979">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5980">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-5980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-5981">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-5981">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-5982">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-5982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-5983">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-5984">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-5984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-5985">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-5985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-5986">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-5986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-5987">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-5987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-5988">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5989">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-5989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-5990">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-5990">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-5992">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5993">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-5993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-5994">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-5994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-5995">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-5995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-5996">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-5996">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-5997">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-5997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-5998">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-5998">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6000">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6000">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-6001">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-6001">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-6002">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-6002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-6003">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6003">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6005">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6005">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="93a62-6006">DXGI_FORMAT_B8G8R8X8 \_ UNORM 的<sup>FCS</sup> (88) </span><span class="sxs-lookup"><span data-stu-id="93a62-6006">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="93a62-6007">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6007">Target</span></span> | <span data-ttu-id="93a62-6008">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6008">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-6009">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-6009">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-6010">32</span><span class="sxs-lookup"><span data-stu-id="93a62-6010">32</span></span> |
| <span data-ttu-id="93a62-6011">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6011">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6013">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-6013">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6015">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6015">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6017">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6017">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6018">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6018">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6019">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-6019">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-6021">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-6023">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-6025">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6027">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-6027">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6029">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6029">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6031">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-6032">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-6033">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-6033">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-6034">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-6034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-6035">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-6035">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6037">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-6037">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6039">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6041">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6041">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6043">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-6043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-6044">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-6045">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6046">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6047">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-6047">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-6048">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-6048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-6049">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-6050">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-6050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-6051">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-6051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-6052">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-6052">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-6053">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-6053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-6054">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6055">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6056">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-6056">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6058">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6058">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6060">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6060">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6062">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-6062">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6064">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-6064">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6066">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6066">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6068">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-6068">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-6069">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-6069">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6071">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6071">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-6072">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-6072">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6074">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-6074">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6076">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6076">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6078">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6078">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="93a62-6079">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ SRGB<sup>FCS</sup> (93) </span><span class="sxs-lookup"><span data-stu-id="93a62-6079">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="93a62-6080">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6080">Target</span></span> | <span data-ttu-id="93a62-6081">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6081">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-6082">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-6082">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-6083">32</span><span class="sxs-lookup"><span data-stu-id="93a62-6083">32</span></span> |
| <span data-ttu-id="93a62-6084">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6084">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6086">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-6086">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6087">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6087">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6088">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6088">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6089">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6089">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6090">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-6090">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6092">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-6092">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6094">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-6094">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6096">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-6096">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6098">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-6098">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6100">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6100">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6102">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6102">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-6103">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6103">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-6104">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-6104">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-6105">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-6105">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-6106">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-6106">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6108">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-6108">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6110">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6110">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6112">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6112">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6114">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-6114">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-6115">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6115">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-6116">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6116">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6117">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6117">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6118">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-6118">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-6119">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-6119">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-6120">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6120">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-6121">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-6121">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-6122">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-6122">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-6123">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-6123">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-6124">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-6124">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-6125">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6125">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6126">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6126">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6127">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-6127">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6129">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6129">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6131">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6131">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6133">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-6133">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6135">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-6135">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6137">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6137">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6139">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-6139">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-6140">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-6140">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6142">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6142">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-6143">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-6143">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-6144">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-6144">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-6145">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6145">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6147">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="93a62-6148">DXGI_FORMAT_AYUV<sup>V</sup> (100) </span><span class="sxs-lookup"><span data-stu-id="93a62-6148">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="93a62-6149">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6149">Target</span></span> | <span data-ttu-id="93a62-6150">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6150">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-6151">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-6151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-6152">32</span><span class="sxs-lookup"><span data-stu-id="93a62-6152">32</span></span> |
| <span data-ttu-id="93a62-6153">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6153">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6155">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-6155">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6156">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6156">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6157">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6157">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6158">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6158">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6159">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-6159">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-6160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-6160">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6162">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-6162">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-6163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-6163">TextureCube</span></span> | \- |
| <span data-ttu-id="93a62-6164">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-6164">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6166">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6166">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6168">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6168">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-6169">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6169">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-6170">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-6170">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6172">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-6172">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-6173">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-6173">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6175">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-6175">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6177">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6177">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6179">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6179">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6181">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-6181">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-6182">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6182">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-6183">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6183">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6184">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6184">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6185">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-6185">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-6186">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-6186">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-6187">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6187">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-6188">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-6188">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-6189">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-6189">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-6190">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-6190">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-6191">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-6191">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-6192">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6192">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6193">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6193">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6194">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-6194">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6196">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6196">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6197">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6197">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6198">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-6198">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-6199">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-6199">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-6200">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6200">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-6201">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-6201">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-6202">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-6202">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-6203">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6203">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6205">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-6205">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6207">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-6207">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6209">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6209">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6211">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6211">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="93a62-6212">DXGI_FORMAT_Y410<sup>V</sup> (101) </span><span class="sxs-lookup"><span data-stu-id="93a62-6212">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="93a62-6213">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6213">Target</span></span> | <span data-ttu-id="93a62-6214">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6214">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-6215">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-6215">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-6216">32</span><span class="sxs-lookup"><span data-stu-id="93a62-6216">32</span></span> |
| <span data-ttu-id="93a62-6217">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6217">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6219">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-6219">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6220">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6220">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6221">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6221">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6222">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6222">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6223">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-6223">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-6224">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-6224">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6226">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-6226">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-6227">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-6227">TextureCube</span></span> | \- |
| <span data-ttu-id="93a62-6228">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-6228">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6230">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6230">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6232">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6232">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-6233">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6233">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-6234">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-6234">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6236">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-6236">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-6237">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-6237">Mipmap</span></span> | \- |
| <span data-ttu-id="93a62-6238">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-6238">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-6239">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6239">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6240">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6240">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6241">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-6241">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-6242">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6242">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-6243">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6243">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6244">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6244">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6245">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-6245">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-6246">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-6246">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-6247">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6247">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-6248">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-6248">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-6249">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-6249">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-6250">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-6250">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-6251">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-6251">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-6252">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6252">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6253">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6253">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6254">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-6254">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6256">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6256">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6257">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6257">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6258">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-6258">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-6259">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-6259">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-6260">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6260">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-6261">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-6261">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-6262">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-6262">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-6263">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6263">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6265">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-6265">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6267">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-6267">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6269">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6269">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6271">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6271">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="93a62-6272">DXGI_FORMAT_Y416<sup>V</sup> (102) </span><span class="sxs-lookup"><span data-stu-id="93a62-6272">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="93a62-6273">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6273">Target</span></span> | <span data-ttu-id="93a62-6274">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6274">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-6275">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-6275">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-6276">64</span><span class="sxs-lookup"><span data-stu-id="93a62-6276">64</span></span> |
| <span data-ttu-id="93a62-6277">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6277">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6279">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-6279">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6280">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6281">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6282">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-6283">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-6284">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-6284">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6286">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-6286">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-6287">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-6287">TextureCube</span></span> | \- |
| <span data-ttu-id="93a62-6288">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-6288">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6290">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6290">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6292">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-6293">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-6294">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-6294">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6296">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-6296">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-6297">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-6297">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6299">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-6299">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-6300">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6300">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6301">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6302">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-6302">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-6303">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-6304">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6305">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6306">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-6306">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-6307">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-6307">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-6308">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6308">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-6309">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-6309">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-6310">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-6310">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-6311">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-6311">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-6312">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-6312">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-6313">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6313">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6314">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6314">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6315">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-6315">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6317">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6318">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6319">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-6319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-6320">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-6320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-6321">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6321">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-6322">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-6322">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-6323">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-6323">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-6324">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6324">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6326">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-6326">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6328">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-6328">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6330">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6330">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6332">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6332">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="93a62-6333">DXGI_FORMAT_NV12<sup>V</sup> (103) </span><span class="sxs-lookup"><span data-stu-id="93a62-6333">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="93a62-6334">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6334">Target</span></span> | <span data-ttu-id="93a62-6335">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6335">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-6336">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-6336">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-6337">8</span><span class="sxs-lookup"><span data-stu-id="93a62-6337">8</span></span> |
| <span data-ttu-id="93a62-6338">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6338">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6340">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-6340">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6341">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6341">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6342">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6342">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6343">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6343">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6344">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-6344">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-6345">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-6345">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6347">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-6347">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-6348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-6348">TextureCube</span></span> | \- |
| <span data-ttu-id="93a62-6349">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-6349">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6351">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6351">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6353">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6353">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-6354">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6354">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-6355">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-6355">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6357">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-6357">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-6358">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-6358">Mipmap</span></span> | \- |
| <span data-ttu-id="93a62-6359">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-6359">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-6360">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6360">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6362">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6362">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6364">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-6364">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-6365">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6365">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-6366">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6366">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6367">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6367">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6368">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-6368">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-6369">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-6369">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-6370">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6370">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-6371">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-6371">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-6372">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-6372">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-6373">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-6373">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-6374">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-6374">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-6375">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6375">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6376">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6376">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6377">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-6377">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6379">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6379">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6380">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6380">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6381">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-6381">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-6382">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-6382">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-6383">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6383">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-6384">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-6384">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-6385">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-6385">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-6386">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6386">Video Decoder Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6388">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-6388">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6390">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-6390">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6392">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6392">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6394">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6394">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="93a62-6395">DXGI_FORMAT_P010<sup>V</sup> (104) </span><span class="sxs-lookup"><span data-stu-id="93a62-6395">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="93a62-6396">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6396">Target</span></span> | <span data-ttu-id="93a62-6397">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6397">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-6398">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-6398">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-6399">16</span><span class="sxs-lookup"><span data-stu-id="93a62-6399">16</span></span> |
| <span data-ttu-id="93a62-6400">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6400">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6402">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-6402">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6403">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6403">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6404">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6404">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6405">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6405">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6406">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-6406">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-6407">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-6407">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6409">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-6409">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-6410">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-6410">TextureCube</span></span> | \- |
| <span data-ttu-id="93a62-6411">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-6411">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6413">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6413">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6415">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6415">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-6416">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6416">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-6417">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-6417">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6419">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-6419">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-6420">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-6420">Mipmap</span></span> | \- |
| <span data-ttu-id="93a62-6421">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-6421">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-6422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6422">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6424">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6424">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6426">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-6426">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-6427">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6427">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-6428">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6428">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6429">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6429">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6430">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-6430">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-6431">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-6431">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-6432">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6432">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-6433">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-6433">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-6434">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-6434">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-6435">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-6435">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-6436">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-6436">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-6437">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6437">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6438">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6438">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6439">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-6439">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6441">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6441">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6442">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6442">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6443">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-6443">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-6444">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-6444">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-6445">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6445">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-6446">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-6446">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-6447">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-6447">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-6448">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6448">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6450">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-6450">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6452">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-6452">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6454">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6454">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6456">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6456">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="93a62-6457">DXGI_FORMAT_P016<sup>V</sup> (105) </span><span class="sxs-lookup"><span data-stu-id="93a62-6457">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="93a62-6458">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6458">Target</span></span> | <span data-ttu-id="93a62-6459">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6459">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-6460">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-6460">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-6461">16</span><span class="sxs-lookup"><span data-stu-id="93a62-6461">16</span></span> |
| <span data-ttu-id="93a62-6462">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6462">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6464">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-6464">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6465">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6465">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6466">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6466">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6467">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6467">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6468">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-6468">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-6469">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-6469">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6471">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-6471">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-6472">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-6472">TextureCube</span></span> | \- |
| <span data-ttu-id="93a62-6473">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-6473">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6475">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6475">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6477">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6477">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-6478">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6478">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-6479">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-6479">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6481">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-6481">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-6482">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-6482">Mipmap</span></span> | \- |
| <span data-ttu-id="93a62-6483">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-6483">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-6484">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6484">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6486">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6486">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6488">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-6488">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-6489">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6489">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-6490">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6490">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6491">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6491">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6492">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-6492">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-6493">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-6493">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-6494">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6494">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-6495">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-6495">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-6496">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-6496">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-6497">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-6497">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-6498">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-6498">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-6499">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6499">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6500">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6500">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6501">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-6501">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6503">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6503">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6504">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6504">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6505">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-6505">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-6506">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-6506">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-6507">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6507">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-6508">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-6508">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-6509">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-6509">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-6510">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6510">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6512">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-6512">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6514">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-6514">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6516">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6516">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6518">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6518">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="93a62-6519">DXGI_FORMAT_420 不 \_ 透明的<sup>V</sup> (106) </span><span class="sxs-lookup"><span data-stu-id="93a62-6519">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="93a62-6520">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6520">Target</span></span> | <span data-ttu-id="93a62-6521">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6521">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-6522">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-6522">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-6523">8</span><span class="sxs-lookup"><span data-stu-id="93a62-6523">8</span></span> |
| <span data-ttu-id="93a62-6524">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6524">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6526">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-6526">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6527">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6527">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6528">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6528">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6529">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6529">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6530">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-6530">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-6531">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-6531">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6533">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-6533">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-6534">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-6534">TextureCube</span></span> | \- |
| <span data-ttu-id="93a62-6535">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-6535">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-6536">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6536">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-6537">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6537">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-6538">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6538">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-6539">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-6539">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-6540">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-6540">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-6541">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-6541">Mipmap</span></span> | \- |
| <span data-ttu-id="93a62-6542">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-6542">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-6543">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6543">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6544">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6544">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6545">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-6545">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-6546">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6546">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-6547">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6547">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6548">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6548">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6549">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-6549">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-6550">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-6550">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-6551">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6551">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-6552">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-6552">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-6553">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-6553">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-6554">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-6554">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-6555">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-6555">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-6556">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6556">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6557">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6557">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6558">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-6558">CPU Lockable</span></span> | \- |
| <span data-ttu-id="93a62-6559">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6559">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6560">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6560">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6561">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-6561">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-6562">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-6562">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-6563">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6563">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-6564">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-6564">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-6565">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-6565">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-6566">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6566">Video Decoder Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6568">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-6568">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6570">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-6570">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6572">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6572">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6574">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6574">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="93a62-6575">DXGI_FORMAT_YUY2<sup>V</sup> (107) </span><span class="sxs-lookup"><span data-stu-id="93a62-6575">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="93a62-6576">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6576">Target</span></span> | <span data-ttu-id="93a62-6577">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6577">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-6578">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-6578">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-6579">16</span><span class="sxs-lookup"><span data-stu-id="93a62-6579">16</span></span> |
| <span data-ttu-id="93a62-6580">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6580">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6582">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-6582">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6583">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6583">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6584">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6584">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6585">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6585">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6586">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-6586">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-6587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-6587">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-6589">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-6590">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-6590">TextureCube</span></span> | \- |
| <span data-ttu-id="93a62-6591">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-6591">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6593">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6593">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6595">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6595">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-6596">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6596">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-6597">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-6597">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6599">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-6599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-6600">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-6600">Mipmap</span></span> | \- |
| <span data-ttu-id="93a62-6601">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-6601">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-6602">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6602">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6603">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6603">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6604">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-6604">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-6605">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6605">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-6606">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6606">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6607">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6607">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6608">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-6608">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-6609">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-6609">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-6610">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6610">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-6611">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-6611">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-6612">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-6612">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-6613">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-6613">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-6614">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-6614">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-6615">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6615">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6616">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6616">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6617">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-6617">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6619">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6619">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6620">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6620">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6621">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-6621">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-6622">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-6622">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-6623">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6623">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-6624">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-6624">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-6625">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-6625">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-6626">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6626">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6628">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-6628">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6630">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-6630">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6632">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6632">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6634">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6634">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="93a62-6635">DXGI_FORMAT_Y210<sup>V</sup> (108) </span><span class="sxs-lookup"><span data-stu-id="93a62-6635">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="93a62-6636">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6636">Target</span></span> | <span data-ttu-id="93a62-6637">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6637">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-6638">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-6638">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-6639">32</span><span class="sxs-lookup"><span data-stu-id="93a62-6639">32</span></span> |
| <span data-ttu-id="93a62-6640">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6640">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6642">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-6642">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6643">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6643">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6644">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6644">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6645">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6645">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6646">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-6646">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-6647">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-6647">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6649">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-6649">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-6650">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-6650">TextureCube</span></span> | \- |
| <span data-ttu-id="93a62-6651">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-6651">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6653">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6653">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6655">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6655">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-6656">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6656">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-6657">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-6657">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6659">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-6659">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-6660">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-6660">Mipmap</span></span> | \- |
| <span data-ttu-id="93a62-6661">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-6661">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-6662">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6662">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6663">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6663">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6664">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-6664">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-6665">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6665">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-6666">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6666">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6667">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6667">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6668">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-6668">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-6669">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-6669">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-6670">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6670">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-6671">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-6671">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-6672">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-6672">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-6673">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-6673">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-6674">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-6674">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-6675">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6675">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6676">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6676">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6677">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-6677">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6679">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6679">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6680">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6680">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6681">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-6681">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-6682">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-6682">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-6683">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6683">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-6684">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-6684">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-6685">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-6685">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-6686">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6686">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6688">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-6688">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6690">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-6690">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6692">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6692">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6694">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6694">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="93a62-6695">DXGI_FORMAT_Y216<sup>V</sup> (109) </span><span class="sxs-lookup"><span data-stu-id="93a62-6695">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="93a62-6696">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6696">Target</span></span> | <span data-ttu-id="93a62-6697">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6697">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-6698">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-6698">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-6699">32</span><span class="sxs-lookup"><span data-stu-id="93a62-6699">32</span></span> |
| <span data-ttu-id="93a62-6700">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6700">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6702">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-6702">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6703">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6703">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6704">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6704">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6705">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6705">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6706">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-6706">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-6707">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-6707">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6709">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-6709">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-6710">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-6710">TextureCube</span></span> | \- |
| <span data-ttu-id="93a62-6711">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-6711">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6713">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6713">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6715">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6715">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-6716">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6716">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-6717">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-6717">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6719">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-6719">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-6720">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-6720">Mipmap</span></span> | \- |
| <span data-ttu-id="93a62-6721">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-6721">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-6722">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6722">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6723">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6723">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6724">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-6724">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-6725">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6725">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-6726">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6726">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6727">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6727">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6728">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-6728">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-6729">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-6729">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-6730">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6730">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-6731">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-6731">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-6732">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-6732">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-6733">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-6733">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-6734">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-6734">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-6735">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6735">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6736">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6736">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6737">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-6737">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6739">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6739">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6740">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6740">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6741">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-6741">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-6742">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-6742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-6743">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6743">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-6744">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-6744">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-6745">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-6745">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-6746">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6746">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6748">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-6748">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6750">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-6750">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6752">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6752">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6754">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6754">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="93a62-6755">DXGI_FORMAT_NV11<sup>V</sup> (110) </span><span class="sxs-lookup"><span data-stu-id="93a62-6755">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="93a62-6756">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6756">Target</span></span> | <span data-ttu-id="93a62-6757">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6757">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-6758">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-6758">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-6759">8</span><span class="sxs-lookup"><span data-stu-id="93a62-6759">8</span></span> |
| <span data-ttu-id="93a62-6760">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6760">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6762">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-6762">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6763">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6763">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6764">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6764">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6765">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6765">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6766">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-6766">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-6767">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-6767">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6769">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-6769">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-6770">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-6770">TextureCube</span></span> | \- |
| <span data-ttu-id="93a62-6771">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-6771">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6773">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6773">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6775">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6775">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-6776">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6776">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-6777">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-6777">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6779">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-6779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-6780">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-6780">Mipmap</span></span> | \- |
| <span data-ttu-id="93a62-6781">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-6781">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-6782">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6782">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6784">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6784">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6786">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-6786">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-6787">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6787">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-6788">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6788">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6789">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6789">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6790">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-6790">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-6791">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-6791">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-6792">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6792">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-6793">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-6793">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-6794">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-6794">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-6795">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-6795">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-6796">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-6796">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-6797">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6797">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6798">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6798">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6799">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-6799">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6801">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6801">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6802">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6802">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6803">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-6803">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-6804">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-6804">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-6805">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6805">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-6806">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-6806">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-6807">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-6807">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-6808">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6808">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6810">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-6810">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6812">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-6812">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6814">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6814">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6816">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6816">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="93a62-6817">DXGI_FORMAT_AI44<sup>V</sup> (111) </span><span class="sxs-lookup"><span data-stu-id="93a62-6817">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="93a62-6818">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6818">Target</span></span> | <span data-ttu-id="93a62-6819">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6819">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-6820">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-6820">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-6821">8</span><span class="sxs-lookup"><span data-stu-id="93a62-6821">8</span></span> |
| <span data-ttu-id="93a62-6822">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6822">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6824">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-6824">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6825">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6825">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6826">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6826">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6827">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6827">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6828">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-6828">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-6829">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-6829">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6831">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-6831">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-6832">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-6832">TextureCube</span></span> | \- |
| <span data-ttu-id="93a62-6833">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-6833">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-6834">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6834">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-6835">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6835">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-6836">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6836">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-6837">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-6837">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-6838">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-6838">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-6839">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-6839">Mipmap</span></span> | \- |
| <span data-ttu-id="93a62-6840">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-6840">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-6841">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6841">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6842">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6842">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6843">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-6843">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-6844">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6844">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-6845">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6845">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6846">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6846">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6847">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-6847">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-6848">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-6848">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-6849">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6849">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-6850">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-6850">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-6851">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-6851">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-6852">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-6852">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-6853">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-6853">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-6854">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6854">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6855">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6855">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6856">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-6856">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6858">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6858">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6859">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6859">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6860">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-6860">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-6861">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-6861">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-6862">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6862">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-6863">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-6863">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-6864">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-6864">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-6865">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6865">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-6866">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-6866">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6868">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-6868">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-6869">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6869">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-6870">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6870">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="93a62-6871">DXGI_FORMAT_IA44<sup>V</sup> (112) </span><span class="sxs-lookup"><span data-stu-id="93a62-6871">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="93a62-6872">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6872">Target</span></span> | <span data-ttu-id="93a62-6873">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6873">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-6874">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-6874">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-6875">8</span><span class="sxs-lookup"><span data-stu-id="93a62-6875">8</span></span> |
| <span data-ttu-id="93a62-6876">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6876">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6878">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-6878">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6879">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6879">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6880">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6880">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6881">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6881">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6882">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-6882">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-6883">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-6883">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6885">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-6885">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-6886">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-6886">TextureCube</span></span> | \- |
| <span data-ttu-id="93a62-6887">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-6887">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-6888">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6888">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-6889">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6889">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-6890">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6890">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-6891">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-6891">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-6892">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-6892">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-6893">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-6893">Mipmap</span></span> | \- |
| <span data-ttu-id="93a62-6894">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-6894">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-6895">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6895">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6896">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6896">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6897">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-6897">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-6898">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6898">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-6899">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6899">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6900">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6900">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6901">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-6901">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-6902">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-6902">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-6903">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6903">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-6904">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-6904">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-6905">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-6905">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-6906">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-6906">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-6907">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-6907">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-6908">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6908">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6909">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6909">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6910">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-6910">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6912">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6912">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6913">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6913">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6914">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-6914">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-6915">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-6915">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-6916">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6916">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-6917">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-6917">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-6918">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-6918">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-6919">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6919">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-6920">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-6920">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6922">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-6922">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-6923">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6923">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-6924">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6924">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="93a62-6925">DXGI_FORMAT_P8<sup>V</sup> (113) </span><span class="sxs-lookup"><span data-stu-id="93a62-6925">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="93a62-6926">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6926">Target</span></span> | <span data-ttu-id="93a62-6927">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6927">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-6928">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-6928">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-6929">8</span><span class="sxs-lookup"><span data-stu-id="93a62-6929">8</span></span> |
| <span data-ttu-id="93a62-6930">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6930">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6932">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-6932">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6933">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6933">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6934">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6934">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6935">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6935">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6936">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-6936">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-6937">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-6937">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6939">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-6939">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-6940">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-6940">TextureCube</span></span> | \- |
| <span data-ttu-id="93a62-6941">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-6941">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-6942">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6942">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-6943">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6943">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-6944">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6944">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-6945">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-6945">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-6946">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-6946">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-6947">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-6947">Mipmap</span></span> | \- |
| <span data-ttu-id="93a62-6948">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-6948">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-6949">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6949">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6950">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6950">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6951">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-6951">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-6952">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6952">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-6953">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6953">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6954">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-6954">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-6955">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-6955">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-6956">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-6956">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-6957">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6957">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-6958">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-6958">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-6959">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-6959">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-6960">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-6960">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-6961">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-6961">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-6962">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6962">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6963">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-6963">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-6964">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-6964">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6966">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6966">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6967">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-6967">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-6968">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-6968">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-6969">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-6969">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-6970">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-6970">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-6971">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-6971">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-6972">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-6972">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-6973">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6973">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-6974">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-6974">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6976">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-6976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-6977">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6977">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-6978">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-6978">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="93a62-6979">DXGI_FORMAT_A8P8<sup>V</sup> (114) </span><span class="sxs-lookup"><span data-stu-id="93a62-6979">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="93a62-6980">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-6980">Target</span></span> | <span data-ttu-id="93a62-6981">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6981">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-6982">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-6982">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-6983">16</span><span class="sxs-lookup"><span data-stu-id="93a62-6983">16</span></span> |
| <span data-ttu-id="93a62-6984">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-6984">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-6986">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-6986">Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6987">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6987">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6988">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6988">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6989">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-6989">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-6990">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-6990">Texture1D</span></span> | \- |
| <span data-ttu-id="93a62-6991">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-6991">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-6993">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-6993">Texture3D</span></span> | \- |
| <span data-ttu-id="93a62-6994">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-6994">TextureCube</span></span> | \- |
| <span data-ttu-id="93a62-6995">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-6995">Shader ld</span></span> | \- |
| <span data-ttu-id="93a62-6996">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6996">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="93a62-6997">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6997">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-6998">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-6998">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-6999">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-6999">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-7000">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-7000">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-7001">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-7001">Mipmap</span></span> | \- |
| <span data-ttu-id="93a62-7002">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-7002">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="93a62-7003">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-7003">RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-7004">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-7004">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-7005">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-7005">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-7006">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-7006">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-7007">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-7007">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-7008">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-7008">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-7009">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-7009">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-7010">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-7010">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-7011">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-7011">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-7012">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-7012">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-7013">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-7013">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-7014">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-7014">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-7015">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-7015">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-7016">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-7016">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-7017">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-7017">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-7018">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-7018">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-7020">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-7020">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-7021">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-7021">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="93a62-7022">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-7022">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="93a62-7023">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-7023">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="93a62-7024">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-7024">Multisample Load</span></span> | \- |
| <span data-ttu-id="93a62-7025">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-7025">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-7026">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-7026">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-7027">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-7027">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-7028">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-7028">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-7030">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-7030">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-7031">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-7031">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-7032">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-7032">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="93a62-7033">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115) </span><span class="sxs-lookup"><span data-stu-id="93a62-7033">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="93a62-7034">目標</span><span class="sxs-lookup"><span data-stu-id="93a62-7034">Target</span></span> | <span data-ttu-id="93a62-7035">支援</span><span class="sxs-lookup"><span data-stu-id="93a62-7035">Support</span></span> |
| - | - |
| <span data-ttu-id="93a62-7036">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="93a62-7036">Bits Per Element (BPE)</span></span> | <span data-ttu-id="93a62-7037">16</span><span class="sxs-lookup"><span data-stu-id="93a62-7037">16</span></span> |
| <span data-ttu-id="93a62-7038">格式支援</span><span class="sxs-lookup"><span data-stu-id="93a62-7038">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-7040">Buffer</span><span class="sxs-lookup"><span data-stu-id="93a62-7040">Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-7042">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-7042">Input Assembler Vertex Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-7044">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-7044">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="93a62-7045">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="93a62-7045">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="93a62-7046">Texture1D</span><span class="sxs-lookup"><span data-stu-id="93a62-7046">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-7048">Texture2D</span><span class="sxs-lookup"><span data-stu-id="93a62-7048">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-7050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="93a62-7050">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-7052">TextureCube</span><span class="sxs-lookup"><span data-stu-id="93a62-7052">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-7054">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="93a62-7054">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-7056">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-7056">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-7058">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-7058">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="93a62-7059">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="93a62-7059">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="93a62-7060">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="93a62-7060">Shader gather4</span></span> | \- |
| <span data-ttu-id="93a62-7061">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="93a62-7061">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="93a62-7062">Mipmap</span><span class="sxs-lookup"><span data-stu-id="93a62-7062">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-7064">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="93a62-7064">Mipmap Auto-Generation</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-7066">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-7066">RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-7068">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-7068">Blendable RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-7070">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="93a62-7070">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="93a62-7071">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="93a62-7071">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="93a62-7072">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-7072">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-7073">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="93a62-7073">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="93a62-7074">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="93a62-7074">Typed UAV</span></span> | \- |
| <span data-ttu-id="93a62-7075">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="93a62-7075">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="93a62-7076">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="93a62-7076">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="93a62-7077">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="93a62-7077">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="93a62-7078">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="93a62-7078">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="93a62-7079">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="93a62-7079">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="93a62-7080">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="93a62-7080">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="93a62-7081">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-7081">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-7082">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="93a62-7082">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="93a62-7083">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="93a62-7083">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-7085">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-7085">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-7087">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="93a62-7087">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-7089">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="93a62-7089">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-7091">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="93a62-7091">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="93a62-7093">多級載入</span><span class="sxs-lookup"><span data-stu-id="93a62-7093">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="93a62-7095">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="93a62-7095">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="93a62-7096">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="93a62-7096">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="93a62-7097">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="93a62-7097">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="93a62-7098">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="93a62-7098">Video Processor Input</span></span> | \- |
| <span data-ttu-id="93a62-7099">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="93a62-7099">Video Processor Output</span></span> | \- |
| <span data-ttu-id="93a62-7100">共用資源</span><span class="sxs-lookup"><span data-stu-id="93a62-7100">Shared Resource</span></span> | \- |
| <span data-ttu-id="93a62-7101">磚資源</span><span class="sxs-lookup"><span data-stu-id="93a62-7101">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="93a62-7102">格式化附注</span><span class="sxs-lookup"><span data-stu-id="93a62-7102">Format notes</span></span>

<span data-ttu-id="93a62-7103">格式的用途可從一個硬體功能層級變更為下一個硬體功能層級。</span><span class="sxs-lookup"><span data-stu-id="93a62-7103">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="93a62-7104"><sup>L</sup> ：無格式的格式</span><span class="sxs-lookup"><span data-stu-id="93a62-7104"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="93a62-7105"><sup>電腦</sup> ：部分類型、可轉換和簡單版面配置</span><span class="sxs-lookup"><span data-stu-id="93a62-7105"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="93a62-7106"><sup>FCS</sup> ：完整型別、可轉換和 simple 版面配置</span><span class="sxs-lookup"><span data-stu-id="93a62-7106"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="93a62-7107"><sup>FNS</sup> ：完全具類型、非可轉換和簡單版面配置</span><span class="sxs-lookup"><span data-stu-id="93a62-7107"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="93a62-7108"><sup>PCC</sup> ：部分類型、可轉換和複雜版面配置</span><span class="sxs-lookup"><span data-stu-id="93a62-7108"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="93a62-7109"><sup>FCC</sup> ：完整型別、可轉換和複雜的版面配置</span><span class="sxs-lookup"><span data-stu-id="93a62-7109"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="93a62-7110"><sup>FNC</sup> ：完整型別、非可轉換和複雜的版面配置</span><span class="sxs-lookup"><span data-stu-id="93a62-7110"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="93a62-7111"><sup>V</sup> ：影片格式</span><span class="sxs-lookup"><span data-stu-id="93a62-7111"><sup>V</sup> : video format</span></span>
</dt> </dl>

<span data-ttu-id="93a62-7112">使用 [**DXGI \_ 格式 \_ R16G16B16A16 \_ FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式的背景緩衝區和掃描輸出包含線性值 gamma 資料。</span><span class="sxs-lookup"><span data-stu-id="93a62-7112">Back buffers and scan outs with the [**DXGI\_FORMAT\_R16G16B16A16\_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format contain linear-valued gamma data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93a62-7113">相關主題</span><span class="sxs-lookup"><span data-stu-id="93a62-7113">Related topics</span></span>

[<span data-ttu-id="93a62-7114">D3D12 硬體功能等級</span><span class="sxs-lookup"><span data-stu-id="93a62-7114">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="93a62-7115">**ID3D10Device::CheckFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="93a62-7115">**ID3D10Device::CheckFormatSupport**</span></span>](/windows/win32/api/d3d10/nf-d3d10-id3d10device-checkformatsupport)

[<span data-ttu-id="93a62-7116">DXGI 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="93a62-7116">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
