---
title: '捨棄 (sm4-asm) '
description: 有條件地標示圖元著色器的結果，以在到達程式結束時捨棄。
ms.assetid: 566C4A9A-B32A-4AA6-A888-70F6965B1B5A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba6b5744ee8cf8d2953247711d95fe5d5ec6f96c36c700e1a38ce4e0cb1e1ff5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986598"
---
# <a name="discard-sm4---asm"></a>捨棄 (sm4-asm) 

有條件地標示圖元著色器的結果，以在到達程式結束時捨棄。



| 捨棄 { \_ z \|\_nz} src0. 選取 \_ 元件 |
|-------------------------------------------|



 



| 項目                                                            | 描述                                                                                       |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[\]值，這個值會決定是否要捨棄目前正在處理的圖元。<br/> |



 

## <a name="remarks"></a>備註

此指令會將目前的圖元標示為已終止，並繼續執行，如此一來，平行執行的其他圖元可能會在必要時取得衍生。 雖然繼續執行， **但在捨棄指令之前** 或之後的所有圖元著色器輸出寫入都會被捨棄。

若為 **捨棄 \_ z**，如果 src0 中的所有位， *select \_ 元件* 為零，則會捨棄圖元。

若為 **捨棄 \_ nz**，src0 中的任何位 *。 \_ select 元件* 為非零值，則會捨棄圖元。

此外， **捨棄** 指令可以存在於任何流程式控制制結構內。

著色器中可能會有多個 **捨棄** 指令，而且如果有任何執行的，則會結束圖元。

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
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





