---
title: texdepth-ps
description: 計算要在此圖元的深度緩衝區比較測試中使用的深度值。
ms.assetid: f7128dbb-a5f3-4e95-b53b-7432439ae0c4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f39135c34c07a9a20f03c9ebc979647733884b37680ef07b9bc666b882052690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284172"
---
# <a name="texdepth---ps"></a>texdepth-ps

計算要在此圖元的深度緩衝區比較測試中使用的深度值。

## <a name="syntax"></a>Syntax



| texdepth dst |
|--------------|



 

其中

-   dst 是目的地註冊。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdepth              |      |      |      | x    |      |      |       |      |       |



 

此指令會在此圖元的深度緩衝區比較測試中使用 r5. r/r5. g。 藍色和 Alpha 通道中的資料會被忽略。 如果 r5 = 0，則是 r5. r/r5. g = 1.0 的結果。

暫時登錄 r5 是此指令唯一可以使用的暫存器。

執行此指令之後，無法在著色器中使用暫時性登錄 r5。

取樣時，使用此指令可排除較高解析度深度緩衝區的大部分優點。 因為圖元著色器每圖元執行一次，所以 [texm3x2depth-ps](texm3x2depth---ps.md) 或 texdepth 的單一深度值輸出將用於每個子圖元深度比較測試。

## <a name="examples"></a>範例

以下是使用 texdepth 的範例。


```
ps_1_4              
texld  r0, t0        // Sample texture from texture stage 0 (dest 
                     //   register number) into r0
                     // Use texture coordinate data from t0
texcrd r1.rgb, t1    // Load a second set of texture coordinate data into r1
add    r5.rg, r0, r1 // Add the two sets of texture coordinate data
phase                // Phase marker, required when using texdepth instruction
texdepth  r5         // Calculate pixel depth as r5.r / r5.g
                     // Do other color calculations with shader output r0
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




