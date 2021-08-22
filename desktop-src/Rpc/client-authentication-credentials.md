---
title: 用戶端驗證認證
description: 每個已驗證的用戶端都必須提供驗證認證給伺服器。
ms.assetid: d567e944-8d68-4d95-be6a-840e30f57ba9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2410b073886ffd70409cd749ea90305faa8d4635754e8f9596547c47bb976800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932184"
---
# <a name="client-authentication-credentials"></a>用戶端驗證認證

每個已驗證的用戶端都必須提供驗證認證給伺服器。 在 RPC 下，用戶端會將其驗證認證儲存在用戶端與伺服器之間的系結中。 若要這樣做，用戶端會呼叫 [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) 或 [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)。

有兩種類型的認證，隱含和明確：

-   當用戶端提供使用者名稱、密碼和網域時，會有明確的認證。
-   當用戶端使用來自呼叫 **RpcBindingSetAuthInfo** 或 **RpcBindingSetAuthInfoEx** 函式之執行緒或進程權杖的認證時，就會有隱含的認證。

用戶端應該避免提供明確的認證，因為如果使用了明確的認證，儲存、操作及取出使用者密碼可能會導致分散式系統產生安全性弱點。

若要使用隱含認證，用戶端會呼叫 **RpcBindingSetAuthInfo** (*例如*) 。 安全性系統和 RPC 會從執行緒或進程權杖取得認證，以便用於驗證會話中。

如果用戶端使用明確的認證，則這兩個函式的第五個參數屬於 [**RPC \_ AUTH 身分 \_ 識別 \_ 控制碼**](rpc-auth-identity-handle.md)類型。 這是一種彈性類型，也就是資料結構的指標。 資料結構的內容可以與每個驗證服務不同。 目前，RPC 支援的 Ssp 要求您的應用程式將 **rpc \_ 驗證身分 \_ 識別 \_ 控制碼** 設定為指向 [**SEC 的 \_ WINNT \_ AUTH \_ identity**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) 結構。 **每秒的 \_ WINNT 驗證身分 \_ \_ 識別** 結構包含使用者名稱、網域和密碼的欄位。

 

 




