---
title: 頂點著色器差異
description: 頂點著色器差異
ms.assetid: 94fe4033-94c0-4561-b0fd-1fb85d8f796b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 411a3a742fca508839651d56912fa00b2a6d8b82908b159694a3b1eff88f2318
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982818"
---
# <a name="vertex-shader-differences"></a>頂點著色器差異

## <a name="instruction-slots"></a>指令插槽

每個版本都支援不同數目的最大指令插槽。



| 版本  | 指令位置數目上限                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| vs \_ 1 \_ 1 | 128                                                                                                                               |
| vs \_ 2 \_ 0 | 256                                                                                                                               |
| vs \_ 2 \_ x | 256                                                                                                                               |
| vs \_ 3 \_ 0 | 最小值為512，最多可達 D3DCAPS9 中的插槽數目。MaxVertexShader30InstructionSlots. 請參閱 [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)。 |



 

如需軟體著色器限制的詳細資訊，請參閱 [軟體著色](dx9-graphics-reference-asm-software-shaders.md)器。

## <a name="flow-control-nesting-limits"></a>Flow控制項嵌套限制

-   請參閱[Flow 控制項嵌套限制](dx9-graphics-reference-asm-vs-instructions-flow-control.md)。

## <a name="vs_1_1-features"></a>vs \_ 1 \_ 1 功能

新的指示：

請參閱 [指示-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md)。

新的暫存器：

請參閱暫存器 [-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)。

## <a name="vs_2_0-features"></a>vs \_ 2 \_ 0 功能

新功能︰

-   靜態流程式控制制
-   [Address Register](dx9-graphics-reference-asm-vs-registers-address.md) (a0) 的四個元件都可以使用。

新的指示：

-   設定指示- [defb-vs](defb---vs.md)、 [defi-vs](defi---vs.md)
-   算術指示- [abs-vs](abs---vs.md)、 [crs-vs](crs---vs.md)、 [lrp-vs](lrp---vs.md)、 [mova-vs](mova---vs.md)、 [nrm-vs](nrm---vs.md)、 [pow-vs](pow---vs.md)、 [登錄-vs](sgn---vs.md)、 [sincos-vs](sincos---vs.md)
-   靜態流程式控制制指示-- [call-vs](call---vs.md)、 [callnz bool-vs](callnz-bool---vs.md)、 [else-vs](else---vs.md)、 [endif-vs](endif---vs.md)、 [endloop-vs](endloop---vs.md)、 [endrep-vs](endrep---vs.md)、 [bool-vs](if-bool---vs.md)、 [label-vs](label---vs.md)、[迴圈-](loop---vs.md)vs、 [rep-vs](rep---vs.md)、 [ret](ret---vs.md) -vs

新的暫存器：

-   [常數 Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \#) 
-   [常數整數 Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (我 \#) 
-   [迴圈計數器 Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) 

## <a name="vs_2_x-features"></a>vs \_ 2 \_ x 功能

 (D3DCAPS9 的新功能。VS20Caps) ：

-   動態流程式控制制
-   動態和靜態流程式控制制指示的嵌套
-    (r) 增加的[暫存](dx9-graphics-reference-asm-vs-registers-temporary.md)登錄數目 \#
-   預測

新的指示：

-   動態流程式控制制指示- [break-vs](break---vs.md)、 [break \_ comp-vs](break-comp---vs.md)、 [breakp-vs](breakp---vs.md)、 [callnz pred-vs](callnz-pred---vs.md)、 [if \_ ](if-comp---vs.md) [pred-vs](if-pred---vs.md)、 [setp \_ comp-](setp-comp---vs.md) vs

新的暫存器：

-   述詞[Register](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0) 

## <a name="vs_3_0-features"></a>vs \_ 3 \_ 0 功能

新功能：

-   紋理查閱
-   可編制索引的 [輸出](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) 暫存器 (o \#) 
-    (r [](dx9-graphics-reference-asm-vs-registers-temporary.md) \#) 增加到32的暫存登錄數目

新的指示：

-   設定指令- [dcl \_ samplerType (sm3-vs asm) ](dcl-samplertype---vs.md)
-   材質指令- [texldl-vs](texldl---vs.md)

新的暫存器：

-   [ (Direct3D 9 asm 的取樣器-vs) ](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \#) 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 