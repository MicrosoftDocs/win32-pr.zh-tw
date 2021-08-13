---
title: ms DS 可系結物件類別
description: 代表可系結物件的輔助類別。 任何代表可用來系結至目錄之實體的使用者定義類別 (也就是使用者) ，都應該包含這個輔助類別。
ms.assetid: 181b3e2b-9442-4f11-9af7-4697491115f3
ms.tgt_platform: multiple
keywords:
- ms DS 可系結-物件類別 AD 架構
- BindableObject 類別 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Bindable-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b702a26c61920f5a3868ccc479b1f8578a3075907b5dc5bc2eb9d070321c91d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118680778"
---
# <a name="ms-ds-bindable-object-class"></a>ms DS 可系結物件類別

代表可系結物件的輔助類別。 任何代表可用來系結至目錄之實體的使用者定義類別 (也就是使用者) ，都應該包含這個輔助類別。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | ms DS 可系結-物件                |
| Ldap-顯示名稱 | BindableObject                  |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| 架構識別碼-Guid    | 89f4a69f-4416-6b49-821d-6e3c4a0ff802 |



## <a name="implementations"></a>實作

-   [**亞當**](#adam-attributes)

## <a name="adam"></a>亞當

-   [屬性](#adam-attributes)



| 進入 | 值 |
|-----------------------------|--------------------------------------------------------------|
| System-Only                 | 否                                                        |
| Object-Category             | 3                                                            |
| 預設-物件-類別     | \-                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.244                                       |
| 預設值-隱藏-值        | 1                                                            |
| Rdn-Att-Id                  | \-                                                           |
| 的子類別                 | [**安全性-主體**](c-securityprincipal.md)<br/> |
| 可能的 Superiors          | \-                                                           |
| 輔助類別           | \-                                                           |
| NT-Security-描述元      | O:BAG：不正確： S：                                                 |
| 預設安全描述項 | \-                                                           |
| System-Flags                | 0x00000010                                                   |



## <a name="adam-attributes"></a>ADAM 屬性

此類別包含 ADAM 的下列屬性：



| 屬性                                                                                      | 強制性 | 衍生自                                                                                 |
|------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**帳戶-到期**](a-accountexpires.md)                                                    | 否     | **ms DS 可系結-物件**                                                                    |
| [**系統管理員-描述**](a-admindescription.md)                                                | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**系統管理員-顯示名稱**](a-admindisplayname.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**允許-屬性**](a-allowedattributes.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**允許-屬性-有效**](a-allowedattributeseffective.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**允許-子類別**](a-allowedchildclasses.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**允許-子類別-有效**](a-allowedchildclasseseffective.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**錯誤的密碼時間**](a-badpasswordtime.md)                                                 | 否     | **ms DS 可系結-物件**                                                                    |
| [**錯誤-Pwd-計數**](a-badpwdcount.md)                                                         | 否     | **ms DS 可系結-物件**                                                                    |
| [**橋頭-伺服器-清單-BL**](a-bridgeheadserverlistbl.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**標準名稱**](a-canonicalname.md)                                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**一般名稱**](a-cn.md)                                                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**建立時間戳記**](a-createtimestamp.md)                                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**描述**](a-description.md)                                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**顯示名稱**](a-displayname.md)                                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**DSA-簽章**](a-dsasignature.md)                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**DS-核心-傳播-資料**](a-dscorepropagationdata.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**從-進入**](a-fromentry.md)                                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**FSMO 角色-擁有者**](a-fsmoroleowner.md)                                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**實例類型**](a-instancetype.md)                                                        | 是      | [**返回頁首**](c-top.md)<br/>                                                              |
| [**為關鍵-系統物件**](a-iscriticalsystemobject.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**已刪除**](a-isdeleted.md)                                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**是-DL 的成員**](a-memberof.md)                                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**最後一個已知-父系**](a-lastknownparent.md)                                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**上次登入時間戳記**](a-lastlogontimestamp.md)                                           | 否     | **ms DS 可系結-物件**                                                                    |
| [**鎖定時間**](a-lockouttime.md)                                                          | 否     | **ms DS 可系結-物件**                                                                    |
| [**Managed 物件**](a-managedobjects.md)                                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**主要**](a-masteredby.md)                                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**修改時間戳記**](a-modifytimestamp.md)                                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms-DS-Immed-從屬**](a-msds-approx-immed-subordinates.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**MS DS-一致性-子計數**](a-ms-ds-consistencychildcount.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms-DS-停用-實例-BL**](a-msds-disableforinstancesbl.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms DS-主要-依據**](a-msds-masteredby.md)                                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms DS-NC-複寫-資料指標**](a-msds-ncreplcursors.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-複寫-輸入-相鄰**](a-msds-ncreplinboundneighbors.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms DS-NC-複寫-輸出-相鄰**](a-msds-ncreploutboundneighbors.md)                     | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms-DS-複寫-屬性中繼資料**](a-msds-replattributemetadata.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms-DS-複製-值中繼資料**](a-msds-replvaluemetadata.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms-DS-服務-帳戶-BL**](a-msds-serviceaccountbl.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms DS-使用者-帳戶-自動鎖定**](a-ms-ds-useraccountautolocked.md)                        | 否     | **ms DS 可系結-物件**                                                                    |
| [**ms-DS-使用者-帳戶-控制項計算**](a-msds-user-account-control-computed.md)            | 否     | **ms DS 可系結-物件**                                                                    |
| [**ms DS-使用者-帳戶-已停用**](a-msds-useraccountdisabled.md)                              | 否     | **ms DS 可系結-物件**                                                                    |
| [**ms DS-使用者不會過期-密碼**](a-msds-userdontexpirepassword.md)                       | 否     | **ms DS 可系結-物件**                                                                    |
| [**ms DS-使用者加密-文字-允許的密碼**](a-ms-ds-userencryptedtextpasswordallowed.md) | 否     | **ms DS 可系結-物件**                                                                    |
| [**ms-DS-使用者密碼-已過期**](a-msds-userpasswordexpired.md)                              | 否     | **ms DS 可系結-物件**                                                                    |
| [**ms-DS-使用者-密碼-非必要**](a-ms-ds-userpasswordnotrequired.md)                    | 否     | **ms DS 可系結-物件**                                                                    |
| [**Nt-Pwd-歷程記錄**](a-ntpwdhistory.md)                                                       | 否     | **ms DS 可系結-物件**                                                                    |
| [**NT-Security-描述元**](a-ntsecuritydescriptor.md)                                       | 是      | [**安全性-主體**](c-securityprincipal.md)<br/> [**返回頁首**](c-top.md)<br/> |
| [**Obj-Dist 名稱**](a-distinguishedname.md)                                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**物件-類別**](a-objectcategory.md)                                                    | 是      | [**返回頁首**](c-top.md)<br/>                                                              |
| [**物件類別**](a-objectclass.md)                                                          | 是      | [**返回頁首**](c-top.md)<br/>                                                              |
| [**物件-Guid**](a-objectguid.md)                                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**物件 Sid**](a-objectsid.md)                                                              | 是      | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**物件版本**](a-objectversion.md)                                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**其他知名物件**](a-otherwellknownobjects.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**部分屬性-刪除-清單**](a-partialattributedeletionlist.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**部分屬性集**](a-partialattributeset.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**可能-Inferiors**](a-possibleinferiors.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**Proxy-物件名稱**](a-proxiedobjectname.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**Proxy 位址**](a-proxyaddresses.md)                                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**Pwd-上次設定**](a-pwdlastset.md)                                                           | 否     | **ms DS 可系結-物件**                                                                    |
| [**查詢-原則-BL**](a-querypolicybl.md)                                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**複寫-屬性中繼資料**](a-replpropertymetadata.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**複寫-UpToDate-向量**](a-repluptodatevector.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**代表-來源**](a-repsfrom.md)                                                                | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**代表**](a-repsto.md)                                                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**修訂**](a-revision.md)                                                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**SD-Rights-有效**](a-sdrightseffective.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**伺服器參考-BL**](a-serverreferencebl.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**顯示-內建-僅限視圖**](a-showinadvancedviewonly.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**網站-物件-BL**](a-siteobjectbl.md)                                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**結構物件類別**](a-structuralobjectclass.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**子 Refs**](a-subrefs.md)                                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**補充認證**](a-supplementalcredentials.md)                                  | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**系統旗標**](a-systemflags.md)                                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**權杖群組**](a-tokengroups.md)                                                          | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**Unicode-Pwd**](a-unicodepwd.md)                                                            | 否     | **ms DS 可系結-物件**                                                                    |
| [**USN-已變更**](a-usnchanged.md)                                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-已建立**](a-usncreated.md)                                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-已移除-最後-Obj**](a-usndsalastobjremoved.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-站間**](a-usnintersite.md)                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-最後-Obj-Rem**](a-usnlastobjrem.md)                                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-來源**](a-usnsource.md)                                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**Wbem-路徑**](a-wbempath.md)                                                                | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**知名物件**](a-wellknownobjects.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**變更時**](a-whenchanged.md)                                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**建立時間**](a-whencreated.md)                                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**WWW-首頁**](a-wwwhomepage.md)                                                         | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**WWW-頁面-其他**](a-url.md)                                                                | 否     | [**返回頁首**](c-top.md)<br/>                                                              |



 

 





