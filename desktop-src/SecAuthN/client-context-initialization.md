---
description: 用戶端內容初始化
ms.assetid: 0c8aad3e-e726-49ce-8fc9-94dbd60cc5cb
title: 用戶端內容初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 615ce5c157371f1ebfec685d6227bd11a1d76531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114948"
---
# <a name="client-context-initialization"></a>用戶端內容初始化

為了建立安全連線，用戶端會先 [*取得輸出認證*](/windows/desktop/SecGloss/c-gly) 控制碼，然後再將驗證要求傳送至伺服器。 伺服器會從驗證要求建立用戶端的安全性內容。 有兩個與驗證設定相關的用戶端 SSPI 函數：

-   [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) 會取得先前取得之登入 [*認證*](/windows/desktop/SecGloss/c-gly)的參考。
-   [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 會建立初始驗證要求安全性權杖。

您可以在 [使用 SSPI 搭配 Windows 通訊端用戶端](using-sspi-with-a-windows-sockets-client.md)的 **GenClientCoNtext** 函式中，看到此進程的程式碼。

如果用戶端程式除了本身的登入認證（例如不同的使用者名稱、功能變數名稱和密碼）之外，還需要使用認證，它會在 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)呼叫中提供它們，並指定額外 [**的認證。 \_ \_ \_**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) 如需認證功能的詳細資訊，請參閱 [認證管理](authentication-functions.md)。

> [!Note]  
>  [**\_ \_ \_**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) \_ \_ \_ \_ 當結構中的字串是 ASCI 或 OEM 時，每秒的 winnt 驗證身分識別結構的旗標成員都可以設定為 sec 的 winnt auth identity ANSI。 如果使用 MultiByteToWideChar 函式將 ANSI 字串第一次轉換成 unicode，則 ANSI 字串可以與 **sec \_ winnt \_ auth \_ identity** 結構的 Flags 成員一起使用 \_ \_ \_ \_ 。 [](/windows/desktop/SecGloss/u-gly) [](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)

 

為了起始驗證的第一個階段，用戶端會呼叫 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 來取得要在連線要求訊息中傳送至伺服器的初始安全性權杖。

用戶端會使用輸出緩衝區描述項中收到的安全性權杖資訊來產生要傳送至伺服器的訊息。 訊息的結構（就不同的緩衝區的放置等而言）是 [*應用程式協定*](/windows/desktop/SecGloss/a-gly) 的一部分，而且必須由雙方理解。

用戶端會從 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 檢查傳回狀態，以查看驗證是否會在單一呼叫中完成。 當我繼續需要秒的傳回狀態 \_ 時 \_ \_ ，表示安全性通訊協定需要多個驗證訊息。 如需內容函數的詳細資訊，請參閱 [內容管理](authentication-functions.md)。

 

 
