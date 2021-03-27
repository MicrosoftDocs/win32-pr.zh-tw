---
title: texm3x2depth-ps
description: 計算要用於此圖元深度測試的深度值。
ms.assetid: bacdd471-a6ee-4998-badd-93ffd4fd61d4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26d2c3efd1a31681520828b18d606d618d8c900a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971565"
---
# <a name="texm3x2depth---ps"></a>texm3x2depth-ps

計算要用於此圖元深度測試的深度值。

## <a name="syntax"></a>Syntax



| texm3x2depth dst、src |
|-----------------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2depth          |      |      | x    |      |      |      |       |      |       |



 

此指令必須搭配 [texm3x2pad ps](texm3x2pad---ps.md) 指令使用。

當您使用這兩個指示時，材質暫存器必須使用下列順序。


```
 
tex t(n)                     // Define tn as a standard 3-vector.(tn must be 
                             // defined in some way before it is used
texm3x2pad   t(m),   t(n)    // Where m > n
                             // Calculate z value
texm3x2depth t(m+1), t(n)    // Calculate w value; use both z and w to
                             // find depth
```



深度計算是在使用點乘積運算來尋找 z 和 w 之後完成。 以下是如何完成深度計算的詳細資料。

Texm3x2pad 指令會計算 z。

z = TextureCoordinates (階段 m) <sub>UVW</sub> \* t (n) <sub>RGB</sub>

Texm3x2depth 指令會計算 w。

w = TextureCoordinates (階段 m + 1) <sub>UVW</sub> \* t (n) <sub>RGB</sub>

計算深度並將結果儲存在 t (m + 1) 。


```
 
if (w == 0)
  t(m+1) = 1.0
else
  t(m+1) = z/w
```



計算的深度會標記為要用於圖元的深度測試，並取代圖元的現有深度測試值。

請務必將 z/w 夾具在 (0-1) 的範圍內。 如果 z/w 超出此範圍，則儲存在深度緩衝區的結果將會是未定義的。

執行 texm3x2depth 之後，請註冊 t (m + 1) 不再適用于著色器。

取樣時，使用此指令可排除較高解析度深度緩衝區的大部分優點。 因為圖元著色器每圖元執行一次，所以 texm3x2depth 或 [texdepth](texdepth---ps.md) 的單一深度值輸出將用於每個子圖元深度比較測試。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




