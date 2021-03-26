---
title: 來源註冊級別 x 2
description: 將值乘以二，再于指令中使用。
ms.assetid: a02c9572-e03d-410b-8b65-7ea1a0bfaa0f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7e88127e4027767d23a2ab576e94802019068dc3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971453"
---
# <a name="source-register-scale-x-2"></a>來源註冊級別 x 2

將值乘以二，再于指令中使用。

## <a name="syntax"></a>Syntax


```
register_x2
```



## <a name="register"></a>註冊

來源註冊。 如需註冊類型的詳細資訊，請參閱[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)。

## <a name="remarks"></a>備註

註冊的內容不會變更。 修飾詞只會套用至從註冊讀取的資料。

此修飾詞與來源登錄 [反轉](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)互斥，因此無法套用至相同的暫存器。

此修飾詞僅適用于第1版中的算術指令 \_ 。

## <a name="example"></a>範例

此範例會取樣材質、將資料轉換為-1 到 + 1 的範圍，並計算點乘積。


```
mul r0, r0, r1_x2;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器來源登錄修飾詞](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




