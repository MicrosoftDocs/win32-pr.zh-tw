---
description: 其他驅動程式基本功能旗標。
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ace0b9070d158769e22e02a759545b1bf7785
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343133"
---
# <a name="d3dpmisccaps"></a>D3DPMISCCAPS

其他驅動程式基本功能旗標。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#定義</td>
<td>值</td>
<td>描述</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MASKZ</td>
<td>0x00000002L</td>
<td>裝置可以啟用和停用圖元作業的深度緩衝區修改。</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLNONE</td>
<td>0x00000010L</td>
<td>驅動程式不會執行三角形剔除。 這會對應至 <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> 列舉型別的 D3DCULL_NONE 成員。</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CULLCW</td>
<td>0x00000020L</td>
<td>此驅動程式支援透過 D3DRS_CULLMODE 狀態進行順時針三角形的挑選。  (這只適用于三角形基本專案。 ) 此旗標對應至 <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> 列舉型別的 D3DCULL_CW 成員。</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLCCW</td>
<td>0x00000040L</td>
<td>此驅動程式支援透過 D3DRS_CULLMODE 狀態的逆時針剔除。  (這只適用于三角形基本專案。 ) 此旗標對應至 <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> 列舉型別的 D3DCULL_CCW 成員。</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_COLORWRITEENABLE</td>
<td>0x00000100L</td>
<td>裝置可透過 D3DRS_COLORWRITEENABLE 狀態，針對轉譯目標色彩緩衝區支援每個通道的寫入。</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</td>
<td>0x00000200L</td>
<td>裝置會正確地將大小大於1.0 的縮放點裁剪到使用者定義的裁剪平面。</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CLIPTLVERTS</td>
<td>0x00000200L</td>
<td>裝置會裁剪轉換後的頂點基本專案。 指定管線不應進行任何裁剪時的 D3DUSAGE_DONOTCLIP。 在此情況下，可能需要在繪圖時執行額外的軟體裁剪，以要求在系統記憶體中有頂點緩衝區。<br/></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_TSSARGTEMP</td>
<td>0x00000400L</td>
<td>裝置支援暫時註冊的 <a href="d3dta.md">D3DTA</a> 。</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_BLENDOP</td>
<td>0x00000800L</td>
<td>裝置除了 D3DBLENDOP_ADD 之外，也支援 Alpha 混色作業。</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_NullREFERENCE</td>
<td>0x00000100L</td>
<td>未轉譯的參考裝置。</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_INDEPENDENTWRITEMASKS</td>
<td>0x00004000L</td>
<td>裝置支援多個元素紋理或多個呈現目標的獨立寫入遮罩。</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_PERSTAGECONSTANT</td>
<td>0x00008000L</td>
<td>裝置支援每一階段的常數。 請參閱 <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>中的 D3DTSS_CONSTANT。</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_POSTBLENDSRGBCONVERT</td>
<td>0x00200000L</td>
<td>裝置支援在混合之後轉換成 sRGB。 
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
<td>D3DPMISCCAPS_FOGANDSPECULARALPHA</td>
<td>0x00010000L</td>
<td>裝置支援個別的霧化和反射 Alpha。 許多裝置都會使用反射 Alpha 通道來儲存霧化因數。</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_SEPARATEALPHABLEND</td>
<td>0x00020000L</td>
<td>裝置支援 Alpha 通道的不同 blend 設定。</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</td>
<td>0x00040000L</td>
<td>裝置針對多個呈現目標支援不同的位深度。</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</td>
<td>0x00080000L</td>
<td>裝置支援多個呈現目標的後置圖元著色器作業。</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_FOGVERTEXCLAMPED</td>
<td>0x00100000L</td>
<td>裝置個會對每個頂點的 blend 因數進行霧化。</td>
</tr>
</tbody>
</table>



 

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 PrimitiveMiscCaps 成員會使用這些常數。

## <a name="constant-information"></a>常數資訊



| 需求                         |  值          |
|--------------------------|------------|
| 標頭                   | d3d9caps。h |
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
