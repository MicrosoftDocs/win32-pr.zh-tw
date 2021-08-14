---
title: RPC 應用程式中的相互驗證
description: RPC 服務可以使用服務連接點來發佈本身，也可以使用 RPC 名稱服務 (RpcNs) Api。
ms.assetid: 9f575aef-0a4b-4e1b-8ea9-5f40e6c3d9c7
ms.tgt_platform: multiple
keywords:
- RPC 應用程式中的相互驗證 AD
- Active Directory，使用，相互驗證，RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c7d5ea3632d08671861b72267419efd54c1a6a89770fbde72543596b29fa8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186053"
---
# <a name="mutual-authentication-in-rpc-applications"></a>RPC 應用程式中的相互驗證

RPC 服務可以使用服務連接點來發佈本身，也可以使用 RPC 名稱服務 (RpcNs) Api。 本主題討論如何使用 rpc 服務來執行相互驗證，此服務會使用 RPC 名稱服務 (RpcNs) Api 來發佈本身。

**在目錄中註冊 SPN**

1.  呼叫 [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) 函式，為服務 (SPN) 撰寫服務主體名稱。
2.  呼叫 [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) 函式，在服務將在其內容中執行的服務帳戶或電腦帳戶上註冊 SPN。

**向 RPC 命名服務註冊服務**

1.  確認已在執行服務的帳戶上註冊適當的 Spn。 如需詳細資訊，請參閱 [登入帳戶維護](logon-account-maintenance-tasks.md)工作。
2.  呼叫 [**RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) 函式，以使用 rpc 驗證服務來註冊服務 SPN，並指定 **rpc \_ C \_ 驗證 \_ GSS \_ NEGOTIATE** 作為要使用的驗證服務。

如需在 RPC 服務中執行相互驗證的詳細資訊，請參閱 [撰寫經過驗證的 SSPI 伺服器](/windows/desktop/Rpc/writing-an-authenticated-sspi-server)。

**從用戶端驗證服務**

1.  從 RPC 系結中解壓縮主機名稱。
2.  使用服務類別、DNS 主機名稱和服務名稱呼叫 [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) 函式，以撰寫服務的 SPN;這是 RpcNs 案例中連接點的分辨名稱。

    如需撰寫 RpcNs 服務之 SPN 的詳細資訊，請參閱 [撰寫 RpcNs 服務的 spn](composing-spns-for-an-rpcns-service.md)。

3.  設定 [**RPC \_ 安全性 \_ QOS**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) 結構以要求相互驗證。
4.  呼叫 [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) 函數，以設定 RPC 系結的驗證資料。 用戶端至少必須要求 **RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 完整性** ，以確保通訊未遭到篡改。 為了提高安全性，用戶端應該指定 **RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權** 來要求加密。
5.  執行 RPC 呼叫。

如需在 RPC 用戶端中執行相互驗證的詳細資訊，請參閱 [撰寫經過驗證的 SSPI 用戶端](/windows/desktop/Rpc/writing-an-authenticated-sspi-client)。

**從服務驗證用戶端**

1.  呼叫 [**RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) 函數來驗證用戶端所指定的驗證參數。 如果用戶端未要求所需的驗證層級，請拒絕呼叫。 請注意，RPC 服務必須在每次呼叫時驗證驗證等級、驗證服務和用戶端身分識別，以確保用戶端已通過適當的驗證。
2.  呼叫 [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) 函數來模擬用戶端。
3.  執行要求的作業。
4.  呼叫 [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) 函式來還原至服務安全性內容。

如需 RPC 用戶端模擬的詳細資訊，請參閱 [用戶端](/windows/desktop/Rpc/client-impersonation)模擬。

如需詳細資訊，請參閱

-   [使用 RPC 名稱服務發行 (RpcNs) ](publishing-with-the-rpc-name-service-rpcns.md)
-   [RPC 安全性基本知識](/windows/desktop/Rpc/rpc-security-essentials)

 

 