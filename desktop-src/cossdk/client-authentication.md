---
description: 驗證是判斷呼叫者實際上是&郵件的程式 \# ; 驗證身分識別宣告的真實性。
ms.assetid: c1b11f58-5bab-45d9-a686-86c95415990e
title: 用戶端驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd24edf341fc2033807587b01fd37420d781d5f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936374"
---
# <a name="client-authentication"></a>用戶端驗證

驗證是一種判斷呼叫者實際上是他們聲稱的程式，也就是驗證身分識別宣告的真實性。 一般而言，這可以由伺服器和用戶端來完成，每個都驗證另一個。 但是針對授權用戶端的伺服器應用程式（如同以角色為基礎的安全性）也是很重要的，也就是進行驗證。 驗證用戶端是有意義的授權原則的先決條件。 您可以進行所有您想要的角色檢查，但如果您不知道您正在檢查的用戶端身分識別是否為真，則您的應用程式基本上會依賴「接受」系統。

針對 COM + 應用程式，您可以開啟並設定系統管理的驗證，之後就能以透明的方式在應用程式中運作。 您可以使用 [元件服務] 系統管理工具或系統管理功能，以管理的方式指定驗證層級。 如需設定驗證的詳細資訊，請參閱 [設定伺服器應用程式的驗證層級](setting-an-authentication-level-for-a-server-application.md) 及 [啟用程式庫應用程式的驗證](enabling-authentication-for-a-library-application.md)層級。

根據應用程式的類型是伺服器或程式庫應用程式，設定驗證表示不同的專案。

## <a name="setting-authentication-for-com-server-applications"></a>設定 COM + 伺服器應用程式的驗證

若是 COM + 伺服器應用程式，您可以設定驗證層級，以決定當用戶端呼叫應用程式內的元件時，將如何執行驗證。 您可以從數種驗證層級中選擇，以提供不同程度的安全性，範圍從無驗證到每個封包的加密，以及所有方法呼叫參數。 如需詳細資訊，請參閱 [設定伺服器應用程式的驗證層級](setting-an-authentication-level-for-a-server-application.md)。

更高的安全性會有一些效能成本，但在設定應用程式時，您應該考慮這一點。 COM + 會在用戶端和伺服器所指定的驗證層級之間進行協調。 這項協商的執行方式有一個優點，就是讓您能夠從伺服器端自行進行系統管理控制驗證。 如需詳細資訊，請參閱 [驗證層級的協商](negotiation-of-authentication-level.md)。

> [!Note]  
> 您絕對不應該使用 COM + 應用程式中的 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ，以程式設計方式指定驗證層級。 COM + 會為您呼叫 **CoInitializeSecurity** ，而且每個進程只能呼叫一次。

 

基礎驗證服務是由 COM 和 Microsoft Windows 提供。 在驗證服務中，協力廠商為使用者提供憑證，證明到使用者身分識別的真實性。 這項認證與憑證授權單位單位一樣可靠，而且與驅動程式的授權或 passport 一樣，也可以作為認證檔，其相依于簽發者的授權單位。 如需有關驗證服務的詳細資訊，請參閱 COM 檔中的 [com 和安全性封裝](/windows/desktop/com/com-and-security-packages) 。

## <a name="setting-authentication-for-com-library-applications"></a>設定 COM + 程式庫應用程式的驗證

針對 COM + 程式庫應用程式，您可以啟用或停用驗證，以判斷應用程式是否會受限於裝載進程所執行的驗證。 雖然 COM + 程式庫應用程式的驗證大多是由裝載進程所控制，但您可以設定程式庫應用程式，使其不會參與驗證。 也就是說，對應用程式的呼叫可以驗證或未經驗證，在後者的情況下，用戶端的「驗證」一律會成功。 如需詳細資訊，請參閱 [啟用程式庫應用程式的驗證](enabling-authentication-for-a-library-application.md)。

此外，您可能會想要或需要在資料庫或某些下游應用程式上驗證用戶端，而在 COM + 應用程式上單獨驗證用戶端可能還不夠。 如果是這種情況，您必須模擬用戶端，以便將用戶端的身分識別傳播到下游。 如需模擬的詳細資訊，請參閱 [用戶端模擬和委派](client-impersonation-and-delegation.md)。 如需有關決定是否要在資料層進行驗證的問題討論，請參閱 [多層式應用程式安全性](multi-tier-application-security.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[用戶端模擬和委派](client-impersonation-and-delegation.md)
</dt> <dt>

[程式庫應用程式安全性](library-application-security.md)
</dt> <dt>

[多層式應用程式安全性](multi-tier-application-security.md)
</dt> <dt>

[程式設計元件安全性](programmatic-component-security.md)
</dt> <dt>

[以角色為基礎的安全性管理](role-based-security-administration.md)
</dt> <dt>

[在 COM + 中使用軟體限制原則](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
