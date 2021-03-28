---
title: texm3x3vspec-ps
description: 執行3x3 矩陣相乘，並使用結果來執行材質查閱。
ms.assetid: 3798bc23-2929-48fe-93ae-5aa025823714
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 28f1ee1ddb0193f9ccdaa4976e4963e748091f37
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103932823"
---
# <a name="texm3x3vspec---ps"></a>texm3x3vspec-ps

執行3x3 矩陣相乘，並使用結果來執行材質查閱。 這可用於反射向量和環境對應，其中的眼睛光線不是常數。 texm3x3vspec 必須搭配兩個 [texm3x3pad ps](texm3x3pad---ps.md) 指令使用。 如果眼睛向量是常數，則 [texm3x3spec 的 ps](texm3x3spec---ps.md) 指令會執行相同的矩陣乘法和紋理查閱。

## <a name="syntax"></a>Syntax



| texm3x3vspec dst、src |
|-----------------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3vspec          | x    | x    | x    |      |      |      |       |      |       |



 

此指令會執行3x3 矩陣乘法運算的最後一個資料列，將產生的向量視為一般向量以反映眼睛的向量，然後使用反映的向量作為紋理查閱的材質位址。 它的運作方式就像 [texm3x3spec-ps](texm3x3spec---ps.md)，不同之處在于，會從紋理座標的第四個元件取得眼睛光線向量。 3x3 矩陣相乘通常適用于將一般向量定位至所呈現介面的正確正切空間。

3x3 矩陣是由第三個材質階段的材質座標和上述兩個材質階段所組成。 產生的後置反映向量 (UVW) 用來取樣第3階段中的材質。 所有指派給上述兩個材質階段的材質都會被忽略。

此指令必須搭配 texm3x3pad 指令使用。 材質暫存器必須使用下列順序。


```
tex t(n)                    // Define tn as a standard 3-vector (tn must
                            //   be defined in some way before it is used)
texm3x3pad   t(m),   t(n)   // where m > n
                            // Perform first row of matrix multiply
texm3x3pad   t(m+1), t(n)   // Perform second row of matrix multiply
texm3x3vspec t(m+2), t(n)   // Perform third row of matrix multiply
                            // Then do a texture lookup on the texture
                            // associated with texture stage m+2
```



第一個 texm3x3pad 指令會執行乘法的第一個資料列來尋找 u<sup>'</sup>。

u<sup>'</sup> = TextureCoordinates (階段 m) <sub>UVW</sub> \* t (n) <sub>RGB</sub>

第二個 texm3x3pad 指令會執行乘法的第二個數據列，以找出 v<sup>'</sup>。

v<sup>'</sup> = TextureCoordinates (階段 m + 1) <sub>UVW</sub> \* t (n) <sub>RGB</sub>

Texm3x3spec 指令會執行乘法的第三個數據列，以找出 w<sup>'</sup>。

w<sup>'</sup> = TextureCoordinates (階段 m + 2) <sub>UVW</sub> \* t (n) <sub>RGB</sub>

Texm3x3vspec 指令也會進行反映計算。

 (u<sup>'</sup> 、v<sup>'</sup> 、w<sup>'</sup> ) = 2 \* \[ (n \* E) / (n \* n) \] \* n-E

其中的一般 N 是由

N = (u<sup>'</sup> ，v<sup>'</sup> ，w<sup>'</sup> ) 

而眼睛向量 E 的指定方式為

E = (TextureCoordinates (階段 m) <sub>Q</sub> ，

TextureCoordinates (階段 m + 1) <sub>Q</sub> ，

TextureCoordinates (階段 m + 2) <sub>Q</sub> ) 

最後，texm3x3vspec 指令範例 t (m + 2) 使用 (u<sup>'</sup>，v<sup>'</sup>，w<sup>'</sup>) 並將結果儲存在 t (m + 2) 中。

t (m + 2) <sub>RGBA</sub> = TextureSample (階段 m + 2) 使用 (u<sup>'</sup> ，v<sup>'</sup> ，w<sup>'</sup> ) 作為座標的<sub>RGBA</sub>

## <a name="examples"></a>範例

以下是已識別材質地圖和識別材質階段的範例著色器。


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad   t1,  t0  // First row of matrix multiply
texm3x3pad   t2,  t0  // Second row of matrix multiply
texm3x3vspec t3,  t0  // Third row of matrix multiply to get a 3-vector
                      // Reflect 3-vector by the eye-ray vector
                      // Use reflected vector to do a texture lookup
                      //   at stage 3
mov r0, t3            // Output the result
```



此範例需要下列紋理階段設定。

-   階段0會指派具有一般資料的材質對應。 這通常稱為「凹凸地圖」。 資料是每個材質的 XYZ) 法線 (。 階段 n 的材質座標定義如何取樣此標準地圖。
-   紋理座標集合 m 會指派給3x3 矩陣的第1列。 指派給階段 m 的任何材質都會被忽略。
-   紋理座標集合 m + 1 會指派給3x3 矩陣的資料列2。 指派給階段 m + 1 的任何材質都會被忽略。
-   紋理座標集合 m + 2 會指派給3x3 矩陣的第3列。 階段 m + 2 是指派給磁片區或 cube 材質地圖。 材質提供色彩資料 (RGBA) 。
-   眼睛向量 E 會傳遞至第四個元件中的指示， (q) 的材質座標資料階段 m、m + 1 和 m + 2。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




