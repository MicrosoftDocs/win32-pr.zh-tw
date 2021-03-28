---
title: 10Level9 >id3d11devicecoNtext 方法
description: 本節將列出每個10Level9 功能等級和 D3D \_ 功能 \_ 等級 \_ 11 \_ 0 和更高的 >id3d11devicecoNtext 方法功能層級之間的差異。
ms.assetid: 84478b56-0306-491a-9545-0849b06d8342
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb3dc46aeeb5d629c4bf50492083d09b34de1b08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020984"
---
# <a name="10level9-id3d11devicecontext-methods"></a><span data-ttu-id="1276e-103">10Level9 >id3d11devicecoNtext 方法</span><span class="sxs-lookup"><span data-stu-id="1276e-103">10Level9 ID3D11DeviceContext Methods</span></span>

<span data-ttu-id="1276e-104">本節將列出每個10Level9 功能等級和 D3D \_ 功能 \_ 等級 \_ 11 \_ 0 和更高的 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 方法功能層級之間的差異。</span><span class="sxs-lookup"><span data-stu-id="1276e-104">This section lists the differences between each 10Level9 feature level and the D3D\_FEATURE\_LEVEL\_11\_0 and higher feature level for the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods.</span></span>

-   [<span data-ttu-id="1276e-105">>id3d11devicecoNtext：： CopySubresourceRegion</span><span class="sxs-lookup"><span data-stu-id="1276e-105">ID3D11DeviceContext::CopySubresourceRegion</span></span>](#id3d11devicecontextcopysubresourceregion)
-   [<span data-ttu-id="1276e-106">>id3d11devicecoNtext：： CopyResource</span><span class="sxs-lookup"><span data-stu-id="1276e-106">ID3D11DeviceContext::CopyResource</span></span>](#id3d11devicecontextcopyresource)
-   [<span data-ttu-id="1276e-107">>id3d11devicecoNtext：： CopyStructureCount</span><span class="sxs-lookup"><span data-stu-id="1276e-107">ID3D11DeviceContext::CopyStructureCount</span></span>](#id3d11devicecontextcopystructurecount)
-   [<span data-ttu-id="1276e-108">>id3d11devicecoNtext：： ClearUnorderedAccessViewFloat</span><span class="sxs-lookup"><span data-stu-id="1276e-108">ID3D11DeviceContext::ClearUnorderedAccessViewFloat</span></span>](#id3d11devicecontextclearunorderedaccessviewfloat)
-   [<span data-ttu-id="1276e-109">>id3d11devicecoNtext：： ClearUnorderedAccessViewUint</span><span class="sxs-lookup"><span data-stu-id="1276e-109">ID3D11DeviceContext::ClearUnorderedAccessViewUint</span></span>](#id3d11devicecontextclearunorderedaccessviewuint)
-   [<span data-ttu-id="1276e-110">>id3d11devicecoNtext：： ClearRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="1276e-110">ID3D11DeviceContext::ClearRenderTargetView</span></span>](#id3d11devicecontextclearrendertargetview)
-   [<span data-ttu-id="1276e-111">>id3d11devicecoNtext：： CSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="1276e-111">ID3D11DeviceContext::CSSetConstantBuffers</span></span>](#id3d11devicecontextcssetconstantbuffers)
-   [<span data-ttu-id="1276e-112">>id3d11devicecoNtext：： CSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="1276e-112">ID3D11DeviceContext::CSSetSamplers</span></span>](#id3d11devicecontextcssetsamplers)
-   [<span data-ttu-id="1276e-113">>id3d11devicecoNtext：： CSSetShader</span><span class="sxs-lookup"><span data-stu-id="1276e-113">ID3D11DeviceContext::CSSetShader</span></span>](#id3d11devicecontextcssetshader)
-   [<span data-ttu-id="1276e-114">>id3d11devicecoNtext：： CSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="1276e-114">ID3D11DeviceContext::CSSetShaderResources</span></span>](#id3d11devicecontextcssetshaderresources)
-   [<span data-ttu-id="1276e-115">>id3d11devicecoNtext：： CSSetUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="1276e-115">ID3D11DeviceContext::CSSetUnorderedAccessViews</span></span>](#id3d11devicecontextcssetunorderedaccessviews)
-   [<span data-ttu-id="1276e-116">>id3d11devicecoNtext：:D ispatch</span><span class="sxs-lookup"><span data-stu-id="1276e-116">ID3D11DeviceContext::Dispatch</span></span>](#id3d11devicecontextdispatch)
-   [<span data-ttu-id="1276e-117">>id3d11devicecoNtext：:D ispatchIndirect</span><span class="sxs-lookup"><span data-stu-id="1276e-117">ID3D11DeviceContext::DispatchIndirect</span></span>](#id3d11devicecontextdispatchindirect)
-   [<span data-ttu-id="1276e-118">ID3D11DeviceContext::Draw</span><span class="sxs-lookup"><span data-stu-id="1276e-118">ID3D11DeviceContext::Draw</span></span>](#id3d11devicecontextdraw)
-   [<span data-ttu-id="1276e-119">ID3D11DeviceContext::DrawAuto</span><span class="sxs-lookup"><span data-stu-id="1276e-119">ID3D11DeviceContext::DrawAuto</span></span>](#id3d11devicecontextdrawauto)
-   [<span data-ttu-id="1276e-120">ID3D11DeviceContext::DrawIndexed</span><span class="sxs-lookup"><span data-stu-id="1276e-120">ID3D11DeviceContext::DrawIndexed</span></span>](#id3d11devicecontextdrawindexed)
-   [<span data-ttu-id="1276e-121">ID3D11DeviceContext::DrawIndexedInstanced</span><span class="sxs-lookup"><span data-stu-id="1276e-121">ID3D11DeviceContext::DrawIndexedInstanced</span></span>](#id3d11devicecontextdrawindexedinstanced)
-   [<span data-ttu-id="1276e-122">>id3d11devicecoNtext：:D rawIndexedInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="1276e-122">ID3D11DeviceContext::DrawIndexedInstancedIndirect</span></span>](#id3d11devicecontextdrawindexedinstancedindirect)
-   [<span data-ttu-id="1276e-123">ID3D11DeviceContext::DrawInstanced</span><span class="sxs-lookup"><span data-stu-id="1276e-123">ID3D11DeviceContext::DrawInstanced</span></span>](#id3d11devicecontextdrawinstanced)
-   [<span data-ttu-id="1276e-124">>id3d11devicecoNtext：:D rawInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="1276e-124">ID3D11DeviceContext::DrawInstancedIndirect</span></span>](#id3d11devicecontextdrawinstancedindirect)
-   [<span data-ttu-id="1276e-125">>id3d11devicecoNtext：:D SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="1276e-125">ID3D11DeviceContext::DSSetConstantBuffers</span></span>](#id3d11devicecontextdssetconstantbuffers)
-   [<span data-ttu-id="1276e-126">>id3d11devicecoNtext：:D SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="1276e-126">ID3D11DeviceContext::DSSetSamplers</span></span>](#id3d11devicecontextdssetsamplers)
-   [<span data-ttu-id="1276e-127">>id3d11devicecoNtext：:D SSetShader</span><span class="sxs-lookup"><span data-stu-id="1276e-127">ID3D11DeviceContext::DSSetShader</span></span>](#id3d11devicecontextdssetshader)
-   [<span data-ttu-id="1276e-128">>id3d11devicecoNtext：:D SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="1276e-128">ID3D11DeviceContext::DSSetShaderResources</span></span>](#id3d11devicecontextdssetshaderresources)
-   [<span data-ttu-id="1276e-129">>id3d11devicecoNtext：： GSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="1276e-129">ID3D11DeviceContext::GSSetConstantBuffers</span></span>](#id3d11devicecontextgssetconstantbuffers)
-   [<span data-ttu-id="1276e-130">>id3d11devicecoNtext：： GSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="1276e-130">ID3D11DeviceContext::GSSetSamplers</span></span>](#id3d11devicecontextgssetsamplers)
-   [<span data-ttu-id="1276e-131">>id3d11devicecoNtext：： GSSetShader</span><span class="sxs-lookup"><span data-stu-id="1276e-131">ID3D11DeviceContext::GSSetShader</span></span>](#id3d11devicecontextgssetshader)
-   [<span data-ttu-id="1276e-132">>id3d11devicecoNtext：： GSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="1276e-132">ID3D11DeviceContext::GSSetShaderResources</span></span>](#id3d11devicecontextgssetshaderresources)
-   [<span data-ttu-id="1276e-133">>id3d11devicecoNtext：： HSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="1276e-133">ID3D11DeviceContext::HSSetConstantBuffers</span></span>](#id3d11devicecontexthssetconstantbuffers)
-   [<span data-ttu-id="1276e-134">>id3d11devicecoNtext：： HSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="1276e-134">ID3D11DeviceContext::HSSetSamplers</span></span>](#id3d11devicecontexthssetsamplers)
-   [<span data-ttu-id="1276e-135">>id3d11devicecoNtext：： HSSetShader</span><span class="sxs-lookup"><span data-stu-id="1276e-135">ID3D11DeviceContext::HSSetShader</span></span>](#id3d11devicecontexthssetshader)
-   [<span data-ttu-id="1276e-136">>id3d11devicecoNtext：： HSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="1276e-136">ID3D11DeviceContext::HSSetShaderResources</span></span>](#id3d11devicecontexthssetshaderresources)
-   [<span data-ttu-id="1276e-137">ID3D11DeviceContext::IASetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="1276e-137">ID3D11DeviceContext::IASetIndexBuffer</span></span>](#id3d11devicecontextiasetindexbuffer)
-   [<span data-ttu-id="1276e-138">ID3D11DeviceContext::IASetPrimitiveTopology</span><span class="sxs-lookup"><span data-stu-id="1276e-138">ID3D11DeviceContext::IASetPrimitiveTopology</span></span>](#id3d11devicecontextiasetprimitivetopology)
-   [<span data-ttu-id="1276e-139">>id3d11devicecoNtext：： OMSetBlendState</span><span class="sxs-lookup"><span data-stu-id="1276e-139">ID3D11DeviceContext::OMSetBlendState</span></span>](#id3d11devicecontextomsetblendstate)
-   [<span data-ttu-id="1276e-140">>id3d11devicecoNtext：： OMSetRenderTargets</span><span class="sxs-lookup"><span data-stu-id="1276e-140">ID3D11DeviceContext::OMSetRenderTargets</span></span>](#id3d11devicecontextomsetrendertargets)
-   [<span data-ttu-id="1276e-141">>id3d11devicecoNtext：： OMSetRenderTargetsAndUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="1276e-141">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</span></span>](#id3d11devicecontextomsetrendertargetsandunorderedaccessviews)
-   [<span data-ttu-id="1276e-142">>id3d11devicecoNtext：:P SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="1276e-142">ID3D11DeviceContext::PSSetConstantBuffers</span></span>](#id3d11devicecontextpssetconstantbuffers)
-   [<span data-ttu-id="1276e-143">>id3d11devicecoNtext：:P SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="1276e-143">ID3D11DeviceContext::PSSetSamplers</span></span>](#id3d11devicecontextpssetsamplers)
-   [<span data-ttu-id="1276e-144">>id3d11devicecoNtext：:P SSetShader</span><span class="sxs-lookup"><span data-stu-id="1276e-144">ID3D11DeviceContext::PSSetShader</span></span>](#id3d11devicecontextpssetshader)
-   [<span data-ttu-id="1276e-145">>id3d11devicecoNtext：:P SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="1276e-145">ID3D11DeviceContext::PSSetShaderResources</span></span>](#id3d11devicecontextpssetshaderresources)
-   [<span data-ttu-id="1276e-146">>id3d11devicecoNtext：： RSSetScissorRects</span><span class="sxs-lookup"><span data-stu-id="1276e-146">ID3D11DeviceContext::RSSetScissorRects</span></span>](#id3d11devicecontextrssetscissorrects)
-   [<span data-ttu-id="1276e-147">>id3d11devicecoNtext：： RSSetViewports</span><span class="sxs-lookup"><span data-stu-id="1276e-147">ID3D11DeviceContext::RSSetViewports</span></span>](#id3d11devicecontextrssetviewports)
-   [<span data-ttu-id="1276e-148">>id3d11devicecoNtext：： SetPredication</span><span class="sxs-lookup"><span data-stu-id="1276e-148">ID3D11DeviceContext::SetPredication</span></span>](#id3d11devicecontextsetpredication)
-   [<span data-ttu-id="1276e-149">>id3d11devicecoNtext：： SOSetTargets</span><span class="sxs-lookup"><span data-stu-id="1276e-149">ID3D11DeviceContext::SOSetTargets</span></span>](#id3d11devicecontextsosettargets)
-   [<span data-ttu-id="1276e-150">>id3d11devicecoNtext：： VSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="1276e-150">ID3D11DeviceContext::VSSetConstantBuffers</span></span>](#id3d11devicecontextvssetconstantbuffers)
-   [<span data-ttu-id="1276e-151">>id3d11devicecoNtext：： VSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="1276e-151">ID3D11DeviceContext::VSSetSamplers</span></span>](#id3d11devicecontextvssetsamplers)
-   [<span data-ttu-id="1276e-152">>id3d11devicecoNtext：： VSSetShader</span><span class="sxs-lookup"><span data-stu-id="1276e-152">ID3D11DeviceContext::VSSetShader</span></span>](#id3d11devicecontextvssetshader)
-   [<span data-ttu-id="1276e-153">>id3d11devicecoNtext：： VSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="1276e-153">ID3D11DeviceContext::VSSetShaderResources</span></span>](#id3d11devicecontextvssetshaderresources)
-   [<span data-ttu-id="1276e-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="1276e-154">Related topics</span></span>](#related-topics)

## <a name="id3d11devicecontextcopysubresourceregion"></a><span data-ttu-id="1276e-155">>id3d11devicecoNtext：： CopySubresourceRegion</span><span class="sxs-lookup"><span data-stu-id="1276e-155">ID3D11DeviceContext::CopySubresourceRegion</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-156">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-156">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-157">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-157">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-158">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-158">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="1276e-159">只有 Texture2D 和緩衝區可在 GPU 可存取的記憶體中複製。</span><span class="sxs-lookup"><span data-stu-id="1276e-159">Only Texture2D and buffers may be copied within GPU-accessible memory.</span></span><br/> <span data-ttu-id="1276e-160">Texture3D 無法從 GPU 可存取的記憶體複製到可存取 CPU 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1276e-160">Texture3D cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="1276e-161">只有 D3D10_BIND_SHADER_RESOURCE 的任何資源都無法從 GPU 可存取的記憶體複製到可存取 CPU 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1276e-161">Any resource that has only D3D10_BIND_SHADER_RESOURCE cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="1276e-162">您無法複製 mipmapped 磁片區紋理。</span><span class="sxs-lookup"><span data-stu-id="1276e-162">You can't copy mipmapped volume textures.</span></span> <br/> <span data-ttu-id="1276e-163">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-163">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-164">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-164">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-165">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-165">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopyresource"></a><span data-ttu-id="1276e-166">>id3d11devicecoNtext：： CopyResource</span><span class="sxs-lookup"><span data-stu-id="1276e-166">ID3D11DeviceContext::CopyResource</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-167">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-167">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-168">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-168">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-169">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-169">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="1276e-170">只有 Texture2D 和緩衝區可在 GPU 可存取的記憶體中複製。</span><span class="sxs-lookup"><span data-stu-id="1276e-170">Only Texture2D and buffers may be copied within GPU-accessible memory.</span></span><br/> <span data-ttu-id="1276e-171">Texture3D 無法從 GPU 可存取的記憶體複製到可存取 CPU 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1276e-171">Texture3D cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="1276e-172">只有 D3D10_BIND_SHADER_RESOURCE 的任何資源都無法從 GPU 可存取的記憶體複製到可存取 CPU 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1276e-172">Any resource that has only D3D10_BIND_SHADER_RESOURCE cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="1276e-173">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-173">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-174">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-174">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-175">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-175">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopystructurecount"></a><span data-ttu-id="1276e-176">>id3d11devicecoNtext：： CopyStructureCount</span><span class="sxs-lookup"><span data-stu-id="1276e-176">ID3D11DeviceContext::CopyStructureCount</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-177">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-177">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-178">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-178">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-179">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-179">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-180">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-180">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-181">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-181">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-182">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-182">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a><span data-ttu-id="1276e-183">>id3d11devicecoNtext：： ClearUnorderedAccessViewFloat</span><span class="sxs-lookup"><span data-stu-id="1276e-183">ID3D11DeviceContext::ClearUnorderedAccessViewFloat</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-184">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-184">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-185">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-185">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-186">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-186">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-187">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-187">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-188">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-188">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-189">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-189">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a><span data-ttu-id="1276e-190">>id3d11devicecoNtext：： ClearUnorderedAccessViewUint</span><span class="sxs-lookup"><span data-stu-id="1276e-190">ID3D11DeviceContext::ClearUnorderedAccessViewUint</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-191">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-191">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-192">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-192">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-193">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-193">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-194">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-194">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-195">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-195">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-196">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-196">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearrendertargetview"></a><span data-ttu-id="1276e-197">>id3d11devicecoNtext：： ClearRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="1276e-197">ID3D11DeviceContext::ClearRenderTargetView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-198">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-198">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-199">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-199">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-200">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-200">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-201">只會清除第一個陣列配量。</span><span class="sxs-lookup"><span data-stu-id="1276e-201">Only the first array slice will be cleared.</span></span> <span data-ttu-id="1276e-202">應用程式應該為每個臉部或陣列配量建立轉譯目標視圖，然後個別清除每個視圖。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-202">Applications should create a render target view for each face or array slice, then clear each view individually.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-203">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-203">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-204">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-204">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetconstantbuffers"></a><span data-ttu-id="1276e-205">>id3d11devicecoNtext：： CSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="1276e-205">ID3D11DeviceContext::CSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-206">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-206">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-207">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-207">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-208">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-208">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-209">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-209">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-210">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-210">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-211">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-211">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetsamplers"></a><span data-ttu-id="1276e-212">>id3d11devicecoNtext：： CSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="1276e-212">ID3D11DeviceContext::CSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-213">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-213">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-214">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-214">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-215">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-215">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-216">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-216">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-217">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-217">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-218">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-218">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshader"></a><span data-ttu-id="1276e-219">>id3d11devicecoNtext：： CSSetShader</span><span class="sxs-lookup"><span data-stu-id="1276e-219">ID3D11DeviceContext::CSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-220">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-220">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-221">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-221">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-222">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-222">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-223">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-223">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-224">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-224">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-225">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-225">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshaderresources"></a><span data-ttu-id="1276e-226">>id3d11devicecoNtext：： CSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="1276e-226">ID3D11DeviceContext::CSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-227">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-227">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-228">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-228">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-229">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-229">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-230">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-230">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-231">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-231">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-232">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-232">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a><span data-ttu-id="1276e-233">>id3d11devicecoNtext：： CSSetUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="1276e-233">ID3D11DeviceContext::CSSetUnorderedAccessViews</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-234">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-234">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-235">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-235">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-236">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-236">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-237">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-237">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-238">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-238">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-239">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-239">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatch"></a><span data-ttu-id="1276e-240">>id3d11devicecoNtext：:D ispatch</span><span class="sxs-lookup"><span data-stu-id="1276e-240">ID3D11DeviceContext::Dispatch</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-241">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-241">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-242">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-242">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-243">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-243">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-244">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-244">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-245">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-245">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-246">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-246">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatchindirect"></a><span data-ttu-id="1276e-247">>id3d11devicecoNtext：:D ispatchIndirect</span><span class="sxs-lookup"><span data-stu-id="1276e-247">ID3D11DeviceContext::DispatchIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-248">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-248">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-249">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-249">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-250">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-250">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-251">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-251">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-252">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-252">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-253">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-253">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdraw"></a><span data-ttu-id="1276e-254">ID3D11DeviceContext::Draw</span><span class="sxs-lookup"><span data-stu-id="1276e-254">ID3D11DeviceContext::Draw</span></span>



| <span data-ttu-id="1276e-255">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-255">Feature Level</span></span>             | <span data-ttu-id="1276e-256">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-256">Behavior Differences</span></span>                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1276e-257">D3D \_ 功能 \_ 層級 \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1276e-257">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="1276e-258">基本數目不可超過65535。</span><span class="sxs-lookup"><span data-stu-id="1276e-258">Number of primitives may not exceed 65535.</span></span><br/> <span data-ttu-id="1276e-259">紋理無法重複超過128次的一個基本類型。</span><span class="sxs-lookup"><span data-stu-id="1276e-259">Textures cannot repeat over one primitive more than 128 times.</span></span><br/>    |
| <span data-ttu-id="1276e-260">D3D \_ 功能 \_ 層級 \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="1276e-260">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="1276e-261">基本數目不可超過1048575。</span><span class="sxs-lookup"><span data-stu-id="1276e-261">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="1276e-262">紋理無法重複超過2048次的一個基本類型。</span><span class="sxs-lookup"><span data-stu-id="1276e-262">Textures cannot repeat over one primitive more than 2048 times.</span></span><br/> |
| <span data-ttu-id="1276e-263">D3D \_ 功能 \_ 層級 \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1276e-263">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="1276e-264">基本數目不可超過1048575。</span><span class="sxs-lookup"><span data-stu-id="1276e-264">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="1276e-265">紋理無法重複超過8192次的一個基本類型。</span><span class="sxs-lookup"><span data-stu-id="1276e-265">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> |



 

## <a name="id3d11devicecontextdrawauto"></a><span data-ttu-id="1276e-266">ID3D11DeviceContext::DrawAuto</span><span class="sxs-lookup"><span data-stu-id="1276e-266">ID3D11DeviceContext::DrawAuto</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-267">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-267">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-268">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-268">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-269">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-269">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-270">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-270">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-271">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-271">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-272">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-272">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexed"></a><span data-ttu-id="1276e-273">ID3D11DeviceContext::DrawIndexed</span><span class="sxs-lookup"><span data-stu-id="1276e-273">ID3D11DeviceContext::DrawIndexed</span></span>



| <span data-ttu-id="1276e-274">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-274">Feature Level</span></span>             | <span data-ttu-id="1276e-275">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-275">Behavior Differences</span></span>                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1276e-276">D3D \_ 功能 \_ 層級 \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1276e-276">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="1276e-277">基本數目不可超過65535。</span><span class="sxs-lookup"><span data-stu-id="1276e-277">Number of primitives may not exceed 65535.</span></span><br/> <span data-ttu-id="1276e-278">紋理無法重複超過128次的一個基本類型。</span><span class="sxs-lookup"><span data-stu-id="1276e-278">Textures cannot repeat over one primitive more than 128 times.</span></span><br/> <span data-ttu-id="1276e-279">索引值不能超過65534。</span><span class="sxs-lookup"><span data-stu-id="1276e-279">Index values cannot exceed 65534.</span></span><br/> <span data-ttu-id="1276e-280">不支援索引點清單。</span><span class="sxs-lookup"><span data-stu-id="1276e-280">Indexed point lists not supported.</span></span><br/>      |
| <span data-ttu-id="1276e-281">D3D \_ 功能 \_ 層級 \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="1276e-281">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="1276e-282">基本數目不可超過1048575。</span><span class="sxs-lookup"><span data-stu-id="1276e-282">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="1276e-283">紋理無法重複超過2048次的一個基本類型。</span><span class="sxs-lookup"><span data-stu-id="1276e-283">Textures cannot repeat over one primitive more than 2048 times.</span></span><br/> <span data-ttu-id="1276e-284">索引值不能超過1048575。</span><span class="sxs-lookup"><span data-stu-id="1276e-284">Index values cannot exceed 1048575.</span></span><br/> <span data-ttu-id="1276e-285">不支援索引點清單。</span><span class="sxs-lookup"><span data-stu-id="1276e-285">Indexed point lists not supported.</span></span><br/> |
| <span data-ttu-id="1276e-286">D3D \_ 功能 \_ 層級 \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1276e-286">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="1276e-287">基本數目不可超過1048575。</span><span class="sxs-lookup"><span data-stu-id="1276e-287">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="1276e-288">紋理無法重複超過8192次的一個基本類型。</span><span class="sxs-lookup"><span data-stu-id="1276e-288">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> <span data-ttu-id="1276e-289">索引值不能超過1048575。</span><span class="sxs-lookup"><span data-stu-id="1276e-289">Index values cannot exceed 1048575.</span></span><br/> <span data-ttu-id="1276e-290">不支援索引點清單。</span><span class="sxs-lookup"><span data-stu-id="1276e-290">Indexed point lists not supported.</span></span><br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a><span data-ttu-id="1276e-291">ID3D11DeviceContext::DrawIndexedInstanced</span><span class="sxs-lookup"><span data-stu-id="1276e-291">ID3D11DeviceContext::DrawIndexedInstanced</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-292">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-292">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-293">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-293">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-294">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-294">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="1276e-295">不支援 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-295">Not supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-296">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-296">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-297">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-297">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="1276e-298">基本數目不可超過1048575。</span><span class="sxs-lookup"><span data-stu-id="1276e-298">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="1276e-299">紋理無法重複超過8192次的一個基本類型。</span><span class="sxs-lookup"><span data-stu-id="1276e-299">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> <span data-ttu-id="1276e-300">索引值不能超過1048575。</span><span class="sxs-lookup"><span data-stu-id="1276e-300">Index values cannot exceed 1048575.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1276e-301">當您使用系結至管線的頂點著色器呼叫 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> 方法，但未匯入任何個別實例資料時，某些 Direct3D 9 圖形硬體可能不會繪製任何資料。</span><span class="sxs-lookup"><span data-stu-id="1276e-301">When you call the <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> method with a vertex shader that is bound to the pipeline and that doesn't import any per-instance data, some Direct3D 9 graphics hardware might not draw anything.</span></span> <span data-ttu-id="1276e-302">尤其是，如果端點著色器未使用任何個別實例資料，則使用1個實例呼叫 <strong>DrawIndexedInstanced</strong> 就不等於呼叫 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="1276e-302">In particular, if the vertex shader does not use any per-instance data, calling <strong>DrawIndexedInstanced</strong> with 1 instance is not equivalent to calling <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw</strong></a>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a><span data-ttu-id="1276e-303">>id3d11devicecoNtext：:D rawIndexedInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="1276e-303">ID3D11DeviceContext::DrawIndexedInstancedIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-304">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-304">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-305">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-305">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-306">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-306">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="1276e-307">不支援任何 9. \* 或 10. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-307">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-308">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-308">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-309">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-309">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="1276e-310">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="1276e-310">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-311">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="1276e-311">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstanced"></a><span data-ttu-id="1276e-312">ID3D11DeviceContext::DrawInstanced</span><span class="sxs-lookup"><span data-stu-id="1276e-312">ID3D11DeviceContext::DrawInstanced</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-313">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-313">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-314">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-314">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-315">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-315">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-316">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-316">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-317">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-317">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-318">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-318">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstancedindirect"></a><span data-ttu-id="1276e-319">>id3d11devicecoNtext：:D rawInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="1276e-319">ID3D11DeviceContext::DrawInstancedIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-320">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-320">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-321">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-321">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-322">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-322">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="1276e-323">不支援任何 9. \* 或 10. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-323">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-324">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-324">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-325">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-325">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="1276e-326">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="1276e-326">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-327">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="1276e-327">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetconstantbuffers"></a><span data-ttu-id="1276e-328">>id3d11devicecoNtext：:D SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="1276e-328">ID3D11DeviceContext::DSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-329">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-329">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-330">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-330">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-331">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-331">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="1276e-332">不支援任何 9. \* 或 10. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-332">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-333">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-333">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-334">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-334">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="1276e-335">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="1276e-335">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-336">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="1276e-336">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetsamplers"></a><span data-ttu-id="1276e-337">>id3d11devicecoNtext：:D SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="1276e-337">ID3D11DeviceContext::DSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-338">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-338">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-339">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-339">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-340">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-340">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="1276e-341">不支援任何 9. \* 或 10. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-341">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-342">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-342">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-343">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-343">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="1276e-344">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="1276e-344">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-345">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="1276e-345">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshader"></a><span data-ttu-id="1276e-346">>id3d11devicecoNtext：:D SSetShader</span><span class="sxs-lookup"><span data-stu-id="1276e-346">ID3D11DeviceContext::DSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-347">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-347">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-348">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-348">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-349">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-349">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="1276e-350">不支援任何 9. \* 或 10. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-350">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-351">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-351">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-352">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-352">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="1276e-353">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="1276e-353">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-354">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="1276e-354">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshaderresources"></a><span data-ttu-id="1276e-355">>id3d11devicecoNtext：:D SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="1276e-355">ID3D11DeviceContext::DSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-356">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-356">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-357">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-357">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-358">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-358">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="1276e-359">不支援任何 9. \* 或 10. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-359">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-360">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-360">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-361">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-361">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="1276e-362">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="1276e-362">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-363">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="1276e-363">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetconstantbuffers"></a><span data-ttu-id="1276e-364">>id3d11devicecoNtext：： GSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="1276e-364">ID3D11DeviceContext::GSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-365">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-365">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-366">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-366">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-367">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-367">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-368">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-368">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-369">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-369">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-370">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-370">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetsamplers"></a><span data-ttu-id="1276e-371">>id3d11devicecoNtext：： GSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="1276e-371">ID3D11DeviceContext::GSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-372">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-372">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-373">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-373">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-374">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-374">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-375">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-375">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-376">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-376">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-377">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-377">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshader"></a><span data-ttu-id="1276e-378">>id3d11devicecoNtext：： GSSetShader</span><span class="sxs-lookup"><span data-stu-id="1276e-378">ID3D11DeviceContext::GSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-379">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-379">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-380">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-380">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-381">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-381">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-382">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-382">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-383">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-383">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-384">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-384">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshaderresources"></a><span data-ttu-id="1276e-385">>id3d11devicecoNtext：： GSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="1276e-385">ID3D11DeviceContext::GSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-386">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-386">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-387">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-387">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-388">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-388">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-389">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-389">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-390">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-390">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-391">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-391">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetconstantbuffers"></a><span data-ttu-id="1276e-392">>id3d11devicecoNtext：： HSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="1276e-392">ID3D11DeviceContext::HSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-393">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-393">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-394">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-394">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-395">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-395">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="1276e-396">不支援任何 9. \* 或 10. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-396">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-397">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-397">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-398">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-398">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="1276e-399">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="1276e-399">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-400">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="1276e-400">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetsamplers"></a><span data-ttu-id="1276e-401">>id3d11devicecoNtext：： HSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="1276e-401">ID3D11DeviceContext::HSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-402">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-402">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-403">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-403">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-404">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-404">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="1276e-405">不支援任何 9. \* 或 10. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-405">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-406">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-406">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-407">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-407">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="1276e-408">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="1276e-408">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-409">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="1276e-409">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshader"></a><span data-ttu-id="1276e-410">>id3d11devicecoNtext：： HSSetShader</span><span class="sxs-lookup"><span data-stu-id="1276e-410">ID3D11DeviceContext::HSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-411">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-411">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-412">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-412">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-413">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-413">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="1276e-414">不支援任何 9. \* 或 10. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-414">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-415">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-415">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-416">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-416">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="1276e-417">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="1276e-417">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-418">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="1276e-418">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshaderresources"></a><span data-ttu-id="1276e-419">>id3d11devicecoNtext：： HSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="1276e-419">ID3D11DeviceContext::HSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-420">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-420">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-421">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-421">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-422">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-422">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="1276e-423">不支援任何 9. \* 或 10. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-423">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-424">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-424">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-425">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-425">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="1276e-426">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="1276e-426">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-427">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="1276e-427">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetindexbuffer"></a><span data-ttu-id="1276e-428">ID3D11DeviceContext::IASetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="1276e-428">ID3D11DeviceContext::IASetIndexBuffer</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-429">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-429">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-430">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-430">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-431">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-431">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="1276e-432">允許的格式與建立緩衝區時所指定的格式不同，但會產生昂貴的轉譯。</span><span class="sxs-lookup"><span data-stu-id="1276e-432">Format is allowed to be different from that specified at buffer creation, but an expensive translation will be incurred.</span></span><br/> <span data-ttu-id="1276e-433">只允許具有 DXGI_FORMAT_R16_UINT 格式的索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1276e-433">Only allows index buffers with the DXGI_FORMAT_R16_UINT format.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-434">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-434">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="1276e-435">允許的格式與建立緩衝區時所指定的格式不同，但會產生昂貴的轉譯。</span><span class="sxs-lookup"><span data-stu-id="1276e-435">Format is allowed to be different from that specified at buffer creation, but an expensive translation will be incurred.</span></span><br/> <span data-ttu-id="1276e-436">允許具有 DXGI_FORMAT_R16_UINT 的索引緩衝區，以及 D3D_FEATURE_LEVEL_10_0 和更高版本的 DXGI_FORMAT_R32_UINT 格式。</span><span class="sxs-lookup"><span data-stu-id="1276e-436">Allows index buffers with the DXGI_FORMAT_R16_UINT and DXGI_FORMAT_R32_UINT formats like D3D_FEATURE_LEVEL_10_0 and higher.</span></span> <br/> <span data-ttu-id="1276e-437">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-437">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-438">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-438">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetprimitivetopology"></a><span data-ttu-id="1276e-439">ID3D11DeviceContext::IASetPrimitiveTopology</span><span class="sxs-lookup"><span data-stu-id="1276e-439">ID3D11DeviceContext::IASetPrimitiveTopology</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-440">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-440">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-441">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-441">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-442">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-442">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-443">不支援具有連續的基本拓撲 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-443">Primitive topologies with adjacency are not supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-444">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-444">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-445">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-445">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetblendstate"></a><span data-ttu-id="1276e-446">>id3d11devicecoNtext：： OMSetBlendState</span><span class="sxs-lookup"><span data-stu-id="1276e-446">ID3D11DeviceContext::OMSetBlendState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-447">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-447">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-448">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-448">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-449">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-449">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-450">SampleMask 不可為零 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-450">SampleMask cannot be zero${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-451">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-451">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-452">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-452">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargets"></a><span data-ttu-id="1276e-453">>id3d11devicecoNtext：： OMSetRenderTargets</span><span class="sxs-lookup"><span data-stu-id="1276e-453">ID3D11DeviceContext::OMSetRenderTargets</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-454">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-454">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-455">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-455">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-456">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-456">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="1276e-457">只有一個轉譯目標支援 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-457">Only one render target supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-458">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-458">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-459">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-459">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="1276e-460">僅支援四個轉譯目標，而且所有系結的資源都必須具有相同的位深度。</span><span class="sxs-lookup"><span data-stu-id="1276e-460">Only four render targets supported, and all bound resources must have same bit depth.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a><span data-ttu-id="1276e-461">>id3d11devicecoNtext：： OMSetRenderTargetsAndUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="1276e-461">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-462">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-462">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-463">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-463">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-464">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-464">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-465">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-465">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-466">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-466">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-467">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-467">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetconstantbuffers"></a><span data-ttu-id="1276e-468">>id3d11devicecoNtext：:P SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="1276e-468">ID3D11DeviceContext::PSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-469">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-469">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-470">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-470">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-471">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-471">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-472">請參閱功能等級10.0，但著色器所使用的常數總數不能超過 32 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-472">See feature level 10.0, but total number of constants used by shader cannot exceed 32${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-473">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-473">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-474">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-474">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetsamplers"></a><span data-ttu-id="1276e-475">>id3d11devicecoNtext：:P SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="1276e-475">ID3D11DeviceContext::PSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-476">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-476">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-477">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-477">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-478">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-478">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-479">不能有超過16個取樣器可以系結 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-479">No more than 16 samplers can be bound${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-480">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-480">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-481">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-481">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshader"></a><span data-ttu-id="1276e-482">>id3d11devicecoNtext：:P SSetShader</span><span class="sxs-lookup"><span data-stu-id="1276e-482">ID3D11DeviceContext::PSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-483">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-483">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-484">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-484">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-485">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-485">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="1276e-486">僅 ps_4_0_level_9_1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-486">Only ps_4_0_level_9_1${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-487">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-487">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-488">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-488">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="1276e-489">僅 ps_4_0_level_9_3 或 ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-489">Only ps_4_0_level_9_3 or ps_4_0_level_9_1</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshaderresources"></a><span data-ttu-id="1276e-490">>id3d11devicecoNtext：:P SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="1276e-490">ID3D11DeviceContext::PSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-491">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-491">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-492">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-492">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-493">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-493">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-494">不超過8個同時系結的著色器資源 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-494">No more than 8 simultaneously bound shader resources${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-495">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-495">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-496">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-496">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetscissorrects"></a><span data-ttu-id="1276e-497">>id3d11devicecoNtext：： RSSetScissorRects</span><span class="sxs-lookup"><span data-stu-id="1276e-497">ID3D11DeviceContext::RSSetScissorRects</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-498">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-498">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-499">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-499">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-500">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-500">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-501">只有第零個剪式矩形可供使用 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-501">Only the zeroth scissor rect is available${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-502">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-502">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-503">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-503">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetviewports"></a><span data-ttu-id="1276e-504">>id3d11devicecoNtext：： RSSetViewports</span><span class="sxs-lookup"><span data-stu-id="1276e-504">ID3D11DeviceContext::RSSetViewports</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-505">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-505">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-506">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-506">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-507">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-507">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-508">只有第零個區可供使用 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-508">Only the zeroth viewport is available${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-509">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-509">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-510">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-510">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="1276e-511">即使您在 [功能層級](overviews-direct3d-11-devices-downlevel-intro.md)9 x 的 [**>id3d11devicecoNtext：： RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports)呼叫中將 Float 值指定給 *pViewports* 陣列的 [**D3D11 \_ 區**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport)結構成員，RSSetViewports 還是會在 \_ 內部使用 dword。 </span><span class="sxs-lookup"><span data-stu-id="1276e-511">Even though you specify float values to the members of the [**D3D11\_VIEWPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) structure for the *pViewports* array in a call to [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) for [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 9\_x, **RSSetViewports** uses DWORDs internally.</span></span> <span data-ttu-id="1276e-512">由於這種行為，當您使用區的負左上角時，功能層級 9 x 的 **RSSetViewports** 呼叫 \_ 會失敗。</span><span class="sxs-lookup"><span data-stu-id="1276e-512">Because of this behavior, when you use a negative top left corner for the viewport, the call to **RSSetViewports** for feature levels 9\_x fails.</span></span> <span data-ttu-id="1276e-513">發生這種失敗的原因是， **RSSetViewports** 9 \_ x 將浮點值轉換成不帶正負號的整數而不經過驗證，這會導致整數溢位。</span><span class="sxs-lookup"><span data-stu-id="1276e-513">This failure occurs because **RSSetViewports** for 9\_x casts the floating point values into unsigned integers without validation, which results in integer overflow.</span></span>

<span data-ttu-id="1276e-514">針對 [功能層級](overviews-direct3d-11-devices-downlevel-intro.md)10 x 和 11 x 的 [**>id3d11devicecoNtext：： RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports)呼叫 \_ \_ 會如您所預期般運作，即使您使用的是區的負左上角。</span><span class="sxs-lookup"><span data-stu-id="1276e-514">The call to [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) for [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 10\_x and 11\_x works as you expect even when you use a negative top left corner for the viewport.</span></span>

## <a name="id3d11devicecontextsetpredication"></a><span data-ttu-id="1276e-515">>id3d11devicecoNtext：： SetPredication</span><span class="sxs-lookup"><span data-stu-id="1276e-515">ID3D11DeviceContext::SetPredication</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-516">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-516">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-517">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-517">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-518">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-518">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-519">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-519">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-520">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-520">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-521">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-521">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextsosettargets"></a><span data-ttu-id="1276e-522">>id3d11devicecoNtext：： SOSetTargets</span><span class="sxs-lookup"><span data-stu-id="1276e-522">ID3D11DeviceContext::SOSetTargets</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-523">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-523">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-524">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-524">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-525">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-525">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-526">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-526">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-527">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-527">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-528">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-528">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetconstantbuffers"></a><span data-ttu-id="1276e-529">>id3d11devicecoNtext：： VSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="1276e-529">ID3D11DeviceContext::VSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-530">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-530">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-531">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-531">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-532">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-532">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-533">請參閱功能等級10.0，但著色器所使用的常數總數不能超過 255 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-533">See feature level 10.0, but total number of constants used by shader cannot exceed 255${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-534">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-534">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-535">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-535">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetsamplers"></a><span data-ttu-id="1276e-536">>id3d11devicecoNtext：： VSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="1276e-536">ID3D11DeviceContext::VSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-537">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-537">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-538">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-538">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-539">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-539">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-540">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-540">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-541">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-541">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-542">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-542">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshader"></a><span data-ttu-id="1276e-543">>id3d11devicecoNtext：： VSSetShader</span><span class="sxs-lookup"><span data-stu-id="1276e-543">ID3D11DeviceContext::VSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-544">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-544">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-545">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-545">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-546">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-546">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="1276e-547">僅 vs_4_0_level_9_1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-547">Only vs_4_0_level_9_1${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-548">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-548">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-549">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-549">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="1276e-550">僅 vs_4_0_level_9_3 或 vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-550">Only vs_4_0_level_9_3 or vs_4_0_level_9_1</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshaderresources"></a><span data-ttu-id="1276e-551">>id3d11devicecoNtext：： VSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="1276e-551">ID3D11DeviceContext::VSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1276e-552">功能層級</span><span class="sxs-lookup"><span data-stu-id="1276e-552">Feature Level</span></span></th>
<th><span data-ttu-id="1276e-553">行為差異</span><span class="sxs-lookup"><span data-stu-id="1276e-553">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1276e-554">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1276e-554">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1276e-555">不支援任何 9. \* 功能等級。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1276e-555">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1276e-556">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1276e-556">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1276e-557">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1276e-557">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="1276e-558">相關主題</span><span class="sxs-lookup"><span data-stu-id="1276e-558">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1276e-559">10Level9 參考</span><span class="sxs-lookup"><span data-stu-id="1276e-559">10Level9 Reference</span></span>](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





