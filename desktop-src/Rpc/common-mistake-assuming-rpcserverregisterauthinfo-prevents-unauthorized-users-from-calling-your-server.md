---
title: 常見的錯誤假設 RpcServerRegisterAuthInfo 可防止未經授權的使用者呼叫您的伺服器
description: 當安全性提供者在伺服器上使用 RpcServerRegisterAuthInfo 函式註冊時，就會新增一個選項，而不是需求。
ms.assetid: c8db8973-6d47-47b4-b927-72cfb464e9f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a60c800d377dc122de561b87c41a5ec635328
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675092"
---
# <a name="common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server"></a>常見錯誤：假設 RpcServerRegisterAuthInfo 可防止未經授權的使用者呼叫您的伺服器

當安全性提供者在伺服器上使用 [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) 函式註冊時，就會新增一個選項，而不是需求。 這表示不會取代先前的 **RpcServerRegisterAuthInfo** 註冊。 這也表示未經驗證的用戶端仍然可以連接。 藉由呼叫 **RpcServerRegisterAuthInfo** 函式，不允許未經驗證的用戶端進行連接;它們仍然可以連接，但 [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) 和 [**RpcGetAuthorizationCoNtextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) 之類的函式呼叫會失敗。 因此，當呼叫 **RpcServerRegisterAuthInfo** 函式時，潛在的攻擊者也不會被 weeded 出，而應該有存取權的用戶端也有機會證明其身分識別。 檢查仍必須備妥，以判斷是否有潛在攻擊者嘗試連接。

 

 




