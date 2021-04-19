---
description: 材質內容通常會以 sRGB 格式儲存。
ms.assetid: d076140d-3e91-412a-b099-9baa52f8d7d8
title: " (Direct3D 9) 的 Gamma"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cea4b3ba224452e1c3be8f96b7136f4e4f649c8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971272"
---
# <a name="gamma-direct3d-9"></a> (Direct3D 9) 的 Gamma

材質內容通常會以 sRGB 格式儲存。 傳統上，圖元管線假設色彩為線性，因此會以線性空間執行混合作業。 不過，由於 sRGB 內容是由 gamma 修正，因此線性空間中的混合作業將會產生不正確的結果。 視訊卡現在可以修正此問題，方法是在讀取任何 sRGB 內容時復原 gamma 修正，並在寫出圖元時將圖元資料轉換回 sRGB 格式。 在此情況下，圖元管線內的所有作業都會線上性空間中執行。

## <a name="gamma-correction"></a>Gamma 修正

Direct3D 9 可以：

-   指出材質是否已更正為 gamma 2.2，或不 (sRGB 或不) 。 驅動程式會在 SetTexture 階段轉換成線性 gamma 以進行混合作業，或取樣器會在查閱時將它轉換成線性資料。
-   指出將圖元管線寫出至轉譯目標時，是否應將其 gamma 校正為 sRGB 空間。

所有其他色彩 (清除色彩、材質色彩、頂點色彩等等 ) 都會假設線上性空間中。 應用程式可以使用圖元著色器指令，以 gamma 更正寫入框架緩衝區的色彩。 Linearization 只能套用至 RGB 通道，而不應套用至 Alpha 色板。

並非所有的表面格式都可以 linearized。 只有通過 [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE \_ QUERY SRGBREAD 的格式 \_ 可以是 linearized。 \_其餘部分會忽略取樣器狀態 D3DSAMP SRGBTEXTURE。 只有未簽署的材質格式才支援這種轉換。 不帶正負號的材質格式只包含 R、G、B 和 L 元件。 如果 Alpha 色板存在，則會予以忽略。 如果混合格式支援 sRGB linearization，則只會影響不帶正負號的通道。 在理想的情況下，硬體應該在篩選之前執行 linearization，但在 Direct3D 9 中，硬體可以在篩選之後執行 linearization。

並非所有表面格式都可以在 sRGB 空間中撰寫。 只有傳遞 [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) 與使用旗標 D3DUSAGE 查詢 SRGBWRITE 的格式 \_ \_ 可以是 linearized。 \_其餘部分會忽略轉譯狀態 D3DRS SRGBWRITEENABLE。 每個通道 RGB 未簽署格式的8個位預期會公開此功能。

在理想的情況下，硬體應該線上性空間中執行框架緩衝區混合作業，但硬體可以在圖元著色器之後，但在框架緩衝區 blender 之前執行。 這表示在 sRGB 空間中進行的框架緩衝區混合作業將會產生不正確的結果。 \_執行明確轉譯目標時，會接受 D3DRS SRGBWRITEENABLE。 針對支援 [多個轉譯目標的硬體 (direct3d 9) ](multiple-render-targets.md) 或 [多元素紋理 (direct3d 9) ](multiple-element-textures.md)，則只會寫入第一個轉譯目標或元素。

### <a name="api-changes"></a>API 變更


```
// New sampler state (DWORD)
// If this is nonzero, the texture is linearized on lookup.
D3DSAMP_SRGBTEXTURE       // Default FALSE

// New render state (DWORD)
D3DRS_SRGBWRITEENABLE     // Default FALSE

// New usage flags
D3DUSAGE_QUERY_SRGBWRITE
D3DUSAGE_QUERY_SRGBREAD
```



### <a name="windowed-swap-chains"></a>視窗型交換鏈

應用程式會將其交換鏈的背景緩衝區保留線上性空間中，以啟用正確的混色作業，是很重要的。 由於桌面通常不線上性空間中，因此必須先進行 gamma 修正，然後才能呈現背景緩衝區的內容。 應用程式可以藉由配置額外的緩衝區，並從線性緩衝區執行自己的更正複製到背景緩衝區，來影響此修正本身。 這需要額外的複本，如果驅動程式在展示 array.blit 中執行 gamma 修正，則可以避免此情況。

在 Direct3D 9 中，有一個新的旗標（ [D3DPRESENT \_ 線性 \_ 內容](d3dpresent.md)） [**可供使用**](/windows/desktop/api) ，讓簡報從線性空間隱含轉換為 sRGB/gamma 2.2。 如果背景緩衝區格式為16位浮點數以符合全螢幕 gamma 行為的視窗模式，則應用程式應指定此旗標， \_ \_ \_ \_ 並針對透過 [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps)抓取的裝置功能傳回 D3DCAPS3 線性至 SRGB 簡報。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[框架緩衝區](frame-buffer.md)
</dt> </dl>

 

 
