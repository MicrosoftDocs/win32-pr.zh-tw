---
title: texm3x3tex-ps
description: 執行3x3 矩陣相乘，並使用結果來執行材質查閱。 texm3x3tex 必須搭配兩個 texm3x3pad ps 指令使用。
ms.assetid: bb61cd6f-57d0-4b2d-9186-f04f7f4d3516
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a228b61dbed22dc8d285e0fdc833de53b16e7be7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373939"
---
# <a name="texm3x3tex---ps"></a>texm3x3tex-ps

執行3x3 矩陣相乘，並使用結果來執行材質查閱。 texm3x3tex 必須搭配兩個 [texm3x3pad ps](texm3x3pad---ps.md) 指令使用。

## <a name="syntax"></a>Syntax



| texm3x3tex dst、src |
|---------------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3tex            | x    | x    | x    |      |      |      |       |      |       |



 

此指令會當做三個指示的最後一個，表示3x3 矩陣乘法運算，後面接著紋理查閱。 3x3 矩陣是由第三個材質階段的材質座標和上述兩個材質階段所組成。 產生的三個元件向量 (u、v、w) 用來取樣第3階段中的材質。 所有指派給上述兩個材質階段的材質都會被忽略。 3x3 矩陣相乘通常適用于將一般向量定位至所呈現介面的正確正切空間。

此指令必須搭配 texm3x3pad 指令使用。 材質暫存器必須使用下列順序。


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)  //   where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3tex t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         //   3-vector with which to sample texture
                         //   associated with texture stage m+2
```



以下是有關3x3 乘法如何完成的更多詳細資料。

第一個 texm3x3pad 指令會執行乘法的第一個資料列來尋找 u<sup>'</sup>。

u<sup>'</sup> = TextureCoordinates (階段 m) <sub>UVW</sub> \* t (n) <sub>RGB</sub>

第二個 texm3x3pad 指令會執行乘法的第二個數據列，以找出 v<sup>'</sup>。

v<sup>'</sup> = TextureCoordinates (階段 m + 1) <sub>UVW</sub> \* t (n) <sub>RGB</sub>

Texm3x3spec 指令會執行乘法的第三個數據列，以找出 w<sup>'</sup>。

w<sup>'</sup> = TextureCoordinates (階段 m + 2) <sub>UVW</sub> \* t (n) <sub>RGB</sub>

最後，texm3x3tex 指令範例 t (m + 2) 使用 (u<sup>'</sup>，v<sup>'</sup>，w<sup>'</sup>) 並將結果儲存在 t (m + 2) 中。

t (m + 2) <sub>rgba</sub> = TextureSample (階段 m + 2) 使用 (u<sup>'</sup> ，v<sup>'</sup> ，w<sup>'</sup> ) 作為座標的<sub>RGBA</sub> 。

## <a name="examples"></a>範例

以下是已識別材質地圖和識別材質階段的範例著色器。


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad  t1,  t0   // First row of matrix multiply
texm3x3pad  t2,  t0   // Second row of matrix multiply
texm3x3tex  t3,  t0   // Third row of matrix multiply to get a
                      // 3-vector with which to sample texture at 
mov r0, t3            // stage 3 output result
```



此範例需要下列紋理階段設定。

-   階段0會指派具有一般資料的材質對應。 這通常稱為「凹凸地圖」。 資料是每個材質的 XYZ) 法線 (。 材質座標集合0定義如何取樣此標準地圖。
-   紋理座標集合1會指派給3x3 矩陣的第1列。 指派給階段1的任何材質都會被忽略。
-   紋理座標集合2會指派給3x3 矩陣的第2列。 指派給階段2的任何材質都會被忽略。
-   紋理座標集合3會指派給3x3 矩陣的第3列。 必須將磁片區或 cube 材質設定為第3階段，才能依轉換的3D 向量進行查閱。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




