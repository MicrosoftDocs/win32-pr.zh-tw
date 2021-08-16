---
title: texm3x2tex-ps
description: 執行3x2 矩陣相乘的最後一個資料列，並使用結果來執行材質查閱。 texm3x2tex 必須搭配 texm3x2pad ps 指令使用。
ms.assetid: c6cfbf75-4a63-4c82-9fb6-286b51b7f883
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9653325098b05959fcbd9e7a838801652a532d936bdaebc829055b717a49096f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723016"
---
# <a name="texm3x2tex---ps"></a>texm3x2tex-ps

執行3x2 矩陣相乘的最後一個資料列，並使用結果來執行材質查閱。 texm3x2tex 必須搭配 [texm3x2pad ps](texm3x2pad---ps.md) 指令使用。

## <a name="syntax"></a>Syntax



| texm3x2tex dst、src |
|---------------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2tex            | x    | x    | x    |      |      |      |       |      |       |



 

指令會用來做為兩個表示3x2 矩陣乘法運算的指示之一。 此指令必須搭配 [texm3x2pad ps](texm3x2pad---ps.md) 指令使用。

當您使用這兩個指示時，材質暫存器必須使用下列順序。


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must 
                              // be defined in some way before it is used)
texm3x2pad  t(m),   t(n)      // where m > n
                              // Perform first row of matrix multiply
texm3x2tex  t(m+1), t(n)      // Perform second row of matrix multiply 
                              // to get (u,v) to sample texture 
                              // associated with stage m+1
```



以下是如何完成3x2 乘法的詳細資料。

Texm3x2pad 指令會執行乘法的第一個資料列來尋找 u<sup>'</sup>。

u<sup>'</sup> = t (n) <sub>RGB</sub> \* TextureCoordinates (階段 m) <sub>UVW</sub>

Texm3x2tex 指令會執行乘法的第二個數據列，以找出 v<sup>'</sup>。

v<sup>'</sup> = t (n) <sub>RGB</sub> \* TextureCoordinates (階段 m + 1) <sub>UVW</sub>

Texm3x2tex 指令會使用 (u<sup>'</sup>，v<sup>'</sup>) ，在階段 (m + 1) 的材質取樣，並將結果儲存在 t (m + 1) 中。

t (m + 1) <sub>RGB</sub> = TextureSample (階段 m + 1) <sub>RGB</sub> 使用 (u<sup>'</sup>，v<sup>'</sup> ) 作為座標

## <a name="examples"></a>範例

以下是已識別材質地圖和材質階段的範例著色器。


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x2pad  t1,  t0   // First row of matrix multiply
texm3x2tex  t2,  t0   // Second row of matrix multiply to get (u,v)
                      // with which to sample texture in stage 2
mov r0, t2            // Output result
```



此範例需要下列紋理階段中的材質。

-   階段0採用的地圖具有 (x、y、z) 更動資料。
-   階段1保存材質座標。 紋理階段中不需要材質。
-   階段2同時保有紋理座標，以及該材質階段的2D 材質集。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




