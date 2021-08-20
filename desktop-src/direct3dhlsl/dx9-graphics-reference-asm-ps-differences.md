---
title: 圖元著色器差異
description: 圖元著色器差異
ms.assetid: 11aefb26-eb82-486c-81ff-7c0cfbab1b7a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b63833b893f02dcf852d9de7547818bf63af07337806601dc5d0707fa4e7860
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908596"
---
# <a name="pixel-shader-differences"></a>圖元著色器差異

## <a name="instruction-slots"></a>指令插槽

每個版本都支援不同數目的最大指令插槽。



| 版本  | 指令位置數目上限                                                                                   |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| ps \_ 1 \_ 1 | 4材質 + 8 算術                                                                                              |
| ps \_ 1 \_ 2 | 4材質 + 8 算術                                                                                              |
| ps \_ 1 \_ 3 | 4材質 + 8 算術                                                                                              |
| ps \_ 1 \_ 4 | 6個材質 + 每個階段8個算術                                                                                    |
| ps \_ 2 \_ 0 | 32材質 + 64 算術                                                                                            |
| ps \_ 2 \_ x | 最小值為96，最多可達 D3DCAPS9 中的插槽數目。D3DPSHADERCAPS2 \_ 0. NumInstructionSlots。 請參閱 D3DPSHADERCAPS2 \_ 0。 |
| ps \_ 3 \_ 0 | 最小值為512，最多可達 D3DCAPS9 中的插槽數目。MaxPixelShader30InstructionSlots. 請參閱 D3DPSHADERCAPS2 \_ 0。      |



 

如需軟體著色器限制的詳細資訊，請參閱 [軟體著色](dx9-graphics-reference-asm-software-shaders.md)器。

## <a name="flow-control-nesting-limits"></a>Flow控制項嵌套限制

-   請參閱[Flow 控制限制](dx9-graphics-reference-asm-ps-instructions-flow-control.md)。

## <a name="ps_1_x-features"></a>ps \_ 1 \_ x 功能

新的指示：

請參閱 [ps \_ 1 \_ 1、ps \_ 1 \_ 2、ps \_ 1 \_ 3、ps \_ 1 \_ 4 指示](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md)。

新的暫存器：

請參閱[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)。

## <a name="ps_2_0-features"></a>ps \_ 2 \_ 0 功能

新功能︰

-   三個新的 swizzles-. yzxw、. zxyw、. wzyx
-    (r) 增加至12的[暫存註冊](dx9-graphics-reference-asm-ps-registers-temporary.md)數目 \#
-   [常數浮點數](dx9-graphics-reference-asm-ps-registers-constant-float.md)暫存器 (c \#) 增加到32的數目
-    (t) 增加為8的[材質座標](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)暫存器數目 \#

新的指示：

-   設定指示- [dcl- (sm2、sm3-ps asm) ](dcl---ps.md)、 [dcl \_ samplerType (sm2、sm3-ps asm) ](dcl-samplertype---ps.md)
-   算術指示- [abs-ps](abs---ps.md)、 [crs-ps](crs---ps.md)、 [dp2add/ps](dp2add---ps.md)、 [exp-ps](exp---ps.md)、 [frc-ps](frc---ps.md)、 [log-ps](log---ps.md)、 [m3x2-ps](m3x2---ps.md)、 [m3x3-ps](m3x3---ps.md)、 [m3x4-ps](m3x4---ps.md)、 [m4x3-ps](m4x3---ps.md)、 [m4x4](m4x4---ps.md) [-ps](nrm---ps.md)、 [max-](max---ps.md) [ps、](min---ps.md) [rcp-ps](rcp---ps.md) [、nrm-](rsq---ps.md)ps、 [](pow---ps.md) [pow-](sincos---ps.md) ps
-   材質指示- [texld-ps \_ 2 \_ 0 和 up](texld---ps-2-0.md) (不同的語法) 、 [texldb-ps](texldb---ps.md)、 [texldp-ps](texldp---ps.md)

新的暫存器：

-   [ (Direct3D 9 asm-ps)  (s 的取樣 ](dx9-graphics-reference-asm-ps-registers-sampler.md) 器 \#) 

## <a name="ps_2_x-features"></a>ps \_ 2 \_ x 功能

新功能 (請參閱 [**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)。 ) ：

-   動態流程式控制制
-   靜態流程式控制制
-   動態和靜態流程式控制制指示的嵌套
-    (r) 增加的[暫存](dx9-graphics-reference-asm-ps-registers-temporary.md)登錄數目 \#
-   任意來源 swizzle
-   漸層指令
-   預測
-   沒有相依材質讀取限制
-   沒有紋理指示限制

新的指示：

-   靜態流程式控制制指示- [如果 bool-ps](if-bool---ps.md)、 [call](call---ps.md)、 [callnz bool-ps](callnz-bool---ps.md)、 [else-ps](else---ps.md)、 [endif-ps](endif---ps.md)、 [rep-ps](rep---ps.md)、 [endrep-ps](endrep---ps.md)、 [label-ps](label---ps.md)、 [ret-ps](ret---ps.md)
-   動態流程式控制制指示-[斷路-ps](break---ps.md)、 [break、 \_ ps](break-comp---ps.md)、 [breakp-ps](break-p---ps.md)、 [callnz pred-ps](callnz-pred---ps.md)（如果[ \_ ](if-comp---ps.md) [pred-ps](if-pred---ps.md)、 [setp \_ comp ps](setp-comp---ps.md) ）
-   算術指示- [dsx-ps](dsx---ps.md)、 [dsy-ps](dsy---ps.md)
-   材質指令- [texldd-ps](texldd---ps.md)

新的暫存器：

-   述詞[Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0) 

## <a name="ps_3_0-features"></a>ps \_ 3 \_ 0 功能

新功能︰

-   合併10個 [輸入 Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \#) 
-   [](dx9-graphics-reference-asm-ps-registers-input-color.md) \# 使用[迴圈計數器 register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL (v) 可編制索引的輸入色彩暫存器) 
-    (r [](dx9-graphics-reference-asm-ps-registers-temporary.md) \#) 增加到32的暫存登錄數目
-    (c) 增加到224的[常數 Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)的數目 \#

新的指示：

-   設定指令- [dcl \_ 語義 (sm3-ps asm) ](dcl-usage---ps.md)
-   靜態流程指示- [迴圈-ps](loop---ps.md)、 [endloop-ps](endloop---ps.md)
-   算術指令- [sincos-ps](sincos---ps.md) (新的語法) 
-   材質指令- [texldl-ps](texldl---ps.md)

新的暫存器：

-   [輸入 Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \#) 
-   [Position Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPos) 
-   [臉部報名](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace) 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 