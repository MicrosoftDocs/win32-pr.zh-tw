---
title: 使用網域使用者帳戶做為服務登入帳戶
description: 網域使用者帳戶可讓服務充分利用 Windows 和 Microsoft Active Directory Domain Services 的服務安全性功能。
ms.assetid: 03c486fd-faec-450c-9348-314680eb73cb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: 7c61816fa140a6126d020285d80a71fb59cc1808ae6888f12dc0e4340447060e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192246"
---
# <a name="using-a-domain-user-account-as-a-service-logon-account"></a>使用網域使用者帳戶做為服務登入帳戶

網域使用者帳戶可讓服務充分利用 Windows 和 Microsoft Active Directory Domain Services 的服務安全性功能。 服務具有授與帳戶的任何本機和網路存取權，或帳戶為其成員的任何群組。 服務可以支援 Kerberos 相互驗證。

> [!Note]  
> 下列檔適用于開發人員。 如果您是使用者尋找有關網域使用者帳戶之錯誤訊息的資訊，請參閱 [Microsoft 社區論壇](https://answers.microsoft.com)。 如需管理網域使用者帳戶的相關資訊，請參閱 [TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754217(v=ws.11))。

使用網域使用者帳戶的優點是，服務的動作受限於與帳戶相關聯的存取權限和許可權。 不同于 `LocalSystem` 服務，使用者帳戶服務中的 bug 無法損毀系統。 如果服務受到安全性攻擊的危害，則損毀會與系統允許使用者帳戶執行的作業隔離。 同時，在不同許可權層級上執行的用戶端可以連接到服務，這可讓服務模擬用戶端來執行敏感性作業。

服務的使用者帳戶不能是任何屬於本機、網域或企業之系統管理員群組的成員。 如果您的服務需要本機系統管理許可權，請在帳戶下執行它 `LocalSystem` 。 對於需要網域系統管理許可權的作業，請模擬用戶端應用程式的安全性內容來執行這些作業。

使用網域使用者帳戶的服務實例需要定期系統管理動作來維護帳戶密碼。 服務實例的主機電腦上的服務控制管理員 (SCM) 快取帳戶密碼，以便用於服務的記錄。 當您變更帳戶密碼時，也必須更新安裝服務之主機電腦上的快取密碼。 如需詳細資訊和程式碼範例，請參閱 [變更服務使用者帳戶的密碼](changing-the-password-on-a-serviceampaposs-user-account.md)。 您可以將密碼保持不變，以避免定期維護，但是這樣會增加對服務帳戶進行密碼攻擊的可能性。 請注意，即使 SCM 將密碼儲存在登錄的安全部分中，還是可能受到攻擊。

網域使用者帳戶有兩種名稱格式：目錄中使用者物件的辨別名稱，以及 <domain> \\ <username> 本機服務控制管理員所使用的 "" 格式。 如需詳細資訊和從某種格式轉換成另一種格式的程式碼範例，請參閱 [轉換網域帳戶名稱格式](converting-domain-account-name-formats.md)。

 

 
