---
title: 'deriv_rtx (sm4-asm) '
description: Src0 的每個 float32 元件的內容變化率 (swizzle 後) ，與 RenderTarget x 方向 (rtx) 或 RenderTarget y 方向有關。
ms.assetid: 2438DB36-C348-4854-AE1B-EC3C890B0B42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d4543805c02cf70d9c6b7856461c427788f616
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373723"
---
# <a name="deriv_rtx-sm4---asm"></a>deriv \_ rtx (sm4-asm) 

*Src0* 的每個 float32 元件的內容變化率 (swizzle 後) ，與 RenderTarget x 方向 (rtx) 或 RenderTarget y 方向有關。



| deriv \_ rtx \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] ， |
|--------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在作業 \] 的元件中。<br/>             |



 

## <a name="remarks"></a>備註

每個2x2 的圖元戳記都只會計算單一 x、y 衍生配對。

這項操作與硬體相依。

三角形的參考轉譯器執行：

-   圖元著色器一律會透過密集建置 (中的2x2 四個圖元來執行著色器，即使是透過流量控制、遮罩停用的圖元) 。
-   四邊形永遠有偶數的圖元座標， (左上圖元的 x 和 y) 。
-   如果基本類型太小，無法填滿2x2 的四個，則虛擬圖元會關閉基本型別。
-   **deriv \_ rtx** 的計算方式是先選擇2圖元：目前的圖元，以及與四的 y 座標相同的另一個圖元。 然後，結果會計算為： *src0* (奇數 x 圖元) - *src0* (偶數 x 圖元) \[ 每個元件\]
-   [deriv \_ rty](deriv-rty--sm4---asm-.md) 的計算方式是先選擇2個圖元：目前的圖元，以及與四個相同 x 座標的另一個圖元。 然後，結果會計算為： *src0* (奇數 y 圖元) - *src0* (偶數 y 圖元) \[ 每個元件\]

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 是       |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 是       |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





