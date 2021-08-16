---
title: 關於服務登入帳戶
description: 以 Win32 為基礎的服務啟動時，會登入本機電腦。
ms.assetid: 637ad0c0-118f-43e8-9d21-a93f6886f546
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ba72ffca4362f42c6a5ad6ee494e36e9698d7883c19e3fe2a157e153ce556b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841018"
---
# <a name="about-service-logon-accounts"></a>關於服務登入帳戶

以 Win32 為基礎的服務啟動時，會登入本機電腦。 可以用下列方式登入：

-   本機或網域使用者帳戶。
-   LocalSystem 帳戶。

登入帳戶會在執行時間決定服務的安全性識別，也就是服務的主要安全性內容。 安全性內容會決定服務存取本機和網路資源的能力。 例如，在本機使用者帳戶的安全性內容中執行的服務無法存取網路資源。 相反地，在 Windows 2000 網域控制站上的 LocalSystem 帳戶的安全性內容中執行的服務 (dc) ，將不受限制地存取 DC。 如需詳細資訊，以及使用者帳戶和 LocalSystem 之間的優點和限制的討論，請參閱 [安全性內容和 Active Directory Domain Services](security-contexts-and-active-directory-domain-services.md)。

最後，安裝服務的系統管理員可以控制服務的登入帳戶。 基於安全性理由，某些系統管理員可能不允許您在 LocalSystem 帳戶下安裝您的服務。 您的服務必須能夠以網域使用者帳戶執行。 如果您是程式設計人員，您可以對服務的登入帳戶執行一些控制權。 您的服務安裝程式會在呼叫 [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) 函式時，指定服務的登入帳戶，以在主機電腦上安裝服務。 您的安裝程式可以建議預設的登入帳戶，但它應該允許系統管理員指定實際的帳戶。

您的安裝程式也可以執行與服務登入帳戶相關的下列工作：

-   安裝。 如果您的服務是在使用者帳戶下執行，則帳戶必須存在，才能呼叫 [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea)。 您可以使用現有的帳戶，或在主機電腦的 installrt 中建立一個帳戶。 如需詳細資訊，請參閱 [設定服務的使用者帳戶](setting-up-a-serviceampaposs-user-account.md)。
-   驗證。 如果您想要讓用戶端使用 Kerberos 相互驗證，請在服務的登入帳戶上註冊 Spn。 如果服務是以 LocalSystem 帳戶執行，服務的登入帳戶就是主機電腦的電腦帳戶。 如需詳細資訊，請參閱[服務主體名稱](service-principal-names.md)。
-   授與存取權。 確定服務在執行時間具有執行其工作所需的存取權和許可權。 這可能需要在各種資源（也就是目錄物件、檔案共用等）的安全描述項中，設定 (Ace) 的存取控制專案，以允許使用者或電腦帳戶的必要存取權限。 如需詳細資訊，請參閱授 [與服務登入帳戶的存取](granting-access-rights-to-the-service-logon-account.md)權。
-   設定許可權。 指派許可權給指定的登入帳戶，例如以服務方式登入主機電腦的許可權。 如需詳細資訊，請參閱 [主機電腦上的授與以服務方式登入許可權](granting-logon-as-service-right-on-the-host-computer.md)。

安裝服務之後，會有與您的服務登入帳戶相關的維護工作。 如需詳細資訊，請參閱 [登入帳戶維護](logon-account-maintenance-tasks.md)工作。

-   密碼維護。 對於在使用者帳戶下執行的服務，您必須定期變更密碼，並將密碼與一或多個本機服務控制管理員用來啟動服務的密碼保持同步。
-   SPN 維護。 如果服務登入帳戶變更，請移除舊帳戶上所註冊的 Spn，並在新帳戶上註冊。 請注意，安裝服務時，網域系統管理員可以變更您的服務執行所使用的帳戶;使用「電腦管理」系統管理工具的 Win32 函數或使用者介面。
-   ACE 維護。 如果服務登入帳戶變更，您需要更新 Ace 和群組成員資格，以確保服務仍然可以存取所需的資源。

 

 