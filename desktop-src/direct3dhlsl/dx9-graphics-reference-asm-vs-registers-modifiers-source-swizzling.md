---
title: '來源登錄 Swizzling (HLSL 與參考) '
description: 在執行指令之前，會將來源暫存器中的資料複製到臨時暫存器。 Swizzling 是指將任何來源暫存器元件複製到任何暫存登錄元件的能力。 Swizzling 不會影響來源註冊資料。
ms.assetid: 6271d846-c68d-467c-a110-be3279e0c11a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03dd2d9051c185d1be1ccb6fce18549bf5aa3414975c9a600bb8f8c47f78d4c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854548"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a>來源登錄 Swizzling (HLSL 與參考) 

在執行指令之前，會將來源暫存器中的資料複製到臨時暫存器。 Swizzling 是指將任何來源暫存器元件複製到任何暫存登錄元件的能力。 Swizzling 不會影響來源註冊資料。

## <a name="component-swizzling"></a>元件 Swizzling

如下表所示，swizzling 可以套用至來源暫存器資料的個別元件 (其中是其中一個有效的頂點著色器輸入暫存器 [-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)) 。



| 元件修飾詞                 | 描述    |
|------------------------------------|----------------|
| r。 \[xyzw \] \[ xyzw \] \[ xyzw \] \[ xyzw\] | 來源 swizzle |



 

-   所有四個元件一律都會複製。 如果指定了四個以上的元件，則會重複 (xy 表示 xyyy) 的最後一個元件。 如果未指定任何元件，則 x 會重複 ( xxxx) 。
-   元件可以依任何順序顯示。 v0 ywx 會產生 v0. ywxx。
-   Rgba 元件可以分別用於 xyzw (r for x、g for b 等 ) 。
-   這些指示會實作為來源-註冊單一元件 swizzles： exp、expp、log、logp、pow、rcp、rsq。 這些指示的結果會複製到所有的四個目的地註冊元件。

Swizzling 不能用於 [m3x2-vs](m3x2---vs.md)、 [m3x3-vs](m3x3---vs.md)、 [m4x3-vs](m4x3---vs.md)和 [m4x4-vs](m4x4---vs.md) 指令。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器修飾詞](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




