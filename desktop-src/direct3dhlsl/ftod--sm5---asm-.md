---
title: 'ftod (sm5-asm) '
description: 從單精確度浮點數到雙精確度浮點數據的元件取向轉換。
ms.assetid: 95297556-41ED-4ED0-8F9A-16B7A440AF25
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6790735745805426d32aefcc5d5d771ade644e43
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313706"
---
# <a name="ftod-sm5---asm"></a>ftod (sm5-asm) 

從單精確度浮點數到雙精確度浮點數據的元件取向轉換。



| ftod dest \[ . mask \] 、 \[ - \] src \[ . swizzle \] 、 |
|-------------------------------------------|



 



| 項目                                                            | 描述                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[已 \] 轉換資料的位址。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 要轉換的資料中。<br/>          |



 

## <a name="remarks"></a>備註

來源的每個元件都會從單精確度表示轉換為雙精確度標記法。

有效的 *目的地* 遮罩是 xy、. zw 和. xyzw。 xy 接收第一個轉換的結果，而. zw 會接收第二個轉換的結果。

*dest* 是跨 (x 32LSB、y 32MSB) 和 (z 32LSB、w 32MSB) 的雙 vec2。

*src* 是跨 x 和 y 的 float vec2 (zw 會) 忽略 (swizzle 後) 。

針對 float32<->雙精度浮點數轉換，執行可能會接受 denorms 或清除它們。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此指令：



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 不可以        |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 不可以        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





