---
title: Named_type_free_inst 函式
description: Stub 會呼叫指名 \_ 型別 \_ free inst 函式來釋 \_ 出與傳輸類型相關聯的記憶體。
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d3b5103572eb58e4311c65b0e1cff02e91f66f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672260"
---
# <a name="the-named_type_free_inst-function"></a>指名 \_ 型別 \_ free \_ inst 函式

Stub 會呼叫 **指名 \_ 型別 \_ free \_ inst** 函式來釋出與傳輸類型相關聯的記憶體。 函式定義如下：

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

參數指向已傳送型別的實例。 此物件不應該釋放。 如需有關何時呼叫函數的討論，請參閱 [代表 \_ as 屬性](the-represent-as-attribute.md)。

 

 




