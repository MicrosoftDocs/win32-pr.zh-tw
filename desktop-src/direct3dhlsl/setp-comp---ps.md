---
title: setp_comp-ps
description: 設定述詞註冊。 |setp_comp-ps
ms.assetid: a9acb685-f9aa-41f1-8ef1-6d104cb76a09
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a68da290ecb04e9cb7ae49c5525997fbf4c112a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196066"
---
# <a name="setp_comp---ps"></a>setp \_ comp-ps

設定述詞註冊。

## <a name="syntax"></a>Syntax



| setp \_ comp dst、src0、src1 |
|----------------------------|



 

其中：

-   \_comp 是兩個來源暫存器之間的每個通道比較。 可以是下列其中一項： 

    | Syntax | 比較            |
    |--------|-----------------------|
    | \_燃氣輪機   | 大於          |
    | \_淺色   | 小於             |
    | \_通用 電氣   | 大於或等於 |
    | \_樂   | 小於或等於    |
    | \_情 商   | 等於              |
    | \_ne   | 不等於          |

    

     

-   dst 是述詞 [登錄 register，](dx9-graphics-reference-asm-ps-registers-predicate.md) p0。
-   src0 是來源註冊。
-   src1 是來源註冊。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| setp \_ 複合            |      |      |      |      |      | x    | x     | x    | x     |



 

此指示的運作方式如下：


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



針對可根據目的地寫入遮罩寫入的每個通道，請在 src0 與 src1 的對應通道之間儲存比較作業的布林結果，) 之後 (的來源修飾詞 swizzles 已解決。

來源暫存器允許指定任意元件 swizzles。

目的地登錄允許任意的寫入遮罩。

Dst 註冊必須是述詞註冊。

## <a name="applying-the-predicate-register"></a>套用述詞註冊

當述詞登錄使用 setp comp 初始化之後 \_ ，就可以用它來控制每個元件的指令。 語法如下：


```
([!]p0[.swizzle]) instruction dest, src0, ...
```



其中：

-   \[!\] 是選擇性的布林值
-   p0 是述詞註冊
-   \[swizzle \] 是選擇性的 swizzle，可套用至述詞登錄的內容，再使用它來遮罩指令。 可用的 swizzles 為：. xyzw (預設值，但未指定) 或任何複寫 swizzle：. x/. y/g、. z/. b 或. a/w。
-   指令為任何 aritmetic 或材質指令。 這不可以是靜態或動態的流程式控制制指令。
-   dest、src0、.。。是指令所需的暫存器

假設述詞登錄已設定為 (true、true、false、false) 元件值，則可以套用至這個指令：


```
(p0) add r1, r2, r3
```



若要執行2個元件，請新增。


```
r1.x = r2.x + r3.x
r1.y = r2.y + r3.y
```



系統將不會寫入 r1 的 z 和 w 元件，因為述詞註冊在元件 z 和 w 中包含 false。

將述詞暫存器套用至算術或材質指令會將其指示位置計數增加1。

[如果 pred-ps](if-pred---ps.md)、 [callnz pred-ps](callnz-pred---ps.md)和[breakp ps](break-p---ps.md)指示，也可以將述詞登錄套用至。 使用述詞註冊時，這些流程式控制制指示不會增加指令位置計數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




