---
title: 安全性內容和 Active Directory Domain Services
description: 當應用程式系結至 Active Directory 網網域控制站 (DC) 時，它會在安全性主體的安全性內容中執行，這可以是使用者或實體（例如電腦或系統服務）。
ms.assetid: 7ad0acbe-f81b-46d6-be87-3526b0bfbd1b
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory，安全性內容
- 安全性內容 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c337cb05f8158dbb90f231652c42fb10a486aef4
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023218"
---
# <a name="security-contexts-and-active-directory-domain-services"></a>安全性內容和 Active Directory Domain Services

當應用程式系結至 Active Directory 網網域控制站 (DC) 時，它會在安全性主體的安全性內容中執行，這可以是使用者或實體（例如電腦或系統服務）。 安全性內容是指當執行緒嘗試存取安全物件時，系統用來強制執行安全性的使用者帳戶。 此資料包含使用者安全識別碼 (SID) 、群組成員資格和許可權。

使用者藉由呈現驗證的認證來建立安全性內容。 如果認證已通過驗證，系統會產生存取權杖，以識別與使用者帳戶相關聯的群組成員資格和許可權。 當您嘗試存取目錄物件時，系統會驗證您的存取權杖。 它會比較您存取權杖中的資料與由物件安全描述項授與或拒絕存取的帳戶和群組。

使用下列方法來控制您系結至 Active Directory DC 的安全性內容：

-   使用 **ADS \_ 安全 \_ 驗證** 選項搭配 [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) function 或 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject) 方法進行系結，並明確指定使用者名稱和密碼。 系統會驗證這些認證，並產生在該系結期間用來存取驗證的存取權杖。 如需詳細資訊，請參閱[驗證](authentication.md)。
-   使用 **ADS \_ 安全 \_ 驗證** 選項進行系結，但不指定認證。 如果您不是模擬使用者，系統會使用應用程式的主要安全性內容，也就是啟動您應用程式之使用者的安全性內容。 在系統服務的案例中，這是服務帳戶或 LocalSystem 帳戶的安全性內容。
-   模擬使用者，然後與 ADS 系 **結 \_ 安全 \_ 驗證**，但不指定認證。 在此情況下，系統會使用模擬之用戶端的安全性內容。 如需詳細資訊，請參閱 [用戶端](/windows/desktop/SecAuthZ/client-impersonation)模擬。
-   使用 [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) 或 [**IADsOpenDSObject：： Objdso.opendsobject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject) 與 **ADS \_ NO \_ 驗證** 選項進行系結。 這個方法不會進行驗證，而會產生「每個人」做為安全性內容。 只有 LDAP 提供者支援此選項。

可能的話，請系結，而不指定認證。 也就是說，請使用已登入使用者或模擬用戶端的安全性內容。 這可讓您避免快取認證。 如果您必須使用替代的使用者認證，請提示輸入認證，並將其系結，但不要快取這些認證。 若要在多個系結作業中使用相同的安全性內容，您可以指定第一個系結作業的使用者名稱和密碼，然後只指定使用者名稱以進行後續的系結。 如需使用這項技術的詳細資訊，請參閱 [驗證](authentication.md)。

有些安全性內容比其他內容更加強大。 例如，網域控制站上的 LocalSystem 帳戶具有 Active Directory Domain Services 的完整存取權，而一般使用者只能存取目錄中的部分物件。 一般來說，當效能較低的安全性內容足以執行作業時，您的應用程式不應該在強大的安全性內容中執行，例如 LocalSystem。 這表示您可能會想要將應用程式分成不同的元件，而每個元件都是在適用于要執行之作業的安全性內容中執行。 例如，您的應用程式安裝可以分為：

-   在屬於 Schema Administrators 群組成員之使用者的內容中，執行架構變更和延伸。
-   在屬於企業系統管理員群組成員之使用者的內容中，執行設定容器變更。
-   在屬於 Domain Administrators 群組成員之使用者的內容中執行網域容器變更。

 

 