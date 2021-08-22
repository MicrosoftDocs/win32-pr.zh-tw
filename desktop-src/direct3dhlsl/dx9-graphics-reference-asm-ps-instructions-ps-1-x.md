---
title: ps_1_1、ps_1_2、ps_1_3 ps_1_4 指示
description: 本章節包含圖元著色器第1版指示的參考資訊 \_ 。
ms.assetid: cb496887-6755-4f29-b465-a36548b88722
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 217e207d2f60d39979c7117cb48e0cb033fd98c6fbfb419642ff43e59759d510
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119732"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4-instructions"></a>ps \_ 1 \_ 1、ps \_ 1 \_ 2、ps \_ 1 \_ 3、ps \_ 1 \_ 4 指示

本章節包含圖元著色器第 1 X 個指令的參考資訊 \_ 。

有數種類型的圖元著色器指令，如下表所示。

## <a name="instruction-set"></a>指令集



| 版本                                    | 描述                                                                   | 指令插槽 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
|--------------------------------------------|-------------------------------------------------------------------------------|-------------------|------|------|------|------|
| [Ps](ps---ps.md)                          | 版本號碼                                                                | 0                 | x    | x    | x    | x    |
| 常數指示                      |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [def-ps](def---ps.md)                   | 定義常數                                                              | 0                 | x    | x    | x    | x    |
| 階段指示                         |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [階段-ps](phase---ps.md)               | 第1階段和第2階段之間的轉換                                        | 0                 |      |      |      | x    |
| 算術指示                    |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [新增-ps](add---ps.md)                   | 新增兩個向量                                                               | 1                 | x    | x    | x    | x    |
| [bem-ps](bem---ps.md)                   | 套用假的凸塊環境對應轉換                                   | 2                 |      |      |      | x    |
| [cmp-ps](cmp---ps.md)                   | 比較來源與0                                                           | 1¹                |      | x    | x    | x    |
| [cnd-ps](cnd---ps.md)                   | 比較來源與0。5                                                         | 1                 | x    | x    | x    | x    |
| [dp3-ps](dp3---ps.md)                   | 三個元件的點乘積                                                   | 1                 | x    | x    | x    | x    |
| [dp4-ps](dp4---ps.md)                   | 四個元件的點乘積                                                    | 1¹                |      | x    | x    | x    |
| [lrp-ps](lrp---ps.md)                   | 線性插補                                                            | 1                 | x    | x    | x    | x    |
| [mad-ps](mad---ps.md)                   | 相乘和相加                                                              | 1                 | x    | x    | x    | x    |
| [mov-ps](mov---ps.md)                   | 移動                                                                          | 1                 | x    | x    | x    | x    |
| [mul-ps](mul---ps.md)                   | 乘以                                                                      | 1                 | x    | x    | x    | x    |
| [nop-ps](nop---ps.md)                   | 無作業。                                                                  | 0                 | x    | x    | x    | x    |
| [子 ps](sub---ps.md)                   | 減去                                                                      | 1                 | x    | x    | x    | x    |
| 材質指示                       |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [tex-ps](tex---ps.md)                   | 範例紋理                                                              | 1                 | x    | x    | x    |      |
| [texbem-ps](texbem---ps.md)             | 套用假的凸塊環境對應轉換                                   | 1                 | x    | x    | x    |      |
| [texbeml-ps](texbeml---ps.md)           | 套用具有亮度校正的假凸塊環境對應轉換         | 1 +1 ²              | x    | x    | x    |      |
| [texcoord-ps](texcoord---ps.md)         | 將材質座標資料解讀為色彩資料                               | 1                 | x    | x    | x    |      |
| [texcrd-ps](texcrd---ps.md)             | 將材質座標資料複製為色彩資料                                    | 1                 |      |      |      | x    |
| [texdepth-ps](texdepth---ps.md)         | 計算深度值                                                        | 1                 |      |      |      | x    |
| [texdp3-ps](texdp3---ps.md)             | 紋理資料和材質座標之間的三個元件點乘積  | 1                 |      | x    | x    |      |
| [texdp3tex-ps](texdp3tex---ps.md)       | 三個元件的點乘積和1D 紋理查閱                             | 1                 |      | x    | x    |      |
| [texkill-ps](texkill---ps.md)           | 根據比較來取消圖元呈現                             | 1                 | x    | x    | x    | x    |
| [texld-ps \_ 1 \_ 4](texld---ps-1-4.md)     | 範例紋理                                                              | 1                 |      |      |      | x    |
| [texm3x2depth-ps](texm3x2depth---ps.md) | 計算每圖元深度值                                              | 1                 |      |      | x    |      |
| [texm3x2pad-ps](texm3x2pad---ps.md)     | 兩個數據列矩陣相乘的第一個資料列矩陣乘積                        | 1                 | x    | x    | x    |      |
| [texm3x2tex-ps](texm3x2tex---ps.md)     | 兩個數據列矩陣相乘的最後一個資料列矩陣乘積                        | 1                 | x    | x    | x    |      |
| [texm3x3-ps](texm3x3---ps.md)           | 3x3 矩陣相乘                                                           | 1                 |      | x    | x    |      |
| [texm3x3pad-ps](texm3x3pad---ps.md)     | 三個數據列矩陣相乘的第一個或第二個數據列相乘                   | 1                 | x    | x    | x    |      |
| [texm3x3spec-ps](texm3x3spec---ps.md)   | 三個數據列矩陣相乘的最後一個資料列相乘                             | 1                 | x    | x    | x    |      |
| [texm3x3tex-ps](texm3x3tex---ps.md)     | 使用3x3 矩陣相乘的材質查閱                                   | 1                 | x    | x    | x    |      |
| [texm3x3vspec-ps](texm3x3vspec---ps.md) | 紋理查閱使用3x3 矩陣乘法（具有非固定的眼睛向量） | 1                 | x    | x    | x    |      |
| [texreg2ar-ps](texreg2ar---ps.md)       | 使用 Alpha 和 red 元件的材質範例                           | 1                 | x    | x    | x    |      |
| [texreg2gb-ps](texreg2gb---ps.md)       | 使用綠色和藍色元件取樣材質                          | 1                 | x    | x    | x    |      |
| [texreg2rgb-ps](texreg2rgb---ps.md)     | 使用紅色、綠色和藍色元件來取樣材質                     | 1                 |      | x    | x    |      |



 

1.  1個插槽（ps \_ 1 \_ 4）; ps \_ 1 \_ 2 和 ps \_ 1 \_ 3 中的2個插槽
2.  1 + 1 = 1 算術指令 + 1 個材質指令

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




