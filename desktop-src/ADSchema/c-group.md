---
title: Group 類別
description: 儲存使用者名稱的清單。 用來將安全性主體套用至資源。
ms.assetid: e8ce5c43-d0fb-4c67-a6ef-7094fb7e7669
ms.tgt_platform: multiple
keywords:
- 群組類別 AD 架構
- 群組類別 AD 架構
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae33b53eff8305fee4698c5aed2bb072f3fa5b90a5922d0099e40e90f9b3fe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021906"
---
# <a name="group-class"></a>Group 類別

儲存使用者名稱的清單。 用來將安全性主體套用至資源。



| 進入 | 值 |
|-------------------|------------------------------------------------|
| CN                | Group                                          |
| Ldap-顯示名稱 | group                                          |
| 更新許可權  | 此值是由網域系統管理員所設定。 |
| 更新頻率  | \-                                             |
| 架構識別碼-Guid    | bf967a9c-0de6-11d0-a285-00aa003049e2           |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**亞當**](#adam-attributes)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [屬性](#windows-2000-server-attributes)
-   [擴充許可權](#windows-2000-server-extended-rights)
-   [驗證的寫入](#windows-2000-server-validated-writes)
-   [屬性集](#windows-2000-server-property-sets)



| 進入 | 值 |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | 否                                                                                                                                                                                               |
| Object-Category             | 1                                                                                                                                                                                                   |
| 預設-物件-類別     | \-                                                                                                                                                                                                  |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                |
| 預設值-隱藏-值        | 0                                                                                                                                                                                                   |
| Rdn-Att-Id                  | [**一般名稱**](a-cn.md)<br/>                                                                                                                                                              |
| 的子類別                 | [**返回頁首**](c-top.md)<br/>                                                                                                                                                                     |
| 可能的 Superiors          | [**網域 DNS**](c-domaindns.md)[**組織-單位**](c-organizationalunit.md)內 [**建-網域**](c-builtindomain.md)[**容器**](c-container.md)                                       |
| 輔助類別           | [**安全性-主體**](c-securityprincipal.md) (系統) [**Mail-收件**](c-mailrecipient.md) 者 (系統)                                                                                         |
| NT-Security-描述元      | O:BAG：不正確： S：                                                                                                                                                                                        |
| 預設安全描述項 | D： (;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;DA)  (;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)  (A;;RPLCLORC;;;AU)  (A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;AO)  (A;;RPLCLORC;;;PS)  (OA;;CR; ab721a55-1e2f-11d0-9819-00aa0040529b;;AU)  |
| System-Flags                | 0x00000010                                                                                                                                                                                          |



## <a name="windows-2000-server-attributes"></a>Windows 2000 伺服器屬性

此類別包含 Windows 2000 伺服器的下列屬性：



| 屬性                                                                    | 強制性 | 衍生自                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**帳戶-名稱-歷程記錄**](a-accountnamehistory.md)                         | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**系統管理員-計數**](a-admincount.md)                                          | 否     | **群組**                                                                                    |
| [**系統管理員-描述**](a-admindescription.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**系統管理員-顯示名稱**](a-admindisplayname.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**允許-屬性**](a-allowedattributes.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**允許-屬性-有效**](a-allowedattributeseffective.md)         | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**允許-子類別**](a-allowedchildclasses.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**允許-子類別-有效**](a-allowedchildclasseseffective.md)    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**Alt-Security-身分識別**](a-altsecurityidentities.md)                   | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**橋頭-伺服器-清單-BL**](a-bridgeheadserverlistbl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**標準名稱**](a-canonicalname.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**註解**](a-info.md)                                                    | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**一般名稱**](a-cn.md)                                                  | 是      | [**返回頁首**](c-top.md)<br/> [**郵件收件者**](c-mailrecipient.md)<br/>         |
| [**控制存取權**](a-controlaccessrights.md)                       | 否     | **群組**                                                                                    |
| [**建立時間戳記**](a-createtimestamp.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**描述**](a-description.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**桌面-設定檔**](a-desktopprofile.md)                                  | 否     | **群組**                                                                                    |
| [**顯示名稱**](a-displayname.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**顯示-名稱-可列印**](a-displaynameprintable.md)                     | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**DSA-簽章**](a-dsasignature.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**DS-核心-傳播-資料**](a-dscorepropagationdata.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**電子郵件地址**](a-mail.md)                                           | 否     | **群組**                                                                                    |
| [**副檔名-名稱**](a-extensionname.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**標誌**](a-flags.md)                                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**從-進入**](a-fromentry.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**Frs-電腦-參考-BL**](a-frscomputerreferencebl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**FRS-成員參考-BL**](a-frsmemberreferencebl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**FSMO 角色-擁有者**](a-fsmoroleowner.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**垃圾 Coll 期間**](a-garbagecollperiod.md)                           | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**群組-屬性**](a-groupattributes.md)                                | 否     | **群組**                                                                                    |
| [**群組-成員資格-SAM**](a-groupmembershipsam.md)                         | 否     | **群組**                                                                                    |
| [**群組類型**](a-grouptype.md)                                            | 是      | **群組**                                                                                    |
| [**實例類型**](a-instancetype.md)                                      | 是      | [**返回頁首**](c-top.md)<br/>                                                              |
| [**為關鍵-系統物件**](a-iscriticalsystemobject.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**已刪除**](a-isdeleted.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**是-DL 的成員**](a-memberof.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**是-許可權-持有者**](a-isprivilegeholder.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**最後一個已知-父系**](a-lastknownparent.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**舊版-Exchange-DN**](a-legacyexchangedn.md)                             | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**管理者**](a-managedby.md)                                            | 否     | **群組**                                                                                    |
| [**Managed 物件**](a-managedobjects.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**主要**](a-masteredby.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**成員**](a-member.md)                                                   | 否     | **群組**                                                                                    |
| [**修改時間戳記**](a-modifytimestamp.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**MS DS-一致性-子計數**](a-ms-ds-consistencychildcount.md)       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**非安全性成員**](a-nonsecuritymember.md)                           | 否     | **群組**                                                                                    |
| [**非安全性成員-BL**](a-nonsecuritymemberbl.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**NT 群組-成員**](a-ntgroupmembers.md)                                 | 否     | **群組**                                                                                    |
| [**NT-Security-描述元**](a-ntsecuritydescriptor.md)                     | 是      | [**返回頁首**](c-top.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/> |
| [**Obj-Dist 名稱**](a-distinguishedname.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**物件-類別**](a-objectcategory.md)                                  | 是      | [**返回頁首**](c-top.md)<br/>                                                              |
| [**物件類別**](a-objectclass.md)                                        | 是      | [**返回頁首**](c-top.md)<br/>                                                              |
| [**物件-Guid**](a-objectguid.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**物件 Sid**](a-objectsid.md)                                            | 是      | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**物件版本**](a-objectversion.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**運算子-計數**](a-operatorcount.md)                                    | 否     | **群組**                                                                                    |
| [**其他知名物件**](a-otherwellknownobjects.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**部分屬性-刪除-清單**](a-partialattributedeletionlist.md)    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**部分屬性集**](a-partialattributeset.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**可能-Inferiors**](a-possibleinferiors.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**主要群組-Token**](a-primarygrouptoken.md)                           | 否     | **群組**                                                                                    |
| [**Proxy-物件名稱**](a-proxiedobjectname.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**Proxy 位址**](a-proxyaddresses.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**查詢-原則-BL**](a-querypolicybl.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**複寫-屬性中繼資料**](a-replpropertymetadata.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**複寫-UpToDate-向量**](a-repluptodatevector.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**報表**](a-directreports.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**代表-來源**](a-repsfrom.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**代表**](a-repsto.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**修訂**](a-revision.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**擺脫**](a-rid.md)                                                         | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**SAM-帳戶-名稱**](a-samaccountname.md)                                 | 是      | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**SAM-帳戶-類型**](a-samaccounttype.md)                                 | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**SD-Rights-有效**](a-sdrightseffective.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**安全性-識別碼**](a-securityidentifier.md)                          | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**伺服器參考-BL**](a-serverreferencebl.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**顯示位址-書籍**](a-showinaddressbook.md)                          | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**顯示-內建-僅限視圖**](a-showinadvancedviewonly.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**SID-歷程記錄**](a-sidhistory.md)                                          | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**網站-物件-BL**](a-siteobjectbl.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**子 Refs**](a-subrefs.md)                                                | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**補充認證**](a-supplementalcredentials.md)                | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**系統旗標**](a-systemflags.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**電話號碼**](a-telephonenumber.md)                                | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**文字編碼或位址**](a-textencodedoraddress.md)                    | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**權杖群組**](a-tokengroups.md)                                        | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**權杖-群組-全域和通用**](a-tokengroupsglobalanduniversal.md) | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**權杖群組-無-GC-可接受**](a-tokengroupsnogcacceptable.md)         | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**使用者憑證**](a-usercert.md)                                              | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**使用者 SMIME-憑證**](a-usersmimecertificate.md)                     | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**USN-已變更**](a-usnchanged.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-已建立**](a-usncreated.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-已移除-最後-Obj**](a-usndsalastobjremoved.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-站間**](a-usnintersite.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-最後-Obj-Rem**](a-usnlastobjrem.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-來源**](a-usnsource.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**Wbem-路徑**](a-wbempath.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**知名物件**](a-wellknownobjects.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**變更時**](a-whenchanged.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**建立時間**](a-whencreated.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**WWW-首頁**](a-wwwhomepage.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**WWW-頁面-其他**](a-url.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**X509-Cert**](a-usercertificate.md)                                       | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-2000-server-extended-rights"></a>Windows 2000 伺服器擴充許可權

此類別包含 Windows 2000 伺服器的下列擴充許可權：



| 一般名稱                  |
|------------------------------|
| [**傳送至**](r-send-to.md) |



## <a name="windows-2000-server-validated-writes"></a>Windows 2000 伺服器驗證的寫入

此類別包含下列 Windows 2000 伺服器的已驗證寫入：



| 一般名稱                                  |
|----------------------------------------------|
| [**自我成員資格**](r-self-membership.md) |



## <a name="windows-2000-server-property-sets"></a>Windows 2000 伺服器屬性集

這個類別包含 Windows 2000 伺服器的下列屬性集：



| 一般名稱                                      |
|--------------------------------------------------|
| [**電子郵件-資訊**](r-email-information.md) |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [屬性](#windows-server-2003-attributes)
-   [擴充許可權](#windows-server-2003-extended-rights)
-   [驗證的寫入](#windows-server-2003-validated-writes)
-   [屬性集](#windows-server-2003-property-sets)



| 進入 | 值 |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | 否                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| 預設-物件-類別     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| 預設值-隱藏-值        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**一般名稱**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| 的子類別                 | [**返回頁首**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| 可能的 Superiors          | [**網域 DNS**](c-domaindns.md)[**組織單位**](c-organizationalunit.md)內 [**建-網域**](c-builtindomain.md)[**容器**](c-container.md)-[**ds-az-管理-管理員**](c-msds-azadminmanager.md)-ds-az-[**應用程式**](c-msds-azapplication.md)-[**ds-az-範圍**](c-msds-azscope.md) |
| 輔助類別           | [**安全性-主體**](c-securityprincipal.md) (系統) [**Mail-收件**](c-mailrecipient.md) 者 (系統)                                                                                                                                                                                                      |
| NT-Security-描述元      | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                     |
| 預設安全描述項 | D： (;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;DA)  (;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)  (A;;RPLCLORC;;;AU)  (A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;AO)  (A;;RPLCLORC;;;PS)  (OA;;CR; ab721a55-1e2f-11d0-9819-00aa0040529b;;AU)  (OA;;RP; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2;;S-1-5-32-560)                                                    |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-attributes"></a>Windows伺服器2003屬性

此類別包含 Windows Server 2003 的下列屬性：



| 屬性                                                                    | 強制性 | 衍生自                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**帳戶-名稱-歷程記錄**](a-accountnamehistory.md)                         | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**系統管理員-計數**](a-admincount.md)                                          | 否     | **群組**                                                                                    |
| [**系統管理員-描述**](a-admindescription.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**系統管理員-顯示名稱**](a-admindisplayname.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**允許-屬性**](a-allowedattributes.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**允許-屬性-有效**](a-allowedattributeseffective.md)         | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**允許-子類別**](a-allowedchildclasses.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**允許-子類別-有效**](a-allowedchildclasseseffective.md)    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**Alt-Security-身分識別**](a-altsecurityidentities.md)                   | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**橋頭-伺服器-清單-BL**](a-bridgeheadserverlistbl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**標準名稱**](a-canonicalname.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**註解**](a-info.md)                                                    | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**一般名稱**](a-cn.md)                                                  | 是      | [**返回頁首**](c-top.md)<br/> [**郵件收件者**](c-mailrecipient.md)<br/>         |
| [**控制存取權**](a-controlaccessrights.md)                       | 否     | **群組**                                                                                    |
| [**建立時間戳記**](a-createtimestamp.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**描述**](a-description.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**桌面-設定檔**](a-desktopprofile.md)                                  | 否     | **群組**                                                                                    |
| [**顯示名稱**](a-displayname.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**顯示-名稱-可列印**](a-displaynameprintable.md)                     | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**DSA-簽章**](a-dsasignature.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**DS-核心-傳播-資料**](a-dscorepropagationdata.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**電子郵件地址**](a-mail.md)                                           | 否     | **群組**                                                                                    |
| [**副檔名-名稱**](a-extensionname.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**標誌**](a-flags.md)                                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**從-進入**](a-fromentry.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**Frs-電腦-參考-BL**](a-frscomputerreferencebl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**FRS-成員參考-BL**](a-frsmemberreferencebl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**FSMO 角色-擁有者**](a-fsmoroleowner.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**垃圾 Coll 期間**](a-garbagecollperiod.md)                           | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**群組-屬性**](a-groupattributes.md)                                | 否     | **群組**                                                                                    |
| [**群組-成員資格-SAM**](a-groupmembershipsam.md)                         | 否     | **群組**                                                                                    |
| [**群組類型**](a-grouptype.md)                                            | 是      | **群組**                                                                                    |
| [**實例類型**](a-instancetype.md)                                      | 是      | [**返回頁首**](c-top.md)<br/>                                                              |
| [**為關鍵-系統物件**](a-iscriticalsystemobject.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**已刪除**](a-isdeleted.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**是-DL 的成員**](a-memberof.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**是-許可權-持有者**](a-isprivilegeholder.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**labeledURI**](a-labeleduri.md)                                           | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**最後一個已知-父系**](a-lastknownparent.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**舊版-Exchange-DN**](a-legacyexchangedn.md)                             | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**管理者**](a-managedby.md)                                            | 否     | **群組**                                                                                    |
| [**Managed 物件**](a-managedobjects.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**主要**](a-masteredby.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**成員**](a-member.md)                                                   | 否     | **群組**                                                                                    |
| [**修改時間戳記**](a-modifytimestamp.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**PartitionSetLink**](a-mscom-partitionsetlink.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**UserLink**](a-mscom-userlink.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms-DS-Immed-從屬**](a-msds-approx-immed-subordinates.md)  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms DS-Az-LDAP-查詢**](a-msds-azldapquery.md)                            | 否     | **群組**                                                                                    |
| [**MS DS-一致性-子計數**](a-ms-ds-consistencychildcount.md)       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**KeyVersionNumber**](a-msds-keyversionnumber.md)                    | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**ms DS-主要-依據**](a-msds-masteredby.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms DS-成員--Az-Role-BL**](a-msds-membersforazrolebl.md)            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms DS-NC-複寫-資料指標**](a-msds-ncreplcursors.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-複寫-輸入-相鄰**](a-msds-ncreplinboundneighbors.md)     | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms DS-NC-複寫-輸出-相鄰**](a-msds-ncreploutboundneighbors.md)   | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms DS-非成員**](a-msds-nonmembers.md)                               | 否     | **群組**                                                                                    |
| [**ms DS-非成員-BL**](a-msds-nonmembersbl.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**BL-------物件參考**](a-msds-objectreferencebl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**BL-------------------**](a-msds-operationsforazrolebl.md)      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**BL-------------工作-**](a-msds-operationsforaztaskbl.md)      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms-DS-複寫-屬性中繼資料**](a-msds-replattributemetadata.md)       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms-DS-複製-值中繼資料**](a-msds-replvaluemetadata.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms-chap---------BL**](a-msds-tasksforazrolebl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms DS-工作--Az-Task-BL**](a-msds-tasksforaztaskbl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**Ms-exch-assistant-name-助理-名稱**](a-msexchassistantname.md)                      | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**Ms-exch-assistant-name-LabeledURI**](a-msexchlabeleduri.md)                             | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**Ms-exch-assistant-name-擁有者-BL**](a-ownerbl.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**非安全性成員**](a-nonsecuritymember.md)                           | 否     | **群組**                                                                                    |
| [**非安全性成員-BL**](a-nonsecuritymemberbl.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**NT 群組-成員**](a-ntgroupmembers.md)                                 | 否     | **群組**                                                                                    |
| [**NT-Security-描述元**](a-ntsecuritydescriptor.md)                     | 是      | [**返回頁首**](c-top.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/> |
| [**Obj-Dist 名稱**](a-distinguishedname.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**物件-類別**](a-objectcategory.md)                                  | 是      | [**返回頁首**](c-top.md)<br/>                                                              |
| [**物件類別**](a-objectclass.md)                                        | 是      | [**返回頁首**](c-top.md)<br/>                                                              |
| [**物件-Guid**](a-objectguid.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**物件 Sid**](a-objectsid.md)                                            | 是      | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**物件版本**](a-objectversion.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**運算子-計數**](a-operatorcount.md)                                    | 否     | **群組**                                                                                    |
| [**其他知名物件**](a-otherwellknownobjects.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**部分屬性-刪除-清單**](a-partialattributedeletionlist.md)    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**部分屬性集**](a-partialattributeset.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**可能-Inferiors**](a-possibleinferiors.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**主要群組-Token**](a-primarygrouptoken.md)                           | 否     | **群組**                                                                                    |
| [**Proxy-物件名稱**](a-proxiedobjectname.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**Proxy 位址**](a-proxyaddresses.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**查詢-原則-BL**](a-querypolicybl.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**複寫-屬性中繼資料**](a-replpropertymetadata.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**複寫-UpToDate-向量**](a-repluptodatevector.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**報表**](a-directreports.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**代表-來源**](a-repsfrom.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**代表**](a-repsto.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**修訂**](a-revision.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**擺脫**](a-rid.md)                                                         | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**SAM-帳戶-名稱**](a-samaccountname.md)                                 | 是      | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**SAM-帳戶-類型**](a-samaccounttype.md)                                 | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**SD-Rights-有效**](a-sdrightseffective.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**secretary**](a-secretary.md)                                             | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**安全性-識別碼**](a-securityidentifier.md)                          | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**伺服器參考-BL**](a-serverreferencebl.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**顯示位址-書籍**](a-showinaddressbook.md)                          | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**顯示-內建-僅限視圖**](a-showinadvancedviewonly.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**SID-歷程記錄**](a-sidhistory.md)                                          | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**網站-物件-BL**](a-siteobjectbl.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**結構物件類別**](a-structuralobjectclass.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**子 Refs**](a-subrefs.md)                                                | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**補充認證**](a-supplementalcredentials.md)                | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**系統旗標**](a-systemflags.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**電話號碼**](a-telephonenumber.md)                                | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**文字編碼或位址**](a-textencodedoraddress.md)                    | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**權杖群組**](a-tokengroups.md)                                        | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**權杖-群組-全域和通用**](a-tokengroupsglobalanduniversal.md) | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**權杖群組-無-GC-可接受**](a-tokengroupsnogcacceptable.md)         | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**使用者憑證**](a-usercert.md)                                              | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**使用者 SMIME-憑證**](a-usersmimecertificate.md)                     | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |
| [**USN-已變更**](a-usnchanged.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-已建立**](a-usncreated.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-已移除-最後-Obj**](a-usndsalastobjremoved.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-站間**](a-usnintersite.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-最後-Obj-Rem**](a-usnlastobjrem.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-來源**](a-usnsource.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**Wbem-路徑**](a-wbempath.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**知名物件**](a-wellknownobjects.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**變更時**](a-whenchanged.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**建立時間**](a-whencreated.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**WWW-首頁**](a-wwwhomepage.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**WWW-頁面-其他**](a-url.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**X509-Cert**](a-usercertificate.md)                                       | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-server-2003-extended-rights"></a>Windows伺服器2003擴充許可權

此類別包含 Windows Server 2003 的下列擴充許可權：



| 一般名稱                  |
|------------------------------|
| [**傳送至**](r-send-to.md) |



## <a name="windows-server-2003-validated-writes"></a>Windows伺服器2003驗證的寫入

此類別包含下列 Windows Server 2003 的已驗證寫入：



| 一般名稱                                  |
|----------------------------------------------|
| [**自我成員資格**](r-self-membership.md) |



## <a name="windows-server-2003-property-sets"></a>WindowsServer 2003 屬性集

這個類別包含 Windows Server 2003 的下列屬性集：



| 一般名稱                                      |
|--------------------------------------------------|
| [**電子郵件-資訊**](r-email-information.md) |



## <a name="adam"></a>亞當

-   [屬性](#adam-attributes)
-   [驗證的寫入](#adam-validated-writes)
-   [屬性集](#adam-property-sets)



| 進入 | 值 |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------|
| System-Only                 | 否                                                                                                                |
| Object-Category             | 1                                                                                                                    |
| 預設-物件-類別     | \-                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                 |
| 預設值-隱藏-值        | 0                                                                                                                    |
| Rdn-Att-Id                  | [**一般名稱**](a-cn.md)<br/>                                                                               |
| 的子類別                 | [**返回頁首**](c-top.md)<br/>                                                                                      |
| 可能的 Superiors          | [**網域 DNS**](c-domaindns.md)[**組織單位**](c-organizationalunit.md)[**容器**](c-container.md) |
| 輔助類別           | [**安全性-主體**](c-securityprincipal.md) (系統)                                                            |
| NT-Security-描述元      | O:BAG：不正確： S：                                                                                                         |
| 預設安全描述項 | D:S:                                                                                                                 |
| System-Flags                | 0x00000010                                                                                                           |



## <a name="adam-attributes"></a>ADAM 屬性

此類別包含 ADAM 的下列屬性：



| 屬性                                                                   | 強制性 | 衍生自                                                                                 |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**系統管理員-描述**](a-admindescription.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**系統管理員-顯示名稱**](a-admindisplayname.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**允許-屬性**](a-allowedattributes.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**允許-屬性-有效**](a-allowedattributeseffective.md)        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**允許-子類別**](a-allowedchildclasses.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**允許-子類別-有效**](a-allowedchildclasseseffective.md)   | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**橋頭-伺服器-清單-BL**](a-bridgeheadserverlistbl.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**標準名稱**](a-canonicalname.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**一般名稱**](a-cn.md)                                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**建立時間戳記**](a-createtimestamp.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**描述**](a-description.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**桌面-設定檔**](a-desktopprofile.md)                                 | 否     | **群組**                                                                                    |
| [**顯示名稱**](a-displayname.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**DSA-簽章**](a-dsasignature.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**DS-核心-傳播-資料**](a-dscorepropagationdata.md)                 | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**從-進入**](a-fromentry.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**FSMO 角色-擁有者**](a-fsmoroleowner.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**群組類型**](a-grouptype.md)                                           | 是      | **群組**                                                                                    |
| [**實例類型**](a-instancetype.md)                                     | 是      | [**返回頁首**](c-top.md)<br/>                                                              |
| [**為關鍵-系統物件**](a-iscriticalsystemobject.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**已刪除**](a-isdeleted.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**是-DL 的成員**](a-memberof.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**最後一個已知-父系**](a-lastknownparent.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**管理者**](a-managedby.md)                                           | 否     | **群組**                                                                                    |
| [**Managed 物件**](a-managedobjects.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**主要**](a-masteredby.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**成員**](a-member.md)                                                  | 否     | **群組**                                                                                    |
| [**修改時間戳記**](a-modifytimestamp.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms-DS-Immed-從屬**](a-msds-approx-immed-subordinates.md) | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**MS DS-一致性-子計數**](a-ms-ds-consistencychildcount.md)      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms-DS-停用-實例-BL**](a-msds-disableforinstancesbl.md)      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms DS-主要-依據**](a-msds-masteredby.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms DS-NC-複寫-資料指標**](a-msds-ncreplcursors.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms-DS-NC-複寫-輸入-相鄰**](a-msds-ncreplinboundneighbors.md)    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms DS-NC-複寫-輸出-相鄰**](a-msds-ncreploutboundneighbors.md)  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms-DS-複寫-屬性中繼資料**](a-msds-replattributemetadata.md)      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms-DS-複製-值中繼資料**](a-msds-replvaluemetadata.md)              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**ms-DS-服務-帳戶-BL**](a-msds-serviceaccountbl.md)                 | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**NT-Security-描述元**](a-ntsecuritydescriptor.md)                    | 是      | [**返回頁首**](c-top.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/> |
| [**Obj-Dist 名稱**](a-distinguishedname.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**物件-類別**](a-objectcategory.md)                                 | 是      | [**返回頁首**](c-top.md)<br/>                                                              |
| [**物件類別**](a-objectclass.md)                                       | 是      | [**返回頁首**](c-top.md)<br/>                                                              |
| [**物件-Guid**](a-objectguid.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**物件 Sid**](a-objectsid.md)                                           | 是      | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**物件版本**](a-objectversion.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**其他知名物件**](a-otherwellknownobjects.md)                 | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**部分屬性-刪除-清單**](a-partialattributedeletionlist.md)   | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**部分屬性集**](a-partialattributeset.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**可能-Inferiors**](a-possibleinferiors.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**主要群組-Token**](a-primarygrouptoken.md)                          | 否     | **群組**                                                                                    |
| [**Proxy-物件名稱**](a-proxiedobjectname.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**Proxy 位址**](a-proxyaddresses.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**查詢-原則-BL**](a-querypolicybl.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**複寫-屬性中繼資料**](a-replpropertymetadata.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**複寫-UpToDate-向量**](a-repluptodatevector.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**代表-來源**](a-repsfrom.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**代表**](a-repsto.md)                                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**修訂**](a-revision.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**SD-Rights-有效**](a-sdrightseffective.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**伺服器參考-BL**](a-serverreferencebl.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**顯示-內建-僅限視圖**](a-showinadvancedviewonly.md)              | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**網站-物件-BL**](a-siteobjectbl.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**結構物件類別**](a-structuralobjectclass.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**子 Refs**](a-subrefs.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**補充認證**](a-supplementalcredentials.md)               | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**系統旗標**](a-systemflags.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**權杖群組**](a-tokengroups.md)                                       | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                 |
| [**USN-已變更**](a-usnchanged.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-已建立**](a-usncreated.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-已移除-最後-Obj**](a-usndsalastobjremoved.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-站間**](a-usnintersite.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-最後-Obj-Rem**](a-usnlastobjrem.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**USN-來源**](a-usnsource.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**Wbem-路徑**](a-wbempath.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**知名物件**](a-wellknownobjects.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**變更時**](a-whenchanged.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**建立時間**](a-whencreated.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**WWW-首頁**](a-wwwhomepage.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                              |
| [**WWW-頁面-其他**](a-url.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                                              |



## <a name="adam-validated-writes"></a>ADAM 驗證的寫入

此類別包含下列針對 ADAM 所驗證的寫入：



| 一般名稱                                  |
|----------------------------------------------|
| [**自我成員資格**](r-self-membership.md) |



## <a name="adam-property-sets"></a>ADAM 屬性集

這個類別包含下列 ADAM 的屬性集：



| 一般名稱                                      |
|--------------------------------------------------|
| [**電子郵件-資訊**](r-email-information.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [屬性](#windows-server-2003-r2-attributes)
-   [擴充許可權](#windows-server-2003-r2-extended-rights)
-   [驗證的寫入](#windows-server-2003-r2-validated-writes)
-   [屬性集](#windows-server-2003-r2-property-sets)



| 進入 | 值 |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | 否                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| 預設-物件-類別     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| 預設值-隱藏-值        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**一般名稱**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| 的子類別                 | [**返回頁首**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| 可能的 Superiors          | [**網域 DNS**](c-domaindns.md)[**組織單位**](c-organizationalunit.md)內 [**建-網域**](c-builtindomain.md)[**容器**](c-container.md)-[**ds-az-管理-管理員**](c-msds-azadminmanager.md)-ds-az-[**應用程式**](c-msds-azapplication.md)-[**ds-az-範圍**](c-msds-azscope.md) |
| 輔助類別           | [**posixGroup**](c-posixgroup.md)[**安全性-主體**](c-securityprincipal.md) (系統) [**Mail-收件**](c-mailrecipient.md) 者 (系統)                                                                                                                                                                    |
| NT-Security-描述元      | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                     |
| 預設安全描述項 | D： (;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;DA)  (;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)  (A;;RPLCLORC;;;AU)  (A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;AO)  (A;;RPLCLORC;;;PS)  (OA;;CR; ab721a55-1e2f-11d0-9819-00aa0040529b;;AU)  (OA;;RP; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2;;S-1-5-32-560)                                                    |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-r2-attributes"></a>WindowsServer 2003 R2 屬性

此類別包含 Windows Server 2003 R2 的下列屬性：



| 屬性                                                                    | 強制性 | 衍生自                                                                                                                       |
|------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**帳戶-名稱-歷程記錄**](a-accountnamehistory.md)                         | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**系統管理員-計數**](a-admincount.md)                                          | 否     | **群組**                                                                                                                          |
| [**系統管理員-描述**](a-admindescription.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**系統管理員-顯示名稱**](a-admindisplayname.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**允許-屬性**](a-allowedattributes.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**允許-屬性-有效**](a-allowedattributeseffective.md)         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**允許-子類別**](a-allowedchildclasses.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**允許-子類別-有效**](a-allowedchildclasseseffective.md)    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security-身分識別**](a-altsecurityidentities.md)                   | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**橋頭-伺服器-清單-BL**](a-bridgeheadserverlistbl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**標準名稱**](a-canonicalname.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**註解**](a-info.md)                                                    | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**一般名稱**](a-cn.md)                                                  | 是      | [**返回頁首**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**郵件收件者**](c-mailrecipient.md)<br/> |
| [**控制存取權**](a-controlaccessrights.md)                       | 否     | **群組**                                                                                                                          |
| [**建立時間戳記**](a-createtimestamp.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**描述**](a-description.md)                                         | 否     | [**返回頁首**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**桌面-設定檔**](a-desktopprofile.md)                                  | 否     | **群組**                                                                                                                          |
| [**顯示名稱**](a-displayname.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**顯示-名稱-可列印**](a-displaynameprintable.md)                     | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**DSA-簽章**](a-dsasignature.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**DS-核心-傳播-資料**](a-dscorepropagationdata.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**電子郵件地址**](a-mail.md)                                           | 否     | **群組**                                                                                                                          |
| [**副檔名-名稱**](a-extensionname.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**標誌**](a-flags.md)                                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**從-進入**](a-fromentry.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Frs-電腦-參考-BL**](a-frscomputerreferencebl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**FRS-成員參考-BL**](a-frsmemberreferencebl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**FSMO 角色-擁有者**](a-fsmoroleowner.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**垃圾 Coll 期間**](a-garbagecollperiod.md)                           | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                             | 否     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**群組-屬性**](a-groupattributes.md)                                | 否     | **群組**                                                                                                                          |
| [**群組-成員資格-SAM**](a-groupmembershipsam.md)                         | 否     | **群組**                                                                                                                          |
| [**群組類型**](a-grouptype.md)                                            | 是      | **群組**                                                                                                                          |
| [**實例類型**](a-instancetype.md)                                      | 是      | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**為關鍵-系統物件**](a-iscriticalsystemobject.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**已刪除**](a-isdeleted.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**是-DL 的成員**](a-memberof.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**是-許可權-持有者**](a-isprivilegeholder.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                           | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**最後一個已知-父系**](a-lastknownparent.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**舊版-Exchange-DN**](a-legacyexchangedn.md)                             | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**管理者**](a-managedby.md)                                            | 否     | **群組**                                                                                                                          |
| [**Managed 物件**](a-managedobjects.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**主要**](a-masteredby.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**成員**](a-member.md)                                                   | 否     | **群組**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                             | 否     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**修改時間戳記**](a-modifytimestamp.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**PartitionSetLink**](a-mscom-partitionsetlink.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**UserLink**](a-mscom-userlink.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Immed-從屬**](a-msds-approx-immed-subordinates.md)  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-Az-LDAP-查詢**](a-msds-azldapquery.md)                            | 否     | **群組**                                                                                                                          |
| [**MS DS-一致性-子計數**](a-ms-ds-consistencychildcount.md)       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**KeyVersionNumber**](a-msds-keyversionnumber.md)                    | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**ms DS-主要-依據**](a-msds-masteredby.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-成員--Az-Role-BL**](a-msds-membersforazrolebl.md)            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-NC-複寫-資料指標**](a-msds-ncreplcursors.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-複寫-輸入-相鄰**](a-msds-ncreplinboundneighbors.md)     | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-NC-複寫-輸出-相鄰**](a-msds-ncreploutboundneighbors.md)   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-非成員**](a-msds-nonmembers.md)                               | 否     | **群組**                                                                                                                          |
| [**ms DS-非成員-BL**](a-msds-nonmembersbl.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**BL-------物件參考**](a-msds-objectreferencebl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**BL-------------------**](a-msds-operationsforazrolebl.md)      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**BL-------------工作-**](a-msds-operationsforaztaskbl.md)      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-複寫-屬性中繼資料**](a-msds-replattributemetadata.md)       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-複製-值中繼資料**](a-msds-replvaluemetadata.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-chap---------BL**](a-msds-tasksforazrolebl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-工作--Az-Task-BL**](a-msds-tasksforaztaskbl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Ms-exch-assistant-name-助理-名稱**](a-msexchassistantname.md)                      | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**Ms-exch-assistant-name-LabeledURI**](a-msexchlabeleduri.md)                             | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**Ms-exch-assistant-name-擁有者-BL**](a-ownerbl.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-名稱**](a-mssfu30name.md)                                       | 否     | **群組**                                                                                                                          |
| [**msSFU-30-Nis-網域**](a-mssfu30nisdomain.md)                            | 否     | **群組**                                                                                                                          |
| [**msSFU-30-Posix-成員**](a-mssfu30posixmember.md)                        | 否     | **群組**                                                                                                                          |
| [**msSFU-30-Posix-成員**](a-mssfu30posixmemberof.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**非安全性成員**](a-nonsecuritymember.md)                           | 否     | **群組**                                                                                                                          |
| [**非安全性成員-BL**](a-nonsecuritymemberbl.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**NT 群組-成員**](a-ntgroupmembers.md)                                 | 否     | **群組**                                                                                                                          |
| [**NT-Security-描述元**](a-ntsecuritydescriptor.md)                     | 是      | [**返回頁首**](c-top.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist 名稱**](a-distinguishedname.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**物件-類別**](a-objectcategory.md)                                  | 是      | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**物件類別**](a-objectclass.md)                                        | 是      | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**物件-Guid**](a-objectguid.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**物件 Sid**](a-objectsid.md)                                            | 是      | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**物件版本**](a-objectversion.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**運算子-計數**](a-operatorcount.md)                                    | 否     | **群組**                                                                                                                          |
| [**其他知名物件**](a-otherwellknownobjects.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**部分屬性-刪除-清單**](a-partialattributedeletionlist.md)    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**部分屬性集**](a-partialattributeset.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**可能-Inferiors**](a-possibleinferiors.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**主要群組-Token**](a-primarygrouptoken.md)                           | 否     | **群組**                                                                                                                          |
| [**Proxy-物件名稱**](a-proxiedobjectname.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Proxy 位址**](a-proxyaddresses.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**查詢-原則-BL**](a-querypolicybl.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**複寫-屬性中繼資料**](a-replpropertymetadata.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**複寫-UpToDate-向量**](a-repluptodatevector.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**報表**](a-directreports.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**代表-來源**](a-repsfrom.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**代表**](a-repsto.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**修訂**](a-revision.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**擺脫**](a-rid.md)                                                         | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-帳戶-名稱**](a-samaccountname.md)                                 | 是      | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-帳戶-類型**](a-samaccounttype.md)                                 | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-有效**](a-sdrightseffective.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                             | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**安全性-識別碼**](a-securityidentifier.md)                          | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**伺服器參考-BL**](a-serverreferencebl.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**顯示位址-書籍**](a-showinaddressbook.md)                          | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**顯示-內建-僅限視圖**](a-showinadvancedviewonly.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**SID-歷程記錄**](a-sidhistory.md)                                          | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**網站-物件-BL**](a-siteobjectbl.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**結構物件類別**](a-structuralobjectclass.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**子 Refs**](a-subrefs.md)                                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**補充認證**](a-supplementalcredentials.md)                | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**系統旗標**](a-systemflags.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**電話號碼**](a-telephonenumber.md)                                | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**文字編碼或位址**](a-textencodedoraddress.md)                    | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**權杖群組**](a-tokengroups.md)                                        | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**權杖-群組-全域和通用**](a-tokengroupsglobalanduniversal.md) | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**權杖群組-無-GC-可接受**](a-tokengroupsnogcacceptable.md)         | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                               | 否     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**使用者憑證**](a-usercert.md)                                              | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**使用者-密碼**](a-userpassword.md)                                      | 否     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**使用者 SMIME-憑證**](a-usersmimecertificate.md)                     | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-已變更**](a-usnchanged.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-已建立**](a-usncreated.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-已移除-最後-Obj**](a-usndsalastobjremoved.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-站間**](a-usnintersite.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-最後-Obj-Rem**](a-usnlastobjrem.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-來源**](a-usnsource.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Wbem-路徑**](a-wbempath.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**知名物件**](a-wellknownobjects.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**變更時**](a-whenchanged.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**建立時間**](a-whencreated.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**WWW-首頁**](a-wwwhomepage.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**WWW-頁面-其他**](a-url.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**X509-Cert**](a-usercertificate.md)                                       | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2003-r2-extended-rights"></a>WindowsServer 2003 R2 擴充許可權

此類別包含 Windows Server 2003 R2 的下列擴充許可權：



| 一般名稱                  |
|------------------------------|
| [**傳送至**](r-send-to.md) |



## <a name="windows-server-2003-r2-validated-writes"></a>WindowsServer 2003 R2 驗證的寫入

此類別包含下列 Windows Server 2003 R2 的已驗證寫入：



| 一般名稱                                  |
|----------------------------------------------|
| [**自我成員資格**](r-self-membership.md) |



## <a name="windows-server-2003-r2-property-sets"></a>WindowsServer 2003 R2 屬性集

此類別包含 Windows Server 2003 R2 的下列屬性集：



| 一般名稱                                      |
|--------------------------------------------------|
| [**電子郵件-資訊**](r-email-information.md) |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [屬性](#windows-server-2008-attributes)
-   [擴充許可權](#windows-server-2008-extended-rights)
-   [驗證的寫入](#windows-server-2008-validated-writes)
-   [屬性集](#windows-server-2008-property-sets)



| 進入 | 值 |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | 否                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| 預設-物件-類別     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| 預設值-隱藏-值        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**一般名稱**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| 的子類別                 | [**返回頁首**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| 可能的 Superiors          | [**網域 DNS**](c-domaindns.md)[**組織單位**](c-organizationalunit.md)內 [**建-網域**](c-builtindomain.md)[**容器**](c-container.md)-[**ds-az-管理-管理員**](c-msds-azadminmanager.md)-ds-az-[**應用程式**](c-msds-azapplication.md)-[**ds-az-範圍**](c-msds-azscope.md) |
| 輔助類別           | [**posixGroup**](c-posixgroup.md)[**安全性-主體**](c-securityprincipal.md) (系統) [**Mail-收件**](c-mailrecipient.md) 者 (系統)                                                                                                                                                                    |
| NT-Security-描述元      | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                     |
| 預設安全描述項 | D： (;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;DA)  (;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)  (A;;RPLCLORC;;;AU)  (A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;AO)  (A;;RPLCLORC;;;PS)  (OA;;CR; ab721a55-1e2f-11d0-9819-00aa0040529b;;AU)  (OA;;RP; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2;;S-1-5-32-560)                                                    |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-attributes"></a>Windows伺服器2008屬性

此類別包含 Windows Server 2008 的下列屬性：



| 屬性                                                                        | 強制性 | 衍生自                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**帳戶-名稱-歷程記錄**](a-accountnamehistory.md)                             | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**系統管理員-計數**](a-admincount.md)                                              | 否     | **群組**                                                                                                                          |
| [**系統管理員-描述**](a-admindescription.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**系統管理員-顯示名稱**](a-admindisplayname.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**允許-屬性**](a-allowedattributes.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**允許-屬性-有效**](a-allowedattributeseffective.md)             | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**允許-子類別**](a-allowedchildclasses.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**允許-子類別-有效**](a-allowedchildclasseseffective.md)        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security-身分識別**](a-altsecurityidentities.md)                       | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**橋頭-伺服器-清單-BL**](a-bridgeheadserverlistbl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**標準名稱**](a-canonicalname.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**註解**](a-info.md)                                                        | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**一般名稱**](a-cn.md)                                                      | 是      | [**返回頁首**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**郵件收件者**](c-mailrecipient.md)<br/> |
| [**控制存取權**](a-controlaccessrights.md)                           | 否     | **群組**                                                                                                                          |
| [**建立時間戳記**](a-createtimestamp.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**描述**](a-description.md)                                             | 否     | [**返回頁首**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**桌面-設定檔**](a-desktopprofile.md)                                      | 否     | **群組**                                                                                                                          |
| [**顯示名稱**](a-displayname.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**顯示-名稱-可列印**](a-displaynameprintable.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**DSA-簽章**](a-dsasignature.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**DS-核心-傳播-資料**](a-dscorepropagationdata.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**電子郵件地址**](a-mail.md)                                               | 否     | **群組**                                                                                                                          |
| [**副檔名-名稱**](a-extensionname.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**標誌**](a-flags.md)                                                         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**從-進入**](a-fromentry.md)                                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Frs-電腦-參考-BL**](a-frscomputerreferencebl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**FRS-成員參考-BL**](a-frsmemberreferencebl.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**FSMO 角色-擁有者**](a-fsmoroleowner.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**垃圾 Coll 期間**](a-garbagecollperiod.md)                               | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | 否     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**群組-屬性**](a-groupattributes.md)                                    | 否     | **群組**                                                                                                                          |
| [**群組-成員資格-SAM**](a-groupmembershipsam.md)                             | 否     | **群組**                                                                                                                          |
| [**群組類型**](a-grouptype.md)                                                | 是      | **群組**                                                                                                                          |
| [**實例類型**](a-instancetype.md)                                          | 是      | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**為關鍵-系統物件**](a-iscriticalsystemobject.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**已刪除**](a-isdeleted.md)                                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**是-DL 的成員**](a-memberof.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**是-許可權-持有者**](a-isprivilegeholder.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                               | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**最後一個已知-父系**](a-lastknownparent.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**舊版-Exchange-DN**](a-legacyexchangedn.md)                                 | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**管理者**](a-managedby.md)                                                | 否     | **群組**                                                                                                                          |
| [**Managed 物件**](a-managedobjects.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**主要**](a-masteredby.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**成員**](a-member.md)                                                       | 否     | **群組**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                 | 否     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**修改時間戳記**](a-modifytimestamp.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**PartitionSetLink**](a-mscom-partitionsetlink.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**UserLink**](a-mscom-userlink.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Immed-從屬**](a-msds-approx-immed-subordinates.md)      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-Az-應用程式-資料**](a-msds-azapplicationdata.md)                    | 否     | **群組**                                                                                                                          |
| [**ms-chap-Az-Biz-Rule**](a-msds-azbizrule.md)                                    | 否     | **群組**                                                                                                                          |
| [**ms-chap-Az-Biz-Rule-Language**](a-msds-azbizrulelanguage.md)                   | 否     | **群組**                                                                                                                          |
| [**ms DS-Az-Generic-資料**](a-msds-azgenericdata.md)                            | 否     | **群組**                                                                                                                          |
| [**ms-chap-Az-最後匯入-Biz-規則-路徑**](a-msds-azlastimportedbizrulepath.md) | 否     | **群組**                                                                                                                          |
| [**ms DS-Az-LDAP-查詢**](a-msds-azldapquery.md)                                | 否     | **群組**                                                                                                                          |
| [**ms-DS-Az-Object-Guid**](a-msds-azobjectguid.md)                              | 否     | **群組**                                                                                                                          |
| [**MS DS-一致性-子計數**](a-ms-ds-consistencychildcount.md)           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                     | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-chap-為部分複本**](a-msds-ispartialreplicafor.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**KeyVersionNumber**](a-msds-keyversionnumber.md)                        | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-連結-BL**](a-msds-krbtgtlinkbl.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-主要-依據**](a-msds-masteredby.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-成員--Az-Role-BL**](a-msds-membersforazrolebl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-NC-複寫-資料指標**](a-msds-ncreplcursors.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-複寫-輸入-相鄰**](a-msds-ncreplinboundneighbors.md)         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-NC-複寫-輸出-相鄰**](a-msds-ncreploutboundneighbors.md)       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-NC-RO-複本-位置-BL**](a-msds-nc-ro-replica-locations-bl.md)    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC 類型**](a-msds-nctype.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-非成員**](a-msds-nonmembers.md)                                   | 否     | **群組**                                                                                                                          |
| [**ms DS-非成員-BL**](a-msds-nonmembersbl.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**BL-------物件參考**](a-msds-objectreferencebl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**BL-------------------**](a-msds-operationsforazrolebl.md)          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**BL-------------工作-**](a-msds-operationsforaztaskbl.md)          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-語音-顯示名稱**](a-msds-phoneticdisplayname.md)                | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-主體-名稱**](a-msds-principalname.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**PSO-已套用**](a-msds-psoapplied.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-複寫-屬性中繼資料**](a-msds-replattributemetadata.md)           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-複製-值中繼資料**](a-msds-replvaluemetadata.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-顯示的 Dsa**](a-msds-revealeddsas.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-chap---------BL**](a-msds-tasksforazrolebl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-工作--Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Ms-exch-assistant-name-助理-名稱**](a-msexchassistantname.md)                          | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**Ms-exch-assistant-name-LabeledURI**](a-msexchlabeleduri.md)                                 | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**Ms-exch-assistant-name-擁有者-BL**](a-ownerbl.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-名稱**](a-mssfu30name.md)                                           | 否     | **群組**                                                                                                                          |
| [**msSFU-30-Nis-網域**](a-mssfu30nisdomain.md)                                | 否     | **群組**                                                                                                                          |
| [**msSFU-30-Posix-成員**](a-mssfu30posixmember.md)                            | 否     | **群組**                                                                                                                          |
| [**msSFU-30-Posix-成員**](a-mssfu30posixmemberof.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**非安全性成員**](a-nonsecuritymember.md)                               | 否     | **群組**                                                                                                                          |
| [**非安全性成員-BL**](a-nonsecuritymemberbl.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**NT 群組-成員**](a-ntgroupmembers.md)                                     | 否     | **群組**                                                                                                                          |
| [**NT-Security-描述元**](a-ntsecuritydescriptor.md)                         | 是      | [**返回頁首**](c-top.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist 名稱**](a-distinguishedname.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**物件-類別**](a-objectcategory.md)                                      | 是      | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**物件類別**](a-objectclass.md)                                            | 是      | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**物件-Guid**](a-objectguid.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**物件 Sid**](a-objectsid.md)                                                | 是      | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**物件版本**](a-objectversion.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**運算子-計數**](a-operatorcount.md)                                        | 否     | **群組**                                                                                                                          |
| [**其他知名物件**](a-otherwellknownobjects.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**部分屬性-刪除-清單**](a-partialattributedeletionlist.md)        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**部分屬性集**](a-partialattributeset.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**可能-Inferiors**](a-possibleinferiors.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**主要群組-Token**](a-primarygrouptoken.md)                               | 否     | **群組**                                                                                                                          |
| [**Proxy-物件名稱**](a-proxiedobjectname.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Proxy 位址**](a-proxyaddresses.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**查詢-原則-BL**](a-querypolicybl.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**複寫-屬性中繼資料**](a-replpropertymetadata.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**複寫-UpToDate-向量**](a-repluptodatevector.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**報表**](a-directreports.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**代表-來源**](a-repsfrom.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**代表**](a-repsto.md)                                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**修訂**](a-revision.md)                                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**擺脫**](a-rid.md)                                                             | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-帳戶-名稱**](a-samaccountname.md)                                     | 是      | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-帳戶-類型**](a-samaccounttype.md)                                     | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-有效**](a-sdrightseffective.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                 | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**安全性-識別碼**](a-securityidentifier.md)                              | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**伺服器參考-BL**](a-serverreferencebl.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**顯示位址-書籍**](a-showinaddressbook.md)                              | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**顯示-內建-僅限視圖**](a-showinadvancedviewonly.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**SID-歷程記錄**](a-sidhistory.md)                                              | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**網站-物件-BL**](a-siteobjectbl.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**結構物件類別**](a-structuralobjectclass.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**子 Refs**](a-subrefs.md)                                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**補充認證**](a-supplementalcredentials.md)                    | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**系統旗標**](a-systemflags.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**電話號碼**](a-telephonenumber.md)                                    | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**文字編碼或位址**](a-textencodedoraddress.md)                        | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**權杖群組**](a-tokengroups.md)                                            | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**權杖-群組-全域和通用**](a-tokengroupsglobalanduniversal.md)     | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**權杖群組-無-GC-可接受**](a-tokengroupsnogcacceptable.md)             | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | 否     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**使用者憑證**](a-usercert.md)                                                  | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**使用者-密碼**](a-userpassword.md)                                          | 否     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**使用者 SMIME-憑證**](a-usersmimecertificate.md)                         | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-已變更**](a-usnchanged.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-已建立**](a-usncreated.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-已移除-最後-Obj**](a-usndsalastobjremoved.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-站間**](a-usnintersite.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-最後-Obj-Rem**](a-usnlastobjrem.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-來源**](a-usnsource.md)                                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Wbem-路徑**](a-wbempath.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**知名物件**](a-wellknownobjects.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**變更時**](a-whenchanged.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**建立時間**](a-whencreated.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**WWW-首頁**](a-wwwhomepage.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**WWW-頁面-其他**](a-url.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**X509-Cert**](a-usercertificate.md)                                           | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-extended-rights"></a>Windows伺服器2008擴充許可權

此類別包含 Windows Server 2008 的下列擴充許可權：



| 一般名稱                  |
|------------------------------|
| [**傳送至**](r-send-to.md) |



## <a name="windows-server-2008-validated-writes"></a>Windows伺服器2008驗證的寫入

此類別包含下列 Windows Server 2008 的已驗證寫入：



| 一般名稱                                  |
|----------------------------------------------|
| [**自我成員資格**](r-self-membership.md) |



## <a name="windows-server-2008-property-sets"></a>WindowsServer 2008 屬性集

這個類別包含 Windows Server 2008 的下列屬性集：



| 一般名稱                                      |
|--------------------------------------------------|
| [**電子郵件-資訊**](r-email-information.md) |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [屬性](#windows-server-2008-r2-attributes)
-   [擴充許可權](#windows-server-2008-r2-extended-rights)
-   [驗證的寫入](#windows-server-2008-r2-validated-writes)
-   [屬性集](#windows-server-2008-r2-property-sets)



| 進入 | 值 |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | 否                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| 預設-物件-類別     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| 預設值-隱藏-值        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**一般名稱**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| 的子類別                 | [**返回頁首**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| 可能的 Superiors          | [**網域 DNS**](c-domaindns.md)[**組織單位**](c-organizationalunit.md)內 [**建-網域**](c-builtindomain.md)[**容器**](c-container.md)-[**ds-az-管理-管理員**](c-msds-azadminmanager.md)-ds-az-[**應用程式**](c-msds-azapplication.md)-[**ds-az-範圍**](c-msds-azscope.md) |
| 輔助類別           | [**posixGroup**](c-posixgroup.md)[**安全性-主體**](c-securityprincipal.md) (系統) [**Mail-收件**](c-mailrecipient.md) 者 (系統)                                                                                                                                                                    |
| NT-Security-描述元      | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                     |
| 預設安全描述項 | D： (;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;DA)  (;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)  (A;;RPLCLORC;;;AU)  (A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;AO)  (A;;RPLCLORC;;;PS)  (OA;;CR; ab721a55-1e2f-11d0-9819-00aa0040529b;;AU)  (OA;;RP; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2;;S-1-5-32-560)                                                    |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-r2-attributes"></a>WindowsServer 2008 R2 屬性

此類別包含 Windows Server 2008 R2 的下列屬性：



| 屬性                                                                        | 強制性 | 衍生自                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**帳戶-名稱-歷程記錄**](a-accountnamehistory.md)                             | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**系統管理員-計數**](a-admincount.md)                                              | 否     | **群組**                                                                                                                          |
| [**系統管理員-描述**](a-admindescription.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**系統管理員-顯示名稱**](a-admindisplayname.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**允許-屬性**](a-allowedattributes.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**允許-屬性-有效**](a-allowedattributeseffective.md)             | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**允許-子類別**](a-allowedchildclasses.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**允許-子類別-有效**](a-allowedchildclasseseffective.md)        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security-身分識別**](a-altsecurityidentities.md)                       | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**橋頭-伺服器-清單-BL**](a-bridgeheadserverlistbl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**標準名稱**](a-canonicalname.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**註解**](a-info.md)                                                        | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**一般名稱**](a-cn.md)                                                      | 是      | [**返回頁首**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**郵件收件者**](c-mailrecipient.md)<br/> |
| [**控制存取權**](a-controlaccessrights.md)                           | 否     | **群組**                                                                                                                          |
| [**建立時間戳記**](a-createtimestamp.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**描述**](a-description.md)                                             | 否     | [**返回頁首**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**桌面-設定檔**](a-desktopprofile.md)                                      | 否     | **群組**                                                                                                                          |
| [**顯示名稱**](a-displayname.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**顯示-名稱-可列印**](a-displaynameprintable.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**DSA-簽章**](a-dsasignature.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**DS-核心-傳播-資料**](a-dscorepropagationdata.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**電子郵件地址**](a-mail.md)                                               | 否     | **群組**                                                                                                                          |
| [**副檔名-名稱**](a-extensionname.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**標誌**](a-flags.md)                                                         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**從-進入**](a-fromentry.md)                                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Frs-電腦-參考-BL**](a-frscomputerreferencebl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**FRS-成員參考-BL**](a-frsmemberreferencebl.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**FSMO 角色-擁有者**](a-fsmoroleowner.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**垃圾 Coll 期間**](a-garbagecollperiod.md)                               | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | 否     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**群組-屬性**](a-groupattributes.md)                                    | 否     | **群組**                                                                                                                          |
| [**群組-成員資格-SAM**](a-groupmembershipsam.md)                             | 否     | **群組**                                                                                                                          |
| [**群組類型**](a-grouptype.md)                                                | 是      | **群組**                                                                                                                          |
| [**實例類型**](a-instancetype.md)                                          | 是      | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**為關鍵-系統物件**](a-iscriticalsystemobject.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**已刪除**](a-isdeleted.md)                                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**是-DL 的成員**](a-memberof.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**是-許可權-持有者**](a-isprivilegeholder.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**已回收**](a-isrecycled.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                               | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**最後一個已知-父系**](a-lastknownparent.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**舊版-Exchange-DN**](a-legacyexchangedn.md)                                 | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**管理者**](a-managedby.md)                                                | 否     | **群組**                                                                                                                          |
| [**Managed 物件**](a-managedobjects.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**主要**](a-masteredby.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**成員**](a-member.md)                                                       | 否     | **群組**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                 | 否     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**修改時間戳記**](a-modifytimestamp.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**PartitionSetLink**](a-mscom-partitionsetlink.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**UserLink**](a-mscom-userlink.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Immed-從屬**](a-msds-approx-immed-subordinates.md)      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-Az-應用程式-資料**](a-msds-azapplicationdata.md)                    | 否     | **群組**                                                                                                                          |
| [**ms-chap-Az-Biz-Rule**](a-msds-azbizrule.md)                                    | 否     | **群組**                                                                                                                          |
| [**ms-chap-Az-Biz-Rule-Language**](a-msds-azbizrulelanguage.md)                   | 否     | **群組**                                                                                                                          |
| [**ms DS-Az-Generic-資料**](a-msds-azgenericdata.md)                            | 否     | **群組**                                                                                                                          |
| [**ms-chap-Az-最後匯入-Biz-規則-路徑**](a-msds-azlastimportedbizrulepath.md) | 否     | **群組**                                                                                                                          |
| [**ms DS-Az-LDAP-查詢**](a-msds-azldapquery.md)                                | 否     | **群組**                                                                                                                          |
| [**ms-DS-Az-Object-Guid**](a-msds-azobjectguid.md)                              | 否     | **群組**                                                                                                                          |
| [**MS DS-一致性-子計數**](a-ms-ds-consistencychildcount.md)           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**啟用 ms DS-功能-BL**](a-msds-enabledfeaturebl.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-服務-帳戶-BL**](a-msds-hostserviceaccountbl.md)             | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                     | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-chap-為部分複本**](a-msds-ispartialreplicafor.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**KeyVersionNumber**](a-msds-keyversionnumber.md)                        | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-連結-BL**](a-msds-krbtgtlinkbl.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-最近-RDN**](a-msds-lastknownrdn.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-本機有效-刪除時間**](a-msds-localeffectivedeletiontime.md) | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-本機有效-回收時間**](a-msds-localeffectiverecycletime.md)   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-主要-依據**](a-msds-masteredby.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-成員--Az-Role-BL**](a-msds-membersforazrolebl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-NC-複寫-資料指標**](a-msds-ncreplcursors.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-複寫-輸入-相鄰**](a-msds-ncreplinboundneighbors.md)         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-NC-複寫-輸出-相鄰**](a-msds-ncreploutboundneighbors.md)       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-NC-RO-複本-位置-BL**](a-msds-nc-ro-replica-locations-bl.md)    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC 類型**](a-msds-nctype.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-非成員**](a-msds-nonmembers.md)                                   | 否     | **群組**                                                                                                                          |
| [**ms DS-非成員-BL**](a-msds-nonmembersbl.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**BL-------物件參考**](a-msds-objectreferencebl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**OIDToGroup-連結-BL**](a-msds-oidtogrouplinkbl.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**BL-------------------**](a-msds-operationsforazrolebl.md)          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**BL-------------工作-**](a-msds-operationsforaztaskbl.md)          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-語音-顯示名稱**](a-msds-phoneticdisplayname.md)                | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-主體-名稱**](a-msds-principalname.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**PSO-已套用**](a-msds-psoapplied.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-複寫-屬性中繼資料**](a-msds-replattributemetadata.md)           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-複製-值中繼資料**](a-msds-replvaluemetadata.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-顯示的 Dsa**](a-msds-revealeddsas.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-chap---------BL**](a-msds-tasksforazrolebl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-工作--Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Ms-exch-assistant-name-助理-名稱**](a-msexchassistantname.md)                          | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**Ms-exch-assistant-name-LabeledURI**](a-msexchlabeleduri.md)                                 | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**Ms-exch-assistant-name-擁有者-BL**](a-ownerbl.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-名稱**](a-mssfu30name.md)                                           | 否     | **群組**                                                                                                                          |
| [**msSFU-30-Nis-網域**](a-mssfu30nisdomain.md)                                | 否     | **群組**                                                                                                                          |
| [**msSFU-30-Posix-成員**](a-mssfu30posixmember.md)                            | 否     | **群組**                                                                                                                          |
| [**msSFU-30-Posix-成員**](a-mssfu30posixmemberof.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**非安全性成員**](a-nonsecuritymember.md)                               | 否     | **群組**                                                                                                                          |
| [**非安全性成員-BL**](a-nonsecuritymemberbl.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**NT 群組-成員**](a-ntgroupmembers.md)                                     | 否     | **群組**                                                                                                                          |
| [**NT-Security-描述元**](a-ntsecuritydescriptor.md)                         | 是      | [**返回頁首**](c-top.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist 名稱**](a-distinguishedname.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**物件-類別**](a-objectcategory.md)                                      | 是      | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**物件類別**](a-objectclass.md)                                            | 是      | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**物件-Guid**](a-objectguid.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**物件 Sid**](a-objectsid.md)                                                | 是      | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**物件版本**](a-objectversion.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**運算子-計數**](a-operatorcount.md)                                        | 否     | **群組**                                                                                                                          |
| [**其他知名物件**](a-otherwellknownobjects.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**部分屬性-刪除-清單**](a-partialattributedeletionlist.md)        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**部分屬性集**](a-partialattributeset.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**可能-Inferiors**](a-possibleinferiors.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**主要群組-Token**](a-primarygrouptoken.md)                               | 否     | **群組**                                                                                                                          |
| [**Proxy-物件名稱**](a-proxiedobjectname.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Proxy 位址**](a-proxyaddresses.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**查詢-原則-BL**](a-querypolicybl.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**複寫-屬性中繼資料**](a-replpropertymetadata.md)                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**複寫-UpToDate-向量**](a-repluptodatevector.md)                             | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**報表**](a-directreports.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**代表-來源**](a-repsfrom.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**代表**](a-repsto.md)                                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**修訂**](a-revision.md)                                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**擺脫**](a-rid.md)                                                             | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-帳戶-名稱**](a-samaccountname.md)                                     | 是      | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-帳戶-類型**](a-samaccounttype.md)                                     | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-有效**](a-sdrightseffective.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                 | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**安全性-識別碼**](a-securityidentifier.md)                              | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**伺服器參考-BL**](a-serverreferencebl.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**顯示位址-書籍**](a-showinaddressbook.md)                              | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**顯示-內建-僅限視圖**](a-showinadvancedviewonly.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**SID-歷程記錄**](a-sidhistory.md)                                              | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**網站-物件-BL**](a-siteobjectbl.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**結構物件類別**](a-structuralobjectclass.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**子 Refs**](a-subrefs.md)                                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**補充認證**](a-supplementalcredentials.md)                    | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**系統旗標**](a-systemflags.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**電話號碼**](a-telephonenumber.md)                                    | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**文字編碼或位址**](a-textencodedoraddress.md)                        | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**權杖群組**](a-tokengroups.md)                                            | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**權杖-群組-全域和通用**](a-tokengroupsglobalanduniversal.md)     | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**權杖群組-無-GC-可接受**](a-tokengroupsnogcacceptable.md)             | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | 否     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**使用者憑證**](a-usercert.md)                                                  | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**使用者-密碼**](a-userpassword.md)                                          | 否     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**使用者 SMIME-憑證**](a-usersmimecertificate.md)                         | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-已變更**](a-usnchanged.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-已建立**](a-usncreated.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-已移除-最後-Obj**](a-usndsalastobjremoved.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-站間**](a-usnintersite.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-最後-Obj-Rem**](a-usnlastobjrem.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-來源**](a-usnsource.md)                                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Wbem-路徑**](a-wbempath.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**知名物件**](a-wellknownobjects.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**變更時**](a-whenchanged.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**建立時間**](a-whencreated.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**WWW-首頁**](a-wwwhomepage.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**WWW-頁面-其他**](a-url.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**X509-Cert**](a-usercertificate.md)                                           | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-r2-extended-rights"></a>WindowsServer 2008 R2 擴充許可權

此類別包含 Windows Server 2008 R2 的下列擴充許可權：



| 一般名稱                  |
|------------------------------|
| [**傳送至**](r-send-to.md) |



## <a name="windows-server-2008-r2-validated-writes"></a>WindowsServer 2008 R2 驗證的寫入

此類別包含下列 Windows Server 2008 R2 的已驗證寫入：



| 一般名稱                                  |
|----------------------------------------------|
| [**自我成員資格**](r-self-membership.md) |



## <a name="windows-server-2008-r2-property-sets"></a>WindowsServer 2008 R2 屬性集

此類別包含 Windows Server 2008 R2 的下列屬性集：



| 一般名稱                                      |
|--------------------------------------------------|
| [**電子郵件-資訊**](r-email-information.md) |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [屬性](#windows-server-2012-attributes)
-   [擴充許可權](#windows-server-2012-extended-rights)
-   [驗證的寫入](#windows-server-2012-validated-writes)
-   [屬性集](#windows-server-2012-property-sets)



| 進入 | 值 |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | 否                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| 預設-物件-類別     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| 預設值-隱藏-值        | 0                                                                                                                                                                                                                                                                                                                |
| Rdn-Att-Id                  | [**一般名稱**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| 的子類別                 | [**返回頁首**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| 可能的 Superiors          | [**網域 DNS**](c-domaindns.md)[**組織單位**](c-organizationalunit.md)內 [**建-網域**](c-builtindomain.md)[**容器**](c-container.md)-[**ds-az-管理-管理員**](c-msds-azadminmanager.md)-ds-az-[**應用程式**](c-msds-azapplication.md)-[**ds-az-範圍**](c-msds-azscope.md) |
| 輔助類別           | [**posixGroup**](c-posixgroup.md)[**安全性-主體**](c-securityprincipal.md) (系統) [**Mail-收件**](c-mailrecipient.md) 者 (系統)                                                                                                                                                                    |
| NT-Security-描述元      | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                     |
| 預設安全描述項 | D： (;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;DA)  (;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)  (A;;RPLCLORC;;;AU)  (A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;AO)  (A;;RPLCLORC;;;PS)  (OA;;CR; ab721a55-1e2f-11d0-9819-00aa0040529b;;AU)  (OA;;RP; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2;;S-1-5-32-560)                                                    |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012屬性

這個類別包含 Windows Server 2012 的下列屬性：



| 屬性                                                                                    | 強制性 | 衍生自                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**帳戶-名稱-歷程記錄**](a-accountnamehistory.md)                                         | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**系統管理員-計數**](a-admincount.md)                                                          | 否     | **群組**                                                                                                                          |
| [**系統管理員-描述**](a-admindescription.md)                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**系統管理員-顯示名稱**](a-admindisplayname.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**允許-屬性**](a-allowedattributes.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**允許-屬性-有效**](a-allowedattributeseffective.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**允許-子類別**](a-allowedchildclasses.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**允許-子類別-有效**](a-allowedchildclasseseffective.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security-身分識別**](a-altsecurityidentities.md)                                   | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**橋頭-伺服器-清單-BL**](a-bridgeheadserverlistbl.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**標準名稱**](a-canonicalname.md)                                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**註解**](a-info.md)                                                                    | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**一般名稱**](a-cn.md)                                                                  | 是      | [**返回頁首**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**郵件收件者**](c-mailrecipient.md)<br/> |
| [**控制存取權**](a-controlaccessrights.md)                                       | 否     | **群組**                                                                                                                          |
| [**建立時間戳記**](a-createtimestamp.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**描述**](a-description.md)                                                         | 否     | [**返回頁首**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**桌面-設定檔**](a-desktopprofile.md)                                                  | 否     | **群組**                                                                                                                          |
| [**顯示名稱**](a-displayname.md)                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**顯示-名稱-可列印**](a-displaynameprintable.md)                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**DSA-簽章**](a-dsasignature.md)                                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**DS-核心-傳播-資料**](a-dscorepropagationdata.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**電子郵件地址**](a-mail.md)                                                           | 否     | **群組**                                                                                                                          |
| [**副檔名-名稱**](a-extensionname.md)                                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**標誌**](a-flags.md)                                                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**從-進入**](a-fromentry.md)                                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Frs-電腦-參考-BL**](a-frscomputerreferencebl.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**FRS-成員參考-BL**](a-frsmemberreferencebl.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**FSMO 角色-擁有者**](a-fsmoroleowner.md)                                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**垃圾 Coll 期間**](a-garbagecollperiod.md)                                           | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                             | 否     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**群組-屬性**](a-groupattributes.md)                                                | 否     | **群組**                                                                                                                          |
| [**群組-成員資格-SAM**](a-groupmembershipsam.md)                                         | 否     | **群組**                                                                                                                          |
| [**群組類型**](a-grouptype.md)                                                            | 是      | **群組**                                                                                                                          |
| [**實例類型**](a-instancetype.md)                                                      | 是      | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**為關鍵-系統物件**](a-iscriticalsystemobject.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**已刪除**](a-isdeleted.md)                                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**是-DL 的成員**](a-memberof.md)                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**是-許可權-持有者**](a-isprivilegeholder.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**已回收**](a-isrecycled.md)                                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                                           | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**最後一個已知-父系**](a-lastknownparent.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**舊版-Exchange-DN**](a-legacyexchangedn.md)                                             | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**管理者**](a-managedby.md)                                                            | 否     | **群組**                                                                                                                          |
| [**Managed 物件**](a-managedobjects.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**主要**](a-masteredby.md)                                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**成員**](a-member.md)                                                                   | 否     | **群組**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                             | 否     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**修改時間戳記**](a-modifytimestamp.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**UserLink**](a-mscom-userlink.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Immed-從屬**](a-msds-approx-immed-subordinates.md)                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-Az-應用程式-資料**](a-msds-azapplicationdata.md)                                | 否     | **群組**                                                                                                                          |
| [**ms-chap-Az-Biz-Rule**](a-msds-azbizrule.md)                                                | 否     | **群組**                                                                                                                          |
| [**ms-chap-Az-Biz-Rule-Language**](a-msds-azbizrulelanguage.md)                               | 否     | **群組**                                                                                                                          |
| [**ms DS-Az-Generic-資料**](a-msds-azgenericdata.md)                                        | 否     | **群組**                                                                                                                          |
| [**ms-chap-Az-最後匯入-Biz-規則-路徑**](a-msds-azlastimportedbizrulepath.md)             | 否     | **群組**                                                                                                                          |
| [**ms DS-Az-LDAP-查詢**](a-msds-azldapquery.md)                                            | 否     | **群組**                                                                                                                          |
| [**ms-DS-Az-Object-Guid**](a-msds-azobjectguid.md)                                          | 否     | **群組**                                                                                                                          |
| [**ms-chap--------可能-值-BL**](a-msds-claimsharespossiblevalueswithbl.md) | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**MS DS-一致性-子計數**](a-ms-ds-consistencychildcount.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**啟用 ms DS-功能-BL**](a-msds-enabledfeaturebl.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**GeoCoordinates-海拔**](a-msds-geocoordinatesaltitude.md)                       | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**GeoCoordinates-緯度**](a-msds-geocoordinateslatitude.md)                       | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**GeoCoordinates-經度**](a-msds-geocoordinateslongitude.md)                     | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-服務-帳戶-BL**](a-msds-hostserviceaccountbl.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-chap-為部分複本**](a-msds-ispartialreplicafor.md)                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-chap---主要電腦-**](a-msds-isprimarycomputerfor.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**KeyVersionNumber**](a-msds-keyversionnumber.md)                                    | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-連結-BL**](a-msds-krbtgtlinkbl.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-最近-RDN**](a-msds-lastknownrdn.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-本機有效-刪除時間**](a-msds-localeffectivedeletiontime.md)             | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-本機有效-回收時間**](a-msds-localeffectiverecycletime.md)               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-主要-依據**](a-msds-masteredby.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-成員--Az-Role-BL**](a-msds-membersforazrolebl.md)                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-chap-資源--BL 的成員**](a-msds-membersofresourcepropertylistbl.md) | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-NC-複寫-資料指標**](a-msds-ncreplcursors.md)                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-複寫-輸入-相鄰**](a-msds-ncreplinboundneighbors.md)                     | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-NC-複寫-輸出-相鄰**](a-msds-ncreploutboundneighbors.md)                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-NC-RO-複本-位置-BL**](a-msds-nc-ro-replica-locations-bl.md)                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC 類型**](a-msds-nctype.md)                                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-非成員**](a-msds-nonmembers.md)                                               | 否     | **群組**                                                                                                                          |
| [**ms DS-非成員-BL**](a-msds-nonmembersbl.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**BL-------物件參考**](a-msds-objectreferencebl.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**OIDToGroup-連結-BL**](a-msds-oidtogrouplinkbl.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**BL-------------------**](a-msds-operationsforazrolebl.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**BL-------------工作-**](a-msds-operationsforaztaskbl.md)                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-語音-顯示名稱**](a-msds-phoneticdisplayname.md)                            | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-主要電腦**](a-msds-primarycomputer.md)                                     | 否     | **群組**                                                                                                                          |
| [**ms-DS-主體-名稱**](a-msds-principalname.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**PSO-已套用**](a-msds-psoapplied.md)                                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-複寫-屬性中繼資料**](a-msds-replattributemetadata.md)                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-複製-值中繼資料**](a-msds-replvaluemetadata.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-顯示的 Dsa**](a-msds-revealeddsas.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-chap---------BL**](a-msds-tasksforazrolebl.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms DS-工作--Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-chap-Egress-BL**](a-msds-tdoegressbl.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-TDO-輸入-BL**](a-msds-tdoingressbl.md)                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**ms-chap-------Reference-BL**](a-msds-valuetypereferencebl.md)                         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Ms-exch-assistant-name-助理-名稱**](a-msexchassistantname.md)                                      | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**Ms-exch-assistant-name-LabeledURI**](a-msexchlabeleduri.md)                                             | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**Ms-exch-assistant-name-擁有者-BL**](a-ownerbl.md)                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-名稱**](a-mssfu30name.md)                                                       | 否     | **群組**                                                                                                                          |
| [**msSFU-30-Nis-網域**](a-mssfu30nisdomain.md)                                            | 否     | **群組**                                                                                                                          |
| [**msSFU-30-Posix-成員**](a-mssfu30posixmember.md)                                        | 否     | **群組**                                                                                                                          |
| [**msSFU-30-Posix-成員**](a-mssfu30posixmemberof.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**非安全性成員**](a-nonsecuritymember.md)                                           | 否     | **群組**                                                                                                                          |
| [**非安全性成員-BL**](a-nonsecuritymemberbl.md)                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**NT 群組-成員**](a-ntgroupmembers.md)                                                 | 否     | **群組**                                                                                                                          |
| [**NT-Security-描述元**](a-ntsecuritydescriptor.md)                                     | 是      | [**返回頁首**](c-top.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist 名稱**](a-distinguishedname.md)                                                 | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**物件-類別**](a-objectcategory.md)                                                  | 是      | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**物件類別**](a-objectclass.md)                                                        | 是      | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**物件-Guid**](a-objectguid.md)                                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**物件 Sid**](a-objectsid.md)                                                            | 是      | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**物件版本**](a-objectversion.md)                                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**運算子-計數**](a-operatorcount.md)                                                    | 否     | **群組**                                                                                                                          |
| [**其他知名物件**](a-otherwellknownobjects.md)                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**部分屬性-刪除-清單**](a-partialattributedeletionlist.md)                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**部分屬性集**](a-partialattributeset.md)                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**可能-Inferiors**](a-possibleinferiors.md)                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**主要群組-Token**](a-primarygrouptoken.md)                                           | 否     | **群組**                                                                                                                          |
| [**Proxy-物件名稱**](a-proxiedobjectname.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Proxy 位址**](a-proxyaddresses.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**查詢-原則-BL**](a-querypolicybl.md)                                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**複寫-屬性中繼資料**](a-replpropertymetadata.md)                                    | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**複寫-UpToDate-向量**](a-repluptodatevector.md)                                         | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**報表**](a-directreports.md)                                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**代表-來源**](a-repsfrom.md)                                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**代表**](a-repsto.md)                                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**修訂**](a-revision.md)                                                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**擺脫**](a-rid.md)                                                                         | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-帳戶-名稱**](a-samaccountname.md)                                                 | 是      | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-帳戶-類型**](a-samaccounttype.md)                                                 | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-有效**](a-sdrightseffective.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                             | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**安全性-識別碼**](a-securityidentifier.md)                                          | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**伺服器參考-BL**](a-serverreferencebl.md)                                           | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**顯示位址-書籍**](a-showinaddressbook.md)                                          | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**顯示-內建-僅限視圖**](a-showinadvancedviewonly.md)                               | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**SID-歷程記錄**](a-sidhistory.md)                                                          | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**網站-物件-BL**](a-siteobjectbl.md)                                                     | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**結構物件類別**](a-structuralobjectclass.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**子 Refs**](a-subrefs.md)                                                                | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**補充認證**](a-supplementalcredentials.md)                                | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**系統旗標**](a-systemflags.md)                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**電話號碼**](a-telephonenumber.md)                                                | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**文字編碼或位址**](a-textencodedoraddress.md)                                    | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**權杖群組**](a-tokengroups.md)                                                        | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**權杖-群組-全域和通用**](a-tokengroupsglobalanduniversal.md)                 | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**權杖群組-無-GC-可接受**](a-tokengroupsnogcacceptable.md)                         | 否     | [**安全性-主體**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                               | 否     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**使用者憑證**](a-usercert.md)                                                              | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**使用者-密碼**](a-userpassword.md)                                                      | 否     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**使用者 SMIME-憑證**](a-usersmimecertificate.md)                                     | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-已變更**](a-usnchanged.md)                                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-已建立**](a-usncreated.md)                                                          | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-已移除-最後-Obj**](a-usndsalastobjremoved.md)                                   | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-站間**](a-usnintersite.md)                                                      | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-最後-Obj-Rem**](a-usnlastobjrem.md)                                                  | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**USN-來源**](a-usnsource.md)                                                            | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**Wbem-路徑**](a-wbempath.md)                                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**知名物件**](a-wellknownobjects.md)                                             | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**變更時**](a-whenchanged.md)                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**建立時間**](a-whencreated.md)                                                        | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**WWW-首頁**](a-wwwhomepage.md)                                                       | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**WWW-頁面-其他**](a-url.md)                                                              | 否     | [**返回頁首**](c-top.md)<br/>                                                                                                    |
| [**X509-Cert**](a-usercertificate.md)                                                       | 否     | [**郵件收件者**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2012-extended-rights"></a>Windows Server 2012擴充許可權

這個類別包含 Windows Server 2012 的下列擴充許可權：



| 一般名稱                  |
|------------------------------|
| [**傳送至**](r-send-to.md) |



## <a name="windows-server-2012-validated-writes"></a>Windows Server 2012驗證的寫入

這個類別包含下列 Windows Server 2012 的已驗證寫入：



| 一般名稱                                  |
|----------------------------------------------|
| [**自我成員資格**](r-self-membership.md) |



## <a name="windows-server-2012-property-sets"></a>Windows Server 2012屬性集

這個類別包含下列 Windows Server 2012 的屬性集：



| 一般名稱                                      |
|--------------------------------------------------|
| [**電子郵件-資訊**](r-email-information.md) |



 

 





