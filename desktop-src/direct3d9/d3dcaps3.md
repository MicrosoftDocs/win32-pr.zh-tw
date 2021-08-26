---
description: 查看 D3DCAPS3 驅動程式功能旗標的清單。 包含定義、值和描述，以及 Api 的連結。
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706b2f5644b45179f9367aa26be11160e06df517
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622144"
---
# <a name="d3dcaps3"></a>D3DCAPS3

驅動程式功能旗標。



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#定義</td>
<td>值</td>
<td>描述</td>
</tr>
<tr class="even">
<td>D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</td>
<td>0x00000020L</td>
<td>指出當使用翻轉或捨棄交換效果時，裝置可以使用全螢幕模式下的 D3DRS_ALPHABLENDENABLE 呈現狀態。 只有當 D3DRS_SRCBLEND 或 D3DRS_DESTBLEND 狀態設定為下列其中一項時，才適用這種情況：
<ul>
<li>D3DBLEND_DESTALPHA</li>
<li>D3DBLEND_INVDESTALPHA</li>
<li>D3DBLEND_DESTCOLOR</li>
<li>D3DBLEND_INVDESTCOLOR</li>
</ul></td>
</tr>
<tr class="odd">
<td>D3DCAPS3_COPY_TO_VIDMEM</td>
<td>0x00000100L</td>
<td>裝置可以加速從系統記憶體複製到本機視訊記憶體的記憶體。 此上限可確保 <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> 和 <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> 呼叫將會是硬體加速。 如果不存在此上限，則這些呼叫會成功，但速度會變慢。</td>
</tr>
<tr class="even">
<td>D3DCAPS3_COPY_TO_SYSTEMMEM</td>
<td>0x00000200L</td>
<td>裝置可以加速從本機視訊記憶體到系統記憶體的記憶體複製。 此上限可保證 <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> 呼叫將會是硬體加速。 如果不存在此上限，此呼叫將會成功，但會變慢。</td>
</tr>
<tr class="odd">
<td>D3DCAPS3_DXVAHD</td>
<td>0x00000400L</td>
<td>顯示驅動程式支援 DXVA-HD DDI。 如需 DXVA-HD DDI 的詳細資訊，請參閱 <a href="https://msdn.microsoft.com/library/dd835176.aspx">處理 High-Definition 影片</a>。<br/> 
<table>
<tbody>
<tr class="odd">
<td>Direct3D 9 與 Direct3D 9Ex 之間的差異：<br/> 此旗標僅適用于 Direct3D 9Ex。<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</td>
<td>0x00000080L</td>
<td>指出裝置可以從視窗型背景緩衝區執行 gamma 修正， (包含) 至 sRGB 桌面的線性內容。</td>
</tr>
<tr class="odd">
<td>D3DCAPS3_RESERVED</td>
<td>0x8000001fL</td>
<td>保護未使用。</td>
</tr>
</tbody>
</table>



 

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 D3CAPS3 成員會使用這些常數。

## <a name="constant-information"></a>常數資訊



|  需求                        | 值           |
|--------------------------|------------|
| 標頭                   | d3d9caps。h |
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




