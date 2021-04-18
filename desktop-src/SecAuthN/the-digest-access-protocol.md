---
description: 摘要存取通訊協定
ms.assetid: 7b2fd75e-dd0d-4a63-a84b-a64f08f883f2
title: 摘要存取通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86aa8f05580c27c866c0568dbc67c4d5ba5c2016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550463"
---
# <a name="the-digest-access-protocol"></a>摘要存取通訊協定

[RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)所指定的摘要存取通訊協定是由 Microsoft Digest 的 [*安全性支援提供者*](../secgloss/s-gly.md) (SSP) 所執行。 這項功能是由一組 [Microsoft 安全性支援提供者介面](sspi.md) 所組成， (SSPI) 用戶端/伺服器應用程式呼叫的安全性內容功能：

-   建立訊息交換的 [*安全性內容*](../secgloss/s-gly.md) 。
-   取得摘要 SSP 所需的資料物件，例如 [*認證*](../secgloss/c-gly.md) 和內容控制碼。
-   存取訊息 [*完整性*](../secgloss/i-gly.md) 和機密性機制。

摘要式存取驗證會在配對的要求/回應交易內進行，要求是源自用戶端，以及源自伺服器的回應。 成功的摘要式存取驗證需要兩個要求/回應配對。

當摘要 SSP 用於 HTTP 驗證時，不會在第一個和第二個要求/回應配對之間維護連接。 換句話說，伺服器不會在傳送第一個回應之後等候第二個要求。

下圖顯示用戶端和伺服器在 HTTP 路徑上執行的步驟，以使用摘要 SSP 完成驗證。 SASL 機制會使用相互驗證，因此驗證資料會傳回用戶端的最後 ASC 伺服器呼叫，以確認用戶端與正確的伺服器通訊。

![摘要存取通訊協定](images/digest1.png)

此程式會從用戶端開始，並傳送 HTTP 要求1以從伺服器要求受存取保護的資源。

伺服器會接收 HTTP 要求1，並判斷資源需要未包含在要求中的驗證資訊。 伺服器會產生用戶端的挑戰，如下所示：

1.  伺服器會藉由呼叫 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)函數來取得其 [*認證*](../secgloss/c-gly.md)。
2.  伺服器會藉由呼叫 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函數來產生摘要挑戰。
3.  伺服器會將 WWW-Authenticate 標頭傳送給用戶端要求的回應， (顯示為 HTTP 回應 1) 。 標頭包含摘要挑戰和不透明的指示詞，其中包含針對用戶端所建立之部分 [*安全性內容*](../secgloss/s-gly.md) 的參考。 標頭會以401狀態碼傳送，指出用戶端要求產生了未授權的存取錯誤。 如需有關摘要挑戰的詳細資訊，請參閱 [摘要挑戰的內容](contents-of-a-digest-challenge.md) ，並 [產生摘要挑戰](generating-the-digest-challenge.md)。
4.  用戶端會接收 HTTP 回應1、將伺服器所傳送的摘要挑戰解壓縮，並產生摘要挑戰回應，如下所示：
    1.  藉由呼叫 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) 函數或以互動方式提示使用者提供認證，即可取得使用者的認證。
    2.  挑戰和認證資訊會傳遞給 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函數，這會產生摘要挑戰回應。
5.  用戶端會將包含挑戰回應的授權標頭傳送至伺服器， (顯示為 HTTP 要求 2) 。 如需有關摘要挑戰回應的詳細資訊，請參閱 [摘要挑戰回應的內容](contents-of-a-digest-challenge-response.md) ，以及 [產生摘要挑戰回應](generating-the-digest-challenge-response.md)。
6.  伺服器會接收 HTTP 要求2、將用戶端所傳送的挑戰回應解壓縮，然後藉由呼叫 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函數來驗證資訊。 如需有關驗證程式的詳細資訊，請參閱 [使用 Microsoft Digest 的初始驗證](initial-authentication-using-microsoft-digest.md)。
7.  伺服器會將 HTTP 回應2傳送回用戶端，作為摘要存取通訊協定所需的第二個和最後一個回應。 如果驗證成功，則此回應包含要求的資源。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[摘要挑戰回應的內容](contents-of-a-digest-challenge-response.md)
</dt> </dl>

 

 
