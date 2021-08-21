---
title: 使用 SCP Windows 通訊端服務中的相互驗證
description: 本節中的主題包含程式碼範例，示範如何使用服務連接點（ (SCP) ）來對服務進行相互驗證。
ms.assetid: f730464c-95ac-4285-960c-18862f6f7852
ms.tgt_platform: multiple
keywords:
- 使用 SCP AD Windows 通訊端服務中的相互驗證
- Active Directory、使用、相互驗證、Windows sockets 服務和 SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8f3e65b044198c5ebf703b1c62ac03eb07a4d57b6bc5dcf7c5463247815f1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025766"
---
# <a name="mutual-authentication-in-a-windows-sockets-service-with-scp"></a>使用 SCP Windows 通訊端服務中的相互驗證

本節中的主題包含程式碼範例，示範如何使用服務連接點（ (SCP) ）來對服務進行相互驗證。 這些範例是以 Microsoft Windows 通訊端服務為基礎，此服務會使用 SSPI 套件來處理用戶端與服務之間的相互驗證協調。 使用下列程式，在此案例中執行相互驗證。

**若要在安裝服務時于目錄中註冊 Spn**

1.  呼叫 [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) 函式，為服務)  (spn 撰寫服務主體名稱。
2.  呼叫 [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) 函式，在服務將在其內容中執行的服務帳戶或電腦帳戶上註冊 spn。 此步驟必須由網域系統管理員執行;例外狀況是，在 LocalSystem 帳戶下執行的服務可以在 <service class> / <host> 服務主機的電腦帳戶上，以 "" 形式註冊其 SPN。

**確認服務啟動時的設定**

-   確認已在執行服務的帳戶上註冊適當的 Spn。 如需詳細資訊，請參閱 [登入帳戶維護](logon-account-maintenance-tasks.md)工作。

**在用戶端啟動時驗證服務**

1.  從服務的服務連接點取出連接資料。
2.  建立與服務的連接。
3.  呼叫 [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) 函數，以撰寫服務的 SPN。 撰寫來自已知服務類別字串的 SPN，以及從服務連接點取出的資料。 這項資料包含執行服務之伺服器的主機名稱。 請注意，主機名稱必須是 DNS 名稱。
4.  使用 SSPI 安全性套件來執行驗證：
    1.  呼叫 [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) 函數，以取得用戶端的認證。
    2.  將用戶端認證和 SPN 傳遞至 [**InitializeSecurityCoNtext**](../SecAuthN/initializesecuritycontext--general.md) 函式，以產生要傳送至服務的安全性 blob 進行驗證。 將 [ **ISC \_ 要求 \_ 相互 \_** 驗證] 旗標設定為要求相互驗證。
    3.  使用服務 Exchange blob，直到驗證完成為止。
5.  確認「適用于 **ISC 要求 \_ \_ 相互 \_** 驗證」旗標的傳回功能遮罩，以確認已執行相互驗證。
6.  如果驗證成功，請與已驗證的服務交換流量。 使用數位簽章來確保用戶端與服務之間的訊息不會遭到篡改。 除非效能需求很嚴重，否則請使用加密。 如需詳細資訊和示範如何在 SSPI 封裝中使用 [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature)、 [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature)、 [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)和 [**DecryptMessage**](../SecAuthN/decryptmessage--general.md)函式的程式碼範例，請參閱 [確保訊息 Exchange 期間的通訊完整性](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange)。

**當用戶端連線時，由服務驗證用戶端**

1.  載入支援相互驗證的 SSPI 安全性封裝。
2.  當用戶端連接時，請使用安全性套件來執行驗證：
    1.  呼叫 [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) 函數來取得服務認證。
    2.  將從用戶端接收的服務認證和安全性 blob 傳遞至 [**AcceptSecurityCoNtext**](../SecAuthN/acceptsecuritycontext--general.md) 函式，以產生要傳送回用戶端的安全性 blob。
    3.  使用用戶端 Exchange blob，直到驗證完成為止。
3.  檢查「 **ASC \_ RET \_ 相互 \_ 驗證** 」旗標的傳回功能遮罩，確認是否已執行相互驗證。
4.  如果驗證成功，請與已驗證的用戶端交換流量。 除非發生效能問題，否則請使用數位簽章和加密。

如需此相互驗證案例的詳細資訊和程式碼範例，請參閱：

-   [用戶端如何驗證以 SCP 為基礎的 Windows 通訊端服務](how-a-client-authenticates-an-scp-based-windows-sockets-service.md)
-   [針對 SCP 型 Windows 通訊端服務撰寫和註冊 spn](composing-and-registering-spns-for-an-scp-based-windows-sockets-service.md)
-   [Windows 通訊端服務如何驗證用戶端](how-a-windows-sockets-service-authenticates-a-client.md)

如需詳細資訊，請參閱

-   [使用服務連接點發佈](publishing-with-service-connection-points.md)
-   [SSPI 檔](/windows/desktop/SecAuthN/sspi)
-   [Windows通訊端檔](/windows/desktop/WinSock/windows-sockets-start-page-2)

 

 