---
title: 如果 pred-vs
description: If pred 的開頭-vs .。。else-vs .。。endif-vs block，其條件取自述詞登錄的內容。
ms.assetid: 03f60ca3-cda0-4653-8582-74d1a75e0aee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a1a36bb0c6c68f5132757719bbc7e37fbc71501
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313635"
---
# <a name="if-pred---vs"></a>如果 pred-vs

If pred 的開頭-vs .。。[else-vs](else---vs.md).。。[endif-vs](endif---vs.md) block，其條件取自述詞登錄的內容。

## <a name="syntax"></a>Syntax



| 如果 \[ ！ \]pred. replicateSwizzle |
|-------------------------------|



 

其中：

-   \[!\] 選擇性的 NOT 修飾詞。 這會修改述詞註冊中的值。
-   pred 是述詞 register，p0。 請參閱述詞 [註冊](dx9-graphics-reference-asm-vs-registers-predicate.md)。
-   replicateSwizzle 是將 (或複寫) 複製到所有四個元件 (swizzled) 的單一元件。 有效的元件為： x、y、z、w 或 r、g、b、a。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| 如果 pred                |      |      | x    | x     | x    | x     |



 

此指令是用來根據述詞登錄的通道，略過程式碼區塊。 每個 if \_ pred 區塊都必須以 else 或 endif 指令結尾。

限制包含：

如果 \_ pred 區塊可以進行嵌套，則為。 這會計算為動態嵌套深度的總計，以及 [if \_ 複合](if-comp---vs.md) 區塊。

如果 \_ pred 區塊無法跨迴圈區塊，則應該完全在其中，或將它括住。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




