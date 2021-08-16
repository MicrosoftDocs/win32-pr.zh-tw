---
title: IADsUser 屬性與 Active Directory 屬性之間的對應
description: 如果適用的話，ADSI 使用者物件的屬性會對應至適當的 Active Directory 屬性。 ADSI 使用者物件屬性是與 IADsUser 屬性方法相關聯。
ms.assetid: 9b568084-5a6b-4a73-be88-9d9cd8007824
ms.tgt_platform: multiple
keywords:
- IADsUser 屬性與 ADSI 的 Active Directory 屬性之間的對應
- LDAP 提供者 ADSI、user 物件、IADsUser 屬性與 Active Directory 屬性之間的對應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e659c6325457b2654ad5cfeef964975949150232c4ae3376fac640c51c41aa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839478"
---
# <a name="mapping-between-iadsuser-properties-and-active-directory-attributes"></a>IADsUser 屬性與 Active Directory 屬性之間的對應

如果適用的話，ADSI 使用者物件的屬性會對應至適當的 Active Directory 屬性。 ADSI 使用者物件屬性是與 [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) 屬性方法相關聯。

下表列出 LDAP 提供者的 [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) 屬性和對應的 Active Directory 屬性之間的對應。



| IADsUser 屬性                                           | Active Directory 屬性                                                                                  |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**AccountDisabled**](iadsuser-property-methods.md)        | **廣告 \_\_** [**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)屬性中的 UF ACCOUNTDISABLE 旗標。  |
| [**Iadsuser.accountexpirationdate**](iadsuser-property-methods.md)  | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                             |
| [**BadLoginAddress**](iadsuser-property-methods.md)        | 不支援。                                                                                              |
| [**BadLoginCount**](iadsuser-property-methods.md)          | [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)                                                                   |
| [**部門**](iadsuser-property-methods.md)             | [**department**](/windows/desktop/ADSchema/a-department)                                                                     |
| [**描述**](iadsuser-property-methods.md)            | [**描述**](/windows/desktop/ADSchema/a-description)                                                                   |
| [**部門**](iadsuser-property-methods.md)               | [**劃分**](/windows/desktop/ADSchema/a-division)                                                                         |
| [**EmailAddress**](iadsuser-property-methods.md)           | [**mail**](/windows/desktop/ADSchema/a-mail)                                                                                 |
| [**EmployeeID**](iadsuser-property-methods.md)             | [**employeeID**](/windows/desktop/ADSchema/a-employeeid)                                                                     |
| [**FaxNumber**](iadsuser-property-methods.md)              | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)                                         |
| [**FirstName**](iadsuser-property-methods.md)              | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                                                       |
| [**FullName**](iadsuser-property-methods.md)               | [**displayName**](/windows/desktop/ADSchema/a-displayname)                                                                   |
| [**GraceLoginsAllowed**](iadsuser-property-methods.md)     | 不支援。                                                                                              |
| [**GraceLoginsRemaining**](iadsuser-property-methods.md)   | 不支援。                                                                                              |
| [**HomeDirectory**](iadsuser-property-methods.md)          | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)                                                               |
| [**網頁**](iadsuser-property-methods.md)               | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                                                                   |
| [**IsAccountLocked**](iadsuser-property-methods.md)        | [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime)                                                                   |
| [**語言**](iadsuser-property-methods.md)              | 不支援。                                                                                              |
| [**LastFailedLogin**](iadsuser-property-methods.md)        | [**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)                                                           |
| [**LastLogin**](iadsuser-property-methods.md)              | [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)                                                                       |
| [**LastLogoff**](iadsuser-property-methods.md)             | [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)                                                                     |
| [**LastName**](iadsuser-property-methods.md)               | [**錫**](/windows/desktop/ADSchema/a-sn)                                                                                     |
| [**LoginHours**](iadsuser-property-methods.md)             | [**logonHours**](/windows/desktop/ADSchema/a-logonhours)                                                                     |
| [**LoginScript**](iadsuser-property-methods.md)            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)                                                                     |
| [**LoginWorkstations**](iadsuser-property-methods.md)      | [**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations)                                                         |
| [**Manager**](iadsuser-property-methods.md)                | [**經理**](/windows/desktop/ADSchema/a-manager)                                                                           |
| [**MaxLogins**](iadsuser-property-methods.md)              | 不支援。                                                                                              |
| [**MaxStorage**](iadsuser-property-methods.md)             | [**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)                                                                     |
| [**NamePrefix**](iadsuser-property-methods.md)             | [**personalTitle**](/windows/desktop/ADSchema/a-personaltitle)                                                               |
| [**>namesuffix**](iadsuser-property-methods.md)             | [**generationQualifier**](/windows/desktop/ADSchema/a-generationqualifier)                                                   |
| [**OfficeLocations**](iadsuser-property-methods.md)        | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename)                                     |
| [**OtherName**](iadsuser-property-methods.md)              | [**middleName**](/windows/desktop/ADSchema/a-middlename)                                                                     |
| [**PasswordExpirationDate**](iadsuser-property-methods.md) | 使用群組原則編輯器設定                                                                               |
| [**PasswordLastChanged**](iadsuser-property-methods.md)    | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                                     |
| [**PasswordMinimumLength**](iadsuser-property-methods.md)  | 使用群組原則編輯器設定                                                                               |
| [**PasswordRequired**](iadsuser-property-methods.md)       | **廣告 \_UserAccountControl 屬性中的 UF \_ PASSWD \_ NOTREQD** 旗標。 [](/windows/desktop/ADSchema/a-useraccountcontrol) |
| [**Picture**](iadsuser-property-methods.md)                | [**thumbnailPhoto**](/windows/desktop/ADSchema/a-thumbnailphoto)                                                             |
| [**PostalAddresses**](iadsuser-property-methods.md)        | [**postalAddress**](/windows/desktop/ADSchema/a-postaladdress)                                                               |
| [**PostalCodes**](iadsuser-property-methods.md)            | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                                     |
| [**設定檔**](iadsuser-property-methods.md)                | [**profilePath**](/windows/desktop/ADSchema/a-profilepath)                                                                   |
| [**RequireUniquePassword**](iadsuser-property-methods.md)  | 使用群組原則編輯器設定                                                                               |
| [**SeeAlso**](iadsuser-property-methods.md)                | [**seeAlso**](/windows/desktop/ADSchema/a-seealso)                                                                           |
| [**TelephoneHome**](iadsuser-property-methods.md)          | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                                                       |
| [**TelephoneMobile**](iadsuser-property-methods.md)        | [**移動**](/windows/desktop/ADSchema/a-mobile)                                                                             |
| [**TelephoneNumber**](iadsuser-property-methods.md)        | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                                                           |
| [**TelephonePager**](iadsuser-property-methods.md)         | [**傳呼 機**](/windows/desktop/ADSchema/a-pager)                                                                               |
| [**標題**](iadsuser-property-methods.md)                  | [**標題**](/windows/desktop/ADSchema/a-title)                                                                               |



 

 

 