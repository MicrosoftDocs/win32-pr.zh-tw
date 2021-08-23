---
title: if bool-vs
description: 啟動 if .。。還。。。endif-vs block。
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b113c806342d786d258713128bc2cadcbb000235c2639f49e5b57ce3fa3bd2e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986528"
---
# <a name="if-bool---vs"></a>if bool-vs

啟動 if .。。[其他](else---vs.md).。。[endif-vs](endif---vs.md) block。

## <a name="syntax"></a>Syntax



| if bool |
|---------|



 

其中 bool 是 bool 暫存器號碼。 請參閱 [常數布林值](dx9-graphics-reference-asm-vs-registers-constant-boolean.md)暫存器。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| if bool                |      | x    | x    | x     | x    | x     |



 

如果 if 語句中的來源布林值暫存器為 true，則會執行 if 語句所括住的程式碼和相符的 else。 否則，程式碼會以 [其他](else---vs.md).。。[endif-執行 vs](endif---vs.md) 語句。 此指令會使用一個指令位置。

如果區塊可以進行嵌套。

If 區塊無法跨迴圈區塊。

## <a name="example"></a>範例

此指令提供條件式靜態流程式控制制。


```
defb b2, TRUE

...

if b2
// Instructions to run if b2 is nonzero

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[else-vs](else---vs.md)
</dt> <dt>

[endif-vs](endif---vs.md)
</dt> </dl>

 

 




