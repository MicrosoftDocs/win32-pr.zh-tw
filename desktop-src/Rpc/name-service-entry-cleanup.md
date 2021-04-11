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
# <a name="name-service-entry-cleanup"></a><span data-ttu-id="b00fd-103">名稱服務專案清除</span><span class="sxs-lookup"><span data-stu-id="b00fd-103">Name Service Entry Cleanup</span></span>

<span data-ttu-id="b00fd-104">名稱服務專案應該包含不常變更的資訊。</span><span class="sxs-lookup"><span data-stu-id="b00fd-104">A name service entry should contain information that does not change frequently.</span></span> <span data-ttu-id="b00fd-105">基於這個理由，請勿將動態端點包含在匯出的系結控制碼中，因為它們會在每次叫用伺服器時變更，並會讓您的名稱服務專案變得雜亂。</span><span class="sxs-lookup"><span data-stu-id="b00fd-105">For this reason, do not include dynamic endpoints in your exported binding handles because they will change at each invocation of the server and will clutter up your name service entry.</span></span> <span data-ttu-id="b00fd-106">若要移除這些系結控制碼，請使用 [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)。</span><span class="sxs-lookup"><span data-stu-id="b00fd-106">To remove these binding handles, use [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).</span></span>

<span data-ttu-id="b00fd-107">例如，合理的伺服器作業順序如下：</span><span class="sxs-lookup"><span data-stu-id="b00fd-107">For example, a reasonable sequence of server operations would be:</span></span>

<span data-ttu-id="b00fd-108">針對一個以上的傳輸：</span><span class="sxs-lookup"><span data-stu-id="b00fd-108">For more than one transport:</span></span>

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

<span data-ttu-id="b00fd-109">若要在端點對應程式中放置系結：</span><span class="sxs-lookup"><span data-stu-id="b00fd-109">To place bindings in the endpoint mapper:</span></span>

``` syntax
RpcServerInqBindings(&Vector);
RpcEpRegister(Interface, Vector);
```

<span data-ttu-id="b00fd-110">若要從系結移除端點：</span><span class="sxs-lookup"><span data-stu-id="b00fd-110">To remove endpoints from bindings:</span></span>

``` syntax
for (i=0; i < Vector- > Count; + + i)
{
    RpcBindingReset(Vector->BindingH[i];
}
```

<span data-ttu-id="b00fd-111">若要將系結新增至名稱服務：</span><span class="sxs-lookup"><span data-stu-id="b00fd-111">To add bindings to the name service:</span></span>

``` syntax
RpcNsBindingExport(RPC_C_NS_SYNTAX_DEFAULT, EntryName, Interface
                   Vector);
RpcServerListen();
```

 

 




