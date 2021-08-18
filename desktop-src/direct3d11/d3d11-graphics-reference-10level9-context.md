---
title: 10Level9 >id3d11devicecoNtext 方法
description: 本節將列出每個10Level9 功能等級和 D3D \_ 功能 \_ 等級 \_ 11 \_ 0 和更高的 >id3d11devicecoNtext 方法功能層級之間的差異。
ms.assetid: 84478b56-0306-491a-9545-0849b06d8342
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d5cb055e6a290a9500f65ad2d64cdd69b0eaa224e6a81359595688ba1aca657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990068"
---
# <a name="10level9-id3d11devicecontext-methods"></a>10Level9 >id3d11devicecoNtext 方法

本節將列出每個10Level9 功能等級和 D3D \_ 功能 \_ 等級 \_ 11 \_ 0 和更高的 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 方法功能層級之間的差異。

-   [>id3d11devicecoNtext：： CopySubresourceRegion](#id3d11devicecontextcopysubresourceregion)
-   [>id3d11devicecoNtext：： CopyResource](#id3d11devicecontextcopyresource)
-   [>id3d11devicecoNtext：： CopyStructureCount](#id3d11devicecontextcopystructurecount)
-   [>id3d11devicecoNtext：： ClearUnorderedAccessViewFloat](#id3d11devicecontextclearunorderedaccessviewfloat)
-   [>id3d11devicecoNtext：： ClearUnorderedAccessViewUint](#id3d11devicecontextclearunorderedaccessviewuint)
-   [>id3d11devicecoNtext：： ClearRenderTargetView](#id3d11devicecontextclearrendertargetview)
-   [>id3d11devicecoNtext：： CSSetConstantBuffers](#id3d11devicecontextcssetconstantbuffers)
-   [>id3d11devicecoNtext：： CSSetSamplers](#id3d11devicecontextcssetsamplers)
-   [>id3d11devicecoNtext：： CSSetShader](#id3d11devicecontextcssetshader)
-   [>id3d11devicecoNtext：： CSSetShaderResources](#id3d11devicecontextcssetshaderresources)
-   [>id3d11devicecoNtext：： CSSetUnorderedAccessViews](#id3d11devicecontextcssetunorderedaccessviews)
-   [>id3d11devicecoNtext：:D ispatch](#id3d11devicecontextdispatch)
-   [>id3d11devicecoNtext：:D ispatchIndirect](#id3d11devicecontextdispatchindirect)
-   [ID3D11DeviceContext::Draw](#id3d11devicecontextdraw)
-   [ID3D11DeviceContext::DrawAuto](#id3d11devicecontextdrawauto)
-   [ID3D11DeviceContext::DrawIndexed](#id3d11devicecontextdrawindexed)
-   [ID3D11DeviceContext::DrawIndexedInstanced](#id3d11devicecontextdrawindexedinstanced)
-   [>id3d11devicecoNtext：:D rawIndexedInstancedIndirect](#id3d11devicecontextdrawindexedinstancedindirect)
-   [ID3D11DeviceContext::DrawInstanced](#id3d11devicecontextdrawinstanced)
-   [>id3d11devicecoNtext：:D rawInstancedIndirect](#id3d11devicecontextdrawinstancedindirect)
-   [>id3d11devicecoNtext：:D SSetConstantBuffers](#id3d11devicecontextdssetconstantbuffers)
-   [>id3d11devicecoNtext：:D SSetSamplers](#id3d11devicecontextdssetsamplers)
-   [>id3d11devicecoNtext：:D SSetShader](#id3d11devicecontextdssetshader)
-   [>id3d11devicecoNtext：:D SSetShaderResources](#id3d11devicecontextdssetshaderresources)
-   [>id3d11devicecoNtext：： GSSetConstantBuffers](#id3d11devicecontextgssetconstantbuffers)
-   [>id3d11devicecoNtext：： GSSetSamplers](#id3d11devicecontextgssetsamplers)
-   [>id3d11devicecoNtext：： GSSetShader](#id3d11devicecontextgssetshader)
-   [>id3d11devicecoNtext：： GSSetShaderResources](#id3d11devicecontextgssetshaderresources)
-   [>id3d11devicecoNtext：： HSSetConstantBuffers](#id3d11devicecontexthssetconstantbuffers)
-   [>id3d11devicecoNtext：： HSSetSamplers](#id3d11devicecontexthssetsamplers)
-   [>id3d11devicecoNtext：： HSSetShader](#id3d11devicecontexthssetshader)
-   [>id3d11devicecoNtext：： HSSetShaderResources](#id3d11devicecontexthssetshaderresources)
-   [ID3D11DeviceContext::IASetIndexBuffer](#id3d11devicecontextiasetindexbuffer)
-   [ID3D11DeviceContext::IASetPrimitiveTopology](#id3d11devicecontextiasetprimitivetopology)
-   [>id3d11devicecoNtext：： OMSetBlendState](#id3d11devicecontextomsetblendstate)
-   [>id3d11devicecoNtext：： OMSetRenderTargets](#id3d11devicecontextomsetrendertargets)
-   [>id3d11devicecoNtext：： OMSetRenderTargetsAndUnorderedAccessViews](#id3d11devicecontextomsetrendertargetsandunorderedaccessviews)
-   [>id3d11devicecoNtext：:P SSetConstantBuffers](#id3d11devicecontextpssetconstantbuffers)
-   [>id3d11devicecoNtext：:P SSetSamplers](#id3d11devicecontextpssetsamplers)
-   [>id3d11devicecoNtext：:P SSetShader](#id3d11devicecontextpssetshader)
-   [>id3d11devicecoNtext：:P SSetShaderResources](#id3d11devicecontextpssetshaderresources)
-   [>id3d11devicecoNtext：： RSSetScissorRects](#id3d11devicecontextrssetscissorrects)
-   [>id3d11devicecoNtext：： RSSetViewports](#id3d11devicecontextrssetviewports)
-   [>id3d11devicecoNtext：： SetPredication](#id3d11devicecontextsetpredication)
-   [>id3d11devicecoNtext：： SOSetTargets](#id3d11devicecontextsosettargets)
-   [>id3d11devicecoNtext：： VSSetConstantBuffers](#id3d11devicecontextvssetconstantbuffers)
-   [>id3d11devicecoNtext：： VSSetSamplers](#id3d11devicecontextvssetsamplers)
-   [>id3d11devicecoNtext：： VSSetShader](#id3d11devicecontextvssetshader)
-   [>id3d11devicecoNtext：： VSSetShaderResources](#id3d11devicecontextvssetshaderresources)
-   [相關主題](#related-topics)

## <a name="id3d11devicecontextcopysubresourceregion"></a>>id3d11devicecoNtext：： CopySubresourceRegion



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> 只有 Texture2D 和緩衝區可在 GPU 可存取的記憶體中複製。<br/> Texture3D 無法從 GPU 可存取的記憶體複製到可存取 CPU 的記憶體。<br/> 只有 D3D10_BIND_SHADER_RESOURCE 的任何資源都無法從 GPU 可存取的記憶體複製到可存取 CPU 的記憶體。<br/> 您無法複製 mipmapped 磁片區紋理。 <br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopyresource"></a>>id3d11devicecoNtext：： CopyResource



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> 只有 Texture2D 和緩衝區可在 GPU 可存取的記憶體中複製。<br/> Texture3D 無法從 GPU 可存取的記憶體複製到可存取 CPU 的記憶體。<br/> 只有 D3D10_BIND_SHADER_RESOURCE 的任何資源都無法從 GPU 可存取的記憶體複製到可存取 CPU 的記憶體。<br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopystructurecount"></a>>id3d11devicecoNtext：： CopyStructureCount



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a>>id3d11devicecoNtext：： ClearUnorderedAccessViewFloat



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a>>id3d11devicecoNtext：： ClearUnorderedAccessViewUint



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearrendertargetview"></a>>id3d11devicecoNtext：： ClearRenderTargetView



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">只會清除第一個陣列配量。 應用程式應該為每個臉部或陣列配量建立轉譯目標視圖，然後個別清除每個視圖。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetconstantbuffers"></a>>id3d11devicecoNtext：： CSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetsamplers"></a>>id3d11devicecoNtext：： CSSetSamplers



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshader"></a>>id3d11devicecoNtext：： CSSetShader



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshaderresources"></a>>id3d11devicecoNtext：： CSSetShaderResources



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a>>id3d11devicecoNtext：： CSSetUnorderedAccessViews



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatch"></a>>id3d11devicecoNtext：:D ispatch



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatchindirect"></a>>id3d11devicecoNtext：:D ispatchIndirect



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdraw"></a>ID3D11DeviceContext::Draw



| 功能層級             | 行為差異                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ 功能 \_ 層級 \_ 9 \_ 1 | 基本數目不可超過65535。<br/> 紋理無法重複超過128次的一個基本類型。<br/>    |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 2 | 基本數目不可超過1048575。<br/> 紋理無法重複超過2048次的一個基本類型。<br/> |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 3 | 基本數目不可超過1048575。<br/> 紋理無法重複超過8192次的一個基本類型。<br/> |



 

## <a name="id3d11devicecontextdrawauto"></a>ID3D11DeviceContext::DrawAuto



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexed"></a>ID3D11DeviceContext::DrawIndexed



| 功能層級             | 行為差異                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ 功能 \_ 層級 \_ 9 \_ 1 | 基本數目不可超過65535。<br/> 紋理無法重複超過128次的一個基本類型。<br/> 索引值不能超過65534。<br/> 不支援索引點清單。<br/>      |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 2 | 基本數目不可超過1048575。<br/> 紋理無法重複超過2048次的一個基本類型。<br/> 索引值不能超過1048575。<br/> 不支援索引點清單。<br/> |
| D3D \_ 功能 \_ 層級 \_ 9 \_ 3 | 基本數目不可超過1048575。<br/> 紋理無法重複超過8192次的一個基本類型。<br/> 索引值不能超過1048575。<br/> 不支援索引點清單。<br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a>ID3D11DeviceContext::DrawIndexedInstanced



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">不支援 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>基本數目不可超過1048575。<br/> 紋理無法重複超過8192次的一個基本類型。<br/> 索引值不能超過1048575。<br/>
<blockquote>
[!Note]<br />
當您使用系結至管線的頂點著色器呼叫 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> 方法，但未匯入任何個別實例資料時，某些 Direct3D 9 圖形硬體可能不會繪製任何資料。 尤其是，如果端點著色器未使用任何個別實例資料，則使用1個實例呼叫 <strong>DrawIndexedInstanced</strong> 就不等於呼叫 <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw</strong></a>。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a>>id3d11devicecoNtext：:D rawIndexedInstancedIndirect



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">不支援任何 9. * 或 10. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstanced"></a>ID3D11DeviceContext::DrawInstanced



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstancedindirect"></a>>id3d11devicecoNtext：:D rawInstancedIndirect



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">不支援任何 9. * 或 10. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetconstantbuffers"></a>>id3d11devicecoNtext：:D SSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">不支援任何 9. * 或 10. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetsamplers"></a>>id3d11devicecoNtext：:D SSetSamplers



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">不支援任何 9. * 或 10. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshader"></a>>id3d11devicecoNtext：:D SSetShader



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">不支援任何 9. * 或 10. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshaderresources"></a>>id3d11devicecoNtext：:D SSetShaderResources



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">不支援任何 9. * 或 10. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetconstantbuffers"></a>>id3d11devicecoNtext：： GSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetsamplers"></a>>id3d11devicecoNtext：： GSSetSamplers



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshader"></a>>id3d11devicecoNtext：： GSSetShader



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshaderresources"></a>>id3d11devicecoNtext：： GSSetShaderResources



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetconstantbuffers"></a>>id3d11devicecoNtext：： HSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">不支援任何 9. * 或 10. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetsamplers"></a>>id3d11devicecoNtext：： HSSetSamplers



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">不支援任何 9. * 或 10. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshader"></a>>id3d11devicecoNtext：： HSSetShader



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">不支援任何 9. * 或 10. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshaderresources"></a>>id3d11devicecoNtext：： HSSetShaderResources



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">不支援任何 9. * 或 10. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetindexbuffer"></a>ID3D11DeviceContext::IASetIndexBuffer



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td>允許的格式與建立緩衝區時所指定的格式不同，但會產生昂貴的轉譯。<br/> 只允許具有 DXGI_FORMAT_R16_UINT 格式的索引緩衝區。 <br/></td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>
<td rowspan="2"> 允許的格式與建立緩衝區時所指定的格式不同，但會產生昂貴的轉譯。<br/> 允許具有 DXGI_FORMAT_R16_UINT 的索引緩衝區，以及 D3D_FEATURE_LEVEL_10_0 和更高版本的 DXGI_FORMAT_R32_UINT 格式。 <br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetprimitivetopology"></a>ID3D11DeviceContext::IASetPrimitiveTopology



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援具有連續的基本拓撲 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetblendstate"></a>>id3d11devicecoNtext：： OMSetBlendState



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">SampleMask 不可為零 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargets"></a>>id3d11devicecoNtext：： OMSetRenderTargets



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">只有一個轉譯目標支援 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>僅支援四個轉譯目標，而且所有系結的資源都必須具有相同的位深度。</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a>>id3d11devicecoNtext：： OMSetRenderTargetsAndUnorderedAccessViews



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetconstantbuffers"></a>>id3d11devicecoNtext：:P SSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">請參閱功能等級10.0，但著色器所使用的常數總數不能超過 32 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetsamplers"></a>>id3d11devicecoNtext：:P SSetSamplers



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不能有超過16個取樣器可以系結 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshader"></a>>id3d11devicecoNtext：:P SSetShader



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">僅 ps_4_0_level_9_1 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>僅 ps_4_0_level_9_3 或 ps_4_0_level_9_1</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshaderresources"></a>>id3d11devicecoNtext：:P SSetShaderResources



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不超過8個同時系結的著色器資源 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetscissorrects"></a>>id3d11devicecoNtext：： RSSetScissorRects



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">只有第零個剪式矩形可供使用 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetviewports"></a>>id3d11devicecoNtext：： RSSetViewports



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">只有第零個區可供使用 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

即使您在 [功能層級](overviews-direct3d-11-devices-downlevel-intro.md)9 x 的 [**>id3d11devicecoNtext：： RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports)呼叫中將 Float 值指定給 *pViewports* 陣列的 [**D3D11 \_ 區**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport)結構成員，RSSetViewports 還是會在 \_ 內部使用 dword。  由於這種行為，當您使用區的負左上角時，功能層級 9 x 的 **RSSetViewports** 呼叫 \_ 會失敗。 發生這種失敗的原因是， **RSSetViewports** 9 \_ x 將浮點值轉換成不帶正負號的整數而不經過驗證，這會導致整數溢位。

針對 [功能層級](overviews-direct3d-11-devices-downlevel-intro.md)10 x 和 11 x 的 [**>id3d11devicecoNtext：： RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports)呼叫 \_ \_ 會如您所預期般運作，即使您使用的是區的負左上角。

## <a name="id3d11devicecontextsetpredication"></a>>id3d11devicecoNtext：： SetPredication



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextsosettargets"></a>>id3d11devicecoNtext：： SOSetTargets



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetconstantbuffers"></a>>id3d11devicecoNtext：： VSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">請參閱功能等級10.0，但著色器所使用的常數總數不能超過 255 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetsamplers"></a>>id3d11devicecoNtext：： VSSetSamplers



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshader"></a>>id3d11devicecoNtext：： VSSetShader



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">僅 vs_4_0_level_9_1 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>僅 vs_4_0_level_9_3 或 vs_4_0_level_9_1</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshaderresources"></a>>id3d11devicecoNtext：： VSSetShaderResources



<table>
<thead>
<tr class="header">
<th>功能層級</th>
<th>行為差異</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">不支援任何 9. * 功能等級。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[10Level9 參考](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





