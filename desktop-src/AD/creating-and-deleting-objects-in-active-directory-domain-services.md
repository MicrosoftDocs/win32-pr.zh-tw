---
title: 在 Active Directory Domain Services 中建立和刪除物件
description: 在 Active Directory Domain Services 中，用來以程式設計方式建立和刪除物件的程式，取決於所使用的程式設計技術。
ms.assetid: 13f83aea-ad39-4737-af3c-24316a31046d
ms.tgt_platform: multiple
keywords:
- 建立和刪除 Active Directory 物件 Active Directory
- 使用建立和刪除物件的 Active Directory Domain Services Active Directory
- 物件 Active Directory、建立及刪除 Active Directory Domain Services 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d3e85ef3c356978faeab059e3969bb657185bd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462896"
---
# <a name="creating-and-deleting-objects-in-active-directory-domain-services"></a>在 Active Directory Domain Services 中建立和刪除物件

在 Active Directory Domain Services 中，用來以程式設計方式建立和刪除物件的程式，取決於所使用的程式設計技術。 如需有關使用特定程式設計技術在 Active Directory Domain Services 中建立和刪除物件的詳細資訊，請參閱下表所列的主題。



| 程式設計技術                                                                       | 取得詳細資訊                                                            |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Active Directory 服務介面](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [建立和刪除物件](/windows/desktop/ADSI/creating-and-deleting-objects)             |
| [輕量型目錄存取協定](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [修改目錄專案](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry)                 |
| [System.DirectoryServices](/dotnet/api/system.directoryservices) | [建立、刪除、重新命名和移動物件](https://msdn.microsoft.com/library/ms180850(v=VS.80).aspx) |



 

## <a name="creating-an-object"></a>建立物件

一般情況下，建立物件所需的唯一屬性是 **cn** 和 **objectClass** 屬性。 不過，建立物件並不一定會讓它成為功能物件。 某些類型的物件（例如使用者和群組）具有其他必要屬性，可讓它們正常運作。 如需建立特定物件類型的詳細資訊，請參閱[在定義域中](creating-groups-in-a-domain.md)[建立使用者](creating-a-user.md)和建立群組。

**Windows Server 2003：** 在 WWindows 伺服器2003或更新版本上執行的網域控制站上建立 [**使用者**](/windows/desktop/ADSchema/c-user)、 [**群組**](/windows/desktop/ADSchema/c-group)或 [**電腦**](/windows/desktop/ADSchema/c-computer) 類別的物件時，網域控制站會自動將物件的 [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) 屬性設定為唯一字串（如果未指定的話）。

## <a name="deleting-an-object"></a>刪除物件

刪除物件時，Active Directory 伺服器會執行下列動作：

-   已刪除之物件的 **isDeleted** 屬性設定為 **TRUE**。 將 IsDeleted 屬性值設為 **TRUE** 的物件會被 [*稱為「*](/previous-versions/windows/desktop/legacy/ms681941(v=vs.85))標記」（  ）。
-   已刪除的物件會移至其命名內容的 Deleted Objects 容器。 如果 [物件 **systemFlags** ] 屬性包含0x02000000 旗標，則物件不會移至 [已刪除的物件] 容器。 如需有關系結至已刪除物件容器之內容和列舉的詳細資訊，請參閱 [取出已刪除的物件](retrieving-deleted-objects.md)。
-   刪除的物件容器是平面的，因此所有物件都位於已刪除物件容器中的相同層級上。 因此，已刪除之物件的相對辨別名稱會變更，以確保該名稱在已刪除的物件容器中是唯一的。 如果原始名稱的長度超過75個字元，則會截斷為75個字元。 接著會將下列內容附加至新名稱：
    1.  0x0A 字元
    2.  字串 "DEL："
    3.  唯一 GUID 的字串格式，例如 "947e3228-70c9-4311-8b7a-e5c9b5bd4432"

    已刪除的物件名稱範例如下：
    ```C++
    Jeff Smith\0ADEL:947e3228-70c9-4311-8b7a-e5c9b5bd4432
    ```

    

-   已刪除之物件的大部分屬性值都會被移除。 系統會自動保留下列屬性：

    -   **attributeID**
    -   **attributeSyntax**
    -   **distinguishedName**
    -   **dNReferenceUpdate**
    -   **flatName**
    -   **governsID**
    -   **groupType**
    -   **instanceType**
    -   **lDAPDisplayName**
    -   **legacyExchangeDN**
    -   **CreatorSID**
    -   **mSMQOwnerID**
    -   **name**
    -   **nCName**
    -   **objectClass**
    -   **objectGUID**
    -   **objectSid**
    -   **oMSyntax**
    -   **proxiedObjectName**
    -   **replPropertyMetaData**
    -   **sAMAccountName**
    -   **securityIdentifier**
    -   **subClassOf**
    -   **systemFlags**
    -   **trustAttributes**
    -   **trustDirection**
    -   **trustPartner**
    -   **trustType**
    -   **userAccountControl**
    -   **uSNChanged**
    -   **uSNCreated**
    -   **whenCreated**

    包含0x00000008 之 **searchFlags** 屬性值的其他屬性也會保留下來。

    下列屬性值一律會從已刪除的物件中移除：

    -   **objectCategory**
    -   **samAccountType**

-   系統會保留已刪除之物件的安全描述項，並且不會傳播可繼承的存取控制專案。 在刪除物件時，安全描述項會保持原樣。
-   已刪除之物件的連結會被清除。 這會在刪除物件之後于背景中執行。 如果刪除的物件會在清除所有連結之前還原，則會收到錯誤。
-   如果在 Windows Server 2003 網域控制站上刪除物件，已刪除之物件的 **lastKnownParent** 屬性會設為刪除該物件時所包含之容器的分辨名稱。

已刪除的物件會保留在 [已刪除的物件] 容器中一段時間，稱為「*標記存留期」。* 依預設，標記存留期為60天，但系統管理員可以變更此值。 在標記存留期到期之後，物件會從目錄服務中永久移除。 為了避免遺失刪除作業，應用程式必須比標記存留期更頻繁地執行增量同步處理。

Windows Server 2003 新增了還原已刪除物件的功能。 如需有關已刪除物件還原的詳細資訊，請參閱 [還原已刪除的物件](restoring-deleted-objects.md)。

當刪除專案時，不能修改物件的任何屬性。 在 Windows Server 2003 中，可以修改已刪除物件上 (**ntSecurityDescriptor** 屬性) 的安全描述項。 這是為了在還原物件的人員沒有強制屬性的寫入權限時，允許還原物件。 若要更新已刪除之物件上的安全描述項，呼叫者除了一般 **寫入 \_ DAC** 和 **寫入 \_ 擁有** 者存取權之外，還必須具有命名內容的「重新產生標記」存取權限。 即使安全描述項的限制，系統管理員仍可先取得物件的擁有權，假設系統管理員具有「 **SE \_ 取得 \_ 擁有權」 \_ 名稱** 許可權，然後修改安全描述項。 若要這樣做，請在 [**ldap \_ 伺服器 \_ 顯示 \_ 已刪除的 \_ OID**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid)控制項時，使用 [**ldap \_ modify \_ ext \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s)函數。 修改清單必須包含 **ntSecurityDescriptor** 屬性的單一屬性取代。

 

 