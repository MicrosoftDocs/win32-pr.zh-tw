---
title: texm3x3spec-ps
description: 執行3x3 矩陣相乘，並使用結果來執行材質查閱。 這可用於反射反映和環境對應。 texm3x3spec 必須搭配兩個 texm3x3pad ps 指令使用。
ms.assetid: 74269bcf-de1d-48b4-a4d0-aa08fd54b8e6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b5fcef771d6d06a1691d5c5e953b76b1c445c7c8df7b2da37b8b4220bef2b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485428"
---
# <a name="texm3x3spec---ps"></a>texm3x3spec-ps

執行3x3 矩陣相乘，並使用結果來執行材質查閱。 這可用於反射反映和環境對應。 texm3x3spec 必須搭配兩個 [texm3x3pad ps](texm3x3pad---ps.md) 指令使用。

## <a name="syntax"></a>Syntax



| texm3x3spec dst、src0、src1 |
|-----------------------------|



 

其中

-   dst 是目的地註冊。
-   src0 和 src1 是來源暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3spec           | x    | x    | x    |      |      |      |       |      |       |



 

此指令會執行3x3 矩陣相乘的最後一個資料列，使用產生的向量做為一般向量以反映眼睛的向量，然後使用反映的向量來執行材質查閱。 著色器會從常數暫存器讀取眼睛光線向量。 3x3 矩陣相乘通常適用于將一般向量定位至所呈現介面的正確正切空間。

3x3 矩陣是由第三個材質階段的材質座標和上述兩個材質階段所組成。 產生的貼文反映向量 (u、v、w) 用來取樣最後紋理階段上的材質。 所有指派給上述兩個材質階段的材質都會被忽略。

此指令必須搭配兩個 texm3x3pad 指令使用。 材質暫存器必須使用下列順序。


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must
                              //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)       //   where m > n
                              // Perform first row of matrix multiply
texm3x3pad  t(m+1), t(n)      // Perform second row of matrix multiply
texm3x3spec t(m+2), t(n), c0  // Perform third row of matrix multiply
                              // Then do a texture lookup on the texture
                              //   associated with texture stage m+2
```



第一個 texm3x3pad 指令會執行乘法的第一個資料列來尋找 u<sup>'</sup>。

u<sup>'</sup> = TextureCoordinates (階段 m) <sub>UVW</sub> \* t (n) <sub>RGB</sub>

第二個 texm3x3pad 指令會執行乘法的第二個數據列，以找出 v<sup>'</sup>。

v<sup>'</sup> = TextureCoordinates (階段 m + 1) <sub>UVW</sub> \* t (n) <sub>RGB</sub>

Texm3x3spec 指令會執行乘法的第三個數據列，以找出 w<sup>'</sup>。

w<sup>'</sup> = TextureCoordinates (階段 m + 2) <sub>UVW</sub> \* t (n) <sub>RGB</sub>

然後，texm3x3spec 指令會進行反映計算。

 (u<sup>'</sup> 、v<sup>'</sup> 、w<sup>'</sup> ) = 2 \* \[ (n \* E) / (n \* n) \] \* n-E

其中的一般 N 是由

N = (u<sup>'</sup> ，v<sup>'</sup> ，w<sup>'</sup> ) 

常數暫存器提供了眼睛向量 E

E = c \# (任何常數暫存器--c0、c1、c2 等等--可以使用) 

最後，texm3x3spec 指令範例 t (m + 2) 使用 (u<sup>'</sup>，v<sup>'</sup>，w<sup>'</sup>) 並將結果儲存在 t (m + 2) 中。

t (m + 2) <sub>RGBA</sub> = TextureSample (階段 m + 2) 使用 (u<sup>'</sup> ，v<sup>'</sup> ，w<sup>'</sup> ) 作為座標的<sub>RGBA</sub>

## <a name="examples"></a>範例

以下是已識別材質地圖和材質階段的範例著色器。


```
ps_1_1
tex t0                    // Bind texture in stage 0 to register t0 (tn must
                          //   be defined in some way before it is used)
texm3x3pad  t1,  t0       // First row of matrix multiply
texm3x3pad  t2,  t0       // Second row of matrix multiply
texm3x3spec t3,  t0,  c#  // Third row of matrix multiply to get a 3-vector
                          // Reflect 3-vector by the eye-ray vector in c#  
                          // Use reflected vector to lookup texture in
                          //   stage 3
mov r0, t3                // Output the result
```



此範例需要下列紋理階段設定。

-   階段0會指派具有一般資料的材質對應。 這通常稱為「凹凸地圖」。 資料是每個材質的 XYZ) 法線 (。 階段 n 的材質座標定義此標準地圖的取樣位置。
-   紋理座標集合 m 會指派給3x3 矩陣的第1列。 指派給階段 m 的任何材質都會被忽略。
-   紋理座標集合 m + 1 會指派給3x3 矩陣的資料列2。 指派給階段 m + 1 的任何材質都會被忽略。
-   紋理座標集合 m + 2 會指派給3x3 矩陣的第3列。 階段 m + 2 是指派給磁片區或 cube 材質地圖。 材質提供色彩資料 (RGBA) 。
-   眼睛向量 E 是由常數暫存器 E = c 所指定 \# 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




