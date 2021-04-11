---
description: 本節涵蓋如何使用 API 呼叫來檢查 Direct3D 功能等級硬體的格式支援。
ms.assetid: 0C40C73E-06F3-41FA-AA27-2C0B730B357B
title: 檢查硬體功能支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b14f0de50c4236c4fce46ceda1896ee32721c3bd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935867"
---
# <a name="checking-hardware-feature-support"></a><span data-ttu-id="524f7-103">檢查硬體功能支援</span><span class="sxs-lookup"><span data-stu-id="524f7-103">Checking Hardware Feature Support</span></span>

<span data-ttu-id="524f7-104">本節涵蓋如何使用 API 呼叫來檢查 Direct3D 功能等級硬體的格式支援。</span><span class="sxs-lookup"><span data-stu-id="524f7-104">This section covers how to check on Format Support for Direct3D Feature Level Hardware using API calls.</span></span>

<span data-ttu-id="524f7-105">若為 D3D11，請使用 [**ID3D11Device：： CheckFormatSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkformatsupport) ，以程式設計方式驗證先前章節中的資訊。</span><span class="sxs-lookup"><span data-stu-id="524f7-105">For D3D11, use [**ID3D11Device::CheckFormatSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkformatsupport) to programmatically verify the info in the previous sections.</span></span> <span data-ttu-id="524f7-106">若為 D3D12，請使用 [**ID3D12：： CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)。</span><span class="sxs-lookup"><span data-stu-id="524f7-106">For D3D12 use [**ID3D12::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="524f7-107">格式化目標</span><span class="sxs-lookup"><span data-stu-id="524f7-107">Format target</span></span></th>
<th><span data-ttu-id="524f7-108">D3D12</span><span class="sxs-lookup"><span data-stu-id="524f7-108">D3D12</span></span></th>
<th><span data-ttu-id="524f7-109">D3D11</span><span class="sxs-lookup"><span data-stu-id="524f7-109">D3D11</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="524f7-110">Buffer</span><span class="sxs-lookup"><span data-stu-id="524f7-110">Buffer</span></span></td>
<td><span data-ttu-id="524f7-111">D3D12_FORMAT_SUPPORT1_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-111">D3D12_FORMAT_SUPPORT1_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-112">D3D11_FORMAT_SUPPORT_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-112">D3D11_FORMAT_SUPPORT_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-113">輸入組合語言頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="524f7-113">Input Assembler Vertex Buffer</span></span></td>
<td><span data-ttu-id="524f7-114">D3D12_FORMAT_SUPPORT1_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-114">D3D12_FORMAT_SUPPORT1_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-115">D3D11_FORMAT_SUPPORT_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-115">D3D11_FORMAT_SUPPORT_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-116">輸入組合語言索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="524f7-116">Input Assembler Index Buffer</span></span></td>
<td><span data-ttu-id="524f7-117">D3D12_FORMAT_SUPPORT1_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-117">D3D12_FORMAT_SUPPORT1_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-118">D3D11_FORMAT_SUPPORT_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-118">D3D11_FORMAT_SUPPORT_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-119">資料流程輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="524f7-119">Stream Output Buffer</span></span></td>
<td><span data-ttu-id="524f7-120">D3D12_FORMAT_SUPPORT1_SO_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-120">D3D12_FORMAT_SUPPORT1_SO_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-121">D3D11_FORMAT_SUPPORT_SO_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-121">D3D11_FORMAT_SUPPORT_SO_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-122">Texture1D</span><span class="sxs-lookup"><span data-stu-id="524f7-122">Texture1D</span></span></td>
<td><span data-ttu-id="524f7-123">D3D12_FORMAT_SUPPORT1_TEXTURE1D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-123">D3D12_FORMAT_SUPPORT1_TEXTURE1D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-124">D3D11_FORMAT_SUPPORT_TEXTURE1D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-124">D3D11_FORMAT_SUPPORT_TEXTURE1D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-125">Texture2D</span><span class="sxs-lookup"><span data-stu-id="524f7-125">Texture2D</span></span></td>
<td><span data-ttu-id="524f7-126">D3D12_FORMAT_SUPPORT1_TEXTURE2D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-126">D3D12_FORMAT_SUPPORT1_TEXTURE2D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-127">D3D11_FORMAT_SUPPORT_TEXTURE2D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-127">D3D11_FORMAT_SUPPORT_TEXTURE2D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-128">Texture3D</span><span class="sxs-lookup"><span data-stu-id="524f7-128">Texture3D</span></span></td>
<td><span data-ttu-id="524f7-129">D3D12_FORMAT_SUPPORT1_TEXTURE3D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-129">D3D12_FORMAT_SUPPORT1_TEXTURE3D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-130">D3D11_FORMAT_SUPPORT_TEXTURE3D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-130">D3D11_FORMAT_SUPPORT_TEXTURE3D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-131">TextureCube</span><span class="sxs-lookup"><span data-stu-id="524f7-131">TextureCube</span></span></td>
<td><span data-ttu-id="524f7-132">D3D12_FORMAT_SUPPORT1_TEXTURECUBE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-132">D3D12_FORMAT_SUPPORT1_TEXTURECUBE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-133">D3D11_FORMAT_SUPPORT_TEXTURECUBE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-133">D3D11_FORMAT_SUPPORT_TEXTURECUBE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-134">著色器 ld</span><span class="sxs-lookup"><span data-stu-id="524f7-134">Shader ld</span></span></td>
<td><span data-ttu-id="524f7-135">D3D12_FORMAT_SUPPORT1_SHADER_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-135">D3D12_FORMAT_SUPPORT1_SHADER_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-136">D3D11_FORMAT_SUPPORT_SHADER_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-136">D3D11_FORMAT_SUPPORT_SHADER_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-137">著色器範例 (任何篩選) </span><span class="sxs-lookup"><span data-stu-id="524f7-137">Shader sample (any filter)</span></span></td>
<td><span data-ttu-id="524f7-138">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-138">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-139">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-139">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-140">著色器 sample_c (比較篩選) </span><span class="sxs-lookup"><span data-stu-id="524f7-140">Shader sample_c (comparison filter)</span></span></td>
<td><span data-ttu-id="524f7-141">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-141">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-142">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-142">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-143">著色器範例 (mono 1_bit_filter) </span><span class="sxs-lookup"><span data-stu-id="524f7-143">Shader sample (mono 1_bit_filter)</span></span></td>
<td><span data-ttu-id="524f7-144">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-144">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-145">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-145">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-146">著色器 gather4</span><span class="sxs-lookup"><span data-stu-id="524f7-146">Shader gather4</span></span></td>
<td><span data-ttu-id="524f7-147">D3D12_FORMAT_SUPPORT1_SHADER_GATHER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-147">D3D12_FORMAT_SUPPORT1_SHADER_GATHER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-148">D3D11_FORMAT_SUPPORT_SHADER_GATHER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-148">D3D11_FORMAT_SUPPORT_SHADER_GATHER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-149">著色器 gather4_c</span><span class="sxs-lookup"><span data-stu-id="524f7-149">Shader gather4_c</span></span></td>
<td><span data-ttu-id="524f7-150">D3D12_FORMAT_SUPPORT1_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-150">D3D12_FORMAT_SUPPORT1_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-151">D3D11_FORMAT_SUPPORT_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-151">D3D11_FORMAT_SUPPORT_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-152">Mipmap</span><span class="sxs-lookup"><span data-stu-id="524f7-152">Mipmap</span></span></td>
<td><span data-ttu-id="524f7-153">D3D12_FORMAT_SUPPORT1_MIP (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-153">D3D12_FORMAT_SUPPORT1_MIP (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-154">D3D11_FORMAT_SUPPORT_MIP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-154">D3D11_FORMAT_SUPPORT_MIP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-155">Mipmap 自動產生</span><span class="sxs-lookup"><span data-stu-id="524f7-155">Mipmap Auto-Generation</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="524f7-156">D3D12 不再具有專用的 mipmap 產生功能。</span><span class="sxs-lookup"><span data-stu-id="524f7-156">D3D12 no longer has a dedicated mipmap generation functionality.</span></span> <span data-ttu-id="524f7-157">應用程式必須使用著色器自行執行。</span><span class="sxs-lookup"><span data-stu-id="524f7-157">Applications must implement it on their own using shaders.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="524f7-158">D3D11_FORMAT_SUPPORT_MIP_AUTOGEN (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-158">D3D11_FORMAT_SUPPORT_MIP_AUTOGEN (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-159">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="524f7-159">RenderTarget</span></span></td>
<td><span data-ttu-id="524f7-160">D3D12_FORMAT_SUPPORT1_RENDER_TARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-160">D3D12_FORMAT_SUPPORT1_RENDER_TARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-161">D3D11_FORMAT_SUPPORT_RENDER_TARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-161">D3D11_FORMAT_SUPPORT_RENDER_TARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-162">Blendable RenderTarget</span><span class="sxs-lookup"><span data-stu-id="524f7-162">Blendable RenderTarget</span></span></td>
<td><span data-ttu-id="524f7-163">D3D12_FORMAT_SUPPORT1_BLENDABLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-163">D3D12_FORMAT_SUPPORT1_BLENDABLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-164">D3D11_FORMAT_SUPPORT_BLENDABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-164">D3D11_FORMAT_SUPPORT_BLENDABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-165">輸出合併邏輯 Op</span><span class="sxs-lookup"><span data-stu-id="524f7-165">Output Merger Logic Op</span></span></td>
<td><span data-ttu-id="524f7-166">D3D12_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP</span><span class="sxs-lookup"><span data-stu-id="524f7-166">D3D12_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP</span></span></td>
<td><span data-ttu-id="524f7-167">D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-167">D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-168">深度/樣板目標</span><span class="sxs-lookup"><span data-stu-id="524f7-168">Depth/Stencil Target</span></span></td>
<td><span data-ttu-id="524f7-169">D3D12_FORMAT_SUPPORT1_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-169">D3D12_FORMAT_SUPPORT1_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-170">D3D11_FORMAT_SUPPORT_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-170">D3D11_FORMAT_SUPPORT_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-171">原始 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="524f7-171">Raw UAV and SRV</span></span></td>


</tr>
<tr class="even">
<td><span data-ttu-id="524f7-172">結構化 UAV 和 SRV</span><span class="sxs-lookup"><span data-stu-id="524f7-172">Structured UAV and SRV</span></span></td>


</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-173">具類型的 UAV</span><span class="sxs-lookup"><span data-stu-id="524f7-173">Typed UAV</span></span></td>
<td><span data-ttu-id="524f7-174">D3D12_FORMAT_SUPPORT1_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-174">D3D12_FORMAT_SUPPORT1_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-175">D3D11_FORMAT_SUPPORT_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-175">D3D11_FORMAT_SUPPORT_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-176">UAV 具類型的存放區</span><span class="sxs-lookup"><span data-stu-id="524f7-176">UAV Typed Store</span></span></td>
<td><span data-ttu-id="524f7-177">D3D12_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-177">D3D12_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-178">D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-178">D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-179">UAV 具類型的載入</span><span class="sxs-lookup"><span data-stu-id="524f7-179">UAV Typed Load</span></span></td>
<td><span data-ttu-id="524f7-180">D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-180">D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-181">D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-181">D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-182">UAV 不可部分完成的新增</span><span class="sxs-lookup"><span data-stu-id="524f7-182">UAV Atomic Add</span></span></td>
<td><span data-ttu-id="524f7-183">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-183">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-184">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-184">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-185">UAV 不可部分完成的位運算</span><span class="sxs-lookup"><span data-stu-id="524f7-185">UAV Atomic Bitwise Ops</span></span></td>
<td><span data-ttu-id="524f7-186">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-186">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-187">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-187">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-188">UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</span><span class="sxs-lookup"><span data-stu-id="524f7-188">UAV Atomic Cmp&Store/ Cmp&Exch</span></span></td>
<td><span data-ttu-id="524f7-189">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-189">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-190">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-190">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-191">UAV 不可部分完成的交換</span><span class="sxs-lookup"><span data-stu-id="524f7-191">UAV Atomic Exchange</span></span></td>
<td><span data-ttu-id="524f7-192">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-192">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-193">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-193">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-194">UAV 不可部分完成的帶正負號 Min/Max</span><span class="sxs-lookup"><span data-stu-id="524f7-194">UAV Atomic Signed Min/Max</span></span></td>
<td><span data-ttu-id="524f7-195">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-195">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-196">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-196">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-197">UAV 不可部分完成的無符號下限/最大值</span><span class="sxs-lookup"><span data-stu-id="524f7-197">UAV Atomic Unsigned Min/Max</span></span></td>
<td><span data-ttu-id="524f7-198">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-198">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-199">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-199">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-200">CPU 鎖定</span><span class="sxs-lookup"><span data-stu-id="524f7-200">CPU Lockable</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="524f7-201">只有單一格式會防止 cpu 存取 (420_OPAQUE) 。</span><span class="sxs-lookup"><span data-stu-id="524f7-201">Only a single format precludes cpu access (420_OPAQUE).</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="524f7-202">D3D11_FORMAT_SUPPORT_CPU_LOCKABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-202">D3D11_FORMAT_SUPPORT_CPU_LOCKABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-203">4x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="524f7-203">4x Multisample RenderTarget</span></span></td>
<td><span data-ttu-id="524f7-204">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-204">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-205">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-205">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-206">8x 多重採樣 RenderTarget</span><span class="sxs-lookup"><span data-stu-id="524f7-206">8x Multisample RenderTarget</span></span></td>
<td><span data-ttu-id="524f7-207">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-207">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-208">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-208">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-209">其他的多重採樣計數 RT</span><span class="sxs-lookup"><span data-stu-id="524f7-209">Other Multisample Count RT</span></span></td>
<td><span data-ttu-id="524f7-210">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-210">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-211">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-211">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-212">多級取樣解析</span><span class="sxs-lookup"><span data-stu-id="524f7-212">Multisample Resolve</span></span></td>
<td><span data-ttu-id="524f7-213">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-213">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-214">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-214">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-215">多級載入</span><span class="sxs-lookup"><span data-stu-id="524f7-215">Multisample Load</span></span></td>
<td><span data-ttu-id="524f7-216">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-216">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-217">D3D11_FORMAT_SUPPORT_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-217">D3D11_FORMAT_SUPPORT_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-218">顯示 Scan-Out</span><span class="sxs-lookup"><span data-stu-id="524f7-218">Display Scan-Out</span></span></td>
<td><span data-ttu-id="524f7-219">D3D12_FORMAT_SUPPORT1_DISPLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-219">D3D12_FORMAT_SUPPORT1_DISPLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-220">D3D11_FORMAT_SUPPORT_DISPLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-220">D3D11_FORMAT_SUPPORT_DISPLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-221">位配置中的 Cast</span><span class="sxs-lookup"><span data-stu-id="524f7-221">Cast Within Bit Layout</span></span></td>
<td><span data-ttu-id="524f7-222">D3D12_FORMAT_SUPPORT1_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-222">D3D12_FORMAT_SUPPORT1_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-223">D3D11_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-223">D3D11_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-224">影片解碼支援</span><span class="sxs-lookup"><span data-stu-id="524f7-224">Video Decoder Support</span></span></td>
<td><span data-ttu-id="524f7-225">D3D12_FORMAT_SUPPORT1_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-225">D3D12_FORMAT_SUPPORT1_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-226">D3D11_FORMAT_SUPPORT_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-226">D3D11_FORMAT_SUPPORT_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-227">視頻處理器輸入</span><span class="sxs-lookup"><span data-stu-id="524f7-227">Video Processor Input</span></span></td>
<td><span data-ttu-id="524f7-228">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-228">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-229">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-229">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-230">視頻處理器輸出</span><span class="sxs-lookup"><span data-stu-id="524f7-230">Video Processor Output</span></span></td>
<td><span data-ttu-id="524f7-231">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-231">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-232">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-232">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-233">共用資源</span><span class="sxs-lookup"><span data-stu-id="524f7-233">Shared Resource</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="524f7-234">所有格式的材質都可以是共用的已認可資源，也可以放在共用堆積中。</span><span class="sxs-lookup"><span data-stu-id="524f7-234">Textures of all formats may be shared committed resources or be placed in shared heaps.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="524f7-235">D3D11_FORMAT_SUPPORT2_SHAREABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-235">D3D11_FORMAT_SUPPORT2_SHAREABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-236">背景緩衝區可轉換甚至是完整類型</span><span class="sxs-lookup"><span data-stu-id="524f7-236">BackBuffer Castable Even Fully Typed</span></span></td>
<td><span data-ttu-id="524f7-237">D3D12_FORMAT_SUPPORT1_BACK_BUFFER_CAST (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-237">D3D12_FORMAT_SUPPORT1_BACK_BUFFER_CAST (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="524f7-238">沒有任何可用的 API。</span><span class="sxs-lookup"><span data-stu-id="524f7-238">No API available.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-239">磚資源</span><span class="sxs-lookup"><span data-stu-id="524f7-239">Tiled Resource</span></span></td>
<td><span data-ttu-id="524f7-240">D3D12_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-240">D3D12_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-241">D3D11_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-241">D3D11_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="524f7-242">影片編碼器</span><span class="sxs-lookup"><span data-stu-id="524f7-242">Video Encoder</span></span></td>
<td><span data-ttu-id="524f7-243">D3D12_FORMAT_SUPPORT1_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-243">D3D12_FORMAT_SUPPORT1_VIDEO_ENCODER(<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-244">D3D11_FORMAT_SUPPORT_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-244">D3D11_FORMAT_SUPPORT_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="524f7-245">Multiplane 重迭</span><span class="sxs-lookup"><span data-stu-id="524f7-245">Multiplane Overlay</span></span></td>
<td><span data-ttu-id="524f7-246">D3D12_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-246">D3D12_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="524f7-247">D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="524f7-247">D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="524f7-248">相關主題</span><span class="sxs-lookup"><span data-stu-id="524f7-248">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="524f7-249">D3D12 硬體功能等級</span><span class="sxs-lookup"><span data-stu-id="524f7-249">D3D12 Hardware Feature Levels</span></span>](/windows/desktop/direct3d12/hardware-feature-levels)
</dt> <dt>

[<span data-ttu-id="524f7-250">**DXGI \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="524f7-250">**DXGI\_FORMAT**</span></span>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> <dt>

[<span data-ttu-id="524f7-251">**D3D11 \_ 格式 \_ 支援**</span><span class="sxs-lookup"><span data-stu-id="524f7-251">**D3D11\_FORMAT\_SUPPORT**</span></span>](/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support)
</dt> <dt>

[<span data-ttu-id="524f7-252">**D3D11 \_ 格式 \_ SUPPORT2**</span><span class="sxs-lookup"><span data-stu-id="524f7-252">**D3D11\_FORMAT\_SUPPORT2**</span></span>](/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2)
</dt> <dt>

[<span data-ttu-id="524f7-253">DXGI 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="524f7-253">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
</dt> </dl>

