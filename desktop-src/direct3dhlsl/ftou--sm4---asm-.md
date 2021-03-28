---
title: 'ftou (sm4-asm) '
description: 浮點數轉換為不帶正負號的整數。
ms.assetid: 0E3E090B-72C0-4CED-AFA5-2DDCF67D7263
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4a5e65e4bb9d4e71e4a2000f00861cf63e7c181
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313646"
---
# <a name="ftou-sm4---asm"></a>ftou (sm4-asm) 

浮點數轉換為不帶正負號的整數。



| ftou dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle\] |
|----------------------------------------------------|



 



| ftoi dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle\] |
|----------------------------------------------------|



 



| 項目                                                            | 描述                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。 <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[以 \] 轉換的值。<br/>                        |



 

## <a name="remarks"></a>備註

每個元件都會執行轉換。 舍入一律會對零執行，並遵循 C 慣例，從 float 轉換成 int。

需要不同四捨五入語義的應用程式可以在轉換成整數之前叫用 **舍入** 指令。

輸入會壓制至範圍 \[ 0.0 f .。。4294967295.999 f \] 轉換之前，輸入 NaN 值會產生零結果。

選擇性的否定和絕對值修飾詞會在轉換之前套用至來源值。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

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

 

 





