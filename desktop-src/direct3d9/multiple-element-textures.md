---
description: 傳統紋理會視為單一元素紋理。
ms.assetid: 8fe8da80-0879-413a-a7db-617d2f558b28
title: " (Direct3D 9) 的多元素紋理"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a69c04c54f4be73b71a1ac5f2ead123bb51d649ad5e75369411b6bf0906517c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563538"
---
# <a name="multiple-element-textures-direct3d-9"></a> (Direct3D 9) 的多元素紋理

傳統紋理會視為單一元素紋理。 多元素紋理可讓應用程式從圖元著色器同時寫入材質的多個元素。 下一次轉譯階段的結果是，應用程式可以使用一或多個元素做為單一元素材質，也就是圖元著色器的輸入。 您可以將這些額外的元素視為中繼結果的暫存存放區，以供應用程式稍後傳遞。

第一代公開這項功能的硬體具有下列限制：

-   所有多元素紋理介面都會自動設定。 這項限制的解決方式是將它視為新的介面格式類型，並交錯多個 RGBA 通道。
-   多元素材質的所有元素都可以有相同的位深度。 這項限制會以新表面格式的名稱表示。
-   多元素材質不可為主要/可顯示的材質。 換句話說，它必須是僅限畫面。 這項限制是由表面格式列舉來表示。
-   不允許使用遞色、Alpha 測試、fogging、混色、點陣 op 或遮罩。 除了 z 測試和樣板測試以外，不會完成任何的後置圖元著色器處理。
-   紋理不能是 mipmap。 建立 mip 鏈將會失敗。
-   相同的專案無法同時設定為轉譯目標的材質。 不過，相同多元素紋理介面的不同元素可以同時是材質和轉譯目標。
-   不支援消除鋸齒。
-   無法篩選多個元素的材質介面（作為材質使用時）。 這項限制可使用 [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)進行驗證。
-   無法鎖定多元素紋理表面。
-   您可以將每個階段指派給不同的階段，以同時使用一個以上的多重元素紋理介面，就像一般材質一樣。
-   多元素紋理介面支援從2.2 到1.0 的轉換轉換，就像使用其他材質格式一樣。
-   部分的執行不會將輸出寫入遮罩套用 (D3DRS \_ COLORWRITEENABLE) 。 可以有獨立色彩寫入遮罩的人員。 這是使用新的功能位來表示。 可用的獨立色彩寫入遮罩數目會等於裝置所能使用的元素數目上限。
-   [**清除**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) [清除已設定為轉譯目標的多重元素材質的所有元素]。

使用多元素紋理時，會遵循下列步驟：

1.  應用程式會藉由檢查多元素材質格式的可用性，來探索這項功能的支援。
2.  應用程式會藉由呼叫 [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)來建立這些表面。
3.  應用程式會使用 [**SetRenderTarget**](/windows/desktop/api) 呼叫將介面設定為呈現目標。 圖元著色器使用 [mov-ps](../direct3dhlsl/mov---ps.md) 指令提供輸出給表面。
4.  呼叫 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) ，以將多元素紋理介面設定至特定階段。 如同其他材質一樣，相同的表面也可同時設定為多個階段。
5.  呼叫 [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)時，會將 D3DSAMP \_ ELEMENTINDEX 設定為多元素紋理中取樣器範例的適當元素編號。 此狀態的預設值為0，表示非多重元素紋理將可運作。 將此狀態設定為不適當的數位會導致未定義的行為-如果多重元素材質只有兩個元素寬，但是會要求取樣器從第四個元素取樣，例如。

## <a name="api-support"></a>API 支援

以下是支援多元素紋理的 API 元素摘要：

-   [D3DFMT \_ MULTI2 \_ ARGB8](d3dformat.md)表面格式表示格式的交錯性質。
-   D3DSAMP \_ ELEMENTINDEX 取樣器狀態會指出要使用的元素索引。
-   下列轉譯狀態支援多元素紋理：

    -   D3DRS \_ COLORWRITEENABLE1
    -   D3DRS \_ COLORWRITEENABLE2
    -   D3DRS \_ COLORWRITEENABLE3

    D3DRS \_ COLORWRITEENABLE 適用于呈現目標 (或元素) 零。

-   [D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS](d3dpmisccaps.md)旗標表示裝置支援多個元素紋理或多個呈現目標的獨立寫入遮罩。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元管線](pixel-pipeline.md)
</dt> </dl>

 

 
