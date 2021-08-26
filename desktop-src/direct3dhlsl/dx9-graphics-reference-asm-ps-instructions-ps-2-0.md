---
title: ps_2_0 指示
description: 本章節包含圖元著色器第2版指示的參考資訊 \_ 。
ms.assetid: 70492436-4d0d-48e6-b3d2-8934931fb5c2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 292263ed6331c8cc878d6dbd9cfa3e4d766c193d2242b841afb926b296675ccf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067988"
---
# <a name="ps_2_0-instructions"></a>ps \_ 2 \_ 0 指示

本章節包含圖元著色器第2版指示的參考資訊 \_ 。

有數種類型的圖元著色器指令，如下表所示。 右邊的資料行表示下列各項：

-   指示位置-每個指令所使用的指令位置數目。
-   設定-圖元著色器必須有版本指令，而且必須是第一個指令。
-   算術-這些指示可提供著色器中的數學運算。
-   材質-這些指示可用來載入和取樣材質資料，以及修改材質座標。
-   新的-這些指示是此版本的新指示。

## <a name="instruction-set"></a>指令集



| 名稱                                                             | 描述                                                                                      | 指令插槽 | 設定 | 算術 | 紋理 | 新增 |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|-----|
| [abs-ps](abs---ps.md)                                         | 絕對值                                                                                   | 1                 |       | x          |         | x   |
| [新增-ps](add---ps.md)                                         | 新增兩個向量                                                                                  | 1                 |       | x          |         |     |
| [cmp-ps](cmp---ps.md)                                         | 比較來源與0                                                                              | 1                 |       | x          |         |     |
| [crs-ps](crs---ps.md)                                         | 交叉乘積                                                                                    | 2                 |       | x          |         | x   |
| [dcl \_ samplerType (sm2、sm3-ps asm) ](dcl-samplertype---ps.md) | 宣告取樣器的材質維度                                                      | 0                 | x     |            |         | x   |
| [dcl- (sm2、sm3-ps asm) ](dcl---ps.md)                        | 宣告頂點著色器輸出暫存器和圖元著色器輸入暫存器之間的關聯。 | 0                 | x     |            |         | x   |
| [def-ps](def---ps.md)                                         | 定義常數                                                                                 | 0                 | x     |            |         |     |
| [dp2add-ps](dp2add---ps.md)                                   | 2D 點乘積和新增                                                                           | 2                 |       | x          |         | x   |
| [dp3-ps](dp3---ps.md)                                         | 3D 點乘積                                                                                   | 1                 |       | x          |         |     |
| [dp4-ps](dp4---ps.md)                                         | 4D 點乘積                                                                                   | 1                 |       | x          |         |     |
| [exp-ps](exp---ps.md)                                         | 完整精確度 2<sup>x</sup>                                                                     | 1                 |       | x          |         | x   |
| [frc-ps](frc---ps.md)                                         | 分陣列件                                                                             | 1                 |       | x          |         | x   |
| [記錄-ps](log---ps.md)                                         | Full precision log ₂ (x)                                                                            | 1                 |       | x          |         | x   |
| [lrp-ps](lrp---ps.md)                                         | 線性插補                                                                               | 2                 |       | x          |         |     |
| [m3x2-ps](m3x2---ps.md)                                       | 3x2 乘法                                                                                     | 2                 |       | x          |         | x   |
| [m3x3-ps](m3x3---ps.md)                                       | 3x3 乘法                                                                                     | 3                 |       | x          |         | x   |
| [m3x4-ps](m3x4---ps.md)                                       | 3x4 圓乘法                                                                                     | 4                 |       | x          |         | x   |
| [m4x3-ps](m4x3---ps.md)                                       | 4x3 乘法                                                                                     | 3                 |       | x          |         | x   |
| [m4x4-ps](m4x4---ps.md)                                       | 4x4 乘                                                                                     | 4                 |       | x          |         | x   |
| [mad-ps](mad---ps.md)                                         | 相乘和相加                                                                                 | 1                 |       | x          |         |     |
| [最大-ps](max---ps.md)                                         | 最大值                                                                                          | 1                 |       | x          |         | x   |
| [最小-ps](min---ps.md)                                         | 最小值                                                                                          | 1                 |       | x          |         | x   |
| [mov-ps](mov---ps.md)                                         | 移動                                                                                             | 1                 |       | x          |         |     |
| [mul-ps](mul---ps.md)                                         | 乘以                                                                                         | 1                 |       | x          |         |     |
| [nop-ps](nop---ps.md)                                         | 無作業。                                                                                     | 1                 |       | x          |         |     |
| [nrm-ps](nrm---ps.md)                                         | 規範                                                                                        | 3                 |       | x          |         | x   |
| [pow-ps](pow---ps.md)                                         | x<sup>y</sup>                                                                                    | 3                 |       | x          |         | x   |
| [Ps](ps---ps.md)                                                | 版本                                                                                          | 0                 | x     |            |         |     |
| [rcp-ps](rcp---ps.md)                                         | 互惠                                                                                       | 1                 |       | x          |         | x   |
| [rsq-ps](rsq---ps.md)                                         | 互惠平方根                                                                           | 1                 |       | x          |         | x   |
| [sincos-ps](sincos---ps.md)                                   | 正弦和余弦                                                                                  | 8                 |       | x          |         | x   |
| [子 ps](sub---ps.md)                                         | 減去                                                                                         | 1                 |       | x          |         |     |
| [texkill-ps](texkill---ps.md)                                 | 終止圖元呈現                                                                                | 1                 |       |            | x       |     |
| [texld-ps \_ 2 \_ 0 和更新的](texld---ps-2-0.md)                    | 範例紋理                                                                                 | 1                 |       |            | x       | x   |
| [texldb-ps](texldb---ps.md)                                   | 使用來自 w 元件的詳細程度偏差進行紋理取樣                                      | 1                 |       |            | x       | x   |
| [texldp-ps](texldp---ps.md)                                   | Projective 除以 w 元件的材質取樣                                           | 1                 |       |            | x       | x   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




