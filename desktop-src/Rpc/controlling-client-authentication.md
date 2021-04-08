---
title: 控制用戶端驗證
description: 驗證用戶端的最佳方法是使用 RpcServerRegisterIf2 或 RpcServerRegisterIfEx 函式安裝安全性回呼函數;接受安全性回呼函數做為引數。
ms.assetid: 3e858a71-9190-44a3-bc63-08cfbd02d443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3508e99b351cd57fb67a3727710b60562ffe25dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839888"
---
# <a name="controlling-client-authentication"></a>控制用戶端驗證

驗證用戶端的最佳方法是使用 [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) 或 [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) 函式安裝安全性回呼函數;接受安全性回呼函數做為引數。 呼叫安全性回呼函式時，請進行必要的檢查。 您可以檢查連接上的屬性、呼叫端的身分識別，或兩者都有。 若要檢查連接的屬性，請呼叫 [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) 或 [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) 函數。 這可讓您篩選未經過驗證的用戶端、使用特定安全性提供者的用戶端，或未使用強式保護的用戶端 (例如隱私權) 。

若要允許存取已驗證的使用者子集，請使用 [**RpcGetAuthorizationCoNtextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)。 此函數會傳回可用於進行非常複雜之存取檢查的 Authz 用戶端內容。 例如，您可以使用此方法，在正常上班時間內只允許存取組織中的副總裁，以及使用 Active Directory 服務將使用者名稱對應至其標題的任何小時。 使用者可以模擬，並取得其名稱。 知道他們的身分識別之後，就可以進行任何所需的檢查。

 

 




