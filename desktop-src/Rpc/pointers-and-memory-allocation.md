---
title: 指標和記憶體配置
description: 透過指標來變更記憶體的能力通常需要伺服器和用戶端為數組中的元素配置足夠的記憶體。
ms.assetid: 8a49582a-9ae4-4f26-a172-bc8fe2aab65a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d634b209c1f6369429c432d5fad5d4e64b47aeae16778efd8916c00e65911e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927358"
---
# <a name="pointers-and-memory-allocation"></a>指標和記憶體配置

透過指標來變更記憶體的能力通常需要伺服器和用戶端為數組中的元素配置足夠的記憶體。

當存根必須配置或釋放記憶體時，它會呼叫執行時間程式庫函式，進而呼叫 [**midl \_ 使用者 \_ 配置**](/windows/desktop/Midl/midl-user-allocate-1) 和 [**midl \_ 使用者 \_ 免費**](/windows/desktop/Midl/midl-user-free-1)的函式。 這些函數未包含在執行時間程式庫中。 您必須撰寫這些函式的版本，並將它們與您的應用程式連結。 如此一來，您就可以決定如何管理記憶體。 在憑證相容性 (**/osf**) 模式中編譯 IDL 檔案時，您不需要執行這些函數。 您必須將這些函式寫入下列原型：

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
```

例如，應用程式的這些函式版本可以直接呼叫標準程式庫函式：


```C++
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)
{
    return(malloc(len));
}

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 