---
title: 'bufinfo (sm5-asm) '
description: 查詢緩衝區上的元素計數 (但不是常數緩衝區) 。
ms.assetid: 3A5C28F3-FE59-4C67-92AC-66B10E1D9692
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8dd33871aa5bd56db6e7375979c6d49f374b74
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990762"
---
# <a name="bufinfo-sm5---asm"></a>bufinfo (sm5-asm) 

查詢緩衝區上的元素計數 (但不是常數緩衝區) 。



| bufinfo dest \[ . mask \] ，srcResource |
|------------------------------------|



 



| 項目                                                                                                               | 描述                                                                           |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                    | \[在 \] 結果的位址中。<br/>                                         |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[在 \] 緩衝區中，不是常數緩衝區，而是在 SRV (t \#) 或 UAV (u \#) 。<br/> |



 

## <a name="remarks"></a>備註

*Dest* 中的所有元件都會收到緩衝區 s 著色器資源檢視中的整數元素數。 元素數目取決於 view 參數，例如記憶體格式。

如果是具類型的緩衝區 SRV 或 UAV，則傳回值是 view 中的元素數目 (其中元素是) 類型的一個單位。

若為原始緩衝區 SRV 或 UAV，則傳回值為 view 中的位元組數目。

若為結構化緩衝區 SRV 或 UAV，則傳回值為視圖中的結構數目。

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

 

 





