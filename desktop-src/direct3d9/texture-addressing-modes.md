---
description: Direct3D 應用程式可為任何原始物件的任何頂點指派紋理座標。
ms.assetid: 2e23bcb3-9eba-49d9-93ce-0a4fbb15f746
title: " (Direct3D 9) 的材質定址模式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ebad5fdb141c41c43c651a2188640d7a6b764e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973556"
---
# <a name="texture-addressing-modes-direct3d-9"></a> (Direct3D 9) 的材質定址模式

Direct3D 應用程式可為任何原始物件的任何頂點指派紋理座標。 如需詳細資訊，請參閱 [ (Direct3D 9) 的材質座標 ](texture-coordinates.md)。 通常您指派給頂點的 u 及 v 紋理座標，都會位於 0.0 到 1.0 (含) 之間。 不過，藉由指派在該範圍之外的紋理座標，您可以建立特殊的紋理效果。

您可以藉 \[ \] 由設定材質定址模式，來控制 Direct3D 針對0.0、1.0 範圍之外的材質座標所執行的工作。 例如：您可以為您的應用程式設定紋理定址模式，讓紋理並排在原始物件之上。

Direct3D 允許應用程式執行紋理包裹。 請務必注意，將材質定址模式設定為 D3DTADDRESS WRAP 與 \_ 執行材質換行並不相同。 將材質定址模式設定為 D3DTADDRESS \_ ，會將來源材質的多個複本套用至目前的基本型別，並啟用紋理換行，以變更系統將紋理多邊形化的方式。 如需詳細資訊，請參閱 [ (Direct3D 9) 的材質包裝 ](texture-wrapping.md)。

啟用紋理包裝可以有效地讓材質座標超出 \[ 0.0、1.0 \] 範圍無效，而在此情況下，將這類滯納材質座標的行為未定義。 當啟用紋理包裹時，將不會使用紋理定址模式。 請注意：當您啟用紋理包裹時，應用程式將不會指定低於 0.0 或高於 1.0 的紋理座標。

## <a name="setting-the-addressing-mode"></a>設定定址模式

您可以藉由呼叫 [**IDirect3DDevice9：： SetSamplerState**](/windows/desktop/api) 方法，來設定個別材質階段的材質定址模式。 在 *取樣* 器參數中指定所需的材質階段識別碼。 將 *Type* 參數設定為 D3DSAMP \_ ADDRESSU、D3DSAMP \_ ADDRESSV 或 D3DSAMP \_ ADDRESSW 值，以個別更新 u、v 或 w 定址模式。 *Value* 參數會決定要設定的模式。 這可以是 [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 列舉型別的任何成員。 若要取得材質階段目前的材質位址模式，請使用[](/windows/desktop/api) \_ D3DSAMP 列舉的 D3DSAMP ADDRESSU、ADDRESSV \_ D3DSAMP 或 ADDRESSW D3DSAMPLERSTATETYPE 成員來呼叫 IDirect3DDevice9：： GetSamplerState， \_ 以找出您想要的資訊的位址模式。 [](./d3dsamplerstatetype.md)

## <a name="device-limitations"></a>裝置限制

雖然系統一般會允許位在 0.0 和 1.0 (含) 範圍之外的紋理座標，硬體限制通常會影響到在該範圍之外紋理座標的最遠距離。 當您取得裝置功能時，轉譯裝置會在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)結構的 **MaxTextureRepeat** 成員中傳達這項限制。 此成員中的值描述裝置允許的材質座標完整範圍。 例如：若該值為 128，輸入的紋理座標就必須維持在 -128.0 到 128.0 的範圍之中。 傳送此範圍之外的頂點紋理座標無效。 該項限制同樣適用於自動紋理座標生成產生出的紋理座標，以及紋理座標轉換。

**MaxTextureRepeat** 的解讀也會受到 D3DPTEXTURECAPS \_ TEXREPEATNOTSCALEDBYSIZE 功能位的影響。 如果設定此位，則會精確地使用 **MaxTextureRepeat** 成員的值，如所述。 不過，當 \_ 未設定 D3DPTEXTURECAPS TEXREPEATNOTSCALEDBYSIZE 時，材質重複限制會視材質座標所編制的材質大小而定。 在此情況下， **MaxTextureRepeat** 必須以最大詳細資料層級的目前紋理大小進行縮放，以計算有效的材質座標範圍。 例如，假設紋理維度32和 **MaxTextureRepeat** 為512，則實際有效的材質座標範圍為 512/32 = 16，因此此裝置的材質座標必須在-16.0 到 + 16.0 的範圍內。

下列主題包含紋理定址模式的其他相關資訊。

-   [將材質位址模式換行 (Direct3D 9) ](wrap-texture-address-mode.md)
-   [ (Direct3D 9) 的鏡像材質位址模式 ](mirror-texture-address-mode.md)
-   [ (Direct3D 9) 的夾具材質位址模式 ](clamp-texture-address-mode.md)
-   [ (Direct3D 9) 的框線色彩材質位址模式 ](border-color-texture-address-mode.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本紋理概念](basic-texturing-concepts.md)
</dt> </dl>

 

 
