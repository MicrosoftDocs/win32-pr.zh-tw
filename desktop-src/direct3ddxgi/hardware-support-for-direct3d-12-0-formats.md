---
description: 本節指定 Direct3D 功能等級12.0 硬體支援的格式 ([ **DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)值) 。
ms.assetid: A039A82B-2E30-41A6-96B5-AD5538FE2285
title: Direct3D 功能層級 12.0 硬體的格式支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae4a33e54034d7fd3e8db1fb44046da9c9587fff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467929"
---
# <a name="format-support-for-direct3d-feature-level-120-hardware"></a><span data-ttu-id="4845f-103">Direct3D 功能層級 12.0 硬體的格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-103">Format support for Direct3D Feature Level 12.0 hardware</span></span>

<span data-ttu-id="4845f-104">此區段會指定 Direct3D 功能等級12.0 硬體支援的格式 ([ _\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)值) 。</span><span class="sxs-lookup"><span data-stu-id="4845f-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 12.0 hardware.</span></span>

<span data-ttu-id="4845f-105">下表摘要說明使用下列索引鍵的功能支援。</span><span class="sxs-lookup"><span data-stu-id="4845f-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="4845f-106">符號</span><span class="sxs-lookup"><span data-stu-id="4845f-106">Symbol</span></span>                            | <span data-ttu-id="4845f-107">描述</span><span class="sxs-lookup"><span data-stu-id="4845f-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="4845f-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="4845f-108">_ *-*\*</span></span>                             | <span data-ttu-id="4845f-109">不允許或無法使用。</span><span class="sxs-lookup"><span data-stu-id="4845f-109">Disallowed or not available.</span></span>                                                  |
| ![必要](images/letter-r.jpg)  | <span data-ttu-id="4845f-111">需要硬體支援。</span><span class="sxs-lookup"><span data-stu-id="4845f-111">Hardware support is required.</span></span>                                                 |
| ![選用](images/letter-o.jpg)  | <span data-ttu-id="4845f-113">硬體支援是選擇性的，格式可能或可能不會有硬體加速。</span><span class="sxs-lookup"><span data-stu-id="4845f-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![依賴](images/letter-d.jpg) | <span data-ttu-id="4845f-115">如果支援相關的選擇性功能，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="4845f-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="4845f-116">本主題包含每一種格式的區段。</span><span class="sxs-lookup"><span data-stu-id="4845f-116">This topic contains a section per format.</span></span> <span data-ttu-id="4845f-117">格式 *目標* (資料表每個目標各包含一個資料列) 可以是資源類型、HLSL 內建函式，或是相依于特定格式的特定功能。</span><span class="sxs-lookup"><span data-stu-id="4845f-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="4845f-118">若要以程式設計方式驗證 D3D11 和 D3D12 中的格式支援，請參閱 [檢查硬體功能支援](checking-hardware-feature-support.md)。</span><span class="sxs-lookup"><span data-stu-id="4845f-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="4845f-119">這些格式的數目大多是（但不是全部），以遞增的數值順序來 &mdash; 看，有些會超出數值順序，並與其他相關的格式一起列出。</span><span class="sxs-lookup"><span data-stu-id="4845f-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="4845f-120">另請注意 *，格式名稱的無* 型別可以表示 *部分* 具型別，而不是嚴格的無型別 (請參閱主題結尾的 [格式附注](#format-notes) 章節) 。</span><span class="sxs-lookup"><span data-stu-id="4845f-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="4845f-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0) </span><span class="sxs-lookup"><span data-stu-id="4845f-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="4845f-122">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-122">Target</span></span> | <span data-ttu-id="4845f-123">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-123">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-124">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-125">0</span><span class="sxs-lookup"><span data-stu-id="4845f-125">0</span></span> |
| <span data-ttu-id="4845f-126">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-126">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-128">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-128">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-130">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-131">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-132">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-133">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-134">Texture2D</span></span> | \- |
| <span data-ttu-id="4845f-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-135">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-136">TextureCube</span></span> | \- |
| <span data-ttu-id="4845f-137">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-137">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-138">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-139">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-139">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-140">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-140">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-141">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-142">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-142">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-143">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-143">Mipmap</span></span> | \- |
| <span data-ttu-id="4845f-144">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-146">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-147">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-148">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-149">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-150">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-150">Structured UAV and SRV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-152">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-152">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-153">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-153">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-154">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-154">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-155">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-155">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-156">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-156">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-157">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-157">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-158">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-158">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-159">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-159">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-160">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-160">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-161">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-161">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-163">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-163">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-164">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-164">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-165">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-165">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-166">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-166">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-167">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-167">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-168">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-168">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-169">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-169">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-170">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-170">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-171">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-171">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-172">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-172">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-173">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-173">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-174">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-174">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-175">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-175">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="4845f-177">DXGI_FORMAT_R32G32B32A32 無的 \_ <sup>電腦</sup> (1) </span><span class="sxs-lookup"><span data-stu-id="4845f-177">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="4845f-178">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-178">Target</span></span> | <span data-ttu-id="4845f-179">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-179">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-180">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-180">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-181">128</span><span class="sxs-lookup"><span data-stu-id="4845f-181">128</span></span> |
| <span data-ttu-id="4845f-182">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-182">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-184">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-184">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-185">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-185">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-186">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-186">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-187">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-187">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-188">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-188">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-190">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-190">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-192">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-192">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-194">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-194">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-196">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-196">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-197">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-197">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-198">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-198">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-199">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-199">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-200">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-200">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-201">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-201">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-202">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-202">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-204">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-204">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-205">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-205">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-206">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-206">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-207">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-207">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-208">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-208">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-209">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-209">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-210">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-210">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-211">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-211">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-212">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-212">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-213">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-213">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-214">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-214">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-215">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-215">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-216">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-216">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-217">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-217">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-218">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-218">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-219">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-219">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-220">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-220">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-222">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-223">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-224">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-225">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-226">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-226">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-227">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-228">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-228">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-230">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-230">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-231">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-231">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-232">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-232">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-233">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-233">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-235">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-235">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-236">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-236">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="4845f-238">DXGI_FORMAT_R32G32B32A32 \_ FLOAT<sup>FCS</sup> (2) </span><span class="sxs-lookup"><span data-stu-id="4845f-238">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="4845f-239">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-239">Target</span></span> | <span data-ttu-id="4845f-240">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-240">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-241">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-241">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-242">128</span><span class="sxs-lookup"><span data-stu-id="4845f-242">128</span></span> |
| <span data-ttu-id="4845f-243">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-243">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-245">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-245">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-247">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-247">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-249">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-249">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-250">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-250">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-252">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-252">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-254">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-254">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-256">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-256">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-258">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-258">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-260">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-260">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-262">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-262">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-264">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-264">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-265">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-265">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-266">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-266">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-268">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-268">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-269">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-269">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-271">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-271">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-273">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-273">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-275">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-275">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-277">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-277">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-278">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-278">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-279">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-279">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-280">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-280">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-281">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-281">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-283">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-283">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-285">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-285">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-287">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-287">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-288">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-288">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-289">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-289">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-290">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-290">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-291">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-291">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-292">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-292">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-293">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-293">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-295">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-295">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-297">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-297">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-299">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-299">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-301">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-301">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-303">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-303">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-305">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-305">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-306">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-306">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-308">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-308">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-309">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-309">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-310">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-310">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-311">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-311">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-313">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-313">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-314">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-314">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="4845f-316">DXGI_FORMAT_R32G32B32A32 \_ UINT<sup>FCS</sup> (3) </span><span class="sxs-lookup"><span data-stu-id="4845f-316">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="4845f-317">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-317">Target</span></span> | <span data-ttu-id="4845f-318">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-318">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-319">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-319">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-320">128</span><span class="sxs-lookup"><span data-stu-id="4845f-320">128</span></span> |
| <span data-ttu-id="4845f-321">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-321">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-323">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-323">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-325">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-325">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-327">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-327">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-328">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-328">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-330">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-330">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-332">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-332">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-334">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-334">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-336">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-336">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-338">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-338">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-340">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-340">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-341">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-341">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-342">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-342">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-343">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-343">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-344">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-344">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-345">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-345">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-347">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-347">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-348">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-348">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-350">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-350">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-351">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-351">Output Merger Logic Op</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-353">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-353">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-354">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-354">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-355">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-355">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-356">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-356">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-358">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-358">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-360">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-360">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-362">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-362">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-363">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-363">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-364">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-364">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-365">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-365">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-366">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-366">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-367">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-367">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-368">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-368">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-370">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-370">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-372">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-372">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-374">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-374">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-376">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-376">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-377">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-377">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-379">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-379">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-380">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-380">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-382">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-382">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-383">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-383">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-384">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-384">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-385">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-385">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-387">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-387">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-388">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-388">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="4845f-390">DXGI_FORMAT_R32G32B32A32 \_ 聖的<sup>FCS</sup> (4) </span><span class="sxs-lookup"><span data-stu-id="4845f-390">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="4845f-391">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-391">Target</span></span> | <span data-ttu-id="4845f-392">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-392">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-393">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-394">128</span><span class="sxs-lookup"><span data-stu-id="4845f-394">128</span></span> |
| <span data-ttu-id="4845f-395">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-395">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-397">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-397">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-399">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-399">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-401">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-402">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-402">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-404">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-404">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-406">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-406">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-408">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-408">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-410">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-410">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-412">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-412">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-414">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-414">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-415">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-415">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-416">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-416">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-417">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-417">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-418">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-418">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-419">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-419">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-421">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-421">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-422">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-424">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-424">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-425">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-425">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-426">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-426">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-427">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-427">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-428">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-428">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-429">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-429">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-431">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-431">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-433">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-433">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-435">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-435">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-436">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-436">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-437">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-437">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-438">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-438">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-439">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-439">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-440">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-440">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-441">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-441">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-443">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-443">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-445">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-445">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-447">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-447">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-449">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-449">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-450">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-450">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-452">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-452">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-453">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-453">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-455">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-455">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-456">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-456">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-457">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-457">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-458">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-458">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-460">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-460">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-461">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-461">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="4845f-463">DXGI_FORMAT_R32G32B32 無的 \_ <sup>電腦</sup> (5) </span><span class="sxs-lookup"><span data-stu-id="4845f-463">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="4845f-464">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-464">Target</span></span> | <span data-ttu-id="4845f-465">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-465">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-466">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-466">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-467">96</span><span class="sxs-lookup"><span data-stu-id="4845f-467">96</span></span> |
| <span data-ttu-id="4845f-468">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-468">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-470">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-470">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-471">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-471">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-472">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-472">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-473">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-473">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-474">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-474">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-476">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-476">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-478">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-478">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-480">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-480">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-482">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-482">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-483">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-483">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-484">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-484">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-485">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-485">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-486">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-486">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-487">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-487">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-488">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-488">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-490">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-490">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-491">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-491">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-492">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-492">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-493">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-493">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-494">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-494">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-495">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-495">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-496">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-496">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-497">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-497">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-498">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-498">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-499">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-499">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-500">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-500">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-501">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-501">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-502">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-502">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-503">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-503">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-504">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-504">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-505">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-505">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-506">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-506">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-508">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-508">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-509">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-509">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-510">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-510">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-511">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-511">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-512">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-512">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-513">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-513">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-514">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-514">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-516">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-516">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-517">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-517">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-518">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-518">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-519">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-519">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-520">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-520">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-521">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-521">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="4845f-522">DXGI_FORMAT_R32G32B32 \_ FLOAT<sup>FCS</sup> (6) </span><span class="sxs-lookup"><span data-stu-id="4845f-522">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="4845f-523">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-523">Target</span></span> | <span data-ttu-id="4845f-524">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-524">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-525">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-525">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-526">96</span><span class="sxs-lookup"><span data-stu-id="4845f-526">96</span></span> |
| <span data-ttu-id="4845f-527">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-527">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-529">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-529">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-531">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-531">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-533">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-533">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-534">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-534">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-536">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-536">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-538">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-538">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-540">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-540">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-542">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-542">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-544">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-544">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-546">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-546">Shader sample (any filter)</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-548">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-548">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-549">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-549">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-550">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-550">Shader gather4</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-552">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-552">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-553">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-553">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-555">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-555">Mipmap Auto-Generation</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-557">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-557">RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-559">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-559">Blendable RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="4845f-561">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-561">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-562">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-562">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-563">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-563">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-564">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-564">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-565">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-565">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-566">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-566">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-567">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-567">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-568">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-568">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-569">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-569">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-570">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-570">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-571">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-571">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-572">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-572">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-573">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-573">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-574">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-574">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-576">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-576">4x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="4845f-578">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-578">8x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="4845f-580">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-580">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-582">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-582">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-584">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-584">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-586">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-586">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-587">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-587">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-589">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-590">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-591">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-592">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-592">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-593">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-593">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-594">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="4845f-595">DXGI_FORMAT_R32G32B32 \_ UINT<sup>FCS</sup> (7) </span><span class="sxs-lookup"><span data-stu-id="4845f-595">DXGI_FORMAT_R32G32B32\_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="4845f-596">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-596">Target</span></span> | <span data-ttu-id="4845f-597">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-597">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-598">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-599">96</span><span class="sxs-lookup"><span data-stu-id="4845f-599">96</span></span> |
| <span data-ttu-id="4845f-600">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-600">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-602">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-602">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-604">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-604">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-606">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-606">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-607">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-607">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-609">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-609">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-611">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-611">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-613">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-613">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-615">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-615">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-617">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-617">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-619">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-619">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-620">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-620">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-621">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-621">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-622">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-622">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-623">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-623">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-624">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-624">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-626">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-626">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-627">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-627">RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-629">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-629">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-630">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-630">Output Merger Logic Op</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-632">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-632">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-633">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-633">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-634">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-634">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-635">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-635">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-636">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-636">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-637">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-637">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-638">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-638">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-639">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-639">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-640">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-640">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-641">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-641">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-642">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-642">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-643">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-643">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-644">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-644">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-646">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-646">4x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="4845f-648">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-648">8x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="4845f-650">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-650">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-652">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-653">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-653">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-655">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-655">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-656">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-656">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-658">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-658">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-659">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-659">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-660">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-660">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-661">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-661">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-662">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-662">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-663">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-663">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="4845f-664">DXGI_FORMAT_R32G32B32 \_ 聖的<sup>FCS</sup> (8) </span><span class="sxs-lookup"><span data-stu-id="4845f-664">DXGI_FORMAT_R32G32B32\_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="4845f-665">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-665">Target</span></span> | <span data-ttu-id="4845f-666">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-666">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-667">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-667">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-668">96</span><span class="sxs-lookup"><span data-stu-id="4845f-668">96</span></span> |
| <span data-ttu-id="4845f-669">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-669">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-671">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-671">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-673">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-673">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-675">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-675">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-676">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-676">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-678">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-678">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-680">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-680">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-682">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-682">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-684">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-684">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-686">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-686">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-688">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-688">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-689">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-689">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-690">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-690">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-691">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-691">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-692">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-692">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-693">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-693">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-695">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-695">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-696">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-696">RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-698">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-698">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-699">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-699">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-700">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-700">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-701">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-701">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-702">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-702">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-703">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-703">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-704">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-704">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-705">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-705">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-706">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-706">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-707">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-707">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-708">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-708">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-709">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-709">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-710">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-710">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-711">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-711">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-712">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-712">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-714">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-714">4x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="4845f-716">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-716">8x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="4845f-718">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-718">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-720">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-720">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-721">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-721">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-723">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-723">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-724">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-724">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-726">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-726">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-727">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-727">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-728">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-728">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-729">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-729">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-730">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-730">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-731">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-731">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="4845f-732">DXGI_FORMAT_R16G16B16A16 無別 \_ <sup>電腦</sup> (9) </span><span class="sxs-lookup"><span data-stu-id="4845f-732">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="4845f-733">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-733">Target</span></span> | <span data-ttu-id="4845f-734">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-734">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-735">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-735">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-736">64</span><span class="sxs-lookup"><span data-stu-id="4845f-736">64</span></span> |
| <span data-ttu-id="4845f-737">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-737">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-739">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-739">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-740">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-740">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-741">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-741">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-742">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-742">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-743">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-743">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-745">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-745">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-747">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-747">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-749">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-749">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-751">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-751">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-752">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-752">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-753">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-753">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-754">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-754">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-755">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-755">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-756">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-756">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-757">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-757">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-759">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-759">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-760">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-760">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-761">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-761">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-762">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-762">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-763">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-763">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-764">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-764">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-765">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-765">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-766">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-766">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-767">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-767">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-768">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-768">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-769">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-769">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-770">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-770">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-771">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-771">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-772">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-772">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-773">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-773">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-774">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-774">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-775">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-775">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-777">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-777">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-778">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-778">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-779">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-779">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-780">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-780">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-781">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-781">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-782">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-782">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-783">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-783">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-785">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-785">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-786">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-786">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-787">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-787">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-788">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-788">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-790">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-790">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-791">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-791">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="4845f-793">DXGI_FORMAT_R16G16B16A16 \_ FLOAT<sup>FCS</sup> (10) </span><span class="sxs-lookup"><span data-stu-id="4845f-793">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="4845f-794">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-794">Target</span></span> | <span data-ttu-id="4845f-795">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-795">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-796">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-796">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-797">64</span><span class="sxs-lookup"><span data-stu-id="4845f-797">64</span></span> |
| <span data-ttu-id="4845f-798">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-798">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-800">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-800">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-802">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-802">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-804">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-804">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-805">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-805">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-806">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-806">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-808">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-808">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-810">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-810">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-812">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-812">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-814">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-814">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-816">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-816">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-818">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-818">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-819">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-819">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-820">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-820">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-822">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-822">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-823">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-823">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-825">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-825">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-827">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-827">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-829">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-829">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-831">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-831">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-832">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-832">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-833">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-833">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-834">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-834">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-835">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-835">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-837">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-837">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-839">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-839">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-841">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-841">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-842">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-842">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-843">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-843">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-844">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-844">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-845">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-845">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-846">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-846">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-847">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-847">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-849">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-849">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-851">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-851">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-853">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-853">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-855">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-855">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-857">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-857">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-859">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-859">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-861">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-861">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-863">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-863">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-864">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-864">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-866">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-866">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-868">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-868">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-870">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-870">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-871">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-871">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="4845f-873">DXGI_FORMAT_R16G16B16A16 \_ UNORM 的<sup>FCS</sup> (11) </span><span class="sxs-lookup"><span data-stu-id="4845f-873">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="4845f-874">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-874">Target</span></span> | <span data-ttu-id="4845f-875">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-875">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-876">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-876">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-877">64</span><span class="sxs-lookup"><span data-stu-id="4845f-877">64</span></span> |
| <span data-ttu-id="4845f-878">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-878">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-880">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-880">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-882">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-882">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-884">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-884">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-885">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-885">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-886">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-886">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-888">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-888">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-890">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-890">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-892">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-894">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-894">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-896">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-896">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-898">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-898">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-899">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-899">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-900">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-900">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-902">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-902">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-903">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-903">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-905">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-905">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-907">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-907">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-909">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-909">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-911">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-912">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-913">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-914">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-915">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-915">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-917">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-917">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-919">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-919">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-921">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-921">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-922">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-922">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-923">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-923">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-924">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-924">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-925">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-925">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-926">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-926">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-927">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-927">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-929">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-929">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-931">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-931">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-933">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-933">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-935">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-935">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-937">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-937">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-939">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-939">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-940">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-940">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-942">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-942">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-943">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-943">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-944">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-944">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-945">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-945">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-947">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-947">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-948">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-948">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="4845f-950">DXGI_FORMAT_R16G16B16A16 \_ UINT<sup>FCS</sup> (12) </span><span class="sxs-lookup"><span data-stu-id="4845f-950">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="4845f-951">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-951">Target</span></span> | <span data-ttu-id="4845f-952">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-952">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-953">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-953">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-954">64</span><span class="sxs-lookup"><span data-stu-id="4845f-954">64</span></span> |
| <span data-ttu-id="4845f-955">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-955">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-957">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-957">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-959">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-959">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-961">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-961">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-962">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-962">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-963">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-963">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-965">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-965">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-967">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-967">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-969">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-969">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-971">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-971">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-973">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-973">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-974">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-974">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-975">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-975">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-976">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-976">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-977">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-977">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-978">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-978">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-980">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-980">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-981">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-981">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-983">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-983">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-984">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-984">Output Merger Logic Op</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-986">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-986">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-987">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-987">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-988">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-988">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-989">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-989">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-991">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-991">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-993">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-993">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-995">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-995">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-996">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-996">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-997">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-997">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-998">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-998">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-999">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-999">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1000">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-1000">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1001">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-1001">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1003">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1003">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1005">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1005">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1007">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-1007">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-1009">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-1009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-1010">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1010">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1012">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-1012">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-1013">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-1013">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1015">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1015">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-1016">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-1016">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-1017">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-1017">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-1018">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1018">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1020">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-1020">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-1021">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1021">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="4845f-1023">DXGI_FORMAT_R16G16B16A16 \_ SNORM 的<sup>FCS</sup> (13) </span><span class="sxs-lookup"><span data-stu-id="4845f-1023">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="4845f-1024">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1024">Target</span></span> | <span data-ttu-id="4845f-1025">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1025">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-1026">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-1026">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-1027">64</span><span class="sxs-lookup"><span data-stu-id="4845f-1027">64</span></span> |
| <span data-ttu-id="4845f-1028">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1028">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1030">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-1030">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1032">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1032">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1034">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1034">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1035">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1035">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1036">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-1036">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1038">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-1038">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1040">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-1040">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1042">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-1042">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1044">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-1044">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1046">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1046">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1048">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1048">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-1049">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1049">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-1050">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-1050">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1052">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-1052">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-1053">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-1053">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1055">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-1055">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1057">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1057">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1059">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1059">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1061">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-1061">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-1062">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1062">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-1063">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1063">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1064">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1064">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1065">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-1065">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1067">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-1067">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1069">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1069">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-1071">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-1071">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-1072">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-1072">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-1073">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-1073">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-1074">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-1074">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-1075">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-1075">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1076">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-1076">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1077">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-1077">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1079">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1079">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1081">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1081">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1083">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-1083">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-1085">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-1085">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1087">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1087">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1089">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-1089">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-1090">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-1090">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1092">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1092">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-1093">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-1093">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-1094">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-1094">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-1095">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1095">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1097">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-1097">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-1098">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1098">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="4845f-1100">DXGI_FORMAT_R16G16B16A16 \_ 聖的<sup>FCS</sup> (14) </span><span class="sxs-lookup"><span data-stu-id="4845f-1100">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="4845f-1101">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1101">Target</span></span> | <span data-ttu-id="4845f-1102">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1102">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-1103">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-1103">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-1104">64</span><span class="sxs-lookup"><span data-stu-id="4845f-1104">64</span></span> |
| <span data-ttu-id="4845f-1105">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1105">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1107">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-1107">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1109">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1109">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1111">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1111">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1112">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1112">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1113">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-1113">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1115">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-1115">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1117">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-1117">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1119">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-1119">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1121">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-1121">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1123">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1123">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-1124">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1124">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-1125">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1125">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-1126">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-1126">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-1127">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-1127">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-1128">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-1128">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1130">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-1130">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-1131">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1131">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1133">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1133">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1134">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-1134">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-1135">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1135">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-1136">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1136">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1137">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1137">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1138">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-1138">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1140">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-1140">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1142">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1142">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1144">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-1144">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-1145">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-1145">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-1146">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-1146">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-1147">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-1147">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-1148">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-1148">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1149">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-1149">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1150">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-1150">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1152">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1152">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1154">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1154">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1156">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-1156">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-1158">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-1158">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-1159">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1159">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1161">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-1161">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-1162">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-1162">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1164">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1164">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-1165">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-1165">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-1166">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-1166">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-1167">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1167">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1169">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-1169">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-1170">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1170">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="4845f-1172">DXGI_FORMAT_R32G32 無別 \_ <sup>電腦</sup> (15) </span><span class="sxs-lookup"><span data-stu-id="4845f-1172">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="4845f-1173">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1173">Target</span></span> | <span data-ttu-id="4845f-1174">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1174">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-1175">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-1175">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-1176">64</span><span class="sxs-lookup"><span data-stu-id="4845f-1176">64</span></span> |
| <span data-ttu-id="4845f-1177">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1177">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1179">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-1179">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1180">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1180">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1181">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1181">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1182">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1182">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1183">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-1183">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1185">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-1185">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1187">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-1187">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1189">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-1189">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1191">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-1191">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-1192">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1192">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-1193">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1193">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-1194">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1194">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-1195">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-1195">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-1196">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-1196">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-1197">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-1197">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1199">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-1199">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-1200">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1200">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1201">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1201">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1202">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-1202">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-1203">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1203">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-1204">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1204">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1205">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1205">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1206">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-1206">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-1207">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-1207">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-1208">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1208">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-1209">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-1209">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-1210">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-1210">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-1211">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-1211">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-1212">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-1212">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-1213">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-1213">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1214">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-1214">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1215">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-1215">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1217">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1217">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1218">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1218">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1219">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-1219">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-1220">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-1220">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-1221">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1221">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-1222">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-1222">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-1223">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-1223">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1225">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1225">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-1226">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-1226">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-1227">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-1227">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-1228">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1228">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-1229">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-1229">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-1230">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1230">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="4845f-1232">DXGI_FORMAT_R32G32 \_ FLOAT<sup>FCS</sup> (16) </span><span class="sxs-lookup"><span data-stu-id="4845f-1232">DXGI_FORMAT_R32G32\_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="4845f-1233">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1233">Target</span></span> | <span data-ttu-id="4845f-1234">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1234">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-1235">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-1235">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-1236">64</span><span class="sxs-lookup"><span data-stu-id="4845f-1236">64</span></span> |
| <span data-ttu-id="4845f-1237">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1237">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1239">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-1239">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1241">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1241">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1243">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1243">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1244">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1244">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1246">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-1246">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1248">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-1248">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1250">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-1250">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-1252">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1254">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-1254">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1256">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1256">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1258">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1258">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-1259">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1259">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-1260">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-1260">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1262">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-1262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-1263">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-1263">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1265">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-1265">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1267">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1267">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1269">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1269">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1271">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-1271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-1272">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-1273">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1274">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1275">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-1275">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1277">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-1277">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1279">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1279">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-1281">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-1281">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-1282">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-1282">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-1283">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-1283">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-1284">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-1284">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-1285">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-1285">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1286">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-1286">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1287">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-1287">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1289">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1289">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1291">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1291">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1293">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-1293">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-1295">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-1295">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1297">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1297">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1299">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-1299">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-1300">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-1300">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1302">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1302">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-1303">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-1303">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-1304">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-1304">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-1305">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1305">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-1306">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-1306">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-1307">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1307">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="4845f-1309">DXGI_FORMAT_R32G32 \_ UINT<sup>FCS</sup> (17) </span><span class="sxs-lookup"><span data-stu-id="4845f-1309">DXGI_FORMAT_R32G32\_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="4845f-1310">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1310">Target</span></span> | <span data-ttu-id="4845f-1311">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1311">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-1312">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-1312">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-1313">64</span><span class="sxs-lookup"><span data-stu-id="4845f-1313">64</span></span> |
| <span data-ttu-id="4845f-1314">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1314">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1316">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-1316">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1318">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1318">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1320">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1321">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1321">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1323">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-1323">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1325">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-1325">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1327">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-1327">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1329">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-1329">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1331">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-1331">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1333">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1333">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-1334">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1334">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-1335">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1335">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-1336">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-1336">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-1337">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-1337">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-1338">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-1338">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1340">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-1340">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-1341">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1341">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1343">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1343">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1344">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-1344">Output Merger Logic Op</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1346">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1346">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-1347">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1347">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1348">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1348">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1349">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-1349">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1351">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-1351">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1353">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1353">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-1355">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-1355">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-1356">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-1356">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-1357">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-1357">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-1358">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-1358">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-1359">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-1359">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1360">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-1360">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1361">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-1361">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1363">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1363">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1365">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1365">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1367">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-1367">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-1369">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-1369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-1370">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1370">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1372">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-1372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-1373">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-1373">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1375">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1375">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-1376">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-1376">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-1377">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-1377">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-1378">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1378">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-1379">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-1379">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-1380">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1380">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="4845f-1382">DXGI_FORMAT_R32G32 \_ 聖的<sup>FCS</sup> (18) </span><span class="sxs-lookup"><span data-stu-id="4845f-1382">DXGI_FORMAT_R32G32\_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="4845f-1383">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1383">Target</span></span> | <span data-ttu-id="4845f-1384">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1384">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-1385">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-1385">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-1386">64</span><span class="sxs-lookup"><span data-stu-id="4845f-1386">64</span></span> |
| <span data-ttu-id="4845f-1387">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1387">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1389">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-1389">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1391">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1391">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1393">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1393">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1394">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1394">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1396">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-1396">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1398">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-1398">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1400">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-1400">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1402">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-1402">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1404">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-1404">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1406">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1406">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-1407">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1407">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-1408">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1408">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-1409">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-1409">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-1410">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-1410">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-1411">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-1411">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1413">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-1413">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-1414">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1414">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1416">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1416">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1417">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-1417">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-1418">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1418">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-1419">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1419">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1420">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1420">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1421">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-1421">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1423">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-1423">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1425">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1425">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-1427">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-1427">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-1428">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-1428">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-1429">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-1429">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-1430">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-1430">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-1431">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-1431">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1432">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-1432">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1433">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-1433">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1435">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1435">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1437">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1437">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1439">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-1439">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-1441">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-1441">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-1442">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1442">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1444">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-1444">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-1445">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-1445">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1447">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1447">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-1448">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-1448">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-1449">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-1449">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-1450">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1450">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-1451">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-1451">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-1452">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1452">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r32g8x24_typeless-19"></a><span data-ttu-id="4845f-1454">DXGI_FORMAT_R32G8X24 不 \_ (19) </span><span class="sxs-lookup"><span data-stu-id="4845f-1454">DXGI_FORMAT_R32G8X24\_TYPELESS (19)</span></span>
| <span data-ttu-id="4845f-1455">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1455">Target</span></span> | <span data-ttu-id="4845f-1456">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1456">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-1457">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-1457">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-1458">64</span><span class="sxs-lookup"><span data-stu-id="4845f-1458">64</span></span> |
| <span data-ttu-id="4845f-1459">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1459">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1461">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-1461">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1462">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1462">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1463">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1463">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1464">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1464">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1465">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-1465">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1467">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-1467">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1469">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-1469">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-1470">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-1470">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1472">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-1472">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-1473">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1473">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-1474">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1474">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-1475">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1475">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-1476">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-1476">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-1477">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-1477">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-1478">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-1478">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1480">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-1480">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-1481">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1481">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1482">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1482">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1483">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-1483">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-1484">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1484">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-1485">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1485">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1486">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1486">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1487">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-1487">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-1488">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-1488">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-1489">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1489">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-1490">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-1490">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-1491">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-1491">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-1492">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-1492">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-1493">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-1493">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-1494">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-1494">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1495">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-1495">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1496">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-1496">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1498">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1498">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1499">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1499">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1500">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-1500">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-1501">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-1501">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-1502">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1502">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-1503">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-1503">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-1504">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-1504">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1506">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1506">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-1507">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-1507">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-1508">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-1508">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-1509">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1509">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-1510">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-1510">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-1511">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1511">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uint-20"></a><span data-ttu-id="4845f-1512">DXGI_FORMAT_D32 \_ FLOAT \_ S8X24 \_ UINT (20) </span><span class="sxs-lookup"><span data-stu-id="4845f-1512">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT (20)</span></span>
| <span data-ttu-id="4845f-1513">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1513">Target</span></span> | <span data-ttu-id="4845f-1514">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1514">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-1515">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-1515">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-1516">64</span><span class="sxs-lookup"><span data-stu-id="4845f-1516">64</span></span> |
| <span data-ttu-id="4845f-1517">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1517">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1519">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-1519">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1520">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1520">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1521">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1521">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1522">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1522">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1523">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-1523">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1525">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-1525">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1527">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-1527">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-1528">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-1528">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1530">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-1530">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-1531">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1531">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-1532">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1532">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-1533">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1533">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-1534">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-1534">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-1535">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-1535">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-1536">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-1536">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1538">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-1538">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-1539">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1539">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1540">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1540">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1541">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-1541">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-1542">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1542">Depth/Stencil Target</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1544">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1544">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1545">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1545">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1546">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-1546">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-1547">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-1547">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-1548">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1548">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-1549">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-1549">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-1550">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-1550">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-1551">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-1551">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-1552">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-1552">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-1553">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-1553">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1554">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-1554">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1555">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-1555">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1557">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1557">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1559">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1559">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1561">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-1561">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-1563">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-1563">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-1564">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1564">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-1565">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-1565">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-1566">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-1566">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1568">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1568">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-1569">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-1569">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-1570">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-1570">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-1571">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1571">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-1572">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-1572">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-1573">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1573">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typeless-21"></a><span data-ttu-id="4845f-1574">DXGI_FORMAT_R32 \_ FLOAT X8X24 無型別 \_ \_ (21) </span><span class="sxs-lookup"><span data-stu-id="4845f-1574">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS (21)</span></span>
| <span data-ttu-id="4845f-1575">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1575">Target</span></span> | <span data-ttu-id="4845f-1576">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1576">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-1577">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-1577">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-1578">64</span><span class="sxs-lookup"><span data-stu-id="4845f-1578">64</span></span> |
| <span data-ttu-id="4845f-1579">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1579">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1581">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-1581">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1582">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1582">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1583">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1583">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1584">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1584">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-1585">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-1587">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-1589">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-1590">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-1590">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1592">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-1592">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1594">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1594">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1596">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1596">Shader sample\_c (comparison filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1598">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1598">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-1599">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-1599">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1601">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-1601">Shader gather4\_c</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1603">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-1603">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1605">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-1605">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-1606">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1606">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1607">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1607">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1608">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-1608">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-1609">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1609">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-1610">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1610">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1611">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1611">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1612">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-1612">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-1613">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-1613">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-1614">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1614">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-1615">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-1615">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-1616">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-1616">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-1617">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-1617">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-1618">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-1618">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-1619">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-1619">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1620">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-1620">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1621">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-1621">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1623">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1623">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1624">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1624">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1625">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-1625">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-1626">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-1626">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-1627">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1627">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1629">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-1629">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-1630">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-1630">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1632">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1632">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-1633">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-1633">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-1634">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-1634">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-1635">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1635">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-1636">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-1636">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-1637">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1637">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uint-22"></a><span data-ttu-id="4845f-1638">DXGI_FORMAT_X32 無別 \_ \_ G8X24 \_ UINT (22) </span><span class="sxs-lookup"><span data-stu-id="4845f-1638">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT (22)</span></span>
| <span data-ttu-id="4845f-1639">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1639">Target</span></span> | <span data-ttu-id="4845f-1640">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1640">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-1641">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-1641">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-1642">64</span><span class="sxs-lookup"><span data-stu-id="4845f-1642">64</span></span> |
| <span data-ttu-id="4845f-1643">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1643">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1645">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-1645">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1646">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1646">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1647">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1647">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1648">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1648">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1649">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-1649">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1651">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-1651">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1653">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-1653">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-1654">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-1654">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1656">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-1656">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1658">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1658">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-1659">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1659">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-1660">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1660">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-1661">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-1661">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-1662">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-1662">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-1663">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-1663">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1665">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-1665">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-1666">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1666">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1667">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1667">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1668">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-1668">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-1669">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1669">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-1670">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1670">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1671">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1671">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1672">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-1672">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-1673">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-1673">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-1674">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1674">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-1675">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-1675">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-1676">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-1676">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-1677">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-1677">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-1678">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-1678">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-1679">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-1679">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1680">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-1680">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1681">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-1681">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1683">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1683">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1684">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1684">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1685">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-1685">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-1686">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-1686">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-1687">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1687">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1689">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-1689">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-1690">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-1690">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1692">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1692">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-1693">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-1693">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-1694">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-1694">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-1695">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1695">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-1696">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-1696">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-1697">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1697">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="4845f-1698">DXGI_FORMAT_R10G10B10A2 無別 \_ <sup>電腦</sup> (23) </span><span class="sxs-lookup"><span data-stu-id="4845f-1698">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="4845f-1699">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1699">Target</span></span> | <span data-ttu-id="4845f-1700">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1700">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-1701">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-1701">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-1702">32</span><span class="sxs-lookup"><span data-stu-id="4845f-1702">32</span></span> |
| <span data-ttu-id="4845f-1703">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1703">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1705">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-1705">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1706">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1706">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1707">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1707">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1708">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1708">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1709">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-1709">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1711">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-1711">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1713">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-1713">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1715">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-1715">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1717">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-1717">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-1718">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1718">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-1719">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1719">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-1720">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1720">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-1721">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-1721">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-1722">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-1722">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-1723">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-1723">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1725">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-1725">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-1726">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1726">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1727">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1727">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1728">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-1728">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-1729">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1729">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-1730">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1730">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1731">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1731">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1732">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-1732">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-1733">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-1733">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-1734">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1734">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-1735">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-1735">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-1736">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-1736">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-1737">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-1737">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-1738">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-1738">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-1739">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-1739">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1740">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-1740">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1741">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-1741">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1743">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1743">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1744">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1744">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1745">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-1745">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-1746">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-1746">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-1747">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1747">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-1748">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-1748">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-1749">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-1749">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1751">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1751">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-1752">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-1752">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-1753">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-1753">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-1754">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1754">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1756">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-1756">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-1757">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1757">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="4845f-1759">DXGI_FORMAT_R10G10B10A2 \_ UNORM 的<sup>FCS</sup> (24) </span><span class="sxs-lookup"><span data-stu-id="4845f-1759">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="4845f-1760">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1760">Target</span></span> | <span data-ttu-id="4845f-1761">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1761">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-1762">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-1762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-1763">32</span><span class="sxs-lookup"><span data-stu-id="4845f-1763">32</span></span> |
| <span data-ttu-id="4845f-1764">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1764">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1766">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-1766">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1768">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1768">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1770">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1770">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1771">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1771">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1772">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-1772">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1774">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-1774">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1776">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-1776">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1778">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-1778">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1780">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-1780">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1782">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1782">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1784">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1784">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-1785">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1785">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-1786">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-1786">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1788">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-1788">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-1789">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-1789">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1791">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-1791">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1793">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1793">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1795">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1795">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1797">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-1797">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-1798">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1798">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-1799">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1799">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1800">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1800">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1801">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-1801">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1803">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-1803">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1805">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1805">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-1807">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-1807">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-1808">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-1808">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-1809">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-1809">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-1810">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-1810">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-1811">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-1811">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1812">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-1812">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1813">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-1813">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1815">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1815">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1817">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1817">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1819">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-1819">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-1821">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-1821">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1823">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1823">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1825">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-1825">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1827">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-1827">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1829">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1829">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-1830">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-1830">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-1832">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-1832">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1834">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1834">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1836">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-1836">BackBuffer Castable Even Fully Typed</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1838">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1838">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="4845f-1840">DXGI_FORMAT_R10G10B10A2 \_ UINT<sup>FCS</sup> (25) </span><span class="sxs-lookup"><span data-stu-id="4845f-1840">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="4845f-1841">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1841">Target</span></span> | <span data-ttu-id="4845f-1842">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1842">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-1843">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-1843">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-1844">32</span><span class="sxs-lookup"><span data-stu-id="4845f-1844">32</span></span> |
| <span data-ttu-id="4845f-1845">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1845">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1847">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-1847">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1849">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1849">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1851">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1851">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1852">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1852">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1853">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-1853">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1855">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-1855">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1857">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-1857">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1859">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-1859">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1861">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-1861">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1863">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1863">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-1864">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1864">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-1865">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1865">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-1866">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-1866">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-1867">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-1867">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-1868">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-1868">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1870">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-1870">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-1871">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1871">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1873">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1873">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1874">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-1874">Output Merger Logic Op</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1876">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1876">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-1877">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1877">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1878">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1878">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1879">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-1879">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1881">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-1881">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1883">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1883">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-1885">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-1885">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-1886">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-1886">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-1887">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-1887">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-1888">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-1888">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-1889">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-1889">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1890">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-1890">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1891">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-1891">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1893">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1893">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1895">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1895">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1897">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-1897">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-1899">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-1899">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-1900">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1900">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1902">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-1902">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-1903">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-1903">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1905">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1905">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-1906">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-1906">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-1907">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-1907">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-1908">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1908">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1910">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-1910">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-1911">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1911">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="4845f-1913">DXGI_FORMAT_R10G10B10 \_ XR \_ 偏差 \_ A2 \_ UNORM<sup>FCS</sup> (89) </span><span class="sxs-lookup"><span data-stu-id="4845f-1913">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="4845f-1914">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1914">Target</span></span> | <span data-ttu-id="4845f-1915">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1915">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-1916">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-1916">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-1917">32</span><span class="sxs-lookup"><span data-stu-id="4845f-1917">32</span></span> |
| <span data-ttu-id="4845f-1918">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1918">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1920">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-1920">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1921">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1921">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1922">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1922">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1923">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1923">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1924">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-1924">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-1925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-1925">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-1927">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-1928">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-1928">TextureCube</span></span> | \- |
| <span data-ttu-id="4845f-1929">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-1929">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-1930">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1930">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-1931">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1931">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-1932">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1932">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-1933">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-1933">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-1934">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-1934">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-1935">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-1935">Mipmap</span></span> | \- |
| <span data-ttu-id="4845f-1936">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-1936">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-1937">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1937">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1938">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1938">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1939">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-1939">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-1940">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1940">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-1941">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1941">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1942">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-1942">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-1943">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-1943">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-1944">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-1944">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-1945">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1945">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-1946">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-1946">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-1947">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-1947">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-1948">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-1948">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-1949">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-1949">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-1950">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-1950">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1951">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-1951">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-1952">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-1952">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1954">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1954">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1955">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-1955">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-1956">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-1956">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-1957">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-1957">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-1958">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-1958">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-1959">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-1959">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1961">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-1961">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1963">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1963">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-1964">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-1964">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-1966">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-1966">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1968">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1968">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1970">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-1970">BackBuffer Castable Even Fully Typed</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1972">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-1972">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="4845f-1974">DXGI_FORMAT_R11G11B10 \_ FLOAT<sup>FNS</sup> (26) </span><span class="sxs-lookup"><span data-stu-id="4845f-1974">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="4845f-1975">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-1975">Target</span></span> | <span data-ttu-id="4845f-1976">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1976">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-1977">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-1977">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-1978">32</span><span class="sxs-lookup"><span data-stu-id="4845f-1978">32</span></span> |
| <span data-ttu-id="4845f-1979">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-1979">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1981">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-1981">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1983">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1983">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1985">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1985">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1986">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-1986">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-1987">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-1987">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1989">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-1989">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1991">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-1991">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1993">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-1993">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1995">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-1995">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1997">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1997">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-1999">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-1999">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-2000">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2000">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-2001">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-2001">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2003">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-2003">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-2004">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-2004">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2006">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-2006">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2008">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2008">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2010">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2010">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2012">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-2012">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-2013">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2013">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-2014">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2015">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2016">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-2016">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2018">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-2018">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2020">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2020">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2022">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-2022">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-2023">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-2023">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-2024">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-2024">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-2025">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-2025">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-2026">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-2026">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2027">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-2027">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2028">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-2028">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2030">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2030">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2032">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2032">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2034">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-2034">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2036">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-2036">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2038">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2038">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2040">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-2040">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-2041">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-2041">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-2042">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2042">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-2043">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-2043">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-2044">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-2044">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-2045">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2045">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-2046">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-2046">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-2047">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2047">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="4845f-2049">DXGI_FORMAT_R8G8B8A8 無別 \_ <sup>電腦</sup> (27) </span><span class="sxs-lookup"><span data-stu-id="4845f-2049">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="4845f-2050">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2050">Target</span></span> | <span data-ttu-id="4845f-2051">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2051">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-2052">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-2052">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-2053">32</span><span class="sxs-lookup"><span data-stu-id="4845f-2053">32</span></span> |
| <span data-ttu-id="4845f-2054">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2054">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2056">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-2056">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2057">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2057">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2058">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2058">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2059">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2059">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2060">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-2060">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2062">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-2062">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2064">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-2064">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2066">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-2066">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2068">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-2068">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-2069">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2069">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-2070">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2070">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-2071">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2071">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-2072">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-2072">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-2073">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-2073">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-2074">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-2074">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2076">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-2076">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-2077">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2077">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-2078">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2078">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-2079">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-2079">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-2080">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2080">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-2081">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2081">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2082">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2082">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2083">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-2083">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-2084">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-2084">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-2085">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2085">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-2086">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-2086">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-2087">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-2087">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-2088">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-2088">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-2089">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-2089">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-2090">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-2090">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2091">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-2091">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2092">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-2092">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2094">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2094">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-2095">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2095">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-2096">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-2096">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-2097">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-2097">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-2098">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2098">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-2099">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-2099">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-2100">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-2100">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2102">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2102">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-2103">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-2103">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-2104">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-2104">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-2105">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2105">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2107">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-2107">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-2108">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2108">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="4845f-2110">DXGI_FORMAT_R8G8B8A8 \_ UNORM 的<sup>FCS</sup> (28) </span><span class="sxs-lookup"><span data-stu-id="4845f-2110">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="4845f-2111">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2111">Target</span></span> | <span data-ttu-id="4845f-2112">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2112">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-2113">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-2113">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-2114">32</span><span class="sxs-lookup"><span data-stu-id="4845f-2114">32</span></span> |
| <span data-ttu-id="4845f-2115">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2115">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2117">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-2117">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2119">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2119">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2121">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2121">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2122">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2122">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2123">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-2123">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2125">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-2125">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2127">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-2127">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2129">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-2129">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2131">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-2131">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2133">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2133">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2135">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2135">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-2136">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2136">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-2137">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-2137">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2139">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-2139">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-2140">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-2140">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2142">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-2142">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2144">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2144">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2146">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2146">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2148">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-2148">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-2149">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2149">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-2150">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2150">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2151">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2151">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2152">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-2152">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2154">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-2154">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2156">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2156">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2158">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-2158">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-2159">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-2159">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-2160">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-2160">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-2161">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-2161">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-2162">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-2162">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2163">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-2163">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2164">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-2164">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2166">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2166">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2168">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2168">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2170">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-2170">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2172">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-2172">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2174">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2174">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2176">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-2176">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2178">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-2178">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2180">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2180">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-2181">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-2181">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2183">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-2183">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2185">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2185">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2187">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-2187">BackBuffer Castable Even Fully Typed</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2189">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2189">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="4845f-2191">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ SRGB<sup>FCS</sup> (29) </span><span class="sxs-lookup"><span data-stu-id="4845f-2191">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="4845f-2192">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2192">Target</span></span> | <span data-ttu-id="4845f-2193">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2193">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-2194">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-2194">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-2195">32</span><span class="sxs-lookup"><span data-stu-id="4845f-2195">32</span></span> |
| <span data-ttu-id="4845f-2196">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2196">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2198">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-2198">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2199">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2199">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2200">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2200">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2201">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2201">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2202">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-2202">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2204">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-2204">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2206">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-2206">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2208">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-2208">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2210">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-2210">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2212">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2212">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2214">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2214">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-2215">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2215">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-2216">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-2216">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2218">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-2218">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-2219">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-2219">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2221">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-2221">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2223">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2223">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2225">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2225">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2227">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-2227">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-2228">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2228">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-2229">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2229">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2230">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2230">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2231">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-2231">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-2232">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-2232">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-2233">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2233">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-2234">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-2234">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-2235">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-2235">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-2236">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-2236">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-2237">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-2237">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-2238">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-2238">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2239">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-2239">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2240">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-2240">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2242">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2242">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2244">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2244">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2246">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-2246">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2248">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-2248">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2250">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2250">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2252">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-2252">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2254">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-2254">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2256">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2256">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-2257">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-2257">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2259">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-2259">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2261">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2261">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2263">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-2263">BackBuffer Castable Even Fully Typed</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2265">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2265">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="4845f-2267">DXGI_FORMAT_R8G8B8A8 \_ UINT<sup>FCS</sup> (30) </span><span class="sxs-lookup"><span data-stu-id="4845f-2267">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="4845f-2268">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2268">Target</span></span> | <span data-ttu-id="4845f-2269">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2269">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-2270">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-2270">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-2271">32</span><span class="sxs-lookup"><span data-stu-id="4845f-2271">32</span></span> |
| <span data-ttu-id="4845f-2272">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2272">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2274">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-2274">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2276">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2276">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2278">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2278">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2279">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2279">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2280">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-2280">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2282">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-2282">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2284">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-2284">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2286">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-2286">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2288">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-2288">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2290">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2290">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-2291">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2291">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-2292">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2292">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-2293">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-2293">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-2294">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-2294">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-2295">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-2295">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2297">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-2297">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-2298">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2298">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2300">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2300">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-2301">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-2301">Output Merger Logic Op</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2303">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-2304">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2305">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2306">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-2306">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2308">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-2308">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2310">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2310">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2312">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-2312">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-2313">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-2313">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-2314">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-2314">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-2315">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-2315">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-2316">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-2316">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2317">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-2317">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2318">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-2318">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2320">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2320">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2322">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2322">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2324">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-2324">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2326">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-2326">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-2327">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2327">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2329">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-2329">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-2330">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-2330">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2332">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2332">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-2333">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-2333">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-2334">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-2334">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-2335">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2335">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2337">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-2337">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-2338">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2338">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="4845f-2340">DXGI_FORMAT_R8G8B8A8 \_ SNORM 的<sup>FCS</sup> (31) </span><span class="sxs-lookup"><span data-stu-id="4845f-2340">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="4845f-2341">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2341">Target</span></span> | <span data-ttu-id="4845f-2342">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2342">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-2343">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-2343">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-2344">32</span><span class="sxs-lookup"><span data-stu-id="4845f-2344">32</span></span> |
| <span data-ttu-id="4845f-2345">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2345">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2347">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-2347">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2349">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2349">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2351">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2351">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2352">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2352">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2353">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-2353">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2355">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-2355">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2357">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-2357">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2359">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-2359">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2361">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-2361">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2363">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2363">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2365">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2365">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-2366">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2366">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-2367">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-2367">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2369">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-2369">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-2370">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-2370">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2372">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-2372">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2374">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2374">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2376">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2376">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2378">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-2378">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-2379">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2379">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-2380">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2380">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2381">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2381">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2382">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-2382">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2384">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-2384">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2386">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2386">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2388">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-2388">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-2389">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-2389">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-2390">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-2390">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-2391">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-2391">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-2392">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-2392">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2393">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-2393">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2394">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-2394">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2396">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2396">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2398">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2398">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2400">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-2400">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2402">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-2402">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2404">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2404">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2406">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-2406">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-2407">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-2407">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2409">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2409">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-2410">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-2410">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-2411">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-2411">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-2412">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2412">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2414">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-2414">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-2415">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2415">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="4845f-2417">DXGI_FORMAT_R8G8B8A8 \_ 聖的<sup>FCS</sup> (32) </span><span class="sxs-lookup"><span data-stu-id="4845f-2417">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="4845f-2418">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2418">Target</span></span> | <span data-ttu-id="4845f-2419">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2419">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-2420">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-2420">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-2421">32</span><span class="sxs-lookup"><span data-stu-id="4845f-2421">32</span></span> |
| <span data-ttu-id="4845f-2422">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2422">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2424">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-2424">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2426">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2426">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2428">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2428">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2429">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2429">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2430">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-2430">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2432">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-2432">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2434">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-2434">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2436">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-2436">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2438">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-2438">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2440">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-2441">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-2442">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2442">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-2443">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-2443">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-2444">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-2444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-2445">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-2445">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2447">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-2447">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-2448">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2448">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2450">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2450">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-2451">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-2451">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-2452">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2452">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-2453">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2453">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2454">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2454">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2455">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-2455">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2457">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-2457">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2459">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2459">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2461">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-2461">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-2462">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-2462">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-2463">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-2463">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-2464">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-2464">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-2465">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-2465">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2466">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-2466">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2467">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-2467">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2469">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2469">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2471">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2471">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2473">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-2473">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2475">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-2475">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-2476">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2476">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2478">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-2478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-2479">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-2479">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2481">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-2482">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-2482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-2483">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-2483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-2484">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2484">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2486">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-2486">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-2487">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2487">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="4845f-2489">DXGI_FORMAT_R16G16 無的 \_ <sup>電腦</sup> (33) </span><span class="sxs-lookup"><span data-stu-id="4845f-2489">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="4845f-2490">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2490">Target</span></span> | <span data-ttu-id="4845f-2491">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2491">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-2492">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-2492">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-2493">32</span><span class="sxs-lookup"><span data-stu-id="4845f-2493">32</span></span> |
| <span data-ttu-id="4845f-2494">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2494">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2496">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-2496">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2497">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2498">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2499">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-2500">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2502">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-2502">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-2504">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2506">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-2506">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2508">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-2508">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-2509">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2509">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-2510">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2510">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-2511">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2511">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-2512">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-2512">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-2513">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-2513">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-2514">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-2514">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2516">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-2516">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-2517">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2517">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-2518">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2518">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-2519">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-2519">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-2520">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2520">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-2521">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2521">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2522">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2522">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2523">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-2523">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-2524">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-2524">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-2525">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2525">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-2526">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-2526">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-2527">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-2527">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-2528">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-2528">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-2529">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-2529">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-2530">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-2530">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2531">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-2531">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2532">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-2532">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2534">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2534">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-2535">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2535">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-2536">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-2536">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-2537">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-2537">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-2538">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2538">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-2539">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-2539">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-2540">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-2540">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2542">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2542">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-2543">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-2543">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-2544">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-2544">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-2545">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2545">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-2546">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-2546">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-2547">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2547">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="4845f-2549">DXGI_FORMAT_R16G16 \_ FLOAT<sup>FCS</sup> (34) </span><span class="sxs-lookup"><span data-stu-id="4845f-2549">DXGI_FORMAT_R16G16\_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="4845f-2550">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2550">Target</span></span> | <span data-ttu-id="4845f-2551">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2551">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-2552">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-2552">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-2553">32</span><span class="sxs-lookup"><span data-stu-id="4845f-2553">32</span></span> |
| <span data-ttu-id="4845f-2554">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2554">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2556">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-2556">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2558">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2558">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2560">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2560">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2561">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2561">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2562">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-2562">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2564">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-2564">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2566">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-2566">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2568">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-2568">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2570">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-2570">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2572">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2572">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2574">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2574">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-2575">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2575">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-2576">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-2576">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2578">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-2578">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-2579">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-2579">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2581">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-2581">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2583">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2583">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2585">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2585">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2587">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-2587">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-2588">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2588">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-2589">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2589">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2590">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2590">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2591">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-2591">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2593">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-2593">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2595">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2595">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2597">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-2597">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-2598">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-2598">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-2599">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-2599">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-2600">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-2600">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-2601">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-2601">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2602">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-2602">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2603">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-2603">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2605">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2605">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2607">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2607">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2609">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-2609">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2611">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-2611">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2613">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2613">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2615">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-2615">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-2616">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-2616">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2618">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2618">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-2619">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-2619">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-2620">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-2620">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-2621">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2621">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-2622">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-2622">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-2623">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2623">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="4845f-2625">DXGI_FORMAT_R16G16 \_ UNORM 的<sup>FCS</sup> (35) </span><span class="sxs-lookup"><span data-stu-id="4845f-2625">DXGI_FORMAT_R16G16\_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="4845f-2626">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2626">Target</span></span> | <span data-ttu-id="4845f-2627">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2627">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-2628">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-2628">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-2629">32</span><span class="sxs-lookup"><span data-stu-id="4845f-2629">32</span></span> |
| <span data-ttu-id="4845f-2630">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2630">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2632">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-2632">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2634">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2634">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2636">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2636">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2637">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2637">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2638">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-2638">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2640">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-2640">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2642">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-2642">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2644">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-2644">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2646">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-2646">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2648">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2648">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2650">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2650">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-2651">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2651">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-2652">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-2652">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2654">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-2654">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-2655">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-2655">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2657">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-2657">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2659">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2659">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2661">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2661">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2663">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-2663">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-2664">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2664">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-2665">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2665">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2666">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2666">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2667">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-2667">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2669">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-2669">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2671">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2671">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2673">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-2673">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-2674">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-2674">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-2675">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-2675">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-2676">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-2676">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-2677">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-2677">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2678">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-2678">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2679">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-2679">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2681">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2681">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2683">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2683">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2685">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-2685">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2687">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-2687">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2689">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2689">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2691">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-2691">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-2692">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-2692">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2694">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2694">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-2695">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-2695">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-2696">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-2696">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-2697">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2697">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-2698">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-2698">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-2699">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2699">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="4845f-2701">DXGI_FORMAT_R16G16 \_ UINT<sup>FCS</sup> (36) </span><span class="sxs-lookup"><span data-stu-id="4845f-2701">DXGI_FORMAT_R16G16\_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="4845f-2702">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2702">Target</span></span> | <span data-ttu-id="4845f-2703">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2703">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-2704">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-2704">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-2705">32</span><span class="sxs-lookup"><span data-stu-id="4845f-2705">32</span></span> |
| <span data-ttu-id="4845f-2706">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2706">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2708">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-2708">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2710">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2710">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2712">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2712">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2713">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2713">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2714">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-2714">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2716">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-2716">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2718">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-2718">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2720">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-2720">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2722">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-2722">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2724">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2724">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-2725">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2725">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-2726">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2726">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-2727">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-2727">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-2728">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-2728">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-2729">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-2729">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2731">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-2731">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-2732">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2732">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2734">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2734">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-2735">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-2735">Output Merger Logic Op</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2737">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-2738">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2739">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2740">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-2740">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2742">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-2742">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2744">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2744">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2746">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-2746">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-2747">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-2747">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-2748">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-2748">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-2749">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-2749">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-2750">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-2750">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2751">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-2751">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2752">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-2752">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2754">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2754">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2756">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2756">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2758">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-2758">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2760">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-2760">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-2761">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2761">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2763">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-2763">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-2764">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-2764">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2766">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2766">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-2767">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-2767">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-2768">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-2768">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-2769">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2769">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-2770">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-2770">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-2771">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2771">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="4845f-2773">DXGI_FORMAT_R16G16 \_ SNORM 的<sup>FCS</sup> (37) </span><span class="sxs-lookup"><span data-stu-id="4845f-2773">DXGI_FORMAT_R16G16\_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="4845f-2774">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2774">Target</span></span> | <span data-ttu-id="4845f-2775">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2775">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-2776">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-2776">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-2777">32</span><span class="sxs-lookup"><span data-stu-id="4845f-2777">32</span></span> |
| <span data-ttu-id="4845f-2778">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2778">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2780">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-2780">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2782">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2782">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2784">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2784">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2785">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2785">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2786">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-2786">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2788">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-2788">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2790">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-2790">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2792">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-2792">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2794">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-2794">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2796">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2796">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2798">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2798">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-2799">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2799">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-2800">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-2800">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2802">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-2802">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-2803">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-2803">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2805">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-2805">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2807">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2807">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2809">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2809">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2811">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-2811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-2812">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2812">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-2813">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2813">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2814">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2814">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2815">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-2815">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2817">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-2817">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2819">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2819">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2821">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-2821">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-2822">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-2822">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-2823">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-2823">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-2824">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-2824">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-2825">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-2825">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2826">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-2826">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2827">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-2827">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2829">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2829">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2831">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2831">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2833">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-2833">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2835">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-2835">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2837">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2837">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2839">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-2839">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-2840">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-2840">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2842">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2842">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-2843">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-2843">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-2844">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-2844">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-2845">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2845">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-2846">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-2846">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-2847">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2847">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="4845f-2849">DXGI_FORMAT_R16G16 \_ 聖的<sup>FCS</sup> (38) </span><span class="sxs-lookup"><span data-stu-id="4845f-2849">DXGI_FORMAT_R16G16\_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="4845f-2850">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2850">Target</span></span> | <span data-ttu-id="4845f-2851">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2851">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-2852">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-2852">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-2853">32</span><span class="sxs-lookup"><span data-stu-id="4845f-2853">32</span></span> |
| <span data-ttu-id="4845f-2854">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2854">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2856">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-2856">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2858">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2858">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2860">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2861">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-2862">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2864">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-2864">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2866">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-2866">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2868">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-2868">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2870">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-2870">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2872">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2872">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-2873">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2873">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-2874">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2874">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-2875">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-2875">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-2876">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-2876">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-2877">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-2877">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2879">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-2879">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-2880">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2880">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2882">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-2883">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-2883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-2884">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-2885">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2886">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2887">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-2887">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2889">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-2889">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2891">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2891">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2893">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-2893">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-2894">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-2894">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-2895">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-2895">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-2896">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-2896">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-2897">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-2897">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2898">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-2898">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2899">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-2899">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2901">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2901">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2903">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2903">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2905">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-2905">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-2907">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-2907">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-2908">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2908">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2910">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-2910">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-2911">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-2911">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2913">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2913">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-2914">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-2914">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-2915">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-2915">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-2916">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2916">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-2917">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-2917">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-2918">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2918">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="4845f-2920">DXGI_FORMAT_R32 無的 \_ <sup>電腦</sup> (39) </span><span class="sxs-lookup"><span data-stu-id="4845f-2920">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="4845f-2921">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2921">Target</span></span> | <span data-ttu-id="4845f-2922">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2922">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-2923">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-2923">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-2924">32</span><span class="sxs-lookup"><span data-stu-id="4845f-2924">32</span></span> |
| <span data-ttu-id="4845f-2925">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2925">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2927">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-2927">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2928">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2928">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2929">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2929">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2930">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2930">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2931">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-2931">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2933">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-2933">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2935">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-2935">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2937">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-2937">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2939">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-2939">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-2940">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2940">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-2941">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2941">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-2942">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-2942">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-2943">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-2943">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-2944">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-2944">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-2945">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-2945">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2947">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-2947">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-2948">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2948">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-2949">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2949">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-2950">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-2950">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-2951">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2951">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-2952">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2952">Raw UAV and SRV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2954">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-2954">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-2955">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-2955">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-2956">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-2956">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-2957">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2957">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-2958">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-2958">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-2959">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-2959">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-2960">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-2960">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-2961">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-2961">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-2962">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-2962">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2963">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-2963">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-2964">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-2964">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2966">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2966">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-2967">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-2967">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-2968">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-2968">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-2969">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-2969">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-2970">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-2970">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-2971">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-2971">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-2972">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-2972">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2974">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2974">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-2975">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-2975">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-2976">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-2976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-2977">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2977">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2979">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-2979">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-2980">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-2980">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="4845f-2982">DXGI_FORMAT_D32 \_ FLOAT<sup>FCS</sup> (40) </span><span class="sxs-lookup"><span data-stu-id="4845f-2982">DXGI_FORMAT_D32\_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="4845f-2983">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-2983">Target</span></span> | <span data-ttu-id="4845f-2984">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2984">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-2985">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-2985">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-2986">32</span><span class="sxs-lookup"><span data-stu-id="4845f-2986">32</span></span> |
| <span data-ttu-id="4845f-2987">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-2987">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2989">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-2989">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2990">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2990">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2991">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2991">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2992">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-2992">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-2993">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-2993">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2995">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-2995">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-2997">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-2997">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-2998">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-2998">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3000">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-3000">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-3001">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3001">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-3002">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3002">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-3003">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3003">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-3004">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-3004">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-3005">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-3005">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-3006">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-3006">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3008">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-3008">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-3009">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3009">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3010">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3010">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3011">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-3011">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-3012">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3012">Depth/Stencil Target</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3014">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3015">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3016">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-3016">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-3017">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-3017">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-3018">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3018">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-3019">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-3019">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-3020">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-3020">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-3021">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-3021">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-3022">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-3022">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-3023">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-3023">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3024">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-3024">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3025">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-3025">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3027">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3027">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3029">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3029">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3031">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-3031">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-3033">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-3033">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-3034">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3034">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-3035">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-3035">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-3036">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-3036">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3038">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3038">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-3039">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-3039">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-3040">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-3040">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-3041">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3041">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3043">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-3043">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-3044">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3044">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="4845f-3046">DXGI_FORMAT_R32 \_ FLOAT<sup>FCS</sup> (41) </span><span class="sxs-lookup"><span data-stu-id="4845f-3046">DXGI_FORMAT_R32\_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="4845f-3047">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3047">Target</span></span> | <span data-ttu-id="4845f-3048">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3048">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-3049">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-3049">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-3050">32</span><span class="sxs-lookup"><span data-stu-id="4845f-3050">32</span></span> |
| <span data-ttu-id="4845f-3051">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3051">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3053">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-3053">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3055">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3055">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3057">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3057">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3058">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3058">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3060">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-3060">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3062">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-3062">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3064">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-3064">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3066">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-3066">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3068">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-3068">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3070">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3070">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3072">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3072">Shader sample\_c (comparison filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3074">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3074">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-3075">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-3075">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3077">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-3077">Shader gather4\_c</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3079">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-3079">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3081">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-3081">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3083">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3083">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3085">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3085">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3087">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-3087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-3088">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-3089">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3090">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3091">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-3091">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3093">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-3093">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3095">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3095">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3097">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-3097">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-3098">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-3098">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-3099">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-3099">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-3100">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-3100">UAV Atomic Exchange</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3102">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-3102">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3103">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-3103">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3104">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-3104">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3106">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3106">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3108">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3108">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3110">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-3110">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-3112">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-3112">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3114">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3114">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3116">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-3116">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-3117">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-3117">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3119">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3119">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-3120">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-3120">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-3121">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-3121">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-3122">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3122">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3124">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-3124">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-3125">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3125">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="4845f-3127">DXGI_FORMAT_R32 \_ UINT<sup>FCS</sup> (42) </span><span class="sxs-lookup"><span data-stu-id="4845f-3127">DXGI_FORMAT_R32\_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="4845f-3128">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3128">Target</span></span> | <span data-ttu-id="4845f-3129">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3129">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-3130">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-3130">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-3131">32</span><span class="sxs-lookup"><span data-stu-id="4845f-3131">32</span></span> |
| <span data-ttu-id="4845f-3132">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3132">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3134">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-3134">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3136">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3136">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3138">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3138">Input Assembler Index Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3140">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3140">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3142">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-3142">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3144">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-3144">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3146">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-3146">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3148">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-3148">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3150">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-3150">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3152">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3152">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-3153">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3153">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-3154">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3154">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-3155">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-3155">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-3156">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-3156">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-3157">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-3157">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3159">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-3159">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-3160">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3160">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3162">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3162">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3163">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-3163">Output Merger Logic Op</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3165">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3165">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-3166">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3166">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3167">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3167">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3168">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-3168">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3170">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-3170">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3172">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3172">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3174">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-3174">UAV Atomic Add</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3176">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-3176">UAV Atomic Bitwise Ops</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3178">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-3178">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3180">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-3180">UAV Atomic Exchange</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3182">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-3182">UAV Atomic Signed Min/Max</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3184">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-3184">UAV Atomic Unsigned Min/Max</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3186">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-3186">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3188">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3188">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3190">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3190">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3192">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-3192">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-3194">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-3194">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-3195">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3195">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3197">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-3197">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-3198">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-3198">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3200">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3200">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-3201">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-3201">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-3202">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-3202">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-3203">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3203">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3205">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-3205">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-3206">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3206">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="4845f-3208">DXGI_FORMAT_R32 \_ 聖的<sup>FCS</sup> (43) </span><span class="sxs-lookup"><span data-stu-id="4845f-3208">DXGI_FORMAT_R32\_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="4845f-3209">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3209">Target</span></span> | <span data-ttu-id="4845f-3210">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3210">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-3211">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-3211">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-3212">32</span><span class="sxs-lookup"><span data-stu-id="4845f-3212">32</span></span> |
| <span data-ttu-id="4845f-3213">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3213">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3215">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-3215">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3217">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3217">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3219">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3219">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3220">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3220">Stream Output Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3222">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-3222">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3224">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-3224">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3226">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-3226">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3228">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-3228">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3230">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-3230">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3232">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3232">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-3233">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3233">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-3234">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3234">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-3235">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-3235">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-3236">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-3236">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-3237">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-3237">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3239">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-3239">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-3240">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3240">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3242">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3242">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3243">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-3243">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-3244">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3244">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-3245">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3245">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3246">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3246">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3247">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-3247">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3249">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-3249">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3251">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3251">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3253">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-3253">UAV Atomic Add</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3255">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-3255">UAV Atomic Bitwise Ops</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3257">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-3257">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3259">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-3259">UAV Atomic Exchange</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3261">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-3261">UAV Atomic Signed Min/Max</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3263">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-3263">UAV Atomic Unsigned Min/Max</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3265">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-3265">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3267">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3267">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3269">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3269">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3271">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-3271">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-3273">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-3273">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-3274">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3274">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3276">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-3276">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-3277">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-3277">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3279">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3279">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-3280">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-3280">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-3281">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-3281">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-3282">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3282">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3284">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-3284">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-3285">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3285">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r24g8_typeless-44"></a><span data-ttu-id="4845f-3287">DXGI_FORMAT_R24G8 不 \_ (44) </span><span class="sxs-lookup"><span data-stu-id="4845f-3287">DXGI_FORMAT_R24G8\_TYPELESS (44)</span></span>
| <span data-ttu-id="4845f-3288">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3288">Target</span></span> | <span data-ttu-id="4845f-3289">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3289">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-3290">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-3290">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-3291">32</span><span class="sxs-lookup"><span data-stu-id="4845f-3291">32</span></span> |
| <span data-ttu-id="4845f-3292">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3292">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3294">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-3294">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3295">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3295">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3296">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3296">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3297">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3297">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3298">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-3298">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3300">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-3300">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3302">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-3302">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-3303">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-3303">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3305">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-3305">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-3306">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3306">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-3307">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3307">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-3308">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3308">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-3309">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-3309">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-3310">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-3310">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-3311">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-3311">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3313">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-3313">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-3314">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3314">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3315">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3315">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3316">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-3316">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-3317">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3317">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-3318">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3318">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3319">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3319">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3320">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-3320">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-3321">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-3321">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-3322">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3322">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-3323">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-3323">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-3324">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-3324">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-3325">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-3325">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-3326">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-3326">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-3327">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-3327">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3328">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-3328">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3329">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-3329">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3331">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3331">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3332">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3332">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3333">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-3333">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-3334">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-3334">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-3335">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3335">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-3336">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-3336">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-3337">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-3337">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3339">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3339">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-3340">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-3340">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-3341">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-3341">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-3342">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3342">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-3343">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-3343">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-3344">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3344">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uint-45"></a><span data-ttu-id="4845f-3345">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT (45) </span><span class="sxs-lookup"><span data-stu-id="4845f-3345">DXGI_FORMAT_D24\_UNORM\_S8\_UINT (45)</span></span>
| <span data-ttu-id="4845f-3346">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3346">Target</span></span> | <span data-ttu-id="4845f-3347">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3347">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-3348">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-3348">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-3349">32</span><span class="sxs-lookup"><span data-stu-id="4845f-3349">32</span></span> |
| <span data-ttu-id="4845f-3350">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3350">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3352">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-3352">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3353">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3353">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3354">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3354">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3355">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3355">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3356">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-3356">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3358">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-3358">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3360">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-3360">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-3361">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-3361">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3363">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-3363">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-3364">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3364">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-3365">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3365">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-3366">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3366">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-3367">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-3367">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-3368">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-3368">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-3369">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-3369">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3371">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-3371">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-3372">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3372">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3373">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3373">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3374">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-3374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-3375">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3375">Depth/Stencil Target</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3377">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3377">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3378">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3378">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3379">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-3379">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-3380">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-3380">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-3381">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3381">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-3382">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-3382">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-3383">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-3383">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-3384">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-3384">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-3385">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-3385">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-3386">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-3386">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3387">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-3387">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3388">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-3388">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3390">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3390">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3392">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3392">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3394">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-3394">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-3396">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-3396">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-3397">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3397">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-3398">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-3398">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-3399">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-3399">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3401">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3401">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-3402">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-3402">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-3403">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-3403">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-3404">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3404">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-3405">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-3405">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-3406">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3406">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typeless-46"></a><span data-ttu-id="4845f-3407">DXGI_FORMAT_R24 \_ UNORM \_ X8 無別 \_ (46) </span><span class="sxs-lookup"><span data-stu-id="4845f-3407">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS (46)</span></span>
| <span data-ttu-id="4845f-3408">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3408">Target</span></span> | <span data-ttu-id="4845f-3409">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3409">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-3410">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-3410">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-3411">32</span><span class="sxs-lookup"><span data-stu-id="4845f-3411">32</span></span> |
| <span data-ttu-id="4845f-3412">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3412">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3414">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-3414">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3415">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3415">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3416">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3416">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3417">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3417">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3418">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-3418">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3420">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-3420">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3422">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-3422">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-3423">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-3423">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3425">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-3425">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3427">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3427">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3429">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3429">Shader sample\_c (comparison filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3431">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3431">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-3432">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-3432">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3434">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-3434">Shader gather4\_c</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3436">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-3436">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3438">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-3438">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-3439">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3439">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3440">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3440">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3441">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-3441">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-3442">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3442">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-3443">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3443">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3444">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3444">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3445">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-3445">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-3446">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-3446">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-3447">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3447">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-3448">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-3448">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-3449">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-3449">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-3450">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-3450">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-3451">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-3451">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-3452">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-3452">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3453">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-3453">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3454">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-3454">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3456">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3456">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3457">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3457">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3458">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-3458">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-3459">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-3459">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-3460">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3460">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3462">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-3462">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-3463">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-3463">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3465">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3465">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-3466">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-3466">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-3467">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-3467">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-3468">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3468">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-3469">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-3469">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-3470">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3470">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uint-47"></a><span data-ttu-id="4845f-3471">DXGI_FORMAT_X24 無別 \_ \_ G8 \_ UINT (47) </span><span class="sxs-lookup"><span data-stu-id="4845f-3471">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT (47)</span></span>
| <span data-ttu-id="4845f-3472">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3472">Target</span></span> | <span data-ttu-id="4845f-3473">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3473">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-3474">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-3474">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-3475">32</span><span class="sxs-lookup"><span data-stu-id="4845f-3475">32</span></span> |
| <span data-ttu-id="4845f-3476">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3476">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3478">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-3478">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3479">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3479">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3480">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3480">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3481">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3481">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3482">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-3482">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3484">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-3484">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3486">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-3486">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-3487">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-3487">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3489">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-3489">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3491">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3491">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-3492">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3492">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-3493">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3493">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-3494">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-3494">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-3495">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-3495">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-3496">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-3496">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3498">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-3498">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-3499">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3499">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3500">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3500">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3501">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-3501">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-3502">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3502">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-3503">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3503">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3504">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3504">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3505">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-3505">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-3506">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-3506">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-3507">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3507">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-3508">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-3508">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-3509">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-3509">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-3510">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-3510">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-3511">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-3511">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-3512">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-3512">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3513">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-3513">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3514">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-3514">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3516">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3516">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3517">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3517">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3518">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-3518">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-3519">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-3519">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-3520">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3520">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3522">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-3522">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-3523">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-3523">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3525">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3525">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-3526">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-3526">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-3527">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-3527">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-3528">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3528">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-3529">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-3529">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-3530">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3530">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="4845f-3531">DXGI_FORMAT_R8G8 無的 \_ <sup>電腦</sup> (48) </span><span class="sxs-lookup"><span data-stu-id="4845f-3531">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="4845f-3532">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3532">Target</span></span> | <span data-ttu-id="4845f-3533">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3533">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-3534">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-3534">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-3535">16</span><span class="sxs-lookup"><span data-stu-id="4845f-3535">16</span></span> |
| <span data-ttu-id="4845f-3536">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3536">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3538">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-3538">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3539">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3539">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3540">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3540">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3541">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3541">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3542">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-3542">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3544">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-3544">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3546">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-3546">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3548">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-3548">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3550">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-3550">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-3551">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3551">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-3552">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3552">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-3553">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3553">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-3554">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-3554">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-3555">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-3555">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-3556">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-3556">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3558">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-3558">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-3559">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3559">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3560">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3560">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3561">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-3561">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-3562">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3562">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-3563">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3563">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3564">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3564">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3565">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-3565">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-3566">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-3566">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-3567">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3567">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-3568">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-3568">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-3569">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-3569">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-3570">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-3570">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-3571">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-3571">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-3572">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-3572">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3573">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-3573">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3574">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-3574">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3576">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3576">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3577">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3577">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3578">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-3578">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-3579">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-3579">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-3580">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3580">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-3581">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-3581">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-3582">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-3582">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3584">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3584">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-3585">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-3585">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-3586">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-3586">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-3587">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3587">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-3588">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-3588">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-3589">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3589">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="4845f-3591">DXGI_FORMAT_R8G8 \_ UNORM 的<sup>FCS</sup> (49) </span><span class="sxs-lookup"><span data-stu-id="4845f-3591">DXGI_FORMAT_R8G8\_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="4845f-3592">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3592">Target</span></span> | <span data-ttu-id="4845f-3593">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3593">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-3594">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-3594">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-3595">16</span><span class="sxs-lookup"><span data-stu-id="4845f-3595">16</span></span> |
| <span data-ttu-id="4845f-3596">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3596">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3598">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-3598">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3600">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3600">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3602">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3602">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3603">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3603">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3604">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-3604">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3606">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-3606">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3608">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-3608">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-3610">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3612">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-3612">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3614">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3614">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3616">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3616">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-3617">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3617">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-3618">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-3618">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3620">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-3620">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-3621">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-3621">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3623">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-3623">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3625">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3625">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3627">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3627">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3629">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-3629">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-3630">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3630">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-3631">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3631">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3632">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3632">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3633">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-3633">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3635">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-3635">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3637">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3637">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-3639">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-3639">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-3640">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-3640">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-3641">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-3641">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-3642">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-3642">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-3643">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-3643">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3644">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-3644">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3645">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-3645">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3647">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3647">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3649">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3649">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3651">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-3651">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-3653">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-3653">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3655">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3655">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3657">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-3657">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-3658">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-3658">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3660">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3660">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-3661">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-3661">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-3662">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-3662">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-3663">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3663">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3665">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-3665">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-3666">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3666">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="4845f-3668">DXGI_FORMAT_R8G8 \_ UINT<sup>FCS</sup> (50) </span><span class="sxs-lookup"><span data-stu-id="4845f-3668">DXGI_FORMAT_R8G8\_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="4845f-3669">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3669">Target</span></span> | <span data-ttu-id="4845f-3670">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3670">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-3671">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-3671">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-3672">16</span><span class="sxs-lookup"><span data-stu-id="4845f-3672">16</span></span> |
| <span data-ttu-id="4845f-3673">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3673">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3675">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-3675">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3677">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3677">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3679">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3679">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3680">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3680">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3681">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-3681">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3683">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-3683">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3685">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-3685">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3687">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-3687">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3689">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-3689">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3691">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3691">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-3692">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3692">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-3693">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3693">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-3694">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-3694">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-3695">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-3695">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-3696">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-3696">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3698">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-3698">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-3699">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3699">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3701">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3701">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3702">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-3702">Output Merger Logic Op</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3704">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3704">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-3705">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3705">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3706">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3706">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3707">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-3707">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3709">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-3709">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3711">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3711">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-3713">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-3713">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-3714">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-3714">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-3715">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-3715">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-3716">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-3716">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-3717">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-3717">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3718">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-3718">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3719">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-3719">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3721">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3721">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3723">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3723">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3725">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-3725">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-3727">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-3727">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-3728">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3728">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3730">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-3730">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-3731">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-3731">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3733">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3733">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-3734">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-3734">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-3735">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-3735">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-3736">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3736">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-3737">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-3737">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-3738">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3738">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="4845f-3740">DXGI_FORMAT_R8G8 \_ SNORM 的<sup>FCS</sup> (51) </span><span class="sxs-lookup"><span data-stu-id="4845f-3740">DXGI_FORMAT_R8G8\_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="4845f-3741">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3741">Target</span></span> | <span data-ttu-id="4845f-3742">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3742">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-3743">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-3743">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-3744">16</span><span class="sxs-lookup"><span data-stu-id="4845f-3744">16</span></span> |
| <span data-ttu-id="4845f-3745">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3745">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3747">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-3747">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3749">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3749">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3751">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3751">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3752">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3752">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3753">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-3753">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3755">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-3755">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-3757">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3759">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-3759">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3761">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-3761">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3763">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3763">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3765">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3765">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-3766">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3766">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-3767">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-3767">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3769">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-3769">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-3770">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-3770">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3772">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-3772">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3774">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3774">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3776">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3776">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3778">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-3778">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-3779">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3779">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-3780">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3780">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3781">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3781">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3782">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-3782">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3784">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-3784">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3786">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3786">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-3788">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-3788">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-3789">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-3789">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-3790">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-3790">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-3791">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-3791">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-3792">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-3792">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3793">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-3793">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3794">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-3794">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3796">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3796">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3798">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3798">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3800">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-3800">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-3802">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-3802">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3804">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3804">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3806">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-3806">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-3807">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-3807">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3809">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3809">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-3810">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-3810">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-3811">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-3811">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-3812">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3812">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-3813">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-3813">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-3814">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3814">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="4845f-3816">DXGI_FORMAT_R8G8 \_ 聖的<sup>FCS</sup> (52) </span><span class="sxs-lookup"><span data-stu-id="4845f-3816">DXGI_FORMAT_R8G8\_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="4845f-3817">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3817">Target</span></span> | <span data-ttu-id="4845f-3818">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3818">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-3819">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-3819">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-3820">16</span><span class="sxs-lookup"><span data-stu-id="4845f-3820">16</span></span> |
| <span data-ttu-id="4845f-3821">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3821">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3823">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-3823">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3825">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3825">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3827">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3827">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3828">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3828">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3829">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-3829">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3831">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-3831">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3833">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-3833">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3835">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-3835">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3837">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-3837">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3839">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3839">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-3840">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3840">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-3841">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3841">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-3842">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-3842">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-3843">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-3843">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-3844">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-3844">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3846">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-3846">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-3847">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3847">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3849">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3849">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3850">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-3850">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-3851">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3851">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-3852">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3852">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3853">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3853">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3854">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-3854">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3856">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-3856">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3858">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3858">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-3860">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-3860">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-3861">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-3861">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-3862">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-3862">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-3863">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-3863">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-3864">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-3864">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3865">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-3865">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3866">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-3866">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3868">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3868">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3870">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3870">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3872">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-3872">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-3874">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-3874">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-3875">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3875">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3877">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-3877">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-3878">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-3878">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3880">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3880">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-3881">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-3881">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-3882">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-3882">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-3883">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3883">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-3884">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-3884">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-3885">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3885">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="4845f-3887">DXGI_FORMAT_R16 無的 \_ <sup>電腦</sup> (53) </span><span class="sxs-lookup"><span data-stu-id="4845f-3887">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="4845f-3888">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3888">Target</span></span> | <span data-ttu-id="4845f-3889">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3889">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-3890">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-3890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-3891">16</span><span class="sxs-lookup"><span data-stu-id="4845f-3891">16</span></span> |
| <span data-ttu-id="4845f-3892">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3892">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3894">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-3894">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3895">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3896">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3897">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-3898">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3900">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-3900">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3902">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-3902">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3904">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-3904">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3906">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-3906">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-3907">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3907">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-3908">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3908">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-3909">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3909">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-3910">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-3910">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-3911">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-3911">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-3912">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-3912">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3914">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-3914">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-3915">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3915">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3916">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3916">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3917">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-3917">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-3918">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3918">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-3919">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3919">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3920">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3920">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3921">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-3921">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-3922">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-3922">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-3923">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3923">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-3924">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-3924">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-3925">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-3925">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-3926">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-3926">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-3927">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-3927">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-3928">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-3928">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3929">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-3929">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-3930">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-3930">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3932">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3932">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3933">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3933">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-3934">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-3934">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-3935">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-3935">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-3936">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3936">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-3937">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-3937">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-3938">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-3938">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3940">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3940">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-3941">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-3941">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-3942">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-3942">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-3943">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3943">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3945">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-3945">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-3946">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-3946">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="4845f-3948">DXGI_FORMAT_R16 \_ FLOAT<sup>FCS</sup> (54) </span><span class="sxs-lookup"><span data-stu-id="4845f-3948">DXGI_FORMAT_R16\_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="4845f-3949">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3949">Target</span></span> | <span data-ttu-id="4845f-3950">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3950">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-3951">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-3951">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-3952">16</span><span class="sxs-lookup"><span data-stu-id="4845f-3952">16</span></span> |
| <span data-ttu-id="4845f-3953">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-3953">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3955">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-3955">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3957">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3957">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3959">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3959">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3960">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-3960">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-3961">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-3961">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3963">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-3963">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3965">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-3965">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3967">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-3967">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3969">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-3969">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3971">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3971">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3973">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3973">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-3974">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-3974">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-3975">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-3975">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3977">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-3977">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-3978">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-3978">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3980">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-3980">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3982">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3982">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3984">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-3984">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3986">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-3986">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-3987">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-3987">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-3988">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3988">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3989">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-3989">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-3990">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-3990">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3992">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-3992">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3994">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-3994">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-3996">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-3996">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-3997">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-3997">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-3998">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-3998">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-3999">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-3999">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-4000">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-4000">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4001">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-4001">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4002">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-4002">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4004">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4004">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4006">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4006">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4008">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-4008">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-4010">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-4010">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4012">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4012">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4014">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-4014">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-4015">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-4015">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4017">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4017">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-4018">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-4018">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-4019">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-4019">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-4020">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4020">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4022">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-4022">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-4023">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4023">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="4845f-4025">DXGI_FORMAT_D16 \_ UNORM 的<sup>FCS</sup> (55) </span><span class="sxs-lookup"><span data-stu-id="4845f-4025">DXGI_FORMAT_D16\_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="4845f-4026">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4026">Target</span></span> | <span data-ttu-id="4845f-4027">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4027">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-4028">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-4028">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-4029">16</span><span class="sxs-lookup"><span data-stu-id="4845f-4029">16</span></span> |
| <span data-ttu-id="4845f-4030">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4030">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4032">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-4032">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4033">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4033">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4034">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4034">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4035">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4035">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4036">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-4036">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4038">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-4038">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4040">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-4040">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-4041">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-4041">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4043">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-4043">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-4044">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4044">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-4045">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4045">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-4046">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4046">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-4047">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-4047">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-4048">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-4048">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-4049">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-4049">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4051">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-4051">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-4052">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4052">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4053">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4053">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4054">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-4054">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-4055">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4055">Depth/Stencil Target</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4057">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4057">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4058">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4058">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4059">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-4059">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-4060">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-4060">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-4061">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4061">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-4062">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-4062">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-4063">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-4063">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-4064">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-4064">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-4065">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-4065">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-4066">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-4066">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4067">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-4067">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4068">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-4068">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4070">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4070">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4072">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4072">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4074">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-4074">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-4076">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-4076">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-4077">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4077">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-4078">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-4078">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-4079">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-4079">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4081">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4081">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-4082">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-4082">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-4083">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-4083">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-4084">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4084">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4086">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-4086">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-4087">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4087">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="4845f-4089">DXGI_FORMAT_R16 \_ UNORM 的<sup>FCS</sup> (56) </span><span class="sxs-lookup"><span data-stu-id="4845f-4089">DXGI_FORMAT_R16\_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="4845f-4090">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4090">Target</span></span> | <span data-ttu-id="4845f-4091">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4091">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-4092">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-4092">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-4093">16</span><span class="sxs-lookup"><span data-stu-id="4845f-4093">16</span></span> |
| <span data-ttu-id="4845f-4094">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4094">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4096">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-4096">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4098">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4098">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4100">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4100">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4101">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4101">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4102">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-4102">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4104">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-4104">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4106">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-4106">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4108">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-4108">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4110">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-4110">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4112">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4112">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4114">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4114">Shader sample\_c (comparison filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4116">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4116">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-4117">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-4117">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4119">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-4119">Shader gather4\_c</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4121">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-4121">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4123">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-4123">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4125">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4125">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4127">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4127">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4129">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-4129">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-4130">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4130">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-4131">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4131">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4132">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4132">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4133">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-4133">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4135">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-4135">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4137">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4137">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-4139">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-4139">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-4140">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-4140">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-4141">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-4141">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-4142">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-4142">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-4143">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-4143">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4144">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-4144">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4145">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-4145">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4147">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4147">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4149">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4149">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4151">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-4151">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-4153">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-4153">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4155">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4155">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4157">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-4157">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-4158">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-4158">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4160">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4160">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-4161">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-4161">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-4162">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-4162">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-4163">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4163">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4165">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-4165">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-4166">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4166">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="4845f-4168">DXGI_FORMAT_R16 \_ UINT<sup>FCS</sup> (57) </span><span class="sxs-lookup"><span data-stu-id="4845f-4168">DXGI_FORMAT_R16\_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="4845f-4169">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4169">Target</span></span> | <span data-ttu-id="4845f-4170">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4170">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-4171">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-4171">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-4172">16</span><span class="sxs-lookup"><span data-stu-id="4845f-4172">16</span></span> |
| <span data-ttu-id="4845f-4173">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4173">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4175">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-4175">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4177">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4177">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4179">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4179">Input Assembler Index Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4181">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4181">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4182">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-4182">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4184">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-4184">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4186">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-4186">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4188">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-4188">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4190">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-4190">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4192">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4192">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-4193">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4193">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-4194">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4194">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-4195">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-4195">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-4196">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-4196">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-4197">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-4197">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4199">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-4199">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-4200">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4200">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4202">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4202">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4203">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-4203">Output Merger Logic Op</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4205">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-4206">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4207">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4208">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-4208">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4210">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-4210">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4212">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4212">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4214">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-4214">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-4215">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-4215">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-4216">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-4216">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-4217">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-4217">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-4218">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-4218">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4219">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-4219">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4220">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-4220">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4222">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4222">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4224">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4224">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4226">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-4226">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-4228">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-4228">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-4229">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4229">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4231">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-4231">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-4232">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-4232">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4234">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4234">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-4235">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-4235">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-4236">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-4236">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-4237">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4237">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4239">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-4239">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-4240">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4240">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="4845f-4242">DXGI_FORMAT_R16 \_ SNORM 的<sup>FCS</sup> (58) </span><span class="sxs-lookup"><span data-stu-id="4845f-4242">DXGI_FORMAT_R16\_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="4845f-4243">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4243">Target</span></span> | <span data-ttu-id="4845f-4244">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4244">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-4245">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-4245">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-4246">16</span><span class="sxs-lookup"><span data-stu-id="4845f-4246">16</span></span> |
| <span data-ttu-id="4845f-4247">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4247">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4249">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-4249">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4251">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4251">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4253">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4253">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4254">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4254">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4255">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-4255">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4257">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-4257">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4259">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-4259">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4261">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-4261">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4263">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-4263">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4265">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4265">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4267">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4267">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-4268">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4268">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-4269">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-4269">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4271">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-4271">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-4272">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-4272">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4274">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-4274">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4276">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4276">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4278">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4278">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4280">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-4280">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-4281">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4281">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-4282">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4282">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4283">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4283">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4284">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-4284">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4286">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-4286">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4288">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4288">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-4290">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-4290">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-4291">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-4291">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-4292">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-4292">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-4293">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-4293">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-4294">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-4294">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4295">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-4295">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4296">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-4296">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4298">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4298">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4300">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4300">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4302">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-4302">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-4304">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-4304">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4306">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4306">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4308">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-4308">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-4309">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-4309">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4311">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4311">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-4312">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-4312">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-4313">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-4313">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-4314">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4314">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4316">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-4316">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-4317">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4317">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="4845f-4319">DXGI_FORMAT_R16 \_ 聖的<sup>FCS</sup> (59) </span><span class="sxs-lookup"><span data-stu-id="4845f-4319">DXGI_FORMAT_R16\_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="4845f-4320">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4320">Target</span></span> | <span data-ttu-id="4845f-4321">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4321">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-4322">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-4322">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-4323">16</span><span class="sxs-lookup"><span data-stu-id="4845f-4323">16</span></span> |
| <span data-ttu-id="4845f-4324">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4324">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4326">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-4326">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4328">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4328">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4330">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4330">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4331">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4331">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4332">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-4332">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-4334">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4336">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-4336">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4338">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-4338">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4340">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-4340">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4342">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4342">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-4343">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4343">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-4344">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4344">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-4345">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-4345">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-4346">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-4346">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-4347">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-4347">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4349">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-4349">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-4350">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4350">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4352">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4352">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4353">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-4353">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-4354">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4354">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-4355">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4355">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4356">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4356">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4357">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-4357">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4359">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-4359">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4361">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4361">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4363">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-4363">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-4364">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-4364">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-4365">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-4365">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-4366">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-4366">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-4367">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-4367">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4368">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-4368">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4369">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-4369">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4371">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4371">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4373">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4373">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4375">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-4375">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-4377">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-4377">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-4378">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4378">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4380">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-4380">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-4381">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-4381">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4383">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4383">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-4384">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-4384">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-4385">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-4385">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-4386">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4386">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4388">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-4388">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-4389">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4389">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="4845f-4391">DXGI_FORMAT_R8 無的 \_ <sup>電腦</sup> (60) </span><span class="sxs-lookup"><span data-stu-id="4845f-4391">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="4845f-4392">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4392">Target</span></span> | <span data-ttu-id="4845f-4393">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4393">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-4394">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-4394">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-4395">8</span><span class="sxs-lookup"><span data-stu-id="4845f-4395">8</span></span> |
| <span data-ttu-id="4845f-4396">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4396">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4398">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-4398">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4399">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4399">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4400">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4400">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4401">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4401">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4402">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-4402">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-4404">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4406">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-4406">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4408">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-4408">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4410">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-4410">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-4411">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4411">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-4412">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4412">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-4413">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4413">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-4414">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-4414">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-4415">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-4415">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-4416">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-4416">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4418">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-4418">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-4419">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4419">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4420">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4420">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4421">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-4421">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-4422">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4422">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-4423">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4423">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4424">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4424">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4425">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-4425">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-4426">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-4426">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-4427">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4427">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-4428">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-4428">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-4429">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-4429">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-4430">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-4430">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-4431">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-4431">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-4432">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-4432">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4433">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-4433">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4434">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-4434">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4436">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4436">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4437">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4437">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4438">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-4438">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-4439">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-4439">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-4440">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4440">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-4441">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-4441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-4442">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-4442">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4444">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4444">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-4445">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-4445">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-4446">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-4446">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-4447">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4447">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4449">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-4449">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-4450">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4450">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="4845f-4452">DXGI_FORMAT_R8 \_ UNORM 的<sup>FCS</sup> (61) </span><span class="sxs-lookup"><span data-stu-id="4845f-4452">DXGI_FORMAT_R8\_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="4845f-4453">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4453">Target</span></span> | <span data-ttu-id="4845f-4454">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4454">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-4455">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-4455">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-4456">8</span><span class="sxs-lookup"><span data-stu-id="4845f-4456">8</span></span> |
| <span data-ttu-id="4845f-4457">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4457">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4459">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-4459">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4461">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4461">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4463">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4463">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4464">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4464">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4465">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-4465">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4467">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-4467">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4469">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-4469">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4471">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-4471">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4473">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-4473">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4475">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4475">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4477">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4477">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-4478">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4478">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-4479">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-4479">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4481">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-4481">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-4482">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-4482">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4484">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-4484">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4486">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4486">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4488">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4488">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4490">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-4490">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-4491">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4491">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-4492">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4492">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4493">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4493">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4494">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-4494">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4496">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-4496">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4498">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4498">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4500">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-4500">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-4501">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-4501">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-4502">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-4502">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-4503">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-4503">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-4504">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-4504">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4505">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-4505">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4506">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-4506">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4508">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4508">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4510">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4510">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4512">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-4512">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-4514">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-4514">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4516">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4516">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4518">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-4518">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-4519">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-4519">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4521">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4521">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-4522">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-4522">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-4523">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-4523">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-4524">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4524">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4526">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-4526">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-4527">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4527">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="4845f-4529">DXGI_FORMAT_R8 \_ UINT<sup>FCS</sup> (62) </span><span class="sxs-lookup"><span data-stu-id="4845f-4529">DXGI_FORMAT_R8\_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="4845f-4530">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4530">Target</span></span> | <span data-ttu-id="4845f-4531">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4531">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-4532">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-4532">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-4533">8</span><span class="sxs-lookup"><span data-stu-id="4845f-4533">8</span></span> |
| <span data-ttu-id="4845f-4534">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4534">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4536">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-4536">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4538">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4538">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4540">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4540">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4541">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4541">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4542">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-4542">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4544">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-4544">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4546">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-4546">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4548">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-4548">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4550">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-4550">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4552">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4552">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-4553">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4553">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-4554">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4554">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-4555">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-4555">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-4556">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-4556">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-4557">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-4557">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4559">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-4559">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-4560">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4560">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4562">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4562">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4563">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-4563">Output Merger Logic Op</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4565">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-4566">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4567">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4568">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-4568">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4570">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-4570">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4572">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4572">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4574">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-4574">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-4575">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-4575">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-4576">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-4576">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-4577">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-4577">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-4578">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-4578">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4579">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-4579">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4580">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-4580">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4582">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4582">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4584">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4584">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4586">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-4586">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-4588">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-4588">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-4589">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4589">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4591">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-4591">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-4592">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-4592">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4594">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4594">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-4595">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-4595">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-4596">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-4596">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-4597">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4597">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4599">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-4599">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-4600">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4600">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="4845f-4602">DXGI_FORMAT_R8 \_ SNORM 的<sup>FCS</sup> (63) </span><span class="sxs-lookup"><span data-stu-id="4845f-4602">DXGI_FORMAT_R8\_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="4845f-4603">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4603">Target</span></span> | <span data-ttu-id="4845f-4604">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4604">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-4605">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-4605">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-4606">8</span><span class="sxs-lookup"><span data-stu-id="4845f-4606">8</span></span> |
| <span data-ttu-id="4845f-4607">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4607">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4609">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-4609">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4611">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4611">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4613">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4613">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4614">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4614">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4615">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-4615">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4617">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-4617">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4619">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-4619">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4621">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-4621">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4623">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-4623">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4625">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4625">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4627">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4627">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-4628">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4628">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-4629">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-4629">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4631">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-4631">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-4632">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-4632">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4634">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-4634">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4636">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4636">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4638">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4638">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4640">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-4640">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-4641">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4641">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-4642">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4642">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4643">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4643">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4644">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-4644">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4646">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-4646">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4648">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4648">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-4650">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-4650">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-4651">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-4651">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-4652">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-4652">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-4653">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-4653">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-4654">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-4654">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4655">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-4655">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4656">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-4656">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4658">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4658">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4660">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4660">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4662">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-4662">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-4664">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-4664">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4666">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4666">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4668">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-4668">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-4669">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-4669">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4671">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4671">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-4672">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-4672">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-4673">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-4673">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-4674">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4674">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4676">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-4676">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-4677">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4677">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="4845f-4679">DXGI_FORMAT_R8 \_ 聖的<sup>FCS</sup> (64) </span><span class="sxs-lookup"><span data-stu-id="4845f-4679">DXGI_FORMAT_R8\_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="4845f-4680">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4680">Target</span></span> | <span data-ttu-id="4845f-4681">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4681">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-4682">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-4682">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-4683">8</span><span class="sxs-lookup"><span data-stu-id="4845f-4683">8</span></span> |
| <span data-ttu-id="4845f-4684">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4684">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4686">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-4686">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4688">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4688">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4690">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4690">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4691">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4691">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4692">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-4692">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4694">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-4694">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4696">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-4696">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4698">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-4698">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4700">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-4700">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4702">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4702">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-4703">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4703">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-4704">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4704">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-4705">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-4705">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-4706">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-4706">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-4707">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-4707">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4709">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-4709">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-4710">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4710">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4712">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4712">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4713">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-4713">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-4714">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4714">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-4715">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4715">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4716">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4716">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4717">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-4717">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4719">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-4719">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4721">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4721">UAV Typed Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4723">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-4723">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-4724">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-4724">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-4725">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-4725">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-4726">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-4726">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-4727">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-4727">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4728">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-4728">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4729">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-4729">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4731">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4731">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4733">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4733">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4735">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-4735">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-4737">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-4737">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-4738">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4738">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4740">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-4740">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-4741">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-4741">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4743">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4743">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-4744">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-4744">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-4745">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-4745">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-4746">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4746">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4748">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-4748">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-4749">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4749">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="4845f-4751">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65) </span><span class="sxs-lookup"><span data-stu-id="4845f-4751">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="4845f-4752">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4752">Target</span></span> | <span data-ttu-id="4845f-4753">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4753">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-4754">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-4754">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-4755">8</span><span class="sxs-lookup"><span data-stu-id="4845f-4755">8</span></span> |
| <span data-ttu-id="4845f-4756">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4756">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4758">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-4758">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4759">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4759">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4760">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4760">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4761">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4761">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4762">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-4762">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4764">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-4764">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4766">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-4766">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4768">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-4768">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4770">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-4770">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4772">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4772">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4774">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4774">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-4775">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4775">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-4776">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-4776">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4778">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-4778">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-4779">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-4779">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4781">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-4781">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4783">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4783">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4785">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4785">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4787">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-4787">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-4788">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4788">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-4789">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4789">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4790">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4790">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4791">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-4791">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4793">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-4793">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4795">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4795">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-4797">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-4797">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-4798">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-4798">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-4799">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-4799">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-4800">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-4800">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-4801">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-4801">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4802">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-4802">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4803">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-4803">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4805">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4805">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4807">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4807">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4809">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-4809">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-4811">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-4811">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4813">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4813">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4815">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-4815">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-4816">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-4816">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-4817">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4817">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-4818">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-4818">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-4819">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-4819">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-4820">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4820">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4822">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-4822">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-4823">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4823">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="4845f-4825">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67) </span><span class="sxs-lookup"><span data-stu-id="4845f-4825">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="4845f-4826">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4826">Target</span></span> | <span data-ttu-id="4845f-4827">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4827">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-4828">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-4828">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-4829">32</span><span class="sxs-lookup"><span data-stu-id="4845f-4829">32</span></span> |
| <span data-ttu-id="4845f-4830">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4830">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4832">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-4832">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4833">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4833">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4834">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4834">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4835">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4835">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4836">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-4836">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4838">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-4838">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4840">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-4840">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4842">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-4842">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4844">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-4844">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4846">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4846">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4848">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4848">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-4849">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4849">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-4850">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-4850">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4852">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-4852">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-4853">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-4853">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4855">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-4855">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-4856">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4856">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4857">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4857">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4858">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-4858">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-4859">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4859">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-4860">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4860">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4861">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4861">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4862">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-4862">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-4863">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-4863">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-4864">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4864">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-4865">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-4865">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-4866">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-4866">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-4867">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-4867">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-4868">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-4868">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-4869">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-4869">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4870">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-4870">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4871">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-4871">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4873">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4873">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4874">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4874">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4875">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-4875">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-4876">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-4876">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-4877">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4877">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-4878">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-4878">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-4879">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-4879">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-4880">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4880">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-4881">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-4881">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-4882">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-4882">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-4883">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4883">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-4884">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-4884">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-4885">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4885">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="4845f-4887">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68) </span><span class="sxs-lookup"><span data-stu-id="4845f-4887">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="4845f-4888">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4888">Target</span></span> | <span data-ttu-id="4845f-4889">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4889">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-4890">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-4890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-4891">16</span><span class="sxs-lookup"><span data-stu-id="4845f-4891">16</span></span> |
| <span data-ttu-id="4845f-4892">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4892">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4894">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-4894">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4895">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4896">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4897">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-4898">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4900">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-4900">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4902">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-4902">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4904">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-4904">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4906">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-4906">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4908">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4908">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4910">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4910">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-4911">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4911">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-4912">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-4912">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4914">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-4914">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-4915">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-4915">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4917">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-4917">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-4918">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4918">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4919">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4919">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4920">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-4920">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-4921">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4921">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-4922">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4922">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4923">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4923">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4924">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-4924">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-4925">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-4925">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-4926">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4926">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-4927">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-4927">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-4928">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-4928">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-4929">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-4929">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-4930">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-4930">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-4931">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-4931">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4932">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-4932">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4933">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-4933">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4935">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4935">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4936">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4936">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4937">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-4937">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-4938">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-4938">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-4939">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4939">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-4940">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-4940">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-4941">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-4941">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-4942">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4942">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-4943">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-4943">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-4944">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-4944">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-4945">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4945">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-4946">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-4946">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-4947">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-4947">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="4845f-4948">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69) </span><span class="sxs-lookup"><span data-stu-id="4845f-4948">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="4845f-4949">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4949">Target</span></span> | <span data-ttu-id="4845f-4950">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4950">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-4951">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-4951">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-4952">16</span><span class="sxs-lookup"><span data-stu-id="4845f-4952">16</span></span> |
| <span data-ttu-id="4845f-4953">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-4953">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4955">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-4955">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4956">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4956">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4957">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4957">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4958">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-4958">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-4959">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-4959">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4961">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-4961">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4963">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-4963">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4965">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-4965">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4967">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-4967">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4969">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4969">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4971">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4971">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-4972">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-4972">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-4973">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-4973">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4975">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-4975">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-4976">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-4976">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4978">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-4978">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-4979">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4979">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4980">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4980">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4981">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-4981">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-4982">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-4982">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-4983">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4983">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4984">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-4984">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-4985">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-4985">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-4986">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-4986">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-4987">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-4987">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-4988">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-4988">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-4989">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-4989">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-4990">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-4990">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-4991">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-4991">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-4992">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-4992">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4993">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-4993">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-4994">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-4994">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-4996">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4996">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4997">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-4997">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-4998">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-4998">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-4999">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-4999">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-5000">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5000">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-5001">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-5001">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-5002">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-5002">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-5003">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5003">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-5004">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-5004">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-5005">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-5005">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-5006">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5006">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-5007">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-5007">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-5008">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5008">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="4845f-5009">DXGI_FORMAT_BC1 無別 \_ <sup>PCC</sup> (70) </span><span class="sxs-lookup"><span data-stu-id="4845f-5009">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="4845f-5010">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5010">Target</span></span> | <span data-ttu-id="4845f-5011">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5011">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-5012">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-5012">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-5013">64</span><span class="sxs-lookup"><span data-stu-id="4845f-5013">64</span></span> |
| <span data-ttu-id="4845f-5014">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5014">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5016">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-5016">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5017">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5017">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5018">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5018">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5019">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5019">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5020">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-5020">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-5021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-5021">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-5023">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-5025">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5027">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-5027">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-5028">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5028">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-5029">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5029">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-5030">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5030">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-5031">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-5031">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-5032">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-5032">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-5033">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-5033">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5035">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-5035">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-5036">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5036">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5037">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5037">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5038">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-5038">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-5039">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5039">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-5040">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5040">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5041">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5041">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5042">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-5042">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-5043">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-5043">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-5044">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5044">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-5045">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-5045">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-5046">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-5046">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-5047">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-5047">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-5048">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-5048">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-5049">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-5049">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5050">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-5050">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5051">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-5051">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5053">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5053">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5054">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5054">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5055">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-5055">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-5056">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-5056">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-5057">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5057">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-5058">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-5058">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-5059">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-5059">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5061">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5061">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-5062">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-5062">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-5063">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-5063">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-5064">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5064">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5066">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-5066">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-5067">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5067">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm-supfccsup-71"></a><span data-ttu-id="4845f-5069">DXGI_FORMAT_BC1 \_ UNORM <sup>FCC</sup> (71) </span><span class="sxs-lookup"><span data-stu-id="4845f-5069">DXGI_FORMAT_BC1\_UNORM <sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="4845f-5070">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5070">Target</span></span> | <span data-ttu-id="4845f-5071">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5071">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-5072">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-5072">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-5073">64</span><span class="sxs-lookup"><span data-stu-id="4845f-5073">64</span></span> |
| <span data-ttu-id="4845f-5074">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5074">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5076">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-5076">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5077">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5077">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5078">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5078">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5079">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5079">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5080">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-5080">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-5081">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-5081">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5083">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-5083">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5085">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-5085">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5087">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-5087">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5089">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5089">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5091">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5091">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-5092">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5092">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-5093">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-5093">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5095">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-5095">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-5096">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-5096">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5098">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-5098">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-5099">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5099">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5100">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5100">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5101">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-5101">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-5102">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5102">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-5103">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5103">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5104">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5104">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5105">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-5105">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-5106">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-5106">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-5107">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5107">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-5108">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-5108">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-5109">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-5109">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-5110">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-5110">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-5111">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-5111">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-5112">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-5112">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5113">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-5113">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5114">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-5114">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5116">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5116">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5117">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5117">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5118">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-5118">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-5119">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-5119">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-5120">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5120">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-5121">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-5121">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-5122">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-5122">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5124">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5124">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-5125">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-5125">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-5126">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-5126">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-5127">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5127">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5129">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-5129">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-5130">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5130">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm_srgb-supfccsup-72"></a><span data-ttu-id="4845f-5132">DXGI_FORMAT_BC1 \_ UNORM \_ SRGB <sup>FCC</sup> (72) </span><span class="sxs-lookup"><span data-stu-id="4845f-5132">DXGI_FORMAT_BC1\_UNORM\_SRGB <sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="4845f-5133">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5133">Target</span></span> | <span data-ttu-id="4845f-5134">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5134">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-5135">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-5135">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-5136">64</span><span class="sxs-lookup"><span data-stu-id="4845f-5136">64</span></span> |
| <span data-ttu-id="4845f-5137">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5137">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5139">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-5139">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5140">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5140">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5141">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5141">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5142">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5142">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5143">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-5143">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-5144">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-5144">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5146">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-5146">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5148">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-5148">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5150">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-5150">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5152">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5152">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5154">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5154">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-5155">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5155">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-5156">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-5156">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5158">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-5158">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-5159">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-5159">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5161">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-5161">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-5162">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5162">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5163">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5163">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5164">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-5164">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-5165">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5165">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-5166">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5166">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5167">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5167">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5168">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-5168">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-5169">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-5169">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-5170">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5170">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-5171">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-5171">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-5172">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-5172">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-5173">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-5173">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-5174">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-5174">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-5175">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-5175">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5176">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-5176">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5177">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-5177">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5179">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5179">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5180">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5180">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5181">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-5181">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-5182">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-5182">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-5183">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5183">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-5184">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-5184">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-5185">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-5185">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5187">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5187">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-5188">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-5188">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-5189">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-5189">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-5190">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5190">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5192">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-5192">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-5193">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5193">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="4845f-5195">DXGI_FORMAT_BC2 無別 \_ <sup>PCC</sup> (73) </span><span class="sxs-lookup"><span data-stu-id="4845f-5195">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="4845f-5196">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5196">Target</span></span> | <span data-ttu-id="4845f-5197">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5197">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-5198">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-5198">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-5199">128</span><span class="sxs-lookup"><span data-stu-id="4845f-5199">128</span></span> |
| <span data-ttu-id="4845f-5200">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5200">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5202">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-5202">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5203">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5203">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5204">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5204">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5205">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5205">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5206">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-5206">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-5207">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-5207">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5209">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-5209">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5211">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-5211">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5213">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-5213">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-5214">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5214">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-5215">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5215">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-5216">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5216">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-5217">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-5217">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-5218">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-5218">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-5219">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-5219">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5221">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-5221">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-5222">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5222">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5223">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5223">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5224">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-5224">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-5225">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5225">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-5226">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5226">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5227">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5227">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5228">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-5228">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-5229">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-5229">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-5230">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5230">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-5231">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-5231">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-5232">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-5232">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-5233">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-5233">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-5234">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-5234">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-5235">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-5235">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5236">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-5236">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5237">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-5237">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5239">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5239">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5240">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5240">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5241">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-5241">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-5242">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-5242">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-5243">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5243">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-5244">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-5244">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-5245">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-5245">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5247">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5247">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-5248">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-5248">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-5249">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-5249">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-5250">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5250">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5252">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-5252">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-5253">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5253">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm-supfccsup-74"></a><span data-ttu-id="4845f-5255">DXGI_FORMAT_BC2 \_ UNORM <sup>FCC</sup> (74) </span><span class="sxs-lookup"><span data-stu-id="4845f-5255">DXGI_FORMAT_BC2\_UNORM <sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="4845f-5256">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5256">Target</span></span> | <span data-ttu-id="4845f-5257">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5257">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-5258">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-5258">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-5259">128</span><span class="sxs-lookup"><span data-stu-id="4845f-5259">128</span></span> |
| <span data-ttu-id="4845f-5260">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5260">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5262">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-5262">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5263">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5263">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5264">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5264">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5265">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5265">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5266">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-5266">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-5267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-5267">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-5269">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5271">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-5271">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5273">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-5273">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5275">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5275">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5277">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5277">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-5278">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5278">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-5279">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-5279">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5281">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-5281">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-5282">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-5282">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5284">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-5284">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-5285">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5285">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5286">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5286">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5287">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-5287">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-5288">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5288">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-5289">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5289">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5290">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5290">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5291">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-5291">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-5292">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-5292">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-5293">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5293">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-5294">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-5294">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-5295">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-5295">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-5296">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-5296">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-5297">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-5297">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-5298">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-5298">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5299">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-5299">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5300">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-5300">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5302">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5302">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5303">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5303">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5304">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-5304">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-5305">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-5305">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-5306">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5306">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-5307">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-5307">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-5308">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-5308">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5310">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5310">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-5311">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-5311">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-5312">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-5312">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-5313">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5313">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5315">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-5315">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-5316">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5316">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm_srgb-supfccsup-75"></a><span data-ttu-id="4845f-5318">DXGI_FORMAT_BC2 \_ UNORM \_ SRGB <sup>FCC</sup> (75) </span><span class="sxs-lookup"><span data-stu-id="4845f-5318">DXGI_FORMAT_BC2\_UNORM\_SRGB <sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="4845f-5319">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5319">Target</span></span> | <span data-ttu-id="4845f-5320">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5320">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-5321">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-5321">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-5322">128</span><span class="sxs-lookup"><span data-stu-id="4845f-5322">128</span></span> |
| <span data-ttu-id="4845f-5323">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5323">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5325">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-5325">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5326">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5326">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5327">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5327">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5328">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5328">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5329">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-5329">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-5330">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-5330">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5332">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-5332">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5334">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-5334">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5336">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-5336">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5338">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5338">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5340">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5340">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-5341">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5341">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-5342">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-5342">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5344">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-5344">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-5345">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-5345">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5347">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-5347">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-5348">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5348">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5349">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5349">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5350">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-5350">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-5351">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5351">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-5352">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5352">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5353">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5353">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5354">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-5354">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-5355">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-5355">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-5356">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5356">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-5357">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-5357">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-5358">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-5358">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-5359">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-5359">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-5360">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-5360">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-5361">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-5361">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5362">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-5362">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5363">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-5363">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5365">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5365">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5366">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5366">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5367">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-5367">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-5368">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-5368">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-5369">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5369">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-5370">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-5370">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-5371">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-5371">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5373">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5373">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-5374">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-5374">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-5375">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-5375">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-5376">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5376">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5378">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-5378">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-5379">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5379">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="4845f-5381">DXGI_FORMAT_BC3 無別 \_ <sup>PCC</sup> (76) </span><span class="sxs-lookup"><span data-stu-id="4845f-5381">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="4845f-5382">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5382">Target</span></span> | <span data-ttu-id="4845f-5383">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5383">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-5384">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-5384">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-5385">128</span><span class="sxs-lookup"><span data-stu-id="4845f-5385">128</span></span> |
| <span data-ttu-id="4845f-5386">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5386">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5388">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-5388">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5389">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5389">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5390">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5390">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5391">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5391">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5392">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-5392">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-5393">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-5393">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5395">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-5395">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5397">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-5397">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5399">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-5399">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-5400">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-5401">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5401">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-5402">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5402">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-5403">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-5403">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-5404">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-5404">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-5405">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-5405">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5407">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-5407">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-5408">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5408">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5409">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5409">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5410">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-5410">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-5411">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5411">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-5412">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5412">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5413">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5413">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5414">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-5414">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-5415">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-5415">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-5416">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5416">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-5417">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-5417">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-5418">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-5418">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-5419">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-5419">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-5420">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-5420">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-5421">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-5421">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5422">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-5422">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5423">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-5423">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5425">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5425">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5426">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5426">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5427">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-5427">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-5428">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-5428">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-5429">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5429">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-5430">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-5430">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-5431">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-5431">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5433">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5433">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-5434">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-5434">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-5435">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-5435">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-5436">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5436">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5438">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-5438">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-5439">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5439">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm-supfccsup-77"></a><span data-ttu-id="4845f-5441">DXGI_FORMAT_BC3 \_ UNORM <sup>FCC</sup> (77) </span><span class="sxs-lookup"><span data-stu-id="4845f-5441">DXGI_FORMAT_BC3\_UNORM <sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="4845f-5442">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5442">Target</span></span> | <span data-ttu-id="4845f-5443">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5443">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-5444">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-5444">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-5445">128</span><span class="sxs-lookup"><span data-stu-id="4845f-5445">128</span></span> |
| <span data-ttu-id="4845f-5446">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5446">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5448">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-5448">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5449">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5449">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5450">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5450">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5451">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5451">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5452">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-5452">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-5453">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-5453">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5455">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-5455">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5457">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-5457">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5459">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-5459">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5461">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5461">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5463">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5463">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-5464">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5464">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-5465">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-5465">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5467">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-5467">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-5468">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-5468">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5470">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-5470">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-5471">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5471">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5472">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5472">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5473">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-5473">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-5474">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5474">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-5475">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5475">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5476">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5476">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5477">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-5477">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-5478">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-5478">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-5479">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5479">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-5480">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-5480">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-5481">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-5481">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-5482">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-5482">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-5483">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-5483">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-5484">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-5484">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5485">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-5485">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5486">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-5486">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5488">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5488">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5489">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5489">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5490">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-5490">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-5491">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-5491">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-5492">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5492">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-5493">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-5493">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-5494">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-5494">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5496">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5496">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-5497">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-5497">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-5498">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-5498">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-5499">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5499">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5501">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-5501">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-5502">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5502">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm_srgb-supfccsup-78"></a><span data-ttu-id="4845f-5504">DXGI_FORMAT_BC3 \_ UNORM \_ SRGB <sup>FCC</sup> (78) </span><span class="sxs-lookup"><span data-stu-id="4845f-5504">DXGI_FORMAT_BC3\_UNORM\_SRGB <sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="4845f-5505">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5505">Target</span></span> | <span data-ttu-id="4845f-5506">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5506">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-5507">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-5507">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-5508">128</span><span class="sxs-lookup"><span data-stu-id="4845f-5508">128</span></span> |
| <span data-ttu-id="4845f-5509">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5509">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5511">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-5511">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5512">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5512">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5513">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5513">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5514">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5514">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5515">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-5515">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-5516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-5516">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-5518">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-5520">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5522">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-5522">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5524">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5524">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5526">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5526">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-5527">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5527">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-5528">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-5528">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5530">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-5530">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-5531">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-5531">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5533">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-5533">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-5534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5534">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5535">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5535">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5536">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-5536">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-5537">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5537">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-5538">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5538">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5539">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5539">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5540">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-5540">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-5541">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-5541">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-5542">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5542">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-5543">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-5543">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-5544">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-5544">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-5545">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-5545">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-5546">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-5546">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-5547">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-5547">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5548">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-5548">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5549">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-5549">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5551">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5551">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5552">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5552">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5553">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-5553">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-5554">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-5554">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-5555">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5555">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-5556">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-5556">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-5557">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-5557">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5559">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5559">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-5560">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-5560">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-5561">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-5561">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-5562">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5562">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5564">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-5564">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-5565">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5565">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="4845f-5567">DXGI_FORMAT_BC4 無別 \_ <sup>PCC</sup> (79) </span><span class="sxs-lookup"><span data-stu-id="4845f-5567">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="4845f-5568">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5568">Target</span></span> | <span data-ttu-id="4845f-5569">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5569">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-5570">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-5570">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-5571">64</span><span class="sxs-lookup"><span data-stu-id="4845f-5571">64</span></span> |
| <span data-ttu-id="4845f-5572">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5572">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5574">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-5574">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5575">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5575">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5576">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5576">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5577">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5577">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5578">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-5578">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-5579">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-5579">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5581">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-5581">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5583">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-5583">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5585">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-5585">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-5586">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5586">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-5587">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5587">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-5588">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5588">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-5589">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-5589">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-5590">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-5590">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-5591">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-5591">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5593">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-5593">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-5594">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5594">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5595">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5595">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5596">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-5596">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-5597">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5597">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-5598">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5598">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5599">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5599">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5600">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-5600">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-5601">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-5601">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-5602">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5602">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-5603">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-5603">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-5604">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-5604">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-5605">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-5605">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-5606">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-5606">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-5607">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-5607">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5608">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-5608">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5609">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-5609">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5611">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5611">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5612">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5612">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5613">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-5613">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-5614">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-5614">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-5615">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5615">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-5616">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-5616">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-5617">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-5617">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5619">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5619">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-5620">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-5620">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-5621">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-5621">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-5622">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5622">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-5623">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-5623">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-5624">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5624">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_unorm-supfccsup-80"></a><span data-ttu-id="4845f-5626">DXGI_FORMAT_BC4 \_ UNORM <sup>FCC</sup> (80) </span><span class="sxs-lookup"><span data-stu-id="4845f-5626">DXGI_FORMAT_BC4\_UNORM <sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="4845f-5627">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5627">Target</span></span> | <span data-ttu-id="4845f-5628">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5628">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-5629">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-5629">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-5630">64</span><span class="sxs-lookup"><span data-stu-id="4845f-5630">64</span></span> |
| <span data-ttu-id="4845f-5631">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5631">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5633">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-5633">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5634">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5634">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5635">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5635">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5636">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5636">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5637">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-5637">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-5638">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-5638">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5640">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-5640">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5642">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-5642">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5644">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-5644">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5646">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5646">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5648">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5648">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-5649">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5649">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-5650">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-5650">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5652">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-5652">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-5653">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-5653">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5655">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-5655">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-5656">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5656">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5657">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5657">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5658">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-5658">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-5659">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5659">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-5660">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5660">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5661">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5661">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5662">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-5662">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-5663">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-5663">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-5664">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5664">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-5665">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-5665">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-5666">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-5666">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-5667">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-5667">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-5668">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-5668">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-5669">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-5669">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5670">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-5670">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5671">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-5671">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5673">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5673">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5674">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5674">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5675">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-5675">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-5676">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-5676">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-5677">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5677">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-5678">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-5678">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-5679">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-5679">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5681">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5681">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-5682">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-5682">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-5683">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-5683">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-5684">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5684">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-5685">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-5685">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-5686">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5686">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_snorm-supfccsup-81"></a><span data-ttu-id="4845f-5688">DXGI_FORMAT_BC4 \_ SNORM <sup>FCC</sup> (81) </span><span class="sxs-lookup"><span data-stu-id="4845f-5688">DXGI_FORMAT_BC4\_SNORM <sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="4845f-5689">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5689">Target</span></span> | <span data-ttu-id="4845f-5690">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5690">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-5691">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-5691">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-5692">64</span><span class="sxs-lookup"><span data-stu-id="4845f-5692">64</span></span> |
| <span data-ttu-id="4845f-5693">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5693">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5695">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-5695">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5696">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5696">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5697">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5697">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5698">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5698">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5699">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-5699">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-5700">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-5700">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5702">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-5702">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5704">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-5704">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5706">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-5706">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5708">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5708">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5710">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5710">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-5711">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5711">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-5712">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-5712">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5714">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-5714">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-5715">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-5715">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5717">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-5717">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-5718">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5718">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5719">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5719">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5720">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-5720">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-5721">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5721">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-5722">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5722">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5723">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5723">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5724">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-5724">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-5725">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-5725">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-5726">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5726">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-5727">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-5727">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-5728">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-5728">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-5729">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-5729">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-5730">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-5730">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-5731">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-5731">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5732">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-5732">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5733">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-5733">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5735">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5735">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5736">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5736">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5737">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-5737">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-5738">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-5738">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-5739">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5739">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-5740">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-5740">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-5741">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-5741">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5743">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5743">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-5744">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-5744">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-5745">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-5745">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-5746">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5746">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-5747">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-5747">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-5748">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5748">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="4845f-5750">DXGI_FORMAT_BC5 無別 \_ <sup>PCC</sup> (82) </span><span class="sxs-lookup"><span data-stu-id="4845f-5750">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="4845f-5751">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5751">Target</span></span> | <span data-ttu-id="4845f-5752">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5752">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-5753">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-5753">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-5754">128</span><span class="sxs-lookup"><span data-stu-id="4845f-5754">128</span></span> |
| <span data-ttu-id="4845f-5755">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5755">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5757">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-5757">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5758">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5758">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5759">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5760">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-5761">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-5762">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-5762">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5764">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-5764">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5766">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-5766">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5768">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-5768">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-5769">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5769">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-5770">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5770">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-5771">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5771">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-5772">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-5772">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-5773">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-5773">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-5774">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-5774">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5776">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-5776">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-5777">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5777">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5778">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5778">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5779">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-5779">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-5780">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5780">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-5781">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5781">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5782">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5782">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5783">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-5783">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-5784">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-5784">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-5785">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5785">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-5786">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-5786">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-5787">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-5787">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-5788">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-5788">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-5789">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-5789">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-5790">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-5790">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5791">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-5791">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5792">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-5792">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5794">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5794">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5795">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5795">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5796">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-5796">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-5797">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-5797">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-5798">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5798">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-5799">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-5799">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-5800">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-5800">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5802">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5802">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-5803">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-5803">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-5804">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-5804">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-5805">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5805">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-5806">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-5806">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-5807">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5807">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_unorm-supfccsup-83"></a><span data-ttu-id="4845f-5809">DXGI_FORMAT_BC5 \_ UNORM <sup>FCC</sup> (83) </span><span class="sxs-lookup"><span data-stu-id="4845f-5809">DXGI_FORMAT_BC5\_UNORM <sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="4845f-5810">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5810">Target</span></span> | <span data-ttu-id="4845f-5811">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5811">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-5812">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-5812">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-5813">128</span><span class="sxs-lookup"><span data-stu-id="4845f-5813">128</span></span> |
| <span data-ttu-id="4845f-5814">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5814">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5816">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-5816">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5817">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5817">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5818">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5818">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5819">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5819">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5820">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-5820">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-5821">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-5821">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5823">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-5823">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5825">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-5825">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5827">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-5827">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5829">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5829">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5831">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5831">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-5832">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5832">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-5833">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-5833">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5835">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-5835">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-5836">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-5836">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5838">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-5838">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-5839">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5839">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5840">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5841">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-5841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-5842">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5842">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-5843">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5843">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5844">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5844">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5845">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-5845">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-5846">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-5846">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-5847">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5847">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-5848">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-5848">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-5849">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-5849">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-5850">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-5850">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-5851">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-5851">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-5852">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-5852">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5853">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-5853">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5854">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-5854">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5856">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5856">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5857">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5857">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5858">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-5858">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-5859">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-5859">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-5860">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5860">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-5861">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-5861">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-5862">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-5862">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5864">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5864">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-5865">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-5865">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-5866">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-5866">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-5867">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5867">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-5868">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-5868">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-5869">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5869">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_snorm-supfccsup-84"></a><span data-ttu-id="4845f-5871">DXGI_FORMAT_BC5 \_ SNORM <sup>FCC</sup> (84) </span><span class="sxs-lookup"><span data-stu-id="4845f-5871">DXGI_FORMAT_BC5\_SNORM <sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="4845f-5872">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5872">Target</span></span> | <span data-ttu-id="4845f-5873">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5873">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-5874">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-5874">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-5875">128</span><span class="sxs-lookup"><span data-stu-id="4845f-5875">128</span></span> |
| <span data-ttu-id="4845f-5876">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5876">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5878">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-5878">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5879">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5879">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5880">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5880">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5881">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5881">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5882">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-5882">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-5883">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-5883">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5885">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-5885">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5887">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-5887">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5889">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-5889">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5891">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5891">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5893">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5893">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-5894">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5894">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-5895">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-5895">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5897">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-5897">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-5898">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-5898">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5900">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-5900">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-5901">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5901">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5902">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5902">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5903">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-5903">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-5904">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5904">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-5905">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5905">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5906">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5906">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5907">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-5907">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-5908">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-5908">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-5909">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5909">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-5910">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-5910">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-5911">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-5911">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-5912">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-5912">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-5913">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-5913">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-5914">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-5914">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5915">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-5915">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5916">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-5916">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5918">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5918">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5919">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5919">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-5920">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-5920">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-5921">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-5921">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-5922">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5922">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-5923">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-5923">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-5924">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-5924">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5926">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5926">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-5927">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-5927">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-5928">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-5928">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-5929">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5929">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-5930">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-5930">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-5931">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-5931">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="4845f-5933">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85) </span><span class="sxs-lookup"><span data-stu-id="4845f-5933">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="4845f-5934">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5934">Target</span></span> | <span data-ttu-id="4845f-5935">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5935">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-5936">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-5936">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-5937">16</span><span class="sxs-lookup"><span data-stu-id="4845f-5937">16</span></span> |
| <span data-ttu-id="4845f-5938">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-5938">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5940">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-5940">Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-5942">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5942">Input Assembler Vertex Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-5944">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5944">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5945">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-5945">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-5946">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-5946">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5948">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-5948">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5950">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-5950">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5952">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-5952">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5954">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-5954">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5956">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5956">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5958">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5958">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-5959">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-5959">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-5960">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-5960">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5962">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-5962">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-5963">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-5963">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5965">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-5965">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5967">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5967">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5969">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5969">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5971">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-5971">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-5972">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-5972">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-5973">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5973">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5974">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-5974">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-5975">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-5975">Typed UAV</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-5977">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-5977">UAV Typed Store</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-5979">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5979">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-5981">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-5981">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-5982">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-5982">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-5983">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-5983">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-5984">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-5984">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-5985">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-5985">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5986">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-5986">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-5987">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-5987">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5989">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5989">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5991">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-5991">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5993">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-5993">Other Multisample Count RT</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5995">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-5995">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5997">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-5997">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-5999">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-5999">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-6000">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-6000">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-6001">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6001">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-6002">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-6002">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-6003">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-6003">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-6004">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6004">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-6005">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-6005">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-6006">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6006">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="4845f-6008">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86) </span><span class="sxs-lookup"><span data-stu-id="4845f-6008">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="4845f-6009">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6009">Target</span></span> | <span data-ttu-id="4845f-6010">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6010">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-6011">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-6011">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-6012">16</span><span class="sxs-lookup"><span data-stu-id="4845f-6012">16</span></span> |
| <span data-ttu-id="4845f-6013">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6013">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6015">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-6015">Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6017">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6017">Input Assembler Vertex Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6019">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6019">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6020">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6020">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6021">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-6021">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6023">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-6023">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6025">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-6025">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6027">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-6027">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6029">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-6029">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6031">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6031">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6033">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6033">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-6034">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6034">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-6035">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-6035">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6037">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-6037">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-6038">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-6038">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6040">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-6040">Mipmap Auto-Generation</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6042">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6042">RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6044">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6044">Blendable RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6046">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-6046">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-6047">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6047">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-6048">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6048">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6049">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6049">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6050">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-6050">Typed UAV</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6052">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-6052">UAV Typed Store</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6054">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6054">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6056">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-6056">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-6057">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-6057">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-6058">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-6058">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-6059">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-6059">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-6060">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-6060">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6061">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-6061">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6062">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-6062">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6064">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6064">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6066">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6066">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6068">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-6068">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6070">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-6070">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6072">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6072">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6074">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-6074">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-6075">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-6075">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-6076">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6076">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-6077">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-6077">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-6078">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-6078">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-6079">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6079">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-6080">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-6080">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-6081">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6081">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="4845f-6083">DXGI_FORMAT_B8G8R8A8 無的 \_ <sup>電腦</sup> (90) </span><span class="sxs-lookup"><span data-stu-id="4845f-6083">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="4845f-6084">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6084">Target</span></span> | <span data-ttu-id="4845f-6085">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6085">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-6086">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-6086">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-6087">32</span><span class="sxs-lookup"><span data-stu-id="4845f-6087">32</span></span> |
| <span data-ttu-id="4845f-6088">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6088">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6090">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-6090">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6091">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6091">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6092">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6092">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6093">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6093">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6094">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-6094">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6096">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-6096">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6098">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-6098">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6100">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-6100">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6102">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-6102">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-6103">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6103">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-6104">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6104">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-6105">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6105">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-6106">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-6106">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-6107">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-6107">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-6108">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-6108">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6110">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-6110">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-6111">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6111">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6112">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6112">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6113">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-6113">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-6114">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6114">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-6115">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6115">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6116">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6116">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6117">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-6117">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-6118">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-6118">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-6119">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6119">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-6120">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-6120">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-6121">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-6121">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-6122">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-6122">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-6123">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-6123">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-6124">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-6124">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6125">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-6125">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6126">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-6126">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6128">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6128">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6129">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6129">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6130">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-6130">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-6131">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-6131">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-6132">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6132">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-6133">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-6133">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-6134">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-6134">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6136">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6136">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-6137">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-6137">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-6138">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-6138">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-6139">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6139">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6141">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-6141">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-6142">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6142">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="4845f-6144">DXGI_FORMAT_B8G8R8A8 \_ UNORM 的<sup>FCS</sup> (87) </span><span class="sxs-lookup"><span data-stu-id="4845f-6144">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="4845f-6145">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6145">Target</span></span> | <span data-ttu-id="4845f-6146">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6146">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-6147">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-6147">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-6148">32</span><span class="sxs-lookup"><span data-stu-id="4845f-6148">32</span></span> |
| <span data-ttu-id="4845f-6149">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6149">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6151">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-6151">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6153">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6153">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6155">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6155">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6156">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6156">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6157">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-6157">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6159">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-6159">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6161">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-6161">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-6163">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6165">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-6165">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6167">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6167">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6169">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6169">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-6170">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6170">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-6171">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-6171">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6173">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-6173">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-6174">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-6174">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6176">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-6176">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6178">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6178">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6180">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6180">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6182">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-6182">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-6183">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6183">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-6184">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6184">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6185">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6185">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6186">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-6186">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-6187">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-6187">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-6188">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6188">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-6189">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-6189">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-6190">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-6190">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-6191">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-6191">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-6192">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-6192">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-6193">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-6193">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6194">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-6194">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6195">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-6195">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6197">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6197">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6199">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6199">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6201">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-6201">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6203">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-6203">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6205">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6205">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6207">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-6207">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6209">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-6209">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6211">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6211">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-6212">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-6212">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6214">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-6214">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6216">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6216">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6218">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-6218">BackBuffer Castable Even Fully Typed</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6220">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6220">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="4845f-6222">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ SRGB<sup>FCS</sup> (91) </span><span class="sxs-lookup"><span data-stu-id="4845f-6222">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="4845f-6223">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6223">Target</span></span> | <span data-ttu-id="4845f-6224">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6224">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-6225">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-6225">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-6226">32</span><span class="sxs-lookup"><span data-stu-id="4845f-6226">32</span></span> |
| <span data-ttu-id="4845f-6227">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6227">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6229">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-6229">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6230">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6230">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6231">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6232">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-6233">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6235">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-6235">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6237">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-6237">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-6239">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6241">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-6241">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6243">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6243">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6245">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6245">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-6246">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6246">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-6247">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-6247">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6249">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-6249">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-6250">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-6250">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6252">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-6252">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6254">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6254">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6256">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6256">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6258">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-6258">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-6259">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6259">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-6260">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6260">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6261">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6261">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6262">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-6262">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-6263">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-6263">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-6264">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6264">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-6265">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-6265">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-6266">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-6266">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-6267">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-6267">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-6268">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-6268">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-6269">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-6269">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6270">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-6270">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6271">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-6271">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6273">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6273">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6275">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6275">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6277">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-6277">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6279">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-6279">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6281">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6281">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6283">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-6283">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6285">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-6285">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6287">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6287">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-6288">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-6288">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6290">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-6290">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6292">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6292">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6294">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-6294">BackBuffer Castable Even Fully Typed</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6296">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6296">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="4845f-6298">DXGI_FORMAT_B8G8R8X8 無的 \_ <sup>電腦</sup> (92) </span><span class="sxs-lookup"><span data-stu-id="4845f-6298">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="4845f-6299">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6299">Target</span></span> | <span data-ttu-id="4845f-6300">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6300">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-6301">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-6301">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-6302">32</span><span class="sxs-lookup"><span data-stu-id="4845f-6302">32</span></span> |
| <span data-ttu-id="4845f-6303">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6303">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6305">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-6305">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6306">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6306">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6307">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6307">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6308">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6308">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6309">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-6309">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6311">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-6311">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6313">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-6313">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6315">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-6315">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6317">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-6317">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-6318">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6318">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-6319">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6319">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-6320">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6320">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-6321">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-6321">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-6322">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-6322">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-6323">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-6323">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6325">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-6325">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-6326">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6326">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6327">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6327">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6328">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-6328">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-6329">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6329">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-6330">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6330">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6331">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6331">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6332">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-6332">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-6333">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-6333">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-6334">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6334">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-6335">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-6335">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-6336">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-6336">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-6337">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-6337">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-6338">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-6338">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-6339">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-6339">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6340">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-6340">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6341">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-6341">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6343">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6343">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6344">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6344">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6345">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-6345">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-6346">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-6346">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-6347">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6347">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-6348">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-6348">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-6349">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-6349">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6351">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6351">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-6352">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-6352">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-6353">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-6353">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-6354">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6354">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6356">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-6356">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-6357">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6357">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="4845f-6359">DXGI_FORMAT_B8G8R8X8 \_ UNORM 的<sup>FCS</sup> (88) </span><span class="sxs-lookup"><span data-stu-id="4845f-6359">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="4845f-6360">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6360">Target</span></span> | <span data-ttu-id="4845f-6361">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6361">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-6362">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-6362">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-6363">32</span><span class="sxs-lookup"><span data-stu-id="4845f-6363">32</span></span> |
| <span data-ttu-id="4845f-6364">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6364">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6366">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-6366">Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6368">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6368">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6370">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6370">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6371">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6371">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6372">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-6372">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6374">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-6374">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6376">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-6376">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6378">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-6378">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6380">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-6380">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6382">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6382">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6384">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6384">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-6385">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6385">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-6386">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-6386">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6388">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-6388">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-6389">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-6389">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6391">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-6391">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6393">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6393">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6395">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6395">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6397">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-6397">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-6398">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6398">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-6399">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6399">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6400">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6400">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6401">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-6401">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-6402">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-6402">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-6403">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6403">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-6404">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-6404">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-6405">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-6405">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-6406">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-6406">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-6407">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-6407">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-6408">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-6408">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6409">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-6409">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6410">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-6410">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6412">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6412">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6414">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6414">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6416">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-6416">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6418">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-6418">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6420">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6420">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6422">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-6422">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-6423">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-6423">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6425">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6425">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-6426">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-6426">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6428">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-6428">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6430">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6430">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6432">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-6432">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-6433">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6433">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="4845f-6435">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ SRGB<sup>FCS</sup> (93) </span><span class="sxs-lookup"><span data-stu-id="4845f-6435">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="4845f-6436">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6436">Target</span></span> | <span data-ttu-id="4845f-6437">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6437">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-6438">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-6438">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-6439">32</span><span class="sxs-lookup"><span data-stu-id="4845f-6439">32</span></span> |
| <span data-ttu-id="4845f-6440">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6440">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6442">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-6442">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6443">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6443">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6444">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6444">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6445">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6445">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6446">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-6446">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-6448">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6450">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-6450">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6452">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-6452">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6454">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-6454">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6456">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6456">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6458">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6458">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-6459">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6459">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-6460">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-6460">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6462">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-6462">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-6463">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-6463">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6465">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-6465">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6467">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6467">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6469">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6469">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6471">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-6471">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-6472">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6472">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-6473">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6473">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6474">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6474">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6475">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-6475">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-6476">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-6476">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-6477">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6477">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-6478">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-6478">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-6479">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-6479">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-6480">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-6480">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-6481">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-6481">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-6482">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-6482">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6483">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-6483">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6484">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-6484">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6486">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6486">4x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6488">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6488">8x Multisample RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6490">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-6490">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6492">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-6492">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6494">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6494">Multisample Load</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6496">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-6496">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-6497">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-6497">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6499">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6499">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-6500">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-6500">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-6501">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-6501">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-6502">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6502">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6504">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-6504">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-6505">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6505">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_typelesssuppccsup-94"></a><span data-ttu-id="4845f-6507">DXGI_FORMAT_BC6H 無別 \_ <sup>PCC</sup> (94) </span><span class="sxs-lookup"><span data-stu-id="4845f-6507">DXGI_FORMAT_BC6H\_TYPELESS<sup>PCC</sup> (94)</span></span>
| <span data-ttu-id="4845f-6508">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6508">Target</span></span> | <span data-ttu-id="4845f-6509">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6509">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-6510">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-6510">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-6511">128</span><span class="sxs-lookup"><span data-stu-id="4845f-6511">128</span></span> |
| <span data-ttu-id="4845f-6512">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6512">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6514">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-6514">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6515">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6515">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6516">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6516">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6517">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6517">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6518">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-6518">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-6519">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-6519">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6521">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-6521">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6523">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-6523">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6525">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-6525">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-6526">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6526">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-6527">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6527">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-6528">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6528">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-6529">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-6529">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-6530">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-6530">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-6531">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-6531">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6533">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-6533">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-6534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6534">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6535">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6535">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6536">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-6536">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-6537">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6537">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-6538">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6538">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6539">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6539">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6540">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-6540">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-6541">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-6541">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-6542">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6542">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-6543">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-6543">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-6544">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-6544">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-6545">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-6545">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-6546">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-6546">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-6547">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-6547">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6548">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-6548">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6549">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-6549">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6551">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6551">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6552">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6552">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6553">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-6553">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-6554">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-6554">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-6555">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6555">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-6556">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-6556">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-6557">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-6557">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6559">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6559">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-6560">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-6560">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-6561">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-6561">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-6562">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6562">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-6563">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-6563">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-6564">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6564">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_uf16-supfccsup-95"></a><span data-ttu-id="4845f-6566">DXGI_FORMAT_BC6H \_ UF16 <sup>FCC</sup> (95) </span><span class="sxs-lookup"><span data-stu-id="4845f-6566">DXGI_FORMAT_BC6H\_UF16 <sup>FCC</sup> (95)</span></span>
| <span data-ttu-id="4845f-6567">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6567">Target</span></span> | <span data-ttu-id="4845f-6568">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6568">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-6569">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-6569">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-6570">128</span><span class="sxs-lookup"><span data-stu-id="4845f-6570">128</span></span> |
| <span data-ttu-id="4845f-6571">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6571">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6573">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-6573">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6574">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6574">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6575">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6575">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6576">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6576">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6577">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-6577">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-6578">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-6578">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6580">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-6580">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6582">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-6582">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6584">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-6584">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6586">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6586">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6588">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6588">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-6589">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6589">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-6590">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-6590">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6592">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-6592">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-6593">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-6593">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6595">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-6595">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-6596">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6596">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6597">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6597">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6598">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-6598">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-6599">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6599">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-6600">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6600">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6601">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6601">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6602">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-6602">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-6603">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-6603">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-6604">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6604">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-6605">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-6605">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-6606">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-6606">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-6607">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-6607">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-6608">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-6608">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-6609">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-6609">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6610">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-6610">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6611">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-6611">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6613">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6613">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6614">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6614">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6615">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-6615">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-6616">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-6616">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-6617">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6617">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-6618">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-6618">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-6619">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-6619">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6621">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6621">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-6622">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-6622">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-6623">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-6623">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-6624">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6624">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-6625">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-6625">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-6626">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6626">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_sf16-supfccsup-96"></a><span data-ttu-id="4845f-6628">DXGI_FORMAT_BC6H \_ SF16 <sup>FCC</sup> (96) </span><span class="sxs-lookup"><span data-stu-id="4845f-6628">DXGI_FORMAT_BC6H\_SF16 <sup>FCC</sup> (96)</span></span>
| <span data-ttu-id="4845f-6629">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6629">Target</span></span> | <span data-ttu-id="4845f-6630">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6630">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-6631">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-6631">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-6632">128</span><span class="sxs-lookup"><span data-stu-id="4845f-6632">128</span></span> |
| <span data-ttu-id="4845f-6633">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6633">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6635">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-6635">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6636">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6636">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6637">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6637">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6638">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6638">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6639">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-6639">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-6640">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-6640">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6642">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-6642">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6644">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-6644">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6646">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-6646">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6648">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6648">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6650">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6650">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-6651">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6651">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-6652">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-6652">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6654">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-6654">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-6655">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-6655">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6657">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-6657">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-6658">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6658">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6659">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6659">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6660">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-6660">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-6661">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6661">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-6662">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6662">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6663">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6663">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6664">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-6664">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-6665">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-6665">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-6666">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6666">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-6667">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-6667">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-6668">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-6668">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-6669">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-6669">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-6670">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-6670">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-6671">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-6671">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6672">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-6672">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6673">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-6673">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6675">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6675">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6676">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6676">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6677">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-6677">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-6678">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-6678">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-6679">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6679">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-6680">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-6680">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-6681">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-6681">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6683">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6683">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-6684">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-6684">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-6685">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-6685">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-6686">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6686">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-6687">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-6687">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-6688">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6688">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_typelesssuppccsup-97"></a><span data-ttu-id="4845f-6690">DXGI_FORMAT_BC7 無別 \_ <sup>PCC</sup> (97) </span><span class="sxs-lookup"><span data-stu-id="4845f-6690">DXGI_FORMAT_BC7\_TYPELESS<sup>PCC</sup> (97)</span></span>
| <span data-ttu-id="4845f-6691">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6691">Target</span></span> | <span data-ttu-id="4845f-6692">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6692">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-6693">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-6693">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-6694">128</span><span class="sxs-lookup"><span data-stu-id="4845f-6694">128</span></span> |
| <span data-ttu-id="4845f-6695">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6695">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6697">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-6697">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6698">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6698">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6699">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6699">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6700">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6700">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6701">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-6701">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-6702">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-6702">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6704">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-6704">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6706">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-6706">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6708">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-6708">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-6709">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6709">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-6710">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6710">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-6711">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6711">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-6712">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-6712">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-6713">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-6713">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-6714">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-6714">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6716">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-6716">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-6717">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6717">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6718">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6718">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6719">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-6719">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-6720">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6720">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-6721">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6721">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6722">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6722">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6723">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-6723">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-6724">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-6724">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-6725">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6725">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-6726">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-6726">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-6727">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-6727">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-6728">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-6728">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-6729">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-6729">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-6730">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-6730">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6731">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-6731">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6732">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-6732">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6734">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6734">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6735">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6735">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6736">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-6736">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-6737">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-6737">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-6738">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6738">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-6739">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-6739">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-6740">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-6740">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6742">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6742">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-6743">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-6743">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-6744">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-6744">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-6745">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6745">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-6746">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-6746">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-6747">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6747">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm-supfccsup-98"></a><span data-ttu-id="4845f-6749">DXGI_FORMAT_BC7 \_ UNORM <sup>FCC</sup> (98) </span><span class="sxs-lookup"><span data-stu-id="4845f-6749">DXGI_FORMAT_BC7\_UNORM <sup>FCC</sup> (98)</span></span>
| <span data-ttu-id="4845f-6750">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6750">Target</span></span> | <span data-ttu-id="4845f-6751">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6751">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-6752">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-6752">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-6753">128</span><span class="sxs-lookup"><span data-stu-id="4845f-6753">128</span></span> |
| <span data-ttu-id="4845f-6754">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6754">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6756">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-6756">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6757">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6757">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6758">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6758">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6759">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6759">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6760">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-6760">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-6761">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-6761">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6763">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-6763">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6765">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-6765">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6767">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-6767">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6769">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6769">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6771">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6771">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-6772">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6772">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-6773">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-6773">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6775">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-6775">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-6776">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-6776">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6778">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-6778">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-6779">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6779">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6780">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6780">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6781">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-6781">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-6782">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6782">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-6783">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6783">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6784">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6784">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6785">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-6785">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-6786">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-6786">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-6787">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6787">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-6788">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-6788">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-6789">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-6789">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-6790">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-6790">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-6791">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-6791">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-6792">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-6792">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6793">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-6793">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6794">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-6794">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6796">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6796">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6797">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6797">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6798">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-6798">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-6799">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-6799">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-6800">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6800">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-6801">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-6801">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-6802">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-6802">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6804">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6804">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-6805">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-6805">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-6806">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-6806">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-6807">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6807">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-6808">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-6808">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-6809">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6809">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm_srgb-supfccsup-99"></a><span data-ttu-id="4845f-6811">DXGI_FORMAT_BC7 \_ UNORM \_ SRGB <sup>FCC</sup> (99) </span><span class="sxs-lookup"><span data-stu-id="4845f-6811">DXGI_FORMAT_BC7\_UNORM\_SRGB <sup>FCC</sup> (99)</span></span>
| <span data-ttu-id="4845f-6812">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6812">Target</span></span> | <span data-ttu-id="4845f-6813">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6813">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-6814">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-6814">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-6815">128</span><span class="sxs-lookup"><span data-stu-id="4845f-6815">128</span></span> |
| <span data-ttu-id="4845f-6816">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6816">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6818">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-6818">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6819">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6819">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6820">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6820">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6821">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6821">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6822">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-6822">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-6823">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-6823">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6825">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-6825">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-6827">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6829">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-6829">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6831">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6831">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6833">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6833">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-6834">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6834">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-6835">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-6835">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6837">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-6837">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-6838">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-6838">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6840">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-6840">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-6841">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6841">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6842">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6842">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6843">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-6843">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-6844">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6844">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-6845">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6845">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6846">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6846">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6847">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-6847">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-6848">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-6848">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-6849">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6849">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-6850">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-6850">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-6851">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-6851">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-6852">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-6852">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-6853">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-6853">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-6854">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-6854">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6855">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-6855">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6856">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-6856">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6858">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6858">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6859">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6859">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6860">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-6860">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-6861">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-6861">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-6862">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6862">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-6863">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-6863">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-6864">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-6864">Cast Within Bit Layout</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6866">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6866">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-6867">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-6867">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-6868">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-6868">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-6869">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6869">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-6870">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-6870">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-6871">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6871">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="4845f-6873">DXGI_FORMAT_AYUV<sup>V</sup> (100) </span><span class="sxs-lookup"><span data-stu-id="4845f-6873">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="4845f-6874">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6874">Target</span></span> | <span data-ttu-id="4845f-6875">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6875">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-6876">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-6876">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-6877">32</span><span class="sxs-lookup"><span data-stu-id="4845f-6877">32</span></span> |
| <span data-ttu-id="4845f-6878">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6878">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6880">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-6880">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6881">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6881">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6882">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6882">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6883">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6883">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6884">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-6884">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-6885">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-6885">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6887">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-6887">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-6888">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-6888">TextureCube</span></span> | \- |
| <span data-ttu-id="4845f-6889">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-6889">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6891">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6891">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6893">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6893">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-6894">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6894">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-6895">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-6895">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6897">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-6897">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-6898">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-6898">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6900">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-6900">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6902">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6902">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6904">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6904">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6906">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-6906">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-6907">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6907">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-6908">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6908">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6909">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6909">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6910">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-6910">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6912">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-6912">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6914">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6914">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-6915">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-6915">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-6916">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-6916">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-6917">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-6917">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-6918">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-6918">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-6919">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-6919">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6920">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-6920">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6921">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-6921">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6923">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6923">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6924">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6924">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6925">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-6925">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-6926">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-6926">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-6927">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6927">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-6928">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-6928">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-6929">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-6929">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-6930">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6930">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6932">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-6932">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6934">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-6934">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6936">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6936">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6938">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-6938">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-6939">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6939">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="4845f-6940">DXGI_FORMAT_Y410<sup>V</sup> (101) </span><span class="sxs-lookup"><span data-stu-id="4845f-6940">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="4845f-6941">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6941">Target</span></span> | <span data-ttu-id="4845f-6942">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6942">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-6943">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-6943">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-6944">32</span><span class="sxs-lookup"><span data-stu-id="4845f-6944">32</span></span> |
| <span data-ttu-id="4845f-6945">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6945">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6947">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-6947">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6948">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6948">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6949">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6949">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6950">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-6950">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-6951">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-6951">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-6952">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-6952">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6954">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-6954">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-6955">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-6955">TextureCube</span></span> | \- |
| <span data-ttu-id="4845f-6956">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-6956">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6958">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6958">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6960">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6960">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-6961">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-6961">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-6962">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-6962">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6964">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-6964">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-6965">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-6965">Mipmap</span></span> | \- |
| <span data-ttu-id="4845f-6966">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-6966">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-6967">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6967">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6968">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6968">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6969">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-6969">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-6970">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-6970">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-6971">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6971">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6972">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-6972">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-6973">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-6973">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6975">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-6975">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6977">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6977">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-6978">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-6978">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-6979">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-6979">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-6980">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-6980">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-6981">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-6981">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-6982">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-6982">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6983">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-6983">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-6984">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-6984">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-6986">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6986">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6987">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-6987">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-6988">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-6988">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-6989">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-6989">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-6990">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-6990">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-6991">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-6991">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-6992">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-6992">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-6993">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-6993">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6995">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-6995">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6997">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-6997">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-6999">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-6999">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7001">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-7001">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-7002">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7002">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="4845f-7003">DXGI_FORMAT_Y416<sup>V</sup> (102) </span><span class="sxs-lookup"><span data-stu-id="4845f-7003">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="4845f-7004">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7004">Target</span></span> | <span data-ttu-id="4845f-7005">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7005">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-7006">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-7006">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-7007">64</span><span class="sxs-lookup"><span data-stu-id="4845f-7007">64</span></span> |
| <span data-ttu-id="4845f-7008">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7008">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7010">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-7010">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7011">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7011">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7012">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7012">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7013">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7013">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7014">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-7014">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-7015">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-7015">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7017">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-7017">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-7018">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-7018">TextureCube</span></span> | \- |
| <span data-ttu-id="4845f-7019">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-7019">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7021">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7021">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7023">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7023">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-7024">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7024">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-7025">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-7025">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7027">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-7027">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-7028">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-7028">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7030">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-7030">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-7031">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7031">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7032">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7032">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7033">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-7033">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-7034">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7034">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-7035">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7035">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7036">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7036">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7037">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-7037">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7039">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-7039">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7041">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7041">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-7042">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-7042">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-7043">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-7043">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-7044">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-7044">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-7045">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-7045">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-7046">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-7046">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7047">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-7047">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7048">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-7048">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7050">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7050">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7051">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7051">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7052">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-7052">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-7053">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-7053">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-7054">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7054">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-7055">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-7055">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-7056">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-7056">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-7057">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7057">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7059">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-7059">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7061">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-7061">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7063">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7063">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7065">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-7065">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-7066">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7066">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="4845f-7067">DXGI_FORMAT_NV12<sup>V</sup> (103) </span><span class="sxs-lookup"><span data-stu-id="4845f-7067">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="4845f-7068">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7068">Target</span></span> | <span data-ttu-id="4845f-7069">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7069">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-7070">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-7070">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-7071">8</span><span class="sxs-lookup"><span data-stu-id="4845f-7071">8</span></span> |
| <span data-ttu-id="4845f-7072">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7072">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7074">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-7074">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7075">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7075">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7076">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7076">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7077">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7077">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7078">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-7078">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-7079">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-7079">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7081">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-7081">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-7082">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-7082">TextureCube</span></span> | \- |
| <span data-ttu-id="4845f-7083">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-7083">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7085">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7085">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7087">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7087">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-7088">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7088">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-7089">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-7089">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7091">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-7091">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-7092">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-7092">Mipmap</span></span> | \- |
| <span data-ttu-id="4845f-7093">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-7093">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-7094">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7094">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7096">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7096">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7098">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-7098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-7099">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-7100">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7101">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7102">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-7102">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7104">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-7104">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7106">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7106">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-7107">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-7107">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-7108">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-7108">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-7109">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-7109">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-7110">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-7110">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-7111">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-7111">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7112">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-7112">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7113">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-7113">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7115">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7115">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7116">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7116">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7117">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-7117">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-7118">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-7118">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-7119">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7119">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-7120">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-7120">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-7121">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-7121">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-7122">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7122">Video Decoder Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7124">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-7124">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7126">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-7126">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7128">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7128">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7130">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-7130">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-7131">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7131">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="4845f-7132">DXGI_FORMAT_P010<sup>V</sup> (104) </span><span class="sxs-lookup"><span data-stu-id="4845f-7132">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="4845f-7133">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7133">Target</span></span> | <span data-ttu-id="4845f-7134">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7134">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-7135">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-7135">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-7136">16</span><span class="sxs-lookup"><span data-stu-id="4845f-7136">16</span></span> |
| <span data-ttu-id="4845f-7137">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7137">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7139">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-7139">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7140">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7140">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7141">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7141">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7142">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7142">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7143">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-7143">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-7144">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-7144">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7146">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-7146">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-7147">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-7147">TextureCube</span></span> | \- |
| <span data-ttu-id="4845f-7148">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-7148">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7150">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7150">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7152">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7152">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-7153">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7153">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-7154">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-7154">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7156">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-7156">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-7157">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-7157">Mipmap</span></span> | \- |
| <span data-ttu-id="4845f-7158">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-7158">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-7159">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7159">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7161">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7161">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7163">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-7163">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-7164">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7164">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-7165">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7165">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7166">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7166">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7167">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-7167">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7169">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-7169">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7171">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-7172">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-7172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-7173">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-7173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-7174">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-7174">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-7175">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-7175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-7176">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-7176">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7177">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-7177">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7178">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-7178">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7180">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7180">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7181">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7181">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7182">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-7182">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-7183">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-7183">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-7184">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7184">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-7185">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-7185">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-7186">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-7186">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-7187">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7187">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7189">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-7189">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7191">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-7191">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7193">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7193">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7195">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-7195">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-7196">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7196">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="4845f-7197">DXGI_FORMAT_P016<sup>V</sup> (105) </span><span class="sxs-lookup"><span data-stu-id="4845f-7197">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="4845f-7198">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7198">Target</span></span> | <span data-ttu-id="4845f-7199">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7199">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-7200">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-7200">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-7201">16</span><span class="sxs-lookup"><span data-stu-id="4845f-7201">16</span></span> |
| <span data-ttu-id="4845f-7202">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7202">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7204">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-7204">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7205">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7205">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7206">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7206">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7207">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7207">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7208">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-7208">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-7209">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-7209">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7211">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-7211">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-7212">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-7212">TextureCube</span></span> | \- |
| <span data-ttu-id="4845f-7213">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-7213">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7215">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7215">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7217">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7217">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-7218">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7218">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-7219">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-7219">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7221">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-7221">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-7222">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-7222">Mipmap</span></span> | \- |
| <span data-ttu-id="4845f-7223">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-7223">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-7224">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7224">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7226">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7226">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7228">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-7228">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-7229">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7229">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-7230">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7230">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7231">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7231">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7232">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-7232">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7234">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-7234">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7236">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7236">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-7237">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-7237">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-7238">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-7238">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-7239">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-7239">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-7240">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-7240">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-7241">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-7241">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7242">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-7242">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7243">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-7243">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7245">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7245">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7246">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7246">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7247">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-7247">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-7248">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-7248">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-7249">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7249">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-7250">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-7250">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-7251">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-7251">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-7252">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7252">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7254">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-7254">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7256">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-7256">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7258">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7258">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7260">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-7260">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-7261">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7261">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="4845f-7262">DXGI_FORMAT_420 不 \_ 透明的<sup>V</sup> (106) </span><span class="sxs-lookup"><span data-stu-id="4845f-7262">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="4845f-7263">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7263">Target</span></span> | <span data-ttu-id="4845f-7264">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7264">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-7265">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-7265">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-7266">8</span><span class="sxs-lookup"><span data-stu-id="4845f-7266">8</span></span> |
| <span data-ttu-id="4845f-7267">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7267">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7269">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-7269">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7270">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7270">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7271">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7271">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7272">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7272">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7273">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-7273">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-7274">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-7274">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7276">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-7276">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-7277">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-7277">TextureCube</span></span> | \- |
| <span data-ttu-id="4845f-7278">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-7278">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-7279">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7279">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-7280">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7280">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-7281">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7281">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-7282">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-7282">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-7283">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-7283">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-7284">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-7284">Mipmap</span></span> | \- |
| <span data-ttu-id="4845f-7285">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-7285">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-7286">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7286">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7287">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7287">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7288">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-7288">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-7289">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7289">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-7290">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7290">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7291">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7291">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7292">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-7292">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-7293">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-7293">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-7294">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7294">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-7295">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-7295">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-7296">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-7296">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-7297">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-7297">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-7298">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-7298">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-7299">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-7299">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7300">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-7300">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7301">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-7301">CPU Lockable</span></span> | \- |
| <span data-ttu-id="4845f-7302">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7302">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7303">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7303">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7304">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-7304">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-7305">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-7305">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-7306">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7306">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-7307">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-7307">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-7308">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-7308">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-7309">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7309">Video Decoder Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7311">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-7311">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7313">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-7313">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7315">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7315">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7317">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-7317">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-7318">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7318">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="4845f-7319">DXGI_FORMAT_YUY2<sup>V</sup> (107) </span><span class="sxs-lookup"><span data-stu-id="4845f-7319">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="4845f-7320">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7320">Target</span></span> | <span data-ttu-id="4845f-7321">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7321">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-7322">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-7322">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-7323">16</span><span class="sxs-lookup"><span data-stu-id="4845f-7323">16</span></span> |
| <span data-ttu-id="4845f-7324">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7324">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7326">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-7326">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7327">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7327">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7328">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7328">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7329">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7329">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7330">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-7330">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-7331">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-7331">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7333">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-7333">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-7334">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-7334">TextureCube</span></span> | \- |
| <span data-ttu-id="4845f-7335">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-7335">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7337">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7337">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7339">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7339">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-7340">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7340">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-7341">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-7341">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7343">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-7343">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-7344">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-7344">Mipmap</span></span> | \- |
| <span data-ttu-id="4845f-7345">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-7345">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-7346">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7346">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7347">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7347">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7348">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-7348">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-7349">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7349">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-7350">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7350">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7351">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7351">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7352">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-7352">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7354">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-7354">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7356">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7356">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-7357">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-7357">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-7358">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-7358">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-7359">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-7359">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-7360">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-7360">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-7361">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-7361">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7362">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-7362">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7363">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-7363">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7365">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7365">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7366">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7366">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7367">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-7367">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-7368">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-7368">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-7369">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7369">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-7370">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-7370">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-7371">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-7371">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-7372">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7372">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7374">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-7374">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7376">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-7376">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7378">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7378">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7380">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-7380">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-7381">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7381">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="4845f-7382">DXGI_FORMAT_Y210<sup>V</sup> (108) </span><span class="sxs-lookup"><span data-stu-id="4845f-7382">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="4845f-7383">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7383">Target</span></span> | <span data-ttu-id="4845f-7384">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7384">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-7385">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-7385">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-7386">32</span><span class="sxs-lookup"><span data-stu-id="4845f-7386">32</span></span> |
| <span data-ttu-id="4845f-7387">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7387">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7389">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-7389">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7390">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7390">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7391">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7391">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7392">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7392">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7393">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-7393">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-7394">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-7394">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7396">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-7396">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-7397">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-7397">TextureCube</span></span> | \- |
| <span data-ttu-id="4845f-7398">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-7398">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7400">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7400">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7402">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7402">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-7403">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7403">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-7404">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-7404">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7406">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-7406">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-7407">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-7407">Mipmap</span></span> | \- |
| <span data-ttu-id="4845f-7408">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-7408">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-7409">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7409">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7410">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7410">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7411">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-7411">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-7412">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7412">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-7413">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7413">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7414">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7414">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7415">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-7415">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7417">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-7417">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7419">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7419">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-7420">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-7420">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-7421">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-7421">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-7422">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-7422">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-7423">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-7423">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-7424">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-7424">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7425">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-7425">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7426">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-7426">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7428">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7428">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7429">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7429">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7430">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-7430">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-7431">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-7431">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-7432">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7432">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-7433">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-7433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-7434">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-7434">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-7435">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7435">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7437">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-7437">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7439">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-7439">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7441">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7441">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7443">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-7443">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-7444">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7444">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="4845f-7445">DXGI_FORMAT_Y216<sup>V</sup> (109) </span><span class="sxs-lookup"><span data-stu-id="4845f-7445">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="4845f-7446">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7446">Target</span></span> | <span data-ttu-id="4845f-7447">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7447">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-7448">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-7448">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-7449">32</span><span class="sxs-lookup"><span data-stu-id="4845f-7449">32</span></span> |
| <span data-ttu-id="4845f-7450">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7450">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7452">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-7452">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7453">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7453">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7454">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7454">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7455">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7455">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7456">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-7456">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-7457">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-7457">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7459">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-7459">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-7460">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-7460">TextureCube</span></span> | \- |
| <span data-ttu-id="4845f-7461">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-7461">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7463">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7463">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7465">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7465">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-7466">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7466">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-7467">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-7467">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7469">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-7469">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-7470">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-7470">Mipmap</span></span> | \- |
| <span data-ttu-id="4845f-7471">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-7471">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-7472">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7472">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7473">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7473">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7474">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-7474">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-7475">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7475">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-7476">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7476">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7477">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7477">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7478">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-7478">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7480">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-7480">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7482">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7482">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-7483">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-7483">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-7484">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-7484">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-7485">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-7485">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-7486">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-7486">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-7487">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-7487">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7488">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-7488">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7489">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-7489">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7491">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7491">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7492">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7492">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7493">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-7493">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-7494">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-7494">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-7495">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7495">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-7496">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-7496">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-7497">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-7497">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-7498">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7498">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7500">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-7500">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7502">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-7502">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7504">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7504">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7506">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-7506">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-7507">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7507">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="4845f-7508">DXGI_FORMAT_NV11<sup>V</sup> (110) </span><span class="sxs-lookup"><span data-stu-id="4845f-7508">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="4845f-7509">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7509">Target</span></span> | <span data-ttu-id="4845f-7510">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7510">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-7511">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-7511">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-7512">8</span><span class="sxs-lookup"><span data-stu-id="4845f-7512">8</span></span> |
| <span data-ttu-id="4845f-7513">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7513">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7515">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-7515">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7516">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7516">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7517">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7517">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7518">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7518">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7519">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-7519">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-7520">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-7520">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7522">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-7522">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-7523">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-7523">TextureCube</span></span> | \- |
| <span data-ttu-id="4845f-7524">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-7524">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7526">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7526">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7528">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7528">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-7529">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7529">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-7530">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-7530">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7532">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-7532">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-7533">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-7533">Mipmap</span></span> | \- |
| <span data-ttu-id="4845f-7534">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-7534">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-7535">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7535">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7537">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7537">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7539">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-7539">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-7540">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7540">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-7541">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7541">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7542">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7542">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7543">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-7543">Typed UAV</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7545">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-7545">UAV Typed Store</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7547">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7547">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-7548">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-7548">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-7549">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-7549">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-7550">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-7550">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-7551">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-7551">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-7552">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-7552">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7553">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-7553">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7554">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-7554">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7556">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7556">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7557">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7557">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7558">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-7558">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-7559">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-7559">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-7560">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7560">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-7561">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-7561">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-7562">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-7562">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-7563">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7563">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7565">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-7565">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7567">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-7567">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7569">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7569">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7571">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-7571">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-7572">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7572">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="4845f-7573">DXGI_FORMAT_AI44<sup>V</sup> (111) </span><span class="sxs-lookup"><span data-stu-id="4845f-7573">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="4845f-7574">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7574">Target</span></span> | <span data-ttu-id="4845f-7575">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7575">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-7576">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-7576">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-7577">8</span><span class="sxs-lookup"><span data-stu-id="4845f-7577">8</span></span> |
| <span data-ttu-id="4845f-7578">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7578">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7580">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-7580">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7581">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7581">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7582">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7583">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7583">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7584">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-7584">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-7585">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-7585">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7587">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-7587">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-7588">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-7588">TextureCube</span></span> | \- |
| <span data-ttu-id="4845f-7589">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-7589">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-7590">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7590">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-7591">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7591">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-7592">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7592">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-7593">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-7593">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-7594">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-7594">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-7595">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-7595">Mipmap</span></span> | \- |
| <span data-ttu-id="4845f-7596">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-7596">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-7597">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7597">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7598">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7598">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7599">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-7599">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-7600">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7600">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-7601">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7601">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7602">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7602">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7603">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-7603">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-7604">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-7604">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-7605">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7605">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-7606">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-7606">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-7607">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-7607">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-7608">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-7608">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-7609">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-7609">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-7610">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-7610">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7611">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-7611">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7612">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-7612">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7614">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7614">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7615">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7615">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7616">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-7616">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-7617">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-7617">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-7618">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7618">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-7619">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-7619">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-7620">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-7620">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-7621">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7621">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-7622">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-7622">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7624">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-7624">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-7625">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7625">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-7626">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-7626">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-7627">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7627">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="4845f-7628">DXGI_FORMAT_IA44<sup>V</sup> (112) </span><span class="sxs-lookup"><span data-stu-id="4845f-7628">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="4845f-7629">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7629">Target</span></span> | <span data-ttu-id="4845f-7630">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7630">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-7631">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-7631">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-7632">8</span><span class="sxs-lookup"><span data-stu-id="4845f-7632">8</span></span> |
| <span data-ttu-id="4845f-7633">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7633">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7635">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-7635">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7636">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7636">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7637">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7637">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7638">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7638">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7639">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-7639">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-7640">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-7640">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7642">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-7642">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-7643">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-7643">TextureCube</span></span> | \- |
| <span data-ttu-id="4845f-7644">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-7644">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-7645">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7645">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-7646">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7646">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-7647">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7647">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-7648">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-7648">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-7649">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-7649">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-7650">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-7650">Mipmap</span></span> | \- |
| <span data-ttu-id="4845f-7651">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-7651">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-7652">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7652">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7653">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7653">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7654">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-7654">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-7655">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7655">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-7656">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7656">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7657">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7657">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7658">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-7658">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-7659">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-7659">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-7660">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7660">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-7661">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-7661">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-7662">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-7662">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-7663">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-7663">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-7664">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-7664">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-7665">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-7665">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7666">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-7666">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7667">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-7667">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7669">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7669">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7670">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7670">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7671">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-7671">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-7672">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-7672">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-7673">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7673">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-7674">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-7674">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-7675">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-7675">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-7676">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7676">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-7677">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-7677">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7679">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-7679">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-7680">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7680">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-7681">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-7681">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-7682">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7682">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="4845f-7683">DXGI_FORMAT_P8<sup>V</sup> (113) </span><span class="sxs-lookup"><span data-stu-id="4845f-7683">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="4845f-7684">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7684">Target</span></span> | <span data-ttu-id="4845f-7685">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7685">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-7686">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-7686">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-7687">8</span><span class="sxs-lookup"><span data-stu-id="4845f-7687">8</span></span> |
| <span data-ttu-id="4845f-7688">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7688">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7690">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-7690">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7691">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7691">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7692">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7692">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7693">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7693">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7694">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-7694">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-7695">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-7695">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7697">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-7697">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-7698">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-7698">TextureCube</span></span> | \- |
| <span data-ttu-id="4845f-7699">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-7699">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-7700">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7700">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-7701">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7701">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-7702">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7702">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-7703">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-7703">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-7704">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-7704">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-7705">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-7705">Mipmap</span></span> | \- |
| <span data-ttu-id="4845f-7706">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-7706">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-7707">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7707">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7708">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7708">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7709">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-7709">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-7710">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7710">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-7711">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7711">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7712">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7712">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7713">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-7713">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-7714">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-7714">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-7715">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7715">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-7716">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-7716">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-7717">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-7717">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-7718">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-7718">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-7719">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-7719">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-7720">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-7720">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7721">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-7721">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7722">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-7722">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7724">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7724">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7725">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7725">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7726">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-7726">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-7727">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-7727">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-7728">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7728">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-7729">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-7729">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-7730">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-7730">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-7731">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7731">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-7732">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-7732">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7734">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-7734">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-7735">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7735">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-7736">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-7736">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-7737">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7737">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="4845f-7738">DXGI_FORMAT_A8P8<sup>V</sup> (114) </span><span class="sxs-lookup"><span data-stu-id="4845f-7738">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="4845f-7739">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7739">Target</span></span> | <span data-ttu-id="4845f-7740">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7740">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-7741">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-7741">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-7742">16</span><span class="sxs-lookup"><span data-stu-id="4845f-7742">16</span></span> |
| <span data-ttu-id="4845f-7743">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7743">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7745">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-7745">Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7746">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7746">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7747">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7747">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7748">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7748">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7749">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-7749">Texture1D</span></span> | \- |
| <span data-ttu-id="4845f-7750">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-7750">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7752">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-7752">Texture3D</span></span> | \- |
| <span data-ttu-id="4845f-7753">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-7753">TextureCube</span></span> | \- |
| <span data-ttu-id="4845f-7754">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-7754">Shader ld</span></span> | \- |
| <span data-ttu-id="4845f-7755">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7755">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="4845f-7756">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7756">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-7757">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7757">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-7758">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-7758">Shader gather4</span></span> | \- |
| <span data-ttu-id="4845f-7759">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-7759">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-7760">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-7760">Mipmap</span></span> | \- |
| <span data-ttu-id="4845f-7761">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-7761">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="4845f-7762">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7762">RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7763">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7763">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7764">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-7764">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-7765">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7765">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-7766">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7766">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7767">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7767">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7768">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-7768">Typed UAV</span></span> | \- |
| <span data-ttu-id="4845f-7769">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-7769">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="4845f-7770">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7770">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="4845f-7771">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-7771">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-7772">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-7772">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-7773">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-7773">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-7774">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-7774">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-7775">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-7775">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7776">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-7776">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7777">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-7777">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7779">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7779">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7780">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7780">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="4845f-7781">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-7781">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="4845f-7782">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-7782">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="4845f-7783">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7783">Multisample Load</span></span> | \- |
| <span data-ttu-id="4845f-7784">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-7784">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-7785">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-7785">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-7786">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7786">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-7787">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-7787">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7789">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-7789">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-7790">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7790">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-7791">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-7791">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-7792">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7792">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="4845f-7793">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115) </span><span class="sxs-lookup"><span data-stu-id="4845f-7793">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="4845f-7794">目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7794">Target</span></span> | <span data-ttu-id="4845f-7795">支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7795">Support</span></span> |
| - | - |
| <span data-ttu-id="4845f-7796">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="4845f-7796">Bits Per Element (BPE)</span></span> | <span data-ttu-id="4845f-7797">16</span><span class="sxs-lookup"><span data-stu-id="4845f-7797">16</span></span> |
| <span data-ttu-id="4845f-7798">格式支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7798">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7800">Buffer</span><span class="sxs-lookup"><span data-stu-id="4845f-7800">Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7802">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7802">Input Assembler Vertex Buffer</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7804">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7804">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7805">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="4845f-7805">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="4845f-7806">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4845f-7806">Texture1D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7808">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4845f-7808">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7810">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4845f-7810">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7812">TextureCube</span><span class="sxs-lookup"><span data-stu-id="4845f-7812">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7814">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="4845f-7814">Shader ld</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7816">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7816">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7818">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7818">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="4845f-7819">著色器範例 (mono 1 \_ 位 \_ 篩選) </span><span class="sxs-lookup"><span data-stu-id="4845f-7819">Shader sample (mono 1\_bit\_filter)</span></span> | \- |
| <span data-ttu-id="4845f-7820">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="4845f-7820">Shader gather4</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7822">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="4845f-7822">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="4845f-7823">Mipmap</span><span class="sxs-lookup"><span data-stu-id="4845f-7823">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7825">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="4845f-7825">Mipmap Auto-Generation</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7827">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7827">RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7829">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7829">Blendable RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7831">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="4845f-7831">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="4845f-7832">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="4845f-7832">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="4845f-7833">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7833">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7834">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="4845f-7834">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="4845f-7835">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="4845f-7835">Typed UAV</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7837">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="4845f-7837">UAV Typed Store</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7839">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7839">UAV Typed Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7841">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="4845f-7841">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="4845f-7842">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="4845f-7842">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="4845f-7843">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="4845f-7843">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="4845f-7844">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="4845f-7844">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="4845f-7845">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="4845f-7845">UAV Atomic Signed Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7846">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="4845f-7846">UAV Atomic Unsigned Min/Max</span></span> | \- |
| <span data-ttu-id="4845f-7847">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="4845f-7847">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7849">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7849">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7851">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="4845f-7851">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7853">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="4845f-7853">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7855">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="4845f-7855">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="4845f-7857">多級載入</span><span class="sxs-lookup"><span data-stu-id="4845f-7857">Multisample Load</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="4845f-7859">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="4845f-7859">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="4845f-7860">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="4845f-7860">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="4845f-7861">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="4845f-7861">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="4845f-7862">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-7862">Video Processor Input</span></span> | \- |
| <span data-ttu-id="4845f-7863">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-7863">Video Processor Output</span></span> | \- |
| <span data-ttu-id="4845f-7864">共用資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7864">Shared Resource</span></span> | \- |
| <span data-ttu-id="4845f-7865">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="4845f-7865">BackBuffer Castable Even Fully Typed</span></span> | \- |
| <span data-ttu-id="4845f-7866">磚資源</span><span class="sxs-lookup"><span data-stu-id="4845f-7866">Tiled Resource</span></span> | ![必要](images/letter-r.jpg) |

## <a name="format-notes"></a><span data-ttu-id="4845f-7868">格式化附注</span><span class="sxs-lookup"><span data-stu-id="4845f-7868">Format notes</span></span>

<span data-ttu-id="4845f-7869">格式的用途可從一個硬體功能層級變更為下一個硬體功能層級。</span><span class="sxs-lookup"><span data-stu-id="4845f-7869">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="4845f-7870"><sup>L</sup> ：無格式的格式</span><span class="sxs-lookup"><span data-stu-id="4845f-7870"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="4845f-7871"><sup>電腦</sup> ：部分類型、可轉換和簡單版面配置</span><span class="sxs-lookup"><span data-stu-id="4845f-7871"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="4845f-7872"><sup>FCS</sup> ：完整型別、可轉換和 simple 版面配置</span><span class="sxs-lookup"><span data-stu-id="4845f-7872"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="4845f-7873"><sup>FNS</sup> ：完全具類型、非可轉換和簡單版面配置</span><span class="sxs-lookup"><span data-stu-id="4845f-7873"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="4845f-7874"><sup>PCC</sup> ：部分類型、可轉換和複雜版面配置</span><span class="sxs-lookup"><span data-stu-id="4845f-7874"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="4845f-7875"><sup>FCC</sup> ：完整型別、可轉換和複雜的版面配置</span><span class="sxs-lookup"><span data-stu-id="4845f-7875"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="4845f-7876"><sup>FNC</sup> ：完整型別、非可轉換和複雜的版面配置</span><span class="sxs-lookup"><span data-stu-id="4845f-7876"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="4845f-7877"><sup>V</sup> ：影片格式</span><span class="sxs-lookup"><span data-stu-id="4845f-7877"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="4845f-7878">相關主題</span><span class="sxs-lookup"><span data-stu-id="4845f-7878">Related topics</span></span>

[<span data-ttu-id="4845f-7879">D3D12 硬體功能等級</span><span class="sxs-lookup"><span data-stu-id="4845f-7879">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="4845f-7880">DXGI 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="4845f-7880">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
