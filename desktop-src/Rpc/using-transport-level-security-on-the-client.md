---
title: 在用戶端上使用 Transport-Level 安全性
description: 用戶端會指定當用戶端建立字串系結時，伺服器模擬用戶端的方式。
ms.assetid: 0d02b7f2-4dcb-41e8-829c-6942dfdcd4c6
keywords:
- 在用戶端上使用傳輸層級安全性的遠端程序呼叫 RPC、工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10360d5b8d11640803e31ee1d1d0490a6edfdf7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933535"
---
# <a name="using-transport-level-security-on-the-client"></a>在用戶端上使用 Transport-Level 安全性

用戶端會指定當用戶端建立字串系結時，伺服器模擬用戶端的方式。 這項 QOS 資訊是在字串系結中以端點選項的形式提供。 用戶端可以指定模擬、動態或靜態追蹤的層級，以及僅限有效的旗標。

**提供伺服器的服務品質資訊**

1.  用戶端會呼叫 [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) ，以在正確的字串系結內容中建立元件字串，包括端點選項。
2.  用戶端會呼叫 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) 來取得新的系結控制碼，並套用用戶端的服務品質資訊。
3.  用戶端會使用控制碼進行遠端程序呼叫。

Microsoft RPC 只支援 [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np) 和 [**ncalrpc**](/windows/desktop/Midl/ncalrpc)上的 Windows 安全性功能。 其他傳輸的安全性選項會被忽略。

用戶端可以將下列安全性參數與具名管道傳輸 [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np) 或 [**ncalrpc**](/windows/desktop/Midl/ncalrpc)的系結產生關聯：

-   識別、模擬或匿名。 指定使用的安全性類型。 預設值是模擬。
-   動態或靜態。 判斷與執行緒相關聯的安全性資訊是否為遠端程序呼叫 (靜態) 時所建立之安全性資訊的複本，或 (動態) 之安全性資訊的指標。

    靜態安全性資訊不會變更。 動態設定會反映目前的安全性設定，包括在進行遠端程序呼叫之後所做的變更。 針對 [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np)，遠端具名管道連線的預設值是靜態的，針對本機具名管道連線，預設為動態。

-   **TRUE** 或 **FALSE**。 指定僅限有效旗標的值。 **TRUE** 值表示在呼叫時，只有在上設定為 on 的權杖許可權有效。 值為 **FALSE** 表示擁有權限都可使用，而且應用程式可以修改它們。

這些設定的任何組合都可以指派給系結，如下列範例所示：

``` syntax
"Security=Identification Dynamic True"
"Security=Anonymous Static True"
"Security=Impersonation Static False"
```

預設安全性參數設定會根據傳輸通訊協定而有所不同。

如需端點選項語法的詳細資訊，請參閱 [端點](/windows/desktop/Midl/endpoint)。

 

 