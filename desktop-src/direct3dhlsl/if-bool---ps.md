---
title: if bool-ps
description: If 區塊的開頭。
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 611ec04a5c3a53bbb8c6c35380bd0d9f824dc697a7d27a3656b262d885fb4eac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457508"
---
# <a name="if-bool---ps"></a>if bool-ps

If 區塊的開頭。

## <a name="syntax"></a>Syntax



| if bool |
|---------|



 

其中：

-   bool 是布林值 (布林值) register 號碼。 請參閱 [常數布林值](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| if bool               |      |      |      |      |      | x    | x     | x    | x     |



 

如果 if 語句中的來源布林值暫存器為 true，則會執行 if 語句所括住的程式碼和對應的 [endif-ps](endif---ps.md) 或 [else-ps](else---ps.md) 。 否則，程式碼是由 else-ps 所括住 .。。endif-執行的 ps 語句。 此指令會使用一個指令位置。

如果可以嵌套 if 區塊，則為。

If 區塊無法跨迴圈區塊。

If 區塊後面可以接著語句區塊、/或 [其他-ps](else---ps.md) 指令，以及/或 [endif-ps](endif---ps.md) 指令。

## <a name="example"></a>範例

此指令提供條件式靜態流程式控制制。


```
defb b3, true

if b3
// Instructions to run if b3 is nonzero
else
// Instructions to run otherwise
endif
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[其他-ps](else---ps.md)
</dt> <dt>

[endif-ps](endif---ps.md)
</dt> </dl>

 

 




