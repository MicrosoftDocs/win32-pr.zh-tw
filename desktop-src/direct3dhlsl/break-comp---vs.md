---
title: break_comp-vs
description: 有條件地中斷最接近 endloop-vs 或 endrep-vs 的目前迴圈。
ms.assetid: 01745e03-874a-4594-b6ab-12db22d0cb4a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 631998aeba6612d945495d8115a74d00f7e657c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841664"
---
# <a name="break_comp---vs"></a>中斷 \_ 複合-vs

有條件地中斷最接近 [endloop-vs](endloop---vs.md) 或 [endrep-vs](endrep---vs.md)的目前迴圈。

## <a name="syntax"></a>Syntax



| break \_ comp src0，src1 |
|------------------------|



 

其中：

-   \_comp 是兩個來源暫存器之間的比較。 可以是下列其中一項： 

    | Syntax | 比較            |
    |--------|-----------------------|
    | \_燃氣輪機   | 大於          |
    | \_淺色   | 小於             |
    | \_通用 電氣   | 大於或等於 |
    | \_樂   | 小於或等於    |
    | \_情 商   | 等於              |
    | \_ne   | 不等於          |

    

     

-   src0 是來源註冊。 需要複寫 swizzle 才能選取單一元件。
-   src1 是來源註冊。 需要複寫 swizzle 才能選取單一元件。

## <a name="remarks"></a>備註

下列版本支援此指令。



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| 中斷 \_ 複合            |      |      | x    | x     | x    | x     |



 

當比較結果為 true 時，它會中斷目前的迴圈，如下所示。


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




