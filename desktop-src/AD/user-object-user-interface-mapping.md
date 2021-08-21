---
title: 使用者物件使用者介面對應
description: 下表指出 Active Directory 消費者和電腦嵌入式管理單元所提供的屬性頁。
ms.assetid: f309c139-c957-40c4-b369-f527aa87157c
ms.tgt_platform: multiple
keywords:
- 消費者介面對應 AD 的使用者物件
- 消費者介面對應 AD、使用者物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656e8071b558b730ecb1fc0463834f6fbadb7eb9bf4c56b11640e2b95209735f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024496"
---
# <a name="user-object-user-interface-mapping"></a>使用者物件使用者介面對應

下表指出 Active Directory 消費者和電腦嵌入式管理單元所提供的屬性頁。 每個資料表都會識別屬性頁的使用者介面元素，以及與該使用者介面專案相關聯的屬性。 由於 Active Directory 消費者和電腦嵌入式管理單元所顯示的屬性頁可以擴充，因此無法為屬性工作表中顯示的所有頁面提供此資料。

## <a name="general-property-page"></a>一般屬性頁

下表列出 [ **一般** ] 屬性頁的 UI 標籤。



| UI 標籤         | Active Directory Domain Services 中的屬性                           |
|------------------|-------------------------------------------------------------------------|
| 名字       | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                   |
| 姓氏        | [**錫**](/windows/desktop/ADSchema/a-sn)                                                 |
| 縮寫         | [**縮寫**](/windows/desktop/ADSchema/a-initials)                                     |
| 顯示名稱     | [**displayName**](/windows/desktop/ADSchema/a-displayname)                               |
| 描述      | [**描述**](/windows/desktop/ADSchema/a-description)                               |
| Office           | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) |
| 電話號碼 | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                       |
| 電話：其他 | [**otherTelephone**](/windows/desktop/ADSchema/a-othertelephone)                         |
| 電子郵件           | [**電子郵件地址**](/windows/desktop/ADSchema/a-mail)                                 |
| 網頁         | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                               |
| 網頁：其他  | [**Url**](/windows/desktop/ADSchema/a-url)                                               |



 

## <a name="account-property-page"></a>帳戶屬性頁面

下表列出 [ **帳戶** ] 屬性頁的 UI 標籤。



| UI 標籤                                | Active Directory Domain Services 中的屬性                                                   | 註解                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UserLogon 名稱                          | [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname)                                           | 此欄位會從 [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) 屬性中最後一個 ' @ ' 字元之前的所有專案中取得。 最後的 ' @ ' 字元和其後的所有專案都放在尾碼下拉式方塊中。                                                                                                                                                      |
| 使用者登入名稱 (預先 Windows 2000)       | [**sAMAccountname**](/windows/desktop/ADSchema/a-samaccountname)                                                 | 不加評論。                                                                                                                                                                                                                                                                                                                                                                             |
| 登入時數                             | [**logonHours**](/windows/desktop/ADSchema/a-logonhours)                                                         | 不加評論。                                                                                                                                                                                                                                                                                                                                                                             |
| 登入到                               | [**logonWorkstation**](/windows/desktop/ADSchema/a-logonworkstation)                                             | 不加評論。                                                                                                                                                                                                                                                                                                                                                                             |
| 帳戶已鎖定                   | [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime)和 [ **lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) | 如果 [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) 屬性不是零，就會將 [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) 屬性新增至 **lockoutTime** ，並比較目前的日期和時間，以判斷帳戶是否已被鎖定。                                                                                                                                |
| 使用者必須在下次登入時變更密碼 | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                         | 不加評論。                                                                                                                                                                                                                                                                                                                                                                             |
| 使用者不能變更密碼             | N/A                                                                                             | 這是 ACL 中的變更密碼控制項。                                                                                                                                                                                                                                                                                                                                         |
| 其他帳戶選項                   | [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)                                         | 帳戶選項中的其餘專案會切換 [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) 屬性位元遮罩中的位， (DWORD) 中的旗標。                                                                                                                                                                                                                                 |
| 帳戶到期                         | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                 | **帳戶到期** 控制會顯示帳戶將于結束時到期的日期。 [**AccountExpires**](/windows/desktop/ADSchema/a-accountexpires)屬性會儲存為帳戶到期的日期。 因此， **帳戶到期** 控制項中顯示的日期會顯示為比 **accountExpires** 屬性中包含的日期還早的一天。 |



 

## <a name="address-property-page"></a>位址屬性頁

下表列出 [ **位址** ] 屬性頁的 UI 標籤。



| UI 標籤        | Active Directory Domain Services 中的屬性                                                 | 註解                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Street          | [**streetAddress**](/windows/desktop/ADSchema/a-streetaddress)                                                 | 不加評論。                                               |
| P. O Box         | [**postOfficeBox**](/windows/desktop/ADSchema/a-postofficebox)                                                 | 不加評論。                                               |
| City            | [**我**](/windows/desktop/ADSchema/a-l)                                                                         | **L** 屬性名稱在地區設定中是小寫的 "l"。 |
| 州/省  | [**聖**](/windows/desktop/ADSchema/a-st)                                                                       | 不加評論。                                               |
| 郵遞區號 | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                       | 不加評論。                                               |
| 國家/地區  | [**c**](/windows/desktop/ADSchema/a-c)、 [**co**](/windows/desktop/ADSchema/a-co)和 [**countryCode**](/windows/desktop/ADSchema/a-countrycode) | 不加評論。                                               |



 

## <a name="member-of-property-page"></a>屬性頁的成員

下表列出屬性頁面 **成員** 的 UI 標籤。



| UI 標籤          | Active Directory Domain Services 中的屬性   | 註解                                                                                                                                                                    |
|-------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 成員隸屬         | [**memberOf**](/windows/desktop/ADSchema/a-memberof)             | 包含 UI 清單中的所有群組（主要群組除外），而主要群組是透過 [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) 屬性在廣告中表示。 |
| 設定主要群組 | [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) | LDAP：系結至主要群組的 [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) 。                                                                                  |



 

## <a name="organization-property-page"></a>組織屬性頁面

下表顯示 [ **組織** ] 屬性頁的 UI 標籤。



| UI 標籤       | Active Directory Domain Services 中的屬性 | 註解     |
|----------------|-----------------------------------------------|-------------|
| 標題          | [**標題**](/windows/desktop/ADSchema/a-title)                 | 不加評論。 |
| department     | [**department**](/windows/desktop/ADSchema/a-department)       | 不加評論。 |
| 公司        | [**公司**](/windows/desktop/ADSchema/a-company)             | 不加評論。 |
| 管理員：名稱   | [**經理**](/windows/desktop/ADSchema/a-manager)             | 不加評論。 |
| Direct Reports | [**directReports**](/windows/desktop/ADSchema/a-directreports) | 不加評論。 |



 

## <a name="profile-property-page"></a>配置檔案屬性頁面

下表列出 **設定檔** 屬性頁的 UI 標籤。



| UI 標籤                | Active Directory Domain Services 中的屬性 | 註解                                                                                                                 |
|-------------------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| 設定檔路徑            | [**profilePath**](/windows/desktop/ADSchema/a-profilepath)     | 不加評論。                                                                                                             |
| 登入腳本            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)       | 不加評論。                                                                                                             |
| 主資料夾：本機路徑 | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | 如果選取 **本機路徑** ，則本機路徑會儲存在 [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) 屬性中。 |
| 主資料夾：連線    | [**homeDrive**](/windows/desktop/ADSchema/a-homedrive)         | 如果選取 **連線**，則會將對應的磁片磁碟機儲存在 [**homeDrive**](/windows/desktop/ADSchema/a-homedrive)屬性中。          |
| 主資料夾：到         | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | 如果選取 **連線**，路徑會儲存在 [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)屬性中。          |



 

## <a name="telephones-property-page"></a>電話屬性頁

下表列出 [ **電話** ] 屬性頁的 UI 元素，以及其對應的 Active Directory 屬性。



| UI 標籤        | Active Directory Domain Services 中的屬性                                 |
|-----------------|-------------------------------------------------------------------------------|
| 首頁            | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                         |
| 首頁：其他     | [**otherHomePhone**](/windows/desktop/ADSchema/a-otherhomephone)                               |
| 呼叫器           | [**傳呼 機**](/windows/desktop/ADSchema/a-pager)                                                 |
| 呼機：其他    | [**otherPager**](/windows/desktop/ADSchema/a-otherpager)                                       |
| 行動          | [**移動**](/windows/desktop/ADSchema/a-mobile)                                               |
| Mobile：其他   | [**otherMobile**](/windows/desktop/ADSchema/a-othermobile)                                     |
| 傳真             | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)           |
| 傳真：其他      | [**otherFacsimileTelephoneNumber**](/windows/desktop/ADSchema/a-otherfacsimiletelephonenumber) |
| IP 電話        | [**ipPhone**](/windows/desktop/ADSchema/a-ipphone)                                             |
| IP 電話：其他 | [**otherIpPhone**](/windows/desktop/ADSchema/a-otheripphone)                                   |
| 備註           | [**資訊**](/windows/desktop/ADSchema/a-info)                                                   |



 

## <a name="environment-sessions-remote-control-and-terminal-services-profile-property-pages"></a>環境、會話、遠端控制和終端機服務配置檔案屬性頁面

系統會為使用者物件提供 **環境**、 **會話**、 **遠端控制** 和 **終端機服務設定檔** 頁面，以支援終端機服務。 這些頁面的 UI 元素不會對應到個別的屬性。 相反地，這些設定會儲存在 Active Directory Domain Services 中的私用資料。 您可以使用 [**IADsTsUserEx**](/windows/desktop/api/tsuserex/nn-tsuserex-iadstsuserex) 介面來存取終端機服務設定。

 

 