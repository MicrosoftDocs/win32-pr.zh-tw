---
description: 查看 D3DCAPS2 驅動程式功能旗標的清單。 包含定義、值和描述，以及 Api 的連結。
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fc58f0e249a90a325631123ce7b8e43d4149a7244e7b2032c489c0999137ea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989118"
---
# <a name="d3dcaps2"></a>D3DCAPS2

驅動程式功能旗標。



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
<td>D3DCAPS2_CANAUTOGENMIPMAP</td>
<td>0x40000000L</td>
<td>驅動程式能夠自動產生 mipmap。 如需詳細資訊，請參閱 <a href="automatic-generation-of-mipmaps.md">自動產生 mipmap (Direct3D 9) </a>。</td>
</tr>
<tr class="odd">
<td>D3DCAPS2_CANCALIBRATEGAMMA</td>
<td>0x00100000L</td>
<td>系統已安裝校正器，可自動調整 gamma 的斜坡，使所有具有校正器的系統上的結果都相同。 若要在設定新的 gamma 層級時叫用校正器，請在呼叫 <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>時使用 D3DSGR_CALIBRATE 旗標。 校準 gamma 的斜坡會產生一些處理的額外負荷，不應經常使用。</td>
</tr>
<tr class="even">
<td>D3DCAPS2_CANSHARERESOURCE</td>
<td>0x80000000L</td>
<td>裝置可以建立可共用的資源。 建立資源的方法可以設定其 <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> 參數的非 Null 值。 
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
<td>D3DCAPS2_CANMANAGERESOURCE</td>
<td>0x10000000L</td>
<td>驅動程式能夠管理資源。 在這類驅動程式上，D3DPOOL_MANAGED 資源將由驅動程式管理。 若要讓 Direct3D 覆寫驅動程式，以便 Direct3D 管理資源，請在呼叫 <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>時使用 D3DCREATE_DISABLE_DRIVER_MANAGEMENT 旗標。</td>
</tr>
<tr class="even">
<td>D3DCAPS2_DYNAMICTEXTURES</td>
<td>0x20000000L</td>
<td>此驅動程式支援動態紋理。</td>
</tr>
<tr class="odd">
<td>D3DCAPS2_FULLSCREENGAMMA</td>
<td>0x00020000L</td>
<td>此驅動程式支援以全螢幕模式進行動態 gamma 遞增調整。</td>
</tr>
<tr class="even">
<td>D3DCAPS2_RESERVED</td>
<td>0x02000000L</td>
<td>保護未使用。</td>
</tr>
</tbody>
</table>



 

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 D3CAPS2 成員會使用這些常數。

## <a name="constant-information"></a>常數資訊



|  需求                        | 值           |
|--------------------------|------------|
| 標頭                   | d3d9caps。h |
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
