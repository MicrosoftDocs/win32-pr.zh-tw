---
title: midl_user_allocate 屬性
description: Midl \_ 使用者配置函式 \_ 是用戶端和伺服器應用程式提供來配置記憶體的函式。
ms.assetid: 0eaf6df5-791d-4f6d-8f49-cc1ce64e7ab4
keywords:
- midl_user_allocate 屬性 MIDL
topic_type:
- apiref
api_name:
- midl_user_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16729e0a0a422c8ed2d8a8f323b563cb6a268fcb041e6a9d2ba13a9c9b847d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806656"
---
# <a name="midl_user_allocate-attribute"></a>midl \_ 使用者 \_ 配置屬性

**Midl \_ 使用者 \_ 配置** 函式是用戶端和伺服器應用程式提供來配置記憶體的函式。

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate (size_t cBytes);
```

## <a name="parameters"></a>參數

<dl> <dt>

*cBytes* 
</dt> <dd>

指定要配置的位元組計數。

</dd> </dl>

## <a name="remarks"></a>備註

用戶端應用程式和伺服器應用程式都必須執行 **midl \_ 使用者 \_ 配置** 函式，除非您在憑證相容性 ([**/osf**](-osf.md)) 模式中進行編譯。 應用程式和產生的存根在處理指標所參考的物件時，會呼叫 **midl \_ 使用者 \_ 配置** ：

-   伺服器應用程式應該呼叫 **midl \_ 使用者 \_ 配置** 來配置 applicationâ的記憶體，例如，建立新節點時。
-   當將指向的資料封送處理至伺服器位址空間時，伺服器 stub 會呼叫 **midl \_ 使用者 \_ 配置** 。
-   從 [**out**](out-idl.md)指標所參考的伺服器封送資料時，用戶端 stub 會呼叫 **midl \_ 使用者 \_ 配置**。 請注意，對於 **\[** [**in**](in.md) **\]** 、 **\[ out \]** 和 **\[** [**unique**](unique.md) **\]** 指標而言，只有在輸入上的 **\[ 唯一 \]** 指標值為 **Null** ，且在呼叫期間變更為非 **Null** 值時，用戶端 stub 才會呼叫 **midl \_ 使用者 \_ 配置**。 如果輸入上的 **\[ \] unique** 指標不是 **Null** ，則用戶端 stub 會將相關聯的資料寫入現有的記憶體。

如果 **midl \_ 使用者 \_ 配置** 無法配置記憶體，則必須傳回 **Null** 指標。

建議 **midl \_ 使用者 \_ 配置** 傳回8個位元組對齊的指標。

## <a name="examples"></a>範例


```C++
#include <windows.h>

void __RPC_FAR * __RPC_API midl_user_allocate(size_t cBytes) 
{ 
    return(malloc(cBytes)); 
}
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**分配**](allocate.md)
</dt> <dt>

[**陣 列**](arrays-1.md)
</dt> <dt>

[陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**在**](in.md)
</dt> <dt>

[**midl \_ 使用者 \_ 免費**](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**獨特**](unique.md)
</dt> </dl>

 

 