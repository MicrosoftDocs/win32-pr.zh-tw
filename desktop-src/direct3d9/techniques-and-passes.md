---
description: 技術可提供轉譯肌肉。 技術會封裝決定轉譯樣式的效果狀態。 一項技術是由一或多個階段所組成。
ms.assetid: 0a4d8f44-c7c0-4355-ac7f-6bc3315eeff0
title: " (Direct3D 9) 的技術和傳遞"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3a68ac40db16b3e6819adf6fcd1f8a6f790325
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973557"
---
# <a name="techniques-and-passes-direct3d-9"></a> (Direct3D 9) 的技術和傳遞

技術可提供轉譯肌肉。 技術會封裝決定轉譯樣式的效果狀態。 一項技術是由一或多個階段所組成。

## <a name="techniques"></a>技術

呼叫技術的語法如下所示：


```
technique [ id ]  [< annotation(s) >] 
    { pass(es) }
```



其中：

-   識別碼是選擇性的唯一名稱。
-   批註是零或多個選擇性的使用者特定資訊。 請參閱 [使用 \_ 批註將資訊新增至效果參數](using-an-effect.md)。
-   pass (es) 為零或多個行程。 每個階段都包含狀態指派。 請參閱下文。

## <a name="passes"></a>通過

Pass 包含轉譯所需的狀態指派。


```
pass  [ id ]  [< annotation(s) >] 
    { state assignment(s) }
```



其中：

-   識別碼是選擇性的唯一名稱。
-   批註是一或多個選擇性的使用者特定資訊。 請參閱 [使用 \_ 批註將資訊新增至效果參數](using-an-effect.md)。
-   指派 (s) 指派零個以上的狀態值，或評估一或多個運算式。 請參閱 [ (direct3d 9) ](effect-states.md) 和 [運算式 (direct3d 9) ](expressions.md)的效果狀態。

將一組重複指派中的最後一項指派傳遞給相同的狀態，即會略過全部。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果格式](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



