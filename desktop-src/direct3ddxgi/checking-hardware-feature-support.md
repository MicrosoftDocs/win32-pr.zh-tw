---
description: 本節涵蓋如何使用 API 呼叫來檢查 Direct3D 功能等級硬體的格式支援。
ms.assetid: 0C40C73E-06F3-41FA-AA27-2C0B730B357B
title: 檢查硬體功能支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ee68a97b30c9828e2a5d27aadb58d668b74858
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624064"
---
# <a name="checking-hardware-feature-support"></a>檢查硬體功能支援

本節涵蓋如何使用 API 呼叫來檢查 Direct3D 功能等級硬體的格式支援。

若為 D3D11，請使用 [**ID3D11Device：： CheckFormatSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkformatsupport) ，以程式設計方式驗證先前章節中的資訊。 若為 D3D12，請使用 [**ID3D12：： CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)。



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>格式化目標</th>
<th>D3D12</th>
<th>D3D11</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Buffer</td>
<td>D3D12_FORMAT_SUPPORT1_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="even">
<td>輸入組合語言頂點緩衝區</td>
<td>D3D12_FORMAT_SUPPORT1_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="odd">
<td>輸入組合語言索引緩衝區</td>
<td>D3D12_FORMAT_SUPPORT1_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="even">
<td>資料流程輸出緩衝區</td>
<td>D3D12_FORMAT_SUPPORT1_SO_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_SO_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="odd">
<td>Texture1D</td>
<td>D3D12_FORMAT_SUPPORT1_TEXTURE1D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_TEXTURE1D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="even">
<td>Texture2D</td>
<td>D3D12_FORMAT_SUPPORT1_TEXTURE2D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_TEXTURE2D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="odd">
<td>Texture3D</td>
<td>D3D12_FORMAT_SUPPORT1_TEXTURE3D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_TEXTURE3D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="even">
<td>TextureCube</td>
<td>D3D12_FORMAT_SUPPORT1_TEXTURECUBE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_TEXTURECUBE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="odd">
<td>著色器 ld</td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_SHADER_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="even">
<td>著色器範例 (任何篩選) </td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="odd">
<td>著色器 sample_c (比較篩選) </td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="even">
<td>著色器範例 (mono 1_bit_filter) </td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="odd">
<td>著色器 gather4</td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_GATHER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_SHADER_GATHER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="even">
<td>著色器 gather4_c</td>
<td>D3D12_FORMAT_SUPPORT1_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="odd">
<td>Mipmap</td>
<td>D3D12_FORMAT_SUPPORT1_MIP (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_MIP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="even">
<td>Mipmap 自動產生</td>
<td><blockquote>
[!Note]<br />
D3D12 不再具有專用的 mipmap 產生功能。 應用程式必須使用著色器自行執行。
</blockquote>
<br/></td>
<td>D3D11_FORMAT_SUPPORT_MIP_AUTOGEN (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="odd">
<td>RenderTarget</td>
<td>D3D12_FORMAT_SUPPORT1_RENDER_TARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_RENDER_TARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="even">
<td>Blendable RenderTarget</td>
<td>D3D12_FORMAT_SUPPORT1_BLENDABLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_BLENDABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="odd">
<td>輸出合併邏輯 Op</td>
<td>D3D12_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP</td>
<td>D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </td>
</tr>
<tr class="even">
<td>深度/樣板目標</td>
<td>D3D12_FORMAT_SUPPORT1_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="odd">
<td>原始 UAV 和 SRV</td>


</tr>
<tr class="even">
<td>結構化 UAV 和 SRV</td>


</tr>
<tr class="odd">
<td>具類型的 UAV</td>
<td>D3D12_FORMAT_SUPPORT1_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="even">
<td>UAV 具類型的存放區</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </td>
</tr>
<tr class="odd">
<td>UAV 具類型的載入</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </td>
</tr>
<tr class="even">
<td>UAV 不可部分完成的新增</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </td>
</tr>
<tr class="odd">
<td>UAV 不可部分完成的位運算</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </td>
</tr>
<tr class="even">
<td>UAV 不可部分完成的 Cmp&Store/Cmp&Ms-exch-assistant-name</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </td>
</tr>
<tr class="odd">
<td>UAV 不可部分完成 Exchange</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </td>
</tr>
<tr class="even">
<td>UAV 不可部分完成的帶正負號 Min/Max</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </td>
</tr>
<tr class="odd">
<td>UAV 不可部分完成的無符號下限/最大值</td>
<td>D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </td>
</tr>
<tr class="even">
<td>CPU 鎖定</td>
<td><blockquote>
[!Note]<br />
只有單一格式會防止 cpu 存取 (420_OPAQUE) 。
</blockquote>
<br/></td>
<td>D3D11_FORMAT_SUPPORT_CPU_LOCKABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="odd">
<td>4x 多重採樣 RenderTarget</td>
<td>D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="even">
<td>8x 多重採樣 RenderTarget</td>
<td>D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="odd">
<td>其他的多重採樣計數 RT</td>
<td>D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="even">
<td>多級取樣解析</td>
<td>D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="odd">
<td>多級載入</td>
<td>D3D12_FORMAT_SUPPORT1_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="even">
<td>顯示 Scan-Out</td>
<td>D3D12_FORMAT_SUPPORT1_DISPLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_DISPLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="odd">
<td>位配置中的 Cast</td>
<td>D3D12_FORMAT_SUPPORT1_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="even">
<td>影片解碼支援</td>
<td>D3D12_FORMAT_SUPPORT1_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="odd">
<td>視頻處理器輸入</td>
<td>D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="even">
<td>視頻處理器輸出</td>
<td>D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="odd">
<td>共用資源</td>
<td><blockquote>
[!Note]<br />
所有格式的材質都可以是共用的已認可資源，也可以放在共用堆積中。
</blockquote>
<br/></td>
<td>D3D11_FORMAT_SUPPORT2_SHAREABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </td>
</tr>
<tr class="even">
<td>背景緩衝區可轉換甚至是完整類型</td>
<td>D3D12_FORMAT_SUPPORT1_BACK_BUFFER_CAST (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td><blockquote>
[!Note]<br />
沒有任何可用的 API。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>磚資源</td>
<td>D3D12_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </td>
</tr>
<tr class="even">
<td>影片編碼器</td>
<td>D3D12_FORMAT_SUPPORT1_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>) </td>
</tr>
<tr class="odd">
<td>Multiplane 重迭</td>
<td>D3D12_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>) </td>
<td>D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>) </td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[D3D12 硬體功能等級](/windows/desktop/direct3d12/hardware-feature-levels)
</dt> <dt>

[**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> <dt>

[**D3D11 \_ 格式 \_ 支援**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support)
</dt> <dt>

[**D3D11 \_ 格式 \_ SUPPORT2**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2)
</dt> <dt>

[DXGI 的程式設計指南](dx-graphics-dxgi-overviews.md)
</dt> </dl>

