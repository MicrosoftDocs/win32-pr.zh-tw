---
title: enable_allocate 屬性
description: '\ Enable \_ allocate \ ACF 屬性指定伺服器 stub 程式碼應啟用存根記憶體管理環境。'
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- enable_allocate 屬性 MIDL
topic_type:
- apiref
api_name:
- enable_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f44b3a2f11094c37edf24f5fc00bbd8229d65dc2a54292acd2ca3221472e85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979618"
---
# <a name="enable_allocate-attribute"></a>啟用 \_ 配置屬性

[ **\[ 啟用 \_ 配置 \]** ACF] 屬性會指定伺服器 stub 程式碼應啟用存根記憶體管理環境。

> [!Note]  
> **\[ 啟用 \_ 配置 \]** 屬性已淘汰，不再支援。

 

``` syntax
[
    enable_allocate
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a>參數

<dl> <dt>

*選用-屬性-清單* 
</dt> <dd>

指定零個或多個其他 MIDL 屬性的清單。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

將套用 **\[ enable \_ allcoate \]** 屬性的介面名稱。

</dd> </dl>

## <a name="remarks"></a>備註

在預設模式下，只有在使用「 **\[ 啟用 \_ 配置 \]** 」屬性時，伺服器 stub 才會啟用記憶體環境。 記憶體管理環境必須先啟用，才能使用 [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate)來配置記憶體。 在 **憑證** 模式中 (當您使用 [**/osf**](-osf.md)參數) 進行編譯時，存根會自動啟用此環境，或在使用 **\[ 啟用 \_ 配置 \]** 屬性時，于要求上啟用。

用戶端 stub 可能會對「 **Rpcss** 記憶體管理」環境很敏感。 如果在停用 **Rpcss** 套件時執行敏感性用戶端存根，則會 (呼叫預設的使用者配置器/解除配置器，例如 [midl \_ 使用者 \_ 配置](/windows/desktop/Rpc/the-midl-user-allocate-function) /  [midl \_ 使用者 \_ free](/windows/desktop/Rpc/the-midl-user-free-function)) 。 啟用時， **Rpcss** 封裝會使用套件中的配置器/釋放器組。 在預設模式下，只有在使用「 **\[ 啟用 \_ 配置 \]** 」屬性時，用戶端才是敏感的。 一般而言，用戶端 stub 會在停用的環境中運作。 在 **憑證** 模式中 (當您使用 [**/osf**](-osf.md)參數) 進行編譯時，用戶端一律會受到 **Rpcss** 記憶體管理環境的影響，因此， **\[ 啟用 \_ 配置 \]** 屬性不會影響用戶端存根。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[midl \_ 使用者 \_ 配置](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[midl \_ 使用者 \_ 免費](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[RpcSmDisableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[RpcSmEnableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[RpcSmFree](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 