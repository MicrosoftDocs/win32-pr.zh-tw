---
title: ftoi (sm4 - asm)
description: 浮點數轉換為帶正負號的整數。
ms.assetid: 580AB4A6-0C1C-409B-B2B9-BA1D37772F46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02ce1b506d112a59d3087f59d219557575b8def
ms.sourcegitcommit: 8c658e9872a2173e3dcec94195f9067fbcd85d3d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/17/2020
ms.locfileid: "104316669"
---
# <a name="ftoi-sm4---asm"></a>ftoi (sm4 - asm)

浮點數轉換為帶正負號的整數。

| ftoi dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle\] |
|-|

| 項目 | 描述 |
|-|-|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。<br/> *目的地*  = [圓形 \_ z](round-z--sm4---asm-.md) (*src0*) <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 要轉換的元件中。<br/> |

## <a name="remarks"></a>備註

每個元件都會執行轉換。 舍入一律會對零執行，並遵循 C 慣例，從 float 轉換成 int。需要不同四捨五入語義的應用程式可以在轉換成整數之前叫用 **舍入** 指令。

輸入會壓制至 2147483648.999 f 的範圍 ... \[2147483647.999 f \] 轉換之前，輸入 NaN 值會產生零結果。

選擇性的否定和絕對值修飾詞會在轉換之前套用至來源值。

此指示適用于下列著色器階段：

| 頂點著色器 | 幾何著色器 | 像素著色器 |
|-|-|-|
| x | x | x |

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。

| 著色器模型 | 支援 |
|-|-|
| [著色器模型5](d3d11-graphics-reference-sm5.md) | 是 |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md) | 是 |
| [著色器模型4](dx-graphics-hlsl-sm4.md) | 是 |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以 |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以 |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以 |

## <a name="related-topics"></a>相關主題

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
