---
title: 若為 pred-ps
description: If bool-ps 的開頭 .。。其他-ps .。。endif-ps 區塊，其中的條件取自述詞登錄的內容。
ms.assetid: 7b43bf71-a2e9-468f-805f-620de065db08
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ead7c5936550715d48ee1ef6a3938b6219558823
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679116"
---
# <a name="if-pred---ps"></a>若為 pred-ps

[If bool-ps](if-bool---ps.md)的開頭 .。。[其他-ps](else---ps.md).。。[endif-ps](endif---ps.md)區塊，其中的條件取自述詞登錄的內容。

## <a name="syntax"></a>Syntax



| 如果 \[ ！ \]pred. replicateSwizzle |
|-------------------------------|



 

其中：

-   \[!\] 這是選擇性的 NOT 修飾詞。 這會修改述詞註冊中的值。
-   pred 是述詞 [註冊](dx9-graphics-reference-asm-ps-registers-predicate.md)。
-   replicateSwizzle 是將 (或複寫) 複製到所有四個元件 (swizzled) 的單一元件。 有效的元件為： \[ x、y、z、w \] 或 \[ r、g、b、a \] 。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| 如果 \_ pred              |      |      |      |      |      | x    | x     | x    | x     |



 

此指令是用來根據述詞登錄的通道，略過程式碼區塊。 每個 if \_ pred 區塊都必須以 [else-ps](else---ps.md) 或 [endif-ps](endif---ps.md) 指令結尾。

限制包含：

如果 \_ pred 區塊可以進行嵌套，則為。 這會計算為動態嵌套深度的總計，以及 [if \_ 複合](if-comp---ps.md) 區塊。

如果 \_ pred 區塊無法跨迴圈區塊，則應該完全在其中，或將它括住。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




