---
title: ADSI 與 ASP 的驗證問題
description: 根據內部網路的設定，從 ASP 頁面執行 ADSI 程式碼時可能會發生驗證問題。
ms.assetid: 287e2e19-7da9-497b-bf46-595ff4755261
ms.tgt_platform: multiple
keywords:
- ADSI、ASP pages、驗證問題
- ADSI、驗證、ASP 問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423d1aa39006f89ca366423da9d135e00af45693
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683083"
---
# <a name="authentication-issues-for-adsi-with-asp"></a>ADSI 與 ASP 的驗證問題

根據內部網路的設定，從 ASP 頁面執行 ADSI 程式碼時可能會發生驗證問題。

您可以使用委派來指定存取網域控制站的驗證。 委派允許服務以使用者身分運作，因此可以使用該使用者認證來存取網路資源。 如果您的內部網路採用此設定，您必須將 IIS 設定為使用委派。 將 IIS 驗證機制設定為 [匿名] 或 [NTLM]。 如果您選擇 [匿名]，安全性內容將會對應到 [IUSR \_ 電腦帳戶]。 如果您選取 [NTLM]，安全性內容將會變更，視使用者登入您的網站而定。 如需有關設定 IIS 伺服器以進行委派的詳細資訊和指示，請參閱 [Windows 2000 資源套件](https://support.microsoft.com/kb/927229)。

如果您使用的 IIS 伺服器使用 NT 挑戰/回應，或不支援 Kerberos 的瀏覽器用戶端，則不支援雙躍點驗證。 雙躍點驗證表示使用者認證會從瀏覽器用戶端傳遞至 IIS 伺服器，然後 IIS 伺服器會將認證傳遞給後端伺服器。 在這種情況下，您可以使用下列其中一個解決方案，允許從 ASP 頁面存取目錄：

-   使用 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) 或 [**ADsOpenObject**](binding-with-adsopenobject-and-iadsopendsobject-opendsobject.md) 將認證傳遞至 Active Directory。 網頁會向 IIS 伺服器驗證已連接的使用者。 當使用者經過驗證後，網頁可以使用 Objdso.opendsobject 或 ADsOpenObject 將使用者名稱和密碼傳遞至目錄服務，以取得後端伺服器的驗證。 然後，網頁可以存取目錄中的資料。
-   將您的程式碼新增至 COM 物件，並將此物件放入 [Com + 應用程式](../cossdk/com--application-overview.md) 中， (先前稱為 MTS 封裝) 。 然後，COM + 應用程式可以做為 [網域使用者帳戶](/windows/desktop/AD/domain-user-accounts)來執行。
-   使用多個 ASP 頁面，其中一個頁面會驗證用戶端，而另一個頁面會在網域使用者帳戶上使用匿名驗證，將認證傳遞至目錄。

這些方法牽涉到驗證網頁用戶端，然後在聯繫目錄時變更認證，因為使用相同認證的雙躍點驗證是不可能的。

 

 