---
title: User 物件屬性
description: 使用者物件具有多個屬性。 本節記載 Windows、系統管理工具和 Windows 通訊錄 (WAB) 所使用的重要屬性。 它不會描述所有屬性;許多屬性不會用於使用者物件。
ms.assetid: c173c5d1-2680-4b9c-961d-251fba6e2c7c
ms.tgt_platform: multiple
keywords:
- User 物件屬性廣告
- Users AD、User 物件屬性
- 物件 AD、使用者、屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a1bb6b347bd55daceb07dfe1fad4adc3e1352afc91ec14018aab6b24615c2b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182627"
---
# <a name="user-object-attributes"></a>User 物件屬性

使用者物件具有多個屬性。 本節記載 Windows、系統管理工具和 Windows 通訊錄 (WAB) 所使用的重要屬性。 它不會描述所有屬性;許多屬性不會用於使用者物件。

某些屬性會儲存在目錄中（例如 [**cn**](/windows/desktop/ADSchema/a-cn)、 [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)、 [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)等），並複寫到網域內的所有網域控制站。 這些屬性的子集也會複寫到通用類別目錄。

非複寫的屬性會儲存在每個網域控制站上，但不會複寫到其他位置，例如 [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)、 [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)、 [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)等等。 非複寫的屬性是與特定網域控制站相關的屬性。 例如， **lastLogon** 是使用者網路登入的最後一個日期和時間，會由傳回該屬性的特定網域控制站進行驗證。

使用者物件也具有未儲存在目錄中的已建立屬性，但網域控制站會計算這些屬性，例如 [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname)、 [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname)、 [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes)等等。

使用者物件的屬性會分類為：

<dl> <dt>

<span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>基底物件屬性
</dt> <dd>

此類別包含所有目錄物件（例如 [**objectClass**](/windows/desktop/ADSchema/a-objectclass)、 [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)等）所需的屬性。

</dd> <dt>

<span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>命名屬性
</dt> <dd>

這個類別包含用來參考或識別物件的屬性，例如 [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname)、 [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)、 [**objectSID**](/windows/desktop/ADSchema/a-objectsid)等等。 如需有關為使用者物件命名屬性的詳細資訊，請參閱 [使用者命名屬性](naming-properties.md)。

</dd> <dt>

<span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>安全性屬性
</dt> <dd>

此類別包含登入和存取控制的屬性。 如需有關使用者物件之安全性屬性的詳細資訊，請參閱 [使用者安全性屬性](security-properties.md)。

</dd> <dt>

<span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>通訊錄屬性
</dt> <dd>

此類別包括電子郵件和使用者資料的屬性。 如需有關使用者物件通訊錄屬性的詳細資訊，請參閱 [使用者通訊錄屬性](address-book-properties.md)。

</dd> <dt>

<span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>應用程式特定屬性
</dt> <dd>

此類別包含特定應用程式的使用者特定設定資料。

</dd> </dl>

如需有關讀取和修改使用者物件屬性的詳細資訊，請參閱 [在 Active Directory Domain Services 中讀取和寫入物件的屬性](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md)。

如需使用者類別的詳細資訊，包括類別的 [**mayContain**](/windows/desktop/ADSchema/a-maycontain) 和 [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) 屬性的完整清單，請參閱 [**使用者**](/windows/desktop/ADSchema/c-user)。

## <a name="setting-passwords"></a>設定密碼

無法直接修改使用者的密碼，因為這牽涉到透過網路傳送未加密的密碼。 若要設定使用者的密碼，必須使用 [**IADsUser**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) 或 [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) 方法。 當應用程式允許使用者變更自己的密碼時，會使用 **IADsUser. ChangePassword** 方法。 當應用程式可讓系統管理員重設密碼時，會使用 **IADsUser. SetPassword** 方法。

 

 