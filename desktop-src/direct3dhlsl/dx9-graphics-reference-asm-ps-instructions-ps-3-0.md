---
title: ps_3_0 指示
description: 本章節包含圖元著色器 3 0 個指令的參考資訊 \_ 。
ms.assetid: 36972b9b-a4e7-45b4-83f5-959e75d270de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e44d13bfc726830a8c3fb770b34d5563fde2684f5c8bdf3fea54dec2312af4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982858"
---
# <a name="ps_3_0-instructions"></a>ps \_ 3 \_ 0 指示

本章節包含圖元著色器 3 0 個指令的參考資訊 \_ 。

有數種類型的圖元著色器指令，如下表所示。 右邊的資料行表示下列各項：

-   指示位置-每個指令所使用的指令位置數目。
-   設定-圖元著色器必須有版本指令，而且必須是第一個指令。
-   算術-這些指示可提供著色器中的數學運算。
-   材質-這些指示可用來載入和取樣材質資料，以及修改材質座標。
-   Flow 控制項-這些指示會提供靜態和動態流量控制給執行指示。
-   新的-這些指示是此版本的新指示。

## <a name="instruction-set"></a>指令集



| 名稱                                                             | 描述                                                                          | 指令插槽 | 設定 | 算術 | 紋理 | 流量控制 | 新增 |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------|-------|------------|---------|--------------|-----|
| [abs-ps](abs---ps.md)                                         | 絕對值                                                                       | 1                 |       | x          |         |              |     |
| [新增-ps](add---ps.md)                                         | 新增兩個向量                                                                      | 1                 |       | x          |         |              |     |
| [中斷-ps](break---ps.md)                                     | 中斷迴圈 .。。endloop 或 rep .。。endrep 區塊                                  | 1                 |       |            |         | x            |     |
| [中斷 \_ 複合-ps](break-comp---ps.md)                          | 有條件地中斷迴圈 .。。endloop 或 rep .。。具有比較的 endrep 區塊 | 3                 |       |            |         | x            |     |
| [breakp-ps](break-p---ps.md)                                  | 中斷迴圈 .。。endloop 或 rep .。。以述詞為基礎的 endrep 區塊            | 3                 |       |            |         | x            |     |
| [呼叫-ps](call---ps.md)                                       | 呼叫副程式                                                                    | 2                 |       |            |         | x            |     |
| [callnz bool-ps](callnz-bool---ps.md)                         | 如果布林值暫存器不是零，則呼叫副程式                                  | 3                 |       |            |         | x            |     |
| [callnz pred-ps](callnz-pred---ps.md)                         | 如果述詞登錄不是零，則呼叫副程式                                | 3                 |       |            |         | x            |     |
| [cmp-ps](cmp---ps.md)                                         | 比較來源與0                                                                  | 1                 |       | x          |         |              |     |
| [crs-ps](crs---ps.md)                                         | 交叉乘積                                                                        | 2                 |       | x          |         |              |     |
| [dcl \_ samplerType (sm2、sm3-ps asm) ](dcl-samplertype---ps.md) | 宣告取樣器的材質維度                                          | 0                 | x     |            |         |              |     |
| [dcl \_ 語義 (sm3-ps asm) ](dcl-usage---ps.md)              | 宣告輸入和輸出暫存器                                                   | 0                 | x     |            |         |              | x   |
| [def-ps](def---ps.md)                                         | 定義常數                                                                     | 0                 | x     |            |         |              |     |
| [defb-ps](defb---ps.md)                                       | 定義布林常數                                                            | 0                 | x     |            |         |              |     |
| [defi-ps](defi---ps.md)                                       | 定義整數常數                                                           | 0                 | x     |            |         |              |     |
| [dp2add-ps](dp2add---ps.md)                                   | 2D 點乘積和新增                                                               | 2                 |       | x          |         |              |     |
| [dp3-ps](dp3---ps.md)                                         | 3D 點乘積                                                                       | 1                 |       | x          |         |              |     |
| [dp4-ps](dp4---ps.md)                                         | 4D 點乘積                                                                       | 1                 |       | x          |         |              |     |
| [dsx-ps](dsx---ps.md)                                         | X 方向的變化率                                                    | 2                 |       | x          |         |              |     |
| [dsy-ps](dsy---ps.md)                                         | Y 方向的變化率                                                    | 2                 |       | x          |         |              |     |
| [其他-ps](else---ps.md)                                       | 開始其他區塊                                                                  | 1                 |       |            |         | x            |     |
| [endif-ps](endif---ps.md)                                     | 結束 if .。。else 封鎖                                                               | 1                 |       |            |         | x            |     |
| [endloop-ps](endloop---ps.md)                                 | 結束迴圈                                                                           | 2                 |       |            |         | x            | x   |
| [endrep-ps](endrep---ps.md)                                   | 重複區塊的結尾                                                                | 2                 |       |            |         | x            |     |
| [exp-ps](exp---ps.md)                                         | 完整精確度 2<sup>x</sup>                                                         | 1                 |       | x          |         |              |     |
| [frc-ps](frc---ps.md)                                         | 分陣列件                                                                 | 1                 |       | x          |         |              |     |
| [if bool-ps](if-bool---ps.md)                                 | 開始 a if 區塊                                                                    | 3                 |       |            |         | x            |     |
| [如果 \_ 是](if-comp---ps.md)                                | 使用比較來開始 if 區塊                                                  | 3                 |       |            |         | x            |     |
| [若為 pred-ps](if-pred---ps.md)                                 | 開始 a if 區塊 with predication                                                   | 3                 |       |            |         | x            |     |
| [標籤-ps](label---ps.md)                                     | 標籤                                                                                | 0                 |       |            |         | x            |     |
| [記錄-ps](log---ps.md)                                         | Full precision log ₂ (x)                                                                | 1                 |       | x          |         |              |     |
| [迴圈-ps](loop---ps.md)                                       | Loop                                                                                 | 3                 |       |            |         | x            | x   |
| [lrp-ps](lrp---ps.md)                                         | 線性插補                                                                   | 2                 |       | x          |         |              |     |
| [m3x2-ps](m3x2---ps.md)                                       | 3x2 乘法                                                                         | 2                 |       | x          |         |              |     |
| [m3x3-ps](m3x3---ps.md)                                       | 3x3 乘法                                                                         | 3                 |       | x          |         |              |     |
| [m3x4-ps](m3x4---ps.md)                                       | 3x4 圓乘法                                                                         | 4                 |       | x          |         |              |     |
| [m4x3-ps](m4x3---ps.md)                                       | 4x3 乘法                                                                         | 3                 |       | x          |         |              |     |
| [m4x4-ps](m4x4---ps.md)                                       | 4x4 乘                                                                         | 4                 |       | x          |         |              |     |
| [mad-ps](mad---ps.md)                                         | 相乘和相加                                                                     | 1                 |       | x          |         |              |     |
| [最大-ps](max---ps.md)                                         | 最大值                                                                              | 1                 |       | x          |         |              |     |
| [最小-ps](min---ps.md)                                         | 最小值                                                                              | 1                 |       | x          |         |              |     |
| [mov-ps](mov---ps.md)                                         | 移動                                                                                 | 1                 |       | x          |         |              |     |
| [mul-ps](mul---ps.md)                                         | 乘以                                                                             | 1                 |       | x          |         |              |     |
| [nop-ps](nop---ps.md)                                         | 無作業。                                                                         | 1                 |       | x          |         |              |     |
| [nrm-ps](nrm---ps.md)                                         | 規範                                                                            | 3                 |       | x          |         |              |     |
| [pow-ps](pow---ps.md)                                         | x<sup>y</sup>                                                                        | 3                 |       | x          |         |              |     |
| [Ps](ps---ps.md)                                                | 版本                                                                              | 0                 | x     |            |         |              |     |
| [rcp-ps](rcp---ps.md)                                         | 互惠                                                                           | 1                 |       | x          |         |              |     |
| [rep-ps](rep---ps.md)                                         | Repeat                                                                               | 3                 |       |            |         | x            |     |
| [ret-ps](ret---ps.md)                                         | 副程式的結尾                                                                  | 1                 |       |            |         | x            |     |
| [rsq-ps](rsq---ps.md)                                         | 互惠平方根                                                               | 1                 |       | x          |         |              |     |
| [setp \_ 複合](setp-comp---ps.md)                                 | 設定述詞註冊                                                           | 1                 |       |            |         | x            |     |
| [sincos-ps](sincos---ps.md)                                   | 正弦和余弦                                                                      | 8                 |       | x          |         |              |     |
| [子 ps](sub---ps.md)                                         | 減去                                                                             | 1                 |       | x          |         |              |     |
| [texkill-ps](texkill---ps.md)                                 | 終止圖元呈現                                                                    | 2                 |       |            | x       |              |     |
| [texld-ps \_ 2 \_ 0 和更新的](texld---ps-2-0.md)                    | 範例紋理                                                                     | 請參閱附注1        |       |            | x       |              |     |
| [texldb-ps](texldb---ps.md)                                   | 使用來自 w 元件的詳細程度偏差進行紋理取樣                          | 6                 |       |            | x       |              |     |
| [texldl-ps](texldl---ps.md)                                   | 使用來自 w 元件的詳細資料層級進行紋理取樣                               | 請參閱附註 2        |       |            | x       |              | x   |
| [texldd-ps](texldd---ps.md)                                   | 使用使用者提供的漸層進行紋理取樣                                        | 3                 |       |            | x       |              |     |
| [texldp-ps](texldp---ps.md)                                   | Projective 除以 w 元件的材質取樣                               | 請參閱附注3        |       |            | x       |              |     |



 

注意：

1.  如果材質是立方體圖，則插槽 = 4;否則插槽 = 1。
2.  如果材質是立方體圖，則插槽 = 5;否則插槽 = 2。
3.  如果材質是立方體圖，則插槽 = 4;否則插槽 = 3。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




