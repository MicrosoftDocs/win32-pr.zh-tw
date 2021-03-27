---
title: 指示-vs_1_1
description: 本章節包含頂點著色器第1版指示的參考資訊 \_ 。
ms.assetid: db3c14ce-6e50-4931-b07f-966acc7ffb0a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1b4def55dfaca19608599d9c79e20d3e0690832c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971337"
---
# <a name="instructions---vs_1_1"></a>指示-vs \_ 1 \_ 1

本章節包含頂點著色器第1版指示的參考資訊 \_ 。

有數種類型的頂點著色器指示，如下表所示。 右邊的資料行表示下列各項：

-   指示位置-每個指令所使用的指令位置數目。
-   設定-非算術指令。 每個著色器都必須有 version 指令，而且必須是第一個指令。
-   算術-這些指示可提供著色器中的數學運算。
-   新的-這些指示是此版本的新指示。

## <a name="instruction-set"></a>指令集



| Name                                                                           | 描述                                                                                                     | 指令插槽 | 設定 | 算術 | 新增 |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------|-------|------------|-----|
| [新增-vs](add---vs.md)                                                       | 新增兩個向量                                                                                                 | 1                 |       | x          | x   |
| [dcl \_ 使用方式輸入 (sm1、sm2、sm3-vs asm) ](dcl-usage-input-register---vs.md) | 宣告輸入頂點暫存器 (查看暫存器 [-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md))  | 0                 | x     |            | x   |
| [def-vs](def---vs.md)                                                       | 定義常數                                                                                                | 0                 | x     |            | x   |
| [dp3-vs](dp3---vs.md)                                                       | 三個元件的點乘積                                                                                     | 1                 |       | x          | x   |
| [dp4-vs](dp4---vs.md)                                                       | 四個元件的點乘積                                                                                      | 1                 |       | x          | x   |
| [dst-vs](dst---vs.md)                                                       | 計算距離向量                                                                                   | 1                 |       | x          | x   |
| [exp-vs](exp---vs.md)                                                       | 完整精確度 2<sup>x</sup>                                                                                    | 10                |       | x          | x   |
| [exp-vs](exp---vs.md)                                                       | 部分有效位數 2<sup>x</sup>                                                                                 | 1                 |       | x          | x   |
| [frc-vs](frc---vs.md)                                                       | 分陣列件                                                                                            | 3                 |       | x          | x   |
| [亮-vs](lit---vs.md)                                                       | 部分光源計算                                                                                    | 1                 |       | x          | x   |
| [記錄檔-vs](log---vs.md)                                                       | Full precision log ₂ (x)                                                                                           | 10                |       | x          | x   |
| [logp-vs](logp---vs.md)                                                     | 部分有效位數記錄₂ (x)                                                                                        | 1                 |       | x          | x   |
| [m3x2-vs](m3x2---vs.md)                                                     | 3x2 乘法                                                                                                    | 2                 |       | x          | x   |
| [m3x3-vs](m3x3---vs.md)                                                     | 3x3 乘法                                                                                                    | 3                 |       | x          | x   |
| [m3x4-vs](m3x4---vs.md)                                                     | 3x4 圓乘法                                                                                                    | 4                 |       | x          | x   |
| [m4x3-vs](m4x3---vs.md)                                                     | 4x3 乘法                                                                                                    | 3                 |       | x          | x   |
| [m4x4-vs](m4x4---vs.md)                                                     | 4x4 乘                                                                                                    | 4                 |       | x          | x   |
| [mad-vs](mad---vs.md)                                                       | 相乘和相加                                                                                                | 1                 |       | x          | x   |
| [最大值-vs](max---vs.md)                                                       | 最大值                                                                                                         | 1                 |       | x          | x   |
| [最小值-vs](min---vs.md)                                                       | 最小值                                                                                                         | 1                 |       | x          | x   |
| [mov-vs](mov---vs.md)                                                       | 移動                                                                                                            | 1                 |       | x          | x   |
| [mul-vs](mul---vs.md)                                                       | 乘以                                                                                                        | 1                 |       | x          | x   |
| [nop-vs](nop---vs.md)                                                       | 無作業。                                                                                                    | 1                 |       | x          | x   |
| [rcp-vs](rcp---vs.md)                                                       | 互惠                                                                                                      | 1                 |       | x          | x   |
| [rsq-vs](rsq---vs.md)                                                       | 互惠平方根                                                                                          | 1                 |       | x          | x   |
| [sge-vs](sge---vs.md)                                                       | 大於或等於比較                                                                                   | 1                 |       | x          | x   |
| [slt-vs](slt---vs.md)                                                       | 小於比較                                                                                               | 1                 |       | x          | x   |
| [sub-vs](sub---vs.md)                                                       | 減去                                                                                                        | 1                 |       | x          | x   |
| [與](vs---vs.md)                                                              | 版本                                                                                                         | 0                 | x     |            | x   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




