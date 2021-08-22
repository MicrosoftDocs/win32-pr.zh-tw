---
title: 哪些應用程式和服務開發人員需要瞭解群組
description: 開發應用程式或服務時，您可以使用群組來委派整體或部分的管理或控制應用程式或服務的存取權。
ms.assetid: 19e189a5-2880-4b45-84c8-e7b542c4fbb6
ms.tgt_platform: multiple
keywords:
- 哪些應用程式和服務開發人員需要瞭解群組
- 為應用程式和服務開發人員分組 AD、資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b59a8a1ce369d9b5fa1093297f219bf6a206178a950b9d0762fde3069846551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024388"
---
# <a name="what-application-and-service-developers-need-to-know-about-groups"></a>哪些應用程式和服務開發人員需要瞭解群組

開發應用程式或服務時，您可以使用群組來委派整體或部分的管理或控制應用程式或服務的存取權。 例如，應用程式可以控制誰可以執行各種系統管理作業。 若要這樣做，請建立 Ace，以將指定的存取權限授與適當的群組。 最好的程式設計作法是讓 ACE 授與群組的存取權，而不是授與個別使用者或電腦存取權的數個 Ace。

使用群組時，建議應用程式使用下列指導方針：

-   請勿建立硬式編碼群組的相依性，如果刪除或移動群組，這可能會產生複雜的專案。
-   除非群組的功能提供應用程式的特定需求，否則請避免使用內建群組。 例如，不要求使用者必須是 Administrators 群組的成員，就能為使用者提供建立電腦帳戶的許可權。 這麼做會為使用者提供他們可能不需要的許可權，這可能會造成安全性弱點。 相反地，您應該建立具有所需特定許可權的新安全性群組，並將使用者新增至此新群組。
-   建立新群組時，請記住下列建議：
    -   藉由設定 Ace 來控制可以加入或移除成員的使用者，來保護群組。
    -   如果使用全域群組進行 Active Directory Domain Services 中物件的存取控制，請使用全域群組。
    -   只有在必要時才使用萬用群組 (成員資料是使用通用類別目錄的全域需求;群組可包含任何) 的使用者/群組。 如果您使用萬用群組，請將全域群組放置在萬用群組中，並在全域群組中新增/移除使用者。 避免對萬用群組進行過多的變更，以提供複寫效率。
-   請勿使用存取控制的群組成員資格。 相反地，請使用 ACE 並藉由讓系統執行存取檢查來控制存取權。

若要控制不符合 Active Directory 網域 services 中物件之預先定義存取權限的作業存取權，請使用 Windows 2000 中存取控制的 [存取控制] 存取權限功能。 如需詳細資訊，請參閱 [**ADS \_ 許可權 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_rights_enum)。

**使用控制項存取權限控制執行作業的許可權**

1.  建立可定義應用程式或服務存取類型的 control 存取權限。 如需詳細資訊，請參閱 [控制存取權限](control-access-rights.md)。
2.  在 Active Directory Domain Services 中建立代表應用程式、服務或資源的物件。
3.  將物件 Ace 新增至物件安全描述項中的 DACL，以授與或拒絕使用者或群組該物件上的控制項存取權限。 如需詳細資訊，請參閱 [設定物件的存取權限](setting-access-rights-on-an-object.md)。
4.  當使用者嘗試執行受保護的作業時，您的應用程式或服務會使用 [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) 函式來判斷是否將控制項存取權授與使用者。 如需詳細資訊，請參閱 [在物件的 ACL 中檢查控制項訪問](checking-a-control-access-right-in-an-objectampaposs-acl.md)許可權。
5.  根據對物件進行存取檢查的結果，您的應用程式或服務可以授與或拒絕使用者對應用程式或服務的存取權。

服務應用程式也可以建立一個群組，其成員會是不同的服務實例。 例如，在整個企業中的多部電腦上安裝實例的服務，可能會有所有服務實例寫入的通用記錄檔。 服務安裝程式會建立記錄檔，並使用 DACL 將存取權授與群組的成員。 群組成員將會是執行不同服務實例的使用者帳戶，或者，如果服務是在 LocalSystem 帳戶下執行，則成員會是主機伺服器的電腦帳戶。

 

 