---
title: 設定物件的存取權限
description: 本主題說明如何建立存取權的 ACE，並在物件的 DACL 上設定該 ACE。
ms.assetid: c0b45709-4652-46c7-8d52-44076802d109
ms.tgt_platform: multiple
keywords:
- 設定物件 AD 的存取權限
- 物件 AD，設定物件的存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bcf54de381dab2af1dab4ea44654fb0a5682f06
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462820"
---
# <a name="setting-access-rights-on-an-object"></a>設定物件的存取權限

當使用 ADSI COM 物件 [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) (安全描述項) 、 [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) (dacl 和 Sacl) ，以及 [**IADSACCESSCONTROLENTRY**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) (ACE) 將 ace 新增至 ACL 時，您要對屬性快取中指定物件的 **nTSecurityDescriptor** 屬性進行變更。 這表示將方法放在包含新 ACE 的物件上，而且必須呼叫 [**IADs SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 方法，以便將更新的安全描述項寫入至屬性快取中的目錄。

如需在 Active Directory Domain Services 中為物件設定 ACE 的詳細資訊和程式碼範例，請參閱在 [目錄物件上設定 ace 的範例程式碼](example-code-for-setting-an-ace-on-a-directory-object.md)。

使用下列一般程式來建立存取權限的 ACE，並在物件的 DACL 上設定該 ACE。

1.  取得物件的 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 介面指標。
2.  使用 [**IADs**](/windows/desktop/api/iads/nf-iads-iads-get) 取得物件的安全描述項。 包含安全描述項的屬性名稱是 **nTSecurityDescriptor**。 屬性將會以包含 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)指標的 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)傳回， (**vt** 成員是 **vt \_ 分派**) 。 在該 **IDispatch** 指標上呼叫 **QueryInterface** 來取得 [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor)介面，以便使用該介面上的方法來存取安全描述項的 ACL。
3.  使用 [**IADsSecurityDescriptor. objdescriptor.discretionaryacl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) 屬性來取得 DACL。 方法會傳回 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 指標。 在該 **IDispatch** 指標上呼叫 **QueryInterface** 來取得 [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)介面，以便使用該介面上的方法來存取 ACL 中的個別 ace。
4.  使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立新 ACE 的 ADSI COM 物件，並取得該物件的 [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) 介面指標。 請注意，類別識別碼是 CLSID \_ AccessControlEntry。
5.  使用 [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) 方法來設定 ACE 的屬性：

    1.  使用 [**IADsAccessControlEntry：:p 的 ui \_ 信任者**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ，設定要套用此 ACE 的信任者。 信任者是使用者、群組或其他安全性主體。 您的應用程式應該使用您想要套用 ACE 之信任者的使用者或群組物件中的適當屬性值。 信任者指定為 **BSTR** ，並且可以採用下列形式：
        -   網域帳戶 (舊版 Windows NT) 的登入名稱，格式為 " <domain> \\ <user account> "，其中 " &lt; domain &gt; " 是包含使用者之 Windows NT 網域的名稱，而 " &lt; user account &gt; " 是指定使用者的 **sAMAccountName** 屬性。 例如： "fabrikam \\ jeffsmith"。
        -   知名的安全性主體，代表 Windows NT 安全性系統所定義的特殊身分識別，例如 everyone、local system、principal self、已驗證的使用者、creator owner 等等。 代表知名安全性主體的物件會儲存在「設定」容器底下的知名安全性主體容器中。 例如，匿名登入。
        -   內建組，代表 Windows NT 安全性系統所定義的內建使用者群組。 它的形式是「內建」， \\ <group name> 其中「 &lt; 組名」 &gt; 是內建使用者群組的名稱。 代表內建組的物件會儲存在網域容器底下的內建容器中。 例如，「內建系統 \\ 管理員」。
        -   SID (字串格式) 指定的使用者，也就是指定使用者的 **objectSID** 屬性。 您可以使用 Win32 安全性 API 中的 [**ConvertSidToStringSid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) 函式，將轉換成字串形式。 例如： "S-1-5-32-548"。
    2.  使用 [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性來設定指定存取權限的遮罩。 [**ADS \_ 許可權 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_rights_enum)列舉會指定您可以在目錄物件上設定的存取權限。
    3.  您可以使用 [**IADsAccessControlEntry AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性來指定是要允許還是拒絕 **AccessMask** 所設定的存取權限。 針對標準許可權，這可以是 **廣告 \_ ACETYPE \_ 存取 \_ 允許** 的 **或 \_ ads \_ ACETYPE \_ 拒絕存取**。 針對特定物件使用權限 (套用至特定物件部分或特定物件類型) 的許可權，請使用 **ADS \_ ACETYPE \_ 存取 \_ 允許的 \_ 物件** 或 **ADS \_ ACETYPE \_ \_ 拒絕存取 \_ 物件**。 [**ADS \_ ACETYPE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_acetype_enum)列舉會指定您可以在 ACE 上設定的存取類型。
    4.  使用 [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性來指定指定物件下的其他容器或物件是否可以繼承 ACE。 [**ADS \_ ACEFLAG \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum)列舉會指定您可以在 ACE 上設定的繼承旗標。
    5.  您可以使用 [ [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ] 屬性來指定是否要將許可權套用至物件的特定部分、繼承的物件類型，或兩者。
    6.  如果 [ **旗標** ] 設定為 [ **ads \_ 旗標 \_ 物件 \_ 類型 \_**]，請將 [ [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ] 屬性設為 [指定包含物件 (類別的 GUID 的字串]，以讓 **ads \_ right \_ ds \_ 建立 \_ 子** 系或 **ADS \_ right \_ ds \_ 刪除 \_ 子**) 、屬性、屬性集、驗證的寫入或套用 ACE 的擴充許可權。 GUID 必須指定為 COM 程式庫中 [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) 函式所產生的格式字串。
    7.  如果 [ **旗標** ] 設定為 [ **ADS \_ 旗標繼承的 \_ \_ 物件 \_ 類型 \_ 存在**]，請設定 [**IADsAccessControlEntry InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性，以指定包含套用 ACE 之繼承物件類別之 GUID 的字串。 GUID 必須指定為 COM 程式庫中 [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) 函式所產生的格式字串。

6.  在 [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry)物件上使用 **QueryInterface** 方法來取得 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)指標。 [**IADsAccessControlList. AddAce**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-addace)方法需要對 ACE 的 **IDispatch** 介面指標。
7.  使用 [**IADsAccessControlList. AddAce**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-addace) 將新的 ACE 新增至 DACL。 請注意，在 ACL 中的 Ace 順序可能會影響對物件的存取評估。 對物件的正確存取權可能會要求您建立新的 ACL、從現有 ACL 將 Ace 以正確的順序新增至新的 ACL，然後將安全描述項中的現有 ACL 取代為新的 ACL。 如需詳細資訊，請參閱 [DACL 中的 Ace 順序](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)。
8.  使用 [**IADsSecurityDescriptor. objdescriptor.discretionaryacl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) 屬性，將包含新 ACE 的 DACL 寫入安全描述項。 如需 Dacl 的詳細資訊，請參閱 [Null dacl 和空白的 dacl](null-dacls-and-empty-dacls.md)。
9.  使用 [**IADs**](/windows/desktop/api/iads/nf-iads-iads-put) 方法，將安全描述項寫入物件的 **nTSecurityDescriptor** 屬性至屬性快取。
10. 使用 [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 方法來更新目錄中物件的屬性。

 

 