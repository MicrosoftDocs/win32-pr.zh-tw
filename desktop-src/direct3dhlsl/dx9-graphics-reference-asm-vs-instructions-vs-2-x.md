---
title: 指示-vs_2_x
description: 本章節包含頂點著色器第2版 x 指令的參考資訊 \_ 。
ms.assetid: fac85f96-0f4b-49a8-9c00-9e68000d1c76
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e9997e26625005abd0f2e38ab885b95b8f8febd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990639"
---
# <a name="instructions---vs_2_x"></a>指示-vs \_ 2 \_ x

本章節包含頂點著色器第2版 x 指令的參考資訊 \_ 。

有數種類型的頂點著色器指示，如下表所示。 右邊的資料行表示下列各項：

-   指示位置-每個指令所使用的指令位置數目。
-   設定-非算術指令。 每個著色器都必須有 version 指令，而且必須是第一個指令。
-   算術-這些指示可提供著色器中的數學運算。
-   流程式控制制-這些指示會新增流程式控制制功能，例如 [迴圈-與](loop---vs.md).。。[endloop-vs](endloop---vs.md)、 [if bool-vs](if-bool---vs.md).。。[其他](else---vs.md).。。[endif](endif---vs.md)和副程式呼叫。
-   新的-這些指示是此版本的新指示。

## <a name="instruction-set"></a>指令集



| Name                                                                           | 描述                                                                                                                                                            | 指令插槽 | 設定 | 算術 | 流量控制 | 新增 |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|--------------|-----|
| [abs-vs](abs---vs.md)                                                       | 絕對值                                                                                                                                                         | 1                 |       | x          |              |     |
| [新增-vs](add---vs.md)                                                       | 新增兩個向量                                                                                                                                                        | 1                 |       | x          |              |     |
| [中斷-vs](break---vs.md)                                                   | 中斷 [迴圈-與](loop---vs.md).。。[endloop-vs](endloop---vs.md) 或 [rep](rep---vs.md).。。[endrep](endrep---vs.md) 區塊                                  | 1                 |       |            | x            | x   |
| [中斷 \_ 複合-vs](break-comp---vs.md)                                        | 有條件地中斷 [迴圈-相對](loop---vs.md)于 .。。[endloop-vs](endloop---vs.md) 或 [rep](rep---vs.md).。。具有比較的[endrep](endrep---vs.md) 區塊 | 3                 |       |            | x            | x   |
| [breakp-vs](breakp---vs.md)                                                 | 中斷 [迴圈-與](loop---vs.md).。。[endloop-vs](endloop---vs.md) 或 [rep](rep---vs.md).。。以述詞為基礎的[endrep](endrep---vs.md) 區塊            | 3                 |       |            | x            | x   |
| [呼叫-vs](call---vs.md)                                                     | 呼叫副程式                                                                                                                                                      | 2                 |       |            | x            |     |
| [callnz bool-vs](callnz-bool---vs.md)                                       | 如果布林值暫存器不是零，則呼叫副程式                                                                                                                    | 3                 |       |            | x            |     |
| [callnz pred-vs](callnz-pred---vs.md)                                       | 如果述詞登錄不是零，則呼叫副程式                                                                                                                  | 3                 |       |            | x            | x   |
| [crs-vs](crs---vs.md)                                                       | 交叉乘積                                                                                                                                                          | 2                 |       | x          |              |     |
| [dcl \_ 使用方式輸入 (sm1、sm2、sm3-vs asm) ](dcl-usage-input-register---vs.md) | 宣告輸入頂點暫存器 (查看暫存器 [-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md))                                                         | 0                 | x     |            |              |     |
| [def-vs](def---vs.md)                                                       | 定義常數                                                                                                                                                       | 0                 | x     |            |              |     |
| [defb-vs](defb---vs.md)                                                     | 定義布林常數                                                                                                                                              | 0                 | x     |            |              |     |
| [defi-vs](defi---vs.md)                                                     | 定義整數常數                                                                                                                                             | 0                 | x     |            |              |     |
| [dp3-vs](dp3---vs.md)                                                       | 三個元件的點乘積                                                                                                                                            | 1                 |       | x          |              |     |
| [dp4-vs](dp4---vs.md)                                                       | 四個元件的點乘積                                                                                                                                             | 1                 |       | x          |              |     |
| [dst-vs](dst---vs.md)                                                       | 計算距離向量                                                                                                                                          | 1                 |       | x          |              |     |
| [else-vs](else---vs.md)                                                     | 開始 [其他-vs](else---vs.md) 區塊                                                                                                                              | 1                 |       |            | x            |     |
| [endif-vs](endif---vs.md)                                                   | 如果是 [bool，則](if-bool---vs.md)結束[else-vs](else---vs.md) block                                                                                             | 1                 |       |            | x            |     |
| [endloop-vs](endloop---vs.md)                                               | [迴圈結束-vs](loop---vs.md) block                                                                                                                              | 2                 |       |            | x            |     |
| [endrep-vs](endrep---vs.md)                                                 | 重複區塊的結尾                                                                                                                                                  | 2                 |       |            | x            |     |
| [exp-vs](exp---vs.md)                                                       | 完整精確度 2<sup>x</sup>                                                                                                                                           | 1                 |       | x          |              |     |
| [exp-vs](exp---vs.md)                                                       | 部分有效位數 2<sup>x</sup>                                                                                                                                        | 1                 |       | x          |              |     |
| [frc-vs](frc---vs.md)                                                       | 分陣列件                                                                                                                                                   | 1                 |       | x          |              |     |
| [if bool-vs](if-bool---vs.md)                                               | 使用布林值條件開始 [if bool-vs](if-bool---vs.md) 區塊 ()                                                                                             | 3                 |       |            | x            |     |
| [如果是 \_ 複合-vs](if-comp---vs.md)                                              | 使用比較來開始 [if bool-vs](if-bool---vs.md) 區塊                                                                                                     | 3                 |       |            | x            | x   |
| [如果 pred-vs](if-pred---vs.md)                                               | 以述詞條件開頭 [if bool-vs](if-bool---vs.md) 區塊                                                                                             | 3                 |       |            | x            | x   |
| [標籤-vs](label---vs.md)                                                   | 標籤                                                                                                                                                                  | 0                 |       |            | x            |     |
| [亮-vs](lit---vs.md)                                                       | 部分光源計算                                                                                                                                           | 3                 |       | x          |              |     |
| [記錄檔-vs](log---vs.md)                                                       | Full precision log ₂ (x)                                                                                                                                                  | 1                 |       | x          |              |     |
| [logp-vs](logp---vs.md)                                                     | 部分有效位數記錄₂ (x)                                                                                                                                               | 1                 |       | x          |              |     |
| [迴圈-vs](loop---vs.md)                                                     | Loop                                                                                                                                                                   | 3                 |       |            | x            |     |
| [lrp-vs](lrp---vs.md)                                                       | 線性插補                                                                                                                                                   | 2                 |       | x          |              |     |
| [m3x2-vs](m3x2---vs.md)                                                     | 3x2 乘法                                                                                                                                                           | 2                 |       | x          |              |     |
| [m3x3-vs](m3x3---vs.md)                                                     | 3x3 乘法                                                                                                                                                           | 3                 |       | x          |              |     |
| [m3x4-vs](m3x4---vs.md)                                                     | 3x4 圓乘法                                                                                                                                                           | 4                 |       | x          |              |     |
| [m4x3-vs](m4x3---vs.md)                                                     | 4x3 乘法                                                                                                                                                           | 3                 |       | x          |              |     |
| [m4x4-vs](m4x4---vs.md)                                                     | 4x4 乘                                                                                                                                                           | 4                 |       | x          |              |     |
| [mad-vs](mad---vs.md)                                                       | 相乘和相加                                                                                                                                                       | 1                 |       | x          |              |     |
| [最大值-vs](max---vs.md)                                                       | 最大值                                                                                                                                                                | 1                 |       | x          |              |     |
| [最小值-vs](min---vs.md)                                                       | 最小值                                                                                                                                                                | 1                 |       | x          |              |     |
| [mov-vs](mov---vs.md)                                                       | 移動                                                                                                                                                                   | 1                 |       | x          |              |     |
| [mova-vs](mova---vs.md)                                                     | 將資料從浮點暫存器移至位址暫存器 (a0)                                                                                                   | 1                 |       | x          |              |     |
| [mul-vs](mul---vs.md)                                                       | 乘以                                                                                                                                                               | 1                 |       | x          |              |     |
| [nop-vs](nop---vs.md)                                                       | 無作業。                                                                                                                                                           | 1                 |       | x          |              |     |
| [nrm-vs](nrm---vs.md)                                                       | 將4D 向量標準化                                                                                                                                                  | 3                 |       | x          |              |     |
| [pow-vs](pow---vs.md)                                                       | x<sup>y</sup>                                                                                                                                                          | 3                 |       | x          |              |     |
| [rcp-vs](rcp---vs.md)                                                       | 互惠                                                                                                                                                             | 1                 |       | x          |              |     |
| [rep-vs](rep---vs.md)                                                       | Repeat                                                                                                                                                                 | 3                 |       |            | x            |     |
| [ret-vs](ret---vs.md)                                                       | 副程式或 main 的結尾                                                                                                                                     | 1                 |       |            | x            |     |
| [rsq-vs](rsq---vs.md)                                                       | 互惠平方根                                                                                                                                                 | 1                 |       | x          |              |     |
| [setp \_ 複合-vs](setp-comp---vs.md)                                          | 設定述詞註冊                                                                                                                                             | 1                 |       |            | x            | x   |
| [sge-vs](sge---vs.md)                                                       | 大於或等於比較                                                                                                                                          | 1                 |       | x          |              |     |
| [登錄-vs](sgn---vs.md)                                                       | 簽署                                                                                                                                                                   | 3                 |       | x          |              |     |
| [sincos-vs](sincos---vs.md)                                                 | 正弦和余弦                                                                                                                                                        | 8                 |       | x          |              |     |
| [slt-vs](slt---vs.md)                                                       | 小於比較                                                                                                                                                      | 1                 |       | x          |              |     |
| [sub-vs](sub---vs.md)                                                       | 減去                                                                                                                                                               | 1                 |       | x          |              |     |
| [與](vs---vs.md)                                                              | 版本                                                                                                                                                                | 0                 | x     |            |              |     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




