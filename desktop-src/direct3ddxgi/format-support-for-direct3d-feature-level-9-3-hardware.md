---
description: 本節指定 Direct3D Feature 10Level9 9.3 硬體支援的格式 ([ **DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)值) 。
ms.assetid: B2A843D5-6A6B-4180-8B94-D032B1322798
title: Direct3D 功能 10Level9 9.3 硬體的格式支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79185ddb360fe9359371671e3722372c3a1615f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025652"
---
# <a name="format-support-for-direct3d-feature-10level9-93-hardware"></a><span data-ttu-id="6e083-103">Direct3D 功能 10Level9 9.3 硬體的格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-103">Format support for Direct3D Feature 10Level9 9.3 hardware</span></span>

<span data-ttu-id="6e083-104">本節指定 Direct3D Feature 10Level9 9.3 硬體支援的格式 ([ _\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)值) 。</span><span class="sxs-lookup"><span data-stu-id="6e083-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature 10Level9 9.3 hardware.</span></span>

<span data-ttu-id="6e083-105">下表摘要說明使用下列索引鍵的功能支援。</span><span class="sxs-lookup"><span data-stu-id="6e083-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="6e083-106">符號</span><span class="sxs-lookup"><span data-stu-id="6e083-106">Symbol</span></span>                            | <span data-ttu-id="6e083-107">描述</span><span class="sxs-lookup"><span data-stu-id="6e083-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="6e083-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="6e083-108">_ *-*\*</span></span>                             | <span data-ttu-id="6e083-109">不允許或無法使用。</span><span class="sxs-lookup"><span data-stu-id="6e083-109">Disallowed or not available.</span></span>                                                  |
| ![必要](images/letter-r.jpg)  | <span data-ttu-id="6e083-111">需要硬體支援。</span><span class="sxs-lookup"><span data-stu-id="6e083-111">Hardware support is required.</span></span>                                                 |
| ![選用](images/letter-o.jpg)  | <span data-ttu-id="6e083-113">硬體支援是選擇性的，格式可能或可能不會有硬體加速。</span><span class="sxs-lookup"><span data-stu-id="6e083-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![依賴](images/letter-d.jpg) | <span data-ttu-id="6e083-115">如果支援相關的選擇性功能，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="6e083-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="6e083-116">本主題包含每一種格式的區段。</span><span class="sxs-lookup"><span data-stu-id="6e083-116">This topic contains a section per format.</span></span> <span data-ttu-id="6e083-117">格式 *目標* (資料表每個目標各包含一個資料列) 可以是資源類型、HLSL 內建函式，或是相依于特定格式的特定功能。</span><span class="sxs-lookup"><span data-stu-id="6e083-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="6e083-118">若要以程式設計方式驗證 D3D11 和 D3D12 中的格式支援，請參閱 [檢查硬體功能支援](checking-hardware-feature-support.md)。</span><span class="sxs-lookup"><span data-stu-id="6e083-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="6e083-119">這些格式的數目大多是（但不是全部），以遞增的數值順序來 &mdash; 看，有些會超出數值順序，並與其他相關的格式一起列出。</span><span class="sxs-lookup"><span data-stu-id="6e083-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="6e083-120">另請注意 *，格式名稱的無* 型別可以表示 *部分* 具型別，而不是嚴格的無型別 (請參閱主題結尾的 [格式附注](#format-notes) 章節) 。</span><span class="sxs-lookup"><span data-stu-id="6e083-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="6e083-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0) </span><span class="sxs-lookup"><span data-stu-id="6e083-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="6e083-122">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-122">Target</span></span> | <span data-ttu-id="6e083-123">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-123">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-124">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-125">0</span><span class="sxs-lookup"><span data-stu-id="6e083-125">0</span></span> |
| <span data-ttu-id="6e083-126">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-126">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-127">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-127">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-128">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-128">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-129">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-129">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-130">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-130">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-131">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-131">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-132">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-132">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-133">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-134">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-135">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-135">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-136">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-137">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-138">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-139">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-139">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-140">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-141">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-141">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-142">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-143">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-144">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-145">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-146">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-147">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-148">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-149">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-149">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-150">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-151">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-152">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-153">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-154">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-154">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-155">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-156">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-157">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-158">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-158">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-159">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-159">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-160">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-160">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-161">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-161">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-162">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-163">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-163">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-164">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-165">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-166">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-167">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-168">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-169">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-169">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-170">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="6e083-171">DXGI_FORMAT_R32G32B32A32 無的 \_ <sup>電腦</sup> (1) </span><span class="sxs-lookup"><span data-stu-id="6e083-171">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="6e083-172">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-172">Target</span></span> | <span data-ttu-id="6e083-173">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-173">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-174">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-175">128</span><span class="sxs-lookup"><span data-stu-id="6e083-175">128</span></span> |
| <span data-ttu-id="6e083-176">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-176">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-177">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-177">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-178">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-178">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-179">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-179">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-180">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-180">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-181">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-181">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-182">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-182">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-183">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-184">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-185">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-185">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-186">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-186">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-187">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-187">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-188">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-188">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-189">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-189">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-190">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-190">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-191">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-191">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-192">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-192">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-193">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-193">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-194">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-194">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-195">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-195">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-196">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-196">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-197">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-197">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-198">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-198">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-199">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-199">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-200">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-200">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-201">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-201">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-202">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-202">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-203">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-203">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-204">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-204">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-205">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-205">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-206">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-206">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-207">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-207">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-208">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-208">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-209">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-209">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-210">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-210">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-211">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-211">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-212">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-212">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-213">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-213">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-214">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-214">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-215">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-215">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-216">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-216">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-217">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-217">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-218">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-218">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-219">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-219">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-220">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-220">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a><span data-ttu-id="6e083-221">DXGI_FORMAT_R32G32B32A32 \_ FLOAT<sup>FNS</sup> (2) </span><span class="sxs-lookup"><span data-stu-id="6e083-221">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FNS</sup> (2)</span></span>
| <span data-ttu-id="6e083-222">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-222">Target</span></span> | <span data-ttu-id="6e083-223">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-223">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-224">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-224">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-225">128</span><span class="sxs-lookup"><span data-stu-id="6e083-225">128</span></span> |
| <span data-ttu-id="6e083-226">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-226">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-228">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-228">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-229">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-229">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-231">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-232">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-233">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-234">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-234">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-236">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-236">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-238">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-238">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-240">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-240">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-242">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-242">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-243">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-243">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-244">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-244">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-245">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-245">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-246">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-246">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-247">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-247">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-249">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-249">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-251">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-251">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-253">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-253">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-254">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-254">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-255">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-255">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-256">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-256">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-257">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-257">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-258">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-258">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-259">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-259">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-260">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-260">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-261">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-261">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-262">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-262">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-263">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-263">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-264">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-264">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-265">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-265">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-266">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-266">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-267">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-267">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-269">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-269">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-271">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-271">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-273">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-273">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-275">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-275">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-277">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-277">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-278">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-278">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-279">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-279">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-280">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-280">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-281">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-281">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-282">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-282">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-283">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-283">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-284">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-284">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a><span data-ttu-id="6e083-285">DXGI_FORMAT_R32G32B32A32 \_ UINT<sup>FNS</sup> (3) </span><span class="sxs-lookup"><span data-stu-id="6e083-285">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FNS</sup> (3)</span></span>
| <span data-ttu-id="6e083-286">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-286">Target</span></span> | <span data-ttu-id="6e083-287">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-287">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-288">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-288">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-289">128</span><span class="sxs-lookup"><span data-stu-id="6e083-289">128</span></span> |
| <span data-ttu-id="6e083-290">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-290">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-291">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-291">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-292">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-292">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-293">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-293">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-294">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-294">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-295">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-295">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-296">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-296">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-297">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-297">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-298">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-298">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-299">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-299">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-300">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-300">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-301">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-301">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-302">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-302">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-303">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-303">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-304">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-304">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-305">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-305">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-306">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-306">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-307">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-307">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-308">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-308">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-309">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-309">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-310">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-310">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-311">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-311">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-312">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-312">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-313">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-313">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-314">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-314">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-315">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-315">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-316">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-316">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-317">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-317">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-318">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-318">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-319">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-319">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-320">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-320">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-321">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-321">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-322">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-322">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-323">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-323">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-324">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-324">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-325">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-325">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-326">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-326">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-327">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-327">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-328">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-328">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-329">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-329">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-330">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-330">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-331">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-331">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-332">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-332">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-333">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-333">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-334">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-334">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a><span data-ttu-id="6e083-335">DXGI_FORMAT_R32G32B32A32 \_ 聖<sup>FNS</sup> (4) </span><span class="sxs-lookup"><span data-stu-id="6e083-335">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FNS</sup> (4)</span></span>
| <span data-ttu-id="6e083-336">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-336">Target</span></span> | <span data-ttu-id="6e083-337">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-337">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-338">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-338">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-339">128</span><span class="sxs-lookup"><span data-stu-id="6e083-339">128</span></span> |
| <span data-ttu-id="6e083-340">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-340">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-341">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-341">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-342">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-342">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-343">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-343">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-344">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-344">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-345">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-345">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-346">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-346">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-347">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-347">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-348">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-349">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-349">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-350">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-350">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-351">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-351">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-352">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-352">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-353">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-353">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-354">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-354">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-355">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-355">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-356">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-356">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-357">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-357">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-358">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-358">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-359">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-359">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-360">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-360">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-361">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-361">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-362">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-362">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-363">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-363">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-364">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-364">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-365">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-365">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-366">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-366">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-367">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-367">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-368">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-368">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-369">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-369">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-370">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-370">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-371">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-371">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-372">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-372">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-373">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-373">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-374">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-374">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-375">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-375">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-376">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-376">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-377">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-377">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-378">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-378">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-379">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-379">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-380">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-380">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-381">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-381">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-382">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-382">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-383">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-383">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-384">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-384">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="6e083-385">DXGI_FORMAT_R32G32B32 無的 \_ <sup>電腦</sup> (5) </span><span class="sxs-lookup"><span data-stu-id="6e083-385">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="6e083-386">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-386">Target</span></span> | <span data-ttu-id="6e083-387">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-387">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-388">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-388">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-389">96</span><span class="sxs-lookup"><span data-stu-id="6e083-389">96</span></span> |
| <span data-ttu-id="6e083-390">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-390">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-391">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-391">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-392">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-392">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-393">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-393">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-394">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-394">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-395">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-395">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-396">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-396">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-397">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-397">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-398">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-398">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-399">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-399">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-400">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-401">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-401">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-402">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-402">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-403">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-403">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-404">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-404">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-405">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-405">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-406">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-406">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-407">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-407">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-408">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-409">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-410">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-411">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-412">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-413">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-414">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-415">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-416">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-417">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-418">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-418">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-419">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-420">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-421">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-422">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-422">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-423">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-423">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-424">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-424">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-425">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-425">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-426">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-426">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-427">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-427">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-428">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-428">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-429">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-429">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-430">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-430">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-431">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-431">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-432">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-432">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-433">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-433">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-434">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-434">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a><span data-ttu-id="6e083-435">DXGI_FORMAT_R32G32B32 \_ FLOAT<sup>FNS</sup> (6) </span><span class="sxs-lookup"><span data-stu-id="6e083-435">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FNS</sup> (6)</span></span>
| <span data-ttu-id="6e083-436">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-436">Target</span></span> | <span data-ttu-id="6e083-437">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-437">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-438">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-438">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-439">96</span><span class="sxs-lookup"><span data-stu-id="6e083-439">96</span></span> |
| <span data-ttu-id="6e083-440">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-440">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-442">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-442">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-443">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-443">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-445">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-446">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-447">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-448">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-449">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-449">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-450">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-450">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-451">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-451">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-452">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-452">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-453">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-454">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-455">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-455">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-456">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-457">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-457">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-458">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-458">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-459">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-459">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-460">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-460">Blendable RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="6e083-462">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-462">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-463">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-463">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-464">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-464">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-465">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-465">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-466">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-466">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-467">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-467">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-468">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-468">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-469">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-469">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-470">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-470">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-471">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-471">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-472">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-472">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-473">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-473">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-474">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-474">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-475">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-475">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-476">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-476">4x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="6e083-478">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-478">8x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="6e083-480">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-480">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-481">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-481">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-482">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-482">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-483">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-483">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-484">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-484">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-485">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-485">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-486">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-486">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-487">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-487">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-488">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-488">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-489">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-489">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a><span data-ttu-id="6e083-490">DXGI_FORMAT_R32G32B32 \_ UINT<sup>FNS</sup> (7) </span><span class="sxs-lookup"><span data-stu-id="6e083-490">DXGI_FORMAT_R32G32B32\_UINT<sup>FNS</sup> (7)</span></span>
| <span data-ttu-id="6e083-491">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-491">Target</span></span> | <span data-ttu-id="6e083-492">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-492">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-493">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-493">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-494">96</span><span class="sxs-lookup"><span data-stu-id="6e083-494">96</span></span> |
| <span data-ttu-id="6e083-495">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-495">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-496">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-496">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-497">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-498">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-499">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-500">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-501">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-502">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-502">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-503">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-503">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-504">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-504">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-505">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-505">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-506">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-507">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-508">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-508">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-509">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-510">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-510">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-511">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-511">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-512">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-512">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-513">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-513">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-514">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-514">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-515">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-515">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-516">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-516">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-517">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-517">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-518">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-518">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-519">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-519">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-520">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-520">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-521">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-521">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-522">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-522">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-523">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-523">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-524">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-524">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-525">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-525">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-526">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-526">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-527">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-527">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-528">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-528">4x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="6e083-530">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-530">8x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="6e083-532">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-533">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-534">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-534">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-535">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-536">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-537">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-538">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-539">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-540">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-540">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-541">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a><span data-ttu-id="6e083-542">DXGI_FORMAT_R32G32B32 \_ 聖<sup>FNS</sup> (8) </span><span class="sxs-lookup"><span data-stu-id="6e083-542">DXGI_FORMAT_R32G32B32\_SINT<sup>FNS</sup> (8)</span></span>
| <span data-ttu-id="6e083-543">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-543">Target</span></span> | <span data-ttu-id="6e083-544">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-544">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-545">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-546">96</span><span class="sxs-lookup"><span data-stu-id="6e083-546">96</span></span> |
| <span data-ttu-id="6e083-547">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-547">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-548">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-548">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-549">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-550">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-551">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-552">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-553">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-554">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-555">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-556">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-557">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-558">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-559">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-560">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-560">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-561">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-562">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-562">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-563">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-564">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-565">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-566">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-567">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-568">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-569">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-570">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-570">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-571">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-572">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-573">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-574">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-575">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-576">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-577">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-578">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-579">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-580">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-580">4x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="6e083-582">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-582">8x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="6e083-584">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-584">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-585">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-585">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-586">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-586">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-587">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-587">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-588">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-588">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-589">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-590">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-591">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-592">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-592">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-593">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-593">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="6e083-594">DXGI_FORMAT_R16G16B16A16 無別 \_ <sup>電腦</sup> (9) </span><span class="sxs-lookup"><span data-stu-id="6e083-594">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="6e083-595">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-595">Target</span></span> | <span data-ttu-id="6e083-596">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-596">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-597">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-597">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-598">64</span><span class="sxs-lookup"><span data-stu-id="6e083-598">64</span></span> |
| <span data-ttu-id="6e083-599">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-599">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-600">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-600">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-601">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-601">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-602">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-602">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-603">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-603">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-604">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-604">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-605">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-605">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-606">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-606">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-607">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-607">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-608">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-608">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-609">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-609">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-610">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-610">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-611">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-611">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-612">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-612">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-613">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-613">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-614">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-614">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-615">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-615">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-616">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-616">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-617">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-617">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-618">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-618">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-619">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-619">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-620">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-620">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-621">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-621">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-622">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-622">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-623">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-623">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-624">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-624">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-625">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-625">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-626">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-626">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-627">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-627">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-628">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-628">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-629">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-629">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-630">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-630">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-631">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-631">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-632">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-632">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-633">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-633">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-634">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-634">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-635">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-635">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-636">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-636">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-637">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-637">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-638">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-638">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-639">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-639">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-640">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-640">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-641">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-641">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-642">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-642">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-643">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-643">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a><span data-ttu-id="6e083-644">DXGI_FORMAT_R16G16B16A16 \_ FLOAT<sup>FNS</sup> (10) </span><span class="sxs-lookup"><span data-stu-id="6e083-644">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FNS</sup> (10)</span></span>
| <span data-ttu-id="6e083-645">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-645">Target</span></span> | <span data-ttu-id="6e083-646">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-646">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-647">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-647">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-648">64</span><span class="sxs-lookup"><span data-stu-id="6e083-648">64</span></span> |
| <span data-ttu-id="6e083-649">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-649">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-651">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-651">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-652">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-652">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-654">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-654">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-655">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-655">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-656">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-656">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-657">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-657">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-659">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-659">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-661">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-661">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-663">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-663">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-665">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-665">Shader sample (any filter)</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-667">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-667">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-668">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-668">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-669">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-669">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-670">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-670">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-671">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-671">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-673">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-673">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-675">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-675">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-677">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-677">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-679">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-679">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-680">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-680">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-681">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-681">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-682">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-682">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-683">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-683">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-684">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-684">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-685">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-685">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-686">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-686">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-687">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-687">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-688">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-688">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-689">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-689">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-690">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-690">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-691">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-691">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-692">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-692">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-694">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-694">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-696">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-696">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-698">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-698">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-700">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-700">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-702">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-702">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-703">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-703">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-704">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-704">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-705">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-705">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-706">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-706">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-707">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-707">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-708">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-708">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-710">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-710">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a><span data-ttu-id="6e083-711">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FNS</sup> (11) </span><span class="sxs-lookup"><span data-stu-id="6e083-711">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FNS</sup> (11)</span></span>
| <span data-ttu-id="6e083-712">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-712">Target</span></span> | <span data-ttu-id="6e083-713">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-713">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-714">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-714">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-715">64</span><span class="sxs-lookup"><span data-stu-id="6e083-715">64</span></span> |
| <span data-ttu-id="6e083-716">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-716">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-718">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-718">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-719">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-719">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-720">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-720">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-721">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-721">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-722">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-722">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-723">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-723">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-725">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-725">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-727">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-727">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-729">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-729">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-731">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-731">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-733">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-733">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-734">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-734">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-735">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-735">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-736">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-736">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-737">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-737">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-739">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-739">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-741">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-741">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-743">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-743">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-744">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-744">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-745">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-745">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-746">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-746">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-747">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-747">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-748">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-748">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-749">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-749">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-750">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-750">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-751">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-751">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-752">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-752">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-753">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-753">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-754">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-754">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-755">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-755">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-756">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-756">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-757">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-757">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-759">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-759">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-761">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-761">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-763">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-763">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-765">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-765">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-767">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-767">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-768">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-768">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-769">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-769">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-770">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-770">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-771">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-771">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-772">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-772">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-773">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-773">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-774">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-774">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a><span data-ttu-id="6e083-775">DXGI_FORMAT_R16G16B16A16 \_ UINT<sup>FNS</sup> (12) </span><span class="sxs-lookup"><span data-stu-id="6e083-775">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FNS</sup> (12)</span></span>
| <span data-ttu-id="6e083-776">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-776">Target</span></span> | <span data-ttu-id="6e083-777">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-777">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-778">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-778">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-779">64</span><span class="sxs-lookup"><span data-stu-id="6e083-779">64</span></span> |
| <span data-ttu-id="6e083-780">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-780">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-781">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-781">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-782">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-782">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-783">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-783">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-784">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-784">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-785">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-785">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-786">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-786">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-787">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-787">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-788">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-788">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-789">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-789">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-790">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-790">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-791">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-791">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-792">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-792">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-793">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-793">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-794">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-794">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-795">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-795">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-796">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-796">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-797">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-797">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-798">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-798">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-799">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-799">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-800">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-800">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-801">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-801">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-802">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-802">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-803">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-803">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-804">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-804">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-805">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-805">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-806">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-806">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-807">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-807">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-808">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-808">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-809">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-809">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-810">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-810">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-811">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-811">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-812">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-812">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-813">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-813">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-814">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-814">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-815">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-815">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-816">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-816">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-817">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-817">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-818">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-818">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-819">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-819">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-820">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-820">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-821">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-821">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-822">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-822">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-823">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-823">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-824">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-824">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a><span data-ttu-id="6e083-825">DXGI_FORMAT_R16G16B16A16 \_ SNORM<sup>FNS</sup> (13) </span><span class="sxs-lookup"><span data-stu-id="6e083-825">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FNS</sup> (13)</span></span>
| <span data-ttu-id="6e083-826">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-826">Target</span></span> | <span data-ttu-id="6e083-827">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-827">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-828">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-828">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-829">64</span><span class="sxs-lookup"><span data-stu-id="6e083-829">64</span></span> |
| <span data-ttu-id="6e083-830">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-830">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-832">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-832">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-833">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-833">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-835">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-835">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-836">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-836">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-837">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-837">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-838">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-838">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-839">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-839">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-840">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-840">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-841">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-841">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-842">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-842">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-843">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-843">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-844">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-844">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-845">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-845">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-846">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-846">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-847">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-847">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-848">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-848">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-849">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-849">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-850">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-850">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-851">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-851">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-852">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-852">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-853">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-853">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-854">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-854">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-855">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-855">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-856">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-856">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-857">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-857">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-858">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-858">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-859">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-859">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-860">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-860">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-861">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-861">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-862">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-862">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-863">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-863">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-864">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-864">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-865">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-865">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-866">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-866">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-867">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-867">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-868">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-868">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-869">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-869">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-870">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-870">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-871">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-871">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-872">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-872">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-873">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-873">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-874">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-874">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-875">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-875">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-876">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-876">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a><span data-ttu-id="6e083-877">DXGI_FORMAT_R16G16B16A16 \_ 聖<sup>FNS</sup> (14) </span><span class="sxs-lookup"><span data-stu-id="6e083-877">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FNS</sup> (14)</span></span>
| <span data-ttu-id="6e083-878">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-878">Target</span></span> | <span data-ttu-id="6e083-879">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-879">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-880">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-880">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-881">64</span><span class="sxs-lookup"><span data-stu-id="6e083-881">64</span></span> |
| <span data-ttu-id="6e083-882">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-882">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-884">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-884">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-885">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-885">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-887">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-887">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-888">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-888">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-889">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-889">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-890">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-890">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-891">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-891">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-892">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-893">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-893">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-894">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-894">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-895">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-895">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-896">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-896">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-897">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-897">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-898">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-898">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-899">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-899">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-900">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-900">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-901">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-901">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-902">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-902">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-903">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-903">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-904">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-904">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-905">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-905">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-906">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-906">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-907">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-907">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-908">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-908">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-909">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-909">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-910">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-910">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-911">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-911">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-912">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-912">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-913">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-913">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-914">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-914">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-915">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-915">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-916">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-916">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-917">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-917">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-918">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-918">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-919">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-919">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-920">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-920">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-921">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-921">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-922">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-922">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-923">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-923">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-924">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-924">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-925">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-925">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-926">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-926">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-927">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-927">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-928">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="6e083-929">DXGI_FORMAT_R32G32 無別 \_ <sup>電腦</sup> (15) </span><span class="sxs-lookup"><span data-stu-id="6e083-929">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="6e083-930">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-930">Target</span></span> | <span data-ttu-id="6e083-931">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-931">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-932">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-933">64</span><span class="sxs-lookup"><span data-stu-id="6e083-933">64</span></span> |
| <span data-ttu-id="6e083-934">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-934">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-935">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-935">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-936">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-936">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-937">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-937">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-938">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-938">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-939">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-939">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-940">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-940">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-941">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-941">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-942">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-942">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-943">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-943">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-944">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-944">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-945">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-945">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-946">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-946">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-947">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-947">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-948">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-948">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-949">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-949">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-950">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-950">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-951">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-951">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-952">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-952">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-953">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-953">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-954">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-954">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-955">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-955">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-956">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-956">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-957">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-957">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-958">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-958">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-959">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-959">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-960">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-960">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-961">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-961">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-962">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-962">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-963">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-963">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-964">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-964">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-965">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-965">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-966">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-966">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-967">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-967">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-968">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-968">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-969">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-969">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-970">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-970">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-971">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-971">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-972">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-972">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-973">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-973">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-974">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-974">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-975">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-975">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-976">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-977">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-977">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-978">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-978">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a><span data-ttu-id="6e083-979">DXGI_FORMAT_R32G32 \_ FLOAT<sup>FNS</sup> (16) </span><span class="sxs-lookup"><span data-stu-id="6e083-979">DXGI_FORMAT_R32G32\_FLOAT<sup>FNS</sup> (16)</span></span>
| <span data-ttu-id="6e083-980">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-980">Target</span></span> | <span data-ttu-id="6e083-981">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-981">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-982">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-982">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-983">64</span><span class="sxs-lookup"><span data-stu-id="6e083-983">64</span></span> |
| <span data-ttu-id="6e083-984">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-984">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-986">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-986">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-987">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-987">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-989">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-990">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-991">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-992">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-992">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-994">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-994">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-996">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-996">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-998">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-998">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1000">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1000">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-1001">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1001">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1002">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1002">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1003">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1003">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1004">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1004">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1005">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1005">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-1006">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1006">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-1007">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1007">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1009">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1009">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1010">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1010">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1011">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1011">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1012">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1012">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1013">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1013">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1014">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1014">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1015">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1015">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1016">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1016">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1017">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1017">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1018">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1018">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1019">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1019">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1020">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1020">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1021">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1021">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1022">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1022">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1023">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1023">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1025">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1025">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-1027">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1027">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-1029">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1029">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-1031">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1031">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1033">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1033">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1034">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1034">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-1035">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1035">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1036">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1036">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1037">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1037">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-1038">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1038">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-1039">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1039">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-1040">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1040">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a><span data-ttu-id="6e083-1041">DXGI_FORMAT_R32G32 \_ UINT<sup>FNS</sup> (17) </span><span class="sxs-lookup"><span data-stu-id="6e083-1041">DXGI_FORMAT_R32G32\_UINT<sup>FNS</sup> (17)</span></span>
| <span data-ttu-id="6e083-1042">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1042">Target</span></span> | <span data-ttu-id="6e083-1043">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1043">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1044">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1044">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1045">64</span><span class="sxs-lookup"><span data-stu-id="6e083-1045">64</span></span> |
| <span data-ttu-id="6e083-1046">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1046">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-1047">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1047">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1048">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1048">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1049">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1049">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1050">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1050">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1051">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1051">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1052">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1052">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-1053">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1053">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-1054">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1054">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-1055">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1055">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-1056">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1056">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-1057">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1057">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1058">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1058">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1059">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1059">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1060">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1060">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1061">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1061">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-1062">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1062">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-1063">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1063">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1064">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1064">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1065">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1065">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1066">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1066">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1067">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1067">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1068">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1068">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1069">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1069">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1070">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1070">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1071">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1071">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1072">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1072">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1073">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1073">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1074">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1074">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1075">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1075">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1076">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1076">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1077">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1077">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1078">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1078">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-1079">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1079">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1080">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1080">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1081">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1081">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-1082">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1082">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-1083">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1083">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1084">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1084">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-1085">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1085">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1086">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1086">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1087">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1087">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-1088">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1088">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-1089">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1089">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-1090">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1090">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a><span data-ttu-id="6e083-1091">DXGI_FORMAT_R32G32 \_ 聖<sup>FNS</sup> (18) </span><span class="sxs-lookup"><span data-stu-id="6e083-1091">DXGI_FORMAT_R32G32\_SINT<sup>FNS</sup> (18)</span></span>
| <span data-ttu-id="6e083-1092">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1092">Target</span></span> | <span data-ttu-id="6e083-1093">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1093">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1094">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1094">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1095">64</span><span class="sxs-lookup"><span data-stu-id="6e083-1095">64</span></span> |
| <span data-ttu-id="6e083-1096">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1096">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-1097">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1097">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1098">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1098">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1099">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1099">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1100">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1100">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1101">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1101">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1102">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1102">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-1103">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1103">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-1104">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1104">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-1105">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1105">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-1106">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1106">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-1107">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1107">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1108">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1108">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1109">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1109">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1110">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1110">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1111">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1111">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-1112">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1112">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-1113">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1113">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1114">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1114">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1115">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1115">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1116">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1116">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1117">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1117">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1118">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1118">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1119">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1119">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1120">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1120">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1121">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1121">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1122">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1122">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1123">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1123">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1124">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1124">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1125">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1125">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1126">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1126">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1127">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1127">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1128">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1128">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-1129">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1129">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1130">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1130">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1131">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1131">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-1132">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1132">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-1133">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1133">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1134">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1134">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-1135">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1135">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1136">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1136">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1137">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1137">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-1138">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1138">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-1139">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1139">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-1140">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1140">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="6e083-1141">DXGI_FORMAT_R32G8X24 無別 \_ <sup>電腦</sup> (19) </span><span class="sxs-lookup"><span data-stu-id="6e083-1141">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="6e083-1142">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1142">Target</span></span> | <span data-ttu-id="6e083-1143">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1143">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1144">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1144">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1145">64</span><span class="sxs-lookup"><span data-stu-id="6e083-1145">64</span></span> |
| <span data-ttu-id="6e083-1146">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1146">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-1147">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1147">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1148">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1148">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1149">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1149">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1150">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1150">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1151">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1151">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1152">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1152">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-1153">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1153">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-1154">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1154">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-1155">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1155">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-1156">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1156">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-1157">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1157">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1158">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1158">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1159">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1159">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1160">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1160">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1161">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1161">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-1162">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1162">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-1163">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1163">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1164">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1164">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1165">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1165">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1166">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1166">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1167">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1167">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1168">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1168">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1169">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1169">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1170">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1170">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1171">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1172">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1173">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1174">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1174">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1175">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1176">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1176">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1177">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1177">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1178">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1178">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-1179">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1179">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1180">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1180">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1181">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1181">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-1182">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1182">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-1183">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1183">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1184">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1184">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-1185">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1185">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1186">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1186">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1187">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1187">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-1188">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1188">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-1189">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1189">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-1190">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1190">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a><span data-ttu-id="6e083-1191">DXGI_FORMAT_D32 \_ FLOAT \_ S8X24 \_ UINT<sup>FNS</sup> (20) </span><span class="sxs-lookup"><span data-stu-id="6e083-1191">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FNS</sup> (20)</span></span>
| <span data-ttu-id="6e083-1192">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1192">Target</span></span> | <span data-ttu-id="6e083-1193">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1193">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1194">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1194">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1195">64</span><span class="sxs-lookup"><span data-stu-id="6e083-1195">64</span></span> |
| <span data-ttu-id="6e083-1196">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1196">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-1197">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1197">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1198">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1198">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1199">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1199">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1200">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1200">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1201">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1201">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1202">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1202">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-1203">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1203">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-1204">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1204">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-1205">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1205">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-1206">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1206">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-1207">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1207">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1208">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1208">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1209">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1209">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1210">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1210">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1211">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1211">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-1212">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1212">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-1213">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1213">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1214">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1214">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1215">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1215">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1216">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1216">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1217">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1217">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1218">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1218">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1219">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1219">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1220">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1220">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1221">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1221">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1222">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1222">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1223">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1223">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1224">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1224">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1225">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1225">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1226">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1226">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1227">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1227">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1228">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1228">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-1229">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1229">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1230">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1230">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1231">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1231">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-1232">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1232">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-1233">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1233">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1234">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1234">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-1235">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1235">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1236">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1236">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1237">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1237">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-1238">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1238">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-1239">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1239">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-1240">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1240">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a><span data-ttu-id="6e083-1241">DXGI_FORMAT_R32 \_ FLOAT X8X24 無型別 \_ \_ <sup>FNS</sup> (21) </span><span class="sxs-lookup"><span data-stu-id="6e083-1241">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FNS</sup> (21)</span></span>
| <span data-ttu-id="6e083-1242">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1242">Target</span></span> | <span data-ttu-id="6e083-1243">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1243">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1244">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1244">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1245">64</span><span class="sxs-lookup"><span data-stu-id="6e083-1245">64</span></span> |
| <span data-ttu-id="6e083-1246">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1246">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-1247">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1247">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1248">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1248">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1249">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1249">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1250">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1250">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1251">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1251">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1252">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1252">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-1253">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1253">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-1254">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1254">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-1255">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1255">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-1256">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1256">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-1257">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1257">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1258">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1258">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1259">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1259">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1260">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1260">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1261">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1261">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-1262">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1262">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-1263">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1263">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1264">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1264">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1265">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1265">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1266">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1266">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1267">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1267">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1268">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1268">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1269">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1269">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1270">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1270">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1271">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1271">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1272">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1272">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1273">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1273">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1274">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1274">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1275">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1275">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1276">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1276">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1277">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1277">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1278">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1278">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-1279">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1279">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1280">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1280">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1281">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1281">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-1282">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1282">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-1283">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1283">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1284">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1284">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-1285">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1285">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1286">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1286">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1287">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1287">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-1288">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1288">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-1289">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1289">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-1290">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1290">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a><span data-ttu-id="6e083-1291">DXGI_FORMAT_X32 無別 \_ \_ G8X24 \_ UINT<sup>FNS</sup> (22) </span><span class="sxs-lookup"><span data-stu-id="6e083-1291">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FNS</sup> (22)</span></span>
| <span data-ttu-id="6e083-1292">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1292">Target</span></span> | <span data-ttu-id="6e083-1293">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1293">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1294">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1294">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1295">64</span><span class="sxs-lookup"><span data-stu-id="6e083-1295">64</span></span> |
| <span data-ttu-id="6e083-1296">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1296">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-1297">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1297">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1298">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1298">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1299">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1299">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1300">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1300">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1301">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1301">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1302">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1302">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-1303">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1303">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-1304">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1304">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-1305">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1305">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-1306">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1306">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-1307">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1307">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1308">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1308">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1309">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1309">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1310">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1310">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1311">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1311">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-1312">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1312">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-1313">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1313">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1314">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1314">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1315">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1315">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1316">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1316">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1317">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1317">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1318">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1318">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1319">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1319">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1320">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1320">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1321">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1321">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1322">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1322">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1323">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1323">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1324">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1324">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1325">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1325">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1326">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1326">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1327">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1327">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1328">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1328">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-1329">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1329">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1330">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1330">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1331">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1331">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-1332">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1332">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-1333">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1333">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1334">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1334">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-1335">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1335">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1336">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1336">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1337">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1337">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-1338">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1338">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-1339">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1339">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-1340">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1340">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="6e083-1341">DXGI_FORMAT_R10G10B10A2 無別 \_ <sup>電腦</sup> (23) </span><span class="sxs-lookup"><span data-stu-id="6e083-1341">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="6e083-1342">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1342">Target</span></span> | <span data-ttu-id="6e083-1343">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1343">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1344">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1344">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1345">32</span><span class="sxs-lookup"><span data-stu-id="6e083-1345">32</span></span> |
| <span data-ttu-id="6e083-1346">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1346">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-1347">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1347">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1348">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1348">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1349">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1349">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1350">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1350">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1351">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1351">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1352">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1352">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-1353">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1353">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-1354">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1354">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-1355">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1355">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-1356">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1356">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-1357">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1357">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1358">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1358">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1359">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1359">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1360">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1360">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1361">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1361">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-1362">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1362">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-1363">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1363">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1364">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1364">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1365">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1365">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1366">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1366">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1367">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1367">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1368">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1368">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1369">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1369">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1370">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1370">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1371">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1371">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1372">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1372">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1373">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1373">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1374">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1374">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1375">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1375">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1376">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1376">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1377">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1377">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1378">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1378">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-1379">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1379">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1380">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1380">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1381">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1381">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-1382">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1382">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-1383">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1383">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1384">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1384">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-1385">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1385">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1386">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1386">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1387">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1387">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-1388">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1388">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-1389">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1389">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-1390">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1390">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a><span data-ttu-id="6e083-1391">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FNS</sup> (24) </span><span class="sxs-lookup"><span data-stu-id="6e083-1391">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FNS</sup> (24)</span></span>
| <span data-ttu-id="6e083-1392">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1392">Target</span></span> | <span data-ttu-id="6e083-1393">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1393">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1394">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1394">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1395">32</span><span class="sxs-lookup"><span data-stu-id="6e083-1395">32</span></span> |
| <span data-ttu-id="6e083-1396">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1396">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-1397">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1397">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1398">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1398">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1399">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1399">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1400">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1400">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1401">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1401">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1402">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1402">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-1403">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1403">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-1404">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1404">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-1405">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1405">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-1406">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1406">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-1407">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1407">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1408">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1408">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1409">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1409">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1410">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1410">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1411">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1411">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-1412">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1412">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-1413">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1413">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1414">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1414">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1415">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1415">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1416">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1416">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1417">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1417">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1418">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1418">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1419">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1419">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1420">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1420">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1421">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1421">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1422">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1422">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1423">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1423">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1424">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1424">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1425">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1425">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1426">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1426">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1427">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1427">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1428">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1428">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-1429">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1429">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1430">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1430">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1431">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1431">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-1432">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1432">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-1433">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1433">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1434">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1434">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-1435">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1435">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1436">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1437">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-1438">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-1439">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1439">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1441">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a><span data-ttu-id="6e083-1442">DXGI_FORMAT_R10G10B10A2 \_ UINT<sup>FNS</sup> (25) </span><span class="sxs-lookup"><span data-stu-id="6e083-1442">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FNS</sup> (25)</span></span>
| <span data-ttu-id="6e083-1443">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1443">Target</span></span> | <span data-ttu-id="6e083-1444">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1444">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1445">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1446">32</span><span class="sxs-lookup"><span data-stu-id="6e083-1446">32</span></span> |
| <span data-ttu-id="6e083-1447">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1447">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-1448">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1448">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1449">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1449">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1450">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1450">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1451">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1451">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1452">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1452">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1453">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1453">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-1454">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1454">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-1455">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1455">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-1456">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1456">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-1457">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1457">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-1458">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1458">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1459">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1459">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1460">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1460">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1461">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1461">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1462">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1462">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-1463">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1463">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-1464">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1464">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1465">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1465">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1466">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1466">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1467">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1467">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1468">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1468">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1469">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1469">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1470">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1470">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1471">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1471">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1472">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1472">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1473">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1473">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1474">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1474">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1475">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1475">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1476">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1476">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1477">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1477">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1478">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1478">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1479">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1479">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-1480">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1480">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1481">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1481">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1482">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1482">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-1483">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1483">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-1484">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1484">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1485">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1485">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-1486">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1486">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1487">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1487">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1488">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1488">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-1489">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1489">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-1490">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1490">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-1491">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1491">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a><span data-ttu-id="6e083-1492">DXGI_FORMAT_R10G10B10 \_ XR \_ 偏差 \_ A2 \_ UNORM<sup>FNS</sup> (89) </span><span class="sxs-lookup"><span data-stu-id="6e083-1492">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FNS</sup> (89)</span></span>
| <span data-ttu-id="6e083-1493">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1493">Target</span></span> | <span data-ttu-id="6e083-1494">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1494">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1495">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1495">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1496">32</span><span class="sxs-lookup"><span data-stu-id="6e083-1496">32</span></span> |
| <span data-ttu-id="6e083-1497">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1497">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-1498">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1498">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1499">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1499">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1500">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1500">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1501">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1501">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1502">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1502">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1503">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1503">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-1504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1504">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-1505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1505">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-1506">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1506">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-1507">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1507">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-1508">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1509">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1510">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1510">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1511">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1512">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1512">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-1513">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1513">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-1514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1514">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1515">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1515">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1516">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1516">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1517">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1517">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1518">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1518">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1519">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1519">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1520">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1520">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1521">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1521">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1522">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1522">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1523">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1523">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1524">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1524">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1525">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1525">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1526">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1526">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1527">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1527">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1528">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1528">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1529">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1529">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-1530">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1530">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1531">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1531">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1532">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-1533">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-1534">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1534">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1535">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-1536">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1537">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1538">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-1539">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-1540">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1540">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-1541">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="6e083-1542">DXGI_FORMAT_R11G11B10 \_ FLOAT<sup>FNS</sup> (26) </span><span class="sxs-lookup"><span data-stu-id="6e083-1542">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="6e083-1543">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1543">Target</span></span> | <span data-ttu-id="6e083-1544">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1544">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1545">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1546">32</span><span class="sxs-lookup"><span data-stu-id="6e083-1546">32</span></span> |
| <span data-ttu-id="6e083-1547">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1547">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-1548">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1548">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1549">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1550">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1551">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1552">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1553">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-1554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1554">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-1555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1555">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-1556">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-1557">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-1558">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1559">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1560">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1560">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1561">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1562">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1562">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-1563">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-1564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1564">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1565">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1566">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1567">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1568">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1569">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1570">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1570">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1571">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1572">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1573">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1574">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1575">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1576">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1577">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1578">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1579">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-1580">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1581">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1582">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-1583">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-1584">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1584">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1585">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-1586">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1587">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1587">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1588">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1588">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-1589">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1589">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-1590">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1590">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-1591">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1591">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="6e083-1592">DXGI_FORMAT_R8G8B8A8 無別 \_ <sup>電腦</sup> (27) </span><span class="sxs-lookup"><span data-stu-id="6e083-1592">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="6e083-1593">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1593">Target</span></span> | <span data-ttu-id="6e083-1594">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1594">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1595">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1595">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1596">32</span><span class="sxs-lookup"><span data-stu-id="6e083-1596">32</span></span> |
| <span data-ttu-id="6e083-1597">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1597">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-1598">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1598">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1599">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1599">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1600">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1601">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1602">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1603">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-1604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1604">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-1605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1605">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-1606">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-1607">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-1608">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1609">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1610">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1610">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1611">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1612">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1612">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-1613">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-1614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1614">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1615">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1616">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1617">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1618">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1619">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1620">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1620">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1621">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1622">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1623">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1624">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1625">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1626">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1627">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1628">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1629">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1629">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-1630">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1630">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1631">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1631">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1632">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1632">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-1633">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1633">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-1634">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1634">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1635">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1635">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-1636">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1636">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1637">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1637">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1638">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1638">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-1639">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1639">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-1640">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1640">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-1641">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1641">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a><span data-ttu-id="6e083-1642">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FNS</sup> (28) </span><span class="sxs-lookup"><span data-stu-id="6e083-1642">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FNS</sup> (28)</span></span>
| <span data-ttu-id="6e083-1643">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1643">Target</span></span> | <span data-ttu-id="6e083-1644">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1644">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1645">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1645">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1646">32</span><span class="sxs-lookup"><span data-stu-id="6e083-1646">32</span></span> |
| <span data-ttu-id="6e083-1647">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1647">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1649">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1649">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1650">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1650">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1652">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1652">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1653">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1653">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1654">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1654">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1655">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1657">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1659">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1661">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1661">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1663">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1663">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1665">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1665">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1666">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1666">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1667">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1667">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1668">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1668">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1669">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1669">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1671">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1671">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1673">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1675">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1675">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1677">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1677">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1678">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1678">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1679">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1679">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1680">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1680">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1681">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1681">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1682">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1682">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1683">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1683">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1684">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1684">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1685">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1685">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1686">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1686">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1687">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1687">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1688">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1688">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1689">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1689">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1690">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1690">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1692">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1692">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-1694">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1694">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-1696">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1696">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-1698">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1698">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1700">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1700">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1701">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1701">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1703">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1703">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1704">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1704">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1705">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1705">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-1707">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1707">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1709">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1709">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1711">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1711">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a><span data-ttu-id="6e083-1712">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ SRGB<sup>FNS</sup> (29) </span><span class="sxs-lookup"><span data-stu-id="6e083-1712">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FNS</sup> (29)</span></span>
| <span data-ttu-id="6e083-1713">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1713">Target</span></span> | <span data-ttu-id="6e083-1714">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1714">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1715">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1715">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1716">32</span><span class="sxs-lookup"><span data-stu-id="6e083-1716">32</span></span> |
| <span data-ttu-id="6e083-1717">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1717">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1719">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1719">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1720">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1720">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1721">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1721">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1722">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1722">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1723">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1723">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1724">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1724">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1726">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1726">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1728">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1728">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1730">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1730">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1732">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1732">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1734">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1734">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1735">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1735">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1736">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1736">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1737">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1737">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1738">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1738">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1740">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1740">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1742">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1742">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1744">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1744">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1746">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1746">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1747">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1747">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1748">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1748">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1749">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1749">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1750">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1750">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1751">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1751">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1752">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1752">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1753">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1753">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1754">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1754">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1755">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1755">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1756">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1756">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1757">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1757">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1758">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1758">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1759">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1759">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1761">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1761">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-1763">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1763">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-1765">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1765">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-1767">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1767">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1769">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1769">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1770">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1770">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1772">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1772">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1773">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1773">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1774">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1774">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-1776">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1776">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1778">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1778">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1780">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1780">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a><span data-ttu-id="6e083-1781">DXGI_FORMAT_R8G8B8A8 \_ UINT<sup>FNS</sup> (30) </span><span class="sxs-lookup"><span data-stu-id="6e083-1781">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FNS</sup> (30)</span></span>
| <span data-ttu-id="6e083-1782">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1782">Target</span></span> | <span data-ttu-id="6e083-1783">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1783">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1784">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1784">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1785">32</span><span class="sxs-lookup"><span data-stu-id="6e083-1785">32</span></span> |
| <span data-ttu-id="6e083-1786">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1786">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1788">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1788">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1789">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1789">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1791">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1791">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1792">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1792">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1793">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1793">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1794">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1794">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-1795">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1795">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-1796">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1796">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-1797">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1797">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-1798">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1798">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-1799">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1799">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1800">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1800">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1801">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1801">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1802">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1802">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1803">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1803">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-1804">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1804">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-1805">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1805">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1806">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1806">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1807">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1807">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1808">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1808">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1809">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1809">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1810">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1810">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1811">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1811">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1812">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1812">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1813">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1813">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1814">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1814">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1815">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1815">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1816">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1816">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1817">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1817">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1818">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1818">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1819">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1819">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1820">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1820">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-1821">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1821">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1822">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1822">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1823">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1823">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-1824">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1824">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-1825">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1825">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1826">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1826">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-1827">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1827">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1828">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1828">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1829">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1829">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-1830">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1830">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-1831">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1831">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-1832">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1832">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a><span data-ttu-id="6e083-1833">DXGI_FORMAT_R8G8B8A8 \_ SNORM<sup>FNS</sup> (31) </span><span class="sxs-lookup"><span data-stu-id="6e083-1833">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FNS</sup> (31)</span></span>
| <span data-ttu-id="6e083-1834">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1834">Target</span></span> | <span data-ttu-id="6e083-1835">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1835">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1836">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1836">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1837">32</span><span class="sxs-lookup"><span data-stu-id="6e083-1837">32</span></span> |
| <span data-ttu-id="6e083-1838">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1838">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1840">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1840">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1841">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1841">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1842">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1842">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1843">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1843">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1844">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1844">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1845">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1845">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1847">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1847">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-1848">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1848">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1850">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1850">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1852">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1852">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1854">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1854">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1855">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1855">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1856">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1856">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1857">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1857">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1858">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1858">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1860">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1860">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-1861">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1861">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1862">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1862">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1863">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1863">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1864">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1864">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1865">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1865">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1866">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1866">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1867">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1867">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1868">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1868">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1869">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1869">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1870">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1870">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1871">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1871">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1872">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1872">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1873">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1873">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1874">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1874">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1875">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1875">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1876">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1876">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1878">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1878">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1879">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1879">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1880">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1880">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-1881">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1881">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-1882">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1882">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1883">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1883">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-1884">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1884">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1885">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1885">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1886">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1886">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-1887">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1887">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-1888">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1888">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-1889">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1889">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a><span data-ttu-id="6e083-1890">DXGI_FORMAT_R8G8B8A8 \_ 聖<sup>FNS</sup> (32) </span><span class="sxs-lookup"><span data-stu-id="6e083-1890">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FNS</sup> (32)</span></span>
| <span data-ttu-id="6e083-1891">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1891">Target</span></span> | <span data-ttu-id="6e083-1892">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1892">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1893">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1893">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1894">32</span><span class="sxs-lookup"><span data-stu-id="6e083-1894">32</span></span> |
| <span data-ttu-id="6e083-1895">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1895">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-1896">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1896">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1897">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1897">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1898">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1898">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1899">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1899">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1900">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1900">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1901">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1901">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-1902">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1902">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-1903">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1903">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-1904">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1904">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-1905">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1905">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-1906">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1906">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1907">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1907">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1908">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1908">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1909">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1909">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1910">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1910">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-1911">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1911">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-1912">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1912">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1913">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1913">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1914">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1914">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1915">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1915">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1916">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1916">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1917">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1917">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1918">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1918">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1919">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1919">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1920">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1920">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1921">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1921">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1922">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1922">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1923">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1923">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1924">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1924">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1925">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1925">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1926">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1926">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1927">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1927">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-1928">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1928">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1929">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1929">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1930">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1930">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-1931">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1931">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-1932">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1932">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1933">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1933">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-1934">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1934">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1935">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1935">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1936">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1936">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-1937">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1937">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-1938">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1938">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-1939">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1939">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="6e083-1940">DXGI_FORMAT_R16G16 無的 \_ <sup>電腦</sup> (33) </span><span class="sxs-lookup"><span data-stu-id="6e083-1940">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="6e083-1941">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1941">Target</span></span> | <span data-ttu-id="6e083-1942">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1942">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1943">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1943">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1944">32</span><span class="sxs-lookup"><span data-stu-id="6e083-1944">32</span></span> |
| <span data-ttu-id="6e083-1945">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1945">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-1946">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1946">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1947">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1947">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1948">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1948">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1949">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1949">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1950">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-1950">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-1951">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-1951">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-1952">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-1952">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-1953">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-1953">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-1954">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-1954">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-1955">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1955">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-1956">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1956">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-1957">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-1957">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-1958">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-1958">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-1959">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-1959">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-1960">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-1960">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-1961">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-1961">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-1962">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1962">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1963">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1963">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1964">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-1964">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-1965">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1965">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-1966">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1966">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1967">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-1967">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-1968">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-1968">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-1969">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-1969">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-1970">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1970">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-1971">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-1971">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-1972">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-1972">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-1973">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-1973">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-1974">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-1974">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-1975">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1975">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1976">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-1976">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-1977">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-1977">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-1978">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1978">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1979">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-1979">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-1980">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-1980">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-1981">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-1981">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-1982">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-1982">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-1983">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-1983">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-1984">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-1984">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-1985">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1985">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-1986">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-1986">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-1987">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-1987">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-1988">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1988">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-1989">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-1989">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a><span data-ttu-id="6e083-1990">DXGI_FORMAT_R16G16 \_ FLOAT<sup>FNS</sup> (34) </span><span class="sxs-lookup"><span data-stu-id="6e083-1990">DXGI_FORMAT_R16G16\_FLOAT<sup>FNS</sup> (34)</span></span>
| <span data-ttu-id="6e083-1991">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-1991">Target</span></span> | <span data-ttu-id="6e083-1992">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1992">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-1993">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-1993">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-1994">32</span><span class="sxs-lookup"><span data-stu-id="6e083-1994">32</span></span> |
| <span data-ttu-id="6e083-1995">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-1995">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-1997">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-1997">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-1998">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-1998">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2000">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2000">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2001">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2001">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2002">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2002">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2003">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2003">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2005">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2005">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2007">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2007">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2009">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2009">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2011">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2011">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-2012">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2012">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2013">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2013">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2014">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2014">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2015">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2015">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2016">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2016">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2018">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2018">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2020">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2020">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2022">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2022">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2023">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2023">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2024">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2024">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2025">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2025">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2026">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2026">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2027">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2027">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2028">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2028">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2029">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2029">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2030">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2030">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2031">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2031">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2032">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2032">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2033">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2033">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2034">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2034">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2035">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2035">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2036">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2036">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2038">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2038">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-2040">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2040">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-2042">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2042">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-2044">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2044">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2046">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2046">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2047">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2047">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2048">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2048">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2049">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2049">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2050">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2050">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2051">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2051">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2052">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2052">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-2053">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2053">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a><span data-ttu-id="6e083-2054">DXGI_FORMAT_R16G16 \_ UNORM<sup>FNS</sup> (35) </span><span class="sxs-lookup"><span data-stu-id="6e083-2054">DXGI_FORMAT_R16G16\_UNORM<sup>FNS</sup> (35)</span></span>
| <span data-ttu-id="6e083-2055">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2055">Target</span></span> | <span data-ttu-id="6e083-2056">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2056">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2057">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2057">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2058">32</span><span class="sxs-lookup"><span data-stu-id="6e083-2058">32</span></span> |
| <span data-ttu-id="6e083-2059">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2059">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2061">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2061">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2062">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2062">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2063">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2063">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2064">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2064">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2065">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2065">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2066">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2066">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2068">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2068">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2070">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2070">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2072">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2072">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2074">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2074">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2076">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2076">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2077">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2077">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2078">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2078">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2079">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2079">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2080">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2080">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2082">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2082">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2084">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2084">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2086">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2086">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2087">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2088">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2089">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2090">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2091">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2091">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2092">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2092">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2093">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2093">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2094">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2094">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2095">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2095">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2096">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2096">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2097">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2097">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2098">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2098">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2099">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2099">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2100">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2100">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2102">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2102">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-2104">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2104">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-2106">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2106">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-2108">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2108">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2110">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2110">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2111">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2111">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2112">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2112">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2113">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2113">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2114">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2114">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2115">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2115">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2116">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2116">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-2117">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2117">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a><span data-ttu-id="6e083-2118">DXGI_FORMAT_R16G16 \_ UINT<sup>FNS</sup> (36) </span><span class="sxs-lookup"><span data-stu-id="6e083-2118">DXGI_FORMAT_R16G16\_UINT<sup>FNS</sup> (36)</span></span>
| <span data-ttu-id="6e083-2119">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2119">Target</span></span> | <span data-ttu-id="6e083-2120">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2120">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2121">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2121">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2122">32</span><span class="sxs-lookup"><span data-stu-id="6e083-2122">32</span></span> |
| <span data-ttu-id="6e083-2123">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2123">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-2124">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2124">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2125">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2125">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2126">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2126">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2127">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2127">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2128">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2128">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2129">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2129">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-2130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2130">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-2131">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2131">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-2132">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2132">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-2133">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2133">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-2134">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2134">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2135">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2135">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2136">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2136">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2137">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2137">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2138">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2138">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-2139">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2139">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-2140">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2140">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2141">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2141">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2142">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2142">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2143">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2143">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2144">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2144">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2145">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2145">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2146">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2146">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2147">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2147">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2148">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2148">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2149">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2149">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2150">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2150">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2151">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2151">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2152">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2152">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2153">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2153">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2154">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2154">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2155">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2155">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-2156">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2156">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2157">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2157">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2158">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2158">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-2159">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2159">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-2160">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2160">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2161">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2161">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2162">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2162">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2163">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2163">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2164">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2164">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2165">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2165">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2166">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2166">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-2167">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2167">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a><span data-ttu-id="6e083-2168">DXGI_FORMAT_R16G16 \_ SNORM<sup>FNS</sup> (37) </span><span class="sxs-lookup"><span data-stu-id="6e083-2168">DXGI_FORMAT_R16G16\_SNORM<sup>FNS</sup> (37)</span></span>
| <span data-ttu-id="6e083-2169">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2169">Target</span></span> | <span data-ttu-id="6e083-2170">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2170">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2171">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2171">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2172">32</span><span class="sxs-lookup"><span data-stu-id="6e083-2172">32</span></span> |
| <span data-ttu-id="6e083-2173">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2173">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2175">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2175">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2176">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2176">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2178">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2178">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2179">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2179">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2180">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2180">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2181">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2181">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2183">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2185">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2185">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2187">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2187">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2189">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2189">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2191">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2191">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2192">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2192">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2193">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2193">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2194">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2194">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2195">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2195">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2197">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2197">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-2198">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2198">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2199">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2199">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2200">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2200">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2201">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2201">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2202">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2202">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2203">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2203">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2204">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2204">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2205">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2205">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2206">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2206">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2207">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2207">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2208">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2208">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2209">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2209">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2210">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2210">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2211">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2211">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2212">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2212">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2213">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2213">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2215">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2215">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2216">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2216">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2217">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2217">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-2218">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2218">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-2219">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2219">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2220">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2220">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2221">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2221">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2222">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2222">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2223">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2223">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2224">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2224">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2225">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2225">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-2226">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2226">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a><span data-ttu-id="6e083-2227">DXGI_FORMAT_R16G16 \_ 聖<sup>FNS</sup> (38) </span><span class="sxs-lookup"><span data-stu-id="6e083-2227">DXGI_FORMAT_R16G16\_SINT<sup>FNS</sup> (38)</span></span>
| <span data-ttu-id="6e083-2228">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2228">Target</span></span> | <span data-ttu-id="6e083-2229">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2229">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2230">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2230">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2231">32</span><span class="sxs-lookup"><span data-stu-id="6e083-2231">32</span></span> |
| <span data-ttu-id="6e083-2232">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2232">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2234">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2234">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2235">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2235">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2237">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2237">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2238">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2238">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2239">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2239">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2240">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2240">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-2241">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2241">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-2242">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2242">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-2243">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2243">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-2244">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2244">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-2245">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2245">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2246">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2246">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2247">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2247">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2248">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2248">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2249">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2249">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-2250">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2250">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-2251">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2251">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2252">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2252">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2253">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2253">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2254">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2254">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2255">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2255">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2256">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2256">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2257">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2257">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2258">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2258">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2259">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2259">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2260">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2260">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2261">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2261">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2262">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2262">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2263">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2263">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2264">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2264">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2265">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2265">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2266">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2266">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-2267">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2267">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2268">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2268">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2269">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2269">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-2270">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2270">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-2271">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2271">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2272">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2272">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2273">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2273">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2274">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2274">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2275">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2275">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2276">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2276">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2277">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2277">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-2278">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2278">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="6e083-2279">DXGI_FORMAT_R32 無的 \_ <sup>電腦</sup> (39) </span><span class="sxs-lookup"><span data-stu-id="6e083-2279">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="6e083-2280">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2280">Target</span></span> | <span data-ttu-id="6e083-2281">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2281">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2282">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2282">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2283">32</span><span class="sxs-lookup"><span data-stu-id="6e083-2283">32</span></span> |
| <span data-ttu-id="6e083-2284">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2284">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-2285">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2285">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2286">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2286">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2287">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2287">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2288">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2288">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2289">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2289">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2290">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2290">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-2291">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2291">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-2292">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2292">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-2293">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2293">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-2294">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2294">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-2295">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2295">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2296">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2296">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2297">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2297">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2298">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2298">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2299">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2299">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-2300">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2300">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-2301">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2301">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2302">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2302">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2303">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2303">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2304">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2304">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2305">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2305">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2306">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2306">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2307">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2307">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2308">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2308">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2309">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2309">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2310">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2310">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2311">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2311">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2312">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2312">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2313">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2313">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2314">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2314">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2315">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2315">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2316">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2316">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-2317">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2318">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2319">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-2320">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-2321">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2321">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2322">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2322">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2323">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2323">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2324">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2324">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2325">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2325">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2326">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2326">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2327">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2327">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-2328">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2328">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a><span data-ttu-id="6e083-2329">DXGI_FORMAT_D32 \_ FLOAT<sup>FNS</sup> (40) </span><span class="sxs-lookup"><span data-stu-id="6e083-2329">DXGI_FORMAT_D32\_FLOAT<sup>FNS</sup> (40)</span></span>
| <span data-ttu-id="6e083-2330">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2330">Target</span></span> | <span data-ttu-id="6e083-2331">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2331">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2332">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2332">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2333">32</span><span class="sxs-lookup"><span data-stu-id="6e083-2333">32</span></span> |
| <span data-ttu-id="6e083-2334">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2334">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-2335">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2335">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2336">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2336">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2337">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2337">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2338">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2338">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2339">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2339">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2340">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2340">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-2341">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2341">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-2342">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2342">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-2343">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2343">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-2344">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2344">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-2345">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2345">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2346">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2346">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2347">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2347">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2348">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2348">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2349">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2349">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-2350">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2350">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-2351">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2351">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2352">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2352">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2353">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2353">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2354">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2354">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2355">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2355">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2356">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2356">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2357">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2357">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2358">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2358">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2359">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2359">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2360">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2360">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2361">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2361">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2362">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2362">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2363">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2363">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2364">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2364">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2365">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2365">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2366">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2366">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-2367">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2367">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2368">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2368">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2369">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2369">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-2370">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2370">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-2371">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2371">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2372">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2373">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2373">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2374">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2375">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2376">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2377">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2377">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-2378">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a><span data-ttu-id="6e083-2379">DXGI_FORMAT_R32 \_ FLOAT<sup>FNS</sup> (41) </span><span class="sxs-lookup"><span data-stu-id="6e083-2379">DXGI_FORMAT_R32\_FLOAT<sup>FNS</sup> (41)</span></span>
| <span data-ttu-id="6e083-2380">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2380">Target</span></span> | <span data-ttu-id="6e083-2381">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2381">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2382">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2383">32</span><span class="sxs-lookup"><span data-stu-id="6e083-2383">32</span></span> |
| <span data-ttu-id="6e083-2384">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2384">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2386">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2386">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2387">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2387">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2389">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2390">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2391">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2392">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2394">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2394">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2396">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2396">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2398">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2398">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2400">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-2401">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2401">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2402">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2402">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2403">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2403">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2404">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2404">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2405">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2405">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2407">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2407">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2409">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2409">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2411">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2411">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2412">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2412">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2413">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2413">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2414">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2414">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2415">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2415">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2416">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2416">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2417">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2417">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2418">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2418">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2419">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2419">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2420">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2420">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2421">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2421">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2422">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2422">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2423">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2423">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2424">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2424">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2425">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2425">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2427">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2427">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-2429">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2429">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-2431">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2431">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-2433">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2433">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2435">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2435">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2436">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2436">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2437">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2437">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2438">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2438">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2439">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2439">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2440">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2440">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2441">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2441">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-2442">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2442">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a><span data-ttu-id="6e083-2443">DXGI_FORMAT_R32 \_ UINT<sup>FNS</sup> (42) </span><span class="sxs-lookup"><span data-stu-id="6e083-2443">DXGI_FORMAT_R32\_UINT<sup>FNS</sup> (42)</span></span>
| <span data-ttu-id="6e083-2444">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2444">Target</span></span> | <span data-ttu-id="6e083-2445">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2445">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2446">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2446">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2447">32</span><span class="sxs-lookup"><span data-stu-id="6e083-2447">32</span></span> |
| <span data-ttu-id="6e083-2448">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2448">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2450">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2450">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2451">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2451">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2452">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2452">Input Assembler Index Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2454">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2454">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2455">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2455">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2456">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2456">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-2457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2457">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-2458">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2458">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-2459">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2459">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-2460">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2460">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-2461">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2461">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2462">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2462">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2463">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2463">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2464">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2464">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2465">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2465">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-2466">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2466">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-2467">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2467">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2468">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2468">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2469">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2469">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2470">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2470">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2471">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2471">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2472">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2472">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2473">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2473">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2474">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2474">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2475">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2475">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2476">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2476">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2477">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2477">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2478">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2478">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2479">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2479">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2480">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2480">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2481">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2481">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2482">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2482">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-2483">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2483">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2484">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2484">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2485">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2485">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-2486">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2486">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-2487">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2487">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2488">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2488">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2489">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2489">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2490">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2490">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2491">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2491">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2492">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2492">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2493">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2493">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-2494">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2494">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a><span data-ttu-id="6e083-2495">DXGI_FORMAT_R32 \_ 聖<sup>FNS</sup> (43) </span><span class="sxs-lookup"><span data-stu-id="6e083-2495">DXGI_FORMAT_R32\_SINT<sup>FNS</sup> (43)</span></span>
| <span data-ttu-id="6e083-2496">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2496">Target</span></span> | <span data-ttu-id="6e083-2497">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2497">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2498">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2498">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2499">32</span><span class="sxs-lookup"><span data-stu-id="6e083-2499">32</span></span> |
| <span data-ttu-id="6e083-2500">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2500">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-2501">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2501">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2502">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2502">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2503">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2503">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2504">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2504">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2505">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2505">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2506">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2506">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-2507">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2507">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-2508">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2508">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-2509">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2509">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-2510">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2510">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-2511">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2511">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2512">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2512">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2513">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2513">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2514">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2514">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2515">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2515">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-2516">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2516">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-2517">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2517">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2518">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2518">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2519">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2519">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2520">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2520">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2521">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2521">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2522">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2522">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2523">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2523">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2524">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2524">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2525">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2525">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2526">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2526">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2527">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2527">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2528">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2528">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2529">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2529">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2530">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2530">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2531">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2531">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2532">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2532">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-2533">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2533">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2534">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2534">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2535">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2535">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-2536">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2536">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-2537">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2537">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2538">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2538">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2539">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2539">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2540">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2540">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2541">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2541">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2542">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2542">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2543">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2543">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-2544">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2544">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="6e083-2545">DXGI_FORMAT_R24G8 無的 \_ <sup>電腦</sup> (44) </span><span class="sxs-lookup"><span data-stu-id="6e083-2545">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="6e083-2546">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2546">Target</span></span> | <span data-ttu-id="6e083-2547">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2547">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2548">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2548">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2549">32</span><span class="sxs-lookup"><span data-stu-id="6e083-2549">32</span></span> |
| <span data-ttu-id="6e083-2550">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2550">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-2551">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2551">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2552">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2552">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2553">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2553">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2554">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2554">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2555">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2555">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2556">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2556">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-2557">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2557">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-2558">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2558">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-2559">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2559">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-2560">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2560">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-2561">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2561">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2562">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2562">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2563">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2563">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2564">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2564">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2565">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2565">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-2566">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2566">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-2567">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2567">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2568">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2568">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2569">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2569">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2570">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2570">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2571">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2571">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2572">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2572">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2573">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2573">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2574">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2574">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2575">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2575">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2576">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2576">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2577">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2577">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2578">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2578">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2579">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2579">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2580">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2580">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2581">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2581">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2582">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2582">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-2583">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2583">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2584">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2584">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2585">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2585">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-2586">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2586">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-2587">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2587">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2588">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2588">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2589">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2589">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2590">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2590">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2591">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2591">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2592">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2592">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2593">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2593">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-2594">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a><span data-ttu-id="6e083-2595">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FNS</sup> (45) </span><span class="sxs-lookup"><span data-stu-id="6e083-2595">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FNS</sup> (45)</span></span>
| <span data-ttu-id="6e083-2596">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2596">Target</span></span> | <span data-ttu-id="6e083-2597">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2597">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2598">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2599">32</span><span class="sxs-lookup"><span data-stu-id="6e083-2599">32</span></span> |
| <span data-ttu-id="6e083-2600">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2600">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2602">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2602">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2603">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2603">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2604">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2604">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2605">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2605">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2606">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2606">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2607">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2607">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2609">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2609">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-2610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2610">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-2611">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2611">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-2612">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2612">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-2613">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2614">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2615">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2615">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2616">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2617">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2617">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-2618">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2618">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-2619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2619">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2620">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2620">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2621">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2621">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2622">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2622">Depth/Stencil Target</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2624">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2624">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2625">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2625">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2626">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2626">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2627">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2627">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2628">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2628">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2629">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2629">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2630">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2630">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2631">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2631">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2632">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2632">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2633">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2633">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2634">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2634">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2635">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2635">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-2636">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2636">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-2638">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2638">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-2640">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2640">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-2642">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2642">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-2643">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2643">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2644">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2644">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2645">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2645">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2646">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2646">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2647">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2647">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2648">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2648">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2649">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2649">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-2650">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2650">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a><span data-ttu-id="6e083-2651">DXGI_FORMAT_R24 \_ UNORM \_ X8 無別 \_ <sup>FNS</sup> (46) </span><span class="sxs-lookup"><span data-stu-id="6e083-2651">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FNS</sup> (46)</span></span>
| <span data-ttu-id="6e083-2652">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2652">Target</span></span> | <span data-ttu-id="6e083-2653">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2653">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2654">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2654">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2655">32</span><span class="sxs-lookup"><span data-stu-id="6e083-2655">32</span></span> |
| <span data-ttu-id="6e083-2656">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2656">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-2657">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2657">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2658">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2658">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2659">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2659">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2660">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2660">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2661">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2661">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2662">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2662">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-2663">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2663">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-2664">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2664">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-2665">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2665">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-2666">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2666">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-2667">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2667">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2668">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2668">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2669">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2669">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2670">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2670">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2671">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2671">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-2672">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2672">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-2673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2673">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2674">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2674">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2675">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2675">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2676">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2676">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2677">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2677">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2678">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2678">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2679">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2679">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2680">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2680">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2681">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2681">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2682">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2682">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2683">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2683">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2684">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2684">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2685">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2685">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2686">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2686">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2687">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2687">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2688">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2688">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-2689">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2689">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2690">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2690">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2691">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2691">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-2692">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2692">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-2693">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2693">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2694">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2694">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2695">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2695">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2696">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2696">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2697">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2697">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2698">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2698">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2699">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2699">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-2700">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2700">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a><span data-ttu-id="6e083-2701">DXGI_FORMAT_X24 無別 \_ \_ G8 \_ UINT<sup>FNS</sup> (47) </span><span class="sxs-lookup"><span data-stu-id="6e083-2701">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FNS</sup> (47)</span></span>
| <span data-ttu-id="6e083-2702">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2702">Target</span></span> | <span data-ttu-id="6e083-2703">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2703">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2704">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2704">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2705">32</span><span class="sxs-lookup"><span data-stu-id="6e083-2705">32</span></span> |
| <span data-ttu-id="6e083-2706">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2706">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-2707">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2707">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2708">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2708">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2709">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2709">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2710">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2710">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2711">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2711">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2712">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2712">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-2713">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2713">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-2714">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2714">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-2715">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2715">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-2716">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2716">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-2717">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2717">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2718">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2718">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2719">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2719">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2720">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2720">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2721">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2721">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-2722">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2722">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-2723">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2723">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2724">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2724">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2725">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2725">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2726">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2726">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2727">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2727">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2728">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2728">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2729">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2729">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2730">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2730">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2731">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2731">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2732">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2732">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2733">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2733">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2734">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2734">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2735">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2735">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2736">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2736">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2737">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2737">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2738">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2738">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-2739">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2739">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2740">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2740">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2741">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2741">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-2742">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-2743">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2743">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2744">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2744">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2745">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2745">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2746">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2746">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2747">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2747">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2748">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2748">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2749">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2749">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-2750">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2750">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="6e083-2751">DXGI_FORMAT_R8G8 無的 \_ <sup>電腦</sup> (48) </span><span class="sxs-lookup"><span data-stu-id="6e083-2751">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="6e083-2752">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2752">Target</span></span> | <span data-ttu-id="6e083-2753">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2753">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2754">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2754">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2755">16</span><span class="sxs-lookup"><span data-stu-id="6e083-2755">16</span></span> |
| <span data-ttu-id="6e083-2756">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2756">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-2757">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2757">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2758">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2758">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2759">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2760">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2761">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2762">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2762">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-2763">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2763">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-2764">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2764">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-2765">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2765">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-2766">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2766">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-2767">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2767">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2768">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2768">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2769">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2769">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2770">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2770">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2771">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2771">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-2772">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2772">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-2773">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2773">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2774">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2774">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2775">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2775">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2776">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2776">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2777">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2777">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2778">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2778">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2779">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2779">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2780">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2780">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2781">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2781">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2782">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2782">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2783">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2783">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2784">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2784">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2785">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2785">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2786">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2786">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2787">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2787">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2788">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2788">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-2789">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2789">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2790">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2790">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2791">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2791">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-2792">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2792">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-2793">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2793">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2794">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2794">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2795">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2795">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2796">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2796">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2797">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2797">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2798">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2798">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2799">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2799">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-2800">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2800">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a><span data-ttu-id="6e083-2801">DXGI_FORMAT_R8G8 \_ UNORM<sup>FNS</sup> (49) </span><span class="sxs-lookup"><span data-stu-id="6e083-2801">DXGI_FORMAT_R8G8\_UNORM<sup>FNS</sup> (49)</span></span>
| <span data-ttu-id="6e083-2802">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2802">Target</span></span> | <span data-ttu-id="6e083-2803">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2803">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2804">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2804">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2805">16</span><span class="sxs-lookup"><span data-stu-id="6e083-2805">16</span></span> |
| <span data-ttu-id="6e083-2806">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2806">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2808">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2808">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2809">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2809">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2810">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2810">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2811">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2811">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2812">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2812">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2813">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2813">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2815">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2815">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-2816">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2816">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-2817">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2817">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2819">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2819">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2821">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2821">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2822">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2822">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2823">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2823">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2824">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2824">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2825">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2825">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-2826">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2826">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-2827">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2827">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2829">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2829">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2831">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2831">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2832">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2832">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2833">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2833">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2834">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2834">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2835">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2835">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2836">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2836">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2837">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2837">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2838">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2838">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2839">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2839">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2840">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2840">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2841">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2841">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2842">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2842">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2843">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2843">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2844">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2844">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2846">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2846">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2847">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2847">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2848">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2848">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-2849">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2849">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-2850">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2850">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2851">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2851">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2852">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2852">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2853">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2853">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2854">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2854">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2855">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2855">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2856">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2856">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2858">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2858">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a><span data-ttu-id="6e083-2859">DXGI_FORMAT_R8G8 \_ UINT<sup>FNS</sup> (50) </span><span class="sxs-lookup"><span data-stu-id="6e083-2859">DXGI_FORMAT_R8G8\_UINT<sup>FNS</sup> (50)</span></span>
| <span data-ttu-id="6e083-2860">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2860">Target</span></span> | <span data-ttu-id="6e083-2861">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2861">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2862">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2862">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2863">16</span><span class="sxs-lookup"><span data-stu-id="6e083-2863">16</span></span> |
| <span data-ttu-id="6e083-2864">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2864">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-2865">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2865">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2866">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2866">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2867">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2867">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2868">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2868">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2869">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2869">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2870">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2870">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-2871">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2871">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-2872">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2872">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-2873">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2873">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-2874">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2874">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-2875">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2875">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2876">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2876">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2877">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2877">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2878">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2878">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2879">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2879">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-2880">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2880">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-2881">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2881">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2882">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2883">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2884">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2885">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2886">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2887">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2887">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2888">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2888">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2889">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2889">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2890">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2890">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2891">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2891">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2892">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2892">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2893">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2893">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2894">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2894">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2895">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2895">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2896">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2896">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-2897">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2897">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2898">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2898">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2899">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2899">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-2900">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2900">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-2901">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2901">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2902">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2902">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2903">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2903">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2904">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2905">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2906">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2907">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2907">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-2908">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2908">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a><span data-ttu-id="6e083-2909">DXGI_FORMAT_R8G8 \_ SNORM<sup>FNS</sup> (51) </span><span class="sxs-lookup"><span data-stu-id="6e083-2909">DXGI_FORMAT_R8G8\_SNORM<sup>FNS</sup> (51)</span></span>
| <span data-ttu-id="6e083-2910">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2910">Target</span></span> | <span data-ttu-id="6e083-2911">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2911">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2912">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2912">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2913">16</span><span class="sxs-lookup"><span data-stu-id="6e083-2913">16</span></span> |
| <span data-ttu-id="6e083-2914">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2914">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2916">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2916">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2917">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2917">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2918">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2918">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2919">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2919">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2920">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2920">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2921">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2921">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2923">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2923">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-2924">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2924">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-2925">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2925">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2927">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2927">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2929">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2929">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2930">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2930">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2931">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2931">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2932">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2932">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2933">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2933">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2935">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2935">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-2936">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2936">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2937">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2937">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2938">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2938">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2939">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2939">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2940">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2940">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2941">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2941">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2942">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2942">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2943">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2943">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2944">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2944">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2945">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2945">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2946">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2946">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2947">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2947">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2948">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2948">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-2949">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2949">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2950">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-2950">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-2951">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-2951">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-2953">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2953">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2954">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2954">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2955">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-2955">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-2956">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-2956">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-2957">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2957">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-2958">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-2958">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-2959">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-2959">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-2960">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2960">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-2961">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-2961">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-2962">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-2962">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-2963">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2963">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-2964">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-2964">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a><span data-ttu-id="6e083-2965">DXGI_FORMAT_R8G8 \_ 聖<sup>FNS</sup> (52) </span><span class="sxs-lookup"><span data-stu-id="6e083-2965">DXGI_FORMAT_R8G8\_SINT<sup>FNS</sup> (52)</span></span>
| <span data-ttu-id="6e083-2966">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2966">Target</span></span> | <span data-ttu-id="6e083-2967">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2967">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-2968">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-2968">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-2969">16</span><span class="sxs-lookup"><span data-stu-id="6e083-2969">16</span></span> |
| <span data-ttu-id="6e083-2970">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-2970">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-2971">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-2971">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2972">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2972">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2973">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2973">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2974">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-2974">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-2975">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-2975">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-2976">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-2976">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-2977">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-2977">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-2978">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-2978">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-2979">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-2979">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-2980">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2980">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-2981">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2981">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-2982">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-2982">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-2983">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-2983">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-2984">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-2984">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-2985">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-2985">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-2986">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-2986">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-2987">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2987">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2988">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-2988">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-2989">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-2989">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-2990">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-2990">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-2991">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2991">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2992">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-2992">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-2993">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-2993">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-2994">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-2994">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-2995">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-2995">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-2996">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-2996">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-2997">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-2997">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-2998">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-2998">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-2999">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-2999">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3000">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3000">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3001">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3001">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3002">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3002">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-3003">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3003">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3004">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3004">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3005">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3005">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3006">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3006">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3007">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3007">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3008">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3008">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3009">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3009">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3010">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3010">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3011">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3011">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3012">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3012">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3013">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3013">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-3014">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3014">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="6e083-3015">DXGI_FORMAT_R16 無的 \_ <sup>電腦</sup> (53) </span><span class="sxs-lookup"><span data-stu-id="6e083-3015">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="6e083-3016">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3016">Target</span></span> | <span data-ttu-id="6e083-3017">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3017">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3018">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3018">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3019">16</span><span class="sxs-lookup"><span data-stu-id="6e083-3019">16</span></span> |
| <span data-ttu-id="6e083-3020">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3020">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-3021">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3021">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3022">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3022">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3023">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3023">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3024">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3024">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3025">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3025">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3026">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3026">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-3027">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3027">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-3028">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3028">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-3029">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3029">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-3030">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3030">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-3031">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3032">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3033">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3033">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3034">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3035">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3035">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-3036">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3036">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3037">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3037">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3038">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3038">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3039">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3039">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3040">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3040">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3041">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3041">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3042">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3042">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3043">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3043">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3044">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3044">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3045">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3045">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3046">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3046">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3047">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3047">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3048">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3048">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3049">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3049">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3050">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3050">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3051">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3051">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3052">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3052">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-3053">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3053">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3054">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3054">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3055">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3055">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3056">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3056">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3057">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3057">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3058">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3058">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3059">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3059">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3060">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3060">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3061">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3061">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3062">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3062">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3063">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3063">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-3064">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3064">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a><span data-ttu-id="6e083-3065">DXGI_FORMAT_R16 \_ FLOAT<sup>FNS</sup> (54) </span><span class="sxs-lookup"><span data-stu-id="6e083-3065">DXGI_FORMAT_R16\_FLOAT<sup>FNS</sup> (54)</span></span>
| <span data-ttu-id="6e083-3066">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3066">Target</span></span> | <span data-ttu-id="6e083-3067">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3067">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3068">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3068">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3069">16</span><span class="sxs-lookup"><span data-stu-id="6e083-3069">16</span></span> |
| <span data-ttu-id="6e083-3070">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3070">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-3071">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3071">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3072">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3072">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3073">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3073">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3074">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3074">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3075">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3075">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3076">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3076">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-3077">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3077">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-3078">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3078">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-3079">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3079">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-3080">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3080">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-3081">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3081">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3082">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3082">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3083">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3083">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3084">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3084">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3085">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3085">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-3086">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3086">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3087">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3087">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3088">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3088">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3089">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3089">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3090">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3090">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3091">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3091">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3092">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3092">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3093">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3093">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3094">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3094">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3095">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3095">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3096">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3096">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3097">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3097">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3098">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3098">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3099">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3099">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3100">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3100">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3101">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3101">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3102">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3102">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-3103">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3103">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3104">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3104">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3105">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3105">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3106">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3106">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3107">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3107">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3108">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3108">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3109">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3109">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3110">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3111">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3112">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3113">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3113">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-3114">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3114">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a><span data-ttu-id="6e083-3115">DXGI_FORMAT_D16 \_ UNORM<sup>FNS</sup> (55) </span><span class="sxs-lookup"><span data-stu-id="6e083-3115">DXGI_FORMAT_D16\_UNORM<sup>FNS</sup> (55)</span></span>
| <span data-ttu-id="6e083-3116">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3116">Target</span></span> | <span data-ttu-id="6e083-3117">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3117">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3118">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3118">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3119">16</span><span class="sxs-lookup"><span data-stu-id="6e083-3119">16</span></span> |
| <span data-ttu-id="6e083-3120">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3120">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3122">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3122">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3123">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3123">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3124">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3124">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3125">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3125">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3126">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3127">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3127">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3129">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3129">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-3130">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3130">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-3131">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3131">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-3132">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3132">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-3133">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3133">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3134">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3134">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3135">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3135">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3136">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3136">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3137">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3137">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-3138">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3138">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3139">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3139">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3140">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3140">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3141">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3141">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3142">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3142">Depth/Stencil Target</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3144">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3144">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3145">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3145">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3146">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3146">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3147">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3147">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3148">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3148">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3149">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3149">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3150">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3150">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3151">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3151">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3152">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3152">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3153">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3153">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3154">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3154">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3155">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3155">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-3156">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3156">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-3158">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3158">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-3160">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3160">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-3162">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3163">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3163">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3164">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3165">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3166">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3167">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3168">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3169">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3169">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-3170">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a><span data-ttu-id="6e083-3171">DXGI_FORMAT_R16 \_ UNORM<sup>FNS</sup> (56) </span><span class="sxs-lookup"><span data-stu-id="6e083-3171">DXGI_FORMAT_R16\_UNORM<sup>FNS</sup> (56)</span></span>
| <span data-ttu-id="6e083-3172">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3172">Target</span></span> | <span data-ttu-id="6e083-3173">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3173">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3174">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3175">16</span><span class="sxs-lookup"><span data-stu-id="6e083-3175">16</span></span> |
| <span data-ttu-id="6e083-3176">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3176">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3178">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3178">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3179">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3179">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3180">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3180">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3181">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3181">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3182">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3182">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3183">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3183">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3185">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3185">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3187">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3187">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3189">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3189">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3191">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3191">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3193">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3193">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3194">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3194">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3195">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3195">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3196">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3196">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3197">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3197">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3199">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3199">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3200">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3200">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3201">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3201">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3202">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3202">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3203">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3203">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3204">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3204">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3205">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3205">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3206">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3206">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3207">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3207">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3208">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3208">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3209">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3209">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3210">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3210">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3211">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3211">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3212">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3212">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3213">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3213">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3214">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3214">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3215">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3215">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3217">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3217">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3218">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3218">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3219">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3219">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3220">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3220">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3221">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3221">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3222">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3222">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3223">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3223">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3224">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3224">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3225">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3225">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3226">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3226">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3227">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3227">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-3228">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3228">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a><span data-ttu-id="6e083-3229">DXGI_FORMAT_R16 \_ UINT<sup>FNS</sup> (57) </span><span class="sxs-lookup"><span data-stu-id="6e083-3229">DXGI_FORMAT_R16\_UINT<sup>FNS</sup> (57)</span></span>
| <span data-ttu-id="6e083-3230">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3230">Target</span></span> | <span data-ttu-id="6e083-3231">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3231">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3232">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3232">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3233">16</span><span class="sxs-lookup"><span data-stu-id="6e083-3233">16</span></span> |
| <span data-ttu-id="6e083-3234">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3234">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3236">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3236">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3237">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3237">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3238">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3238">Input Assembler Index Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3240">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3240">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3241">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3241">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3242">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3242">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-3243">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3243">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-3244">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3244">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-3245">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3245">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-3246">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3246">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-3247">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3247">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3248">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3248">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3249">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3249">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3250">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3250">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3251">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3251">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-3252">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3252">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3253">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3253">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3254">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3254">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3255">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3255">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3256">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3256">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3257">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3257">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3258">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3258">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3259">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3259">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3260">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3260">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3261">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3261">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3262">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3262">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3263">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3263">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3264">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3264">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3265">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3265">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3266">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3266">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3267">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3267">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3268">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3268">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-3269">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3269">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3270">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3270">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3271">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3271">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3272">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3272">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3273">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3273">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3274">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3274">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3275">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3275">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3276">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3276">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3277">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3277">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3278">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3278">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3279">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3279">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-3280">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3280">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a><span data-ttu-id="6e083-3281">DXGI_FORMAT_R16 \_ SNORM<sup>FNS</sup> (58) </span><span class="sxs-lookup"><span data-stu-id="6e083-3281">DXGI_FORMAT_R16\_SNORM<sup>FNS</sup> (58)</span></span>
| <span data-ttu-id="6e083-3282">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3282">Target</span></span> | <span data-ttu-id="6e083-3283">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3283">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3284">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3284">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3285">16</span><span class="sxs-lookup"><span data-stu-id="6e083-3285">16</span></span> |
| <span data-ttu-id="6e083-3286">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3286">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-3287">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3287">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3288">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3288">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3289">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3289">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3290">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3290">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3291">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3291">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3292">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3292">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-3293">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3293">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-3294">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3294">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-3295">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3295">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-3296">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3296">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-3297">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3297">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3298">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3298">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3299">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3299">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3300">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3300">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3301">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3301">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-3302">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3302">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3303">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3303">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3304">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3304">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3305">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3305">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3306">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3306">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3307">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3307">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3308">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3308">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3309">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3309">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3310">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3310">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3311">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3311">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3312">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3312">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3313">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3313">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3314">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3314">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3315">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3315">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3316">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3316">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3317">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3317">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3318">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3318">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-3319">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3319">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3320">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3320">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3321">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3321">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3322">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3322">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3323">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3323">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3324">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3324">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3325">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3325">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3326">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3326">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3327">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3327">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3328">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3328">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3329">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3329">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-3330">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3330">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a><span data-ttu-id="6e083-3331">DXGI_FORMAT_R16 \_ 聖<sup>FNS</sup> (59) </span><span class="sxs-lookup"><span data-stu-id="6e083-3331">DXGI_FORMAT_R16\_SINT<sup>FNS</sup> (59)</span></span>
| <span data-ttu-id="6e083-3332">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3332">Target</span></span> | <span data-ttu-id="6e083-3333">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3333">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3334">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3334">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3335">16</span><span class="sxs-lookup"><span data-stu-id="6e083-3335">16</span></span> |
| <span data-ttu-id="6e083-3336">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3336">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-3337">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3337">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3338">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3338">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3339">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3339">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3340">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3340">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3341">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3341">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3342">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3342">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-3343">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3343">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-3344">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3344">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-3345">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3345">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-3346">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3346">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-3347">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3347">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3348">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3348">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3349">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3349">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3350">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3350">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3351">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3351">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-3352">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3352">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3353">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3353">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3354">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3354">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3355">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3355">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3356">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3356">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3357">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3357">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3358">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3358">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3359">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3359">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3360">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3360">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3361">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3361">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3362">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3362">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3363">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3363">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3364">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3364">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3365">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3365">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3366">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3366">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3367">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3367">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3368">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3368">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-3369">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3369">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3370">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3370">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3371">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3371">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3372">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3372">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3373">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3373">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3374">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3374">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3375">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3375">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3376">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3376">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3377">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3377">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3378">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3378">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3379">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3379">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-3380">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3380">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="6e083-3381">DXGI_FORMAT_R8 無的 \_ <sup>電腦</sup> (60) </span><span class="sxs-lookup"><span data-stu-id="6e083-3381">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="6e083-3382">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3382">Target</span></span> | <span data-ttu-id="6e083-3383">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3383">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3384">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3384">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3385">8</span><span class="sxs-lookup"><span data-stu-id="6e083-3385">8</span></span> |
| <span data-ttu-id="6e083-3386">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3386">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-3387">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3387">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3388">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3388">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3389">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3390">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3391">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3392">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-3393">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3393">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-3394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3394">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-3395">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3395">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-3396">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3396">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-3397">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3397">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3398">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3398">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3399">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3399">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3400">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3400">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3401">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3401">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-3402">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3402">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3403">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3403">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3404">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3404">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3405">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3405">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3406">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3406">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3407">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3407">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3408">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3408">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3409">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3409">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3410">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3410">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3411">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3411">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3412">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3412">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3413">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3413">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3414">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3414">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3415">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3415">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3416">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3416">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3417">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3417">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3418">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3418">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-3419">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3419">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3420">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3420">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3421">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3421">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3422">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3422">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3423">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3423">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3424">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3424">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3425">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3425">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3426">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3426">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3427">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3427">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3428">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3428">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3429">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3429">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-3430">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3430">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a><span data-ttu-id="6e083-3431">DXGI_FORMAT_R8 \_ UNORM<sup>FNS</sup> (61) </span><span class="sxs-lookup"><span data-stu-id="6e083-3431">DXGI_FORMAT_R8\_UNORM<sup>FNS</sup> (61)</span></span>
| <span data-ttu-id="6e083-3432">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3432">Target</span></span> | <span data-ttu-id="6e083-3433">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3433">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3434">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3434">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3435">8</span><span class="sxs-lookup"><span data-stu-id="6e083-3435">8</span></span> |
| <span data-ttu-id="6e083-3436">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3436">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3438">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3438">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3439">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3439">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3440">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3440">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3441">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3441">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3442">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3442">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3443">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3443">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3445">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3445">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3447">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3447">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3449">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3449">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3451">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3451">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3453">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3454">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3455">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3455">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3456">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3457">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3457">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3459">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3459">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3460">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3460">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3462">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3462">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3464">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3465">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3466">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3467">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3468">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3468">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3469">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3470">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3471">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3472">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3473">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3473">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3474">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3475">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3476">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3477">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3477">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3479">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3479">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3480">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3480">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3481">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3481">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3482">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3482">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3483">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3483">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3484">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3484">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3485">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3485">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3486">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3486">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3487">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3487">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3488">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3488">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3489">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3489">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3491">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3491">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a><span data-ttu-id="6e083-3492">DXGI_FORMAT_R8 \_ UINT<sup>FNS</sup> (62) </span><span class="sxs-lookup"><span data-stu-id="6e083-3492">DXGI_FORMAT_R8\_UINT<sup>FNS</sup> (62)</span></span>
| <span data-ttu-id="6e083-3493">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3493">Target</span></span> | <span data-ttu-id="6e083-3494">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3494">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3495">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3495">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3496">8</span><span class="sxs-lookup"><span data-stu-id="6e083-3496">8</span></span> |
| <span data-ttu-id="6e083-3497">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3497">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-3498">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3498">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3499">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3499">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3500">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3500">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3501">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3501">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3502">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3502">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3503">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3503">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-3504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3504">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-3505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3505">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-3506">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3506">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-3507">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3507">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-3508">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3509">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3510">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3510">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3511">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3512">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3512">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-3513">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3513">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3514">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3515">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3515">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3516">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3516">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3517">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3517">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3518">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3518">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3519">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3519">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3520">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3520">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3521">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3521">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3522">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3522">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3523">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3523">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3524">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3524">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3525">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3525">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3526">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3526">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3527">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3527">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3528">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3528">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3529">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3529">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-3530">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3530">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3531">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3531">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3532">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3533">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3534">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3534">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3535">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3536">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3537">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3538">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3539">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3540">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3540">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-3541">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a><span data-ttu-id="6e083-3542">DXGI_FORMAT_R8 \_ SNORM<sup>FNS</sup> (63) </span><span class="sxs-lookup"><span data-stu-id="6e083-3542">DXGI_FORMAT_R8\_SNORM<sup>FNS</sup> (63)</span></span>
| <span data-ttu-id="6e083-3543">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3543">Target</span></span> | <span data-ttu-id="6e083-3544">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3544">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3545">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3546">8</span><span class="sxs-lookup"><span data-stu-id="6e083-3546">8</span></span> |
| <span data-ttu-id="6e083-3547">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3547">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-3548">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3548">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3549">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3550">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3551">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3552">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3553">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-3554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3554">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-3555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3555">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-3556">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-3557">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-3558">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3559">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3560">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3560">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3561">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3562">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3562">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-3563">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3564">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3565">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3566">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3567">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3568">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3569">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3570">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3570">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3571">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3572">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3573">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3574">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3575">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3576">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3577">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3578">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3579">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-3580">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3581">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3582">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3583">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3584">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3584">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3585">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3586">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3587">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3587">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3588">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3588">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3589">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3589">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3590">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3590">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-3591">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3591">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a><span data-ttu-id="6e083-3592">DXGI_FORMAT_R8 \_ 聖<sup>FNS</sup> (64) </span><span class="sxs-lookup"><span data-stu-id="6e083-3592">DXGI_FORMAT_R8\_SINT<sup>FNS</sup> (64)</span></span>
| <span data-ttu-id="6e083-3593">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3593">Target</span></span> | <span data-ttu-id="6e083-3594">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3594">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3595">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3595">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3596">8</span><span class="sxs-lookup"><span data-stu-id="6e083-3596">8</span></span> |
| <span data-ttu-id="6e083-3597">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3597">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-3598">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3598">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3599">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3599">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3600">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3601">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3602">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3603">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-3604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3604">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-3605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3605">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-3606">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-3607">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-3608">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3609">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3610">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3610">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3611">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3612">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3612">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-3613">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3614">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3615">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3616">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3617">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3618">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3619">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3620">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3620">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3621">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3622">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3623">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3624">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3625">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3626">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3627">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3628">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3629">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3629">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-3630">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3630">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3631">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3631">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3632">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3632">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3633">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3633">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3634">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3634">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3635">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3635">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3636">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3636">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3637">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3637">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3638">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3638">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3639">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3639">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3640">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3640">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-3641">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3641">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="6e083-3642">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65) </span><span class="sxs-lookup"><span data-stu-id="6e083-3642">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="6e083-3643">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3643">Target</span></span> | <span data-ttu-id="6e083-3644">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3644">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3645">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3645">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3646">8</span><span class="sxs-lookup"><span data-stu-id="6e083-3646">8</span></span> |
| <span data-ttu-id="6e083-3647">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3647">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3649">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3649">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3650">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3650">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3651">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3651">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3652">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3652">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3653">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3654">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3654">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3656">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3656">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3658">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3658">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3660">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3660">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3662">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3662">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3664">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3665">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3666">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3666">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3667">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3668">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3668">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-3669">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3669">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3670">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3670">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3672">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3672">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3674">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3675">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3676">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3677">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3678">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3678">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3679">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3680">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3681">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3682">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3683">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3683">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3684">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3685">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3686">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3687">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3687">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3689">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3689">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3690">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3690">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3691">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3691">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3692">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3692">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3693">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3693">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3694">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3694">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3695">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3695">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3696">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3696">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3697">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3697">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3698">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3698">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3699">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3699">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3701">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="6e083-3702">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67) </span><span class="sxs-lookup"><span data-stu-id="6e083-3702">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="6e083-3703">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3703">Target</span></span> | <span data-ttu-id="6e083-3704">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3704">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3705">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3706">32</span><span class="sxs-lookup"><span data-stu-id="6e083-3706">32</span></span> |
| <span data-ttu-id="6e083-3707">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3707">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-3708">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3708">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3709">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3709">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3710">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3710">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3711">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3711">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3712">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3712">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3713">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3713">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-3714">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3714">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-3715">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3715">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-3716">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3716">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-3717">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3717">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-3718">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3718">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3719">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3719">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3720">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3720">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3721">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3721">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3722">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3722">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-3723">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3723">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3724">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3724">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3725">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3725">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3726">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3726">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3727">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3727">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3728">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3728">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3729">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3729">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3730">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3730">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3731">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3731">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3732">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3732">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3733">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3733">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3734">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3734">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3735">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3735">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3736">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3736">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3737">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3737">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3738">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3738">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3739">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3739">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-3740">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3740">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3741">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3741">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3742">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3742">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3743">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3743">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3744">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3744">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3745">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3745">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3746">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3746">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3747">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3747">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3748">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3748">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3749">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3749">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3750">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3750">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-3751">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3751">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="6e083-3752">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68) </span><span class="sxs-lookup"><span data-stu-id="6e083-3752">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="6e083-3753">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3753">Target</span></span> | <span data-ttu-id="6e083-3754">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3754">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3755">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3755">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3756">16</span><span class="sxs-lookup"><span data-stu-id="6e083-3756">16</span></span> |
| <span data-ttu-id="6e083-3757">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3757">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-3758">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3758">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3759">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3759">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3760">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3760">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3761">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3761">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3762">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3762">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3763">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3763">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-3764">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3764">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-3765">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3765">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-3766">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3766">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-3767">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3767">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-3768">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3768">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3769">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3769">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3770">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3770">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3771">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3771">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3772">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3772">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-3773">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3773">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3774">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3774">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3775">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3775">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3776">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3776">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3777">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3777">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3778">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3778">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3779">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3779">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3780">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3780">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3781">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3781">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3782">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3782">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3783">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3783">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3784">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3784">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3785">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3785">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3786">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3786">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3787">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3787">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3788">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3788">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3789">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3789">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-3790">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3790">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3791">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3791">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3792">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3792">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3793">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3793">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3794">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3794">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3795">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3795">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3796">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3796">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3797">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3797">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3798">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3798">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3799">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3799">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3800">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3800">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-3801">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3801">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="6e083-3802">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69) </span><span class="sxs-lookup"><span data-stu-id="6e083-3802">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="6e083-3803">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3803">Target</span></span> | <span data-ttu-id="6e083-3804">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3804">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3805">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3805">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3806">16</span><span class="sxs-lookup"><span data-stu-id="6e083-3806">16</span></span> |
| <span data-ttu-id="6e083-3807">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3807">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-3808">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3808">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3809">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3809">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3810">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3810">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3811">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3811">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3812">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3812">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3813">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3813">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-3814">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3814">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-3815">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3815">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-3816">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3816">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-3817">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3817">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-3818">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3818">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3819">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3819">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3820">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3820">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3821">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3821">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3822">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3822">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-3823">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3823">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3824">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3824">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3825">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3825">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3826">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3826">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3827">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3827">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3828">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3828">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3829">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3829">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3830">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3830">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3831">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3831">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3832">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3832">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3833">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3833">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3834">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3834">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3835">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3835">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3836">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3836">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3837">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3837">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3838">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3838">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3839">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3839">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-3840">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3840">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3841">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3841">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3842">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3842">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3843">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3843">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3844">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3844">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3845">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3845">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3846">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3846">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3847">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3847">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3848">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3848">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3849">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3849">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3850">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3850">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-3851">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3851">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="6e083-3852">DXGI_FORMAT_BC1 無別 \_ <sup>PCC</sup> (70) </span><span class="sxs-lookup"><span data-stu-id="6e083-3852">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="6e083-3853">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3853">Target</span></span> | <span data-ttu-id="6e083-3854">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3854">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3855">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3855">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3856">4</span><span class="sxs-lookup"><span data-stu-id="6e083-3856">4</span></span> |
| <span data-ttu-id="6e083-3857">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3857">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-3858">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3858">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3859">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3859">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3860">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3861">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3862">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3863">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3863">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-3864">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3864">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-3865">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3865">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-3866">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3866">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-3867">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3867">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-3868">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3868">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3869">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3869">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3870">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3870">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3871">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3871">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3872">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3872">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-3873">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3873">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3874">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3874">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3875">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3875">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3876">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3877">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3878">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3879">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3880">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3880">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3881">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3882">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3883">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3884">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3885">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3885">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3886">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3887">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3888">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3889">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3889">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-3890">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3890">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3891">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3891">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3892">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3892">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3893">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3893">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3894">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3894">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3895">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3895">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3896">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3896">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3897">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3897">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3898">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3898">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3899">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3899">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3900">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3900">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-3901">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3901">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a><span data-ttu-id="6e083-3902">DXGI_FORMAT_BC1 \_ UNORM<sup>FNC</sup> (71) </span><span class="sxs-lookup"><span data-stu-id="6e083-3902">DXGI_FORMAT_BC1\_UNORM<sup>FNC</sup> (71)</span></span>
| <span data-ttu-id="6e083-3903">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3903">Target</span></span> | <span data-ttu-id="6e083-3904">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3904">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3905">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3905">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3906">4</span><span class="sxs-lookup"><span data-stu-id="6e083-3906">4</span></span> |
| <span data-ttu-id="6e083-3907">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3907">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3909">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3909">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3910">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3910">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3911">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3911">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3912">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3912">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3913">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3913">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3914">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3914">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3916">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3916">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-3917">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3917">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3919">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3919">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3921">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3921">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3923">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3923">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3924">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3924">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3925">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3925">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3926">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3926">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3927">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3927">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3929">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3929">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3930">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3930">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3931">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3931">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3932">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3932">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3933">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3933">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3934">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3934">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3935">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3935">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3936">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3936">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3937">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3937">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3938">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3938">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3939">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3939">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3940">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3940">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3941">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3941">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-3942">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-3942">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-3943">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3943">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3944">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-3944">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-3945">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-3945">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3947">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3947">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3948">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3948">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3949">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-3949">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-3950">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-3950">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-3951">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3951">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-3952">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-3952">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-3953">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-3953">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-3954">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3954">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-3955">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-3955">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-3956">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-3956">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-3957">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3957">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3959">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-3959">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a><span data-ttu-id="6e083-3960">DXGI_FORMAT_BC1 \_ UNORM \_ SRGB<sup>FNC</sup> (72) </span><span class="sxs-lookup"><span data-stu-id="6e083-3960">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FNC</sup> (72)</span></span>
| <span data-ttu-id="6e083-3961">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3961">Target</span></span> | <span data-ttu-id="6e083-3962">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3962">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-3963">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-3963">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-3964">4</span><span class="sxs-lookup"><span data-stu-id="6e083-3964">4</span></span> |
| <span data-ttu-id="6e083-3965">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-3965">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3967">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-3967">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3968">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3968">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3969">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3969">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3970">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-3970">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-3971">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-3971">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-3972">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-3972">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3974">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-3974">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-3975">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-3975">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3977">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-3977">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3979">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3979">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3981">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3981">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-3982">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-3982">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-3983">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-3983">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-3984">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-3984">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-3985">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-3985">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-3987">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-3987">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-3988">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3988">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3989">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-3989">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-3990">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-3990">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-3991">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-3991">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-3992">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3992">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3993">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-3993">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-3994">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-3994">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-3995">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-3995">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-3996">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-3996">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-3997">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-3997">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-3998">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-3998">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-3999">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-3999">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4000">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4000">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4001">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4001">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4002">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4002">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4003">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4003">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4005">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4005">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4006">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4006">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4007">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4007">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-4008">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4008">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-4009">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4009">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4010">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4010">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-4011">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4011">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4012">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4012">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4013">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4013">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-4014">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4014">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-4015">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4015">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4017">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4017">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="6e083-4018">DXGI_FORMAT_BC2 無別 \_ <sup>PCC</sup> (73) </span><span class="sxs-lookup"><span data-stu-id="6e083-4018">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="6e083-4019">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4019">Target</span></span> | <span data-ttu-id="6e083-4020">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4020">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4021">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4021">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4022">8</span><span class="sxs-lookup"><span data-stu-id="6e083-4022">8</span></span> |
| <span data-ttu-id="6e083-4023">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4023">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-4024">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4024">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4025">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4025">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4026">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4026">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4027">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4027">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4028">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4028">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4029">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4029">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-4030">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4030">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-4031">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4031">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-4032">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4032">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-4033">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4033">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-4034">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4034">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4035">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4035">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4036">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4036">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4037">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4037">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4038">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4038">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-4039">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4039">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-4040">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4040">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4041">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4041">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4042">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4042">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4043">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4043">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4044">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4044">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4045">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4045">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4046">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4046">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4047">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4047">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4048">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4048">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4049">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4049">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4050">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4050">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4051">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4051">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4052">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4052">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4053">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4053">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4054">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4054">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4055">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4055">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-4056">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4056">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4057">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4057">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4058">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4058">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-4059">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4059">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-4060">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4060">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4061">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4061">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-4062">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4062">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4063">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4063">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4064">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4064">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-4065">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4065">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-4066">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4066">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-4067">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4067">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a><span data-ttu-id="6e083-4068">DXGI_FORMAT_BC2 \_ UNORM<sup>FNC</sup> (74) </span><span class="sxs-lookup"><span data-stu-id="6e083-4068">DXGI_FORMAT_BC2\_UNORM<sup>FNC</sup> (74)</span></span>
| <span data-ttu-id="6e083-4069">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4069">Target</span></span> | <span data-ttu-id="6e083-4070">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4070">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4071">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4071">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4072">8</span><span class="sxs-lookup"><span data-stu-id="6e083-4072">8</span></span> |
| <span data-ttu-id="6e083-4073">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4073">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4075">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4075">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4076">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4076">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4077">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4077">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4078">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4078">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4079">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4079">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4080">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4080">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4082">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4082">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-4083">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4083">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4085">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4085">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4087">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4087">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4089">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4089">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4090">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4090">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4091">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4091">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4092">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4092">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4093">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4093">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4095">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4095">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-4096">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4096">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4097">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4097">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4098">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4099">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4100">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4101">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4102">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4102">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4103">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4103">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4104">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4104">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4105">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4105">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4106">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4106">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4107">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4107">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4108">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4108">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4109">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4109">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4110">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4110">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4111">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4111">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4113">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4113">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4114">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4114">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4115">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4115">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-4116">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4116">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-4117">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4117">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4118">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4118">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-4119">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4119">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4120">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4120">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4121">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4121">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-4122">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4122">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-4123">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4123">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4125">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4125">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a><span data-ttu-id="6e083-4126">DXGI_FORMAT_BC2 \_ UNORM \_ SRGB<sup>FNC</sup> (75) </span><span class="sxs-lookup"><span data-stu-id="6e083-4126">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FNC</sup> (75)</span></span>
| <span data-ttu-id="6e083-4127">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4127">Target</span></span> | <span data-ttu-id="6e083-4128">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4128">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4129">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4129">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4130">8</span><span class="sxs-lookup"><span data-stu-id="6e083-4130">8</span></span> |
| <span data-ttu-id="6e083-4131">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4131">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4133">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4133">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4134">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4134">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4135">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4135">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4136">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4136">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4137">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4137">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4138">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4138">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4140">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4140">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-4141">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4141">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4143">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4143">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4145">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4145">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4147">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4147">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4148">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4148">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4149">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4149">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4150">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4150">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4151">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4151">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4153">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4153">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-4154">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4154">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4155">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4155">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4156">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4156">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4157">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4157">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4158">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4158">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4159">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4159">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4160">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4160">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4161">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4161">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4162">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4162">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4163">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4163">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4164">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4164">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4165">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4165">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4166">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4166">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4167">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4167">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4168">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4168">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4169">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4169">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4171">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4171">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4172">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4172">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4173">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4173">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-4174">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4174">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-4175">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4175">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4176">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4176">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-4177">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4177">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4178">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4178">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4179">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4179">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-4180">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4180">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-4181">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4181">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4183">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4183">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="6e083-4184">DXGI_FORMAT_BC3 無別 \_ <sup>PCC</sup> (76) </span><span class="sxs-lookup"><span data-stu-id="6e083-4184">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="6e083-4185">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4185">Target</span></span> | <span data-ttu-id="6e083-4186">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4186">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4187">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4187">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4188">8</span><span class="sxs-lookup"><span data-stu-id="6e083-4188">8</span></span> |
| <span data-ttu-id="6e083-4189">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4189">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-4190">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4190">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4191">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4191">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4192">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4192">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4193">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4193">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4194">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4194">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4195">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4195">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-4196">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4196">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-4197">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4197">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-4198">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4198">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-4199">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4199">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-4200">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4200">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4201">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4201">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4202">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4202">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4203">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4203">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4204">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4204">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-4205">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4205">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-4206">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4206">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4207">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4207">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4208">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4208">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4209">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4209">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4210">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4210">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4211">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4211">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4212">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4212">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4213">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4213">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4214">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4214">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4215">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4215">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4216">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4216">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4217">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4217">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4218">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4218">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4219">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4219">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4220">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4220">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4221">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4221">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-4222">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4223">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4224">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-4225">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-4226">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4226">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4227">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-4228">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4228">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4229">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4229">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4230">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4230">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-4231">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4231">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-4232">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4232">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-4233">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4233">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a><span data-ttu-id="6e083-4234">DXGI_FORMAT_BC3 \_ UNORM<sup>FNC</sup> (77) </span><span class="sxs-lookup"><span data-stu-id="6e083-4234">DXGI_FORMAT_BC3\_UNORM<sup>FNC</sup> (77)</span></span>
| <span data-ttu-id="6e083-4235">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4235">Target</span></span> | <span data-ttu-id="6e083-4236">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4236">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4237">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4237">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4238">8</span><span class="sxs-lookup"><span data-stu-id="6e083-4238">8</span></span> |
| <span data-ttu-id="6e083-4239">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4239">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4241">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4241">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4242">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4242">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4243">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4243">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4244">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4244">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4245">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4245">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4246">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4246">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4248">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4248">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-4249">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4249">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4251">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4251">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4253">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4253">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4255">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4255">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4256">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4256">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4257">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4257">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4258">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4258">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4259">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4259">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4261">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4261">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-4262">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4262">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4263">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4263">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4264">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4264">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4265">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4265">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4266">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4266">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4267">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4267">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4268">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4268">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4269">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4269">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4270">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4270">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4271">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4271">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4272">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4272">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4273">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4273">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4274">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4274">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4275">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4275">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4276">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4276">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4277">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4277">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4279">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4279">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4280">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4280">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4281">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4281">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-4282">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4282">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-4283">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4283">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4284">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4284">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-4285">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4285">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4286">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4286">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4287">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4287">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-4288">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4288">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-4289">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4289">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4291">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4291">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a><span data-ttu-id="6e083-4292">DXGI_FORMAT_BC3 \_ UNORM \_ SRGB<sup>FNC</sup> (78) </span><span class="sxs-lookup"><span data-stu-id="6e083-4292">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FNC</sup> (78)</span></span>
| <span data-ttu-id="6e083-4293">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4293">Target</span></span> | <span data-ttu-id="6e083-4294">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4294">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4295">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4295">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4296">8</span><span class="sxs-lookup"><span data-stu-id="6e083-4296">8</span></span> |
| <span data-ttu-id="6e083-4297">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4297">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4299">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4299">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4300">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4300">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4301">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4301">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4302">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4302">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4303">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4303">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4304">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4304">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4306">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4306">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-4307">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4307">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4309">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4309">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4311">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4311">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4313">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4313">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4314">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4314">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4315">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4315">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4316">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4316">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4317">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4317">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4319">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4319">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-4320">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4320">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4321">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4321">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4322">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4322">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4323">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4323">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4324">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4324">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4325">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4325">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4326">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4326">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4327">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4327">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4328">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4328">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4329">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4329">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4330">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4330">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4331">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4331">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4332">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4332">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4333">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4333">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4334">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4334">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4335">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4335">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4337">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4337">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4338">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4338">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4339">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4339">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-4340">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4340">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-4341">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4341">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4342">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4342">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-4343">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4343">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4344">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4344">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4345">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4345">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-4346">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4346">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-4347">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4347">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4349">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4349">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="6e083-4350">DXGI_FORMAT_BC4 無別 \_ <sup>PCC</sup> (79) </span><span class="sxs-lookup"><span data-stu-id="6e083-4350">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="6e083-4351">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4351">Target</span></span> | <span data-ttu-id="6e083-4352">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4352">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4353">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4353">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4354">4</span><span class="sxs-lookup"><span data-stu-id="6e083-4354">4</span></span> |
| <span data-ttu-id="6e083-4355">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4355">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-4356">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4356">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4357">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4357">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4358">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4358">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4359">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4359">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4360">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4360">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4361">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4361">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-4362">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4362">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-4363">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4363">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-4364">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4364">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-4365">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4365">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-4366">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4366">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4367">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4367">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4368">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4368">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4369">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4369">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4370">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4370">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-4371">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4371">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-4372">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4372">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4373">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4373">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4374">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4375">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4375">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4376">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4376">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4377">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4377">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4378">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4378">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4379">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4379">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4380">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4380">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4381">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4381">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4382">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4382">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4383">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4383">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4384">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4384">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4385">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4385">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4386">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4386">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4387">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4387">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-4388">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4388">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4389">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4389">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4390">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4390">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-4391">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4391">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-4392">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4392">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4393">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4393">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-4394">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4394">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4395">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4395">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4396">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4396">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-4397">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4397">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-4398">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4398">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-4399">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4399">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a><span data-ttu-id="6e083-4400">DXGI_FORMAT_BC4 \_ UNORM<sup>FNC</sup> (80) </span><span class="sxs-lookup"><span data-stu-id="6e083-4400">DXGI_FORMAT_BC4\_UNORM<sup>FNC</sup> (80)</span></span>
| <span data-ttu-id="6e083-4401">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4401">Target</span></span> | <span data-ttu-id="6e083-4402">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4402">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4403">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4403">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4404">4</span><span class="sxs-lookup"><span data-stu-id="6e083-4404">4</span></span> |
| <span data-ttu-id="6e083-4405">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4405">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-4406">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4406">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4407">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4407">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4408">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4408">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4409">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4409">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4410">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4410">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4411">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4411">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-4412">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4412">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-4413">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4413">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-4414">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4414">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-4415">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4415">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-4416">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4416">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4417">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4417">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4418">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4418">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4419">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4419">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4420">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4420">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-4421">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4421">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-4422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4422">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4423">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4423">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4424">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4424">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4425">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4425">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4426">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4426">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4427">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4427">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4428">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4428">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4429">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4429">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4430">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4430">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4431">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4431">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4432">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4432">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4433">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4433">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4434">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4434">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4435">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4435">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4436">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4436">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4437">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4437">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-4438">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4438">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4439">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4439">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4440">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4440">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-4441">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4441">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-4442">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4442">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4443">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4443">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-4444">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4444">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4445">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4445">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4446">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4446">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-4447">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4447">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-4448">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4448">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-4449">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4449">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a><span data-ttu-id="6e083-4450">DXGI_FORMAT_BC4 \_ SNORM<sup>FNC</sup> (81) </span><span class="sxs-lookup"><span data-stu-id="6e083-4450">DXGI_FORMAT_BC4\_SNORM<sup>FNC</sup> (81)</span></span>
| <span data-ttu-id="6e083-4451">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4451">Target</span></span> | <span data-ttu-id="6e083-4452">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4452">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4453">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4453">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4454">4</span><span class="sxs-lookup"><span data-stu-id="6e083-4454">4</span></span> |
| <span data-ttu-id="6e083-4455">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4455">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-4456">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4456">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4457">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4457">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4458">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4458">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4459">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4459">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4460">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4460">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4461">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4461">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-4462">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4462">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-4463">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4463">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-4464">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4464">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-4465">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4465">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-4466">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4466">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4467">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4467">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4468">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4468">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4469">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4469">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4470">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4470">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-4471">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4471">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-4472">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4472">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4473">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4473">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4474">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4474">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4475">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4475">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4476">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4476">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4477">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4477">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4478">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4478">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4479">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4479">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4480">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4480">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4481">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4481">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4482">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4482">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4483">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4483">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4484">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4484">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4485">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4485">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4486">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4486">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4487">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4487">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-4488">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4488">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4489">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4489">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4490">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4490">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-4491">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4491">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-4492">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4492">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4493">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4493">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-4494">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4494">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4495">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4496">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-4497">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-4498">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4498">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-4499">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="6e083-4500">DXGI_FORMAT_BC5 無別 \_ <sup>PCC</sup> (82) </span><span class="sxs-lookup"><span data-stu-id="6e083-4500">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="6e083-4501">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4501">Target</span></span> | <span data-ttu-id="6e083-4502">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4502">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4503">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4504">8</span><span class="sxs-lookup"><span data-stu-id="6e083-4504">8</span></span> |
| <span data-ttu-id="6e083-4505">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4505">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-4506">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4506">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4507">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4507">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4508">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4508">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4509">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4509">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4510">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4510">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4511">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4511">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-4512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4512">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-4513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4513">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-4514">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4514">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-4515">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4515">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-4516">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4516">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4517">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4517">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4518">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4518">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4519">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4519">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4520">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4520">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-4521">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4521">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-4522">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4522">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4523">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4523">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4524">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4524">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4525">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4525">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4526">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4526">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4527">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4527">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4528">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4528">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4529">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4529">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4530">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4530">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4531">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4531">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4532">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4532">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4533">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4533">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4534">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4534">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4535">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4535">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4536">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4536">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4537">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4537">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-4538">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4538">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4539">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4539">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4540">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4540">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-4541">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4541">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-4542">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4542">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4543">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4543">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-4544">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4544">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4545">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4545">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4546">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4546">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-4547">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4547">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-4548">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4548">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-4549">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4549">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a><span data-ttu-id="6e083-4550">DXGI_FORMAT_BC5 \_ UNORM<sup>FNC</sup> (83) </span><span class="sxs-lookup"><span data-stu-id="6e083-4550">DXGI_FORMAT_BC5\_UNORM<sup>FNC</sup> (83)</span></span>
| <span data-ttu-id="6e083-4551">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4551">Target</span></span> | <span data-ttu-id="6e083-4552">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4552">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4553">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4553">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4554">8</span><span class="sxs-lookup"><span data-stu-id="6e083-4554">8</span></span> |
| <span data-ttu-id="6e083-4555">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4555">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-4556">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4556">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4557">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4557">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4558">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4558">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4559">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4559">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4560">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4560">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4561">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4561">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-4562">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4562">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-4563">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4563">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-4564">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4564">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-4565">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4565">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-4566">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4566">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4567">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4567">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4568">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4568">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4569">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4569">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4570">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4570">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-4571">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4571">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-4572">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4572">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4573">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4573">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4574">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4574">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4575">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4575">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4576">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4576">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4577">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4577">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4578">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4578">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4579">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4579">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4580">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4580">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4581">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4581">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4582">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4582">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4583">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4583">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4584">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4584">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4585">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4585">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4586">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4586">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4587">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4587">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-4588">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4588">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4589">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4589">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4590">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4590">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-4591">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4591">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-4592">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4592">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4593">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4593">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-4594">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4594">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4595">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4595">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4596">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4596">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-4597">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4597">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-4598">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4598">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-4599">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4599">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a><span data-ttu-id="6e083-4600">DXGI_FORMAT_BC5 \_ SNORM<sup>FNC</sup> (84) </span><span class="sxs-lookup"><span data-stu-id="6e083-4600">DXGI_FORMAT_BC5\_SNORM<sup>FNC</sup> (84)</span></span>
| <span data-ttu-id="6e083-4601">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4601">Target</span></span> | <span data-ttu-id="6e083-4602">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4602">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4603">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4603">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4604">8</span><span class="sxs-lookup"><span data-stu-id="6e083-4604">8</span></span> |
| <span data-ttu-id="6e083-4605">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4605">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-4606">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4606">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4607">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4607">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4608">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4608">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4609">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4609">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4610">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4610">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4611">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4611">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-4612">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4612">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-4613">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4613">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-4614">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4614">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-4615">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4615">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-4616">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4616">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4617">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4617">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4618">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4618">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4619">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4619">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4620">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4620">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-4621">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4621">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-4622">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4622">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4623">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4623">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4624">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4624">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4625">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4625">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4626">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4626">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4627">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4627">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4628">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4628">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4629">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4629">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4630">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4630">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4631">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4631">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4632">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4632">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4633">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4633">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4634">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4634">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4635">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4635">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4636">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4636">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4637">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4637">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-4638">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4638">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4639">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4639">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4640">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4640">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-4641">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4641">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-4642">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4642">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4643">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4643">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-4644">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4644">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4645">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4645">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4646">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4646">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-4647">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4647">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-4648">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4648">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-4649">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4649">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="6e083-4650">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85) </span><span class="sxs-lookup"><span data-stu-id="6e083-4650">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="6e083-4651">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4651">Target</span></span> | <span data-ttu-id="6e083-4652">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4652">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4653">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4653">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4654">16</span><span class="sxs-lookup"><span data-stu-id="6e083-4654">16</span></span> |
| <span data-ttu-id="6e083-4655">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4655">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4657">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4657">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4658">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4658">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4659">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4659">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4660">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4660">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4661">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4661">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4662">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4662">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4664">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4664">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-4665">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4665">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4667">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4667">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4669">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4669">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4671">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4671">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4672">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4672">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4673">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4673">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4674">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4674">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4675">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4675">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4677">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4677">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4679">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4679">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4681">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4681">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4683">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4683">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4684">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4684">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4685">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4685">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4686">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4686">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4687">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4687">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4688">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4688">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4689">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4689">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4690">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4690">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4691">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4691">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4692">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4692">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4693">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4693">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4694">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4694">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4695">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4695">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4696">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4696">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4698">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4698">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-4700">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4700">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-4702">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4702">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-4704">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4704">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4706">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4706">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4707">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4707">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-4708">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4708">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4709">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4709">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4710">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4710">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-4711">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4711">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-4712">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4712">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-4713">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4713">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="6e083-4714">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86) </span><span class="sxs-lookup"><span data-stu-id="6e083-4714">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="6e083-4715">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4715">Target</span></span> | <span data-ttu-id="6e083-4716">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4716">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4717">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4717">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4718">16</span><span class="sxs-lookup"><span data-stu-id="6e083-4718">16</span></span> |
| <span data-ttu-id="6e083-4719">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4719">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4721">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4721">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4722">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4722">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4723">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4723">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4724">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4724">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4725">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4725">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4726">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4728">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-4729">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4729">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4731">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4731">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4733">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4733">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4735">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4735">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4736">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4736">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4737">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4737">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4738">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4738">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4739">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4739">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4741">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4741">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-4742">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4742">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4743">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4743">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4744">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4744">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4745">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4745">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4746">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4746">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4747">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4747">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4748">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4748">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4749">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4749">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4750">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4750">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4751">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4751">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4752">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4752">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4753">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4753">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4754">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4754">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4755">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4755">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4756">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4756">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4757">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4757">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4759">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4759">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4760">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4760">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4761">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4761">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-4762">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4762">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-4763">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4763">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4764">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4764">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-4765">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4765">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4766">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4766">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4767">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4767">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-4768">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4768">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-4769">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4769">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-4770">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4770">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="6e083-4771">DXGI_FORMAT_B8G8R8A8 無的 \_ <sup>電腦</sup> (90) </span><span class="sxs-lookup"><span data-stu-id="6e083-4771">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="6e083-4772">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4772">Target</span></span> | <span data-ttu-id="6e083-4773">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4773">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4774">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4774">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4775">32</span><span class="sxs-lookup"><span data-stu-id="6e083-4775">32</span></span> |
| <span data-ttu-id="6e083-4776">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4776">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-4777">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4777">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4778">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4778">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4779">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4779">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4780">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4780">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4781">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4781">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4782">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4782">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-4783">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4783">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-4784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4784">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-4785">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4785">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-4786">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4786">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-4787">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4787">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4788">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4788">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4789">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4789">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4790">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4790">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4791">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4791">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-4792">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4792">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-4793">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4793">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4794">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4794">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4795">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4795">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4796">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4796">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4797">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4797">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4798">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4798">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4799">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4799">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4800">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4800">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4801">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4801">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4802">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4802">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4803">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4803">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4804">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4804">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4805">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4805">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4806">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4806">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4807">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4807">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4808">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4808">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-4809">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4809">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4810">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4810">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4811">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4811">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-4812">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4812">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-4813">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4813">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4814">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4814">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-4815">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4815">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4816">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4816">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4817">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4817">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-4818">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4818">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-4819">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4819">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-4820">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4820">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a><span data-ttu-id="6e083-4821">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FNS</sup> (87) </span><span class="sxs-lookup"><span data-stu-id="6e083-4821">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FNS</sup> (87)</span></span>
| <span data-ttu-id="6e083-4822">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4822">Target</span></span> | <span data-ttu-id="6e083-4823">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4823">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4824">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4824">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4825">32</span><span class="sxs-lookup"><span data-stu-id="6e083-4825">32</span></span> |
| <span data-ttu-id="6e083-4826">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4826">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4828">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4828">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4829">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4829">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4830">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4830">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4831">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4831">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4832">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4832">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4833">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4833">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4835">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4835">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4837">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4837">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4839">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4839">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4841">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4841">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4843">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4843">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4844">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4844">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4845">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4845">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4846">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4846">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4847">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4847">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4849">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4849">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4851">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4851">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4853">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4853">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4855">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4855">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4856">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4856">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4857">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4857">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4858">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4858">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4859">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4859">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4860">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4860">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4861">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4861">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4862">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4862">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4863">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4863">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4864">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4864">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4865">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4865">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4866">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4866">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4867">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4867">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4868">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4868">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4870">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4870">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-4872">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4872">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-4874">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4874">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-4876">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4876">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4878">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4878">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4879">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4879">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4881">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4881">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4882">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4882">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4883">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4883">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-4885">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4885">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4887">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4887">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4889">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4889">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a><span data-ttu-id="6e083-4890">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ SRGB<sup>FNS</sup> (91) </span><span class="sxs-lookup"><span data-stu-id="6e083-4890">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FNS</sup> (91)</span></span>
| <span data-ttu-id="6e083-4891">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4891">Target</span></span> | <span data-ttu-id="6e083-4892">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4892">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4893">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4893">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4894">32</span><span class="sxs-lookup"><span data-stu-id="6e083-4894">32</span></span> |
| <span data-ttu-id="6e083-4895">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4895">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4897">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4897">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4898">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4898">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4899">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4899">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4900">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4900">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4901">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4901">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4902">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4902">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4904">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4904">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4906">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4906">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4908">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4908">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4910">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4910">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4912">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4912">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4913">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4913">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4914">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4914">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4915">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4915">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4916">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4916">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4918">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4918">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4920">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4920">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4922">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4922">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4924">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4924">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4925">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4925">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4926">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4926">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4927">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4927">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4928">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4928">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4929">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4929">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4930">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4930">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4931">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4931">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4932">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4932">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4933">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4933">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4934">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4934">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4935">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4935">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4936">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4936">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4937">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4937">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4939">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4939">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-4941">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4941">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-4943">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4943">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-4945">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-4945">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4947">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4947">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-4948">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-4948">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4950">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-4950">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-4951">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4951">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-4952">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-4952">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-4954">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-4954">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4956">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4956">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-4958">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-4958">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="6e083-4959">DXGI_FORMAT_B8G8R8X8 無的 \_ <sup>電腦</sup> (92) </span><span class="sxs-lookup"><span data-stu-id="6e083-4959">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="6e083-4960">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4960">Target</span></span> | <span data-ttu-id="6e083-4961">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4961">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-4962">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-4962">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-4963">32</span><span class="sxs-lookup"><span data-stu-id="6e083-4963">32</span></span> |
| <span data-ttu-id="6e083-4964">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-4964">Format Support</span></span> | \- |
| <span data-ttu-id="6e083-4965">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-4965">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4966">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4966">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4967">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4967">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4968">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-4968">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-4969">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-4969">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-4970">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-4970">Texture2D</span></span> | \- |
| <span data-ttu-id="6e083-4971">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-4971">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-4972">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-4972">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-4973">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-4973">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-4974">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4974">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-4975">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4975">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-4976">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-4976">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-4977">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-4977">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-4978">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-4978">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-4979">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-4979">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-4980">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-4980">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-4981">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4981">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4982">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4982">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4983">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-4983">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-4984">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-4984">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-4985">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4985">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4986">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-4986">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-4987">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-4987">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-4988">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-4988">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-4989">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-4989">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-4990">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-4990">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-4991">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-4991">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-4992">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-4992">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-4993">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-4993">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-4994">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4994">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4995">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-4995">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-4996">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-4996">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-4997">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4997">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4998">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-4998">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-4999">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-4999">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-5000">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5000">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-5001">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5001">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5002">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5002">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5003">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5003">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5004">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5004">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-5005">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5005">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-5006">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5006">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-5007">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5007">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-5008">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5008">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a><span data-ttu-id="6e083-5009">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FNS</sup> (88) </span><span class="sxs-lookup"><span data-stu-id="6e083-5009">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FNS</sup> (88)</span></span>
| <span data-ttu-id="6e083-5010">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5010">Target</span></span> | <span data-ttu-id="6e083-5011">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5011">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5012">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5012">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5013">32</span><span class="sxs-lookup"><span data-stu-id="6e083-5013">32</span></span> |
| <span data-ttu-id="6e083-5014">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5014">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5016">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5016">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5017">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5017">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5018">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5018">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5019">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5019">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5020">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5020">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5021">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5023">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5025">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5027">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5027">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5029">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5029">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5031">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5032">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5033">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5033">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5034">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5035">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5035">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5037">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-5037">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5039">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5041">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5041">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5043">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-5043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-5044">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-5045">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5046">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5047">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-5047">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-5048">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-5048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-5049">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-5050">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-5050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-5051">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-5051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-5052">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-5052">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-5053">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-5053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-5054">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5055">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5056">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-5056">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5058">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5058">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5060">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5060">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5062">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-5062">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5064">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5064">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5066">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5066">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5067">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5068">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5069">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-5070">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5070">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5072">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5072">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5074">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5074">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5076">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5076">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a><span data-ttu-id="6e083-5077">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ SRGB<sup>FNS</sup> (93) </span><span class="sxs-lookup"><span data-stu-id="6e083-5077">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FNS</sup> (93)</span></span>
| <span data-ttu-id="6e083-5078">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5078">Target</span></span> | <span data-ttu-id="6e083-5079">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5079">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5080">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5080">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5081">32</span><span class="sxs-lookup"><span data-stu-id="6e083-5081">32</span></span> |
| <span data-ttu-id="6e083-5082">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5082">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5084">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5084">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5085">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5085">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5086">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5086">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5087">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5087">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5088">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5088">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5089">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5089">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5091">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5091">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5093">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5093">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5095">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5095">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5097">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5097">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5099">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5099">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5100">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5100">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5101">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5101">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5102">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5102">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5103">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5103">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5105">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-5105">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5107">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5107">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5109">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5109">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5111">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-5111">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-5112">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5112">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-5113">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5113">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5114">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5114">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5115">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-5115">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-5116">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-5116">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-5117">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5117">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-5118">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-5118">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-5119">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-5119">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-5120">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-5120">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-5121">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-5121">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-5122">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5122">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5123">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5123">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5124">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-5124">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5126">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5126">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5128">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5128">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5130">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-5130">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5132">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5132">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5134">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5134">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5135">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5135">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5136">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5136">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5137">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5137">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-5138">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5138">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-5139">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5139">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-5140">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5140">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5142">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5142">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="6e083-5143">DXGI_FORMAT_AYUV<sup>V</sup> (100) </span><span class="sxs-lookup"><span data-stu-id="6e083-5143">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="6e083-5144">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5144">Target</span></span> | <span data-ttu-id="6e083-5145">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5145">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5146">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5146">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5147">32</span><span class="sxs-lookup"><span data-stu-id="6e083-5147">32</span></span> |
| <span data-ttu-id="6e083-5148">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5148">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5150">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5150">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5151">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5151">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5152">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5152">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5153">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5153">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5154">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5154">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5155">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5155">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5157">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5157">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-5158">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5158">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-5159">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5159">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-5160">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5160">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-5161">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5161">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5162">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5162">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5163">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5163">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5164">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5164">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5165">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5165">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-5166">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-5166">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-5167">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5167">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5168">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5168">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5169">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-5169">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-5170">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5170">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-5171">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5171">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5172">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5172">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5173">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-5173">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-5174">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-5174">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-5175">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5175">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-5176">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-5176">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-5177">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-5177">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-5178">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-5178">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-5179">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-5179">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-5180">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5180">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5181">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5181">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5182">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-5182">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5184">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5184">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5185">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5185">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5186">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-5186">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-5187">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5187">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-5188">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5188">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5189">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5189">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5190">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5190">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5191">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5191">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5193">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5193">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5195">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5195">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5197">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5197">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-5198">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5198">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="6e083-5199">DXGI_FORMAT_Y410<sup>V</sup> (101) </span><span class="sxs-lookup"><span data-stu-id="6e083-5199">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="6e083-5200">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5200">Target</span></span> | <span data-ttu-id="6e083-5201">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5201">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5202">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5202">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5203">32</span><span class="sxs-lookup"><span data-stu-id="6e083-5203">32</span></span> |
| <span data-ttu-id="6e083-5204">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5204">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5206">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5206">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5207">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5207">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5208">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5208">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5209">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5209">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5210">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5210">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5211">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5211">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5213">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5213">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-5214">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5214">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-5215">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5215">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-5216">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5216">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-5217">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5217">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5218">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5218">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5219">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5219">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5220">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5220">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5221">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5221">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-5222">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-5222">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-5223">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5223">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5224">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5224">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5225">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-5225">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-5226">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5226">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-5227">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5227">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5228">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5228">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5229">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-5229">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-5230">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-5230">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-5231">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5231">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-5232">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-5232">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-5233">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-5233">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-5234">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-5234">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-5235">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-5235">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-5236">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5236">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5237">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5237">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5238">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-5238">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5240">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5240">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5241">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5241">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5242">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-5242">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-5243">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5243">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-5244">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5244">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5245">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5245">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5246">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5246">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5247">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5247">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5249">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5249">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5251">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5251">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5253">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5253">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-5254">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5254">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="6e083-5255">DXGI_FORMAT_Y416<sup>V</sup> (102) </span><span class="sxs-lookup"><span data-stu-id="6e083-5255">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="6e083-5256">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5256">Target</span></span> | <span data-ttu-id="6e083-5257">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5257">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5258">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5258">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5259">64</span><span class="sxs-lookup"><span data-stu-id="6e083-5259">64</span></span> |
| <span data-ttu-id="6e083-5260">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5260">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5262">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5262">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5263">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5263">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5264">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5264">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5265">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5265">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5266">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5266">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5267">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5269">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-5270">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5270">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-5271">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5271">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-5272">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5272">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-5273">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5273">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5274">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5274">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5275">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5275">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5276">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5276">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5277">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5277">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-5278">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-5278">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-5279">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5279">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5280">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5280">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5281">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-5281">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-5282">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-5283">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5284">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5285">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-5285">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-5286">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-5286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-5287">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-5288">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-5288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-5289">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-5289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-5290">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-5290">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-5291">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-5291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-5292">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5293">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5294">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-5294">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5296">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5296">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5297">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5297">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5298">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-5298">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-5299">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5299">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-5300">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5300">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5301">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5301">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5302">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5302">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5303">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5303">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5305">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5305">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5307">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5307">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5309">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5309">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-5310">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5310">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="6e083-5311">DXGI_FORMAT_NV12<sup>V</sup> (103) </span><span class="sxs-lookup"><span data-stu-id="6e083-5311">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="6e083-5312">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5312">Target</span></span> | <span data-ttu-id="6e083-5313">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5313">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5314">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5314">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5315">8</span><span class="sxs-lookup"><span data-stu-id="6e083-5315">8</span></span> |
| <span data-ttu-id="6e083-5316">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5316">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5318">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5318">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5319">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5319">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5320">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5321">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5321">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5322">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5322">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5323">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5323">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5325">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5325">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-5326">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5326">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-5327">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5327">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-5328">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5328">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-5329">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5329">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5330">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5330">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5331">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5331">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5332">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5332">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5333">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5333">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-5334">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-5334">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-5335">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5335">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5336">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5336">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5337">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-5337">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-5338">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5338">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-5339">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5339">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5340">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5340">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5341">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-5341">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-5342">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-5342">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-5343">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5343">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-5344">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-5344">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-5345">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-5345">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-5346">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-5346">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-5347">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-5347">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-5348">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5348">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5349">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5349">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5350">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-5350">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5352">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5352">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5353">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5353">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5354">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-5354">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-5355">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5355">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-5356">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5356">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5357">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5357">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5358">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5358">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5359">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5359">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5361">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5361">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5363">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5363">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5365">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5365">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-5366">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5366">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="6e083-5367">DXGI_FORMAT_P010<sup>V</sup> (104) </span><span class="sxs-lookup"><span data-stu-id="6e083-5367">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="6e083-5368">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5368">Target</span></span> | <span data-ttu-id="6e083-5369">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5369">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5370">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5370">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5371">16</span><span class="sxs-lookup"><span data-stu-id="6e083-5371">16</span></span> |
| <span data-ttu-id="6e083-5372">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5372">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5374">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5374">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5375">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5375">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5376">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5376">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5377">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5377">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5378">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5378">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5379">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5379">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5381">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5381">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-5382">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5382">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-5383">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5383">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-5384">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5384">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-5385">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5385">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5386">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5386">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5387">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5387">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5388">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5388">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5389">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5389">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-5390">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-5390">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-5391">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5391">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5392">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5392">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5393">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-5393">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-5394">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5394">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-5395">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5395">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5396">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5396">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5397">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-5397">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-5398">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-5398">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-5399">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5399">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-5400">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-5400">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-5401">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-5401">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-5402">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-5402">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-5403">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-5403">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-5404">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5404">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5405">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5405">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5406">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-5406">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5408">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5408">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5409">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5409">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5410">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-5410">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-5411">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5411">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-5412">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5412">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5413">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5413">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5414">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5414">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5415">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5415">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5417">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5417">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5419">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5419">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5421">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5421">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-5422">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5422">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="6e083-5423">DXGI_FORMAT_P016<sup>V</sup> (105) </span><span class="sxs-lookup"><span data-stu-id="6e083-5423">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="6e083-5424">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5424">Target</span></span> | <span data-ttu-id="6e083-5425">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5425">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5426">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5426">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5427">16</span><span class="sxs-lookup"><span data-stu-id="6e083-5427">16</span></span> |
| <span data-ttu-id="6e083-5428">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5428">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5430">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5430">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5431">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5431">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5432">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5432">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5433">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5433">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5434">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5434">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5435">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5435">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5437">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5437">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-5438">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5438">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-5439">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5439">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-5440">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-5441">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5442">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5443">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5443">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5444">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5445">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5445">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-5446">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-5446">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-5447">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5447">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5448">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5448">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5449">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-5449">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-5450">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5450">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-5451">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5451">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5452">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5452">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5453">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-5453">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-5454">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-5454">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-5455">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5455">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-5456">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-5456">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-5457">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-5457">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-5458">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-5458">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-5459">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-5459">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-5460">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5460">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5461">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5461">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5462">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-5462">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5464">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5464">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5465">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5465">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5466">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-5466">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-5467">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5467">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-5468">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5468">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5469">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5469">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5470">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5470">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5471">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5471">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5473">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5473">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5475">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5475">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5477">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5477">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-5478">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5478">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="6e083-5479">DXGI_FORMAT_420 不 \_ 透明的<sup>V</sup> (106) </span><span class="sxs-lookup"><span data-stu-id="6e083-5479">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="6e083-5480">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5480">Target</span></span> | <span data-ttu-id="6e083-5481">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5481">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5482">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5482">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5483">8</span><span class="sxs-lookup"><span data-stu-id="6e083-5483">8</span></span> |
| <span data-ttu-id="6e083-5484">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5484">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5486">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5486">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5487">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5487">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5488">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5488">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5489">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5489">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5490">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5490">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5491">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5491">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5493">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5493">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-5494">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5494">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-5495">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5495">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-5496">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5496">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-5497">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5497">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5498">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5498">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5499">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5499">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5500">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5500">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5501">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5501">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-5502">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-5502">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-5503">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5503">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5504">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5504">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5505">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-5505">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-5506">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5506">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-5507">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5507">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5508">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5508">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5509">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-5509">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-5510">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-5510">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-5511">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5511">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-5512">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-5512">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-5513">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-5513">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-5514">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-5514">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-5515">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-5515">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-5516">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5516">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5517">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5517">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5518">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-5518">CPU Lockable</span></span> | \- |
| <span data-ttu-id="6e083-5519">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5519">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5520">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5520">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5521">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-5521">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-5522">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5522">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-5523">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5523">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5524">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5524">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5525">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5525">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5526">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5526">Video Decoder Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5528">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5528">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5530">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5530">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5532">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5532">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-5533">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5533">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="6e083-5534">DXGI_FORMAT_YUY2<sup>V</sup> (107) </span><span class="sxs-lookup"><span data-stu-id="6e083-5534">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="6e083-5535">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5535">Target</span></span> | <span data-ttu-id="6e083-5536">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5536">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5537">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5537">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5538">16</span><span class="sxs-lookup"><span data-stu-id="6e083-5538">16</span></span> |
| <span data-ttu-id="6e083-5539">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5539">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5541">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5541">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5542">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5542">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5543">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5543">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5544">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5544">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5545">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5545">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5546">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5546">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5548">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5548">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-5549">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5549">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-5550">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5550">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-5551">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5551">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-5552">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5552">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5553">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5553">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5554">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5554">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5555">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5555">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5556">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5556">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-5557">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-5557">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-5558">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5558">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5559">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5559">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5560">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-5560">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-5561">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5561">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-5562">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5562">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5563">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5563">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5564">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-5564">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-5565">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-5565">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-5566">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5566">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-5567">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-5567">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-5568">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-5568">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-5569">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-5569">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-5570">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-5570">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-5571">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5571">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5572">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5572">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5573">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-5573">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5575">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5575">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5576">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5576">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5577">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-5577">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-5578">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5578">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-5579">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5579">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5580">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5580">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5581">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5581">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5582">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5582">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5584">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5584">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5586">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5586">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5588">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5588">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-5589">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5589">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="6e083-5590">DXGI_FORMAT_Y210<sup>V</sup> (108) </span><span class="sxs-lookup"><span data-stu-id="6e083-5590">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="6e083-5591">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5591">Target</span></span> | <span data-ttu-id="6e083-5592">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5592">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5593">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5593">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5594">32</span><span class="sxs-lookup"><span data-stu-id="6e083-5594">32</span></span> |
| <span data-ttu-id="6e083-5595">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5595">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5597">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5597">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5598">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5598">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5599">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5599">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5600">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5600">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5601">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5601">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5602">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5602">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5604">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-5605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5605">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-5606">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-5607">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-5608">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5609">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5610">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5610">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5611">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5612">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5612">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-5613">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-5613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-5614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5614">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5615">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5616">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-5616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-5617">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-5618">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5619">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5620">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-5620">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-5621">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-5621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-5622">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-5623">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-5623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-5624">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-5624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-5625">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-5625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-5626">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-5626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-5627">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5628">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5629">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-5629">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5631">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5631">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5632">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5632">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5633">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-5633">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-5634">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5634">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-5635">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5635">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5636">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5636">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5637">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5637">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5638">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5638">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5640">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5640">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5642">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5642">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5644">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5644">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-5645">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5645">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="6e083-5646">DXGI_FORMAT_Y216<sup>V</sup> (109) </span><span class="sxs-lookup"><span data-stu-id="6e083-5646">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="6e083-5647">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5647">Target</span></span> | <span data-ttu-id="6e083-5648">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5648">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5649">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5649">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5650">32</span><span class="sxs-lookup"><span data-stu-id="6e083-5650">32</span></span> |
| <span data-ttu-id="6e083-5651">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5651">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5653">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5653">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5654">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5654">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5655">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5655">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5656">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5656">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5657">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5657">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5658">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5658">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5660">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5660">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-5661">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5661">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-5662">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5662">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-5663">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-5664">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5665">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5666">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5666">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5667">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5668">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5668">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-5669">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-5669">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-5670">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5670">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5671">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5671">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5672">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-5672">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-5673">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5673">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-5674">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5674">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5675">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5675">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5676">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-5676">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-5677">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-5677">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-5678">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5678">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-5679">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-5679">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-5680">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-5680">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-5681">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-5681">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-5682">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-5682">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-5683">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5683">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5684">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5684">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5685">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-5685">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5687">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5687">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5688">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5688">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5689">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-5689">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-5690">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5690">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-5691">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5691">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5692">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5692">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5693">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5693">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5694">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5694">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5696">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5696">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5698">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5698">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5700">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5700">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-5701">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="6e083-5702">DXGI_FORMAT_NV11<sup>V</sup> (110) </span><span class="sxs-lookup"><span data-stu-id="6e083-5702">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="6e083-5703">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5703">Target</span></span> | <span data-ttu-id="6e083-5704">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5704">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5705">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5706">8</span><span class="sxs-lookup"><span data-stu-id="6e083-5706">8</span></span> |
| <span data-ttu-id="6e083-5707">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5707">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5709">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5709">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5710">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5710">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5711">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5711">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5712">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5712">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5713">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5713">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5714">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5714">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5716">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5716">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-5717">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5717">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-5718">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5718">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-5719">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5719">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-5720">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5720">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5721">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5721">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5722">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5722">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5723">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5723">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5724">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5724">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-5725">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-5725">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-5726">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5726">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5727">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5727">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5728">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-5728">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-5729">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5729">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-5730">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5730">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5731">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5731">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5732">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-5732">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-5733">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-5733">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-5734">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5734">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-5735">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-5735">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-5736">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-5736">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-5737">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-5737">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-5738">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-5738">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-5739">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5739">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5740">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5740">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5741">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-5741">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5743">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5743">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5744">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5744">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5745">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-5745">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-5746">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5746">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-5747">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5747">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5748">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5748">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5749">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5749">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5750">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5750">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5752">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5752">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5754">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5754">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5756">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5756">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-5757">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5757">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="6e083-5758">DXGI_FORMAT_AI44<sup>V</sup> (111) </span><span class="sxs-lookup"><span data-stu-id="6e083-5758">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="6e083-5759">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5759">Target</span></span> | <span data-ttu-id="6e083-5760">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5760">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5761">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5761">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5762">8</span><span class="sxs-lookup"><span data-stu-id="6e083-5762">8</span></span> |
| <span data-ttu-id="6e083-5763">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5763">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5765">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5765">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5766">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5766">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5767">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5767">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5768">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5768">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5769">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5769">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5770">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5770">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5772">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5772">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-5773">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5773">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-5774">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5774">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-5775">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5775">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-5776">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5776">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5777">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5777">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5778">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5778">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5779">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5780">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5780">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-5781">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-5781">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-5782">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5782">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5783">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5783">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5784">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-5784">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-5785">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5785">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-5786">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5786">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5787">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5787">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5788">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-5788">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-5789">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-5789">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-5790">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5790">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-5791">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-5791">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-5792">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-5792">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-5793">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-5793">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-5794">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-5794">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-5795">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5795">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5796">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5796">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5797">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-5797">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5799">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5799">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5800">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5800">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5801">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-5801">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-5802">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5802">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-5803">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5803">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5804">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5804">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5805">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5805">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5806">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5806">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-5807">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5807">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5809">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5809">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-5810">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5810">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-5811">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="6e083-5812">DXGI_FORMAT_IA44<sup>V</sup> (112) </span><span class="sxs-lookup"><span data-stu-id="6e083-5812">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="6e083-5813">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5813">Target</span></span> | <span data-ttu-id="6e083-5814">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5814">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5815">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5816">8</span><span class="sxs-lookup"><span data-stu-id="6e083-5816">8</span></span> |
| <span data-ttu-id="6e083-5817">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5817">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5819">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5819">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5820">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5821">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5822">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5823">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5824">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5824">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5826">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5826">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-5827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5827">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-5828">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5828">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-5829">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5829">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-5830">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5830">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5831">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5831">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5832">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5832">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5833">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5833">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5834">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5834">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-5835">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-5835">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-5836">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5836">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5837">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5837">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5838">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-5838">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-5839">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5839">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-5840">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5840">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5841">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5841">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5842">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-5842">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-5843">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-5843">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-5844">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5844">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-5845">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-5845">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-5846">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-5846">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-5847">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-5847">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-5848">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-5848">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-5849">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5849">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5850">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5850">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5851">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-5851">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5853">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5853">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5854">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5854">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5855">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-5855">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-5856">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5856">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-5857">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5857">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5858">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5858">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5859">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5859">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5860">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5860">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-5861">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5861">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5863">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5863">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-5864">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5864">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-5865">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5865">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="6e083-5866">DXGI_FORMAT_P8<sup>V</sup> (113) </span><span class="sxs-lookup"><span data-stu-id="6e083-5866">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="6e083-5867">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5867">Target</span></span> | <span data-ttu-id="6e083-5868">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5868">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5869">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5869">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5870">8</span><span class="sxs-lookup"><span data-stu-id="6e083-5870">8</span></span> |
| <span data-ttu-id="6e083-5871">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5871">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5873">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5873">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5874">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5874">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5875">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5875">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5876">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5876">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5877">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5877">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5878">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5878">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5880">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5880">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-5881">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5881">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-5882">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5882">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-5883">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5883">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-5884">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5884">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5885">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5885">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5886">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5886">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5887">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5887">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5888">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5888">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-5889">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-5889">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-5890">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5890">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5891">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5891">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5892">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-5892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-5893">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-5894">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5895">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5896">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-5896">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-5897">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-5897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-5898">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-5899">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-5899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-5900">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-5900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-5901">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-5901">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-5902">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-5902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-5903">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5904">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5905">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-5905">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5907">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5907">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5908">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5908">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5909">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-5909">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-5910">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5910">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-5911">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5911">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5912">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5912">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5913">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5913">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5914">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5914">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-5915">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5915">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5917">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5917">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-5918">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5918">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-5919">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5919">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="6e083-5920">DXGI_FORMAT_A8P8<sup>V</sup> (114) </span><span class="sxs-lookup"><span data-stu-id="6e083-5920">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="6e083-5921">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5921">Target</span></span> | <span data-ttu-id="6e083-5922">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5922">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5923">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5923">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5924">16</span><span class="sxs-lookup"><span data-stu-id="6e083-5924">16</span></span> |
| <span data-ttu-id="6e083-5925">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5925">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-5927">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5927">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5928">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5928">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5929">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5929">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5930">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5930">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5931">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5931">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5932">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5932">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5934">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5934">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-5935">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5935">TextureCube</span></span> | \- |
| <span data-ttu-id="6e083-5936">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5936">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="6e083-5937">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5937">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="6e083-5938">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5938">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5939">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5939">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5940">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5940">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5941">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5941">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5942">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5942">Mipmap</span></span> | \- |
| <span data-ttu-id="6e083-5943">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-5943">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="6e083-5944">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5944">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5945">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5945">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5946">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-5946">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-5947">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5947">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-5948">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5948">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5949">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-5949">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-5950">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-5950">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-5951">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-5951">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-5952">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5952">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-5953">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-5953">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-5954">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-5954">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-5955">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-5955">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-5956">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-5956">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-5957">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5957">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5958">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-5958">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-5959">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-5959">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5961">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5961">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5962">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-5962">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-5963">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-5963">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-5964">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-5964">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-5965">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-5965">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-5966">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-5966">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-5967">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-5967">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-5968">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5968">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-5969">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-5969">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5971">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-5971">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-5972">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5972">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-5973">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-5973">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="6e083-5974">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115) </span><span class="sxs-lookup"><span data-stu-id="6e083-5974">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="6e083-5975">目標</span><span class="sxs-lookup"><span data-stu-id="6e083-5975">Target</span></span> | <span data-ttu-id="6e083-5976">支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5976">Support</span></span> |
| - | - |
| <span data-ttu-id="6e083-5977">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="6e083-5977">Bits Per Element (BPE)</span></span> | <span data-ttu-id="6e083-5978">16</span><span class="sxs-lookup"><span data-stu-id="6e083-5978">16</span></span> |
| <span data-ttu-id="6e083-5979">格式支援</span><span class="sxs-lookup"><span data-stu-id="6e083-5979">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5981">Buffer</span><span class="sxs-lookup"><span data-stu-id="6e083-5981">Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5982">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5982">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5983">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5983">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5984">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="6e083-5984">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="6e083-5985">Texture1D</span><span class="sxs-lookup"><span data-stu-id="6e083-5985">Texture1D</span></span> | \- |
| <span data-ttu-id="6e083-5986">Texture2D</span><span class="sxs-lookup"><span data-stu-id="6e083-5986">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5988">Texture3D</span><span class="sxs-lookup"><span data-stu-id="6e083-5988">Texture3D</span></span> | \- |
| <span data-ttu-id="6e083-5989">TextureCube</span><span class="sxs-lookup"><span data-stu-id="6e083-5989">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5991">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="6e083-5991">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5993">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5993">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-5995">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5995">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="6e083-5996">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="6e083-5996">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="6e083-5997">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="6e083-5997">Shader gather4</span></span> | \- |
| <span data-ttu-id="6e083-5998">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="6e083-5998">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="6e083-5999">Mipmap</span><span class="sxs-lookup"><span data-stu-id="6e083-5999">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-6001">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="6e083-6001">Mipmap Auto-Generation</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="6e083-6003">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-6003">RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-6004">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-6004">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-6005">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="6e083-6005">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="6e083-6006">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="6e083-6006">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="6e083-6007">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-6007">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-6008">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="6e083-6008">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="6e083-6009">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="6e083-6009">Typed UAV</span></span> | \- |
| <span data-ttu-id="6e083-6010">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="6e083-6010">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="6e083-6011">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="6e083-6011">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="6e083-6012">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="6e083-6012">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="6e083-6013">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="6e083-6013">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="6e083-6014">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="6e083-6014">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="6e083-6015">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="6e083-6015">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="6e083-6016">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-6016">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-6017">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="6e083-6017">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="6e083-6018">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="6e083-6018">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="6e083-6020">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-6020">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-6021">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="6e083-6021">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="6e083-6022">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="6e083-6022">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="6e083-6023">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="6e083-6023">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="6e083-6024">多級載入</span><span class="sxs-lookup"><span data-stu-id="6e083-6024">Multisample Load</span></span> | \- |
| <span data-ttu-id="6e083-6025">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="6e083-6025">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="6e083-6026">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="6e083-6026">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="6e083-6027">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="6e083-6027">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="6e083-6028">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="6e083-6028">Video Processor Input</span></span> | \- |
| <span data-ttu-id="6e083-6029">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="6e083-6029">Video Processor Output</span></span> | \- |
| <span data-ttu-id="6e083-6030">共用資源</span><span class="sxs-lookup"><span data-stu-id="6e083-6030">Shared Resource</span></span> | \- |
| <span data-ttu-id="6e083-6031">磚資源</span><span class="sxs-lookup"><span data-stu-id="6e083-6031">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="6e083-6032">格式化附注</span><span class="sxs-lookup"><span data-stu-id="6e083-6032">Format notes</span></span>

<span data-ttu-id="6e083-6033">格式的用途可從一個硬體功能層級變更為下一個硬體功能層級。</span><span class="sxs-lookup"><span data-stu-id="6e083-6033">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="6e083-6034"><sup>L</sup> ：無格式的格式</span><span class="sxs-lookup"><span data-stu-id="6e083-6034"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="6e083-6035"><sup>電腦</sup> ：部分類型、可轉換和簡單版面配置</span><span class="sxs-lookup"><span data-stu-id="6e083-6035"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="6e083-6036"><sup>FCS</sup> ：完整型別、可轉換和 simple 版面配置</span><span class="sxs-lookup"><span data-stu-id="6e083-6036"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="6e083-6037"><sup>FNS</sup> ：完全具類型、非可轉換和簡單版面配置</span><span class="sxs-lookup"><span data-stu-id="6e083-6037"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="6e083-6038"><sup>PCC</sup> ：部分類型、可轉換和複雜版面配置</span><span class="sxs-lookup"><span data-stu-id="6e083-6038"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="6e083-6039"><sup>FCC</sup> ：完整型別、可轉換和複雜的版面配置</span><span class="sxs-lookup"><span data-stu-id="6e083-6039"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="6e083-6040"><sup>FNC</sup> ：完整型別、非可轉換和複雜的版面配置</span><span class="sxs-lookup"><span data-stu-id="6e083-6040"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="6e083-6041"><sup>V</sup> ：影片格式</span><span class="sxs-lookup"><span data-stu-id="6e083-6041"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="6e083-6042">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e083-6042">Related topics</span></span>

[<span data-ttu-id="6e083-6043">D3D12 硬體功能等級</span><span class="sxs-lookup"><span data-stu-id="6e083-6043">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

<span data-ttu-id="6e083-6044">[針對 Direct3D 功能層級9執行陰影緩衝區](/previous-versions/windows/apps/jj262110(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="6e083-6044">[Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10))</span></span>

[<span data-ttu-id="6e083-6045">對應舊版格式</span><span class="sxs-lookup"><span data-stu-id="6e083-6045">Mapping Legacy Formats</span></span>](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[<span data-ttu-id="6e083-6046">DXGI 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="6e083-6046">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
