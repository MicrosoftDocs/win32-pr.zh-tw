---
description: 材質篩選常數。
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46adc4759290691e93ef68a8a4e212eacf5b6451
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343083"
---
# <a name="d3dptfiltercaps"></a>D3DPTFILTERCAPS

材質篩選常數。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#定義</td>
<td>Description</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_CONVOLUTIONMONO</td>
<td>裝置支援單色卷積篩選。 此篩選是以 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_CONVOLUTIONMONO 成員表示。 
<table>
<tbody>
<tr class="odd">
<td>Direct3D 9 與 Direct3D 9Ex 之間的差異：<br/> 此旗標僅適用于 Direct3D 9Ex。<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFPOINT</td>
<td>裝置支援對放大鏡進行每個階段的點範例篩選。 點範例的放大濾波器是以 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_POINT 成員表示。</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFLINEAR</td>
<td>裝置支援對放大鏡的每一階段雙線性插補篩選進行 mipmap。 雙線性插補 mipmap 濾波器是以 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_LINEAR 成員表示。</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFANISOTROPIC</td>
<td>裝置支援對放大鏡進行的每一階段的非等向篩選。 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a>列舉型別的 D3DTEXF_ANISOTROPIC 成員表示非等向放大篩選。</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</td>
<td>裝置支援放大紋理的每一階段金字塔範例篩選。 金字塔放大鏡篩選會以 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_PYRAMIDALQUAD 成員表示。</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</td>
<td>裝置支援放大紋理的每一階段高斯四次篩選。</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFPOINT</td>
<td>裝置支援縮小材質的每個階段點範例篩選。 點範例縮制篩選會以 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_POINT 成員表示。</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFLINEAR</td>
<td>裝置支援縮小材質的每一階段線性篩選。 線性縮制濾波器是以 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_LINEAR 成員表示。</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFANISOTROPIC</td>
<td>裝置支援縮小材質的每一階段非等向篩選。 縮制篩選準則是由 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_ANISOTROPIC 成員表示。</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</td>
<td>裝置支援縮小材質的每一階段金字塔範例篩選。</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFGAUSSIANQUAD</td>
<td>裝置支援縮小材質的每一階段高斯四種篩選。</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MIPFPOINT</td>
<td>裝置支援 mipmap 的每個階段點範例篩選。 點範例 mipmap 篩選會以 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_POINT 成員表示。</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MIPFLINEAR</td>
<td>裝置針對 mipmap 支援每一階段的雙線性插補篩選。 雙線性插補 mipmap 濾波器是以 <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> 列舉型別的 D3DTEXF_LINEAR 成員表示。</td>
</tr>
</tbody>
</table>



 

這些常數由 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 TextureFilterCaps、CubeTextureFilterCaps、VolumeTextureFilterCaps 和 VertexTextureFilterCaps 成員使用。

## <a name="constant-information"></a>常數資訊



|  需求                        | 值           |
|--------------------------|------------|
| 標頭                   | d3d9caps。h |
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
