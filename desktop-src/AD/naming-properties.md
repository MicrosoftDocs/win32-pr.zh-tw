---
title: 使用者命名屬性
description: 使用者命名屬性會識別使用者物件，例如用於安全性目的的登入名稱和識別碼。
ms.assetid: 2192743c-cedd-4b03-a402-3992d64a4801
ms.tgt_platform: multiple
keywords:
- 使用者命名屬性 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a504070cf2e78cf5647072ff740d137b4a6e6056
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933053"
---
# <a name="user-naming-attributes"></a>使用者命名屬性

使用者命名屬性會識別使用者物件，例如用於安全性目的的登入名稱和識別碼。 **Cn**、 **name** 和 **distinguishedName** 屬性都是使用者命名屬性的範例。 使用者物件是安全性主體物件，因此它也包含下列使用者命名屬性：

-   [userPrincipalName](#userprincipalname) —使用者的登入名稱
-   [objectGUID](#objectguid) —使用者的唯一識別碼
-   [sAMAccountName](#samaccountname) -支援舊版 Windows 的登入名稱
-   [objectSid](#objectsid) -使用者的安全識別碼 (SID) 
-   [sIDHistory](#sidhistory) ：使用者物件的先前 sid

> [!Note]  
> 您可以使用 [Active Directory 使用者和電腦] MMC 嵌入式管理單元來查看和管理這些屬性，該嵌入式管理單元可在 [遠端伺服器管理工具 (RSAT) ](https://www.microsoft.com/download/details.aspx?id=45520)中取得。

 

## <a name="userprincipalname"></a>userPrincipalName

**UserPrincipalName** 屬性是使用者的登入名稱。 屬性是由 (UPN) 的使用者主體名稱所組成，這是最常見的 Windows 使用者登入名稱。 使用者通常會使用其 UPN 來登入網域。 這個屬性是單一值的索引字串。

UPN 是使用者的網際網路樣式登入名稱，以網際網路標準 RFC 822 為基礎。 UPN 比分辨名稱短，而且更容易記住。 依照慣例，這應該對應到使用者的電子郵件名稱。 UPN 的點是合併電子郵件和登入命名空間，讓使用者只需要記住單一名稱。

### <a name="upn-format"></a>UPN 格式

UPN 是由 UPN 前置詞 (使用者帳戶名稱) 和 UPN 尾碼 (DNS 網域名稱) 所組成。 前置詞會使用 \"\@\" 符號與尾碼連結。 例如，"someone@ example.com"。 在目錄樹系的所有安全性主體物件之間，UPN 必須是唯一的。 這表示可以重複使用 UPN 的前置詞，而不是使用相同的尾碼。

UPN 尾碼具有下列限制：

-   它必須是網域的 DNS 名稱，但不需要是包含使用者之網域的名稱。
-   它必須是目前網域樹系中的網功能變數名稱稱，或是設定容器內分割區容器的 **upnSuffixes** 屬性中所列的替代名稱。

### <a name="upn-management"></a>UPN 管理

建立使用者帳戶時，可以指派 UPN 但不需要。 建立 UPN 時，不會影響使用者物件的其他屬性變更（例如重新命名或移動的使用者）。 這可讓使用者在重建目錄時保留相同的登入名稱。 不過，系統管理員可以變更 UPN。 當您建立新的使用者物件時，您應該檢查本機網域和通用類別目錄是否有建議的名稱，以確保它不存在。

當使用者使用 UPN 登入網域時，會藉由搜尋本機網域和通用類別目錄來驗證 UPN。 如果在通用類別目錄中找不到 UPN，則登入嘗試會失敗。

## <a name="objectguid"></a>objectGUID

**ObjectGUID** 屬性是使用者的唯一識別碼。 屬性是單一值的128位全域唯一識別碼 (GUID) ，而且會儲存為 [**ADS \_ 八進位 \_ 字串**](/windows/win32/api/iads/ns-iads-ads_octet_string) 結構。 建立使用者物件時，Active Directory server 會建立 GUID。

因為物件的辨別名稱會在物件重新命名或移動時發生變更，所以分辨名稱不是物件的可靠識別碼。 在 Active Directory Domain Services 中，即使物件已重新命名或移動，物件的 **objectGUID** 屬性也永遠不會變更。 您可以在 [IADs 屬性方法](/windows/desktop/ADSI/iads-property-methods)中使用 **GUID** 屬性方法，以取出 **objectGUID** 的字串形式。

## <a name="samaccountname"></a>sAMAccountName

**SAMAccountName** 屬性是用來支援舊版 Windows 用戶端和伺服器的登入名稱，例如 Windows NT 4.0、windows 95、windows 98 和 LAN Manager。 登入名稱必須少於或等於20個字元，而且在網域內的所有安全性主體物件中都是唯一的。

## <a name="objectsid"></a>objectSid

**ObjectSid** 屬性是使用者 (SID) 的安全識別碼。 在與 Windows 安全性互動期間，系統會使用 SID 來識別使用者及其群組成員資格。 屬性是單一值。 SID 是唯一的二進位值，用來將使用者識別為安全性主體。

建立使用者時，系統會設定 SID。 每個使用者都有一個由 Windows 網域發出的唯一 SID，並儲存在目錄中使用者物件的 **objectSid** 屬性中。 每次使用者登入時，系統會從目錄抓取使用者的 SID，並將其放在使用者的存取權杖中。 使用者的 SID 也會用來取得使用者所屬群組的 Sid，並將其放在使用者的存取權杖中。 使用 SID 做為使用者或群組的唯一識別碼時，無法再次使用它來識別另一個使用者或群組。

## <a name="sidhistory"></a>sIDHistory

**SIDHistory** 屬性包含使用者物件先前的 sid。 這是多重值的屬性。 如果使用者已移至另一個網域，則使用者物件具有先前的 Sid。 只要將使用者物件移至新的網域，就會建立新的 SID 並指派 **objectSid** 屬性，並將先前的 sid 新增至 **sIDHistory** 屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[User 物件屬性](user-object-attributes.md)
</dt> </dl>

 

 