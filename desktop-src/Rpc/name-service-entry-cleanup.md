---
title: 名稱服務專案清除
description: 名稱服務專案應該包含不常變更的資訊。
ms.assetid: b581bc10-e537-4714-b89a-d998fec23360
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfe7484d1c6d557899e3b661a3a616c97d3890becfad51df0e91f5a69467faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019603"
---
# <a name="name-service-entry-cleanup"></a>名稱服務專案清除

名稱服務專案應該包含不常變更的資訊。 基於這個理由，請勿將動態端點包含在匯出的系結控制碼中，因為它們會在每次叫用伺服器時變更，並會讓您的名稱服務專案變得雜亂。 若要移除這些系結控制碼，請使用 [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)。

例如，合理的伺服器作業順序如下：

針對一個以上的傳輸：

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

若要在端點對應程式中放置系結：

``` syntax
RpcServerInqBindings(&Vector);
RpcEpRegister(Interface, Vector);
```

若要從系結移除端點：

``` syntax
for (i=0; i < Vector- > Count; + + i)
{
    RpcBindingReset(Vector->BindingH[i];
}
```

若要將系結新增至名稱服務：

``` syntax
RpcNsBindingExport(RPC_C_NS_SYNTAX_DEFAULT, EntryName, Interface
                   Vector);
RpcServerListen();
```

 

 




