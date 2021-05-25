---
description: D3DPRESENT 參數所使用的常數 \_ 。
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 578d41119980719e69b9eb0e502c025414018f73
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343093"
---
# <a name="d3dpresentflag"></a>D3DPRESENTFLAG

[**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)所使用的常數。



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
<td>D3DPRESENTFLAG_DEVICECLIP</td>
<td>0x00000004</td>
<td>在建立 Direct3D 裝置的視訊卡的 [監視器] 畫面區域內，將視窗內的 <a href="/windows/desktop/api"><strong>現有</strong></a> array.blit 裁剪到視窗工作區中。 D3DPRESENTFLAG_DEVICECLIP 對 D3DSWAPEFFECT_FLIPEX 無效。</td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</td>
<td>0x00000002</td>
<td>建立裝置或交換鏈時，請設定此旗標，以啟用 z 緩衝區捨棄。 如果設定此旗標，深度樣板緩衝區的內容在呼叫 <a href="/windows/desktop/api"><strong>其中一個或</strong></a>具有不同深度介面的 <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> 之後將會無效。 捨棄 z 緩衝區資料可能會提高效能，並且與驅動程式相依。 偵錯工具執行時間將會在 <a href="/windows/desktop/api"><strong>呼叫任一值</strong></a>之後，將 z 緩衝區清除為某個常數值，或使用不同的深度介面 <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> 來強制捨棄。<br/> 捨棄 z 緩衝區資料對於所有可鎖定格式（D3DFMT_D16_LOCKABLE 和 D3DFMT_D32F_LOCKABLE 而言不合法。 任何使用指定可鎖定格式和 z 緩衝區捨棄的 <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> 將會失敗。 如需有關格式的詳細資訊，請參閱 <a href="d3dformat.md">D3DFORMAT</a>。<br/></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</td>
<td>0x00000001</td>
<td>如果應用程式需要能夠直接鎖定背景緩衝區，請設定此旗標。 請注意，除非應用程式在呼叫 <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> 或 <a href="/windows/desktop/api"><strong>重設</strong></a>時指定 D3DPRESENTFLAG_LOCKABLE_BACKBUFFER，否則無法鎖定背景緩衝區。 在某些圖形硬體設定上，「鎖定回緩衝區」會產生效能成本。  (或使用 <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> 在可鎖定的緩衝區上執行鎖定作業來寫入) ，會降低許多卡片的效能。 在此情況下，請考慮使用紋理三角形將資料移至背景緩衝區。<br/> 
<table>
<tbody>
<tr class="odd">
<td>Direct3D 9 與 Direct3D 9Ex 之間的差異：<br/> 在 Direct3D9Ex 中，如果 D3DSWAPEFFECT 是 D3DSWAPEFFECT_FLIPEX，就無法設定這個旗標，因為 flip 模型可讓桌面視窗管理員存取應用程式的背景緩衝區。 跨進程的共用介面不應鎖定。<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_NOAUTOROTATE</td>
<td>0x00000020</td>
<td>旋轉的監視器會在簡報期間以旋轉複製自動處理，這並不是非常有效率。 此旗標表示應用程式會執行它自己的顯示旋轉。 
<table>
<tbody>
<tr class="odd">
<td>Direct3D 9 與 Direct3D 9Ex 之間的差異：<br/> 此旗標僅適用于 Direct3D 9Ex。<br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p>應用程式可以使用旋轉的視圖矩陣來達成自己的旋轉。 應使用 <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> 和 <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> 方法來尋找目前的旋轉設定。 <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a>和<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a>中的背景緩衝區寬度和高度參數必須使用橫向方向，而全螢幕顯示模式結構應該與 (<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a>傳回的相同，也就是在旋轉90和270度) 時，會交換寬度和高度。</p>
<p>當您在旋轉轉譯目標上使用鎖定時，左上角的假設不會再保留 true，因此，轉譯目標 SURFACE_DESC 將維持在建立參數) （以及 GDI 視窗、滑鼠座標）所隱含的橫向 (，而且在搭配 Direct3D 轉譯目標和場景使用時必須適當地轉譯。</p></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_UNPRUNEDMODE</td>
<td>0x00000040</td>
<td>您可以使用此旗標來指定顯示介面卡所列舉的任何原始顯示模式，即使 Direct3D 可能指出模式無效也一樣。 應用程式應該以健全的方式來執行這項工作，以防需要的模式確實無效。 
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
<td>D3DPRESENTFLAG_VIDEO</td>
<td>0x00000010</td>
<td>這是驅動程式的提示，其中的後端緩衝區將包含影片資料。</td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</td>
<td>0x00000080</td>
<td>指定覆迭是完整範圍的 RGB 或有限的範圍 RGB。 設定此旗標會指出有限的範圍 RGB。 在有限範圍的 RGB 中，RGB 範圍會壓縮，因此16:16:16 為黑色，而235:235:235 是白色。
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
<td>D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</td>
<td>0x00000100</td>
<td>指定重迭是否為 BT. 601 或 BT. 709。 設定此旗標表示709，適用于高定義電視 (HDTV) 。
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
<td>D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</td>
<td>0x00000200</td>
<td>指定覆迭是否為傳統 YCbCr 或擴充的 YCbCr (xvYCC) 。 設定此旗標表示擴充的 YCbCr (xvYCC) 。
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
<td>D3DPRESENTFLAG_RESTRICTED_CONTENT</td>
<td>0x00000400</td>
<td>設定此旗標表示 swapchain 包含受保護的內容，並自動使執行時間限制對 swapchain 的存取，如此一來，只有桌面 Windows 管理員 (DWM) 可以使用 swapchain。
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
<td>D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</td>
<td>0x00000800</td>
<td>設定此旗標表示驅動程式應該限制對針對 DWM 互動所建立之任何共用資源的存取權。 呼叫端必須使用驅動程式來建立已驗證的通道。 然後，驅動程式應該允許存取嘗試開啟這些共用資源的進程。
<table>
<tbody>
<tr class="odd">
<td>Direct3D 9 與 Direct3D 9Ex 之間的差異：<br/> 此旗標僅適用于 Direct3D 9Ex。<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

這些常數會由 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)使用。

## <a name="constant-information"></a>常數資訊



| 需求                         | 值            |
|--------------------------|-------------|
| 標頭                   | d3d9types。h |
| 最低作業系統 | Windows 98  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




