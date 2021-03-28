---
title: 'callc (sm4-asm) '
description: 有條件地呼叫以程式中的標籤 l 出現位置標示的副程式。
ms.assetid: 7F6E81CE-0C38-499B-B83E-FA76FA154451
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6bc8c9d1e4a99ce25f99253518482181cdb74d8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990759"
---
# <a name="callc-sm4---asm"></a>callc (sm4-asm) 

有條件地呼叫在程式中出現卷 **標 \# l** 的位置所標示的副程式。



| callc { \_ z \|\_nz} src0。選取 \_ 元件，l\# |
|----------------------------------------------|



 



| 項目                                                            | 描述                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 測試條件的元件中。<br/> |
| <span id="l_"></span><span id="L_"></span>*我\#*<br/>      | \[在 \] 副程式的標籤中。<br/>                  |



 

## <a name="remarks"></a>備註

當遇到 [ret](ret--sm4---asm-.md) 時，會在這個呼叫之後，將執行傳回給指令。

標記格式包含著色器中對應標籤的位移，以方便使用。

下列範例顯示呼叫指令。


```
                ...
                callc_z  r1.y, l3 // if all bits in r0.x are 0, call l3
                callc_nz r2.z, l3 // if any bit in r0.x is nonzero, call l3
                ...
                ret
                label l3
                    ...
                    retc_nz r0.x
                    ...
                ret

```



### <a name="restrictions"></a>限制

-   副程式可以嵌套32深度。
-   傳回位址堆疊是由實作為透明管理。
-   如果傳回位址堆疊上已有32個專案，且發出 **呼叫** ，則會略過呼叫。
-   沒有自動參數堆疊。 應用程式可以使用可編制索引的臨時暫存器陣列 (x \# \[ \]) ，以手動方式執行堆疊。 但是，不會顯示副程式呼叫傳回位址，而且會與應用程式所完成的任何手動堆疊管理進行迭。
-   不允許對 *l \#* 參數進行索引。
-   *Src0* 提供的32位暫存器會在位層級進行測試。 如果有任何位為非零值， **callc \_ nz** 將會執行呼叫。 如果所有位都是零， **callc \_ z** 將會執行呼叫。
-   不允許遞迴。

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

 

 





