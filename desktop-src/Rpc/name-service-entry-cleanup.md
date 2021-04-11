---
title: 名稱服務專案清除
description: 名稱服務專案應該包含不常變更的資訊。
ms.assetid: b581bc10-e537-4714-b89a-d998fec23360
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf0ed6a21074a49a472d7505dcfea37cf182026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021781"
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

 

 




