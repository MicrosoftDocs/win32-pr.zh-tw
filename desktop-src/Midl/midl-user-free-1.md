---
title: midl_user_free 屬性
description: Midl \_ 使用者 free 函式 \_ 是由用戶端和伺服器應用程式提供，以解除配置動態配置的記憶體。
ms.assetid: b5d8f133-ddd9-4b92-8540-611a03835be0
keywords:
- midl_user_free 屬性 MIDL
topic_type:
- apiref
api_name:
- midl_user_free
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53819035f700a948c9ca45c565310d7796516147
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314902"
---
# <a name="midl_user_free-attribute"></a>midl \_ 使用者 \_ 可用屬性

**Midl \_ 使用者 \_ free** 函式是由用戶端和伺服器應用程式提供，以解除配置動態配置的記憶體。

``` syntax
void __RPC_API midl_user_free(void __RPC_FAR * p);
```

## <a name="parameters"></a>參數

<dl> <dt>

*P* 
</dt> <dd>

要釋放之記憶體區塊的指標。

</dd> </dl>

## <a name="remarks"></a>備註

用戶端應用程式和伺服器應用程式都必須執行 **midl \_ 使用者 \_ free** 函式，除非您在憑證相容性 ([**/osf**](-osf.md)) 模式中進行編譯。 **Midl \_ 使用者 \_ free** 函數必須能夠釋出 [**midl \_ 使用者配置所 \_ 配置**](/windows/desktop/Rpc/the-midl-user-allocate-function)的所有儲存體。

處理指標所參考的物件時，應用程式和存根會呼叫 **midl \_ 使用者 \_ free** ：

-   伺服器應用程式應該呼叫 **midl \_ 使用者 \_ free** 來釋出 applicationâ所配置的記憶體，例如，刪除指定的節點時。
-   伺服器 stub 會在封送處理所有 **\_ \_** **\[** [**out**](out-idl.md) **\]** 引數、 **\[** [**in**](in.md)、 **out \]** 引數和傳回值之後，呼叫 midl 使用者 free 釋放伺服器上的記憶體。

## <a name="examples"></a>範例


```C++
#include <windows.h>

void __RPC_API midl_user_free(void __RPC_FAR * p) 
{ 
    free(p); 
}
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**陣 列**](arrays-1.md)
</dt> <dt>

[陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**在**](in.md)
</dt> <dt>

[**midl \_ 使用者 \_ 配置**](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**擴展**](out-idl.md)
</dt> <dt>

[**獨特**](unique.md)
</dt> </dl>

 

 