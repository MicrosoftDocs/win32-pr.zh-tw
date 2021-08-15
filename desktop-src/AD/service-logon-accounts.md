---
title: 服務登入帳戶
description: 服務就像任何程式一樣，有一個主要的安全性身分識別，可決定授與本機和網路資源的存取權和許可權。
ms.assetid: c2345967-8415-4cc0-96d3-12c48e74028e
ms.tgt_platform: multiple
keywords:
- Active Directory，使用服務登入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f197432dec2cdddc7841d2615b3ac2d62c0e4c7388198b7a95e37db7523ae1d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183535"
---
# <a name="service-logon-accounts"></a>服務登入帳戶

服務就像任何程式一樣，有一個主要的安全性身分識別，可決定授與本機和網路資源的存取權和許可權。 此安全性身分識別或安全性內容，也會決定服務對於本機和網路資源的損害有何潛力。

Microsoft Win32 服務的安全性內容是由用來啟動服務的登入帳戶所決定。 本節討論與 Win32 服務所使用的服務登入帳戶相關的程式設計問題和最佳作法，並著重在啟用目錄的服務。 本節包含下列主題：

-   [關於服務登入帳戶](about-service-logon-accounts.md)-Win32 服務的服務登入帳戶和安全性內容程式設計問題的總覽。
-   [針對 Win32 服務選取服務登入帳戶的指導方針](guidelines-for-selecting-a-service-logon-account.md) 。
-   [設定服務的使用者帳戶](setting-up-a-serviceampaposs-user-account.md)。
-   [在主機電腦上安裝服務](installing-a-service-on-a-host-computer.md) ，並指定服務登入帳戶。
-   將[主機電腦上的 [以服務方式登](granting-logon-as-service-right-on-the-host-computer.md)入] 許可權授與給服務的使用者帳戶，這是主機電腦上的 [以服務方式登入] 許可權。
-   [測試是否正在網域控制站上執行](testing-whether-running-on-a-domain-controller.md)-在安裝時偵測是否正在安裝網域控制站上的服務實例。
-   將[存取權限授與服務登入帳戶](granting-access-rights-to-the-service-logon-account.md)—設定和維護 ace 和群組成員資格，以確保系統會將所需的本機和網路資源存取權授與執行中的服務。
-   [變更服務使用者帳戶的密碼](changing-the-password-on-a-serviceampaposs-user-account.md)（在服務的使用者帳戶上變更密碼），同時在安裝服務的每部主機伺服器上更新向服務控制管理員註冊的密碼。
-   [使用 Kerberos 進行相互驗證](mutual-authentication-using-kerberos.md)，在與服務的每個實例的登入帳戶相關聯的目錄物件上維護服務主體名稱 (SPN) 註冊。 Spn 可讓用戶端使用 Kerberos 相互驗證來驗證服務。
-   [轉換網域帳戶名稱格式](converting-domain-account-name-formats.md)—例如，將辨別名稱轉換成 * Domain * **\\** _UserName_ 格式，反之亦然。

 

 




