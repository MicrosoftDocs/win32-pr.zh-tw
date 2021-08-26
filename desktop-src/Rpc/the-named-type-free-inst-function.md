---
title: Named_type_free_inst 函式
description: Stub 會呼叫指名 \_ 型別 \_ free inst 函式來釋 \_ 出與傳輸類型相關聯的記憶體。
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa55e896b89fccc513795a62634e805c2ad6e21b7bdecdd99a0b9cfe2d71cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016887"
---
# <a name="the-named_type_free_inst-function"></a>指名 \_ 型別 \_ free \_ inst 函式

Stub 會呼叫 **指名 \_ 型別 \_ free \_ inst** 函式來釋出與傳輸類型相關聯的記憶體。 函式定義如下：

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

參數指向已傳送型別的實例。 此物件不應該釋放。 如需有關何時呼叫函數的討論，請參閱 [代表 \_ as 屬性](the-represent-as-attribute.md)。

 

 




