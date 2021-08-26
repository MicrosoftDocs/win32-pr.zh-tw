---
title: 'emitThenCut (sm4-asm) '
description: '相當於發出命令，後面接著剪下命令。 |emitThenCut (sm4-asm) '
ms.assetid: 80DE112A-790A-4DDF-A5BE-51F70BD7872C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab83fa3eca853a75dca74ef32116e3d13da2dbe76f34fa407f9b0d5f2459d66a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023858"
---
# <a name="emitthencut-sm4---asm"></a>emitThenCut (sm4-asm) 

相當於 [發出](emit--sm4---asm-.md) 命令，後面接著 [剪](cut--sm4---asm-.md) 下命令。



| emitThenCut |
|-------------|



 

## <a name="remarks"></a>備註

當故意輸出拓撲中的最後一個頂點時，此命令很有用。

如果已宣告資料流程，您必須使用 [emitthencut \_ 資料流程](emitthencut-stream--sm5---asm-.md)。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
|               | x               |              |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 是       |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 是       |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




