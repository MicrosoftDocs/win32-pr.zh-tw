---
description: 本節指定 Direct3D Feature 10Level9 9.1 硬體支援的格式 ([ **DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)值) 。
ms.assetid: 770A5396-C5D9-442B-99FE-3D220C54E8EB
title: Direct3D 功能 10Level9 9.1 硬體的格式支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56653fd2fb504e3f23cfac13b432530ebaa7219b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846043"
---
# <a name="format-support-for-direct3d-feature-10level9-91-hardware"></a><span data-ttu-id="ccc12-103">Direct3D 功能 10Level9 9.1 硬體的格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-103">Format support for Direct3D Feature 10Level9 9.1 hardware</span></span>

<span data-ttu-id="ccc12-104">本節指定 Direct3D Feature 10Level9 9.1 硬體支援的格式 ([ _\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)值) 。</span><span class="sxs-lookup"><span data-stu-id="ccc12-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature 10Level9 9.1 hardware.</span></span>

<span data-ttu-id="ccc12-105">下表摘要說明使用下列索引鍵的功能支援。</span><span class="sxs-lookup"><span data-stu-id="ccc12-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="ccc12-106">符號</span><span class="sxs-lookup"><span data-stu-id="ccc12-106">Symbol</span></span>                            | <span data-ttu-id="ccc12-107">描述</span><span class="sxs-lookup"><span data-stu-id="ccc12-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="ccc12-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="ccc12-108">_ *-*\*</span></span>                             | <span data-ttu-id="ccc12-109">不允許或無法使用。</span><span class="sxs-lookup"><span data-stu-id="ccc12-109">Disallowed or not available.</span></span>                                                  |
| ![必要](images/letter-r.jpg)  | <span data-ttu-id="ccc12-111">需要硬體支援。</span><span class="sxs-lookup"><span data-stu-id="ccc12-111">Hardware support is required.</span></span>                                                 |
| ![選用](images/letter-o.jpg)  | <span data-ttu-id="ccc12-113">硬體支援是選擇性的，格式可能或可能不會有硬體加速。</span><span class="sxs-lookup"><span data-stu-id="ccc12-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![依賴](images/letter-d.jpg) | <span data-ttu-id="ccc12-115">如果支援相關的選擇性功能，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="ccc12-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="ccc12-116">本主題包含每一種格式的區段。</span><span class="sxs-lookup"><span data-stu-id="ccc12-116">This topic contains a section per format.</span></span> <span data-ttu-id="ccc12-117">格式 *目標* (資料表每個目標各包含一個資料列) 可以是資源類型、HLSL 內建函式，或是相依于特定格式的特定功能。</span><span class="sxs-lookup"><span data-stu-id="ccc12-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="ccc12-118">若要以程式設計方式驗證 D3D11 和 D3D12 中的格式支援，請參閱 [檢查硬體功能支援](checking-hardware-feature-support.md)。</span><span class="sxs-lookup"><span data-stu-id="ccc12-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="ccc12-119">這些格式的數目大多是（但不是全部），以遞增的數值順序來 &mdash; 看，有些會超出數值順序，並與其他相關的格式一起列出。</span><span class="sxs-lookup"><span data-stu-id="ccc12-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="ccc12-120">另請注意 *，格式名稱的無* 型別可以表示 *部分* 具型別，而不是嚴格的無型別 (請參閱主題結尾的 [格式附注](#format-notes) 章節) 。</span><span class="sxs-lookup"><span data-stu-id="ccc12-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

// 

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="ccc12-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0) </span><span class="sxs-lookup"><span data-stu-id="ccc12-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="ccc12-122">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-122">Target</span></span> | <span data-ttu-id="ccc12-123">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-123">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-124">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-125">0</span><span class="sxs-lookup"><span data-stu-id="ccc12-125">0</span></span> |
| <span data-ttu-id="ccc12-126">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-126">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-127">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-127">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-128">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-128">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-129">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-129">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-130">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-130">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-131">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-131">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-132">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-132">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-133">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-134">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-135">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-135">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-136">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-137">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-138">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-139">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-139">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-140">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-141">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-141">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-142">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-143">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-144">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-145">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-146">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-147">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-148">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-149">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-149">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-150">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-151">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-152">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-153">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-154">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-154">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-155">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-156">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-157">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-158">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-158">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-159">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-159">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-160">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-160">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-161">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-161">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-162">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-163">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-163">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-164">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-165">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-166">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-167">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-168">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-169">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-169">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-170">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="ccc12-171">DXGI_FORMAT_R32G32B32A32 無的 \_ <sup>電腦</sup> (1) </span><span class="sxs-lookup"><span data-stu-id="ccc12-171">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="ccc12-172">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-172">Target</span></span> | <span data-ttu-id="ccc12-173">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-173">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-174">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-175">128</span><span class="sxs-lookup"><span data-stu-id="ccc12-175">128</span></span> |
| <span data-ttu-id="ccc12-176">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-176">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-177">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-177">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-178">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-178">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-179">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-179">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-180">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-180">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-181">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-181">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-182">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-182">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-183">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-184">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-185">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-185">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-186">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-186">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-187">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-187">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-188">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-188">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-189">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-189">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-190">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-190">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-191">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-191">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-192">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-192">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-193">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-193">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-194">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-194">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-195">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-195">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-196">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-196">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-197">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-197">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-198">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-198">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-199">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-199">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-200">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-200">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-201">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-201">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-202">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-202">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-203">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-203">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-204">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-204">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-205">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-205">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-206">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-206">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-207">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-207">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-208">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-208">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-209">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-209">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-210">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-210">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-211">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-211">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-212">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-212">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-213">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-213">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-214">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-214">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-215">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-215">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-216">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-216">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-217">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-217">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-218">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-218">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-219">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-219">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-220">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-220">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a><span data-ttu-id="ccc12-221">DXGI_FORMAT_R32G32B32A32 \_ FLOAT<sup>FNS</sup> (2) </span><span class="sxs-lookup"><span data-stu-id="ccc12-221">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FNS</sup> (2)</span></span>
| <span data-ttu-id="ccc12-222">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-222">Target</span></span> | <span data-ttu-id="ccc12-223">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-223">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-224">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-224">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-225">128</span><span class="sxs-lookup"><span data-stu-id="ccc12-225">128</span></span> |
| <span data-ttu-id="ccc12-226">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-226">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-228">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-228">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-229">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-229">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-231">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-232">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-233">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-234">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-234">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-235">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-235">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-236">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-236">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-237">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-237">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-238">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-238">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-239">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-239">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-240">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-240">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-241">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-241">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-242">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-242">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-243">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-243">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-244">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-244">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-245">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-245">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-246">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-246">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-247">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-247">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-248">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-248">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-249">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-249">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-250">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-250">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-251">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-251">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-252">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-252">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-253">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-253">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-254">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-254">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-255">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-255">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-256">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-256">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-257">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-257">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-258">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-258">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-259">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-259">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-260">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-260">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-261">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-261">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-262">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-262">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-263">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-263">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-264">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-264">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-265">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-265">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-266">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-266">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-267">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-267">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-268">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-268">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-269">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-269">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-270">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-270">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-271">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-271">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-272">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-272">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a><span data-ttu-id="ccc12-273">DXGI_FORMAT_R32G32B32A32 \_ UINT<sup>FNS</sup> (3) </span><span class="sxs-lookup"><span data-stu-id="ccc12-273">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FNS</sup> (3)</span></span>
| <span data-ttu-id="ccc12-274">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-274">Target</span></span> | <span data-ttu-id="ccc12-275">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-275">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-276">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-276">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-277">128</span><span class="sxs-lookup"><span data-stu-id="ccc12-277">128</span></span> |
| <span data-ttu-id="ccc12-278">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-278">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-279">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-279">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-280">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-281">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-282">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-283">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-284">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-284">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-285">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-285">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-286">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-286">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-287">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-287">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-288">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-288">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-289">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-289">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-290">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-290">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-291">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-291">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-292">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-292">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-293">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-293">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-294">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-294">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-295">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-295">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-296">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-296">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-297">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-297">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-298">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-298">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-299">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-299">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-300">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-300">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-301">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-301">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-302">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-302">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-303">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-303">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-304">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-304">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-305">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-305">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-306">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-306">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-307">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-307">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-308">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-308">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-309">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-309">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-310">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-310">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-311">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-311">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-312">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-312">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-313">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-313">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-314">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-314">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-315">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-315">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-316">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-316">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-317">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-317">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-318">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-318">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-319">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-319">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-320">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-320">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-321">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-321">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-322">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-322">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a><span data-ttu-id="ccc12-323">DXGI_FORMAT_R32G32B32A32 \_ 聖<sup>FNS</sup> (4) </span><span class="sxs-lookup"><span data-stu-id="ccc12-323">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FNS</sup> (4)</span></span>
| <span data-ttu-id="ccc12-324">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-324">Target</span></span> | <span data-ttu-id="ccc12-325">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-325">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-326">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-326">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-327">128</span><span class="sxs-lookup"><span data-stu-id="ccc12-327">128</span></span> |
| <span data-ttu-id="ccc12-328">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-328">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-329">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-329">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-330">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-330">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-331">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-331">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-332">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-332">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-333">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-333">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-334">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-335">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-335">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-336">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-336">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-337">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-337">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-338">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-338">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-339">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-339">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-340">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-340">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-341">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-341">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-342">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-342">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-343">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-343">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-344">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-344">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-345">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-345">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-346">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-346">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-347">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-347">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-348">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-348">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-349">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-349">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-350">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-350">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-351">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-351">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-352">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-352">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-353">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-353">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-354">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-354">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-355">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-355">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-356">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-356">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-357">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-357">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-358">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-358">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-359">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-359">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-360">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-360">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-361">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-361">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-362">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-362">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-363">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-363">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-364">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-364">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-365">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-365">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-366">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-366">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-367">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-367">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-368">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-369">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-370">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-371">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-371">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-372">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-372">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="ccc12-373">DXGI_FORMAT_R32G32B32 無的 \_ <sup>電腦</sup> (5) </span><span class="sxs-lookup"><span data-stu-id="ccc12-373">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="ccc12-374">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-374">Target</span></span> | <span data-ttu-id="ccc12-375">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-375">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-376">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-376">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-377">96</span><span class="sxs-lookup"><span data-stu-id="ccc12-377">96</span></span> |
| <span data-ttu-id="ccc12-378">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-378">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-379">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-379">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-380">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-380">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-381">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-381">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-382">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-382">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-383">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-383">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-384">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-384">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-385">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-385">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-386">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-386">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-387">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-387">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-388">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-388">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-389">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-389">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-390">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-390">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-391">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-391">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-392">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-392">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-393">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-393">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-394">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-394">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-395">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-395">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-396">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-396">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-397">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-397">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-398">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-398">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-399">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-399">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-400">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-400">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-401">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-401">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-402">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-402">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-403">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-403">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-404">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-404">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-405">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-405">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-406">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-406">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-407">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-407">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-408">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-408">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-409">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-409">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-410">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-410">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-411">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-411">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-412">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-412">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-413">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-413">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-414">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-414">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-415">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-415">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-416">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-416">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-417">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-417">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-418">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-418">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-419">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-419">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-420">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-420">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-421">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-421">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-422">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-422">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a><span data-ttu-id="ccc12-423">DXGI_FORMAT_R32G32B32 \_ FLOAT<sup>FNS</sup> (6) </span><span class="sxs-lookup"><span data-stu-id="ccc12-423">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FNS</sup> (6)</span></span>
| <span data-ttu-id="ccc12-424">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-424">Target</span></span> | <span data-ttu-id="ccc12-425">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-425">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-426">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-426">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-427">96</span><span class="sxs-lookup"><span data-stu-id="ccc12-427">96</span></span> |
| <span data-ttu-id="ccc12-428">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-428">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-430">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-430">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-431">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-431">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-433">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-433">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-434">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-434">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-435">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-435">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-436">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-436">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-437">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-437">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-438">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-438">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-439">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-439">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-440">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-441">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-442">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-443">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-443">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-444">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-445">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-445">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-446">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-446">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-447">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-447">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-448">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-448">Blendable RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="ccc12-450">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-450">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-451">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-451">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-452">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-452">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-453">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-453">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-454">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-454">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-455">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-455">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-456">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-456">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-457">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-457">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-458">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-458">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-459">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-459">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-460">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-460">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-461">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-461">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-462">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-462">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-463">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-463">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-464">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-464">4x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="ccc12-466">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-466">8x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="ccc12-468">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-468">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-469">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-469">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-470">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-470">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-471">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-471">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-472">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-472">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-473">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-473">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-474">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-474">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-475">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-475">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-476">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-476">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-477">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-477">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a><span data-ttu-id="ccc12-478">DXGI_FORMAT_R32G32B32 \_ UINT<sup>FNS</sup> (7) </span><span class="sxs-lookup"><span data-stu-id="ccc12-478">DXGI_FORMAT_R32G32B32\_UINT<sup>FNS</sup> (7)</span></span>
| <span data-ttu-id="ccc12-479">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-479">Target</span></span> | <span data-ttu-id="ccc12-480">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-480">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-481">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-481">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-482">96</span><span class="sxs-lookup"><span data-stu-id="ccc12-482">96</span></span> |
| <span data-ttu-id="ccc12-483">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-483">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-484">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-484">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-485">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-485">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-486">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-486">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-487">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-487">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-488">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-488">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-489">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-489">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-490">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-490">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-491">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-491">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-492">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-492">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-493">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-493">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-494">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-494">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-495">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-495">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-496">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-496">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-497">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-497">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-498">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-498">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-499">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-499">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-500">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-500">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-501">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-501">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-502">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-502">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-503">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-503">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-504">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-504">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-505">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-505">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-506">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-506">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-507">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-507">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-508">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-508">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-509">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-509">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-510">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-510">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-511">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-511">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-512">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-512">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-513">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-513">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-514">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-514">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-515">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-515">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-516">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-516">4x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="ccc12-518">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-518">8x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="ccc12-520">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-520">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-521">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-521">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-522">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-522">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-523">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-523">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-524">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-524">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-525">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-525">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-526">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-526">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-527">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-527">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-528">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-528">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-529">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-529">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a><span data-ttu-id="ccc12-530">DXGI_FORMAT_R32G32B32 \_ 聖<sup>FNS</sup> (8) </span><span class="sxs-lookup"><span data-stu-id="ccc12-530">DXGI_FORMAT_R32G32B32\_SINT<sup>FNS</sup> (8)</span></span>
| <span data-ttu-id="ccc12-531">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-531">Target</span></span> | <span data-ttu-id="ccc12-532">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-532">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-533">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-533">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-534">96</span><span class="sxs-lookup"><span data-stu-id="ccc12-534">96</span></span> |
| <span data-ttu-id="ccc12-535">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-535">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-536">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-536">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-537">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-537">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-538">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-538">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-539">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-539">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-540">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-540">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-541">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-541">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-542">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-542">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-543">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-543">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-544">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-544">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-545">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-545">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-546">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-546">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-547">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-547">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-548">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-548">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-549">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-549">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-550">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-550">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-551">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-551">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-552">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-552">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-553">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-553">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-554">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-554">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-555">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-555">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-556">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-556">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-557">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-557">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-558">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-558">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-559">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-559">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-560">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-560">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-561">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-561">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-562">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-562">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-563">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-563">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-564">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-564">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-565">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-565">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-566">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-566">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-567">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-567">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-568">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-568">4x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="ccc12-570">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-570">8x Multisample RenderTarget</span></span> | ![依賴](images/letter-d.jpg) |
| <span data-ttu-id="ccc12-572">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-572">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-573">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-573">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-574">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-574">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-575">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-575">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-576">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-576">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-577">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-577">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-578">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-578">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-579">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-579">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-580">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-580">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-581">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-581">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="ccc12-582">DXGI_FORMAT_R16G16B16A16 無別 \_ <sup>電腦</sup> (9) </span><span class="sxs-lookup"><span data-stu-id="ccc12-582">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="ccc12-583">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-583">Target</span></span> | <span data-ttu-id="ccc12-584">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-584">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-585">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-585">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-586">64</span><span class="sxs-lookup"><span data-stu-id="ccc12-586">64</span></span> |
| <span data-ttu-id="ccc12-587">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-587">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-588">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-588">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-589">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-589">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-590">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-590">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-591">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-591">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-592">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-592">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-593">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-593">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-594">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-594">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-595">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-595">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-596">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-596">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-597">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-597">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-598">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-598">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-599">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-599">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-600">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-600">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-601">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-601">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-602">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-602">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-603">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-603">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-604">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-604">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-605">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-606">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-606">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-607">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-607">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-608">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-608">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-609">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-609">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-610">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-610">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-611">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-611">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-612">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-612">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-613">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-613">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-614">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-614">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-615">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-615">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-616">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-616">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-617">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-617">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-618">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-618">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-619">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-619">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-620">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-620">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-621">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-621">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-622">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-622">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-623">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-623">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-624">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-624">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-625">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-625">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-626">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-626">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-627">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-627">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-628">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-628">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-629">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-629">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-630">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-630">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-631">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-631">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a><span data-ttu-id="ccc12-632">DXGI_FORMAT_R16G16B16A16 \_ FLOAT<sup>FNS</sup> (10) </span><span class="sxs-lookup"><span data-stu-id="ccc12-632">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FNS</sup> (10)</span></span>
| <span data-ttu-id="ccc12-633">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-633">Target</span></span> | <span data-ttu-id="ccc12-634">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-634">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-635">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-635">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-636">64</span><span class="sxs-lookup"><span data-stu-id="ccc12-636">64</span></span> |
| <span data-ttu-id="ccc12-637">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-637">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-638">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-638">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-639">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-639">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-640">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-640">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-641">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-641">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-642">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-642">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-643">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-643">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-644">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-644">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-645">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-645">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-646">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-646">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-647">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-647">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-648">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-648">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-649">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-649">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-650">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-650">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-651">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-651">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-652">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-652">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-653">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-653">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-654">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-654">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-655">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-655">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-656">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-656">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-657">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-657">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-658">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-658">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-659">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-659">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-660">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-660">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-661">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-661">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-662">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-662">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-663">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-663">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-664">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-664">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-665">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-665">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-666">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-666">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-667">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-667">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-668">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-668">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-669">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-669">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-670">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-670">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-671">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-671">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-672">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-672">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-673">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-673">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-674">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-674">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-675">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-675">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-676">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-676">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-677">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-677">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-678">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-678">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-679">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-679">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-680">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-680">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-682">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-682">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a><span data-ttu-id="ccc12-683">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FNS</sup> (11) </span><span class="sxs-lookup"><span data-stu-id="ccc12-683">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FNS</sup> (11)</span></span>
| <span data-ttu-id="ccc12-684">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-684">Target</span></span> | <span data-ttu-id="ccc12-685">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-685">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-686">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-686">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-687">64</span><span class="sxs-lookup"><span data-stu-id="ccc12-687">64</span></span> |
| <span data-ttu-id="ccc12-688">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-688">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-689">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-689">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-690">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-690">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-691">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-691">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-692">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-692">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-693">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-693">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-694">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-694">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-695">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-695">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-696">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-696">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-697">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-697">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-698">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-698">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-699">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-699">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-700">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-700">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-701">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-701">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-702">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-702">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-703">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-703">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-704">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-704">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-705">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-705">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-706">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-706">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-707">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-707">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-708">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-708">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-709">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-709">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-710">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-710">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-711">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-711">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-712">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-712">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-713">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-713">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-714">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-714">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-715">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-715">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-716">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-716">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-717">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-717">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-718">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-718">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-719">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-719">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-720">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-720">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-721">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-721">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-722">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-722">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-723">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-723">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-724">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-724">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-725">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-725">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-726">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-726">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-727">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-727">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-728">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-728">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-729">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-729">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-730">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-730">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-731">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-731">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-732">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-732">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a><span data-ttu-id="ccc12-733">DXGI_FORMAT_R16G16B16A16 \_ UINT<sup>FNS</sup> (12) </span><span class="sxs-lookup"><span data-stu-id="ccc12-733">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FNS</sup> (12)</span></span>
| <span data-ttu-id="ccc12-734">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-734">Target</span></span> | <span data-ttu-id="ccc12-735">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-735">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-736">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-736">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-737">64</span><span class="sxs-lookup"><span data-stu-id="ccc12-737">64</span></span> |
| <span data-ttu-id="ccc12-738">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-738">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-739">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-739">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-740">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-740">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-741">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-741">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-742">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-742">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-743">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-743">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-744">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-744">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-745">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-745">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-746">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-746">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-747">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-747">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-748">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-748">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-749">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-749">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-750">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-750">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-751">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-751">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-752">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-752">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-753">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-753">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-754">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-754">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-755">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-755">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-756">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-756">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-757">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-757">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-758">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-758">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-759">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-759">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-760">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-760">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-761">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-761">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-762">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-762">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-763">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-763">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-764">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-764">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-765">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-765">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-766">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-766">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-767">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-767">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-768">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-768">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-769">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-769">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-770">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-770">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-771">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-771">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-772">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-772">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-773">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-773">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-774">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-774">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-775">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-775">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-776">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-776">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-777">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-777">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-778">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-778">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-779">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-779">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-780">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-780">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-781">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-781">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-782">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a><span data-ttu-id="ccc12-783">DXGI_FORMAT_R16G16B16A16 \_ SNORM<sup>FNS</sup> (13) </span><span class="sxs-lookup"><span data-stu-id="ccc12-783">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FNS</sup> (13)</span></span>
| <span data-ttu-id="ccc12-784">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-784">Target</span></span> | <span data-ttu-id="ccc12-785">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-785">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-786">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-787">64</span><span class="sxs-lookup"><span data-stu-id="ccc12-787">64</span></span> |
| <span data-ttu-id="ccc12-788">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-788">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-790">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-790">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-791">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-791">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-793">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-793">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-794">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-794">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-795">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-795">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-796">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-796">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-797">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-798">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-798">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-799">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-799">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-800">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-800">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-801">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-801">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-802">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-802">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-803">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-803">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-804">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-804">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-805">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-805">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-806">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-806">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-807">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-807">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-808">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-808">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-809">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-809">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-810">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-810">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-811">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-811">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-812">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-812">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-813">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-813">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-814">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-814">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-815">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-815">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-816">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-816">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-817">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-817">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-818">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-818">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-819">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-819">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-820">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-820">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-821">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-821">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-822">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-822">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-823">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-823">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-824">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-824">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-825">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-825">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-826">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-826">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-827">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-827">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-828">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-828">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-829">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-829">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-830">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-830">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-831">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-831">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-832">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-832">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-833">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-833">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-834">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-834">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a><span data-ttu-id="ccc12-835">DXGI_FORMAT_R16G16B16A16 \_ 聖<sup>FNS</sup> (14) </span><span class="sxs-lookup"><span data-stu-id="ccc12-835">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FNS</sup> (14)</span></span>
| <span data-ttu-id="ccc12-836">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-836">Target</span></span> | <span data-ttu-id="ccc12-837">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-837">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-838">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-838">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-839">64</span><span class="sxs-lookup"><span data-stu-id="ccc12-839">64</span></span> |
| <span data-ttu-id="ccc12-840">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-840">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-842">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-842">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-843">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-843">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-845">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-845">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-846">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-846">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-847">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-847">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-848">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-848">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-849">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-849">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-850">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-850">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-851">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-851">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-852">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-852">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-853">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-853">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-854">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-854">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-855">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-855">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-856">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-856">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-857">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-857">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-858">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-858">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-859">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-859">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-860">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-860">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-861">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-861">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-862">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-862">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-863">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-863">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-864">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-864">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-865">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-865">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-866">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-866">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-867">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-867">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-868">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-868">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-869">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-869">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-870">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-870">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-871">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-871">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-872">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-872">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-873">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-873">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-874">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-874">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-875">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-875">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-876">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-876">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-877">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-877">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-878">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-878">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-879">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-879">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-880">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-880">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-881">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-881">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-882">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-882">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-883">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-883">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-884">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-884">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-885">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-885">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-886">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-886">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="ccc12-887">DXGI_FORMAT_R32G32 無別 \_ <sup>電腦</sup> (15) </span><span class="sxs-lookup"><span data-stu-id="ccc12-887">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="ccc12-888">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-888">Target</span></span> | <span data-ttu-id="ccc12-889">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-889">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-890">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-890">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-891">64</span><span class="sxs-lookup"><span data-stu-id="ccc12-891">64</span></span> |
| <span data-ttu-id="ccc12-892">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-892">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-893">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-893">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-894">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-894">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-895">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-895">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-896">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-896">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-897">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-897">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-898">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-898">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-899">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-899">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-900">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-900">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-901">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-901">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-902">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-902">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-903">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-903">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-904">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-904">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-905">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-905">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-906">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-906">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-907">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-907">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-908">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-908">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-909">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-909">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-910">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-910">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-911">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-912">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-913">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-914">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-915">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-915">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-916">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-916">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-917">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-917">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-918">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-918">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-919">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-919">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-920">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-920">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-921">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-921">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-922">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-922">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-923">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-923">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-924">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-924">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-925">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-925">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-926">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-926">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-927">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-927">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-928">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-928">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-929">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-929">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-930">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-930">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-931">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-931">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-932">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-932">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-933">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-933">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-934">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-934">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-935">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-935">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-936">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-936">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a><span data-ttu-id="ccc12-937">DXGI_FORMAT_R32G32 \_ FLOAT<sup>FNS</sup> (16) </span><span class="sxs-lookup"><span data-stu-id="ccc12-937">DXGI_FORMAT_R32G32\_FLOAT<sup>FNS</sup> (16)</span></span>
| <span data-ttu-id="ccc12-938">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-938">Target</span></span> | <span data-ttu-id="ccc12-939">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-939">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-940">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-940">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-941">64</span><span class="sxs-lookup"><span data-stu-id="ccc12-941">64</span></span> |
| <span data-ttu-id="ccc12-942">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-942">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-944">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-944">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-945">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-945">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-947">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-947">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-948">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-948">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-949">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-949">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-950">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-950">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-951">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-951">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-952">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-952">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-953">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-953">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-954">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-954">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-955">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-955">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-956">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-956">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-957">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-957">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-958">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-958">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-959">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-959">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-960">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-960">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-961">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-961">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-962">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-962">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-963">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-963">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-964">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-964">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-965">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-965">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-966">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-966">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-967">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-967">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-968">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-968">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-969">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-969">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-970">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-970">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-971">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-971">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-972">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-972">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-973">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-973">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-974">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-974">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-975">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-975">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-976">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-976">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-977">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-977">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-978">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-978">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-979">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-979">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-980">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-980">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-981">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-981">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-982">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-982">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-983">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-983">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-984">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-984">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-985">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-985">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-986">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-986">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-987">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-987">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-988">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-988">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a><span data-ttu-id="ccc12-989">DXGI_FORMAT_R32G32 \_ UINT<sup>FNS</sup> (17) </span><span class="sxs-lookup"><span data-stu-id="ccc12-989">DXGI_FORMAT_R32G32\_UINT<sup>FNS</sup> (17)</span></span>
| <span data-ttu-id="ccc12-990">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-990">Target</span></span> | <span data-ttu-id="ccc12-991">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-991">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-992">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-992">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-993">64</span><span class="sxs-lookup"><span data-stu-id="ccc12-993">64</span></span> |
| <span data-ttu-id="ccc12-994">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-994">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-995">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-995">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-996">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-996">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-997">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-997">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-998">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-998">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-999">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-999">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1000">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1000">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-1001">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1001">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-1002">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1002">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-1003">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1003">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-1004">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1004">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1005">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1005">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1006">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1006">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1007">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1007">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1008">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1008">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1009">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1009">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-1010">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1010">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1011">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1012">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1012">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1013">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1013">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1014">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1014">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1015">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1015">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1016">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1016">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1017">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1017">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1018">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1018">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1019">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1019">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1020">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1020">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1021">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1021">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1022">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1022">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1023">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1023">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1024">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1024">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1025">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1025">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1026">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1026">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-1027">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1027">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1028">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1028">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1029">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1029">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-1030">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1030">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-1031">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1031">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1032">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1032">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-1033">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1033">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1034">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1034">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1035">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1035">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-1036">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1036">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-1037">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1037">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-1038">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1038">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a><span data-ttu-id="ccc12-1039">DXGI_FORMAT_R32G32 \_ 聖<sup>FNS</sup> (18) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1039">DXGI_FORMAT_R32G32\_SINT<sup>FNS</sup> (18)</span></span>
| <span data-ttu-id="ccc12-1040">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1040">Target</span></span> | <span data-ttu-id="ccc12-1041">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1041">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1042">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1042">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1043">64</span><span class="sxs-lookup"><span data-stu-id="ccc12-1043">64</span></span> |
| <span data-ttu-id="ccc12-1044">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1044">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-1045">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1045">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1046">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1046">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1047">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1047">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1048">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1048">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1049">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1049">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1050">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1050">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-1051">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1051">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-1052">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1052">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-1053">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1053">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-1054">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1054">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1055">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1055">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1056">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1056">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1057">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1057">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1058">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1058">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1059">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1059">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-1060">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1060">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-1061">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1061">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1062">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1062">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1063">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1063">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1064">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1064">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1065">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1065">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1066">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1066">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1067">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1067">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1068">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1068">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1069">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1069">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1070">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1070">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1071">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1071">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1072">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1072">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1073">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1073">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1074">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1074">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1075">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1075">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1076">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1076">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-1077">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1077">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1078">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1078">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1079">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1079">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-1080">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-1081">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1081">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1082">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1082">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-1083">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1083">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1084">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1084">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1085">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1085">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-1086">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1086">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-1087">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1087">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-1088">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1088">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="ccc12-1089">DXGI_FORMAT_R32G8X24 無別 \_ <sup>電腦</sup> (19) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1089">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="ccc12-1090">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1090">Target</span></span> | <span data-ttu-id="ccc12-1091">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1091">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1092">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1092">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1093">64</span><span class="sxs-lookup"><span data-stu-id="ccc12-1093">64</span></span> |
| <span data-ttu-id="ccc12-1094">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1094">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-1095">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1095">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1096">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1096">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1097">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1097">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1098">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1098">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1099">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1099">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1100">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1100">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-1101">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1101">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-1102">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1102">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-1103">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1103">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-1104">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1104">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1105">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1105">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1106">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1106">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1107">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1107">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1108">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1108">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1109">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1109">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-1110">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1110">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-1111">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1111">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1112">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1112">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1113">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1113">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1114">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1114">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1115">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1115">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1116">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1116">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1117">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1117">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1118">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1118">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1119">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1119">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1120">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1120">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1121">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1121">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1122">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1122">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1123">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1123">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1124">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1124">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1125">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1125">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1126">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1126">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-1127">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1127">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1128">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1128">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1129">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1129">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-1130">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1130">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-1131">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1131">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1132">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1132">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-1133">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1133">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1134">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1134">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1135">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1135">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-1136">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1136">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-1137">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1137">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-1138">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1138">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a><span data-ttu-id="ccc12-1139">DXGI_FORMAT_D32 \_ FLOAT \_ S8X24 \_ UINT<sup>FNS</sup> (20) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1139">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FNS</sup> (20)</span></span>
| <span data-ttu-id="ccc12-1140">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1140">Target</span></span> | <span data-ttu-id="ccc12-1141">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1141">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1142">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1142">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1143">64</span><span class="sxs-lookup"><span data-stu-id="ccc12-1143">64</span></span> |
| <span data-ttu-id="ccc12-1144">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1144">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-1145">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1145">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1146">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1146">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1147">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1147">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1148">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1148">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1149">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1149">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1150">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1150">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-1151">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1151">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-1152">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1152">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-1153">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1153">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-1154">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1154">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1155">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1155">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1156">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1156">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1157">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1157">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1158">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1158">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1159">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1159">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-1160">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1160">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-1161">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1161">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1162">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1162">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1163">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1163">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1164">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1164">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1165">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1165">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1166">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1166">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1167">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1167">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1168">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1168">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1169">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1169">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1170">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1170">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1171">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1171">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1172">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1172">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1173">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1173">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1174">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1174">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1175">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1175">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1176">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1176">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-1177">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1177">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1178">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1178">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1179">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1179">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-1180">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1180">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-1181">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1181">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1182">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1182">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-1183">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1183">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1184">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1184">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1185">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1185">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-1186">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1186">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-1187">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1187">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-1188">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1188">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a><span data-ttu-id="ccc12-1189">DXGI_FORMAT_R32 \_ FLOAT X8X24 無型別 \_ \_ <sup>FNS</sup> (21) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1189">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FNS</sup> (21)</span></span>
| <span data-ttu-id="ccc12-1190">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1190">Target</span></span> | <span data-ttu-id="ccc12-1191">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1191">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1192">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1192">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1193">64</span><span class="sxs-lookup"><span data-stu-id="ccc12-1193">64</span></span> |
| <span data-ttu-id="ccc12-1194">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1194">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-1195">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1195">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1196">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1196">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1197">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1197">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1198">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1198">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1199">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1199">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1200">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1200">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-1201">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1201">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-1202">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1202">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-1203">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1203">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-1204">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1204">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1205">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1205">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1206">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1206">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1207">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1207">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1208">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1208">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1209">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1209">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-1210">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1210">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-1211">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1211">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1212">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1212">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1213">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1213">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1214">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1214">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1215">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1215">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1216">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1216">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1217">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1217">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1218">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1218">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1219">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1219">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1220">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1220">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1221">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1221">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1222">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1222">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1223">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1223">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1224">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1224">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1225">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1225">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1226">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1226">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-1227">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1227">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1228">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1228">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1229">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1229">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-1230">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1230">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-1231">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1231">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1232">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1232">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-1233">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1233">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1234">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1234">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1235">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1235">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-1236">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1236">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-1237">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1237">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-1238">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1238">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a><span data-ttu-id="ccc12-1239">DXGI_FORMAT_X32 無別 \_ \_ G8X24 \_ UINT<sup>FNS</sup> (22) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1239">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FNS</sup> (22)</span></span>
| <span data-ttu-id="ccc12-1240">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1240">Target</span></span> | <span data-ttu-id="ccc12-1241">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1241">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1242">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1242">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1243">64</span><span class="sxs-lookup"><span data-stu-id="ccc12-1243">64</span></span> |
| <span data-ttu-id="ccc12-1244">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1244">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-1245">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1245">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1246">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1246">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1247">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1247">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1248">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1248">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1249">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1249">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1250">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1250">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-1251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1251">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-1252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1252">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-1253">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1253">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-1254">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1254">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1255">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1255">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1256">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1256">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1257">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1257">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1258">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1258">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1259">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1259">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-1260">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1260">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-1261">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1261">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1262">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1262">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1263">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1263">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1264">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1264">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1265">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1265">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1266">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1266">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1267">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1267">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1268">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1268">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1269">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1269">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1270">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1270">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1271">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1271">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1272">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1272">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1273">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1273">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1274">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1274">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1275">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1275">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1276">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1276">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-1277">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1277">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1278">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1278">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1279">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1279">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-1280">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1280">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-1281">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1281">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1282">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1282">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-1283">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1283">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1284">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1284">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1285">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1285">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-1286">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1286">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-1287">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1287">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-1288">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1288">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="ccc12-1289">DXGI_FORMAT_R10G10B10A2 無別 \_ <sup>電腦</sup> (23) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1289">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="ccc12-1290">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1290">Target</span></span> | <span data-ttu-id="ccc12-1291">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1291">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1292">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1292">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1293">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-1293">32</span></span> |
| <span data-ttu-id="ccc12-1294">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1294">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-1295">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1295">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1296">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1296">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1297">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1297">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1298">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1298">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1299">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1299">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1300">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1300">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-1301">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1301">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-1302">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1302">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-1303">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1303">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-1304">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1304">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1305">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1305">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1306">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1306">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1307">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1307">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1308">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1308">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1309">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1309">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-1310">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1310">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-1311">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1311">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1312">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1312">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1313">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1313">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1314">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1314">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1315">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1315">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1316">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1316">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1317">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1317">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1318">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1318">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1319">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1319">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1320">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1320">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1321">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1321">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1322">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1322">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1323">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1323">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1324">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1324">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1325">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1325">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1326">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1326">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-1327">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1327">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1328">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1328">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1329">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1329">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-1330">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1330">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-1331">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1331">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1332">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1332">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-1333">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1333">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1334">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1334">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1335">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1335">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-1336">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1336">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-1337">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1337">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-1338">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1338">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a><span data-ttu-id="ccc12-1339">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FNS</sup> (24) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1339">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FNS</sup> (24)</span></span>
| <span data-ttu-id="ccc12-1340">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1340">Target</span></span> | <span data-ttu-id="ccc12-1341">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1341">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1342">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1342">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1343">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-1343">32</span></span> |
| <span data-ttu-id="ccc12-1344">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1344">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-1345">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1345">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1346">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1346">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1347">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1347">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1348">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1348">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1349">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1349">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1350">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1350">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-1351">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1351">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-1352">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1352">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-1353">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1353">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-1354">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1354">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1355">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1355">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1356">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1356">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1357">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1357">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1358">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1358">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1359">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1359">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-1360">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1360">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-1361">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1361">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1362">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1362">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1363">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1363">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1364">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1364">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1365">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1365">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1366">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1366">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1367">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1367">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1368">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1368">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1369">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1369">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1370">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1370">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1371">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1371">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1372">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1372">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1373">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1373">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1374">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1374">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1375">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1375">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1376">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1376">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-1377">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1377">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1378">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1378">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1379">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1379">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-1380">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1380">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-1381">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1381">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1382">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1382">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-1383">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1383">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1384">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1385">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-1386">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-1387">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1387">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1389">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1389">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a><span data-ttu-id="ccc12-1390">DXGI_FORMAT_R10G10B10A2 \_ UINT<sup>FNS</sup> (25) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1390">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FNS</sup> (25)</span></span>
| <span data-ttu-id="ccc12-1391">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1391">Target</span></span> | <span data-ttu-id="ccc12-1392">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1392">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1393">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1394">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-1394">32</span></span> |
| <span data-ttu-id="ccc12-1395">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1395">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-1396">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1396">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1397">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1397">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1398">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1398">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1399">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1399">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1400">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1400">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1401">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1401">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-1402">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1402">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-1403">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1403">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-1404">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1404">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-1405">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1405">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1406">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1406">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1407">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1407">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1408">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1408">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1409">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1409">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1410">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1410">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-1411">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1411">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-1412">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1412">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1413">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1413">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1414">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1414">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1415">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1415">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1416">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1416">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1417">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1417">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1418">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1418">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1419">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1419">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1420">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1420">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1421">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1421">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1422">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1422">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1423">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1423">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1424">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1424">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1425">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1425">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1426">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1426">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1427">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1427">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-1428">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1428">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1429">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1429">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1430">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1430">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-1431">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1431">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-1432">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1432">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1433">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-1434">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1434">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1435">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1435">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1436">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1436">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-1437">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1437">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-1438">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1438">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-1439">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1439">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a><span data-ttu-id="ccc12-1440">DXGI_FORMAT_R10G10B10 \_ XR \_ 偏差 \_ A2 \_ UNORM<sup>FNS</sup> (89) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1440">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FNS</sup> (89)</span></span>
| <span data-ttu-id="ccc12-1441">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1441">Target</span></span> | <span data-ttu-id="ccc12-1442">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1442">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1443">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1443">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1444">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-1444">32</span></span> |
| <span data-ttu-id="ccc12-1445">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1445">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-1446">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1446">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1447">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1447">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1448">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1448">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1449">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1449">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1450">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1450">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1451">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1451">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-1452">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1452">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-1453">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1453">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-1454">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1454">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-1455">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1455">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1456">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1456">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1457">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1457">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1458">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1458">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1459">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1459">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1460">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1460">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-1461">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1461">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-1462">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1462">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1463">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1463">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1464">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1465">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1466">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1467">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1468">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1468">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1469">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1470">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1471">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1472">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1473">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1473">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1474">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1475">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1476">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1477">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1477">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-1478">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1478">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1479">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1479">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1480">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1480">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-1481">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1481">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-1482">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1482">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1483">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1483">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-1484">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1484">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1485">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1485">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1486">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1486">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-1487">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1487">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-1488">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1488">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-1489">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1489">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="ccc12-1490">DXGI_FORMAT_R11G11B10 \_ FLOAT<sup>FNS</sup> (26) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1490">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="ccc12-1491">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1491">Target</span></span> | <span data-ttu-id="ccc12-1492">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1492">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1493">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1493">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1494">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-1494">32</span></span> |
| <span data-ttu-id="ccc12-1495">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1495">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-1496">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1496">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1497">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1498">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1499">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1500">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1501">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-1502">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1502">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-1503">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1503">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-1504">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1504">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-1505">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1505">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1506">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1507">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1508">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1508">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1509">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1510">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1510">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-1511">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1511">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-1512">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1512">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1513">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1513">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1514">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1514">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1515">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1515">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1516">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1516">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1517">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1517">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1518">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1518">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1519">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1519">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1520">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1520">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1521">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1521">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1522">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1522">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1523">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1523">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1524">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1524">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1525">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1525">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1526">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1526">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1527">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1527">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-1528">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1528">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1529">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1529">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1530">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1530">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-1531">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1531">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-1532">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1532">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1533">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1533">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-1534">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1534">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1535">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1535">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1536">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1536">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-1537">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1537">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-1538">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1538">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-1539">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1539">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="ccc12-1540">DXGI_FORMAT_R8G8B8A8 無別 \_ <sup>電腦</sup> (27) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1540">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="ccc12-1541">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1541">Target</span></span> | <span data-ttu-id="ccc12-1542">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1542">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1543">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1543">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1544">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-1544">32</span></span> |
| <span data-ttu-id="ccc12-1545">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1545">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-1546">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1546">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1547">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1547">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1548">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1548">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1549">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1549">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1550">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1550">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1551">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1551">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-1552">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1552">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-1553">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1553">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-1554">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1554">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-1555">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1555">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1556">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1556">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1557">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1557">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1558">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1558">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1559">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1559">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1560">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1560">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-1561">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1561">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-1562">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1562">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1563">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1563">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1564">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1564">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1565">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1566">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1567">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1568">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1568">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1569">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1569">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1570">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1570">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1571">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1571">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1572">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1572">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1573">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1573">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1574">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1574">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1575">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1575">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1576">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1576">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1577">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1577">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-1578">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1578">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1579">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1579">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1580">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1580">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-1581">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1581">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-1582">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1582">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1583">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1583">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-1584">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1584">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1585">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1585">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1586">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1586">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-1587">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1587">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-1588">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1588">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-1589">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1589">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a><span data-ttu-id="ccc12-1590">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FNS</sup> (28) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1590">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FNS</sup> (28)</span></span>
| <span data-ttu-id="ccc12-1591">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1591">Target</span></span> | <span data-ttu-id="ccc12-1592">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1592">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1593">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1593">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1594">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-1594">32</span></span> |
| <span data-ttu-id="ccc12-1595">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1595">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1597">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1597">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1598">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1598">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1600">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1601">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1602">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1603">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1605">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1605">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1607">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1607">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1609">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1609">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1611">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1611">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1613">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1614">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1615">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1615">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1616">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1617">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1617">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1619">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1619">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1621">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1621">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1623">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1623">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1625">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1625">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1626">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1626">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1627">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1627">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1628">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1628">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1629">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1629">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1630">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1630">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1631">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1631">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1632">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1632">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1633">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1633">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1634">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1634">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1635">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1635">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1636">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1636">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1637">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1637">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1638">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1638">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1640">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1640">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-1642">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1642">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-1644">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1644">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-1646">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1646">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1648">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1648">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1649">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1649">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1651">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1651">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1652">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1652">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1653">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1653">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-1655">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1655">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1657">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1657">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1659">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1659">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a><span data-ttu-id="ccc12-1660">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ SRGB<sup>FNS</sup> (29) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1660">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FNS</sup> (29)</span></span>
| <span data-ttu-id="ccc12-1661">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1661">Target</span></span> | <span data-ttu-id="ccc12-1662">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1662">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1663">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1663">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1664">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-1664">32</span></span> |
| <span data-ttu-id="ccc12-1665">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1665">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1667">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1667">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1668">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1668">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1669">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1669">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1670">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1670">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1671">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1671">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1672">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1672">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1674">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1674">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1676">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1676">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1678">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1678">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1680">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1680">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1682">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1682">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1683">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1683">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1684">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1684">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1685">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1685">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1686">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1686">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1688">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1688">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1690">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1690">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1692">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1692">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1694">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1694">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1695">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1695">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1696">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1696">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1697">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1697">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1698">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1698">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1699">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1699">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1700">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1700">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1701">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1701">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1702">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1702">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1703">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1703">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1704">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1704">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1705">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1705">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1706">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1706">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1707">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1707">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1709">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1709">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-1711">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1711">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-1713">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1713">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-1715">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1715">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1717">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1717">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1718">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1718">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1720">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1720">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1721">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1721">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1722">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1722">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-1724">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1724">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1726">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1726">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1728">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1728">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a><span data-ttu-id="ccc12-1729">DXGI_FORMAT_R8G8B8A8 \_ UINT<sup>FNS</sup> (30) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1729">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FNS</sup> (30)</span></span>
| <span data-ttu-id="ccc12-1730">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1730">Target</span></span> | <span data-ttu-id="ccc12-1731">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1731">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1732">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1732">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1733">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-1733">32</span></span> |
| <span data-ttu-id="ccc12-1734">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1734">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1736">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1736">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1737">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1737">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1739">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1739">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1740">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1740">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1741">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1741">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1742">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1742">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-1743">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1743">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-1744">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1744">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-1745">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1745">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-1746">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1746">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1747">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1747">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1748">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1748">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1749">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1749">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1750">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1750">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1751">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1751">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-1752">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1752">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-1753">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1753">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1754">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1754">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1755">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1755">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1756">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1756">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1757">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1757">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1758">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1758">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1759">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1759">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1760">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1760">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1761">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1761">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1762">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1762">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1763">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1763">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1764">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1764">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1765">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1765">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1766">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1766">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1767">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1767">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1768">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1768">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-1769">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1769">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1770">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1770">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1771">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1771">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-1772">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1772">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-1773">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1773">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1774">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1774">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-1775">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1775">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1776">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1776">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1777">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1777">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-1778">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1778">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-1779">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1779">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-1780">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1780">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a><span data-ttu-id="ccc12-1781">DXGI_FORMAT_R8G8B8A8 \_ SNORM<sup>FNS</sup> (31) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1781">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FNS</sup> (31)</span></span>
| <span data-ttu-id="ccc12-1782">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1782">Target</span></span> | <span data-ttu-id="ccc12-1783">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1783">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1784">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1784">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1785">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-1785">32</span></span> |
| <span data-ttu-id="ccc12-1786">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1786">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1788">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1788">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1789">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1789">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1790">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1790">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1791">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1791">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1792">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1792">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1793">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1793">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1795">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1795">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-1796">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1796">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1798">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1798">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1800">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1800">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1802">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1802">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1803">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1803">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1804">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1804">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1805">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1805">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1806">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1806">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1808">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1808">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-1809">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1809">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1810">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1810">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1811">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1812">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1812">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1813">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1813">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1814">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1814">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1815">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1815">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1816">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1816">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1817">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1817">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1818">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1818">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1819">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1819">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1820">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1820">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1821">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1821">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1822">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1822">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1823">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1823">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1824">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1824">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-1826">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1826">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1827">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1827">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1828">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1828">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-1829">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1829">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-1830">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1830">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1831">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1831">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-1832">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1832">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1833">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1833">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1834">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1834">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-1835">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1835">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-1836">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1836">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-1837">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1837">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a><span data-ttu-id="ccc12-1838">DXGI_FORMAT_R8G8B8A8 \_ 聖<sup>FNS</sup> (32) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1838">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FNS</sup> (32)</span></span>
| <span data-ttu-id="ccc12-1839">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1839">Target</span></span> | <span data-ttu-id="ccc12-1840">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1840">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1841">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1841">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1842">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-1842">32</span></span> |
| <span data-ttu-id="ccc12-1843">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1843">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-1844">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1844">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1845">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1845">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1846">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1846">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1847">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1847">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1848">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1848">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1849">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1849">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-1850">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1850">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-1851">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1851">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-1852">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1852">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-1853">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1853">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1854">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1854">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1855">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1855">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1856">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1856">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1857">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1857">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1858">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1858">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-1859">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1859">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-1860">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1860">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1861">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1861">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1862">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1862">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1863">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1863">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1864">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1864">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1865">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1865">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1866">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1866">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1867">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1867">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1868">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1868">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1869">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1869">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1870">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1870">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1871">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1871">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1872">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1872">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1873">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1873">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1874">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1874">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1875">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1875">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-1876">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1876">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1877">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1877">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1878">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1878">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-1879">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1879">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-1880">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1880">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1881">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1881">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-1882">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1882">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1883">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1883">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1884">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1884">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-1885">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1885">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-1886">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1886">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-1887">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1887">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="ccc12-1888">DXGI_FORMAT_R16G16 無的 \_ <sup>電腦</sup> (33) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1888">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="ccc12-1889">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1889">Target</span></span> | <span data-ttu-id="ccc12-1890">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1890">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1891">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1891">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1892">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-1892">32</span></span> |
| <span data-ttu-id="ccc12-1893">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1893">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-1894">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1894">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1895">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1895">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1896">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1896">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1897">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1897">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1898">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1898">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1899">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1899">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-1900">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1900">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-1901">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1901">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-1902">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1902">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-1903">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1903">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1904">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1904">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1905">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1905">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1906">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1906">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1907">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1907">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1908">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1908">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-1909">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1909">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-1910">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1910">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1911">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1911">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1912">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1912">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1913">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1913">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1914">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1914">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1915">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1915">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1916">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1916">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1917">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1917">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1918">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1918">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1919">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1919">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1920">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1920">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1921">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1921">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1922">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1922">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1923">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1923">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1924">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1924">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1925">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1925">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-1926">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1926">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1927">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1927">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1928">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1928">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-1929">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1929">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-1930">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1930">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1931">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1931">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-1932">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1932">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1933">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1933">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1934">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1934">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-1935">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1935">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-1936">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1936">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-1937">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1937">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a><span data-ttu-id="ccc12-1938">DXGI_FORMAT_R16G16 \_ FLOAT<sup>FNS</sup> (34) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1938">DXGI_FORMAT_R16G16\_FLOAT<sup>FNS</sup> (34)</span></span>
| <span data-ttu-id="ccc12-1939">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1939">Target</span></span> | <span data-ttu-id="ccc12-1940">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1940">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1941">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1941">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1942">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-1942">32</span></span> |
| <span data-ttu-id="ccc12-1943">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1943">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-1944">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1944">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1945">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1945">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1946">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1946">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1947">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1947">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1948">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1948">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1949">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1949">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-1950">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1950">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-1951">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-1951">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-1952">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1952">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-1953">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1953">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1954">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1954">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1955">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1955">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-1956">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-1956">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-1957">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-1957">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-1958">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-1958">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-1959">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-1959">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-1960">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1960">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1961">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1961">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1962">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-1962">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-1963">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1963">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-1964">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1964">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1965">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1965">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-1966">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-1966">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-1967">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1967">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-1968">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1968">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-1969">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-1969">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-1970">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-1970">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-1971">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-1971">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-1972">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-1972">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-1973">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1973">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1974">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-1974">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-1975">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-1975">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-1976">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1976">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1977">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-1977">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-1978">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-1978">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-1979">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-1979">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-1980">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1980">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-1981">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-1981">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-1982">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-1982">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-1983">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1983">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-1984">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-1984">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-1985">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-1985">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-1986">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1986">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-1987">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-1987">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a><span data-ttu-id="ccc12-1988">DXGI_FORMAT_R16G16 \_ UNORM<sup>FNS</sup> (35) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1988">DXGI_FORMAT_R16G16\_UNORM<sup>FNS</sup> (35)</span></span>
| <span data-ttu-id="ccc12-1989">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-1989">Target</span></span> | <span data-ttu-id="ccc12-1990">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1990">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-1991">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-1991">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-1992">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-1992">32</span></span> |
| <span data-ttu-id="ccc12-1993">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-1993">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-1994">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-1994">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1995">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1995">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1996">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1996">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1997">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-1997">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-1998">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1998">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-1999">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-1999">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-2000">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2000">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2001">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2001">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2002">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2002">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-2003">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2003">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2004">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2004">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2005">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2005">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2006">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2006">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2007">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2007">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2008">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2008">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2009">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2009">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2010">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2010">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2011">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2011">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2012">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2012">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2013">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2013">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2014">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2014">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2015">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2015">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2016">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2016">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2017">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2017">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2018">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2018">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2019">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2019">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2020">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2020">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2021">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2021">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2022">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2022">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2023">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2023">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2024">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2024">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2025">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2025">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-2026">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2026">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2027">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2027">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2028">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2028">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2029">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2029">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2030">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2030">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2031">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2031">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2032">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2032">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2033">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2033">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2034">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2034">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2035">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2035">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2036">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2036">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2037">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2037">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a><span data-ttu-id="ccc12-2038">DXGI_FORMAT_R16G16 \_ UINT<sup>FNS</sup> (36) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2038">DXGI_FORMAT_R16G16\_UINT<sup>FNS</sup> (36)</span></span>
| <span data-ttu-id="ccc12-2039">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2039">Target</span></span> | <span data-ttu-id="ccc12-2040">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2040">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2041">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2041">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2042">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-2042">32</span></span> |
| <span data-ttu-id="ccc12-2043">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2043">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-2044">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2044">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2045">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2045">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2046">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2046">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2047">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2047">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2048">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2048">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2049">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2049">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-2050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2050">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2051">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2051">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2052">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2052">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-2053">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2053">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2054">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2054">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2055">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2055">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2056">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2056">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2057">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2057">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2058">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2058">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2059">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2059">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2060">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2060">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2061">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2061">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2062">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2062">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2063">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2063">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2064">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2064">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2065">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2065">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2066">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2066">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2067">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2067">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2068">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2068">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2069">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2069">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2070">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2070">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2071">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2071">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2072">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2072">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2073">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2073">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2074">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2074">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2075">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2075">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-2076">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2076">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2077">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2077">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2078">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2078">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2079">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2079">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2080">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2080">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2081">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2081">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2082">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2082">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2083">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2083">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2084">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2084">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2085">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2085">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2086">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2086">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2087">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2087">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a><span data-ttu-id="ccc12-2088">DXGI_FORMAT_R16G16 \_ SNORM<sup>FNS</sup> (37) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2088">DXGI_FORMAT_R16G16\_SNORM<sup>FNS</sup> (37)</span></span>
| <span data-ttu-id="ccc12-2089">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2089">Target</span></span> | <span data-ttu-id="ccc12-2090">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2090">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2091">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2091">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2092">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-2092">32</span></span> |
| <span data-ttu-id="ccc12-2093">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2093">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2095">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2095">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2096">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2096">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2098">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2098">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2099">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2099">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2100">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2100">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2101">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2101">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2103">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2103">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2104">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2104">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2105">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2105">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2107">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2107">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2108">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2108">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2109">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2109">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2110">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2110">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2111">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2111">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2112">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2112">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2114">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2114">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2115">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2115">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2116">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2116">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2117">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2117">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2118">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2118">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2119">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2119">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2120">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2120">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2121">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2121">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2122">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2122">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2123">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2123">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2124">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2124">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2125">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2125">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2126">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2126">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2127">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2127">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2128">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2128">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2129">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2129">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2130">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2130">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2132">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2132">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2133">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2133">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2134">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2134">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2135">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2135">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2136">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2136">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2137">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2137">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2138">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2138">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2139">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2139">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2140">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2140">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2141">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2141">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2142">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2142">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2143">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2143">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a><span data-ttu-id="ccc12-2144">DXGI_FORMAT_R16G16 \_ 聖<sup>FNS</sup> (38) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2144">DXGI_FORMAT_R16G16\_SINT<sup>FNS</sup> (38)</span></span>
| <span data-ttu-id="ccc12-2145">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2145">Target</span></span> | <span data-ttu-id="ccc12-2146">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2146">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2147">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2147">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2148">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-2148">32</span></span> |
| <span data-ttu-id="ccc12-2149">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2149">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2151">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2151">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2152">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2152">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2154">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2154">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2155">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2155">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2156">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2156">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2157">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2157">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-2158">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2158">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2159">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2159">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2160">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2160">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-2161">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2161">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2162">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2162">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2163">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2163">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2164">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2164">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2165">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2165">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2166">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2166">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2167">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2167">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2168">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2168">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2169">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2169">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2170">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2170">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2171">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2171">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2172">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2172">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2173">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2173">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2174">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2174">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2175">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2175">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2176">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2176">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2177">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2177">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2178">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2178">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2179">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2179">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2180">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2180">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2181">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2181">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2182">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2182">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2183">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2183">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-2184">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2184">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2185">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2185">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2186">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2186">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2187">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2187">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2188">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2188">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2189">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2189">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2190">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2190">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2191">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2191">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2192">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2192">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2193">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2193">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2194">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2194">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2195">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2195">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="ccc12-2196">DXGI_FORMAT_R32 無的 \_ <sup>電腦</sup> (39) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2196">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="ccc12-2197">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2197">Target</span></span> | <span data-ttu-id="ccc12-2198">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2198">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2199">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2199">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2200">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-2200">32</span></span> |
| <span data-ttu-id="ccc12-2201">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2201">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-2202">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2202">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2203">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2203">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2204">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2204">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2205">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2205">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2206">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2206">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2207">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2207">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-2208">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2208">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2209">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2209">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2210">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2210">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-2211">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2211">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2212">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2212">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2213">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2213">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2214">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2214">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2215">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2215">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2216">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2216">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2217">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2217">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2218">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2218">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2219">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2219">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2220">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2220">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2221">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2221">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2222">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2222">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2223">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2223">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2224">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2224">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2225">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2225">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2226">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2226">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2227">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2227">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2228">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2228">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2229">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2229">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2230">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2230">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2231">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2231">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2232">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2232">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2233">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2233">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-2234">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2234">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2235">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2235">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2236">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2236">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2237">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2237">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2238">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2238">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2239">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2239">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2240">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2240">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2241">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2241">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2242">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2242">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2243">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2243">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2244">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2244">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2245">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2245">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a><span data-ttu-id="ccc12-2246">DXGI_FORMAT_D32 \_ FLOAT<sup>FNS</sup> (40) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2246">DXGI_FORMAT_D32\_FLOAT<sup>FNS</sup> (40)</span></span>
| <span data-ttu-id="ccc12-2247">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2247">Target</span></span> | <span data-ttu-id="ccc12-2248">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2248">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2249">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2249">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2250">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-2250">32</span></span> |
| <span data-ttu-id="ccc12-2251">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2251">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-2252">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2252">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2253">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2253">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2254">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2254">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2255">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2255">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2256">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2256">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2257">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2257">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-2258">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2258">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2259">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2259">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2260">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2260">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-2261">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2261">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2262">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2262">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2263">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2263">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2264">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2264">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2265">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2265">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2266">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2266">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2267">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2267">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2268">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2268">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2269">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2269">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2270">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2270">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2271">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2271">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2272">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2272">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2273">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2273">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2274">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2274">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2275">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2275">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2276">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2276">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2277">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2277">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2278">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2278">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2279">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2279">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2280">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2280">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2281">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2281">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2282">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2282">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2283">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2283">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-2284">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2284">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2285">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2285">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2286">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2286">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2287">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2287">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2288">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2288">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2289">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2289">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2290">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2290">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2291">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2291">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2292">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2292">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2293">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2293">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2294">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2294">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2295">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2295">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a><span data-ttu-id="ccc12-2296">DXGI_FORMAT_R32 \_ FLOAT<sup>FNS</sup> (41) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2296">DXGI_FORMAT_R32\_FLOAT<sup>FNS</sup> (41)</span></span>
| <span data-ttu-id="ccc12-2297">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2297">Target</span></span> | <span data-ttu-id="ccc12-2298">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2298">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2299">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2299">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2300">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-2300">32</span></span> |
| <span data-ttu-id="ccc12-2301">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2301">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2303">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2303">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2304">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2304">Input Assembler Vertex Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2306">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2306">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2307">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2307">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2308">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2308">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2309">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2309">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-2310">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2310">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2311">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2311">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2312">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2312">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-2313">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2313">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2314">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2314">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2315">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2315">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2316">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2316">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2317">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2317">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2318">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2318">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2319">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2319">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2320">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2320">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2321">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2321">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2322">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2322">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2323">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2323">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2324">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2324">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2325">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2325">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2326">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2326">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2327">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2327">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2328">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2328">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2329">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2329">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2330">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2330">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2331">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2331">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2332">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2332">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2333">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2333">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2334">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2334">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2335">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2335">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-2336">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2336">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2337">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2337">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2338">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2338">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2339">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2339">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2340">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2340">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2341">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2341">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2342">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2342">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2343">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2343">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2344">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2344">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2345">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2345">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2346">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2346">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2347">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2347">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a><span data-ttu-id="ccc12-2348">DXGI_FORMAT_R32 \_ UINT<sup>FNS</sup> (42) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2348">DXGI_FORMAT_R32\_UINT<sup>FNS</sup> (42)</span></span>
| <span data-ttu-id="ccc12-2349">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2349">Target</span></span> | <span data-ttu-id="ccc12-2350">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2350">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2351">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2351">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2352">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-2352">32</span></span> |
| <span data-ttu-id="ccc12-2353">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2353">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-2354">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2354">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2355">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2355">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2356">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2356">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2357">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2357">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2358">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2358">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2359">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2359">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-2360">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2360">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2361">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2361">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2362">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2362">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-2363">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2363">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2364">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2364">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2365">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2365">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2366">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2366">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2367">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2367">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2368">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2368">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2369">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2369">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2370">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2370">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2371">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2371">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2372">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2372">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2373">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2373">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2374">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2374">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2375">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2375">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2376">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2376">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2377">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2377">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2378">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2378">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2379">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2379">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2380">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2380">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2381">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2381">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2382">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2382">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2383">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2383">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2384">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2384">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2385">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2385">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-2386">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2386">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2387">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2387">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2388">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2388">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2389">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2389">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2390">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2390">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2391">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2391">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2392">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2392">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2393">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2393">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2394">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2394">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2395">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2395">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2396">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2396">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2397">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2397">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a><span data-ttu-id="ccc12-2398">DXGI_FORMAT_R32 \_ 聖<sup>FNS</sup> (43) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2398">DXGI_FORMAT_R32\_SINT<sup>FNS</sup> (43)</span></span>
| <span data-ttu-id="ccc12-2399">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2399">Target</span></span> | <span data-ttu-id="ccc12-2400">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2400">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2401">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2401">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2402">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-2402">32</span></span> |
| <span data-ttu-id="ccc12-2403">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2403">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-2404">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2404">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2405">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2405">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2406">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2406">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2407">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2407">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2408">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2408">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2409">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2409">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-2410">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2410">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2411">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2411">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2412">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2412">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-2413">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2413">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2414">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2415">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2416">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2416">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2417">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2418">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2418">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2419">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2419">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2420">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2420">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2421">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2421">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2422">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2422">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2423">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2423">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2424">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2424">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2425">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2425">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2426">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2426">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2427">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2427">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2428">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2428">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2429">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2429">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2430">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2430">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2431">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2431">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2432">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2432">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2433">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2433">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2434">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2434">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2435">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2435">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-2436">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2436">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2437">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2437">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2438">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2438">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2439">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2439">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2440">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2440">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2441">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2442">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2442">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2443">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2443">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2444">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2444">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2445">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2445">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2446">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2446">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2447">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2447">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="ccc12-2448">DXGI_FORMAT_R24G8 無的 \_ <sup>電腦</sup> (44) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2448">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="ccc12-2449">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2449">Target</span></span> | <span data-ttu-id="ccc12-2450">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2450">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2451">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2451">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2452">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-2452">32</span></span> |
| <span data-ttu-id="ccc12-2453">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2453">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-2454">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2454">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2455">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2455">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2456">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2456">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2457">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2457">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2458">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2458">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2459">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2459">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-2460">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2460">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2461">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2461">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2462">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2462">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-2463">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2463">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2464">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2464">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2465">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2465">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2466">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2466">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2467">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2467">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2468">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2468">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2469">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2470">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2471">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2472">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2473">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2474">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2475">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2476">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2476">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2477">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2478">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2479">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2480">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2481">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2481">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2482">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2483">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2484">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2485">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2485">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-2486">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2486">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2487">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2487">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2488">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2488">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2489">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2489">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2490">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2490">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2491">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2491">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2492">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2492">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2493">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2493">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2494">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2494">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2495">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2495">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2496">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2496">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2497">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2497">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a><span data-ttu-id="ccc12-2498">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FNS</sup> (45) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2498">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FNS</sup> (45)</span></span>
| <span data-ttu-id="ccc12-2499">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2499">Target</span></span> | <span data-ttu-id="ccc12-2500">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2500">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2501">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2501">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2502">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-2502">32</span></span> |
| <span data-ttu-id="ccc12-2503">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2503">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2505">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2505">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2506">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2506">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2507">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2507">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2508">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2508">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2509">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2509">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2510">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2510">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2512">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2513">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2514">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2514">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-2515">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2515">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2516">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2516">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2517">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2517">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2518">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2518">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2519">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2519">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2520">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2520">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2521">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2521">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2522">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2522">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2523">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2523">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2524">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2524">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2525">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2525">Depth/Stencil Target</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2527">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2527">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2528">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2528">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2529">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2529">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2530">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2530">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2531">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2531">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2532">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2532">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2533">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2533">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2534">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2534">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2535">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2535">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2536">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2536">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2537">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2537">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2538">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2538">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-2539">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2539">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-2541">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2541">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-2543">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2543">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-2545">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2545">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2546">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2546">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2547">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2547">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2548">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2548">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2549">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2549">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2550">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2550">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2551">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2551">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2552">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2552">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2553">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2553">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a><span data-ttu-id="ccc12-2554">DXGI_FORMAT_R24 \_ UNORM \_ X8 無別 \_ <sup>FNS</sup> (46) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2554">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FNS</sup> (46)</span></span>
| <span data-ttu-id="ccc12-2555">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2555">Target</span></span> | <span data-ttu-id="ccc12-2556">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2556">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2557">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2557">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2558">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-2558">32</span></span> |
| <span data-ttu-id="ccc12-2559">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2559">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-2560">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2560">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2561">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2561">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2562">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2562">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2563">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2563">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2564">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2564">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2565">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2565">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-2566">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2566">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2567">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2567">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2568">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2568">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-2569">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2569">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2570">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2570">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2571">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2571">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2572">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2572">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2573">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2573">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2574">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2574">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2575">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2575">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2576">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2576">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2577">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2577">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2578">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2578">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2579">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2579">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2580">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2580">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2581">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2581">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2582">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2582">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2583">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2583">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2584">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2584">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2585">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2585">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2586">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2586">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2587">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2587">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2588">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2588">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2589">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2589">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2590">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2590">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2591">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2591">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-2592">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2592">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2593">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2593">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2594">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2594">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2595">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2595">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2596">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2596">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2597">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2597">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2598">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2598">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2599">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2599">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2600">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2600">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2601">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2601">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2602">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2602">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2603">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2603">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a><span data-ttu-id="ccc12-2604">DXGI_FORMAT_X24 無別 \_ \_ G8 \_ UINT<sup>FNS</sup> (47) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2604">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FNS</sup> (47)</span></span>
| <span data-ttu-id="ccc12-2605">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2605">Target</span></span> | <span data-ttu-id="ccc12-2606">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2606">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2607">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2607">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2608">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-2608">32</span></span> |
| <span data-ttu-id="ccc12-2609">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2609">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-2610">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2610">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2611">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2611">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2612">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2612">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2613">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2613">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2614">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2614">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2615">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2615">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-2616">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2616">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2617">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2617">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2618">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2618">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-2619">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2619">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2620">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2620">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2621">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2621">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2622">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2622">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2623">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2623">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2624">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2624">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2625">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2625">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2626">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2626">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2627">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2627">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2628">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2628">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2629">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2629">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2630">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2630">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2631">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2631">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2632">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2632">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2633">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2633">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2634">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2634">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2635">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2635">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2636">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2636">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2637">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2637">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2638">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2638">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2639">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2639">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2640">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2640">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2641">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2641">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-2642">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2642">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2643">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2643">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2644">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2644">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2645">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2645">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2646">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2646">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2647">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2647">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2648">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2648">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2649">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2649">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2650">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2650">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2651">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2651">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2652">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2652">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2653">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2653">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="ccc12-2654">DXGI_FORMAT_R8G8 無的 \_ <sup>電腦</sup> (48) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2654">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="ccc12-2655">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2655">Target</span></span> | <span data-ttu-id="ccc12-2656">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2656">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2657">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2657">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2658">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-2658">16</span></span> |
| <span data-ttu-id="ccc12-2659">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2659">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-2660">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2660">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2661">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2661">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2662">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2662">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2663">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2663">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2664">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2664">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2665">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2665">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-2666">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2666">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2667">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2667">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2668">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2668">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-2669">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2669">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2670">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2670">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2671">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2671">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2672">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2672">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2673">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2673">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2674">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2674">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2675">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2675">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2676">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2676">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2677">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2677">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2678">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2678">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2679">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2679">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2680">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2680">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2681">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2681">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2682">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2682">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2683">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2683">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2684">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2684">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2685">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2685">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2686">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2686">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2687">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2687">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2688">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2688">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2689">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2689">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2690">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2690">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2691">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2691">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-2692">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2692">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2693">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2693">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2694">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2694">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2695">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2696">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2696">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2697">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2697">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2698">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2698">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2699">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2699">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2700">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2700">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2701">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2701">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2702">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2702">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2703">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2703">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a><span data-ttu-id="ccc12-2704">DXGI_FORMAT_R8G8 \_ UNORM<sup>FNS</sup> (49) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2704">DXGI_FORMAT_R8G8\_UNORM<sup>FNS</sup> (49)</span></span>
| <span data-ttu-id="ccc12-2705">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2705">Target</span></span> | <span data-ttu-id="ccc12-2706">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2706">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2707">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2707">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2708">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-2708">16</span></span> |
| <span data-ttu-id="ccc12-2709">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2709">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2711">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2711">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2712">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2712">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2713">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2713">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2714">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2714">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2715">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2715">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2716">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2716">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2718">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2718">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2719">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2719">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2720">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2720">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2722">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2722">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2724">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2724">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2725">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2725">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2726">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2726">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2727">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2727">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2728">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2728">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2729">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2729">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2730">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2730">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2732">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2732">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2734">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2734">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2735">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2735">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2736">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2736">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2737">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2737">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2738">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2738">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2739">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2739">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2740">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2740">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2741">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2741">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2742">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2742">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2743">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2743">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2744">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2744">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2745">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2745">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2746">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2746">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2747">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2747">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2749">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2749">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2750">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2750">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2751">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2751">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2752">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2752">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2753">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2753">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2754">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2754">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2755">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2755">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2756">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2756">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2757">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2757">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2758">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2758">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2759">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2759">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2761">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2761">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a><span data-ttu-id="ccc12-2762">DXGI_FORMAT_R8G8 \_ UINT<sup>FNS</sup> (50) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2762">DXGI_FORMAT_R8G8\_UINT<sup>FNS</sup> (50)</span></span>
| <span data-ttu-id="ccc12-2763">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2763">Target</span></span> | <span data-ttu-id="ccc12-2764">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2764">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2765">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2765">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2766">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-2766">16</span></span> |
| <span data-ttu-id="ccc12-2767">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2767">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-2768">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2768">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2769">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2769">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2770">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2770">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2771">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2771">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2772">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2772">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2773">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2773">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-2774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2774">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2775">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2775">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2776">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2776">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-2777">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2777">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2778">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2778">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2779">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2779">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2780">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2780">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2781">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2781">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2782">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2782">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2783">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2783">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2784">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2784">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2785">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2785">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2786">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2786">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2787">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2787">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2788">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2788">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2789">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2789">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2790">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2790">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2791">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2791">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2792">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2792">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2793">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2793">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2794">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2794">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2795">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2795">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2796">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2796">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2797">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2797">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2798">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2798">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2799">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2799">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-2800">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2800">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2801">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2801">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2802">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2802">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2803">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2803">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2804">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2804">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2805">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2805">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2806">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2806">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2807">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2807">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2808">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2808">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2809">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2809">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2810">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2810">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2811">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a><span data-ttu-id="ccc12-2812">DXGI_FORMAT_R8G8 \_ SNORM<sup>FNS</sup> (51) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2812">DXGI_FORMAT_R8G8\_SNORM<sup>FNS</sup> (51)</span></span>
| <span data-ttu-id="ccc12-2813">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2813">Target</span></span> | <span data-ttu-id="ccc12-2814">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2814">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2815">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2816">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-2816">16</span></span> |
| <span data-ttu-id="ccc12-2817">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2817">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2819">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2819">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2820">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2821">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2822">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2823">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2824">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2824">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2826">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2826">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2827">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2828">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2828">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2830">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2830">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2832">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2832">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2833">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2833">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2834">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2834">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2835">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2835">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2836">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2836">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2838">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2838">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2839">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2839">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2840">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2841">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2842">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2842">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2843">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2843">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2844">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2844">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2845">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2845">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2846">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2846">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2847">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2847">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2848">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2848">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2849">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2849">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2850">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2850">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2851">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2851">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2852">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2852">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2853">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2853">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2854">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2854">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-2856">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2856">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2857">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2857">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2858">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2858">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2859">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2859">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2860">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2860">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2861">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2861">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2862">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2862">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2863">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2863">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2864">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2864">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2865">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2865">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2866">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2866">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2867">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2867">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a><span data-ttu-id="ccc12-2868">DXGI_FORMAT_R8G8 \_ 聖<sup>FNS</sup> (52) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2868">DXGI_FORMAT_R8G8\_SINT<sup>FNS</sup> (52)</span></span>
| <span data-ttu-id="ccc12-2869">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2869">Target</span></span> | <span data-ttu-id="ccc12-2870">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2870">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2871">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2871">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2872">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-2872">16</span></span> |
| <span data-ttu-id="ccc12-2873">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2873">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-2874">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2874">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2875">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2875">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2876">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2876">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2877">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2877">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2878">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2878">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2879">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2879">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-2880">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2880">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2881">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2881">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2882">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2882">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-2883">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2883">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2884">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2884">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2885">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2885">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2886">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2886">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2887">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2887">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2888">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2888">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2889">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2889">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2890">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2890">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2891">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2891">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2892">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2893">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2894">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2895">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2896">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2896">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2897">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2898">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2899">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2900">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2901">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2901">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2902">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2903">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2904">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2905">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2905">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-2906">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2906">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2907">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2907">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2908">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2908">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2909">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2909">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2910">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2910">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2911">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2911">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2912">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2912">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2913">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2913">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2914">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2914">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2915">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2915">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2916">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2916">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2917">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2917">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="ccc12-2918">DXGI_FORMAT_R16 無的 \_ <sup>電腦</sup> (53) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2918">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="ccc12-2919">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2919">Target</span></span> | <span data-ttu-id="ccc12-2920">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2920">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2921">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2921">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2922">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-2922">16</span></span> |
| <span data-ttu-id="ccc12-2923">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2923">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-2924">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2924">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2925">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2925">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2926">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2926">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2927">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2927">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2928">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2928">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2929">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2929">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-2930">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2930">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2931">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2931">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2932">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2932">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-2933">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2934">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2935">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2936">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2936">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2937">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2938">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2938">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2939">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2939">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2940">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2940">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2941">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2941">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2942">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2942">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2943">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2943">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2944">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2944">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2945">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2945">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2946">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2946">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2947">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2947">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2948">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2948">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2949">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2949">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-2950">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-2950">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-2951">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-2951">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-2952">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-2952">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-2953">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2953">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2954">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-2954">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-2955">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-2955">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-2956">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2956">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2957">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2957">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2958">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-2958">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-2959">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-2959">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-2960">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2960">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-2961">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-2961">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-2962">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-2962">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-2963">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2963">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-2964">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2964">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-2965">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-2965">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-2966">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2966">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-2967">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-2967">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a><span data-ttu-id="ccc12-2968">DXGI_FORMAT_R16 \_ FLOAT<sup>FNS</sup> (54) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2968">DXGI_FORMAT_R16\_FLOAT<sup>FNS</sup> (54)</span></span>
| <span data-ttu-id="ccc12-2969">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2969">Target</span></span> | <span data-ttu-id="ccc12-2970">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2970">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-2971">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2971">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-2972">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-2972">16</span></span> |
| <span data-ttu-id="ccc12-2973">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-2973">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-2974">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-2974">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2975">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2975">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2976">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2976">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2977">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2977">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-2978">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2978">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-2979">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2979">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-2980">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-2980">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-2981">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-2981">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-2982">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2982">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-2983">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2983">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2984">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2984">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2985">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-2985">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-2986">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-2986">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-2987">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-2987">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-2988">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-2988">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-2989">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-2989">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-2990">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2990">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2991">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-2991">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-2992">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-2992">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-2993">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-2993">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-2994">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2994">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2995">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2995">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-2996">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-2996">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-2997">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-2997">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-2998">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-2998">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-2999">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-2999">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3000">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3000">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3001">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3001">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3002">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3002">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3003">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3003">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3004">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3004">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3005">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3005">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-3006">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3006">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3007">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3007">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3008">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3008">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3009">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3010">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3010">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3011">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3011">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3012">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3012">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3013">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3013">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3014">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3014">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3015">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3015">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3016">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3016">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-3017">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3017">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a><span data-ttu-id="ccc12-3018">DXGI_FORMAT_D16 \_ UNORM<sup>FNS</sup> (55) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3018">DXGI_FORMAT_D16\_UNORM<sup>FNS</sup> (55)</span></span>
| <span data-ttu-id="ccc12-3019">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3019">Target</span></span> | <span data-ttu-id="ccc12-3020">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3020">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3021">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3021">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3022">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-3022">16</span></span> |
| <span data-ttu-id="ccc12-3023">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3023">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3025">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3025">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3026">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3026">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3027">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3027">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3028">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3028">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3029">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3029">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3030">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3030">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3032">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3032">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3033">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3033">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-3034">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3034">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-3035">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3035">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3036">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3036">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3037">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3037">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3038">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3038">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3039">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3039">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3040">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3040">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-3041">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3041">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3042">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3042">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3043">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3043">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3044">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3044">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3045">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3045">Depth/Stencil Target</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3047">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3047">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3048">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3048">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3049">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3049">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3050">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3050">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3051">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3051">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3052">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3052">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3053">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3053">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3054">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3054">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3055">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3055">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3056">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3056">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3057">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3057">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3058">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3058">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-3059">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3059">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-3061">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3061">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-3063">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3063">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-3065">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3065">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3066">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3066">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3067">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3068">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3069">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3070">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3070">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3071">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3071">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3072">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3072">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-3073">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3073">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a><span data-ttu-id="ccc12-3074">DXGI_FORMAT_R16 \_ UNORM<sup>FNS</sup> (56) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3074">DXGI_FORMAT_R16\_UNORM<sup>FNS</sup> (56)</span></span>
| <span data-ttu-id="ccc12-3075">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3075">Target</span></span> | <span data-ttu-id="ccc12-3076">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3076">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3077">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3077">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3078">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-3078">16</span></span> |
| <span data-ttu-id="ccc12-3079">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3079">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-3080">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3080">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3081">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3081">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3082">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3082">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3083">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3083">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3084">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3084">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3085">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3085">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-3086">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3086">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3087">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3087">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-3088">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3088">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-3089">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3089">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3090">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3090">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3091">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3091">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3092">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3092">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3093">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3093">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3094">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3094">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-3095">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3095">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3096">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3096">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3097">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3097">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3098">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3099">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3100">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3101">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3102">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3102">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3103">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3103">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3104">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3104">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3105">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3105">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3106">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3106">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3107">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3107">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3108">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3108">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3109">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3109">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3110">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3110">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3111">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3111">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-3112">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3112">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3113">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3113">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3114">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3114">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3115">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3115">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3116">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3116">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3117">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3117">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3118">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3118">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3119">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3119">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3120">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3120">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3121">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3121">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3122">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3122">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-3123">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3123">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a><span data-ttu-id="ccc12-3124">DXGI_FORMAT_R16 \_ UINT<sup>FNS</sup> (57) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3124">DXGI_FORMAT_R16\_UINT<sup>FNS</sup> (57)</span></span>
| <span data-ttu-id="ccc12-3125">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3125">Target</span></span> | <span data-ttu-id="ccc12-3126">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3126">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3127">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3127">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3128">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-3128">16</span></span> |
| <span data-ttu-id="ccc12-3129">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3129">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3131">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3131">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3132">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3132">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3133">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3133">Input Assembler Index Buffer</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3135">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3135">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3136">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3136">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3137">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3137">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-3138">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3138">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3139">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3139">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-3140">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3140">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-3141">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3141">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3142">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3142">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3143">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3143">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3144">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3144">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3145">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3145">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3146">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3146">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-3147">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3147">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3148">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3148">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3149">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3149">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3150">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3150">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3151">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3151">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3152">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3152">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3153">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3153">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3154">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3154">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3155">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3155">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3156">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3156">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3157">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3157">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3158">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3158">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3159">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3159">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3160">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3160">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3161">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3161">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3162">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3162">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3163">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3163">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-3164">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3164">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3165">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3165">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3166">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3166">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3167">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3167">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3168">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3168">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3169">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3169">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3170">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3170">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3171">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3171">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3172">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3172">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3173">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3173">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3174">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3174">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-3175">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3175">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a><span data-ttu-id="ccc12-3176">DXGI_FORMAT_R16 \_ SNORM<sup>FNS</sup> (58) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3176">DXGI_FORMAT_R16\_SNORM<sup>FNS</sup> (58)</span></span>
| <span data-ttu-id="ccc12-3177">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3177">Target</span></span> | <span data-ttu-id="ccc12-3178">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3178">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3179">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3179">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3180">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-3180">16</span></span> |
| <span data-ttu-id="ccc12-3181">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3181">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-3182">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3182">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3183">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3183">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3184">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3184">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3185">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3185">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3186">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3186">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3187">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-3188">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3188">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3189">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3189">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-3190">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3190">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-3191">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3191">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3192">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3192">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3193">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3193">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3194">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3194">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3195">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3195">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3196">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3196">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-3197">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3197">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3198">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3198">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3199">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3199">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3200">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3200">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3201">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3201">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3202">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3202">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3203">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3203">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3204">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3204">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3205">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3205">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3206">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3206">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3207">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3207">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3208">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3208">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3209">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3209">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3210">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3210">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3211">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3211">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3212">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3212">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3213">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3213">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-3214">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3214">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3215">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3215">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3216">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3216">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3217">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3217">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3218">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3218">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3219">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3219">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3220">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3220">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3221">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3221">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3222">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3222">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3223">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3223">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3224">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3224">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-3225">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3225">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a><span data-ttu-id="ccc12-3226">DXGI_FORMAT_R16 \_ 聖<sup>FNS</sup> (59) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3226">DXGI_FORMAT_R16\_SINT<sup>FNS</sup> (59)</span></span>
| <span data-ttu-id="ccc12-3227">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3227">Target</span></span> | <span data-ttu-id="ccc12-3228">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3228">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3229">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3229">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3230">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-3230">16</span></span> |
| <span data-ttu-id="ccc12-3231">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3231">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-3232">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3232">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3233">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3233">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3234">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3234">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3235">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3235">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3236">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3236">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3237">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3237">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-3238">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3238">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3239">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-3240">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3240">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-3241">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3241">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3242">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3242">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3243">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3243">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3244">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3244">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3245">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3245">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3246">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3246">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-3247">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3247">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3248">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3248">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3249">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3249">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3250">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3250">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3251">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3251">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3252">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3252">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3253">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3253">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3254">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3254">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3255">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3255">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3256">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3256">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3257">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3257">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3258">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3258">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3259">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3259">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3260">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3260">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3261">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3261">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3262">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3262">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3263">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3263">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-3264">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3264">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3265">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3265">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3266">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3266">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3267">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3267">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3268">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3268">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3269">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3269">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3270">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3270">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3271">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3271">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3272">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3272">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3273">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3273">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3274">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3274">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-3275">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3275">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="ccc12-3276">DXGI_FORMAT_R8 無的 \_ <sup>電腦</sup> (60) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3276">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="ccc12-3277">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3277">Target</span></span> | <span data-ttu-id="ccc12-3278">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3278">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3279">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3279">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3280">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-3280">8</span></span> |
| <span data-ttu-id="ccc12-3281">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3281">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-3282">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3282">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3283">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3283">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3284">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3284">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3285">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3285">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3286">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3286">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3287">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3287">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-3288">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3288">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3289">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3289">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-3290">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3290">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-3291">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3291">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3292">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3293">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3294">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3294">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3295">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3295">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3296">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3296">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-3297">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3297">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3298">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3298">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3299">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3299">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3300">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3300">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3301">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3301">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3302">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3302">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3303">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3303">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3304">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3304">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3305">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3305">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3306">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3306">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3307">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3307">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3308">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3308">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3309">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3309">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3310">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3310">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3311">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3311">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3312">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3312">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3313">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3313">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-3314">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3314">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3315">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3315">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3316">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3316">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3317">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3317">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3318">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3318">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3319">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3319">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3320">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3320">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3321">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3321">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3322">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3322">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3323">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3323">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3324">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3324">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-3325">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3325">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a><span data-ttu-id="ccc12-3326">DXGI_FORMAT_R8 \_ UNORM<sup>FNS</sup> (61) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3326">DXGI_FORMAT_R8\_UNORM<sup>FNS</sup> (61)</span></span>
| <span data-ttu-id="ccc12-3327">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3327">Target</span></span> | <span data-ttu-id="ccc12-3328">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3328">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3329">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3329">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3330">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-3330">8</span></span> |
| <span data-ttu-id="ccc12-3331">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3331">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3333">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3333">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3334">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3334">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3335">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3335">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3336">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3336">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3337">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3337">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3338">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3338">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3340">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3340">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3342">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3342">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3344">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3344">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3346">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3346">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3348">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3348">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3349">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3349">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3350">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3350">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3351">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3351">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3352">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3352">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3354">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3354">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3355">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3355">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3357">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3357">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3359">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3359">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3360">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3360">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3361">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3361">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3362">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3362">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3363">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3363">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3364">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3364">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3365">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3365">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3366">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3366">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3367">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3367">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3368">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3368">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3369">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3369">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3370">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3370">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3371">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3371">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3372">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3372">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3374">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3374">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3375">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3375">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3376">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3376">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3377">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3377">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3378">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3378">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3379">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3379">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3380">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3380">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3381">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3381">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3382">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3382">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3383">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3383">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3384">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3384">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3386">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3386">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a><span data-ttu-id="ccc12-3387">DXGI_FORMAT_R8 \_ UINT<sup>FNS</sup> (62) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3387">DXGI_FORMAT_R8\_UINT<sup>FNS</sup> (62)</span></span>
| <span data-ttu-id="ccc12-3388">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3388">Target</span></span> | <span data-ttu-id="ccc12-3389">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3389">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3390">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3390">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3391">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-3391">8</span></span> |
| <span data-ttu-id="ccc12-3392">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3392">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-3393">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3393">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3394">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3394">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3395">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3395">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3396">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3396">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3397">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3397">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3398">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3398">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-3399">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3399">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3400">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3400">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-3401">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3401">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-3402">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3402">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3403">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3403">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3404">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3404">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3405">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3405">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3406">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3406">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3407">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3407">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-3408">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3408">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3409">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3409">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3410">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3410">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3411">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3411">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3412">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3412">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3413">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3413">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3414">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3414">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3415">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3415">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3416">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3416">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3417">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3417">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3418">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3418">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3419">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3419">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3420">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3420">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3421">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3421">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3422">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3422">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3423">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3423">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3424">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3424">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-3425">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3425">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3426">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3426">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3427">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3427">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3428">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3428">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3429">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3429">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3430">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3430">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3431">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3431">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3432">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3432">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3433">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3433">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3434">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3434">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3435">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3435">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-3436">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3436">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a><span data-ttu-id="ccc12-3437">DXGI_FORMAT_R8 \_ SNORM<sup>FNS</sup> (63) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3437">DXGI_FORMAT_R8\_SNORM<sup>FNS</sup> (63)</span></span>
| <span data-ttu-id="ccc12-3438">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3438">Target</span></span> | <span data-ttu-id="ccc12-3439">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3439">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3440">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3440">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3441">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-3441">8</span></span> |
| <span data-ttu-id="ccc12-3442">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3442">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-3443">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3443">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3444">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3444">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3445">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3446">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3447">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3448">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-3449">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3449">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3450">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3450">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-3451">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3451">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-3452">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3452">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3453">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3454">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3455">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3455">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3456">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3457">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3457">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-3458">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3458">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3459">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3459">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3460">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3460">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3461">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3461">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3462">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3462">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3463">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3463">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3464">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3464">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3465">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3465">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3466">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3466">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3467">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3467">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3468">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3468">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3469">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3469">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3470">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3470">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3471">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3471">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3472">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3472">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3473">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3473">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3474">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3474">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-3475">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3475">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3476">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3476">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3477">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3477">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3478">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3478">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3479">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3479">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3480">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3480">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3481">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3481">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3482">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3482">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3483">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3483">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3484">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3484">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3485">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3485">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-3486">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3486">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a><span data-ttu-id="ccc12-3487">DXGI_FORMAT_R8 \_ 聖<sup>FNS</sup> (64) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3487">DXGI_FORMAT_R8\_SINT<sup>FNS</sup> (64)</span></span>
| <span data-ttu-id="ccc12-3488">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3488">Target</span></span> | <span data-ttu-id="ccc12-3489">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3489">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3490">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3490">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3491">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-3491">8</span></span> |
| <span data-ttu-id="ccc12-3492">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3492">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-3493">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3493">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3494">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3494">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3495">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3495">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3496">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3496">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3497">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3497">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3498">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3498">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-3499">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3499">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3500">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3500">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-3501">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3501">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-3502">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3502">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3503">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3503">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3504">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3504">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3505">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3505">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3506">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3506">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3507">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3507">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-3508">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3508">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3509">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3509">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3510">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3510">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3511">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3511">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3512">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3512">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3513">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3513">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3514">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3514">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3515">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3515">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3516">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3516">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3517">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3517">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3518">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3518">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3519">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3519">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3520">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3520">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3521">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3521">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3522">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3522">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3523">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3523">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3524">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3524">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-3525">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3525">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3526">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3526">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3527">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3527">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3528">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3528">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3529">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3529">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3530">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3530">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3531">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3531">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3532">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3532">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3533">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3533">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3534">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3534">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3535">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3535">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-3536">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3536">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="ccc12-3537">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3537">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="ccc12-3538">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3538">Target</span></span> | <span data-ttu-id="ccc12-3539">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3539">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3540">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3540">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3541">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-3541">8</span></span> |
| <span data-ttu-id="ccc12-3542">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3542">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3544">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3544">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3545">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3545">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3546">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3546">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3547">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3547">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3548">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3548">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3549">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3549">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3551">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3551">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3552">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3552">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-3553">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3553">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3555">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3555">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3557">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3557">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3558">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3558">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3559">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3559">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3560">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3560">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3561">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3561">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-3562">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3562">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3563">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3563">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3565">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3565">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3567">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3567">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3568">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3568">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3569">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3569">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3570">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3570">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3571">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3571">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3572">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3572">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3573">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3573">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3574">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3574">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3575">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3575">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3576">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3576">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3577">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3577">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3578">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3578">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3579">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3579">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3580">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3580">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3582">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3582">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3583">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3583">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3584">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3584">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3585">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3585">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3586">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3586">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3587">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3587">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3588">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3588">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3589">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3590">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3591">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3592">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3592">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3594">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="ccc12-3595">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3595">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="ccc12-3596">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3596">Target</span></span> | <span data-ttu-id="ccc12-3597">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3597">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3598">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3599">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-3599">32</span></span> |
| <span data-ttu-id="ccc12-3600">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3600">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-3601">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3601">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3602">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3602">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3603">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3603">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3604">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3604">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3605">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3605">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3606">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3606">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-3607">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3607">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3608">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3608">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-3609">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3609">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-3610">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3610">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3611">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3611">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3612">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3612">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3613">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3613">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3614">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3614">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3615">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3615">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-3616">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3616">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3617">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3617">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3618">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3618">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3619">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3619">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3620">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3620">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3621">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3621">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3622">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3622">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3623">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3623">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3624">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3624">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3625">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3625">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3626">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3626">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3627">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3627">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3628">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3628">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3629">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3629">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3630">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3630">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3631">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3631">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3632">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3632">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-3633">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3633">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3634">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3634">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3635">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3635">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3636">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3636">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3637">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3637">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3638">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3638">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3639">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3639">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3640">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3640">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3641">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3641">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3642">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3642">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3643">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3643">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-3644">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3644">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="ccc12-3645">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3645">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="ccc12-3646">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3646">Target</span></span> | <span data-ttu-id="ccc12-3647">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3647">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3648">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3648">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3649">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-3649">16</span></span> |
| <span data-ttu-id="ccc12-3650">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3650">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-3651">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3651">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3652">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3652">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3653">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3653">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3654">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3654">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3655">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3655">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3656">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3656">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-3657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3657">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3658">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3658">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-3659">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3659">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-3660">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3660">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3661">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3661">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3662">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3662">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3663">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3663">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3664">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3664">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3665">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3665">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-3666">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3666">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3667">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3667">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3668">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3668">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3669">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3669">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3670">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3670">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3671">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3671">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3672">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3672">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3673">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3673">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3674">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3674">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3675">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3675">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3676">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3676">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3677">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3677">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3678">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3678">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3679">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3679">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3680">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3680">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3681">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3681">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3682">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3682">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-3683">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3683">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3684">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3684">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3685">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3685">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3686">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3686">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3687">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3687">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3688">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3688">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3689">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3689">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3690">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3690">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3691">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3691">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3692">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3692">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3693">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3693">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-3694">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3694">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="ccc12-3695">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3695">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="ccc12-3696">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3696">Target</span></span> | <span data-ttu-id="ccc12-3697">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3697">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3698">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3698">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3699">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-3699">16</span></span> |
| <span data-ttu-id="ccc12-3700">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3700">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-3701">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3701">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3702">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3702">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3703">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3703">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3704">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3704">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3705">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3705">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3706">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3706">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-3707">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3707">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3708">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3708">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-3709">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3709">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-3710">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3710">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3711">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3711">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3712">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3712">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3713">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3713">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3714">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3714">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3715">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3715">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-3716">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3716">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3717">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3717">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3718">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3718">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3719">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3719">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3720">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3720">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3721">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3721">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3722">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3722">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3723">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3723">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3724">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3724">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3725">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3725">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3726">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3726">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3727">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3727">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3728">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3728">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3729">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3729">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3730">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3730">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3731">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3731">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3732">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3732">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-3733">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3733">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3734">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3734">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3735">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3735">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3736">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3736">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3737">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3737">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3738">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3738">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3739">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3739">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3740">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3740">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3741">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3741">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3742">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3742">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3743">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3743">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-3744">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3744">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="ccc12-3745">DXGI_FORMAT_BC1 無別 \_ <sup>PCC</sup> (70) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3745">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="ccc12-3746">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3746">Target</span></span> | <span data-ttu-id="ccc12-3747">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3747">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3748">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3748">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3749">4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3749">4</span></span> |
| <span data-ttu-id="ccc12-3750">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3750">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-3751">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3751">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3752">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3752">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3753">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3753">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3754">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3754">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3755">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3755">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3756">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3756">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-3757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3757">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3758">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3758">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-3759">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3759">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-3760">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3760">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3761">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3761">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3762">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3762">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3763">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3763">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3764">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3764">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3765">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3765">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-3766">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3766">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3767">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3767">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3768">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3768">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3769">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3769">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3770">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3770">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3771">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3771">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3772">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3772">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3773">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3773">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3774">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3774">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3775">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3775">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3776">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3776">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3777">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3777">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3778">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3778">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3779">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3779">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3780">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3780">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3781">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3781">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3782">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3782">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-3783">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3783">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3784">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3784">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3785">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3785">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3786">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3786">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3787">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3787">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3788">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3788">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3789">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3789">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3790">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3790">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3791">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3791">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3792">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3792">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3793">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3793">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-3794">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3794">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a><span data-ttu-id="ccc12-3795">DXGI_FORMAT_BC1 \_ UNORM<sup>FNC</sup> (71) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3795">DXGI_FORMAT_BC1\_UNORM<sup>FNC</sup> (71)</span></span>
| <span data-ttu-id="ccc12-3796">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3796">Target</span></span> | <span data-ttu-id="ccc12-3797">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3797">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3798">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3798">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3799">4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3799">4</span></span> |
| <span data-ttu-id="ccc12-3800">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3800">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3802">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3802">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3803">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3803">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3804">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3804">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3805">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3805">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3806">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3806">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3807">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3807">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3809">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3809">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3810">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3810">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3812">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3812">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3814">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3814">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3816">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3816">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3817">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3817">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3818">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3818">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3819">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3819">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3820">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3820">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3822">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3822">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3823">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3823">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3824">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3824">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3825">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3825">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3826">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3826">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3827">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3827">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3828">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3828">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3829">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3829">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3830">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3830">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3831">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3831">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3832">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3832">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3833">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3833">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3834">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3834">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3835">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3835">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3836">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3836">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3837">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3837">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3838">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3838">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3840">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3840">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3841">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3841">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3842">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3842">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3843">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3843">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3844">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3844">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3845">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3845">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3846">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3846">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3847">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3847">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3848">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3848">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3849">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3849">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3850">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3850">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3852">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3852">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a><span data-ttu-id="ccc12-3853">DXGI_FORMAT_BC1 \_ UNORM \_ SRGB<sup>FNC</sup> (72) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3853">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FNC</sup> (72)</span></span>
| <span data-ttu-id="ccc12-3854">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3854">Target</span></span> | <span data-ttu-id="ccc12-3855">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3855">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3856">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3856">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3857">4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3857">4</span></span> |
| <span data-ttu-id="ccc12-3858">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3858">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3860">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3860">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3861">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3861">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3862">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3862">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3863">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3863">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3864">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3864">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3865">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3865">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3867">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3867">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3868">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3868">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3870">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3870">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3872">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3872">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3874">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3874">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3875">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3875">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3876">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3876">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3877">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3877">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3878">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3878">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3880">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3880">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3881">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3881">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3882">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3883">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3884">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3885">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3886">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3887">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3887">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3888">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3888">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3889">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3889">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3890">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3890">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3891">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3891">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3892">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3892">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3893">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3893">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3894">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3894">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3895">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3895">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3896">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3896">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3898">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3898">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3899">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3899">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3900">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3900">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3901">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3901">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3902">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3902">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3903">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3903">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3904">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3904">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3905">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3905">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3906">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3906">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3907">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3907">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3908">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3908">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3910">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3910">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="ccc12-3911">DXGI_FORMAT_BC2 無別 \_ <sup>PCC</sup> (73) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3911">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="ccc12-3912">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3912">Target</span></span> | <span data-ttu-id="ccc12-3913">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3913">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3914">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3914">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3915">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-3915">8</span></span> |
| <span data-ttu-id="ccc12-3916">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3916">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-3917">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3917">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3918">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3918">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3919">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3919">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3920">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3920">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3921">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3921">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3922">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3922">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-3923">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3923">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3924">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3924">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-3925">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3925">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-3926">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3926">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3927">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3927">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3928">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3928">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3929">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3929">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3930">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3930">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3931">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3931">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-3932">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3932">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3933">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3933">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3934">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3934">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3935">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3935">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3936">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3936">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3937">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3937">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3938">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3938">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3939">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3939">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3940">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3940">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3941">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3941">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3942">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3942">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3943">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3943">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-3944">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-3944">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-3945">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-3945">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-3946">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3946">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3947">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-3947">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-3948">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-3948">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-3949">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3949">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3950">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3950">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3951">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-3951">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-3952">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-3952">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-3953">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3953">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-3954">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-3954">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-3955">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-3955">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-3956">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3956">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-3957">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3957">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-3958">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-3958">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-3959">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3959">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-3960">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-3960">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a><span data-ttu-id="ccc12-3961">DXGI_FORMAT_BC2 \_ UNORM<sup>FNC</sup> (74) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3961">DXGI_FORMAT_BC2\_UNORM<sup>FNC</sup> (74)</span></span>
| <span data-ttu-id="ccc12-3962">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3962">Target</span></span> | <span data-ttu-id="ccc12-3963">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3963">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-3964">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3964">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-3965">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-3965">8</span></span> |
| <span data-ttu-id="ccc12-3966">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-3966">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3968">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-3968">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3969">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3969">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3970">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3970">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3971">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3971">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-3972">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3972">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-3973">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3973">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3975">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-3975">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-3976">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-3976">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3978">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3978">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3980">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3980">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3982">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3982">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3983">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-3983">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-3984">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-3984">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-3985">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-3985">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-3986">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-3986">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-3988">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-3988">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-3989">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3989">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3990">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-3990">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-3991">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-3991">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-3992">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-3992">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-3993">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3993">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3994">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3994">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-3995">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-3995">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-3996">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-3996">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-3997">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-3997">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-3998">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-3998">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-3999">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-3999">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4000">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4000">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4001">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4001">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4002">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4002">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4003">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4003">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4004">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4004">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4006">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4006">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4007">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4007">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4008">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4008">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-4009">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4009">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-4010">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4010">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4011">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4011">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-4012">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4012">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4013">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4013">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4014">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4014">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-4015">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4015">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-4016">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4016">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4018">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4018">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a><span data-ttu-id="ccc12-4019">DXGI_FORMAT_BC2 \_ UNORM \_ SRGB<sup>FNC</sup> (75) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4019">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FNC</sup> (75)</span></span>
| <span data-ttu-id="ccc12-4020">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4020">Target</span></span> | <span data-ttu-id="ccc12-4021">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4021">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4022">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4022">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4023">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-4023">8</span></span> |
| <span data-ttu-id="ccc12-4024">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4024">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4026">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4026">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4027">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4027">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4028">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4028">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4029">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4029">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4030">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4030">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4031">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4031">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4033">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4033">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-4034">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4034">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4036">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4036">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4038">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4038">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4040">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4040">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4041">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4041">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4042">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4042">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4043">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4043">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4044">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4044">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4046">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4046">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-4047">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4047">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4048">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4048">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4049">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-4049">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-4050">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4050">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-4051">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4051">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4052">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4052">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4053">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4053">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-4054">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4054">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-4055">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4055">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-4056">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-4056">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-4057">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-4057">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4058">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4058">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4059">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4059">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4060">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4060">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4061">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4061">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4062">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4062">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4064">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4064">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4065">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4065">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4066">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4066">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-4067">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4067">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-4068">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4068">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4069">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4069">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-4070">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4070">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4071">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4071">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4072">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4072">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-4073">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4073">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-4074">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4074">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4076">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4076">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="ccc12-4077">DXGI_FORMAT_BC3 無別 \_ <sup>PCC</sup> (76) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4077">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="ccc12-4078">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4078">Target</span></span> | <span data-ttu-id="ccc12-4079">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4079">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4080">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4080">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4081">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-4081">8</span></span> |
| <span data-ttu-id="ccc12-4082">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4082">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-4083">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4083">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4084">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4085">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4086">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4087">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4088">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4088">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-4089">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4089">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-4090">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4090">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-4091">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4091">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-4092">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4092">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4093">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4093">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4094">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4094">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4095">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4095">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4096">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4096">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4097">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4097">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-4098">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4098">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-4099">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4099">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4100">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4100">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4101">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-4101">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-4102">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4102">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-4103">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4103">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4104">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4104">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4105">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4105">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-4106">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4106">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-4107">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4107">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-4108">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-4108">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-4109">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-4109">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4110">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4110">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4111">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4111">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4112">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4112">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4113">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4113">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4114">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4114">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-4115">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4115">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4116">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4116">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4117">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4117">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-4118">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4118">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-4119">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4119">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4120">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4120">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-4121">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4121">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4122">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4122">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4123">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4123">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-4124">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4124">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-4125">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4125">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-4126">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4126">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a><span data-ttu-id="ccc12-4127">DXGI_FORMAT_BC3 \_ UNORM<sup>FNC</sup> (77) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4127">DXGI_FORMAT_BC3\_UNORM<sup>FNC</sup> (77)</span></span>
| <span data-ttu-id="ccc12-4128">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4128">Target</span></span> | <span data-ttu-id="ccc12-4129">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4129">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4130">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4130">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4131">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-4131">8</span></span> |
| <span data-ttu-id="ccc12-4132">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4132">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4134">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4134">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4135">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4135">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4136">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4136">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4137">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4137">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4138">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4139">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4139">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4141">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-4142">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4142">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4144">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4144">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4146">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4146">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4148">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4148">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4149">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4149">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4150">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4150">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4151">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4151">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4152">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4152">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4154">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4154">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-4155">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4155">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4156">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4156">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4157">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-4157">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-4158">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4158">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-4159">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4159">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4160">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4160">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4161">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4161">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-4162">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4162">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-4163">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4163">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-4164">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-4164">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-4165">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-4165">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4166">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4166">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4167">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4167">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4168">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4168">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4169">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4169">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4170">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4170">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4172">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4172">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4173">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4173">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4174">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4174">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-4175">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4175">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-4176">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4176">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4177">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4177">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-4178">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4178">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4179">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4179">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4180">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4180">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-4181">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4181">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-4182">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4182">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4184">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4184">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a><span data-ttu-id="ccc12-4185">DXGI_FORMAT_BC3 \_ UNORM \_ SRGB<sup>FNC</sup> (78) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4185">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FNC</sup> (78)</span></span>
| <span data-ttu-id="ccc12-4186">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4186">Target</span></span> | <span data-ttu-id="ccc12-4187">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4187">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4188">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4188">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4189">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-4189">8</span></span> |
| <span data-ttu-id="ccc12-4190">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4190">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4192">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4192">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4193">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4193">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4194">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4194">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4195">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4195">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4196">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4196">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4197">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4197">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4199">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4199">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-4200">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4200">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4202">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4202">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4204">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4204">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4206">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4206">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4207">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4207">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4208">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4208">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4209">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4209">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4210">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4210">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4212">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4212">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-4213">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4213">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4214">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4214">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4215">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-4215">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-4216">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4216">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-4217">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4217">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4218">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4218">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4219">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4219">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-4220">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4220">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-4221">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4221">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-4222">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-4222">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-4223">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-4223">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4224">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4224">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4225">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4225">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4226">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4226">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4227">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4227">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4228">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4228">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4230">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4230">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4231">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4231">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4232">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4232">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-4233">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4233">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-4234">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4234">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4235">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4235">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-4236">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4236">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4237">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4237">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4238">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4238">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-4239">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4239">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-4240">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4240">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4242">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4242">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="ccc12-4243">DXGI_FORMAT_BC4 無別 \_ <sup>PCC</sup> (79) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4243">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="ccc12-4244">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4244">Target</span></span> | <span data-ttu-id="ccc12-4245">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4245">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4246">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4246">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4247">4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4247">4</span></span> |
| <span data-ttu-id="ccc12-4248">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4248">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-4249">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4249">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4250">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4250">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4251">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4251">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4252">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4252">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4253">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4253">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4254">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4254">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-4255">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4255">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-4256">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4256">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-4257">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4257">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-4258">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4258">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4259">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4260">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4261">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4261">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4262">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4263">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4263">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-4264">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4264">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-4265">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4265">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4266">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4266">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4267">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-4267">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-4268">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4268">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-4269">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4269">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4270">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4270">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4271">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4271">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-4272">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4272">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-4273">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4273">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-4274">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-4274">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-4275">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-4275">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4276">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4276">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4277">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4277">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4278">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4278">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4279">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4279">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4280">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4280">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-4281">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4281">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4282">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4282">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4283">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4283">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-4284">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4284">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-4285">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4285">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4286">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4286">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-4287">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4287">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4288">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4288">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4289">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4289">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-4290">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4290">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-4291">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4291">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-4292">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4292">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a><span data-ttu-id="ccc12-4293">DXGI_FORMAT_BC4 \_ UNORM<sup>FNC</sup> (80) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4293">DXGI_FORMAT_BC4\_UNORM<sup>FNC</sup> (80)</span></span>
| <span data-ttu-id="ccc12-4294">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4294">Target</span></span> | <span data-ttu-id="ccc12-4295">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4295">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4296">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4296">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4297">4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4297">4</span></span> |
| <span data-ttu-id="ccc12-4298">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4298">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-4299">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4299">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4300">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4300">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4301">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4301">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4302">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4302">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4303">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4303">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4304">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4304">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-4305">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4305">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-4306">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4306">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-4307">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4307">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-4308">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4308">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4309">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4309">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4310">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4310">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4311">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4311">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4312">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4312">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4313">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4313">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-4314">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4314">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-4315">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4315">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4316">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4316">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4317">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-4317">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-4318">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4318">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-4319">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4319">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4320">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4320">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4321">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4321">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-4322">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4322">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-4323">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4323">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-4324">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-4324">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-4325">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-4325">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4326">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4326">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4327">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4327">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4328">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4328">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4329">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4329">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4330">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4330">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-4331">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4331">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4332">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4332">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4333">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4333">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-4334">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4334">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-4335">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4335">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4336">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4336">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-4337">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4337">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4338">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4338">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4339">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4339">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-4340">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4340">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-4341">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4341">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-4342">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4342">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a><span data-ttu-id="ccc12-4343">DXGI_FORMAT_BC4 \_ SNORM<sup>FNC</sup> (81) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4343">DXGI_FORMAT_BC4\_SNORM<sup>FNC</sup> (81)</span></span>
| <span data-ttu-id="ccc12-4344">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4344">Target</span></span> | <span data-ttu-id="ccc12-4345">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4345">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4346">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4346">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4347">4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4347">4</span></span> |
| <span data-ttu-id="ccc12-4348">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4348">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-4349">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4349">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4350">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4350">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4351">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4351">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4352">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4352">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4353">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4353">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4354">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4354">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-4355">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4355">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-4356">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4356">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-4357">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4357">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-4358">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4358">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4359">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4359">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4360">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4360">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4361">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4361">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4362">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4362">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4363">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4363">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-4364">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4364">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-4365">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4365">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4366">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4366">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4367">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-4367">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-4368">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4368">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-4369">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4369">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4370">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4370">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4371">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4371">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-4372">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4372">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-4373">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4373">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-4374">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-4374">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-4375">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-4375">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4376">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4376">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4377">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4377">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4378">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4378">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4379">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4379">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4380">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4380">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-4381">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4381">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4382">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4382">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4383">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4383">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-4384">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4384">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-4385">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4385">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4386">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4386">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-4387">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4387">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4388">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4388">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4389">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4389">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-4390">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4390">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-4391">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4391">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-4392">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4392">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="ccc12-4393">DXGI_FORMAT_BC5 無別 \_ <sup>PCC</sup> (82) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4393">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="ccc12-4394">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4394">Target</span></span> | <span data-ttu-id="ccc12-4395">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4395">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4396">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4396">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4397">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-4397">8</span></span> |
| <span data-ttu-id="ccc12-4398">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4398">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-4399">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4399">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4400">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4400">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4401">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4402">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4402">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4403">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4403">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4404">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-4405">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4405">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-4406">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4406">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-4407">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4407">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-4408">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4408">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4409">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4409">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4410">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4410">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4411">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4411">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4412">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4412">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4413">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4413">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-4414">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4414">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-4415">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4415">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4416">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4416">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4417">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-4417">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-4418">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4418">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-4419">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4419">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4420">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4420">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4421">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4421">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-4422">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4422">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-4423">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4423">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-4424">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-4424">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-4425">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-4425">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4426">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4426">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4427">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4427">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4428">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4428">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4429">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4429">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4430">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4430">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-4431">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4431">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4432">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4432">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4433">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4433">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-4434">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4434">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-4435">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4435">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4436">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4436">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-4437">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4437">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4438">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4438">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4439">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4439">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-4440">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4440">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-4441">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4441">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-4442">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4442">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a><span data-ttu-id="ccc12-4443">DXGI_FORMAT_BC5 \_ UNORM<sup>FNC</sup> (83) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4443">DXGI_FORMAT_BC5\_UNORM<sup>FNC</sup> (83)</span></span>
| <span data-ttu-id="ccc12-4444">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4444">Target</span></span> | <span data-ttu-id="ccc12-4445">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4445">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4446">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4446">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4447">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-4447">8</span></span> |
| <span data-ttu-id="ccc12-4448">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4448">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-4449">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4449">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4450">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4451">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4452">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4453">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4454">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4454">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-4455">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4455">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-4456">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4456">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-4457">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4457">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-4458">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4458">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4459">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4459">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4460">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4460">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4461">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4461">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4462">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4462">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4463">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4463">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-4464">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4464">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-4465">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4465">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4466">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4466">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4467">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-4467">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-4468">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4468">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-4469">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4469">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4470">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4470">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4471">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4471">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-4472">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4472">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-4473">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4473">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-4474">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-4474">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-4475">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-4475">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4476">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4476">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4477">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4477">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4478">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4478">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4479">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4479">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4480">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4480">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-4481">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4481">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4482">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4482">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4483">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4483">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-4484">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4484">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-4485">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4485">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4486">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4486">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-4487">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4487">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4488">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4488">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4489">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4489">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-4490">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4490">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-4491">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4491">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-4492">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4492">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a><span data-ttu-id="ccc12-4493">DXGI_FORMAT_BC5 \_ SNORM<sup>FNC</sup> (84) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4493">DXGI_FORMAT_BC5\_SNORM<sup>FNC</sup> (84)</span></span>
| <span data-ttu-id="ccc12-4494">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4494">Target</span></span> | <span data-ttu-id="ccc12-4495">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4495">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4496">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4496">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4497">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-4497">8</span></span> |
| <span data-ttu-id="ccc12-4498">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4498">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-4499">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4499">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4500">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4500">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4501">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4501">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4502">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4502">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4503">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4503">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4504">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4504">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-4505">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4505">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-4506">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4506">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-4507">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4507">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-4508">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4508">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4509">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4509">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4510">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4510">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4511">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4511">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4512">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4512">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4513">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4513">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-4514">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4514">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-4515">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4515">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4516">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4516">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4517">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-4517">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-4518">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4518">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-4519">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4519">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4520">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4520">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4521">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4521">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-4522">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4522">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-4523">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4523">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-4524">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-4524">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-4525">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-4525">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4526">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4526">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4527">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4527">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4528">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4528">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4529">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4529">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4530">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4530">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-4531">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4531">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4532">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4532">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4533">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4533">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-4534">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4534">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-4535">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4535">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4536">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4536">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-4537">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4537">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4538">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4538">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4539">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4539">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-4540">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4540">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-4541">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4541">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-4542">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4542">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="ccc12-4543">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4543">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="ccc12-4544">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4544">Target</span></span> | <span data-ttu-id="ccc12-4545">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4545">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4546">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4546">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4547">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-4547">16</span></span> |
| <span data-ttu-id="ccc12-4548">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4548">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4550">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4550">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4551">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4551">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4552">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4552">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4553">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4553">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4554">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4554">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4555">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4555">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4557">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4557">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-4558">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4558">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4560">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4560">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4562">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4562">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4564">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4564">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4565">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4565">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4566">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4566">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4567">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4567">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4568">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4568">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4570">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4570">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4572">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4572">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4574">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4574">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4576">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-4576">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-4577">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4577">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-4578">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4578">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4579">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4579">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4580">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4580">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-4581">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4581">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-4582">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4582">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-4583">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-4583">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-4584">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-4584">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4585">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4585">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4586">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4586">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4587">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4587">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4588">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4588">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4589">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4589">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4591">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4591">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-4593">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4593">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-4595">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4595">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-4597">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4597">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4599">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4599">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4600">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4600">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-4601">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4601">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4602">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4602">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4603">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4603">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-4604">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4604">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-4605">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4605">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-4606">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4606">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="ccc12-4607">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4607">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="ccc12-4608">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4608">Target</span></span> | <span data-ttu-id="ccc12-4609">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4609">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4610">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4610">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4611">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-4611">16</span></span> |
| <span data-ttu-id="ccc12-4612">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4612">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4614">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4614">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4615">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4615">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4616">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4616">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4617">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4617">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4618">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4618">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4619">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4619">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4621">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4621">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-4622">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4622">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4624">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4624">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4626">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4626">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4628">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4628">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4629">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4629">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4630">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4630">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4631">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4631">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4632">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4632">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4634">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4634">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-4635">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4635">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4636">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4636">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4637">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-4637">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-4638">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4638">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-4639">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4639">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4640">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4640">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4641">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4641">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-4642">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4642">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-4643">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4643">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-4644">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-4644">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-4645">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-4645">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4646">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4646">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4647">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4647">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4648">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4648">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4649">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4649">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4650">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4650">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4652">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4652">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4653">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4653">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4654">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4654">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-4655">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4655">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-4656">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4656">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4657">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4657">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-4658">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4658">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4659">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4659">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4660">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4660">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-4661">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4661">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-4662">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4662">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-4663">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4663">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="ccc12-4664">DXGI_FORMAT_B8G8R8A8 無的 \_ <sup>電腦</sup> (90) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4664">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="ccc12-4665">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4665">Target</span></span> | <span data-ttu-id="ccc12-4666">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4666">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4667">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4667">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4668">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-4668">32</span></span> |
| <span data-ttu-id="ccc12-4669">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4669">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-4670">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4670">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4671">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4671">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4672">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4672">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4673">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4673">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4674">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4674">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4675">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4675">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-4676">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4676">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-4677">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4677">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-4678">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4678">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-4679">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4679">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4680">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4680">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4681">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4681">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4682">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4682">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4683">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4683">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4684">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4684">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-4685">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4685">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-4686">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4686">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4687">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4687">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4688">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-4688">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-4689">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4689">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-4690">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4690">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4691">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4691">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4692">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4692">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-4693">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4693">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-4694">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4694">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-4695">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-4695">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-4696">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-4696">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4697">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4697">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4698">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4698">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4699">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4699">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4700">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4700">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4701">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4701">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-4702">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4702">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4703">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4703">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4704">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4704">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-4705">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4705">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-4706">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4706">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4707">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4707">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-4708">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4708">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4709">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4709">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4710">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4710">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-4711">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4711">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-4712">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4712">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-4713">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4713">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a><span data-ttu-id="ccc12-4714">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FNS</sup> (87) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4714">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FNS</sup> (87)</span></span>
| <span data-ttu-id="ccc12-4715">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4715">Target</span></span> | <span data-ttu-id="ccc12-4716">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4716">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4717">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4717">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4718">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-4718">32</span></span> |
| <span data-ttu-id="ccc12-4719">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4719">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4721">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4721">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4722">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4722">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4723">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4723">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4724">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4724">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4725">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4725">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4726">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4728">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4730">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4730">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4732">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4732">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4734">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4734">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4736">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4736">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4737">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4737">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4738">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4738">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4739">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4739">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4740">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4740">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4742">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4742">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4744">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4744">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4746">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4746">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4748">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-4748">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-4749">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4749">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-4750">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4750">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4751">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4751">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4752">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4752">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-4753">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4753">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-4754">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4754">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-4755">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-4755">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-4756">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-4756">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4757">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4757">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4758">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4758">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4759">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4759">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4760">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4760">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4761">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4761">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4763">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4763">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-4765">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4765">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-4767">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4767">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-4769">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4769">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4771">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4771">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4772">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4772">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4774">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4774">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4775">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4775">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4776">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4776">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-4778">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4778">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4780">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4780">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4782">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a><span data-ttu-id="ccc12-4783">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ SRGB<sup>FNS</sup> (91) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4783">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FNS</sup> (91)</span></span>
| <span data-ttu-id="ccc12-4784">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4784">Target</span></span> | <span data-ttu-id="ccc12-4785">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4785">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4786">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4787">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-4787">32</span></span> |
| <span data-ttu-id="ccc12-4788">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4788">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4790">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4790">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4791">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4791">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4792">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4792">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4793">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4793">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4794">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4794">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4795">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4795">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4797">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4799">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4799">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4801">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4801">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4803">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4803">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4805">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4805">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4806">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4806">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4807">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4807">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4808">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4808">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4809">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4809">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4811">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4811">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4813">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4813">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4815">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4815">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4817">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-4817">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-4818">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4818">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-4819">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4819">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4820">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4820">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4821">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4821">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-4822">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4822">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-4823">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4823">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-4824">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-4824">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-4825">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-4825">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4826">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4826">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4827">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4827">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4828">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4828">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4829">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4829">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4830">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4830">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4832">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4832">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-4834">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4834">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-4836">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4836">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-4838">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4838">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4840">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4840">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4841">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4841">Display Scan-Out</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4843">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4843">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4844">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4844">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4845">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4845">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-4847">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4847">Video Processor Output</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4849">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4849">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4851">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4851">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="ccc12-4852">DXGI_FORMAT_B8G8R8X8 無的 \_ <sup>電腦</sup> (92) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4852">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="ccc12-4853">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4853">Target</span></span> | <span data-ttu-id="ccc12-4854">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4854">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4855">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4855">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4856">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-4856">32</span></span> |
| <span data-ttu-id="ccc12-4857">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4857">Format Support</span></span> | \- |
| <span data-ttu-id="ccc12-4858">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4858">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4859">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4859">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4860">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4861">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4862">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4863">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4863">Texture2D</span></span> | \- |
| <span data-ttu-id="ccc12-4864">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4864">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-4865">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4865">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-4866">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4866">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-4867">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4867">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4868">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4868">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4869">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4869">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4870">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4870">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4871">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4871">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4872">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4872">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-4873">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4873">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-4874">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4874">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4875">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4875">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4876">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-4876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-4877">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-4878">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4879">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4880">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4880">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-4881">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-4882">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-4883">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-4883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-4884">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-4884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4885">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4885">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4886">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4887">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4888">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4889">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4889">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-4890">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4890">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4891">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4891">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-4892">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4892">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-4893">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4893">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-4894">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4894">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4895">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4895">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-4896">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4896">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4897">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4897">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4898">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4898">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-4899">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4899">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-4900">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4900">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-4901">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4901">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a><span data-ttu-id="ccc12-4902">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FNS</sup> (88) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4902">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FNS</sup> (88)</span></span>
| <span data-ttu-id="ccc12-4903">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4903">Target</span></span> | <span data-ttu-id="ccc12-4904">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4904">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4905">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4905">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4906">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-4906">32</span></span> |
| <span data-ttu-id="ccc12-4907">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4907">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4909">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4909">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4910">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4910">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4911">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4911">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4912">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4912">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4913">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4913">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4914">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4914">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4916">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4916">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4918">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4918">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4920">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4920">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4922">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4922">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4924">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4924">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4925">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4925">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4926">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4926">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4927">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4927">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4928">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4928">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4930">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4930">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4932">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4932">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4934">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4934">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4936">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-4936">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-4937">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4937">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-4938">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4938">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4939">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4939">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-4940">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-4940">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-4941">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4941">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-4942">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4942">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-4943">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-4943">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-4944">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-4944">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-4945">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-4945">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-4946">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-4946">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-4947">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4947">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4948">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-4948">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-4949">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-4949">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4951">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4951">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-4953">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-4953">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-4955">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-4955">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-4957">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-4957">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4959">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4959">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-4960">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-4960">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-4961">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-4961">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-4962">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4962">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-4963">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-4963">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-4965">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-4965">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-4967">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4967">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4969">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-4969">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a><span data-ttu-id="ccc12-4970">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ SRGB<sup>FNS</sup> (93) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4970">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FNS</sup> (93)</span></span>
| <span data-ttu-id="ccc12-4971">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-4971">Target</span></span> | <span data-ttu-id="ccc12-4972">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4972">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-4973">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4973">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-4974">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-4974">32</span></span> |
| <span data-ttu-id="ccc12-4975">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-4975">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4977">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-4977">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4978">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4978">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4979">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4979">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4980">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-4980">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-4981">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4981">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-4982">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4982">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4984">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-4984">Texture3D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4986">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-4986">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4988">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4988">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4990">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4990">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4992">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4992">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4993">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-4993">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-4994">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-4994">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-4995">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-4995">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-4996">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-4996">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-4998">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-4998">Mipmap Auto-Generation</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5000">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5000">RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5002">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5002">Blendable RenderTarget</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5004">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-5004">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-5005">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5005">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-5006">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5006">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5007">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5007">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5008">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5008">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-5009">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5009">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-5010">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5010">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-5011">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-5011">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-5012">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-5012">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-5013">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-5013">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-5014">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-5014">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-5015">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5015">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5016">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5016">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5017">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-5017">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5019">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5019">4x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5021">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5021">8x Multisample RenderTarget</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5023">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-5023">Other Multisample Count RT</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5025">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-5025">Multisample Resolve</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5027">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5027">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-5028">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-5028">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-5029">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-5029">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-5030">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5030">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-5031">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5031">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-5032">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-5032">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-5033">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5033">Shared Resource</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5035">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5035">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="ccc12-5036">DXGI_FORMAT_AYUV<sup>V</sup> (100) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5036">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="ccc12-5037">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5037">Target</span></span> | <span data-ttu-id="ccc12-5038">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5038">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-5039">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5039">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-5040">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-5040">32</span></span> |
| <span data-ttu-id="ccc12-5041">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5041">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5043">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-5043">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5044">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5044">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5045">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5045">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5046">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5046">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5047">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5047">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-5048">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5048">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5050">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-5051">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-5051">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-5052">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5052">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-5053">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5053">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5054">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5054">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5055">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5055">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5056">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-5056">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-5057">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-5057">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-5058">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-5058">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-5059">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-5059">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-5060">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5060">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5061">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5061">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5062">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-5062">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-5063">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5063">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-5064">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5064">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5065">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5065">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5066">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5066">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-5067">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5067">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-5068">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5068">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-5069">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-5069">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-5070">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-5070">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-5071">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-5071">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-5072">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-5072">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-5073">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5073">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5074">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5074">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5075">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-5075">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5077">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5077">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5078">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5078">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5079">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-5079">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-5080">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-5080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-5081">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5081">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-5082">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-5082">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-5083">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-5083">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-5084">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5084">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5086">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5086">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5088">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-5088">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5090">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5090">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-5091">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5091">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="ccc12-5092">DXGI_FORMAT_Y410<sup>V</sup> (101) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5092">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="ccc12-5093">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5093">Target</span></span> | <span data-ttu-id="ccc12-5094">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5094">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-5095">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5095">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-5096">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-5096">32</span></span> |
| <span data-ttu-id="ccc12-5097">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5097">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5099">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-5099">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5100">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5100">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5101">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5101">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5102">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5102">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5103">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5103">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-5104">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5104">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5106">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5106">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-5107">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-5107">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-5108">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5108">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-5109">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5109">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5110">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5110">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5111">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5111">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5112">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-5112">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-5113">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-5113">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-5114">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-5114">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-5115">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-5115">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-5116">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5116">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5117">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5117">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5118">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-5118">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-5119">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5119">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-5120">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5120">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5121">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5121">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5122">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5122">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-5123">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5123">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-5124">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5124">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-5125">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-5125">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-5126">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-5126">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-5127">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-5127">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-5128">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-5128">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-5129">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5129">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5130">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5130">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5131">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-5131">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5133">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5133">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5134">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5134">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5135">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-5135">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-5136">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-5136">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-5137">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5137">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-5138">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-5138">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-5139">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-5139">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-5140">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5140">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5142">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5142">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5144">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-5144">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5146">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5146">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-5147">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="ccc12-5148">DXGI_FORMAT_Y416<sup>V</sup> (102) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5148">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="ccc12-5149">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5149">Target</span></span> | <span data-ttu-id="ccc12-5150">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5150">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-5151">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-5152">64</span><span class="sxs-lookup"><span data-stu-id="ccc12-5152">64</span></span> |
| <span data-ttu-id="ccc12-5153">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5153">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5155">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-5155">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5156">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5156">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5157">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5157">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5158">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5158">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5159">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5159">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-5160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5160">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5162">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5162">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-5163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-5163">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-5164">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5164">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-5165">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5165">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5166">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5166">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5167">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5167">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5168">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-5168">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-5169">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-5169">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-5170">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-5170">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-5171">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-5171">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-5172">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5172">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5173">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5173">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5174">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-5174">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-5175">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5175">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-5176">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5176">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5177">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5177">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5178">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5178">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-5179">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5179">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-5180">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5180">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-5181">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-5181">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-5182">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-5182">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-5183">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-5183">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-5184">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-5184">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-5185">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5185">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5186">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5186">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5187">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-5187">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5189">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5189">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5190">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5190">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5191">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-5191">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-5192">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-5192">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-5193">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5193">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-5194">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-5194">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-5195">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-5195">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-5196">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5196">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5198">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5198">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5200">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-5200">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5202">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5202">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-5203">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5203">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="ccc12-5204">DXGI_FORMAT_NV12<sup>V</sup> (103) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5204">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="ccc12-5205">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5205">Target</span></span> | <span data-ttu-id="ccc12-5206">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5206">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-5207">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5207">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-5208">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-5208">8</span></span> |
| <span data-ttu-id="ccc12-5209">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5209">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5211">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-5211">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5212">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5212">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5213">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5213">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5214">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5214">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5215">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5215">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-5216">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5216">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5218">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5218">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-5219">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-5219">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-5220">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5220">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-5221">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5221">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5222">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5222">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5223">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5223">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5224">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-5224">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-5225">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-5225">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-5226">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-5226">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-5227">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-5227">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-5228">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5228">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5229">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5229">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5230">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-5230">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-5231">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5231">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-5232">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5232">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5233">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5233">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5234">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5234">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-5235">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5235">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-5236">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5236">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-5237">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-5237">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-5238">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-5238">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-5239">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-5239">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-5240">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-5240">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-5241">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5241">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5242">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5242">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5243">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-5243">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5245">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5245">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5246">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5246">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5247">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-5247">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-5248">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-5248">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-5249">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5249">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-5250">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-5250">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-5251">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-5251">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-5252">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5252">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5254">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5254">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5256">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-5256">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5258">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5258">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-5259">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5259">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="ccc12-5260">DXGI_FORMAT_P010<sup>V</sup> (104) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5260">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="ccc12-5261">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5261">Target</span></span> | <span data-ttu-id="ccc12-5262">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5262">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-5263">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5263">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-5264">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-5264">16</span></span> |
| <span data-ttu-id="ccc12-5265">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5265">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5267">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-5267">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5268">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5268">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5269">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5269">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5270">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5270">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5271">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5271">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-5272">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5272">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5274">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5274">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-5275">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-5275">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-5276">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5276">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-5277">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5277">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5278">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5278">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5279">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5279">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5280">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-5280">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-5281">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-5281">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-5282">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-5282">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-5283">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-5283">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-5284">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5284">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5285">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5285">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5286">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-5286">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-5287">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5287">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-5288">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5288">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5289">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5289">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5290">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5290">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-5291">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5291">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-5292">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5292">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-5293">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-5293">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-5294">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-5294">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-5295">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-5295">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-5296">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-5296">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-5297">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5297">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5298">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5298">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5299">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-5299">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5301">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5301">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5302">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5302">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5303">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-5303">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-5304">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-5304">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-5305">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5305">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-5306">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-5306">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-5307">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-5307">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-5308">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5308">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5310">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5310">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5312">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-5312">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5314">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5314">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-5315">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5315">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="ccc12-5316">DXGI_FORMAT_P016<sup>V</sup> (105) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5316">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="ccc12-5317">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5317">Target</span></span> | <span data-ttu-id="ccc12-5318">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5318">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-5319">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5319">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-5320">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-5320">16</span></span> |
| <span data-ttu-id="ccc12-5321">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5321">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5323">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-5323">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5324">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5324">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5325">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5325">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5326">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5326">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5327">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5327">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-5328">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5328">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5330">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5330">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-5331">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-5331">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-5332">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5332">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-5333">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5333">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5334">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5334">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5335">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5335">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5336">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-5336">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-5337">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-5337">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-5338">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-5338">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-5339">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-5339">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-5340">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5340">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5341">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5341">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5342">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-5342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-5343">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-5344">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5345">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5346">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5346">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-5347">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-5348">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-5349">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-5349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-5350">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-5350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-5351">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-5351">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-5352">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-5352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-5353">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5354">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5355">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-5355">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5357">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5358">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5359">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-5359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-5360">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-5360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-5361">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5361">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-5362">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-5362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-5363">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-5363">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-5364">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5364">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5366">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5366">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5368">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-5368">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5370">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5370">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-5371">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5371">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="ccc12-5372">DXGI_FORMAT_420 不 \_ 透明的<sup>V</sup> (106) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5372">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="ccc12-5373">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5373">Target</span></span> | <span data-ttu-id="ccc12-5374">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5374">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-5375">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5375">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-5376">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-5376">8</span></span> |
| <span data-ttu-id="ccc12-5377">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5377">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5379">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-5379">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5380">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5380">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5381">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5381">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5382">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5382">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5383">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5383">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-5384">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5384">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5386">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5386">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-5387">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-5387">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-5388">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5388">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-5389">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5389">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5390">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5390">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5391">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5391">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5392">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-5392">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-5393">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-5393">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-5394">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-5394">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-5395">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-5395">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-5396">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5396">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5397">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5397">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5398">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-5398">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-5399">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5399">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-5400">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5400">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5401">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5401">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5402">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5402">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-5403">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5403">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-5404">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5404">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-5405">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-5405">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-5406">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-5406">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-5407">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-5407">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-5408">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-5408">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-5409">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5409">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5410">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5410">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5411">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-5411">CPU Lockable</span></span> | \- |
| <span data-ttu-id="ccc12-5412">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5412">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5413">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5413">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5414">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-5414">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-5415">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-5415">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-5416">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5416">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-5417">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-5417">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-5418">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-5418">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-5419">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5419">Video Decoder Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5421">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5421">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5423">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-5423">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5425">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5425">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-5426">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5426">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="ccc12-5427">DXGI_FORMAT_YUY2<sup>V</sup> (107) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5427">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="ccc12-5428">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5428">Target</span></span> | <span data-ttu-id="ccc12-5429">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5429">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-5430">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5430">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-5431">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-5431">16</span></span> |
| <span data-ttu-id="ccc12-5432">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5432">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5434">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-5434">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5435">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5435">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5436">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5436">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5437">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5437">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5438">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5438">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-5439">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5439">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5441">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5441">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-5442">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-5442">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-5443">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5443">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-5444">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5444">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5445">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5445">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5446">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5446">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5447">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-5447">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-5448">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-5448">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-5449">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-5449">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-5450">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-5450">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-5451">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5451">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5452">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5452">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5453">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-5453">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-5454">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5454">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-5455">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5455">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5456">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5456">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5457">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5457">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-5458">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5458">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-5459">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5459">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-5460">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-5460">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-5461">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-5461">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-5462">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-5462">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-5463">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-5463">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-5464">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5464">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5465">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5465">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5466">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-5466">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5468">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5468">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5469">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5469">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5470">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-5470">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-5471">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-5471">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-5472">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5472">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-5473">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-5473">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-5474">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-5474">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-5475">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5475">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5477">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5477">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5479">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-5479">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5481">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5481">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-5482">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5482">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="ccc12-5483">DXGI_FORMAT_Y210<sup>V</sup> (108) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5483">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="ccc12-5484">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5484">Target</span></span> | <span data-ttu-id="ccc12-5485">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5485">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-5486">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5486">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-5487">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-5487">32</span></span> |
| <span data-ttu-id="ccc12-5488">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5488">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5490">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-5490">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5491">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5491">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5492">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5492">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5493">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5493">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5494">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5494">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-5495">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5495">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5497">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5497">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-5498">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-5498">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-5499">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5499">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-5500">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5500">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5501">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5501">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5502">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5502">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5503">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-5503">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-5504">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-5504">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-5505">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-5505">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-5506">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-5506">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-5507">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5507">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5508">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5508">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5509">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-5509">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-5510">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5510">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-5511">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5511">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5512">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5512">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5513">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5513">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-5514">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5514">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-5515">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5515">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-5516">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-5516">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-5517">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-5517">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-5518">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-5518">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-5519">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-5519">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-5520">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5520">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5521">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5521">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5522">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-5522">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5524">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5524">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5525">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5525">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5526">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-5526">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-5527">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-5527">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-5528">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5528">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-5529">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-5529">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-5530">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-5530">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-5531">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5531">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5533">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5533">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5535">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-5535">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5537">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5537">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-5538">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5538">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="ccc12-5539">DXGI_FORMAT_Y216<sup>V</sup> (109) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5539">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="ccc12-5540">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5540">Target</span></span> | <span data-ttu-id="ccc12-5541">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5541">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-5542">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5542">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-5543">32</span><span class="sxs-lookup"><span data-stu-id="ccc12-5543">32</span></span> |
| <span data-ttu-id="ccc12-5544">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5544">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5546">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-5546">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5547">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5547">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5548">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5548">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5549">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5549">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5550">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5550">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-5551">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5551">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5553">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5553">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-5554">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-5554">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-5555">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5555">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-5556">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5556">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5557">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5557">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5558">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5558">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5559">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-5559">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-5560">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-5560">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-5561">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-5561">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-5562">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-5562">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-5563">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5563">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5564">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5564">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5565">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-5565">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-5566">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5566">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-5567">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5567">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5568">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5568">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5569">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5569">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-5570">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5570">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-5571">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5571">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-5572">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-5572">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-5573">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-5573">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-5574">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-5574">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-5575">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-5575">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-5576">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5576">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5577">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5577">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5578">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-5578">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5580">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5581">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5582">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-5582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-5583">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-5583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-5584">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5584">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-5585">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-5585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-5586">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-5586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-5587">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5587">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5589">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5589">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5591">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-5591">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5593">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5593">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-5594">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="ccc12-5595">DXGI_FORMAT_NV11<sup>V</sup> (110) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5595">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="ccc12-5596">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5596">Target</span></span> | <span data-ttu-id="ccc12-5597">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5597">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-5598">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-5599">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-5599">8</span></span> |
| <span data-ttu-id="ccc12-5600">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5600">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5602">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-5602">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5603">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5603">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5604">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5604">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5605">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5605">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5606">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5606">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-5607">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5607">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5609">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5609">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-5610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-5610">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-5611">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5611">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-5612">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5612">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5613">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5614">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5615">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-5615">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-5616">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-5616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-5617">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-5617">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-5618">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-5618">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-5619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5619">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5620">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5620">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5621">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-5621">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-5622">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5622">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-5623">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5623">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5624">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5624">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5625">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5625">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-5626">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5626">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-5627">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5627">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-5628">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-5628">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-5629">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-5629">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-5630">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-5630">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-5631">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-5631">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-5632">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5632">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5633">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5633">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5634">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-5634">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5636">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5636">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5637">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5637">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5638">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-5638">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-5639">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-5639">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-5640">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5640">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-5641">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-5641">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-5642">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-5642">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-5643">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5643">Video Decoder Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5645">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5645">Video Processor Input</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5647">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-5647">Video Processor Output</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5649">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5649">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-5650">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5650">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="ccc12-5651">DXGI_FORMAT_AI44<sup>V</sup> (111) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5651">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="ccc12-5652">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5652">Target</span></span> | <span data-ttu-id="ccc12-5653">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5653">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-5654">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5654">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-5655">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-5655">8</span></span> |
| <span data-ttu-id="ccc12-5656">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5656">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5658">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-5658">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5659">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5659">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5660">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5660">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5661">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5661">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5662">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5662">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-5663">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5663">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5665">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5665">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-5666">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-5666">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-5667">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5667">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-5668">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5668">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5669">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5669">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5670">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5670">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5671">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-5671">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-5672">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-5672">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-5673">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-5673">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-5674">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-5674">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-5675">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5675">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5676">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5676">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5677">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-5677">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-5678">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5678">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-5679">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5679">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5680">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5680">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5681">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5681">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-5682">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5682">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-5683">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5683">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-5684">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-5684">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-5685">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-5685">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-5686">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-5686">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-5687">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-5687">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-5688">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5688">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5689">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5689">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5690">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-5690">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5692">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5692">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5693">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5693">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5694">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-5694">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-5695">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-5695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-5696">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5696">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-5697">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-5697">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-5698">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-5698">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-5699">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5699">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-5700">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5700">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5702">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-5702">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-5703">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5703">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-5704">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5704">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="ccc12-5705">DXGI_FORMAT_IA44<sup>V</sup> (112) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5705">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="ccc12-5706">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5706">Target</span></span> | <span data-ttu-id="ccc12-5707">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5707">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-5708">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5708">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-5709">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-5709">8</span></span> |
| <span data-ttu-id="ccc12-5710">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5710">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5712">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-5712">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5713">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5713">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5714">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5714">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5715">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5715">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5716">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5716">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-5717">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5717">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5719">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5719">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-5720">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-5720">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-5721">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5721">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-5722">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5722">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5723">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5723">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5724">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5724">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5725">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-5725">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-5726">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-5726">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-5727">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-5727">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-5728">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-5728">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-5729">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5729">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5730">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5730">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5731">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-5731">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-5732">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5732">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-5733">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5733">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5734">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5734">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5735">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5735">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-5736">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5736">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-5737">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5737">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-5738">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-5738">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-5739">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-5739">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-5740">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-5740">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-5741">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-5741">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-5742">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5742">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5743">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5743">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5744">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-5744">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5746">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5746">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5747">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5747">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5748">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-5748">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-5749">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-5749">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-5750">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5750">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-5751">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-5751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-5752">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-5752">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-5753">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5753">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-5754">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5754">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5756">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-5756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-5757">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5757">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-5758">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5758">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="ccc12-5759">DXGI_FORMAT_P8<sup>V</sup> (113) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5759">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="ccc12-5760">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5760">Target</span></span> | <span data-ttu-id="ccc12-5761">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5761">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-5762">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-5763">8</span><span class="sxs-lookup"><span data-stu-id="ccc12-5763">8</span></span> |
| <span data-ttu-id="ccc12-5764">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5764">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5766">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-5766">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5767">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5767">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5768">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5768">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5769">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5769">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5770">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5770">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-5771">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5771">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5773">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5773">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-5774">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-5774">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-5775">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5775">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-5776">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5776">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5777">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5777">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5778">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5778">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5779">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-5779">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-5780">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-5780">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-5781">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-5781">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-5782">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-5782">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-5783">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5783">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5784">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5784">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5785">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-5785">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-5786">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5786">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-5787">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5787">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5788">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5788">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5789">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5789">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-5790">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5790">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-5791">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5791">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-5792">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-5792">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-5793">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-5793">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-5794">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-5794">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-5795">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-5795">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-5796">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5796">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5797">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5797">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5798">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-5798">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5800">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5800">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5801">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5801">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5802">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-5802">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-5803">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-5803">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-5804">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5804">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-5805">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-5805">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-5806">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-5806">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-5807">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5807">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-5808">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5808">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5810">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-5810">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-5811">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5811">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-5812">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5812">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="ccc12-5813">DXGI_FORMAT_A8P8<sup>V</sup> (114) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5813">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="ccc12-5814">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5814">Target</span></span> | <span data-ttu-id="ccc12-5815">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5815">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-5816">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5816">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-5817">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-5817">16</span></span> |
| <span data-ttu-id="ccc12-5818">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5818">Format Support</span></span> | ![選用](images/letter-o.jpg) |
| <span data-ttu-id="ccc12-5820">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-5820">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5821">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5821">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5822">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5822">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5823">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5823">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5824">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5824">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-5825">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5825">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5827">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5827">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-5828">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-5828">TextureCube</span></span> | \- |
| <span data-ttu-id="ccc12-5829">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5829">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="ccc12-5830">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5830">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5831">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5831">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5832">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5832">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5833">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-5833">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-5834">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-5834">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-5835">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-5835">Mipmap</span></span> | \- |
| <span data-ttu-id="ccc12-5836">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-5836">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-5837">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5837">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5838">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5838">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5839">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-5839">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-5840">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5840">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-5841">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5841">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5842">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5842">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5843">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5843">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-5844">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5844">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-5845">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5845">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-5846">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-5846">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-5847">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-5847">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-5848">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-5848">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-5849">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-5849">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-5850">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5850">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5851">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5851">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5852">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-5852">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5854">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5854">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5855">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5855">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5856">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-5856">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-5857">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-5857">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-5858">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5858">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-5859">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-5859">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-5860">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-5860">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-5861">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5861">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-5862">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5862">Video Processor Input</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5864">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-5864">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-5865">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5865">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-5866">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5866">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="ccc12-5867">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5867">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="ccc12-5868">目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5868">Target</span></span> | <span data-ttu-id="ccc12-5869">支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5869">Support</span></span> |
| - | - |
| <span data-ttu-id="ccc12-5870">每個元素的位數 (BPE) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5870">Bits Per Element (BPE)</span></span> | <span data-ttu-id="ccc12-5871">16</span><span class="sxs-lookup"><span data-stu-id="ccc12-5871">16</span></span> |
| <span data-ttu-id="ccc12-5872">格式支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5872">Format Support</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5874">Buffer</span><span class="sxs-lookup"><span data-stu-id="ccc12-5874">Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5875">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5875">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5876">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5876">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5877">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5877">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="ccc12-5878">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5878">Texture1D</span></span> | \- |
| <span data-ttu-id="ccc12-5879">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5879">Texture2D</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5881">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ccc12-5881">Texture3D</span></span> | \- |
| <span data-ttu-id="ccc12-5882">TextureCube</span><span class="sxs-lookup"><span data-stu-id="ccc12-5882">TextureCube</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5884">著色器範例 (point sample only) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5884">Shader sample (point sample only)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5886">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5886">Shader sample (any filter)</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5888">著色 \_ 器範例 c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5888">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5889">著色器範例 (mono 1 位篩選) </span><span class="sxs-lookup"><span data-stu-id="ccc12-5889">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="ccc12-5890">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="ccc12-5890">Shader gather4</span></span> | \- |
| <span data-ttu-id="ccc12-5891">著色器 gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="ccc12-5891">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="ccc12-5892">Mipmap</span><span class="sxs-lookup"><span data-stu-id="ccc12-5892">Mipmap</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5894">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="ccc12-5894">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="ccc12-5895">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5895">RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5896">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5896">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5897">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="ccc12-5897">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="ccc12-5898">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="ccc12-5898">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="ccc12-5899">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5899">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5900">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5900">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="ccc12-5901">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="ccc12-5901">Typed UAV</span></span> | \- |
| <span data-ttu-id="ccc12-5902">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="ccc12-5902">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="ccc12-5903">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5903">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="ccc12-5904">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="ccc12-5904">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="ccc12-5905">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="ccc12-5905">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="ccc12-5906">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="ccc12-5906">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="ccc12-5907">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="ccc12-5907">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="ccc12-5908">UAV 不可部分完成的帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5908">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5909">UAV 不可部分完成的不帶正負號 Min 或 Max</span><span class="sxs-lookup"><span data-stu-id="ccc12-5909">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="ccc12-5910">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="ccc12-5910">CPU Lockable</span></span> | ![必要](images/letter-r.jpg) |
| <span data-ttu-id="ccc12-5912">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5912">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5913">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="ccc12-5913">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="ccc12-5914">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="ccc12-5914">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="ccc12-5915">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="ccc12-5915">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="ccc12-5916">多級載入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5916">Multisample Load</span></span> | \- |
| <span data-ttu-id="ccc12-5917">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="ccc12-5917">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="ccc12-5918">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="ccc12-5918">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="ccc12-5919">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="ccc12-5919">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="ccc12-5920">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="ccc12-5920">Video Processor Input</span></span> | \- |
| <span data-ttu-id="ccc12-5921">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="ccc12-5921">Video Processor Output</span></span> | \- |
| <span data-ttu-id="ccc12-5922">共用資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5922">Shared Resource</span></span> | \- |
| <span data-ttu-id="ccc12-5923">磚資源</span><span class="sxs-lookup"><span data-stu-id="ccc12-5923">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="ccc12-5924">格式化附注</span><span class="sxs-lookup"><span data-stu-id="ccc12-5924">Format notes</span></span>

<span data-ttu-id="ccc12-5925">格式的用途可從一個硬體功能層級變更為下一個硬體功能層級。</span><span class="sxs-lookup"><span data-stu-id="ccc12-5925">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="ccc12-5926"><sup>L</sup> ：無格式的格式</span><span class="sxs-lookup"><span data-stu-id="ccc12-5926"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="ccc12-5927"><sup>電腦</sup> ：部分類型、可轉換和簡單版面配置</span><span class="sxs-lookup"><span data-stu-id="ccc12-5927"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="ccc12-5928"><sup>FCS</sup> ：完整型別、可轉換和 simple 版面配置</span><span class="sxs-lookup"><span data-stu-id="ccc12-5928"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="ccc12-5929"><sup>FNS</sup> ：完全具類型、非可轉換和簡單版面配置</span><span class="sxs-lookup"><span data-stu-id="ccc12-5929"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="ccc12-5930"><sup>PCC</sup> ：部分類型、可轉換和複雜版面配置</span><span class="sxs-lookup"><span data-stu-id="ccc12-5930"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="ccc12-5931"><sup>FCC</sup> ：完整型別、可轉換和複雜的版面配置</span><span class="sxs-lookup"><span data-stu-id="ccc12-5931"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="ccc12-5932"><sup>FNC</sup> ：完整型別、非可轉換和複雜的版面配置</span><span class="sxs-lookup"><span data-stu-id="ccc12-5932"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="ccc12-5933"><sup>V</sup> ：影片格式</span><span class="sxs-lookup"><span data-stu-id="ccc12-5933"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="ccc12-5934">相關主題</span><span class="sxs-lookup"><span data-stu-id="ccc12-5934">Related topics</span></span>

[<span data-ttu-id="ccc12-5935">D3D12 硬體功能等級</span><span class="sxs-lookup"><span data-stu-id="ccc12-5935">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

<span data-ttu-id="ccc12-5936">[針對 Direct3D 功能層級9執行陰影緩衝區](/previous-versions/windows/apps/jj262110(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="ccc12-5936">[Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10))</span></span>

[<span data-ttu-id="ccc12-5937">對應舊版格式</span><span class="sxs-lookup"><span data-stu-id="ccc12-5937">Mapping Legacy Formats</span></span>](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[<span data-ttu-id="ccc12-5938">DXGI 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="ccc12-5938">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
